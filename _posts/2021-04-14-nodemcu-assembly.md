---
layout: post
title: "NodeMCU in Assembly: Following the Train of Thought"
---

About two weeks ago, I finally found enough time to do some serious research into how bootloaders and operating systems worked. However, my chosen resource, the excellent [OSTEP](http://pages.cs.wisc.edu/~remzi/OSTEP/), was simply too theoretical; while its explanations were top-notch, there was little code. So I did some digging, and soon realized why - operating systems needed a surprising amount of hardware support, and the instruction set architecture (ISA) landscape was a nightmare! A learner would quickly miss the point amidst all the `#ifdef`s. But I still wanted some code - its one thing knowing the idea, and another entirely to plant your feet into a mud and make it real. Thus, I decided to look for some open-source kernels. And no, not Linux (or GNU/Linux or whatever). Since I was (and still am) hoping to eventually write my own small kernel and test it on *real* hardware, my poison of choice needed to be carefully selected - it needed to be written for an ISA for which hardware was easily available, and it needed to be small and well-documented enough that reading it wouldn't take years.

My mind first turned to [SerenityOS](TODO); however, I felt that project was too big to easily learn from. Second, I investigated [xv6](TODO), a kernel developed at MIT as a teaching tool (and also mentioned in OSTEP). The kernel had been written in both `RISC-V` and `x86`, but since I wanted real hardware, that wouldn't do - I couldn't find any `RISC-V` boards on Amazon, and the sheer complexity of `x86` put me off. Thus, I finally decided to go with [RPiOS](https://github.com/s-matyukevich/raspberry-pi-os), a GitHub tutorial of sorts which used the Raspberry Pi. I didn't have a Pi however, so I ordered one. While waiting for it, I suddenly remembered, *'Hey, what about that NodeMCU thing? I have one right now! Perhaps I can test out its interrupts or something'*. And thus began my quest to program the NodeMCU in assembly. This is a chronicle of my thought process on that journey.

### What's the ISA?

During my brief study of bootloaders et al. I'd decided that *the ISA is the lowest-level thing I needed to know*.

> Me: After all, the processor just executes instructions, right? So, what instructions does the NodeMCU execute? No, first, what's the CPU called?

Googling to the [NodeMCU website](https://www.nodemcu.com/index_en.html#fr_54747361d775ef1a3600000f): *Less than $2 WI-FI **MCU ESP8266** integrated and easy to prototype development kit.* Sure enough, I could see `ESP8266` written on the large silver chip on the PCB.

> Me:  Ok, what's the ESP8266 MCU?

Googling to [Espressif's website](https://www.espressif.com/en/products/socs/esp8266)

> Me: Alright alright. I need the processor. Where's the datasheet?

[Located](https://www.espressif.com/sites/default/files/documentation/0a-esp8266ex_datasheet_en.pdf) quickly, by following `Resources -> Documents` and running a search (props to Espressif BTW, their website is so nice): *The ESP8266EX integrates a **Tensilica L106 32-bit RISC** processor...*
> Me: Ah, we're getting somewhere. 'RISC' isn't very specific though, looks like I'll have to check out these Tensilica people...

Googling `Tensilica L106`,
> Me: This company got acquired huh... that'll make this harder. There's an [announcement](https://ip.cadence.com/news/243/330/Tensilica-Unveils-Diamond-Standard-106Micro-Processor-Smallest-Licensable-32-bit-Core) for the processor dated to last year however...
> 
> What? It's originally from 2007!! Anyway, what's the ISA.... Well damn; looks like it's some proprietary thing, I've never heard of this '**Xtensa ISA**' before. I was hoping it'd be ARM or RISC-V or something. This is gonna be a lot harder. Alright * *sigh* *, where's the ISA documentation now?

Going back to the previous Google page, I just happened to notice another link before navigating away: [*Xtensa Instruction Set Architecture (ISA) Reference*](https://0x04.net/~mwk/doc/xtensa.pdf)

> Me: Oh... well, that was easy. Hopefully it's still correct haha, this most certainly isn't an official release by Tensilica or whoever they are now. Anyway, might as well check it out...

I open the PDF, and see it's almost 700 pages long.

> Me: ... Alright, time to sleep.

Mission... accomplished?



### What now? Oh yeah, look for the toolchain

The next day, I took a minute to remind myself why I was spending my time reading 700-page PDFs from 2007.

> Me: Oh yeah, I wanted to play with interrupts on the NodeMCU. What do I need for that? Of course, yes, a set of cross architecture tools!

Somewhere along this path, I decided to do this in assembly. I don't know why - maybe the `xv6` startup assembly file was mocking me, or perhaps this 'Bare Bones' x86 kernel I'd copy-pasted from [here](https://wiki.osdev.org/Bare_Bones) a few days ago was still on my mind. Anyhow, at this point, my mind went to something I'd done with the NodeMCU many months ago: program it ***in C***, with the ***Arduino IDE***.

> Me: So apparently the tools for programming this thing in C are available via the Arduino folks... let's see if I can get access to them directly this time. There's gotta be a `gcc-cross-something` at least in there.

So I did some Googling to find a [tutorial](https://create.arduino.cc/projecthub/najad/using-arduino-ide-to-program-nodemcu-33e899) for prepping the IDE to program the NodeMCU. Specifically, that required the installation of 'additional libraries'. I installed it and flashed the 'Blink' example to the NodeMCU, and it worked.

> Me: Ok good, just like I remember it. So where'd that JSON file get the tools from?

Unfortunately I brain-farted and went back to the Google page instead of reading the JSON, but luckily Google saved me by putting a very enticing GitHub [link](https://github.com/esp8266/Arduino) right below, and for some other strange reason, I followed it.

> Me: *oblivious* Oh, excellent! That JSON link is mentioned here as well. I guess this is then the source of the tools then. Let's look for files with `xtensa` in them, for a start...


