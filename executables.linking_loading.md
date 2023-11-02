# [C++ links](README.md): Executables - Linking and Loading

See also:

- [Building](https://github.com/MattPD/cpplinks/blob/master/building.md)
- [Compilers](https://github.com/MattPD/cpplinks/blob/master/compilers.md)
- [Executables](executables.md) - executable & object file formats ([DLL](https://github.com/MattPD/cpplinks/blob/master/executables.md#dll), [ELF](https://github.com/MattPD/cpplinks/blob/master/executables.md#elf), [Mach-O](https://github.com/MattPD/cpplinks/blob/master/executables.md#mach-o), [PE](https://github.com/MattPD/cpplinks/blob/master/executables.md#pe)); debugging data formats ([DWARF](https://github.com/MattPD/cpplinks/blob/master/executables.md#dwarf), [PDB](https://github.com/MattPD/cpplinks/blob/master/executables.md#pdb-program-database))

# Contents

- [Readings](#readings):
	- [Blogs](#readings-blogs)
	- [Books](#readings-books)
	- [Linker Scripts](#readings-linker-scripts)
	- [LTO](#readings-lto)
	- [OS: POSIX](#readings-os-posix) (macOS, Linux, Solaris)
	- [OS: Windows](#readings-os-windows)
	- [Relaxation](#readings-relaxation)
	- [Relocations](#readings-relocations)
	- [Security](#readings-security)
	- [Shared Libraries](#readings-shared-libraries)
- [Software](#software):
	- [Linkers](#software-linkers)
	- [OS: macOS](#software-os-macos)
	- [OS: Linux](#software-os-linux)
	- [OS: Windows](#software-os-windows)
- [Talks](#talks): [2023](#talks-2023), [2022](#talks-2022), [2021](#talks-2021), [2019](#talks-2019), [2018](#talks-2018), [2017](#talks-2017), [2016](#talks-2016), [2012](#talks-2012)

---

# Readings

- Beginner's Guide to Linkers
	- 2010; David Drysdale
	- https://www.lurklurk.org/linkers/linkers.html
- Binary File Descriptor library (BFD)
	- https://sourceware.org/binutils/docs/bfd/
	- https://publicclu2.blogspot.com/2013/05/binary-file-descriptor-library-bfd.html
- Concurrent Linking with the GNU Gold Linker
	- 2013 Thesis; Sander Mathijs van Veen
	- https://smvv.io/gold.pdf
- Linkers and Loaders
	- ACM Computing Surveys, Volume 4, Number 3, September 1972
	- Leon Presser, John R. White
	- http://www-inst.eecs.berkeley.edu/~cs162/sp06/hand-outs/p149-presser-linker-loader.pdf
- Optimizing the LLVM ELF linker for a distributed compilation environment: Concurrent Linking with LLVM LLD
	- 2020 Master’s thesis; Alexander Wilkens
	- https://www.diva-portal.org/smash/record.jsf?pid=diva2:1484152
- Oracle Solaris 11.1 Linkers and Libraries Guide
	- https://docs.oracle.com/cd/E26502_01/html/E26507/
- The Missing Link: Explaining ELF Static Linking, Semantically
	- OOPSLA 2016
	- Stephen Kell, Dominic P. Mulligan, Peter Sewell
	- http://www.cl.cam.ac.uk/~pes20/rems/papers/oopsla-elf-linking-2016.pdf
- The Sad State of Symbol Aliases
	- http://blog.omega-prime.co.uk/2011/07/06/the-sad-state-of-symbol-aliases/
- The Theory, History and Future of System Linkers
	- HelloGCC Workshop 2013; Luba Tang
	- https://github.com/hellogcc/HelloGCC2013/blob/master/linker_overall.pdf

## Readings: Blogs

- Eli Bendersky - Linkers and loaders
	- https://eli.thegreenplace.net/tag/linkers-and-loaders
	- Load-time relocation of shared libraries
		- https://eli.thegreenplace.net/2011/08/25/load-time-relocation-of-shared-libraries
	- Position Independent Code (PIC) in shared libraries
		- https://eli.thegreenplace.net/2011/11/03/position-independent-code-pic-in-shared-libraries
	- Position Independent Code (PIC) in shared libraries on x64
		- https://eli.thegreenplace.net/2011/11/11/position-independent-code-pic-in-shared-libraries-on-x64
	- How statically linked programs run on Linux
		- https://eli.thegreenplace.net/2012/08/13/how-statically-linked-programs-run-on-linux
	- Library order in static linking
		- https://eli.thegreenplace.net/2013/07/09/library-order-in-static-linking
- Fun with weak symbols
	- 2012; Mike Hommey
	- https://glandium.org/blog/?p=2388
- Ian Lance Taylor
	- 20 part linker essay by Ian Lance Taylor
		- Notes: Day 40: Linkers are amazing.
			- 2013; Julia Evans
			- http://jvns.ca/blog/2013/12/10/day-40-learning-about-linkers/
		- TOC: https://checkoway.net/musings/linkers/
		- TOC: https://lwn.net/Articles/276782/
		- 1\. Introduction, personal history, first half of what's-a-linker - http://www.airs.com/blog/archives/38
		- 2\. What's-a-linker: Dynamic linking, linker data types, linker operation - http://www.airs.com/blog/archives/39
		- 3\. Address spaces, Object file formats - http://www.airs.com/blog/archives/40
		- 4\. Shared Libraries - http://www.airs.com/blog/archives/41
		- 5\. More Shared Libraries -- specifically, linker implementation; ELF Symbols - http://www.airs.com/blog/archives/42
		- 6\. Relocations, Position Dependent Shared Libraries - http://www.airs.com/blog/archives/43
		- 7\. Thread Local Storage (TLS) optimization - http://www.airs.com/blog/archives/44
		- 8\. ELF Segments and Sections - http://www.airs.com/blog/archives/45
		- 9\. Symbol Versions, Relaxation optimization - http://www.airs.com/blog/archives/46
		- 10\. Parallel linking - http://www.airs.com/blog/archives/47
		- 11\. Archive format - http://www.airs.com/blog/archives/48
		- 12\. Symbol resolution - http://www.airs.com/blog/archives/49
		- 13\. Symbol resolution from the user's point of view; Static Linking vs. Dynamic Linking - http://www.airs.com/blog/archives/50
		- 14\. Link time optimization, aka Whole Program optimization; Initialization Code - http://www.airs.com/blog/archives/51
		- 15\. COMDAT sections - http://www.airs.com/blog/archives/52
		- 16\. C++ Template Instantiation, Exception Frames - http://www.airs.com/blog/archives/53
		- 17\. Warning Symbols - http://www.airs.com/blog/archives/54
		- 18\. Incremental Linking - http://www.airs.com/blog/archives/55
		- 19\. `__start` and `__stop` Symbols, Byte Swapping - http://www.airs.com/blog/archives/56
		- 20\. Last post; Update on gold's status - http://www.airs.com/blog/archives/57
	- Protected Symbols - https://www.airs.com/blog/archives/307
	- gold
		- Gold Workqueues - https://www.airs.com/blog/archives/78
		- STT_GNU_IFUNC - https://www.airs.com/blog/archives/403
		- A New ELF Linker
			- GCC Summit 2008
			- Proceedings of the GCC Developers' Summit (2008)
			- https://research.google.com/pubs/pub34417.html
			- https://gcc.gnu.org/wiki/HomePage?action=AttachFile&do=view&target=gcc-2008-proceedings.pdf
			- http://airs.com/ian/gold-slides.pdf
- Jordan Rose
	- Dynamic Linking Is Bad For Apps And Static Linking Is Also Bad For Apps
		- https://belkadan.com/blog/2022/02/Dynamic-Linking-and-Static-Linking/
- MaskRay (Fangrui Song)
	- All about COMMON symbols
		- https://maskray.me/blog/2022-02-06-all-about-common-symbols
	- Analysis and introspection options in linkers
		- https://maskray.me/blog/2022-02-27-analysis-and-introspection-options-in-linkers
	- COMDAT and section group
		- https://maskray.me/blog/2021-07-25-comdat-and-section-group
	- Dependency related linker options
		- https://maskray.me/blog/2021-06-13-dependency-related-linker-options
	- Linker notes on AArch64
		- https://maskray.me/blog/2023-03-05-linker-notes-on-aarch64
	- LLD and GNU linker incompatibilities
		- https://maskray.me/blog/2020-12-19-lld-and-gnu-linker-incompatibilities
	- Weak symbol
		- https://maskray.me/blog/2021-04-25-weak-symbol
- Nick Desaulniers
	- Part 1 – Object Files and Symbols - https://nickdesaulniers.github.io/blog/2016/08/13/object-files-and-symbols/
	- Part 2 – Static and Dynamic Libraries - https://nickdesaulniers.github.io/blog/2016/11/20/static-and-dynamic-libraries/
- Stephen Kell
	- Linking and loading: what's incidental?
		- http://www.cl.cam.ac.uk/~srk31/blog/research/linking-and-loading-complexity.html
	- Dynamic linking and security
		- http://www.cl.cam.ac.uk/~srk31/blog/research/dynamic-linker-security.html
	- C libraries and linking
		- http://www.cl.cam.ac.uk/~srk31/blog/research/c-libraries-compilers-and-linking.html
	- How and why to do link-time symbol wrapping (or not?)
		- https://www.humprog.org/~stephen/blog/2022/08/03/#elf-symbol-wrapping-via-replacement
	- How to do link-time symbol wrapping... as a plugin
		- https://www.humprog.org/~stephen/blog/2022/10/06/#elf-symbol-wrapping-plugin
	- Link order
		- http://www.cl.cam.ac.uk/~srk31/blog/devel/link-order.html
	- Weak dynamic symbols
		- http://www.cl.cam.ac.uk/~srk31/blog/devel/weak-symbols.html
- Trevor Pounds
	- Versioning Symbols for Shared Libraries (glibc)
		- https://web.archive.org/web/20150906233231/http://www.trevorpounds.com/blog/?p=33
	- Linking to Older Versioned Symbols (glibc)
		- https://web.archive.org/web/20150906233154/http://www.trevorpounds.com/blog/?p=103

## Readings: Books

- Advanced C and C++ Compiling
	- 2014; Milan Stevanovic​
	- "Engineering guide to C/C++ compiling, linking, and binary files structure"
	- http://www.apress.com/9781430266679
	- http://link.springer.com/book/10.1007%2F978-1-4302-6668-6
	- https://github.com/apress/adv-c-cpp-compiling
- Linkers and Loaders
	- 1999; John R. Levine
	- https://www.iecc.com/linker/

## Readings: Linker Scripts

- OSDev Wiki
	- https://wiki.osdev.org/Category:Linkers
	- Linker Scripts
		- http://wiki.osdev.org/Linker_Scripts
- LD - Linker Scripts
	- https://sourceware.org/binutils/docs/ld/Scripts.html
- Everything You Never Wanted To Know About Linker Script
	- 2021; Miguel Young de la Sota
	- https://mcyoung.xyz/2021/06/01/linker-script/
- From Zero to main(): Demystifying Firmware Linker Scripts
	- 2019; François Baldassari
	- https://interrupt.memfault.com/blog/how-to-write-linker-scripts-for-firmware
- The Most Thoroughly Commented Linker Script in The World (Probably)
	- 2021; Thea "Stargirl" Flowers
	- "a linker script for the Atmel/Microchip SAM D21 with an absolutely obscene amount of documentation"
	- https://blog.thea.codes/the-most-thoroughly-commented-linker-script/
	- https://github.com/theacodes/Winterbloom_Castor_and_Pollux/blob/master/firmware/scripts/samd21g18a.ld

## Readings: LTO

- (Ab)using LTO plugin API for system-wide shrinking of dynamic libraries
	- GNU Tools Cauldron 2018
	- Vladislav Ivanishin
	- https://www.youtube.com/watch?v=BNYGB7dHgkc
	- https://gcc.gnu.org/wiki/cauldron2018?action=AttachFile&do=view&target=lto-plugin-api-abuse.pdf
- GCC Wiki - LinkTimeOptimization
	- https://gcc.gnu.org/wiki/LinkTimeOptimization
- Honza Hubička's Blog
	- Linktime optimization in GCC, part 1 - brief history
		- http://hubicka.blogspot.com/2014/04/linktime-optimization-in-gcc-1-brief.html
	- Linktime optimization in GCC, part 2 - Firefox
		- http://hubicka.blogspot.com/2014/04/linktime-optimization-in-gcc-2-firefox.html
	- Linktime optimization in GCC, part 3 - LibreOffice
		- https://hubicka.blogspot.com/2014/09/linktime-optimization-in-gcc-part-3.html
	- Link time and inter-procedural optimization improvements in GCC 5
		- https://hubicka.blogspot.com/2015/04/GCC5-IPA-LTO-news.html
	- Building libreoffice with GCC 6 and LTO
		- https://hubicka.blogspot.com/2016/03/building-libreoffice-with-gcc-6-and-lto.html
	- GCC 8: link time and interprocedural optimization
		- https://hubicka.blogspot.com/2018/06/gcc-8-link-time-and-interprocedural.html
- LLVM Link Time Optimization: Design and Implementation
	- https://llvm.org/docs/LinkTimeOptimization.html
- Optimizing Large Applications
	- 2014 Master's Thesis; Martin Liška
	- https://arxiv.org/abs/1403.6997
- Optimizing real world applications with GCC Link Time Optimization
	- 2010 GCC Developers' Summit; T. Glek, J. Hubicka
	- https://arxiv.org/abs/1010.2196
- ThinLTO
	- ThinLTO: Scalable and Incremental LTO
		- http://blog.llvm.org/2016/06/thinlto-scalable-and-incremental-lto.html
	- ThinLTO: Scalable and Incremental Link-Time Optimization
		- CppCon 2017; Teresa Johnson
		- https://www.youtube.com/watch?v=p9nH2vZ2mNo
	- ThinLTO: Scalable and incremental LTO
		- CGO 2017
		- Teresa Johnson, Mehdi Amini, and Xinliang David Li
		- https://research.google/pubs/pub47584/

## Readings: OS: POSIX

### macOS

- Debugging Dyld
	- https://lowlevelbits.org/debugging-dyld/
- dyld: Dynamic Linking On OS X
	- Friday Q&A 2012-11-09
	- https://www.mikeash.com/pyblog/friday-qa-2012-11-09-dyld-dynamic-linking-on-os-x.html
- dyld_usage - report dynamic linker activity in real-time
	- https://github.com/apple-opensource/dyld/blob/master/doc/rst/dyld_usage.rst
- Dynamic Library Programming Topics
	- https://developer.apple.com/library/archive/documentation/DeveloperTools/Conceptual/DynamicLibraries
- How iOS 15 makes your app launch faster
	- the chained fixups format
	- https://www.emergetools.com/blog/posts/iOS15LaunchTime

### Linux

- Awesome LD_PRELOAD
	- List of resources related to LD_PRELOAD, a mechanism for changing application behavior at run-time
	- https://github.com/gaul/awesome-ld-preload
- ELF Loaders, Libraries and Executables on Linux
	- https://trugman-internals.com/elf-loaders-libraries-executables/
- ELF symbol interposition and RTLD_LOCAL
	- 2022; Kyle Huey
	- https://pernos.co/blog/interposition-rtld-local/
- Linker limitations on 32-bit architectures
	- 2019; Alexander E. Patrakov
	- https://lwn.net/Articles/797303/
- Linux EDR Evasion With Meterpreter and LD_PRELOAD
	- https://forensicitguy.github.io/posts/linux-edr-evasion-with-ld-preload/
- Linux Internals
	- Dynamic Linking Wizardry
		- https://0x00sec.org/t/linux-internals-dynamic-linking-wizardry/1082
	- The Art Of Symbol Resolution
		- https://0x00sec.org/t/linux-internals-the-art-of-symbol-resolution/1488
- Linux SHELF Loading
	- Introducing SHELF Loading: The Nexus between Static and Position Independent Code
		- tmp.0ut Volume 1 - April 2021
		- ulexec, Anonymous_
		- https://tmpout.sh/1/10/
	- SHELF encounters of the elements kind
		- tmp.0ut Volume 2; February 2022
		- ulexec
		- https://tmpout.sh/2/5.html
- Preloading the linker for fun and profit
	- tmp.0ut Volume 2; February 2022
	- elfmaster
	- https://tmpout.sh/2/6.html
	- "Linker preloading". This technique refers to the idea that one can maniuplate the kernels ELF loader (see linux/fs/binfmt_elf.c) to pass execution to a custom program interpreter instead of the real dynamic linker. 
	- Note that the term 'program interpreter' usually refers to the dynamic linker, i.e. "/lib64/ld-linux.so". Also known as the RTLD (Runtime loader). This paper is about creating an alternate 'program interpreter' which is loaded prior to the dynamic linker itself.
- Understanding ld-linux.so.2
	- https://web.archive.org/web/20190421205537/http://www.cs.virginia.edu/~dww4s/articles/ld_linux.html

### Solaris

- Surfing With The Linker Aliens: Solaris Linking & ELF Blogs
	- http://www.linker-aliens.org/
	- The Link-editors - a source tour
		- http://www.linker-aliens.org/blogs/rie/entry/the_link_editors_a_source/
	- What Are "Tentative" Symbols?
		- http://www.linker-aliens.org/blogs/ali/entry/what_are_tentative_symbols/

## Readings: OS: Windows

- Raymond Chen - The Old New Thing
	- Understanding the classical model for linking
		- https://blogs.msdn.microsoft.com/oldnewthing/tag/linker
		- Groundwork: The algorithm
			- https://devblogs.microsoft.com/oldnewthing/20130107-00/?p=5633
		- Taking symbols along for the ride
			- https://devblogs.microsoft.com/oldnewthing/20130108-00/?p=5623
		- You can override an LIB with another LIB, and a LIB with an OBJ, but you can’t override an OBJ
			- https://devblogs.microsoft.com/oldnewthing/20130109-00/?p=5613
		- Sometimes you don’t want a symbol to come along for a ride
			- https://devblogs.microsoft.com/oldnewthing/20130110-00/?p=5593
		- Understanding errors in classical linking: The delay-load catch-22
			- https://devblogs.microsoft.com/oldnewthing/20130111-00/?p=5583
	- Using linker segments and `__declspec(allocate(…))` to arrange data in a specific order
		- https://blogs.msdn.microsoft.com/oldnewthing/20181107-00/?p=100155
	- Gotchas when using linker sections to arrange data, part 1
		- https://blogs.msdn.microsoft.com/oldnewthing/20181108-00/?p=100165
	- Gotchas when using linker sections to arrange data, part 2
		- https://blogs.msdn.microsoft.com/oldnewthing/20181109-00/?p=100175
	- Why would the incremental linker insert padding between section fragments?
		- https://blogs.msdn.microsoft.com/oldnewthing/20190114-00/?p=100695

## Readings: Performance

- Design and implementation of mold
	- 2021; Rui Ueyama
	- https://github.com/rui314/mold/blob/main/docs/design.md
- Why isn't ld.lld faster?
	- 2021; MaskRay (Fangrui Song)
	- https://maskray.me/blog/2021-12-19-why-isnt-ld.lld-faster

## Readings: Relaxation

- Linker Relaxation in LLD
	- RISC-V Forum: Developer Tools & Tool Chains 2021
	- Chih-Mao Chen
	- https://www.youtube.com/watch?v=4GnQbhNt1Cc
- Linker Relaxation in the RISC-V Toolchain
	- 2017; Palmer Dabbelt
	- https://www.sifive.com/blog/all-aboard-part-3-linker-relaxation-in-riscv-toolchain
- RISC-V linker relaxation in lld
	- 2022; MaskRay (Fangrui Song)
	- https://maskray.me/blog/2022-07-10-riscv-linker-relaxation-in-lld
- The dark side of RISC-V linker relaxation
	- 2021; MaskRay (Fangrui Song)
	- https://maskray.me/blog/2021-03-14-the-dark-side-of-riscv-linker-relaxation

## Readings: Relocations

- Binary Dodo - Arun
	- Investigating linking with COMMON symbols in ELF
		- https://binarydodo.wordpress.com/2016/05/09/investigating-linking-with-common-symbols-in-elf/
	- Symbol binding types in ELF and their effect on linking of relocatable files
		- https://binarydodo.wordpress.com/2016/05/12/symbol-binding-types-in-elf-and-their-effect-on-linking-of-relocatable-files/
	- Symbol resolution during link-editing
		- https://binarydodo.wordpress.com/2016/07/01/symbol-resolution-during-link-editing/
- ELF Binary Relocations and Thread Local Storage - Stafford Horne
	- TLS Examples
		- https://github.com/stffrdhrn/tls-examples
	- ELF Binaries and Relocation Entries
		- http://stffrdhrn.github.io/hardware/embedded/openrisc/2019/11/29/relocs.html
	- Thread Local Storage
		- https://stffrdhrn.github.io/hardware/embedded/openrisc/2020/01/19/tls.html
	- How Relocations and Thread Local Storage are Implemented
		- https://stffrdhrn.github.io/software/toolchain/openrisc/2020/07/21/relocs_tls_impl.html
- [Executable and Linkable Format 101](https://intezer.com/tag/elf/) - Ignacio Sanmillan
	- Part 3: Relocations - https://www.intezer.com/executable-and-linkable-format-101-part-3-relocations/
- GOT and PLT
	- https://systemoverlord.com/2017/03/19/got-and-plt-for-pwning.html
- Ian Lance Taylor
	- Linkers 2\. What's-a-linker: Dynamic linking, linker data types, linker operation
		- http://www.airs.com/blog/archives/39
	- Linkers 5\. More Shared Libraries -- specifically, linker implementation; ELF Symbols
		- http://www.airs.com/blog/archives/42
	- Linkers 6\. Relocations, Position Dependent Shared Libraries
		- http://www.airs.com/blog/archives/43
	- Linkers 9\. Symbol Versions, Relaxation optimization
		- http://www.airs.com/blog/archives/46
	- Linker combreloc
		- https://www.airs.com/blog/archives/186
	- Linker relro
		- https://www.airs.com/blog/archives/189
- Introduction to the ELF Format - Keith Makan
	- Part VI(1): The Symbol Table and Relocations - https://blog.k3170makan.com/2018/10/introduction-to-elf-format-part-vi.html
	- Part VI(2): The Symbol Table and Relocations - https://blog.k3170makan.com/2018/10/introduction-to-elf-format-part-vi_18.html
	- Part VI(3): More Relocation tricks - r_addend execution - https://blog.k3170makan.com/2018/10/introduction-to-elf-format-part-vi-more.html
- Linkers and loaders - Eli Bendersky - http://eli.thegreenplace.net/tag/linkers-and-loaders
	- Load-time relocation of shared libraries
		- https://eli.thegreenplace.net/2011/08/25/load-time-relocation-of-shared-libraries
- Making our own executable packer - Amos Wenger
	- ELF relocations - https://fasterthanli.me/blog/2020/elf-relocations/
	- More ELF relocations - https://fasterthanli.me/blog/2020/more-elf-relocations/
- MaskRay (Fangrui Song)
	- All about Global Offset Table
		- https://maskray.me/blog/2021-08-29-all-about-global-offset-table
	- Copy relocations, canonical PLT entries and protected visibility
		- https://maskray.me/blog/2021-01-09-copy-relocations-canonical-plt-entries-and-protected
	- Relocatable linking
		- https://maskray.me/blog/2022-11-21-relocatable-linking
	- Relocation overflow and code models
		- https://maskray.me/blog/2023-05-14-relocation-overflow-and-code-models
- Moving code around - Thiago Macieira
	- http://blog.qt.io/blog/2010/12/04/moving-code-around/
	- http://blog.qt.io/blog/2010/12/05/moving-code-around-more-easily/
- Oracle Solaris 11.1 Linker and Libraries Guide
	- Relocation Processing
		- https://docs.oracle.com/cd/E26502_01/html/E26507/chapter3-29.html
	- Relocation Sections
		- https://docs.oracle.com/cd/E23824_01/html/819-0690/chapter6-54839.html
- Relocations in ELF Toolchains - Palmer Dabbelt
	- https://www.sifive.com/blog/2017/08/21/all-aboard-part-2-relocations/
- Relocations: fantastic symbols, but where to find them? - Siddhesh Poyarekar
	- https://siddhesh.in/posts/relocations-fantastic-symbols-but-where-to-find-them.html
- Resolving ELF Relocation Name / Symbols - Chris Rohlf
	- https://em386.blogspot.com/2006/10/resolving-elf-relocation-name-symbols.html

## Readings: Research

- MELF: Multivariant Executables for a Heterogeneous World
	- 2023 USENIX Annual Technical Conference (ATC)
	- Dominik Töllner, Christian Dietrich, Illia Ostapyshyn, Florian Rommel, Daniel Lohmann
	- https://www.usenix.org/conference/atc23/presentation/tollner

## Readings: Security

- An Evil Copy: How the Loader Betrays You
	- Network and Distributed System Security Symposium (NDSS) 2017
	- Xinyang Ge, Mathias Payer, Trent Jaeger
	- https://nebelwelt.net/publications/files/17NDSS.pdf
	- https://www.microsoft.com/en-us/research/publication/evil-copy-loader-betrays/
- Breaking the links: Exploiting the linker
	- 2011; Tim Brown
	- https://packetstormsecurity.com/files/102814/Breaking-The-Links-Exploiting-The-Linker.html
	- paper: https://dl.packetstormsecurity.net/papers/general/BTL.pdf
	- slides: https://labs.portcullis.co.uk/download/BTLCC.pdf
- Dynamic Loader Oriented Programming on Linux
	- Reversing and Offensive-oriented Trends Symposium (ROOTS) 2017
	- Julian Kirsch, Bruno Bierbaumer, Thomas Kittel, and Claudia Eckert
	- https://kirschju.re/projects/static/kirsch-roots-2017-paper.pdf
	- https://github.com/kirschju/wiedergaenger
- Types for the Chain of Trust: No (loader) write left behind
	- 2018 PhD dissertation; Rebecca .bx Shapiro
	- http://typedregions.com/
	- Dissertation: http://typedregions.com/main.pdf
	- Defense slides: http://typedregions.com/defense-slides.pdf

## Readings: Shared Libraries

- Chain loading, not preloading: the dynamic linker as a virtualization vector
	- https://www.humprog.org/~stephen/blog/2021/01/04/#elf-chain-loading
	- Tracing system calls in-process, using a chain loader
		- https://www.humprog.org/~stephen/blog/2021/10/14/#syscall-tracing-in-process
	- donald: the Mickey Mouse of dynamic linkers
		- https://github.com/stephenrkell/donald/
- `-fno-semantic-interposition`: ELF interposition, the GCC/Clang option and why it can (sometimes incredibly) optimize `-fPIC` programs
	- https://maskray.me/blog/2021-05-09-fno-semantic-interposition
- Cheating the ELF: Subversive Dynamic Linking to Libraries
	- 2001; the grugq - https://grugq.github.io/docs/
	- https://grugq.github.io/docs/subversiveld.pdf
- Dynamic Linkers Are the Narrow Waist of Operating Systems
	- Workshop on Programming Languages and Operating Systems (PLOS) 2023
	- Charly Castes, Adrien Ghosn
	- https://dl.acm.org/doi/10.1145/3623759.3624548
- ELF dynamic linking: a brief introduction
	- https://www.humprog.org/~stephen/blog/2021/10/18/#elf-dynamic-linking-intro
- Fun with weak dynamic linking
	- https://glandium.org/blog/?p=2764
- Guided Linking: Dynamic Linking without the Costs
	- OOPSLA 2020
	- Sean Bartell, Will Dietz, Vikram S. Adve
	- https://dl.acm.org/doi/abs/10.1145/3428213
	- http://design.cs.iastate.edu/splash20/oopsla20/oopsla20main-p80-p.pdf
	- https://www.youtube.com/watch?v=apzR151q1wE
	- BCDB: The Bitcode Database with Guided Linking
		- https://github.com/yotann/bcdb
- How To Write Shared Libraries - Ulrich Drepper
	- https://www.akkadia.org/drepper/dsohowto.pdf
- Inlining — shared libraries are special
	- https://kristerw.blogspot.com/2016/11/inlining-shared-libraries-are-special.html
- Luci: Loader-based Dynamic Software Updates for Off-the-shelf Shared Objects
	- USENIX Annual Technical Conference (ATC) 2023
	- Bernhard Heinloth, Peter Wägemann, Wolfgang Schröder-Preikschat
	- https://www.usenix.org/conference/atc23/presentation/heinloth
- PLT and GOT - the key to code sharing and dynamic libraries
	- https://www.technovelty.org/linux/plt-and-got-the-key-to-code-sharing-and-dynamic-libraries.html
- Remote Library Injection
	- 2004
	- skape, Jarkko Turkulainen
	- http://hick.org/code/skape/papers/remote-library-injection.pdf
	- Memdlopen: dlopen from memory
		- https://github.com/m1m1x/memdlopen
	- memdlopen-lib: An updated version of m1m1x's memdlopen project (based on Nologin's paper)
		- https://github.com/X-C3LL/memdlopen-lib
- Shared libraries as executables
	- 2022; Harmen Stoppels
	- https://stoppels.ch/2022/08/20/executable-shared-libraries.html
- Shared Libraries: Understanding Dynamic Loading
	- http://amir.rachum.com/blog/2016/09/17/shared-libraries/
- Shrinking a Shared Library
	- 2023-06-23
	- Serge Sans Paille
	- https://serge-sans-paille.github.io/pythran-stories/shrinking-a-shared-library.html
- Software Multiplexing: Share Your Libraries and Statically Link Them Too
	- SPLASH 2018 OOPSLA
	- Will Dietz, Vikram Adve
	- https://2018.splashcon.org/event/splash-2018-oopsla-software-multiplexing-share-your-libraries-and-statically-link-them-too
	- https://publish.illinois.edu/allvm-project/
	- https://github.com/allvm/allvm-tools
- Stop searching for shared libraries
	- 2022; Harmen Stoppels
	- https://stoppels.ch/2022/08/04/stop-searching-for-shared-libraries.html

---

# Software

- GNU Linker Output Viewer & Editor
	- https://github.com/JonTheBurger/GLOVE
- interpose: Function interposition for Linux and macOS
	- This single-header project implements dynamic library symbol interposition for both macOS and Linux.
	- https://github.com/ccurtsinger/interpose
- ld-limiter: Limit number of parallel link jobs
	- https://github.com/yugr/ld-limiter
- libdlbind: Dynamic creation and update of ELF files, or: an allocator for JIT compilers
	- an extension to System V-style dynamic loaders to allow dynamic allocation of objects and dynamic binding of symbols
	- https://github.com/stephenrkell/libdlbind
- libwhich: Like `which`, for dynamic libraries
	- https://github.com/vtjnash/libwhich
- linkermapviz
	- Interactive visualization of GNU ld’s linker map with a tree map.
	- https://github.com/PromyLOPh/linkermapviz
- linksem: Semantic model for aspects of ELF static linking and DWARF debug information
	- https://github.com/rems-project/linksem
- QuarkslaB Dynamic Loader (QBDL)
	- The QuarkslaB Dynamic Linker (QBDL) library aims at providing a modular and portable way to dynamically load and link binaries.
	- https://github.com/quarkslab/QBDL
	- SSTIC 2021; Adrien Guinet, Romain Thomas
		- https://sstic.org/2021/presentation/qbdl_quarkslab_dynamic_loader/
- ShlibVisibilityChecker: Tool for locating internal symbols unnecessarily exported from shared libraries
	- https://github.com/yugr/ShlibVisibilityChecker
- timey: A utility for timing linkers
	- https://github.com/SNSystems/timey

## Software: Linkers

- ld - the GNU linker
	- https://sourceware.org/binutils/docs/ld/
- LLD - The LLVM Linker
	- https://lld.llvm.org/
- mold: A Modern Linker
	- https://github.com/rui314/mold
	- mold: A Modern Linker
		- 2022 EasyBuild Tech Talks VI
		- Rui Ueyama
		- https://www.youtube.com/watch?v=hAt3kCalE0Y
		- https://easybuild.io/tech-talks/006_mold.html

## Software: OS: macOS

- cctools-port: Apple cctools and ld64 port for Linux, \*BSD and macOS
	- https://github.com/tpoechtrager/cctools-port
- ld64
	- https://github.com/apple-opensource/ld64
- ld64: Instructions on how to build the ld64 linker on macOS
	- https://github.com/dmaclach/ld64
- [lld] Initial commit for new Mach-O backend
	- https://reviews.llvm.org/D75382
- macdylibbundler: Utility to ease bundling libraries into executables for OSX
	- https://github.com/auriamg/macdylibbundler
- osxcross: Mac OS X cross toolchain for Linux, FreeBSD, OpenBSD and Android (Termux)
	- https://github.com/tpoechtrager/osxcross
- zld: A faster version of Apple's linker
	- https://github.com/michaeleisel/zld

## Software: OS: Linux

- DDexec: A technique to run binaries filelessly and stealthily on Linux by "overwriting" the shell's process with another
	- https://github.com/arget13/DDexec
- dlinject.py: Inject a shared library (i.e. arbitrary code) into a live linux process, without ptrace
	- https://github.com/DavidBuchanan314/dlinject
- Faulty.lib: Dynamic linker for compressed libraries, with on-demand decompression (ELF Linux systems)
	- https://github.com/glandium/faulty.lib
- Fun with LD_PRELOAD
	- linux.conf.au 2009; Kevin Pulo
	- https://www.youtube.com/watch?v=WocKUD5a4O0
	- http://kev.pulo.com.au/publications/lca2009/lca2009-kevin-pulo-fun-with-ld_preload.pdf
	- LD_PRELOAD libraries
		- libsysconfcpus: override number of CPUs reported by sysconf()
			- http://kev.pulo.com.au/libsysconfcpus/
		- xlibtrace: trace libX11 calls
			- http://kev.pulo.com.au/xlibtrace/
		- xmultiwin: transparently "clone" X11 windows
			- http://kev.pulo.com.au/xmultiwin/
		- tunerlimit: control access to setrlimit(2)
			- http://kev.pulo.com.au/tunerlimit/
- GOTCHA: a library for wrapping function calls in shared libraries
	- Gotcha is a library that wraps functions. Tools can use gotcha to install hooks into other libraries, for example putting a wrapper function around libc's malloc.
	- It is similar to LD_PRELOAD, but operates via a programmable API. This enables easy methods of accomplishing tasks like code instrumentation or wholesale replacement of mechanisms in programs without disrupting their source code.
	- https://github.com/LLNL/GOTCHA
- Implib.so: POSIX equivalent of Windows DLL import libraries
	- https://github.com/yugr/Implib.so
- libosuction: A tool for stripping dynamic libraries of unneeded symbols
	- https://github.com/ispras/libosuction
	- System-Wide Elimination of Unreferenced Code and Data in Dynamically Linked Programs
		- Ivannikov ISPRAS Open Conference (ISPRAS) 2017
		- V. Ivanishin, E. Kudryashov, A. Monakov, D. Melnik, J. Lee
		- https://doi.org/10.1109/ISPRAS.2017.00007
- libpreloadvaccine: Whitelisting LD_PRELOAD libraries using LD_AUDIT
	- https://github.com/ForensicITGuy/libpreloadvaccine
	- Whitelisting LD_PRELOAD for Fun and No Profit
		- Shmoocon 2020; Tony Lambert
		- https://www.youtube.com/watch?v=nM9Y2Sky6S0
		- https://speakerdeck.com/forensicitguy/whitelisting-ld-preload-for-fun-and-no-profit
- libprocesshider: Hide a process under Linux using the ld preloader
	- https://github.com/gianlucaborello/libprocesshider
	- https://sysdig.com/blog/hiding-linux-processes-for-fun-and-profit/
- libtree: ldd as a tree with an option to bundle dependencies into a single folder
	- https://github.com/haampie/libtree
- Shiva JIT micropatching engine
	- A custom ELF linker/loader for installing ET_REL binary patches at runtime
	- Shiva is an ELF dynamic linker that is specialized for patching native Linux software. Shiva has been custom tailored towards the requirements of the DARPA AMP project and currently supports the AArch64 architecture.
	- Patches are written in C and compiled into ELF relocatable objects. Shiva loads, links, and patches the new code into memory.
	- https://github.com/advanced-microcode-patching/shiva
	- Revolutionizing ELF binary patching w Shiva
		- DEF CON 31 2023
		- Ryan “ElfMaster” O’Neill
		- https://www.youtube.com/watch?v=TDMWejaucdg
		- https://media.defcon.org/DEF%20CON%2031/DEF%20CON%2031%20presentations/ElfMaster%20-%20Revolutionizing%20ELF%20binary%20patching%20with%20Shiva%20A%20JIT%20binary%20patching%20system%20for%20Linux.pdf
	- Shiva: a programmable dynamic linker for loading ELF microprograms
		- https://github.com/elfmaster/shiva
- stelf-loader: A stealthy ELF loader - no files, no execve, no RWX
	- https://github.com/DavidBuchanan314/stelf-loader

## Software: OS: Windows

- LoaderLog: Small application that can be used to log loader snaps and other debug output
	- https://github.com/TimMisiak/LoaderLog
- memory-module-loader
	- An implementation of a Windows loader that can load dynamic-linked libraries (DLLs) directly from memory
	- https://github.com/scythe-io/memory-module-loader
	- https://scythe.io/library/loading-capabilities-from-memory-open-sourcing-scythes-windows-c-in-memory-module-loader

---

# Talks

## Talks: 2023

- Everything I wish they told me about linkers
	- MUC++ 2023
	- Ofek Shilon
	- https://www.youtube.com/watch?v=H5VQhQ61aeo
- Meet mergeable libraries
	- WWDC 2023
	- Cyndy Ishida
	- https://developer.apple.com/videos/play/wwdc2023/10268/
- Speeding up the BFD linker
	- SUSE Labs Conference 2023
	- Michael Matz
	- https://www.youtube.com/watch?v=h5pXt_YCwkU

## Talks: 2022

- C++ Function Multiversioning in Windows: High-performance Load-time Implementation Selection
	- CppCon 2022 
	- Joe Bialek and Pranav Kant
	- Load Time Function Selection (LTFS)
	- https://www.youtube.com/watch?v=LTM1was1dTU
	- https://github.com/CppCon/CppCon2022/blob/main/Presentations/Load-Time-Function-Selection.pdf
- How to start a program
	- NDC TechTown 2022; Anders Schau Knatten
	- Linux/ELF
	- https://www.youtube.com/watch?v=OGPmZzhDPYw
- Link fast: Improve build and launch times
	- WWDC 2022; Nick Kledzik
	- https://developer.apple.com/videos/play/wwdc2022/110362/
- LLD for Mach-O: The Journey
	- 2022 EuroLLVM Developers' Meeting
	- Nico Weber, Jez Ng
	- https://www.youtube.com/watch?v=ynbFTojAOiY
	- https://llvm.org/devmtg/2022-05/slides/2022EuroLLVM-LLD-for-Mach-O.pdf
	- https://docs.google.com/presentation/d/16BMWED6foi6mWThtjAMW93HhtuePOYfTOuB2byJT9MQ/view

## Talks: 2021

- Dynamically Loaded Libraries Outside the Standard
	- CppCon 2021; Zhihao Yuan
	- https://www.youtube.com/watch?v=fyFVCUwsMws&list=PLHTh1InhhwT6vjwMy3RG5Tnahw0G9qIx6&index=135
	- https://speakerdeck.com/lichray/dynamically-loaded-libraries-outside-the-standard
	- https://cppcon.digital-medium.co.uk/wp-content/uploads/2021/10/Dynamically-Loaded-Libraries-Outside-the-Standard.pdf
	- https://github.com/zhihaoy/dl-examples
- From Program to Process - What Happens After the Compiler
	- NDC TechTown 2021
	- Anders Schau Knatten
	- https://www.youtube.com/watch?v=fGnbGX88z3Y
- Linker Relaxation in LLD
	- RISC-V Forum 2021; Chih-Mao Chen
	- https://www.youtube.com/watch?v=4GnQbhNt1Cc
- Mach-O linker in Zig: linking in the era of Apple Silicon
	- FOSDEM 2021; Jakub Konka
	- https://fosdem.org/2021/schedule/event/zig_macho/

## Talks: 2019

- Dynamic Linking On GNU/Linux
	- emBO++ 2019; Florian Sowade
	- https://www.youtube.com/watch?v=G2r5JhVDddw
	- https://www.slideshare.net/FlorianSowade/dynamic-linking-on-gnulinux/
- Pardon the Interposition—Modifying and Improving Software Behavior with Interposers
	- USENIX LISA 2019; Danny Chen
	- https://www.usenix.org/conference/lisa19/presentation/chen
- The ACM-NVIDIA Compiler summer school lectures (2019)
	- https://nptel.ac.in/courses/128/106/128106009/
	- https://www.youtube.com/playlist?list=PLPeEbErKGwN15rF-BnlngobapgIRZbAK4
	- Program Execution Environment
		- part 1: https://www.youtube.com/watch?v=Sf4JnUcJxSQ
		- part 2: https://www.youtube.com/watch?v=e3DnPTUunZk
		- part 3: https://www.youtube.com/watch?v=h__sj8IfONg
		- part 4: https://www.youtube.com/watch?v=yzYXrwxu6YM
		- part 5: https://www.youtube.com/watch?v=4_LK7nOSlbM
		- part 6: https://www.youtube.com/watch?v=CzAwzTkbMDw
		- part 7: https://www.youtube.com/watch?v=IWU5Av6YpEw
		- part 8: https://www.youtube.com/watch?v=Wd4NaS0_7Tc
- What makes LLD so fast?
	- FOSDEM 2019; Peter Smith
	- https://fosdem.org/2019/schedule/event/llvm_lld/
	- https://www.youtube.com/watch?v=CeHhveHHzII

## Talks: 2018

- Behind the Scenes of the Xcode Build Process
	- WWDC 2018; Jake Petroules, Jürgen Ributzka, Devin Coughlin, Louis Gerbarg
	- https://developer.apple.com/videos/play/wwdc2018/415/
- The Bits Between the Bits: How We Get to main()
	- CppCon 2018; Matt Godbolt
	- https://www.youtube.com/watch?v=dOfucXtyEsU
	- Slides: https://mattgodbolt.github.io/cppcon-bits-between-bits/

## Talks: 2017

- App Startup Time: Past, Present, and Future
	- WWDC 2017; Louis Gerbarg
	- https://developer.apple.com/videos/play/wwdc2017/413/
	- "Learn about the dyld dynamic linker used on Apple platforms, how it's changed over the years, and where it's headed next. Find out how improved tooling makes it easier to optimize your app's launch time, and see how new changes coming in dyld will bring even further launch time improvements."
- LLD from a user's perspective
	- FOSDEM 2017; Peter Smith
	- https://archive.fosdem.org/2017/schedule/event/lld/
	- https://archive.fosdem.org/2017/schedule/event/lld/attachments/slides/1446/export/events/attachments/lld/slides/1446/FosdemLLD2017.pdf
- lld: A Fast, Simple, and Portable Linker
	- 2017 LLVM Developers’ Meeting; Rui Ueyama
	- https://www.youtube.com/watch?v=yTtWohFzS6s
	- https://llvm.org/devmtg/2017-10/slides/Ueyama-lld.pdf
- My Little Object File: How Linkers Implement C++
	- CppCon 2017; Michael Spencer
	- https://youtu.be/a5L66zguFe4
- The Missing Link: The Curious symbiosis between C++ and the Linker
	- C++ Meetup Sydney hosted by IMC; December 6, 2017
	- Dave Gittins
	- https://www.youtube.com/watch?v=twNoIhGKIoo

## Talks: 2016

- New LLD linker for ELF: A high performance linker from the LLVM project
	- 2016 EuroLLVM Developers' Meeting; Rui Ueyama
	- https://www.youtube.com/watch?v=CYCRqjVa6l4
	- https://llvm.org/devmtg/2016-03/Presentations/EuroLLVM%202016-%20New%20LLD%20linker%20for%20ELF.pdf
- Optimizing App Startup Time: Linkers, loaders, and you
	- WWDC 2016; Nick Kledzik, Louis Gerbarg
	- https://developer.apple.com/videos/play/wwdc2016/406/
	- "Launching an App is a complicated and subtle process and the ramifications on launch times of different App design patterns are often non-obvious. Come learn what happens in the time between when an App begins launching and when the main() function gets control and how that time relates to the code and structure of your App. Learn about the inner details of the dynamic loader, dyld, and best practices for structuring your code to perform at its best from the very start."

## Talks: 2012

- lld - the LLVM Linker
	- 2012 EuroLLVM Developers’ Meeting; Michael Spencer
	- https://www.youtube.com/watch?v=zCaFF3aOabg
	- http://llvm.org/devmtg/2012-04-12/Slides/Michael_Spencer.pdf
