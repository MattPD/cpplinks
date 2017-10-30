# [C++ links](README.md): executable and object file formats (ELF, Mach-O, PE); debugging data formats (DWARF, PDB): articles, documentation, software, and talks.

Executable files, debugging data, object code, shared libraries - file formats information, specifications, software - with relevance to compiler toolchains, debuggers, and general program analysis.

Organization: Preference given to the most specific category -- e.g., if an article discusses DLL-specific information, then it belongs to the DLL section (in preference to the more general PE).

See also: [compilers](compilers.md)

Contents:

* [General](#general): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#talks)
* [DLL](#dll): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-1) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-1) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#talks-1)
* [DWARF](#dwarf): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-2) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-2) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#talks-2)
* [ELF](#elf): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-3) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-3) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#talks-3)
* [Mach-O](#mach-o): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-4) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-4) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#talks-4)
* [PDB](#pdb-program-database): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-5) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-5) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#talks-5)
* [PE](#pe): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-6) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-6) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#talks-6)

---

# General

## Readings

* Comparison of executable file formats - https://en.wikipedia.org/wiki/Comparison_of_executable_file_formats
* Executable and object file formats - https://en.wikipedia.org/wiki/Template:Executables
* Linux Foundation Referenced Specifications: ABI, ELF, DWARF - https://refspecs.linuxfoundation.org/
* Visual Documentation - File formats - Executables: ELF, Mach-O, PE (SVG and PDF available)
	+ https://github.com/corkami/pics/blob/master/binary/README.md#executables
	+ elf101: https://github.com/corkami/pics/tree/master/binary/elf101
	+ macho101: https://github.com/corkami/pics/tree/master/binary/macho101
	+ pe101: https://github.com/corkami/pics/tree/master/binary/pe101
	+ pe102: https://github.com/corkami/pics/tree/master/binary/pe102

## Software

* bingrep: Greps through binaries from various OSs and architectures, and colors them (ELF, Mach-O, PE)
	+ https://github.com/m4b/bingrep
* Bloaty McBloatface: a size profiler for binaries (ELF, Mach-O) - https://github.com/google/bloaty
	+ http://blog.reverberate.org/2016/11/07/introducing-bloaty-mcbloatface.html
* codesize: Code size visualization tool with PDB/ELF/Mach-O support
	+ https://github.com/zeux/codesize
* FileBytes
	+ Library to read and edit files in the following formats: Executable and Linking Format (ELF), Portable Executable (PE), MachO and OAT (Android Runtime)
	+ https://scoding.de/filebytes-introduction
	+ https://github.com/sashs/filebytes/
* LIEF - Library to Instrument Executable Formats
	+ The purpose of this project is to provide a cross platform library which can parse, modify and abstract ELF, PE and MachO formats.
	+ https://github.com/lief-project/LIEF
	+ https://lief.quarkslab.com/
* Pyew - https://github.com/joxeankoret/pyew
	+ Pyew is a (command line) python tool to analyse malware. It does have support for hexadecimal viewing, disassembly (Intel 16, 32 and 64 bits), PE and ELF file formats (it performs code analysis and let you write scripts using an API to perform many types of analysis), follows direct call/jmp instructions in the interactive command line, displays function names and string data references; supports OLE2 format, PDF format and more. It also supports plugins to add more features to the tool.
* Ropper - ROP gadget finder and binary information tool (ELF, PE, Mach-O)
	+ https://scoding.de/ropper/
	+ https://github.com/sashs/ropper

## Talks

* The Life of Binaries
	+ http://www.opensecuritytraining.info/LifeOfBinaries.html
	+ https://www.youtube.com/playlist?list=PLUFkSN0XLZ-n_Na6jwqopTt1Ki57vMIc3

---

# DLL

## Readings

* DLLs and Visual C++ run-time library behavior - https://docs.microsoft.com/en-us/cpp/build/run-time-library-behavior
* Dynamic-Link Library Best Practices - https://msdn.microsoft.com/library/windows/desktop/dn633971.aspx

## Software

* Dependency Walker - http://www.dependencywalker.com/
* Detours - https://www.microsoft.com/en-us/research/project/detours/
* EasyHook
	+ https://easyhook.github.io/
	+ https://github.com/EasyHook/EasyHook
* GNU Binary Utilities - https://sourceware.org/binutils/docs/binutils/
	+ dlltool: Create files needed to build and use DLLs - https://sourceware.org/binutils/docs/binutils/dlltool.html
* MemoryModule: Library to load a DLL from memory
	+ https://github.com/fancycode/MemoryModule
	+ https://www.joachim-bauch.de/tutorials/loading-a-dll-from-memory/
* Reflective DLL Injection with PowerShell - https://clymb3r.wordpress.com/2013/04/06/reflective-dll-injection-with-powershell/
* ReflectiveDLLInjection - https://github.com/stephenfewer/ReflectiveDLLInjection
* ThreadContinue: Reflective DLL injection using SetThreadContext() and NtContinue()
	+ https://github.com/zerosum0x0/ThreadContinue
	+ https://zerosum0x0.blogspot.com/2017/07/threadcontinue-reflective-injection.html
* What is so special about the instance handle 0x10000000? - https://blogs.msdn.microsoft.com/oldnewthing/20121227-00/?p=5713/

## Talks

* 2017 - “Everything You Ever Wanted to Know about DLLs” - James McNellis, CppCon
	+ https://www.youtube.com/watch?v=JPQWQfDhICA
	+ https://github.com/CppCon/CppCon2017/blob/master/Presentations/Everything%20You%20Ever%20Wanted%20to%20Know%20about%20DLLs/

---

# DWARF

* DWARF Debugging Standard Website - http://dwarfstd.org/
* DWARF Debugging Standard Wiki - http://wiki.dwarfstd.org/

## Readings

* An interesting tree serialization algorithm from DWARF - https://eli.thegreenplace.net/2011/09/29/an-interesting-tree-serialization-algorithm-from-dwarf
* David A's DWARF Page - https://www.prevanders.net/dwarf.html
* Debugging formats DWARF and STAB - https://www.ibm.com/developerworks/library/os-debugging/
* DWARF Extensions for Separate Debug Information Files - https://gcc.gnu.org/wiki/DebugFission
* DWARF Package File Format - https://gcc.gnu.org/wiki/DebugFissionDWP
* Exploring the DWARF debug format information - https://www.ibm.com/developerworks/aix/library/au-dwarf-debug-format/index.html
* How debuggers work: Part 3 - Debugging information - http://eli.thegreenplace.net/2011/02/07/how-debuggers-work-part-3-debugging-information
* Implementing a Debugger: The Fundamentals - https://backtrace.io/blog/debugger-internals/
* Introduction to the DWARF Debugging Format - http://www.dwarfstd.org/doc/Debugging%20using%20DWARF.pdf
* Programmatic access to the call stack in C++ - https://eli.thegreenplace.net/2015/programmatic-access-to-the-call-stack-in-c/
* Querying DWARF For Fun And Profit - https://developers.redhat.com/blog/2015/01/22/querying-dwarf-for-fun-and-profit/
* The contents of DWARF sections - https://eli.thegreenplace.net/2011/12/26/the-contents-of-dwarf-sections
* Using COMDAT Sections to Reduce the Size of DWARF Debug Information - https://gcc.gnu.org/wiki/DwarfSeparateTypeInfo
* Where are your symbols, debuginfo and sources? - https://gnu.wildebeest.org/blog/mjw/2016/02/02/where-are-your-symbols-debuginfo-and-sources/
* Writing a Linux Debugger Part 4: Elves and dwarves - https://blog.tartanllama.xyz/writing-a-linux-debugger-elf-dwarf/

## Software

* DIVA - Debug Information Visual Analyzer
	+ DIVA is a command line tool that processes DWARF debug information contained within ELF files and prints the semantics of that debug information. The DIVA output is designed to be understandable by software programmers without any low-level compiler or DWARF knowledge; as such, it can be used to report debug information bugs to the compiler provider.
	+ https://github.com/SNSystems/DIVA
	+ 2017 EuroLLVM Developers’ Meeting lightning talk
		- video: https://www.youtube.com/watch?v=SwtpXaCk2bE
		- slides: http://llvm.org/devmtg/2017-03/assets/slides/diva_debug_information_visual_analyzer.pdf
* dwarfidl: Language, library and tools for DWARF-described interfaces - https://github.com/stephenrkell/dwarfidl
* dwgrep: a tool, an associated language (Zwerg), and a library (libzwerg) for querying Dwarf (debuginfo) graphs
	+ project: https://github.com/pmachata/dwgrep
	+ syntax: http://pmachata.github.io/dwgrep/syntax.html
	+ tutorial: http://pmachata.github.io/dwgrep/tutorial.html
	+ website: http://pmachata.github.io/dwgrep/
* dwz: DWARF optimization and duplicate removal tool
	+ https://sourceware.org/git/?p=dwz.git
	+ https://fedoraproject.org/wiki/Features/DwarfCompressor
	+ announcement (2012) - https://gcc.gnu.org/ml/gcc/2012-04/msg00686.html
* libbacktrace: A C library that may be linked into a C/C++ program to produce symbolic backtraces
	+ As of September 2016, libbacktrace only supports ELF and PE/COFF executables with DWARF debugging information. The library is written to make it straightforward to add support for other object file and debugging formats.
	+ https://github.com/ianlancetaylor/libbacktrace
	+ https://github.com/gcc-mirror/gcc/tree/master/libbacktrace
* libdwarf - DWARF debugging information - https://sourceforge.net/projects/libdwarf/
	+ Libdwarf And Dwarfdump - http://wiki.dwarfstd.org/index.php?title=Libdwarf_And_Dwarfdump
* libdwarfpp: A high-level API for accessing DWARF debugging information, in C++ - https://github.com/stephenrkell/libdwarfpp
* llvm-dwarfdump - dump and verify DWARF debug information - https://llvm.org/docs/CommandGuide/llvm-dwarfdump.html

## Talks

* 2017 - Consistent Views at Recommended Breakpoints (bis), GNU Tools Cauldron 2017
	+ https://slideslive.com/38902686/consistent-views-at-recommended-breakpoints-bis
	+ Related post: https://developers.redhat.com/blog/2017/07/11/statement-frontier-notes-and-location-views/
* 2017 - Build-ids, symbols and debuginfo tooling BoF, GNU Tools Cauldron 2017
	+ https://slideslive.com/38902681/buildids-symbols-and-debuginfo-tooling-bof
* 2016 - Cheap generation of debugging information - http://pauillac.inria.fr/~xleroy/talks/Compilation-2016.pdf
* 2016 - Fixing LTO Debug Information - GNU Tools Cauldron 2016 - https://gcc.gnu.org/wiki/cauldron2016?action=AttachFile&do=view&target=Cauldron2016-LTOEarlyDebug.pdf - https://www.youtube.com/watch?v=xtm7DxDG5js
* 2015 - What is new in DWARF5 - Hafiz Abid Qadeer, GNU Tools Cauldron 2015
	+ https://www.youtube.com/watch?v=Q04ScFDCmyQ&gl=CA
	+ https://gcc.gnu.org/wiki/cauldron2015?action=AttachFile&do=view&target=Hafiz+Abid+Qadeer_+What+is+new+in+DWARF5.pdf
* 2013 - DWARF What Should GCC Tell GDB - GNU Tools Cauldron 2013 - https://www.youtube.com/watch?v=2aWmp5FXLb0
* 2012 - Dwarf Oriented Programming - Overwriting the Exception Handling Cache Pointer - DEFCON 20
	+ https://www.youtube.com/watch?v=FjjTZatJ3ao
	+ https://www.defcon.org/images/defcon-20/dc-20-presentations/Branco-Oakley-Bratus/DEFCON-20-Branco-Oakley-Bratus-Dwarf-Oriented-Programming.pdf
* 2011 - Exploiting the hard-working DWARF: Trojan and Exploit Techniques With No Native Executable Code
	+ http://www.cs.dartmouth.edu/~sergey/battleaxe/
	+ Slides: http://www.cs.dartmouth.edu/~sergey/battleaxe/hackito_2011_oakley_bratus.pdf
	+ Report: http://www.cs.dartmouth.edu/reports/TR2011-688.pdf
	+ Paper: https://www.usenix.org/legacy/event/woot11/tech/final_files/Oakley.pdf
	+ Video (WOOT'11): https://www.usenix.org/conference/woot11/exploiting-hard-working-dwarf-trojan-and-exploit-techniques-no-native-executable
	+ Video (Shmoocon 2011): https://www.youtube.com/watch?v=nLH7ytOTYto

---

# ELF

* ELF and ABI Standards - Linux Foundation Referenced Specifications - http://refspecs.linuxfoundation.org/elf/
* ELF101 a Linux executable walkthrough - https://speakerdeck.com/ange/booklet-elf101-a-linux-executable-walkthrough
* Learning Linux Binary Analysis (2016) - Ryan O'Neill - http://www.bitlackeys.org/#research
* linux-re-101
	+ https://github.com/michalmalik/linux-re-101
	+ https://libraries.io/github/michalmalik/linux-re-101
* References - SkyFree.org - http://www.skyfree.org/linux/references/references.html

## Readings

* About ELF Auxiliary Vectors - http://articles.manugarg.com/aboutelfauxiliaryvectors
* A Whirlwind Tutorial on Creating Really Teensy ELF Executables for Linux
	+ http://www.muppetlabs.com/~breadbox/software/tiny/teensy.html
	+ https://github.com/abraithwaite/teensy
* Building an ELF Parser with Frida - https://versprite.com/og/frida/
* Cheating the ELF: Subversive Dynamic Linking to Libraries - https://grugq.github.io/docs/subversiveld.pdf
* Constructing the ELF - A Magnetized Needle and a Steady Hand - http://nullprogram.com/blog/2016/11/17/
* Custom ELF program headers—what, why and how - http://www.cl.cam.ac.uk/~srk31/blog/2017/02/14/
	+ Rag-bag of utilities and scripts that do strange things with ELF files - https://github.com/stephenrkell/elftin/
* ELF - No Section Header? No Problem - https://em386.blogspot.com/2006/10/elf-no-section-header-no-problem.html
* ELF Hello World Tutorial
	+ http://www.cirosantilli.com/elf-hello-world/
	+ https://github.com/cirosantilli/cirosantilli.github.io/blob/master/elf-hello-world.md
* ELF Parsing Bugs by Example with Melkor Fuzzer
	+ https://ioactive.com/pdfs/IOActive_ELF_Parsing_with_Melkor.pdf
	+ http://blog.ioactive.com/2014/11/elf-parsing-bugs-by-example-with-melkor.html
* ELF shared library injection forensics - https://backtrace.io/blog/elf-shared-library-injection-forensics/
* ELF symbol lookup
	+ ELF: symbol lookup via DT_HASH - https://flapenguin.me/2017/04/24/elf-lookup-dt-hash/
	+ ELF: better symbol lookup via DT_GNU_HASH - https://flapenguin.me/2017/05/10/elf-lookup-dt-gnu-hash/
* ELFs are dorky, Elves are cool - Sergey Bratus and Julian Bangert - PoC||GTFO 00 - https://greatscottgadgets.com/pocorgtfo/pocorgtfo00.pdf
* ELF: From The Programmer's Perspective (1995) - http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.37.8698
* ELF, libelf, compressed sections and elfutils - https://gnu.wildebeest.org/blog/mjw/2016/01/13/elf-libelf-compressed-sections-and-elfutils/
* Eli Bendersky - Linkers and loaders - http://eli.thegreenplace.net/tag/linkers-and-loaders
	+ Load-time relocation of shared libraries - https://eli.thegreenplace.net/2011/08/25/load-time-relocation-of-shared-libraries
	+ Position Independent Code (PIC) in shared libraries - https://eli.thegreenplace.net/2011/11/03/position-independent-code-pic-in-shared-libraries
	+ Position Independent Code (PIC) in shared libraries on x64 - https://eli.thegreenplace.net/2011/11/11/position-independent-code-pic-in-shared-libraries-on-x64
	+ How statically linked programs run on Linux - https://eli.thegreenplace.net/2012/08/13/how-statically-linked-programs-run-on-linux
	+ Library order in static linking - https://eli.thegreenplace.net/2013/07/09/library-order-in-static-linking
* Exploiting ELF Expansion Variables - https://backtrace.io/blog/exploiting-elf-expansion-variables/
* Generating executable files from scratch - https://github.com/cameronswinoga/yabfc/wiki/Generating-executable-files-from-scratch
* Good Practices in Library Design, Implementation, and Maintenance - https://www.akkadia.org/drepper/goodpractice.pdf
* How is a binary executable organized? Let's explore it! - https://jvns.ca/blog/2014/09/06/how-to-read-an-executable/
* How To Write Shared Libraries - https://www.akkadia.org/drepper/dsohowto.pdf
* I/O patterns on ELF binary initialization - https://glandium.org/blog/?p=1016
* Improving binary layout for progressive decompression (2011) - https://glandium.org/blog/?p=2320
* In the lands of corrupted elves: Breaking ELF software with Melkor fuzzer - https://www.blackhat.com/docs/us-14/materials/arsenal/us-14-Hernandez-Melkor-Slides.pdf
* Linux Internals - Dynamic Linking Wizardry - https://0x00sec.org/t/linux-internals-dynamic-linking-wizardry/1082
* Linux Internals - The Art Of Symbol Resolution - https://0x00sec.org/t/linux-internals-the-art-of-symbol-resolution/1488
* Programming With Ones and Zeros
	+ Part 1 - http://www.hanshq.net/ones-and-zeros.html
	+ Ones and Zeros, Part 2: Making Executable Files - http://www.hanshq.net/making-executables.html
* Linux x86 Program Start Up (dynamically loaded x86 ELF files) - http://dbp-consulting.com/tutorials/debugging/linuxProgramStartup.html
* RE a 64bit ELF binary - Devil’s swapper write-up - https://0x00sec.org/t/re-a-64bit-elf-binary-devils-swapper-write-up/2379
* Relocations in ELF Toolchains - https://www.sifive.com/blog/2017/08/21/all-aboard-part-2-relocations/
* Resolving ELF Relocation Name / Symbols - https://em386.blogspot.com/2006/10/resolving-elf-relocation-name-symbols.html
* Smallest x86 ELF Hello World - http://timelessname.com/elfbin/
* Targeting File Parsers with S2E and Kaitai Struct - targeted symbolic execution of readelf - https://adrianherrera.github.io/post/kaitai-s2e/
* The Anatomy of an Executable - dissection of a simple "hello world" ELF binary - https://github.com/mewrev/dissection
* The ELF Object File Format by Dissection (1995) - http://www.linuxjournal.com/article/1060
* The Executable and Linkable Format (ELF)
	+ https://publicclu2.blogspot.com/2013/05/executable-and-linkable-format-elf.html
	+ https://www.cs.stevens.edu/~jschauma/810/elf.html
	+ http://web.archive.org/web/20120415084409/http://www.acsu.buffalo.edu:80/~charngda/elf.html
* Tweaking binaries with elfedit - https://ptribble.blogspot.com/2017/06/tweaking-binaries-with-elfedit.html
* Uncovering a few SIGSEGVs in binutils' BFD and GLIBC
	+ https://chatsubo-labs.blogspot.com/2017/05/uncovering-few-sigsegvs-in-binutils-bfd.html
	+ http://brainoverflow.org/papers/BFD-GLIBC_Fuzzing/0%20Uncovering%20a%20few%20SIGSEGVs%20in%20binutils'%20BFD%20and%20GLIBC.pdf
* Understanding Linux ELF RTLD internals - http://s.eresi-project.org/inc/articles/elf-rtld.txt
* 'Weird Machine' patterns - https://www.researchgate.net/publication/283630248_%27Weird_Machine%27_patterns
* Writing shared libraries - http://plan99.net/~mike/writing-shared-libraries.html

## Software

* ABI Dumper - a tool to dump ABI of an ELF object containing DWARF debug info - https://github.com/lvc/abi-dumper
* abidiff - compares the Application Binary Interfaces (ABI) of two shared libraries in ELF format
	+ https://sourceware.org/libabigail/manual/abidiff.html
	+ Comparing ABIs for Compatibility with libabigail – Part 1 - https://developers.redhat.com/blog/2014/10/23/comparing-abis-for-compatibility-with-libabigail-part-1/
	+ Comparing ABIs for Compatibility with libabigail – Part 2 - https://developers.redhat.com/blog/2014/10/28/comparing-abis-for-compatibility-libabigail-part-2/
	+ Talk: Libabigail: How semantic analysis of C and C++ ELF binaries can be used to analyze ABI changes (openSUSE Conference 2017)
		- https://media.ccc.de/v/1234-libabigail-how-semantic-analysis-of-c-and-c-elf-binaries-can-be-used-to-analyze-abi-changes
		- https://www.youtube.com/watch?v=wxVBuZK8Dl0
* dress: add symbols back into a stripped ELF binary (~strip)
	+ http://van.prooyen.com/projects/#dress
	+ https://github.com/docileninja/dress
	+ http://van.prooyen.com/reversing/2016/10/30/Fuckzing-reverse-Writeup.html
* elf-bf-tools - https://github.com/bx/elf-bf-tools
	+ This project contains tools that can be used to coerce the gcc's runtime loader into performing interesting operations using only valid relocation entries and symbols.
* ELF Tool Chain Project - https://sourceforge.net/projects/elftoolchain/
	+ A BSD-licensed implementation of compilation tools (nm, ar, as, ld, etc.) for the ELF object format.
* ELFbac: runtime intent-level ABI-granular memory protection for Linux - http://elfbac.org/
* Elfesteem: Executable file format parser/generator - https://github.com/serpilliere/elfesteem
* Elfhack: to optimize ELF binaries for size and cold startup speed - https://github.com/mozilla/positron/tree/master/build/unix/elfhack
* ELFIO - ELF (Executable and Linkable Format) reader and producer implemented as a header only C++ library
	+ http://serge1.github.io/ELFIO 
	+ https://github.com/serge1/ELFIO
	+ https://mcuoneclipse.com/2013/04/14/text-data-and-bss-code-and-data-size-explained/
* ELFkickers (ebfc, elfls, elftoc, infect, objres, rebind, sstrip) - http://www.muppetlabs.com/~breadbox/software/elfkickers.html
* elfutils
	+ a collection of utilities and libraries to read, create and modify ELF binary files, find and handle DWARF debug data, symbols, thread state and stacktraces for processes and core files on GNU/Linux
	+ https://sourceware.org/elfutils/
* GNU Binary Utilities - https://sourceware.org/binutils/docs/binutils/
	+ elfedit: Update the ELF header of ELF files - https://sourceware.org/binutils/docs/binutils/elfedit.html
	+ nm: List symbols from object files - https://sourceware.org/binutils/docs/binutils/nm.html
	+ readelf: Display the contents of ELF format files - https://sourceware.org/binutils/docs/binutils/readelf.html
	+ size: List section sizes and total size - https://sourceware.org/binutils/docs/binutils/size.html
		- examples:  
		  http://www.geeksforgeeks.org/memory-layout-of-c-program/
		  Check Size of Code, Data, and .BSS Segments - http://cs-fundamentals.com/c-programming/memory-layout-of-c-program-code-data-segments.php#size-of-code-data-bss-segments
* Libelf - ELF object file access library - http://www.mr511.de/software/english.html
	+ libelf-howto - http://chris.rohlf.googlepages.com/libelf-howto.c
* Libelfin: C++11 ELF/DWARF parser - a from-scratch C++11 library for reading ELF binaries and DWARFv4 debug information - https://github.com/aclements/libelfin
* Melkor - An ELF File Format Fuzzer - https://github.com/IOActive/Melkor_ELF_Fuzzer
* objdump beautifier - https://github.com/diouziou/bod
	+ Supported Targets: elf32-littlearm, elf32-tradlittlemips, elf32-i386, elf64-x86-64
* PatchELF: A small utility to modify the dynamic linker and RPATH of ELF executables
	+ http://nixos.org/patchelf.html
	+ https://github.com/nixos/patchelf
* patchkit - https://github.com/lunixbochs/patchkit
	+ Patches an ELF binary using one or more simple Python scripts.
* pyelftools: Pure-python library for parsing ELF and DWARF - https://github.com/eliben/pyelftools
* syms2elf: a plugin to export the symbols recognized to the ELF symbol table 
	+ Hex-Ray's IDA Pro and radare2 - https://github.com/danigargu/syms2elf
	+ Binary Ninja - https://github.com/monosource/syms2elf
* The ERESI Reverse Engineering Software Interface: ELFsh (ELF shell), Embedded ELF Debugger (e2dbg)
	+ http://www.eresi-project.org
	+ https://github.com/thorkill/eresi
	+ https://github.com/thorkill/eresi/wiki/EresiArticles
	+ Next-Generation Debuggers For Reverse Engineering:
		- https://www.blackhat.com/presentations/bh-europe-07/ERSI/Presentation/bh-eu-07-ersi-apr19.pdf
		- https://www.blackhat.com/presentations/bh-europe-07/ERSI/Whitepaper/bh-eu-07-ersi-WP-apr19.pdf
		- https://www.ekoparty.org/archivo/2007/eko3-Julio%20Auto%20-%20Next-Generation%20Debuggers%20For%20Reverse%20Engineering.pdf
* Vtable-Dumper - a tool to list content of virtual tables in a C++ shared library - https://github.com/lvc/vtable-dumper

## Talks

* 2017 - ELF linking: what it means and why it matters - Stephen Kell (2017) - https://www.cl.cam.ac.uk/~srk31/research/talks/kell17elf-slides.pdf
* 2017 - FOSDEM 2017 - Everything You Always Wanted to Know About "Hello, World"* (*But Were Afraid To Ask)
	+ https://archive.fosdem.org/2017/schedule/event/hello_world/
	+ https://people.freebsd.org/~brooks/talks/fosdem2017-helloworld/?C=M&O=D
* 2017 - FOSDEM 2017 - LLD from a user's perspective
	+ https://archive.fosdem.org/2017/schedule/event/lld/
	+ https://archive.fosdem.org/2017/schedule/event/lld/attachments/slides/1446/export/events/attachments/lld/slides/1446/FosdemLLD2017.pdf
* 2016 - !!Con 2016L Debugging debuggers!! (Symbolic Debugging with DWARF) - Samy Al Bahra
	+ https://backtrace.io/blog/symbolic-debugging-with-dwarf/
	+ https://www.youtube.com/watch?v=OEa0EfJja_Y
* 2016 - BlackHat USA 2016: Intra-Process Memory Protection for Applications on ARM and X86: Leveraging the ELF ABI
	+ https://www.youtube.com/watch?v=YXh2aIc9u64
	+ Slides: http://www.cs.dartmouth.edu/~sergey/io/elfbac/bh16-elfbac-slides.pdf
	+ Whitepaper: http://www.cs.dartmouth.edu/~sergey/io/elfbac/bh16-elfbac-whitepaper.pdf
* 2016 EuroLLVM Developers' Meeting: R. Ueyama "New LLD linker for ELF"
	+ https://www.youtube.com/watch?v=CYCRqjVa6l4
* 2015 - DEF CON 23 - Di Federico and Shoshitaishvili - Dark Side of the ELF
	+ https://www.youtube.com/watch?v=aGoDYa7Kbec
* 2015 - How the ELF Ruined Christmas - USENIX Security Symposium 2015
	+ https://www.usenix.org/conference/usenixsecurity15/technical-sessions/presentation/di-frederico
* 2014 - ABIs, linkers and other animals - Stephen Kell (2014) - https://www.cl.cam.ac.uk/~srk31/research/talks/kell14abis-slides.pdf
* 2013 - Julian Bangert, Sergey Bratus - ELF Eccentricities
	+ https://www.youtube.com/watch?v=4LU6N6THh2U
* 2013 - Rebecca Bx Shapiro, Julian Bangert, Sergey Bratus Any Input Is a Program Weird Machines in ABI
	+ https://www.youtube.com/watch?v=crt5gxOoUuM
* 2013 - "Weird Machines" in ELF: A Spotlight on the Underappreciated Metadata
	+ USENIX  Workshop on Offensive Technologies (WOOT '13)
	+ https://www.usenix.org/conference/woot13/workshop-program/presentation/shapiro
	+ http://www.cs.dartmouth.edu/~sergey/wm/woot13-shapiro.pdf
	+ https://www.youtube.com/watch?v=6xbirzvr-mQ
* 2012 - DEF CON 20: Rebecca "bx" Shapiro and Sergey Bratus - Programming Weird Machines with ELF Metadata
	+ https://www.youtube.com/watch?v=V5KsUm1KfZE
	+ https://www.youtube.com/watch?v=YgtxxLCVD-o
	+ http://cs.dartmouth.edu/~bx/elf-bf-tools/slides/elf-defcon20.pdf

---

# Mach-O

* Mach-O Runtime Architecture - http://math-atlas.sourceforge.net/devel/assembly/MachORuntime.pdf
* Mach-O Programming Topics - https://developer.apple.com/library/content/documentation/DeveloperTools/Conceptual/MachOTopics/0-Introduction/introduction.html
* OS X ABI Mach-O File Format Reference
	+ https://github.com/aidansteele/osx-abi-macho-file-format-reference
	+ PDF: https://pewpewthespells.com/re/Mach-O_File_Format.pdf
* Reverse Engineering/Mac OS X - https://en.wikibooks.org/wiki/Reverse_Engineering/Mac_OS_X

## Readings

* Basics of the Mach-O file format - https://samhuri.net/posts/2010/01/basics-of-the-mach-o-file-format/
* Dynamic Linking: ELF vs. Mach-O - http://timetobleed.com/dynamic-linking-elf-vs-mach-o/
* Dynamic symbol table duel: ELF vs Mach-O, round 2 - http://timetobleed.com/dynamic-symbol-table-duel-elf-vs-mach-o-round-2/
* DYLD Detayled - The internals of DYLD, the dynamic linker, and the `__LINKEDIT` section - http://newosxbook.com/articles/DYLD.html
* Friday Q&A 2012-04-27: PLCrashReporter and Unwinding the Stack With DWARF - https://www.mikeash.com/pyblog/friday-qa-2012-04-27-plcrashreporter-and-unwinding-the-stack-with-dwarf.html
* Friday Q&A 2012-05-04: PLCrashReporter and Unwinding the Stack With DWARF, Part 2 - https://www.mikeash.com/pyblog/friday-qa-2012-05-04-plcrashreporter-and-unwinding-the-stack-with-dwarf-part-2.html
* Friday Q&A 2012-11-09: dyld: Dynamic Linking On OS X - https://www.mikeash.com/pyblog/friday-qa-2012-11-09-dyld-dynamic-linking-on-os-x.html
* Friday Q&A 2012-11-30: Let's Build A Mach-O Executable - https://www.mikeash.com/pyblog/friday-qa-2012-11-30-lets-build-a-mach-o-executable.html
* Mach-O Binaries - http://www.m4b.io/reverse/engineering/mach/binaries/2015/03/29/mach-binaries.html
* Mach-O Executables - https://www.objc.io/issues/6-build-tools/mach-o-executables/
* Parsing Mach-O files - https://lowlevelbits.org/parsing-mach-o-files/
* Playing with Mach-O binaries and dyld
	+ https://blog.lse.epita.fr/articles/82-playing-with-mach-os-and-dyld.html
	+ https://lse.epita.fr/data/lt/2017-03-14/lt-2017-03-14-Stanislas_Lejay-Playing_with_machos_and_dyld.pdf

## Software

* jtool: (Mach-O Analyzer) - http://www.newosxbook.com/tools/jtool.html
* MacDependency: shows all dependent libraries and frameworks of a given executable, dynamic library or framework on Mac OS X
	+ https://github.com/kwin/macdependency/
* mach_override: runtime function overriding for Mac OS X - https://github.com/rentzsch/mach_override
* MachoAnalysis: collection of analysis utils - https://github.com/eeeyes/macho_analysis
* macholibre: Mach-O & Universal Binary Parser - https://github.com/aaronst/macholibre
	+ Mach-O Libre: Pile Driving Apple Malware with Static Analysis, Big-Data, and Automation - https://www.first.org/resources/papers/conf2016/FIRST-2016-130.pdf
* Machotools - "a small set of tools built on top of macholib to retrieve and change informations about mach-o files. Think of it as a pure python, cross-platform implementation of install_name_tool"
	+ https://github.com/enthought/machotools
* MachOView: a visual Mach-O file browser - https://sourceforge.net/projects/machoview/

## Talks

* Mach-O Malware Analysis: Combatting Mac OSX/iOS Malware with Data Visualization
	+ https://infocon.org/cons/DEF%20CON/DEF%20CON%2021/DEF%20CON%2021%20presentations/Remy%20Baumgarten/
	+ https://infocon.org/cons/DEF%20CON/DEF%20CON%2021/DEF%20CON%2021%20presentations/Remy%20Baumgarten/DEFCON-21-Baumgarten-Mach-O-Viz.pdf
	+ https://infocon.org/cons/DEF%20CON/DEF%20CON%2021/DEF%20CON%2021%20presentations/Remy%20Baumgarten/DEFCON-21-Baumgarten-Mach-O-Viz-WP.pdf
	+ https://infocon.org/cons/DEF%20CON/DEF%20CON%2021/DEF%20CON%2021%20video%20and%20slides%20x265/DEF%20CON%2021%20Hacking%20Conference%20Presentation%20By%20Remy%20Baumgarten%20-%20Combatting%20Mac%20OSX%20iOS%20Malware%20with%20Data%20Visualization%20-%20Video%20and%20Slides.mp4
	+ http://macsecurity.net/view/42/
	+ http://www.securitytube.net/video/9133

---

# PDB (Program Database)

## Readings

* CodeView Debug Info Format - http://llvm.org/docs/SourceLevelDebugging.html#codeview-debug-info-format
* Jan Gray on inventing/implementing PDB files 1990-94 - https://twitter.com/jangray/status/659916997711544320
* LLVM on Windows now supports PDB Debug Info - http://blog.llvm.org/2017/08/llvm-on-windows-now-supports-pdb-debug.html
* PDB File Format - https://github.com/google/syzygy/wiki/PdbFileFormat
* PDB Files: What Every Developer Must Know - https://www.wintellect.com/pdb-files-what-every-developer-must-know
* PDB File Internals - http://www.informit.com/articles/article.aspx?p=22685
* PDB v2.0 File Format documentation - https://reverseengineering.stackexchange.com/questions/2548/pdb-v2-0-file-format-documentation
* radare2 PDB usage - https://github.com/radare/radare2/blob/master/doc/pdb/pdb_usage
* The PDB File Format - https://llvm.org/docs/PDB/
* The PDB Info Stream (aka the PDB Stream) - http://llvm.org/docs/PDB/PdbStream.html
* PDB Info Stream - https://www.reddit.com/r/programming/comments/6ukeuk/llvm_on_windows_now_supports_pdb_debug_info/dlvtucx/
* pdbparse - Stream Descriptions wiki - https://code.google.com/archive/p/pdbparse/wikis/StreamDescriptions.wiki
* Symbols the Microsoft Way - https://randomascii.wordpress.com/2013/03/09/symbols-the-microsoft-way/
* What’s inside a PDB File? - https://blogs.msdn.microsoft.com/vcblog/2016/02/08/whats-inside-a-pdb-file/

## Software

* Debug Interface Access SDK (DIA SDK) - provides access to debug information stored in PDB files - https://docs.microsoft.com/en-us/visualstudio/debugger/debug-interface-access/debug-interface-access-sdk
* llvm-pdbutil - PDB File forensics and diagnostics - https://llvm.org/docs/CommandGuide/llvm-pdbutil.html - https://github.com/llvm-mirror/llvm/tree/master/tools/llvm-pdbutil
* llvm-symbolizer - convert addresses into source code locations - https://llvm.org/docs/CommandGuide/llvm-symbolizer.html - https://github.com/Microsoft/llvm/tree/master/test/tools/llvm-symbolizer/pdb
* microsoft-pdb: Information from Microsoft about the PDB format - https://github.com/Microsoft/microsoft-pdb
* MSFViewer - viewing and understanding PDB Multi-Stream File (MSF) data - https://github.com/apoch/epoch-language/tree/master/Tools/MSFViewer
* pdbinfo:  displays information about PDB symbol files (timestamp, GUID, and age) - https://github.com/randomascii/tools/tree/master/pdbinfo
* PDBparse - Python code to parse Microsoft PDB files - https://github.com/moyix/pdbparse
* Syzygy Transformation Toolchain - PDB Module - https://github.com/google/syzygy/tree/master/syzygy/pdb

## Talks

* 2016 LLVM Developers’ Meeting: R. Kleckner "CodeView, the MS Debug Info Format in LLVM"
	+ https://www.youtube.com/watch?v=5twzd06NqGU
	+ http://www.llvm.org/devmtg/2016-11/Slides/Kleckner-CodeViewInLLVM.pdf

---

# PE

## Readings

* A smallest PE executable (x64) with every byte executed - https://drakopensulo.wordpress.com/2017/08/06/smallest-pe-executable-x64-with-every-byte-executed/
* Common Object File Format (COFF) - https://support.microsoft.com/en-us/help/121460/common-object-file-format-coff
* Dynamic Reconstruction of Relocation Information for Stripped Binaries - http://www.cs.columbia.edu/~vpappas/papers/reloc.raid14.pdf
* Introducing New Packing Method: First Reflective PE Packer Amber - https://pentest.blog/introducing-new-packing-method-first-reflective-pe-packer/
* Microsoft Portable Executable (PE) and Common Object File Format (COFF) Specification - https://msdn.microsoft.com/en-us/library/windows/desktop/ms680547.aspx
* PE (corkami wiki) - https://corkamiwiki.github.io/PE - https://github.com/corkami/docs/blob/master/PE/PE.md
* Portable Executable File Format – A Reverse Engineer View - http://www.stonedcoder.org/~kd/lib/CBJ-2005-74.pdf
* Peering Inside the PE: A Tour of the Win32 Portable Executable File Format - https://msdn.microsoft.com/en-us/library/ms809762.aspx
* Robust Static Analysis of Portable Executable Malware - Katja Hahn, Master Thesis - https://github.com/katjahahn/PortEx/tree/master/masterthesis
* The sad state of PE parsing - http://lucasg.github.io/2017/04/28/the-sad-state-of-pe-parsing/
* Tiny PE: Creating the smallest possible PE executable - http://www.phreedom.org/research/tinype/
* Undocumented PECOFF - https://media.blackhat.com/bh-us-11/Vuksan/BH_US_11_VuksanPericin_PECOFF_WP.pdf
* Why does a corrupted binary sometimes result in "Program too big to fit in memory"? - https://blogs.msdn.microsoft.com/oldnewthing/20060130-00/?p=32483
* Why is 0x00400000 the default base address for an executable? - https://blogs.msdn.microsoft.com/oldnewthing/20141003-00/?p=43923

## Software

* Adlice PEViewer - https://www.adlice.com/download/roguekillerpe/
* bearparser: Portable Executable parsing library - https://github.com/hasherezade/bearparser
* CFF Explorer - http://www.ntcore.com/exsuite.php
* ExpDiff: Diff tool for comparing export tables in PE images - https://github.com/WalkingCat/ExpDiff
* fasm_packer: PE Packer written in x86 assembly (FASM syntax) - https://github.com/DimitriFourny/resources/tree/master/fasm_packer
* Five PE Analysis Tools Worth Looking At - https://blog.malwarebytes.com/threat-analysis/2014/05/five-pe-analysis-tools-worth-looking-at/
* Manalyze, a static analyzer for PE executables - https://manalyzer.org/ - https://github.com/JusticeRage/Manalyze
* PEview - http://wjradburn.com/software/
* PE Insider - http://cerbero.io/peinsider/
* PE Tools - http://www.malware-analyzer.com/pe-tools
* PE-bear - https://hshrzd.wordpress.com/pe-bear/
* pe-parse - Principled, lightweight C/C++ PE parser - https://github.com/trailofbits/pe-parse 
* pe_armor: Metamorphic PE packer generated and assembled by a Python code - https://github.com/DimitriFourny/resources/tree/master/pe_armor
* pedump - dump windows PE files using Ruby - http://pedump.me/ - https://github.com/zed-0xff/pedump
* pestudio - https://www.winitor.com/
* PortEx: Java library to analyse Portable Executable files with a special focus on malware analysis and PE malformation robustness
	+ https://github.com/katjahahn/PortEx/
	+ http://katjahahn.github.io/PortEx/
	+ Robust Static Analysis of Portable Executable Malware - Katja Hahn, Master Thesis - https://github.com/katjahahn/PortEx/tree/master/masterthesis
	+ Wiki - https://github.com/katjahahn/PortEx/wiki
	+ PE Visualizer - https://github.com/katjahahn/PortEx/wiki/PE-Visualizer
* PPEE: A Professional PE File Explorer - https://www.mzrst.com/
* Sizer - Win32 executable size report utility - https://github.com/tsafin/pdb-sizer
* SymbolSort: A Utility for Measuring C++ Code Bloat
	+ https://github.com/adrianstone55/SymbolSort
	+ http://gameangst.com/?p=320

## Talks

* 2013 - 44Con 2013 - Exploring the Portable Executable format - Ange Albertini
	+ https://speakerdeck.com/ange/workshop-exploring-the-portable-executable-format
* 2013 - NoVA Hackers - 2013-03-11 - Joshua Pitts - Backdooring Win32 Portable Executables
	+ https://www.youtube.com/watch?v=SXaoVo_U7kA
* 2012 - Hack in Paris 2012 - Ange Albertini A Bit More of PE
	+ https://www.youtube.com/watch?v=3duSgr5b1yc
	+ https://www.youtube.com/watch?v=6HRfuN-fPwM
* 2012 - Hashdays 2012 - Byte-ing the PE that fails you - Ange Albertini
	+ https://www.youtube.com/watch?v=kibEcaG0zCk
	+ https://speakerdeck.com/ange/byte-ing-the-pe-that-fails-you
* 2011 - Berlinsides - x86 & PE - Ange Albertini - https://speakerdeck.com/ange/x86-and-pe
* 2011 - BlackHat 2011 - Constant Insecurity: Things you didn’t know about (PE) Portable Executable file format
	+ https://www.youtube.com/watch?v=uoQL3CE24ls
	+ https://www.reversinglabs.com/newsroom/blog/constant-insecurity-things-you-didnt-know-about-pe-portable-executable-file-format.html
	+ Paper - Undocumented PECOFF: https://media.blackhat.com/bh-us-11/Vuksan/BH_US_11_VuksanPericin_PECOFF_WP.pdf
	+ Slides: https://media.blackhat.com/bh-us-11/Vuksan/BH_US_11_VuksanPericin_PECOFF_Slides.pdf
