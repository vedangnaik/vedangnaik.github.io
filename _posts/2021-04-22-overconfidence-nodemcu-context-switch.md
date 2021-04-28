---
layout: post
title: "Overconfidence: Context Switching in NodeMCU"
---

With my exams done and the Raspberry Pi (and associated serial cable, which I forgot to order) delivered, I decided to start my [quest]({% post_url 2021-04-14-tracing-thought-nodemcu-assembly %}) in earnest. I started following Sergey's tutorial, but right away I ran into problems: while the first lesson compiled (and after some firmware tweaks and a longer foray into the linker, again 😐) ran fine, I was finding the process very tedious: one had to repeatedly remove the SD card, mount it, copy the new files, then insert it back into the Pi, and then reboot it and wait around 30 seconds, and all while the Pi itself had to be connected to a separate power supply (the laptop USB didn't seem to be enough). So I thought, *Hey, I've already read the chapters on scheduling right? Why don't I try making a simple scheduler for the NodeMCU? I already know how to program that in assembly, after all...*


### Step 0: Scope

> Me: Hmm, where should I start? I guess I'll keep it simple for now. How about I just have two processes, and I switch between them every time the scheduler runs... That sounds manageable, it shouldn't take me more than a day.

I decided to make two infinite loops with labels `prog0` and `prog1` which increment counters - that seemed straightforward enough.


### Step 1: I'm not doing this in assembly

Well, that was quick, wasn't it? The first thing I needed was a hardware timer to periodically interrupt the running process so that the scheduler could switch to the other one. After Googling to confirm that the NodeMCU did in fact have such a timer, I opened a file to initialize it, and... nothing. I didn't know where to start. Belatedly, I thought back to how I'd gotten the LED to turn on,

> Me: Damn, how'd I do that? Oh yeah, the StackOverflow post told me the magic value... Yikes, I have no idea where he got it from.

At this point, I went through the Xtensa ISA documentation, as well as several other manuals from Espressif about the ESP8266, but got nothing - most of the documents referenced header files, but didn't provide any links. I assumed that I'd have to download either the RTOS SDK or the NON-OS SDK to get these, but that felt like too much work. So I did the next best thing I could think of - I went to the [ESP8266 Core for Arduino repository](https://github.com/esp8266/Arduino). After about an hour of mucking around, I found the magic values used in the LED example, but more importantly, I'd realized something

> Me: Wow, why not just program it in C? These guys have already taken care of the hardware timer and the LEDs and serial printing and whatnot... if I need some assembly I can just inline it into the C, right?

And so I abandoned the pure ASM, for higher ground.



### Step 2: Testing the hardware timer

Following an example online, I initialized the hardware timer to periodically interrupt the main `loop` function and print some stuff (yeah yeah, serial in ISRs is bad, but whatever). I also tested it with some blocking infinite loops to make sure it actually interrupted the processor. So far, so good. (At this point, I had no *idea* of the *sheer girth* of assembly required just to achieve this...)



### Step 3: Overstepping

Now, I had to learn inline assembly. `gcc` very nicely allows you to insert you own assembly at any point into `C` functions, and even has this nice 'Extended ASM' syntax for safely intermixing `C` variables and assembly instructions. While inline assembly sounds like a simple idea (like dude, just put that instruction there, right?), it's not that simple - the compiler is doing tons of rearrangement behind the scenes, and dropping a few instructions into that which may potentially overwrite important registers is a recipe for causing annoying bugs. In fact, my very first foray into inlining was simply replacing a single `digitalWrite(LED_BUILTIN, HIGH)` with the assembly code from last time which turns on the light - this itself caused havoc; I'd overwritten `a0` and `a1`, and these registers are used by Xtensa as the return and stack pointer registers respectively.

Having identified that, however, I was filled with confidence

> Me: This is gonna be easy! Why don't I just implement the entire saving of registers and the program counter right now?

Foolishness. I wasted at least six hours on this. *Six hours*, I say! Because my understanding of the Extended ASM syntax was pretty bad, it took a ton of trial and error to figure this out, and it was mostly for naught, since I'd yet to figure out the key part: **how does one actually switch between processes?**


### Step 4: Ok, now what?

I was weary and tired and had a bad headache, but was still excited. I'd spent the entire day figuring out the context switch assembly, and now (or so I thought), was the finisher: simply *jump into where the other process left off*, and watch the magic happen.

Right?

> Me: Whooo, it jumped! I can die in peace now... Wait, why isn't it jumping back to the first process? Huh? Why isn't the interrupt firing again?? This is a hardware interrupt right, what's going on!

Yeah... turns out the simple `j prog0`ing into an infinite loop from an interrupt service routine makes the interrupt never end - and since interrupt service routines do not interrupt each other (they're queued and handled in turn, sometimes based on priority), the next interrupt was never getting handled. And sure enough, this was confirmed about 6 seconds later as the ever-hungry hardware watchdog timer reset the entire chip 😐

My feelings at this point are a little hard to describe - I felt as though I'd spent ages on a math problem only to realize I'd misread the very first word of the question. It was close to 2AM. My arms were weak, my head was heavy; my control key was acting sketchy.

> Me: Well, I'm out of ideas... I guess I'll just go brush and call it a night. I can't really say this has been a very efficient use of my time, to be honest...


### Step 5: Epiphany

> Me: Wait a second! If all that's needed is for the ISR to return, then why can't I just *change the return address into the new process*?

I got really excited - all I have to do is just change the `a0` register right? That's the one which contains the return address of the `ISR`, after all. Before doing this, I printed out the value of this register inside the ISR just to see, but I didn't actually check it against the disassembly: I was just too excited. I quickly wrote the address of `prog1` into `a0`, and yes, It actually returned straight into `prog1`! Alas, I had started celebrating too early. The ISR never got called again. The processor stayed inside the while loop in `prog1` until the watchdog timer reset it.


## Giving up

At this point, I decided to call it a night. It was well past 2AM, and I felt I'd achieved very little other than giving myself a really bad headache. As I brushed, I spent some time analyzing why - why had I not gotten anywhere? A context switch seemed like a relatively simple task, right? And therein, I realized, lay the problem: I simply hadn't understood it well enough. I'd just fooled myself into thinking that I had. There were just too many parts that I was unclear about. What was the stack doing? Why doesn't changing the return address count as a 'return'? How are my two programs laid out in memory? Is it safe to reset the watchdog timer in the ISR? I didn't know. I'd simply bumbled along from one half-formed idea to the next. At these levels of a processor, that's about as useful as randomly turning a Rubik's cube and hoping to solve it. The computer expected me to know what I was doing, but I didn't. I had to find out first. To that end, I've decided to indefinitely shelve this project and spend more time with OSTEP and Sergey's tutorials. I'll return when I know I'm ready.