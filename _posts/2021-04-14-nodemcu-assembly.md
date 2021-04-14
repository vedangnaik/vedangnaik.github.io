---
layout: post
title: "NodeMCU in Assembly: Following the Train of Thought"
---

About two weeks ago, I finally found enough time to do some serious research into how bootloaders and operating systems worked. However, my chosen resource, the excellent [OSTEP](http://pages.cs.wisc.edu/~remzi/OSTEP/), was simply too theoretical; while its explanations were top-notch, there was little code. So I did some digging, and soon realized why - operating systems needed a surprising amount of hardware support, and the instruction set architecture (ISA) landscape was a nightmare! A learner would quickly miss the point amidst all the `#ifdef`s. But I still wanted some code - its one thing knowing the idea, and another entirely to plant your feet into a mud and make it real. Thus, I decided to look for some open-source kernels. And no, not Linux (or GNU/Linux or whatever). Since I was (and still am) hoping to eventually write my own small kernel and test it on *real* hardware, my poison of choice needed to be carefully selected - it needed to be written for an ISA for which hardware was easily available, and it needed to be small and well-documented enough that reading it wouldn't take years.

My mind first turned to [SerenityOS](TODO); however, I felt that project was too big to easily learn from. Second, I investigated [xv6](TODO), a kernel developed at MIT as a teaching tool (and also mentioned in OSTEP). The kernel had been written in both `RISC-V` and `x86`, but since I wanted real hardware, that wouldn't do - I couldn't find any `RISC-V` boards on Amazon, and the sheer complexity of `x86` put me off. Thus, I finally decided to go with [RPiOS](https://github.com/s-matyukevich/raspberry-pi-os), a GitHub tutorial of sorts which used the Raspberry Pi. I didn't have a Pi however, so I ordered one. While waiting for it, I suddenly remembered,
> Me: Hey, what about that NodeMCU thing? I have one right now! Perhaps I can test out its interrupts or something.

And thus began my quest to program the NodeMCU in assembly. This is a chronicle of my thought process on that journey.



### What's the ISA?

During my brief study of bootloaders et al. I'd decided that **the ISA** is the lowest-level thing I needed to know.

> Me: After all, the processor just executes instructions, right? So, what instructions does the NodeMCU execute? No, first, what's the CPU called?

Googling to the [NodeMCU website](https://www.nodemcu.com/index_en.html#fr_54747361d775ef1a3600000f): *Less than $2 WI-FI **MCU ESP8266** integrated and easy to prototype development kit.* Sure enough, I could see `ESP8266` written on the large silver chip on the PCB.

> Me:  OK, what's the ESP8266 MCU?

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

> Me: Ahh yes, I wanted to play with interrupts on the NodeMCU. What do I need for that? Of course, yes, a set of cross-architecture tools!

I won't pretend that this is the first thought that came to me; in fact, I'd read ahead (or backwards) a bit, and found this *very useful* [StackOverflow answer](https://stackoverflow.com/a/63908556) that had been given by a wise old-timer to another adventurer just like me. But we're getting ahead of ourselves... somewhere along this path, I'd decided to do this in assembly. I don't know why - maybe the `xv6` startup assembly file was mocking me, or perhaps this 'Bare Bones' x86 kernel I'd copy-pasted from [here](https://wiki.osdev.org/Bare_Bones) a few days ago was still on my mind. Anyhow, at this point, my thoughts turned to something I'd done with the NodeMCU many months ago: program it ***in C***, with the ***Arduino IDE***.

> Me: So apparently the tools for programming this thing in C are available via the Arduino folks... let's see if I can get access to them directly this time. There's gotta be a `gcc-cross-something` at least in there.

Anyway, I did some Googling to find a [tutorial](https://create.arduino.cc/projecthub/najad/using-arduino-ide-to-program-nodemcu-33e899) for prepping the IDE to program the NodeMCU. Specifically, this required the installation of 'additional libraries'. I installed it and flashed the *Blink* example to the NodeMCU, and it worked.

> Me: OK good, just like I remember it. So where'd that JSON file get the tools from?

Unfortunately I brain-farted and went back to the Google page instead of reading the JSON, but luckily Google saved me by putting a very enticing GitHub [link](https://github.com/esp8266/Arduino) right below, and for some other strange reason, I followed it.

> Me: * *oblivious* * Oh, excellent! That JSON link is mentioned here as well. I guess this is then the source of the tools then. Let's look for files with `xtensa` in them, for a start...

If you're wondering how I knew what keywords to look for, it's because that SO post mentioned them by name. Alas, it wasn't that easy. It looked like the repo was getting the tools from someplace else on demand, or maybe it was involved at all. Who knows? I don't, for I had given up and, having apparently taken an arrow to the brain, started searching *online* for someone who had the toolchain. I found a few too, and even one package in Fedora's repositories, which I actually also installed even though I knew it wasn't the `xtensa-lx106-elf-*` line of tools I needed... yeah, I don't know. But then,

> Me: Wait a minute: I literally just compiled 'Blink'! That means I must already have the tools! I just have to find where they are installed!
> 
> (*furiously Googling*) W-h-e-r-e d-o-e-s A-r-d-u-i-n-o I-D-E i-n-s-t-a-l-l b-o-a-r-d-s-?

And yeah, they were right there in some folders in `~/arduino15/packages/esp8266/`: a set of `xtensa-lx106-elf-` tools - `gcc, objdump, objcopy, as, ld`, you name it.

Phew!



### Let's write some assembly!

Whoa, not so fast. Let's see if the tools and that SO code actually work. So I followed the instructions there, (including figuring out the cryptic *"I will let you figure that out"* - hint: it's an `esptool.py` command) and sure enough, I got *Blink* back, but this time in just `asm` and pure `C`.

> Me: Alright! Now, let's set some interrupts.

Whoa, not so fast again! I had the tools, but not the knowledge to use them. What are these strange `.text, .data, .globl _start`? What's a `.ld` file?

> Me: Jeez, alright... where do I start with this. OK OK, let's make this simple. Forget the interrupts. Let's just switch the LED on to begin. The code already does that, so that's something to check against. Let's ditch the C, who needs functions anyway. One assembly file => one binary file. Let's start with the assembler, that's the first command in the post...
> 
> Me: By the way, why don't I know this? Did the systems programming and computer organization courses not teach this? (*Checking syllabus*) Hmm, no... that's odd. Covid syllabi cuts, eh?

I Googled for *'gnu assembler tutorial'* and was greeted by a number of links. I decided to go with [this one](https://www.eecs.umich.edu/courses/eecs373/readings/Assembler.pdf) because a friend of mine goes to the University of Michigan. It was over 300 pages long, but I was unfazed - please, I'd scrolled through 700-page ISA documentations! I went directly to the **Assembler Directives** section since I'd just discovered that that's what the `.text, .data,` etc. are called.

> Me: Alright, let's see what this means.
>
> (*a half-hour of reading later*) Wow! That was a really nicely written document! I feel way more comfortable around the SO code now. They'd even put in some notes about the linking process, that's pretty neat!

With my newfound knowledge, I proceeded to forget everything about the linker script and just start slowly transcribing the disassembly of the `C` from the post into my own assembly file. This... took a while - since I hadn't read the rest of that beautiful PDF, I didn't know how `as` was going to translate the assembly into Xtensa assembly, so I spent hours more scrolling around through the Xtensa ISA PDF learning about the various opcodes instead of, you know, just reading the PDF some more. Anyway, I eventually bumbled into the following, in `test.S`:
```c
.text
    .globl _start
    _start:
        # load word at IOMUX_GPIO2 = 0x60000838
        movi a0, 0x60000838 # move address into a0
        l32i a1, a0, 0 # load a1 with word at address
        # AND this with ~(0x130)
        movi a2, ~0x130
        and a1, a1, a2
        # store a0 back into IOMUX
        movi a0, 0x60000838
        s32i a1, a0, 0

        # put 4 into GPIO ENSET = 0x60000310
        movi a0, 0x60000310
        movi a1, 4
        s32i a1, a0, 0

        # put 4 into GPIO OUTSET = 0x60000304
        movi a0, 0x60000308
        movi a1, 4
        s32i a1, a0, 0

        # infinite loop
        loop0:
            j loop0
```
> Me: Lords above and below, that took a while. Let's assemble this and see what it disassembles to, just to see if it works as expected...

The disassembly of the produced `test.o` file:
```bash
$ xtensa-lx106-elf-as --warn --fatal-warnings test.S -o test.o
$ xtensa-lx106-elf-objdump -d test.o

test.o:     file format elf32-xtensa-le


Disassembly of section .literal:

00000000 <.literal>:
   0:   38 08 00 60             
   4:   38 08 00 60             
   8:   10 03 00 60             
   c:   08 03 00 60             

Disassembly of section .text:

00000000 <_start>:
   0:   000001                  l32r    a0, fffc0000 <loop0+0xfffbffe2>
   3:   0018                    l32i.n  a1, a0, 0
   5:   cfae22                  movi    a2, 0xfffffecf
   8:   101120                  and     a1, a1, a2
   b:   000001                  l32r    a0, fffc000c <loop0+0xfffbffee>
   e:   0019                    s32i.n  a1, a0, 0
  10:   000001                  l32r    a0, fffc0010 <loop0+0xfffbfff2>
  13:   410c                    movi.n  a1, 4
  15:   0019                    s32i.n  a1, a0, 0
  17:   000001                  l32r    a0, fffc0018 <loop0+0xfffbfffa>
  1a:   410c                    movi.n  a1, 4
  1c:   0019                    s32i.n  a1, a0, 0

0000001e <loop0>:
  1e:   ffff06                  j       1e <loop0>
```

> Me: What! Where are all the constants? `movi` is 'move immediate', is it not? Why'd it replace that with that weird offset?
>
> (*reading the datasheet once more*) Ahh, I see... yes of course, a 32-bit processor can't take 32-bit immediate values in a 32-bit instruction. So looks like `as` moved those to this `.literal` section implicitly and replaced the instruction with some other load... Damn.

I was feeling quite stupid - but, I told myself, that's what they made the tools for right? Jeez, I didn't have all week, I wanted to get that light on now!! So I quickly put it through `ld` (that converts `.o` to `.elf` files, right?), converted the `.elf` to `.bin`, and then flashed the `.bin` to the NodeMCU. And....... nothing happened.

> Me: ...
>
> Me: Alright, time to sleep.



### Link to fix, please?

> Me: Alright, jeez... where could it be wrong now? *sigh* I guess we'll start with the code. Maybe it's not setting the GPIO correctly...

I thus spent a some more hours digging through the SO code, my disassembly, and the Xtensa datasheet.

> Me: Nada... they all match up pretty much. This looks like it does exactly what it's supposed to. And I know the constants work, they worked that last time, after all...
>
> ...
>
> Me: Wait, they worked once! Let's start from the beginning and check each step of the toolchain. Alright, `as`, check. `gcc`, not required. `ld` che... oh wait! The `.ld` file! That must do something I suppose. Let's add it and see...

And viola! After linking using the file, the light turned on! Mission accomplished, right? Not really. What does the `.ld` thing do? I thought back to what the UMichigan `as` PDF has said: something about linking 'moving sections around' or something. Or maybe someone else said that?

> Me: Moving sections? Why? Do they need to be somewhere else. Hmmm...
> 
> Me: Oh! Yes, yes of course they do! The processor starts executing from a fixed address right? And this program's first instruction needs to be at that address! Perhaps we're loading it too far ahead, or behind the start address entirely, so the PC never gets there! Alright, so what's the start address? Also, how is the copying being done?

In hindsight, the answer the first question is obvious: look in the linker script (what `.ld` files are called), of course! But I didn't, because I got distracted by the second question.

> Me: What could copy files sent over serial into the flash? It has to be a program, right? A program that must be written in assembly that the CPU can execute, a program which must already be someplace the CPU can always access... Of course! A bootloader! There's a bootloader somewhere on that chip! And that's what copies the stuff into flash, and does this, and ....

I had my search phrase: *'boot process'*. We'd somehow come back to the topic I'd started with in the beginning, or maybe it had been there all along. A Google search for  *'esp8266 boot process'* led to [this excellent post](https://richard.burtons.org/2015/05/17/esp8266-boot-process/) by someone named Richard. in but a few paragraphs, they cleared up everything. The start address is `0x40100000`. The extra bytes added by `esptool.py` to the `.elf` files are actually the bootloader headers and ELF sections (I'd originally thought they were some Xtensa opcodes, and spent ages searching through the PDF for matching instructions). And right there in front of me, in the linker script, was that magic value:
```ld
MEMORY
{
    bob : ORIGIN = 0x40100000, LENGTH = 0x1000
    ted : ORIGIN = 0x3FFE8000, LENGTH = 0x1000
}
```

I'm not sure who `bob` and `ted` are, but maybe that's something you can figure out, with your now-functioning (LED) light!



## Conclusion

Well, that's that. If you made it this far, I sincerely thank you for reading! I hope you found this journey across the Internet and the bowels of CPUs entertaining. The end result was massively reduced in scope and massively over time budget, but hey, it works, right?