# [C++ links](README.md): x86 Assembly

Note: the main focus is on the 64-bit variant (x86-64): thus, primarily up-to-date materials (i.e., 64-bit, AVX) are preferred.

See also: [Computer Architecture](comparch.md) -- recommended background (which makes the following significantly more approachable) includes at least an undergraduate-level course.

---

# Articles

Assembler relaxation
http://eli.thegreenplace.net/2013/01/03/assembler-relaxation

Displaying all argv in x64 assembly  
http://eli.thegreenplace.net/2013/07/24/displaying-all-argv-in-x64-assembly

Gentle Introduction to x86-64 Assembly
http://www.x86-64.org/documentation/assembly.html

Introduction to x64 Assembly
https://software.intel.com/en-us/articles/introduction-to-x64-assembly

Processor Architecture
https://msdn.microsoft.com/en-us/library/windows/hardware/ff553442%28v=vs.85%29.aspx  
x86-32 and x86-64: Architecture, Instructions, Annotated Disassembly

Redundancy of x86 Machine Code
http://www.strchr.com/machine_code_redundancy

Stack frame layout on x86-64
http://eli.thegreenplace.net/2011/09/06/stack-frame-layout-on-x86-64

The x86 architecture is the weirdo
http://blogs.msdn.com/b/oldnewthing/archive/2004/09/14/229387.aspx

Trivia Questions for X86 Nerds  
http://www.msreverseengineering.com/blog/2015/6/9/x86-trivia-for-nerds  
Discussions:  
https://www.reddit.com/r/ReverseEngineering/comments/39gbxc/trivia_questions_for_x86_nerds/  
https://twitter.com/rolfrolles/status/608789071645691904

Understanding the x64 code models
http://eli.thegreenplace.net/2012/01/03/understanding-the-x64-code-models

Where the top of the stack is on x86  
http://eli.thegreenplace.net/2011/02/04/where-the-top-of-the-stack-is-on-x86

Windows x64 ABI  
Part 1: Intro to the Windows x64 calling convention   
http://www.gamasutra.com/view/news/171088/x64_ABI_Intro_to_the_Windows_x64_calling_convention.php  
Part 2: Stack frames  
http://www.gamasutra.com/view/news/178446/Indepth_Windows_x64_ABI_Stack_frames.php

# Books

- Assembly Language Succinctly
	- 2014; Christopher Rose
	- https://www.syncfusion.com/resources/techportal/details/ebooks/assemblylanguage
- Low-Level Programming
	- 2017; Igor Zhirkov
	- https://www.apress.com/us/book/9781484224021
	- https://github.com/Apress/low-level-programming
- Introduction to 64 Bit Assembly Language Programming for Linux and OS X
	- Ray Seyfarth
	- http://rayseyfarth.com/asm/
- Introduction to Computer Organization with x86-64 Assembly Language & GNU/Linux
	- Robert G. Plantz
	- http://bob.cs.sonoma.edu/IntroCompOrg-x64/book.html
- Modern X86 Assembly Language Programming
	- 2018; Daniel Kusswurm
	- Covers x86 64-bit, AVX, AVX2, and AVX-512
	- https://github.com/Apress/modern-x86-assembly-language-programming-2e
- Understanding Assembly Language
	- a.k.a. Reverse Engineering for Beginners; https://yurichev.com/blog/UAL/
	- https://beginners.re/
- x86-64 Assembly Language Programming with Ubuntu
	- Ed Jorgensen
	- http://www.egr.unlv.edu/~ed/x86.html
- Wikibooks
	- x86 Assembly - https://en.wikibooks.org/wiki/X86_Assembly
	- X86_Assembly: https://en.wikibooks.org/wiki/X86_Disassembly

## 32-bit

- Programming from the Ground Up Book  
	- An introduction to programming using Linux assembly language
	- https://savannah.nongnu.org/projects/pgubook/
	- http://programminggroundup.blogspot.com/
	- Download: http://download.savannah.gnu.org/releases/pgubook/
- PC Assembly Language Tutorial
	- http://web.archive.org/web/20150815073439/http://www.drpaulcarter.com/pcasm/

# Communities

alt.lang.asm
https://groups.google.com/d/forum/alt.lang.asm

comp.lang.asm.x86
https://groups.google.com/d/forum/comp.lang.asm.x86

flat assembler: Message board for the users of flat assembler.
http://board.flatassembler.net/

x86 Assembly Language FAQ Supporting the alt.lang.asm and comp.lang.asm.x86 Newsgroups
http://www.fysnet.net/faq/

/r/asm - where every byte counts
https://www.reddit.com/r/asm

`##asm`, Freenode IRC network
http://goo.gl/vZ4xwd

CS270 x86 Assembly Blog
http://cs270assembly.tumblr.com/

# Courses

- In-Depth: C/C++ Low Level Curriculum  
	- (defunct) http://www.altdevblogaday.com/author/alex-darby/
	- original location down; various mirrors available (follow the links to the previous parts):  
	- https://web.archive.org/web/20130810050325/http://www.altdevblogaday.com/author/alex-darby/  
	- https://www.gamasutra.com/search/?search_text=Alex+Darby
	- http://jahej.com/alt/2013_05_22_cc-low-level-curriculum-part-12-multiple-inheritance.html  

NASM Assembly Language Tutorials - asmtutor.com  
http://asmtutor.com/

Introductory Intel x86: Architecture, Assembly, Applications, & Alliteration  
http://opensecuritytraining.info/IntroX86.html  
YouTube: https://www.youtube.com/playlist?list=PL038BE01D3BAEFDB0

Intermediate Intel x86: Architecture, Assembly, Applications, & Alliteration  
http://opensecuritytraining.info/IntermediateX86.html  
YouTube: https://www.youtube.com/playlist?list=PL8F8D45D6C1FFD177

Introduction To Reverse Engineering Software  
http://opensecuritytraining.info/IntroductionToReverseEngineering.html  
YouTube: https://www.youtube.com/playlist?list=PL416CEDF4A931DB0D

Learning assembly for linux-x64
https://github.com/0xAX/asm
https://0xax.github.io/categories/assembly/

# Links

Assembly Language (x86) Resources
http://grail.cba.csuohio.edu/~somos/asmx86.html

Useful assembly links
http://www.agner.org/optimize/#links

# References

Agner Fog: Software optimization resources  
http://www.agner.org/optimize/  
1. Optimizing software in C++: An optimization guide for Windows, Linux and Mac platforms  
http://www.agner.org/optimize/optimizing_cpp.pdf  
2. Optimizing subroutines in assembly language: An optimization guide for x86 platforms  
http://www.agner.org/optimize/optimizing_assembly.pdf  
3. The microarchitecture of Intel, AMD and VIA CPUs: An optimization guide for assembly programmers and compiler makers  
http://www.agner.org/optimize/microarchitecture.pdf  
4. Instruction tables: Lists of instruction latencies, throughputs and micro-operation breakdowns for Intel, AMD and VIA CPUs  
http://www.agner.org/optimize/instruction_tables.pdf  
5. Calling conventions for different C++ compilers and operating systems  
http://www.agner.org/optimize/calling_conventions.pdf

AMD64 Application Binary Interface (ABI)  
http://www.x86-64.org/documentation.html  
http://www.x86-64.org/documentation_folder/abi.pdf

Assembly Optimization Tips
http://mark.masmcode.com/

Assembler x86 (FPU, MMX, SSE, SSE2, SSE3, SSSE3, SSE4, AVX, AVX2, AVX512)  
http://wm.ite.pl/articles/#assembler-x86-fpu-mmx-sse-sse2-sse3-ssse3-sse4-avx-avx2-avx512-new

Brennan's Guide to Inline Assembly  
http://www.delorie.com/djgpp/doc/brennan/brennan_att_inline_djgpp.html  
AT&T/UNIX syntax <-> Intel syntax

Chess Programming Wiki - Hardware: x86-64  
https://chessprogramming.wikispaces.com/x86-64

CPU: Intel® 64 and IA-32 Architectures Software Developer Manuals  
https://www-ssl.intel.com/content/www/us/en/processors/architectures-software-developer-manuals.html

CPU: Developer Guides, Manuals & ISA Documents  
http://developer.amd.com/resources/documentation-articles/developer-guides-manuals/

GCC-Inline-Assembly-HOWTO  
http://www.ibiblio.org/gferg/ldp/GCC-Inline-Assembly-HOWTO.html

Instruction latencies and throughput for AMD and Intel x86 processors  
https://gmplib.org/~tege/x86-timing.pdf

Inline assembly for x86 in Linux  
http://www.ibm.com/developerworks/linux/library/l-ia/

Inline assembly (linux-insides)  
https://0xax.gitbooks.io/linux-insides/content/Theory/asm.html

Intel Intrinsics Guide  
https://software.intel.com/sites/landingpage/IntrinsicsGuide/

Linux Assembly HOWTO  
http://asm.sourceforge.net/howto.html

OS Development Wiki  
http://wiki.osdev.org/

sandpile.org -- "The world's leading source for technical x86 processor information"  
http://www.sandpile.org/

Stack Overflow: 'x86' tag wiki  
https://stackoverflow.com/tags/x86/info

Stack Overflow: Documentation - Intel x86 Assembly Language & Microarchitecture  
http://stackoverflow.com/documentation/x86/topics

The Minimal 80x86 Instruction Set  
http://www.plantation-productions.com/Webster/www.writegreatcode.com/Vol2/wgc2_OA.pdf  
Appendix A of Write Great Code, Volume 2: https://www.nostarch.com/greatcode2.htm

The Netwide Assembler: NASM  
Chapter 11: Writing 64-bit Code (Unix, Win64)  
http://www.nasm.us/xdoc/2.11.09rc1/html/nasmdo11.html  
Links to the latest versions: http://www.nasm.us/docs.php

Wikipedia: x86 assembly topics  
https://en.wikipedia.org/wiki/Template:X86_assembly_topics

x86 Encoding Cheat Sheet  
https://www.akkadia.org/drepper/x86-opcode-structure.pdf

x86 Instruction Set Reference  
http://felixcloutier.com/x86/  
https://github.com/zneak/x86doc

x86 intrinsics cheat sheet  
A cheat sheet containing most x86 intrinsics, like SSE and AVX intrinsics, grouped in an intuitive fashion  
http://www3.in.tum.de/~finis/  
http://www3.in.tum.de/~finis/x86-intrin-cheatsheet-v2.2.pdf

x86, x64 Instruction Latency, Memory Latency and CPUID dumps  
http://users.atw.hu/instlatx64/

x86_64 NASM Assembly Quick Reference ("Cheat Sheet")  
https://www.cs.uaf.edu/2010/fall/cs301/support/x86_64/index.html

X86-64 Instruction Encoding  
http://wiki.osdev.org/X86-64_Instruction_Encoding

X86 Opcode and Instruction Reference  
http://ref.x86asm.net/

x86 Opcode Structure and Instruction Overview  
http://net.cs.uni-bonn.de/fileadmin/user_upload/plohmann/x86_opcode_structure_and_instruction_overview.pdf
 
x86 oddities  
http://x86.corkami.com 

## Slides

* Assembly: The mother of all languages - https://speakerdeck.com/takipiadmin/assembly-the-mother-of-all-languages
* Creating a language using only assembly language
  - https://speakerdeck.com/nineties/creating-a-language-using-only-assembly-language
  - https://github.com/nineties/amber
* Intro to x64 Reversing - Jon Larimer - SummerCon 2011
  - http://acmvm2.srv.mst.edu/wp-content/uploads/2014/07/Intro-to-x64-Reversing-Larimer-2011.pdf
  - http://codetastrophe.com/SummerCon%202011%20-%20Intro%20to%20x64%20Reversing.pdf
* x86 Assembly Primer for C Programmers
  - https://speakerdeck.com/vsergeev/x86-assembly-primer-for-c-programmers
  - https://github.com/vsergeev/apfcp

## Software

* Compiler Explorer: an interactive compiler
  - https://gcc.godbolt.org/
  - https://github.com/mattgodbolt/gcc-explorer
* Intel XED: The X86 Encoder Decoder
  - https://intelxed.github.io/
  - https://github.com/intelxed
* M/o/Vfuscator - the single instruction C compiler - https://github.com/xoreaxeaxeax/movfuscator
* Radare2
  - Radare project started as a forensics tool, a scriptable commandline hexadecimal editor able to open disk files, but later support for analyzing binaries, disassembling code, debugging programs, attaching to remote gdb servers, etc.
  - http://rada.re/
  - https://github.com/radare/radare2
* Remill: Machine code to LLVM binary translator
  - Remill is a static binary translator that translates machine code into LLVM bitcode. It translates x86 and amd64 machine code (including AVX and AVX512) into LLVM bitcode.
  - https://github.com/trailofbits/remill
* Run Nasm x86/x64 Assembly Code Online - https://dbgr.cc/l/nasm
* SASM: Simple crossplatform IDE for NASM, MASM, GAS, FASM assembly languages - https://dman95.github.io/SASM/english.html
* STOKE - a stochastic optimizer for x86_64 assembly
  - https://github.com/StanfordPL/stoke
  - http://stoke.stanford.edu/
  + Talks:
    - STOKE: Search-Based Compiler Optimization - Alex Aiken (2016) - https://www.youtube.com/watch?v=rZFeTTFp7x4
    - Stochastic Optimization for x86 Binaries - Eric Schkufza (2015) - https://www.youtube.com/watch?v=aD9mZDJzb58

### Assemblers

Assemblers - https://en.wikipedia.org/wiki/Comparison_of_assemblers#x86_assemblers

* FASM (flat assembler) - http://flatassembler.net/
* GNU Assembler (as) - https://sourceware.org/binutils/docs/as/
* Keystone assembler framework
  - Core (Arm, Arm64, Hexagon, Mips, PowerPC, Sparc, SystemZ & X86) + bindings
  - http://www.keystone-engine.org
  - https://github.com/keystone-engine/keystone
* NASM (The Netwide Assembler) - http://www.nasm.us/
* Yasm
  - http://yasm.tortall.net/
  - https://github.com/yasm/yasm

### Disassemblers

* Capstone disassembly/disassembler framework
  - Core (Arm, Arm64, Mips, PPC, Sparc, SystemZ, X86, X86_64, XCore) + bindings (Python, Java, Ocaml)
  - http://www.capstone-engine.org/
  - https://github.com/aquynh/capstone
* disasm: Interactive Disassembler GUI
  - Optional Intel Architecture Code Analyzer (IACA) integration
  - https://github.com/mongodb-labs/disasm
* diStorm3 binary stream disassembler library project
  - Disassembler Library For x86/AMD64: "diStorm3 is really a decomposer, which means it takes an instruction and returns a binary structure which describes it rather than static text, which is great for advanced binary code analysis."
  - https://github.com/gdabah/distorm
  - https://github.com/gdabah/distorm/wiki
* EmilPRO
  - EmilPRO is a graphical disassembler for a large number of instruction sets. It's a reimplementation and replacement for the Dissy disassembler.
  - http://www.emilpro.com/
  - https://github.com/SimonKagstrom/emilpro
* Medusa: An open source interactive disassembler
  - https://github.com/wisk/medusa
* Panopticon - A Libre Cross Platform Disassembler
  - https://github.com/das-labor/panopticon
* Plasma is an interactive disassembler for x86/ARM/MIPS. It can generates indented pseudo-code with colored syntax.
  - https://github.com/plasma-disassembler/plasma
  - Interactive disassembler for x86/ARM/MIPS. Generates indented pseudo-code with colored syntax code. 
* Udis86: Disassembler Library for x86 and x86-64
  - https://github.com/vmt/udis86
* Zyan Disassembler Engine (Zydis)
  - Fast and lightweight x86/x86-64 disassembler library.
  - https://github.com/zyantific/zyan-disassembler-engine

### Network

* asmttpd: Web server for Linux written in amd64 assembly.
  - https://github.com/nemasu/asmttpd
* HeavyThing x86_64 assembly language library and showcase programs
  - rwasa web server (bundled with the HeavyThing library): https://2ton.com.au/rwasa/
  - https://2ton.com.au/HeavyThing/
* SERVASM: Your other webserver
  - Literate webserver in assembler.
  - https://zarkzork.com/servasm.html
  - https://github.com/zarkzork/servasm

---

# Videos

## Tutorials

- Bluff your way in x64 assembler
	- ACCU 2017; Roger Orr
	- https://www.youtube.com/watch?v=RI7VL-g6J7g
- Deeper Dive: x86 32/64 Assembly
	- University of Cincinnati Malware Analysis Class (CS7038): Wk06 (2017)
	- https://www.youtube.com/watch?v=JiC0TnYtXXU
	- http://class.malware.re/2017/02/14/asm-crash-course-2.html
- Enough x86 Assembly to Be Dangerous
	- CppCon 2017; Charles Bailey
	- https://www.youtube.com/watch?v=IfUPkUAEwrk
- Intro to x86 Assembly Language - Davy Wybiral
	- https://www.youtube.com/playlist?list=PLmxT2pVYo5LB5EzTPZGfFN0c2GDiSXgQe
	- https://github.com/code-tutorials/assembly-intro
- Introduction to x86 Assembly
	- Derbycon 2018; DazzleCatDuo (Christopher Domas & Stephanie Domas)
	- https://www.youtube.com/watch?v=Ea6yt3SP3y4
	- http://www.irongeek.com/i.php?page=videos/derbycon8/mainlist
- Intro to Reverse Engineering and Debugging with Radare2
	- Chris James
	- https://www.youtube.com/watch?v=LAkYW5ixvhg
	- https://docs.google.com/presentation/d/1vJWsVZnpD25jqLQWeLvDXZSD2MMM5_tyBAqfWnaIx-c/
- Just enough Assembly for Compiler Explorer - Anders Schau Knatten
	- NDC TechTown 2019
	- https://www.youtube.com/watch?v=soeFwz0cOqU
- Linux x64 Assembly   
	- https://www.youtube.com/playlist?list=PLKK11Ligqiti8g3gWRtMjMgf1KoKDOvME
- Modern x64 Assembly
	- https://www.youtube.com/playlist?list=PLKK11Ligqitg9MOX3-0tFT1Rmh3uJp7kA
	- http://web.archive.org/web/20170110154539/http://www.whatsacreel.net76.net/asmtutes.html
- Practical x64 Assembly and C++ Tutorials  
	- https://youtube.com/playlist?list=PL0C5C980A28FEE68D  
	- Slides: http://www.whatsacreel.net76.net/asmtutes.html
- x64 Assembly Multithreading   
	- https://youtube.com/playlist?list=PLKK11LigqithTIZFLTXu7jUB2IvErM_nH
- x86_64 Linux Assembly
	- https://www.youtube.com/playlist?list=PLetF-YjXm-sCH6FrTz4AQhfH6INDQvQSn
- x86-64 Lite for Compiler Writers
	- Hal Perkins
	- https://www.youtube.com/watch?v=jmbBIYdjN2E
	- Slides: https://courses.cs.washington.edu/courses/csep501/16wi/calendar/lecturelist.html

## 2018

- Hardware Backdoors in x86 CPUs
	- Black Hat 2018; Christopher Domas
	- https://www.youtube.com/watch?v=_eSAF_qT_FY
	- https://github.com/xoreaxeaxeax/rosenbridge
- Inside the AMD Microcode ROM
	- 35C3 (2018)
	- https://www.youtube.com/watch?v=W3FbTMqYi4U
	- https://media.ccc.de/v/35c3-9614-inside_the_amd_microcode_rom

## 2017

- Assembly Language is Too High Level
	- DEF CON 25; XlogicX
	- https://www.youtube.com/watch?v=eunYrrcxXfw
	- https://media.defcon.org/DEF%20CON%2025/DEF%20CON%2025%20presentations/DEFCON-25-XlogicX-Assembly-Language-Is-Too-High-Level.pdf
	- Interactive Redundant Assembler (shell)
		- https://github.com/XlogicX/irasm
- Breaking the x86 Instruction Set
	- Christopher Domas
	- sandsifter
		- https://github.com/xoreaxeaxeax/sandsifter
		- sandsifter-tests: A repository of result for runs of sandsifter on various x86 CPU's
			- https://github.com/rigred/sandsifter-tests
	- Black Hat 2017
		- https://www.youtube.com/watch?v=KrksBdWcZgQ
		- https://www.blackhat.com/docs/us-17/thursday/us-17-Domas-Breaking-The-x86-Instruction-Set-wp.pdf
		- https://www.blackhat.com/docs/us-17/thursday/us-17-Domas-Breaking-The-x86-ISA.pdf
	- DEF CON 25
		- https://www.youtube.com/watch?v=ajccZ7LdvoQ
		- https://media.defcon.org/DEF%20CON%2025/DEF%20CON%2025%20presentations/DEFCON-25-Christopher-Domas-Breaking-The-x86-ISA-UPDATED.pdf
		- https://media.defcon.org/DEF%20CON%2025/DEF%20CON%2025%20presentations/DEFCON-25-Christopher-Domas-Breaking-The-x86-ISA.pdf
- Compiling C to printable x86, to make an executable research paper
	- Tom 7
	- https://www.youtube.com/watch?v=LA_DrBwkiJA
	- http://www.cs.cmu.edu/~tom7/abc/
	- http://www.cs.cmu.edu/~tom7/abc/paper.pdf
- Everything you want to know about x86 microcode, but might have been afraid to ask
	- 34C3 (2017); Benjamin Kollenda and Philipp Koppe 
	- An introduction into reverse-engineering x86 microcode and writing it yourself
	- https://media.ccc.de/v/34c3-9058-everything_you_want_to_know_about_x86_microcode_but_might_have_been_afraid_to_ask
	- https://events.ccc.de/congress/2017/Fahrplan/events/9058.html
- POP POP RETN ; An Introduction to Writing Win32 Shellcode
	- Derbycon 2017; Christopher Maddalena
	- http://www.irongeek.com/i.php?page=videos/derbycon7/t313-pop-pop-retn-an-introduction-to-writing-win32-shellcode-christopher-maddalena
- reductio [ad absurdum]
	- Shakacon 2017; Christopher Domas 
	- https://www.slideshare.net/Shakacon/reductio-ad-absurdum-78575394
	- https://www.youtube.com/watch?v=NmWwRmvjAE8
	- An exploration of code homeomorphism: all programs can be reduced to the same instruction stream.
		- https://github.com/xoreaxeaxeax/reductio
- Reverse Engineering x86 Processor Microcode
	- USENIX Security '17
	- Philipp Koppe, Benjamin Kollenda, Marc Fyrbiak, Christian Kison, Robert Gawlik, Christof Paar, and Thorsten Holz
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/koppe
	- https://www.youtube.com/watch?v=I6dQfnb3y0I
	- https://github.com/RUB-SysSec/Microcode
	- Slides: https://www.usenix.org/sites/default/files/conference/protected-files/usenixsecurity17_slides_koppe.pdf
	- PDF: https://www.usenix.org/system/files/conference/usenixsecurity17/sec17-koppe.pdf
	- European Coreboot Conference (ECC) 2017 - https://www.youtube.com/watch?v=6-NFcC8yOXo

## 2016

- An In-Depth Analysis of Disassembly on Full-Scale x86/x64 Binaries
	- USENIX Security 2016
	- https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/andriesse
	- https://www.vusec.net/projects/disassembly/
- Causes of Performance Instability due to Code Placement in X86
	- 2016 LLVM Developers’ Meeting; Zia Ansari
	- https://www.youtube.com/watch?v=IX16gcX4vDQ
	- http://llvm.org/devmtg/2016-11/Slides/Ansari-Code-Alignment.pdf
- Debugging Optimized x64 Code
	- 2016; Jorge L. Rodríguez
	- https://www.youtube.com/watch?v=MUNRvqpske0
- Improving LLVM Generated Code Size for X86 Processors
	- 2016 EuroLLVM Developers' Meeting; Zia Ansari & David Kreitzer
	- https://www.youtube.com/watch?v=yHexQSFud3w
	- http://llvm.org/devmtg/2016-03/Presentations/X86CodeSizePDF.pdf
- Movfuscator Be Gone
	- REcon 2016
	- Julian Kirsch, Clemens Jonischkeit
	- https://www.youtube.com/watch?v=d_R8i0dVBsQ
	- https://github.com/kirschju/demovfuscator
	- https://recon.cx/2016/talks/%22Movfuscator-Be-Gone.html
	- https://infocon.org/cons/REcon/REcon%202016/video/recon2016-20-julian-kirsch-clemens-jonischkeit-Movfuscator-Be-Gone.mp4
- Programming an x64 compiler from scratch
	- 2016; Per Vognsen
	- part 1 - https://www.youtube.com/watch?v=N9B2KeAWXgE
	- part 2 - https://www.youtube.com/watch?v=Mx29YQ4zAuM
	- part 3 - https://www.youtube.com/watch?v=olSZ0d-nksE

## 2015

- Repsych: Psychological Warfare in Reverse Engineering
	- DEF CON 23 (2015); Chris Domas
	- https://www.youtube.com/watch?v=HlUe0TUHOIc
	- https://github.com/xoreaxeaxeax/REpsych
- The Memory Sinkhole - Unleashing An X86 Design Flaw Allowing Universal Privilege Escalation
	- Black Hat 2015
	- https://www.youtube.com/watch?v=lR0nh-TdpVg
- The M/o/Vfuscator - Turning 'mov' into a soul-crushing RE nightmare
	- Derbycon 2015; Christopher Domas
	- https://www.youtube.com/watch?v=R7EEoWg6Ekk
	- http://www.irongeek.com/i.php?page=videos/derbycon5/break-me00-the-movfuscator-turning-mov-into-a-soul-crushing-re-nightmare-christopher-domas
	- REcon 2015
		- https://www.youtube.com/watch?v=2VF_wPkiBJY
- When hardware must „just work“ - An inside look at x86 CPU design
	- 32C3 (2015)
	- https://www.youtube.com/watch?v=e2vPp0fQUkM
	- https://media.ccc.de/v/32c3-7171-when_hardware_must_just_work
	- Slides: https://events.ccc.de/congress/2015/Fahrplan/system/event_attachments/attachments/000/002/801/original/When_HW_must_just_work_--_FINAL.pdf
	- https://lab.dsst.io/32c3-slides/7171.html

## 2014

- x86 instruction encoding and the nasty hacks we do in the kernel  
	- SUSE Labs Conference 2014; Borislav Petkov
	- https://www.youtube.com/watch?v=CUAXCeRjw3c  
	- Slides: http://www.slideshare.net/ennael/kr2014-x86instructions
- x86 Internals for Fun and Profit
	- GOTO 2014; Matt Godbolt
	- https://www.youtube.com/watch?v=hgcNM-6wr34
	- Slides: http://gotocon.com/dl/goto-chicago-2014/slides/MattGodbolt_X86InternalsForFunAndProfit.pdf

## 2013

- Beyond MOV ADD XOR -- the unusual and unexpected in x86
	- 2013; Gynvael Coldwind, Mateusz "j00ru" Jurczyk
	- https://www.youtube.com/watch?v=WufyCW3j3DE
- Page Fault Liberation Army or Gained in Translation: a history of creative x86 virtual memory uses
	- 2013 - #HITB2013AMS D1T1; Sergey Bratus, Julian Bangert
	- https://www.youtube.com/watch?v=vqj3xCATeqQ
	- http://conference.hitb.org/hitbsecconf2013ams/materials/D1T1%20-%20Sergey%20Bratus%20and%20Julian%20Bangert%20-%20Better%20Security%20Through%20Creative%20x86%20Trapping.pdf
- The Page-Fault Weird Machine: Lessons in Instruction-less Computation
	- USENIX Workshop on Offensive Technologies (WOOT) 2013
	- Julian Bangert, Sergey Bratus, Rebecca Shapiro, Sean W. Smith, Dartmouth College
	- https://www.youtube.com/watch?v=YFGwZA_4URg

## 2012

- Page Fault Liberation Army or Gained in Translation a history of creative x86 virtual memory uses
	- 29c3 (2012)
	- https://media.ccc.de/v/29c3-5265-en-page_fault_liberation_army_h264

## 2011

- Such a weird processor - messing with x86 opcodes (and a little bit of PE...)  
	- `#days` 2011; Ange Albertini
	- https://www.youtube.com/watch?v=MJvsshovITE  
	- https://code.google.com/p/corkami/wiki/hashdays2011  
	- x86 & PE: https://speakerdeck.com/ange/x86-and-pe  
	- Slides: http://www.slideshare.net/ange4771/such-a-weird-processor-messing-with-opcodes-and-a-little-bit-of-pe
