# [C++ links](README.md): x86 Assembly

Note: the main focus is on the 64-bit variant (x86-64): thus, primarily up-to-date materials (i.e., 64-bit, AVX) are preferred.

Note: see [Computer Architecture](comparch.md) -- recommended background (which makes the following significantly more approachable) includes at least an undegraduate-level course.

## Why?

C++ is often used for systems programming; in these contexts (and even if you're just plain curious), there are plenty of reasons to familiarize oneself with assembly language:
- debugging (e.g., no source code available)
- optimization assessment (e.g., examining SIMD use)
- object model (e.g., how are virtual functions implemented -- what do [vtbl and vptr](https://en.wikipedia.org/wiki/Virtual_method_table) compile to)
- [understanding](https://software.intel.com/en-us/articles/implementing-scalable-atomic-locks-for-multi-core-intel-em64t-and-ia32-architectures) concurrency and synchronization primitives (e.g., [atomic instructions](http://wiki.osdev.org/Atomic_operation) -- e.g., CMPXCHG with LOCK prefix, XCHG)

# x86(-64)

## Articles

Assembler relaxation
http://eli.thegreenplace.net/2013/01/03/assembler-relaxation

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

Why Intel Added the CLWB and PCOMMIT Instructions
http://danluu.com/clwb-pcommit/

Windows x64 ABI  
Part 1: Intro to the Windows x64 calling convention   
http://www.gamasutra.com/view/news/171088/x64_ABI_Intro_to_the_Windows_x64_calling_convention.php  
Part 2: Stack frames  
http://www.gamasutra.com/view/news/178446/Indepth_Windows_x64_ABI_Stack_frames.php

## Books

Assembly Language Succinctly  
https://www.syncfusion.com/resources/techportal/details/ebooks/assemblylanguage

Introduction to 64 Bit Assembly Language Programming   
(Two versions: "Linux and OS X" and Windows)  
http://rayseyfarth.com/asm/  
http://rayseyfarth.com/asm/purchase.html

Introduction to Computer Organization with x86-64 Assembly Language & GNU/Linux  
http://bob.cs.sonoma.edu/

Modern X86 Assembly Language Programming: 32-bit, 64-bit, SSE, and AVX  
https://www.apress.com/9781484200650

PC Assembly Language Tutorial
http://www.drpaulcarter.com/pcasm/

Programming from the Ground Up Book  
An introduction to programming using Linux assembly language  
https://savannah.nongnu.org/projects/pgubook/  
http://programminggroundup.blogspot.com/  
Download: http://download.savannah.gnu.org/releases/pgubook/

Reverse Engineering for Beginners  
http://beginners.re/

Wikibooks: x86 Assembly
https://en.wikibooks.org/wiki/X86_Assembly

Wikibooks: https://en.wikibooks.org/wiki/X86_Disassembly

## Communities

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

## Courses

In-Depth: C/C++ Low Level Curriculum  
(defunct) http://www.altdevblogaday.com/author/alex-darby/  
original location down; various mirrors available (follow the links to the previous parts):  
http://altdevblog.com/2011/11/09/a-low-level-curriculum-for-c-and-c/  
http://altdevblog.com/?s=Alex+Darby  
http://altdevblog.com/2013/05/22/cc-low-level-curriculum-part-12-multiple-inheritance/  
http://altdevblog.com/2011/10/25/why-i-became-an-educator/  
http://altdevblog.com/2011/11/09/a-low-level-curriculum-for-c-and-c/  
http://altdevblog.com/2011/11/24/c-c-low-level-curriculum-part-2-data-types/  
https://web.archive.org/web/20130810050325/http://www.altdevblogaday.com/author/alex-darby/  
http://www.gamasutra.com/view/news/184430/InDepth_CC_Low_Level_Curriculum_Part_10_User_Defined_Types.php  
http://jahej.com/alt/2013_05_22_cc-low-level-curriculum-part-12-multiple-inheritance.html  
https://web.archive.org/web/20130810043026/http://www.altdevblogaday.com/2013/01/05/cc-low-level-curriculum-part-10-user-defined-types/

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

## Links

Assembly Language (x86) Resources
http://grail.cba.csuohio.edu/~somos/asmx86.html

Useful assembly links
http://www.agner.org/optimize/#links

## References

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

Intel Intrinsics Guide  
https://software.intel.com/sites/landingpage/IntrinsicsGuide/

Linux Assembly HOWTO  
http://asm.sourceforge.net/howto.html

sandpile.org -- "The world's leading source for technical x86 processor information"  
http://www.sandpile.org/

The Minimal 80x86 Instruction Set  
http://www.plantation-productions.com/Webster/www.writegreatcode.com/Vol2/wgc2_OA.pdf  
Appendix A of Write Great Code, Volume 2: https://www.nostarch.com/greatcode2.htm

The Netwide Assembler: NASM  
Chapter 11: Writing 64-bit Code (Unix, Win64)  
http://www.nasm.us/xdoc/2.11.09rc1/html/nasmdo11.html  
Links to the latest versions: http://www.nasm.us/docs.php

Wikipedia: x86 assembly topics  
https://en.wikipedia.org/wiki/Template:X86_assembly_topics

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

Assembly: The mother of all languages  
https://speakerdeck.com/takipiadmin/assembly-the-mother-of-all-languages

Creating a language using only assembly language  
https://speakerdeck.com/nineties/creating-a-language-using-only-assembly-language  
https://github.com/nineties/amber

x86 Assembly Primer for C Programmers  
https://speakerdeck.com/vsergeev/x86-assembly-primer-for-c-programmers  
https://github.com/vsergeev/apfcp

## Software

Assemblers  
https://en.wikipedia.org/wiki/Comparison_of_assemblers#x86_assemblers

Capstone disassembly/disassembler framework  
Core (Arm, Arm64, Mips, PPC, Sparc, SystemZ, X86, X86_64, XCore) + bindings (Python, Java, Ocaml)  
http://www.capstone-engine.org/

disasm: Interactive Disassembler GUI  
Optional Intel Architecture Code Analyzer (IACA) integration  
https://github.com/mongodb-labs/disasm

EmilPRO  
EmilPRO is a graphical disassembler for a large number of instruction sets. It's a reimplementation and replacement for the Dissy disassembler.  
http://www.emilpro.com/  
https://github.com/SimonKagstrom/emilpro

GCC Explorer: an interactive compiler  
https://gcc.godbolt.org/  
https://github.com/mattgodbolt/gcc-explorer

HeavyThing x86_64 assembly language library and showcase programs  
https://2ton.com.au/HeavyThing/  
rwasa web server (bundled with the HeavyThing library): https://2ton.com.au/rwasa/

Intel XED: The X86 Encoder Decoder  
https://intelxed.github.io/  
https://github.com/intelxed

Radare2  
http://rada.re/  
https://github.com/radare/radare2  
Radare project started as a forensics tool, a scriptable commandline hexadecimal editor able to open disk files, but later support for analyzing binaries, disassembling code, debugging programs, attaching to remote gdb servers, etc.

Remill: Machine code to LLVM binary translator  
https://github.com/trailofbits/remill  
Remill is a static binary translator that translates machine code into LLVM bitcode. It translates x86 and amd64 machine code (including AVX and AVX512) into LLVM bitcode.

Run Nasm x86/x64 Assembly Code Online  
https://dbgr.cc/l/nasm

SASM: Simple crossplatform IDE for NASM, MASM, GAS, FASM assembly languages  
https://dman95.github.io/SASM/english.html

SERVASM: Your other webserver  
Literate webserver in assembler.  
https://zarkzork.com/servasm.html  
https://github.com/zarkzork/servasm

STOKE - a stochastic optimizer for x86_64 assembly  
https://github.com/StanfordPL/stoke-release  
http://stoke.stanford.edu/  
Google Tech Talk: https://www.youtube.com/watch?v=aD9mZDJzb58

Udis86: Disassembler Library for x86 and x86-64  
https://github.com/vmt/udis86

Zyan Disassembler Engine (Zydis)  
Fast and lightweight x86/x86-64 disassembler library.  
https://github.com/zyantific/zyan-disassembler-engine

## Videos

An In-Depth Analysis of Disassembly on Full-Scale x86/x64 Binaries  
https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/andriesse  
https://www.vusec.net/projects/disassembly/

Assembly Language Programming   
https://www.youtube.com/playlist?list=PLPedo-T7QiNsIji329HyTzbKBuCAHwNFC  
http://www.rasmurtech.com/free-online-video-classes/programming/assembly-programming-tutorial/

Borislav Petkov: x86 instruction encoding and the nasty hacks we do in the kernel  
https://www.youtube.com/watch?v=CUAXCeRjw3c  
Slides: http://www.slideshare.net/ennael/kr2014-x86instructions

Linux x64 Assembly   
https://www.youtube.com/playlist?list=PLKK11Ligqiti8g3gWRtMjMgf1KoKDOvME

Practical x64 Assembly and C++ Tutorials  
https://youtube.com/playlist?list=PL0C5C980A28FEE68D  
Slides: http://www.whatsacreel.net76.net/asmtutes.html

Such a weird processor - messing with x86 opcodes (and a little bit of PE...)  
https://www.youtube.com/watch?v=MJvsshovITE  
https://code.google.com/p/corkami/wiki/hashdays2011  
x86 & PE: https://speakerdeck.com/ange/x86-and-pe  
Slides: http://www.slideshare.net/ange4771/such-a-weird-processor-messing-with-opcodes-and-a-little-bit-of-pe

x64 Assembly Multithreading   
https://youtube.com/playlist?list=PLKK11LigqithTIZFLTXu7jUB2IvErM_nH

x86 Internals for Fun and Profit - Matt Godbolt  
https://www.youtube.com/watch?v=hgcNM-6wr34  
Slides: http://gotocon.com/dl/goto-chicago-2014/slides/MattGodbolt_X86InternalsForFunAndProfit.pdf
