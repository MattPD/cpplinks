# [C++ links](README.md): executable and object file formats (ELF, Mach-O, PE); debugging data formats (DWARF, PDB): articles, documentation, software, and talks.

Executable files, debugging data, object code, shared libraries - file formats information, specifications, software - with relevance to compiler toolchains, debuggers, and general program analysis.

Organization: Preference given to the most specific category -- e.g., if an article discusses DLL-specific information, then it belongs to the DLL section (in preference to the more general PE).

See also: [compilers](compilers.md)

Contents:

* [General](#general): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#general-talks)
* [DLL](#dll): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-1) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-1) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#dll-talks)
* [DWARF](#dwarf): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-2) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-2) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#dwarf-talks)
* [ELF](#elf): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-3) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-3) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#elf-talks)
* [Mach-O](#mach-o): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-4) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-4) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#mach-o-talks)
* [PDB](#pdb): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-5) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-5) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#pdb-talks)
* [PE](#pe): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-6) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-6) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#pe-talks)

---

# General

## Readings

* Comparison of executable file formats - https://en.wikipedia.org/wiki/Comparison_of_executable_file_formats
* Executable and object file formats - https://en.wikipedia.org/wiki/Template:Executables
* From Hack to Elaborate Technique—A Survey on Binary Rewriting
	- ACM Computing Surveys 52(3) 2019
	- Matthias Wenzl, Georg Merzdovnik, Johanna Ullrich, and Edgar Weippl
	- https://dl.acm.org/citation.cfm?doid=3341324.3316415
	- https://publications.sba-research.org/publications/201906%20-%20GMerzdovnik%20-%20From%20hack%20to%20elaborate%20technique.pdf
* Linux Foundation Referenced Specifications: ABI, ELF, DWARF - https://refspecs.linuxfoundation.org/
* Type Inference on Executables
	+ ACM Computing Surveys, Vol. 48, No. 4, Article 65, 2016
	+ Juan Caballero and Zhiqiang Lin
	+ https://www.utdallas.edu/~zxl111930/file/CSUR16.pdf
	+ http://web.cse.ohio-state.edu/~lin.3021/file/CSUR16.pdf
* Visual Documentation - File formats - Executables: ELF, Mach-O, PE (SVG and PDF available)
	+ https://github.com/corkami/pics/blob/master/binary/README.md#executables
	+ elf101: https://github.com/corkami/pics/tree/master/binary/elf101
	+ macho101: https://github.com/corkami/pics/tree/master/binary/macho101
	+ pe101: https://github.com/corkami/pics/tree/master/binary/pe101
	+ pe102: https://github.com/corkami/pics/tree/master/binary/pe102

## Software

* Backdoor Factory (BDF): patch PE, ELF, Mach-O binaries with shellcode - https://github.com/secretsquirrel/the-backdoor-factory
* bingrep: Greps through binaries from various OSs and architectures, and colors them (ELF, Mach-O, PE)
	+ https://github.com/m4b/bingrep
* Bloaty McBloatface: a size profiler for binaries (ELF, Mach-O) - https://github.com/google/bloaty
	+ http://blog.reverberate.org/2016/11/07/introducing-bloaty-mcbloatface.html
	+ “(Ab)using Compiler Tools”; CppCon 2019; Reka Kovacs
		- https://www.youtube.com/watch?v=5Lke40ywMaU
		- https://github.com/CppCon/CppCon2019/tree/master/Presentations/abusing_compiler_tools
* Boost Dynamic Library Load (Boost.DLL): Library for comfortable work with DLL and DSO
	+ https://github.com/boostorg/dll
	+ https://www.boost.org/doc/libs/release/doc/html/boost_dll.html
* cave_miner: search for code cave in binaries (ELF, Mach-O, PE), and inject code in them - https://github.com/Antonin-Deniau/cave_miner
* codesize: Code size visualization tool with PDB/ELF/Mach-O support
	+ https://github.com/zeux/codesize
* ddbug - Display debugging information
	+ ddbug is a utility that can extract useful information from DWARF/PDB debugging data. Its goal is to use the debugging information to provide insights into the code generation.
	+ Supports: ELF files with DWARF, Mach-O files with DWARF, Windows PDB files (mimimal)
	+ https://github.com/gimli-rs/ddbug
* Delinker: Unlinks a binary executable to get back a set of .o object files for further transformation and re-linking.
	+ https://github.com/jnider/delinker
	+ Reverse the Linking Process
		- Compiler, Architecture, and Tools Conference (CATC) 2018
		- Joel Nider
		- https://software.intel.com/en-us/download/reverse-the-linking-process
* Detect-It-Easy: Program for determining types of files for Windows, Linux and MacOS
	- https://github.com/horsicq/Detect-It-Easy
* FileBytes
	+ Library to read and edit files in the following formats: Executable and Linking Format (ELF), Portable Executable (PE), MachO and OAT (Android Runtime)
	+ https://scoding.de/filebytes-introduction
	+ https://github.com/sashs/filebytes/
* Fileformat: A set of libraries and tools for representation, manipulation, and analysis of binary files in various object file formats
	+ COFF, ELF, Intel HEX, Mach-O, PE, raw data
	+ https://github.com/avast-tl/fileformat
* FunctionSimSearch
	+ Example C++ code to demonstrate how to do SimHash-based similarity search over CFGs extracted from disassemblies
	+ https://github.com/googleprojectzero/functionsimsearch
	+ Searching statically-linked vulnerable library functions in executable code
		- https://googleprojectzero.blogspot.com/2018/12/searching-statically-linked-vulnerable.html
* injectdso - A collection of tools for injecting DSOs - https://github.com/huku-/injectdso
* LIEF - Library to Instrument Executable Formats
	+ The purpose of this project is to provide a cross platform library which can parse, modify and abstract ELF, PE and MachO formats.
	+ https://github.com/lief-project/LIEF
	+ https://lief.quarkslab.com/
	+ references: https://lief.quarkslab.com/doc/latest/references.html
* Pyew - https://github.com/joxeankoret/pyew
	+ Pyew is a (command line) python tool to analyse malware. It does have support for hexadecimal viewing, disassembly (Intel 16, 32 and 64 bits), PE and ELF file formats (it performs code analysis and let you write scripts using an API to perform many types of analysis), follows direct call/jmp instructions in the interactive command line, displays function names and string data references; supports OLE2 format, PDF format and more. It also supports plugins to add more features to the tool.
* Qiew - Hex/File format viewer (ELF and PE plugins available) - https://github.com/mtivadar/qiew
* RetDec: a retargetable machine-code decompiler based on LLVM
	+ Supported file formats: ELF, PE, Mach-O, COFF, AR (archive), Intel HEX, and raw machine code.
	+ Supported architectures (32b only): Intel x86, ARM, MIPS, PIC32, and PowerPC.
	+ https://github.com/avast-tl/retdec
* Ropper - ROP gadget finder and binary information tool (ELF, PE, Mach-O)
	+ https://scoding.de/ropper/
	+ https://github.com/sashs/ropper
* Sample Binaries: Sample binary executables (for a number of architectures) for binary analysis testing
	+ https://github.com/GaloisInc/sample-binaries
* Samples of binary with different formats and architectures. A test suite for your binary analysis tools. (ELF, Mach-O, PE)
	+ https://github.com/JonathanSalwan/binary-samples
* symtool: Static symbol manipulation tool for ELF and Mach-O objects
	+ https://github.com/calebzulawski/symtool
	+ Changing symbol visibility
	+ Renaming symbols
	+ Actions are performed in-place, leaving the rest of the binary untouched
* The Witchcraft Compiler Collection  
	+ https://github.com/endrazine/wcc
	+ wld: The Witchcraft Linker
		- wld takes an ELF executable as an input and modifies it to create a shared library.
	+ wcc: The Witchcraft Compiler
		- The wcc compiler takes binaries (ELF, PE, ...) as an input and creates valid ELF binaries as an output. It can be used to create relocatable object files from executables or shared libraries.
	+ wsh: The Witchcraft shell
		- The witchcraft shell accepts ELF shared libraries, ELF ET_DYN executables and Witchcraft Shell Scripts written in Punk-C as an input. It loads all the executables in its own address space and makes their API available for programming in its embedded interpreter. This provides for binaries functionalities similar to those provided via reflection on languages like Java.
	+ wldd: print shared libraries compilation flags
	+ wcch: generate C headers from binaries

## General: Talks

* Reverse Engineering Binaries
	+ DevConf.CZ 2019; Divya Basant Kumar
	+ https://www.youtube.com/watch?v=TZVBK5hu0sk
* My Little Object File: How Linkers Implement C++
	+ CppCon 2017; Michael Spencer
	+ (ELF, MachO, COFF)
	+ https://www.youtube.com/watch?v=a5L66zguFe4
* The Life of Binaries
	+ http://www.opensecuritytraining.info/LifeOfBinaries.html
	+ https://www.youtube.com/playlist?list=PLUFkSN0XLZ-n_Na6jwqopTt1Ki57vMIc3

---

# DLL

## Readings

* DLLs and Visual C++ run-time library behavior - https://docs.microsoft.com/en-us/cpp/build/run-time-library-behavior
* Dynamic-Link Library Best Practices - https://msdn.microsoft.com/library/windows/desktop/dn633971.aspx
* Everything You Never Wanted To Know About DLLs - http://blog.omega-prime.co.uk/2011/07/04/everything-you-never-wanted-to-know-about-dlls/
* GOTOHELL.DLL: Software Dependencies and the Maintenance of Microsoft Windows
	+ The Maintainers 2016; Stephanie Dick, Dan Volmar
	+ http://themaintainers.org/s/GOTOHELLDLL1.pdf
* How can I specify that my DLL should resolve a DLL dependency from the same directory that the DLL is in? - https://blogs.msdn.microsoft.com/oldnewthing/20171011-00/?p=97195
* How to turn a DLL into a standalone EXE - https://hshrzd.wordpress.com/2016/07/21/how-to-turn-a-dll-into-a-standalone-exe/
* Import by Hash in x64 Assembly - https://emsea.github.io/2017/12/04/import-by-hash/
* Isolating a plugin into its own directory - http://web.archive.org/web/20171011141708/https://blogs.msdn.microsoft.com/talagrand/2010/03/08/isolating-a-plugin-into-its-own-directory/
* Rpath emulation: absolute DLL references on Windows - http://blog.omega-prime.co.uk/2012/12/06/rpath-emulation-absolute-dll-references-on-windows/
* Shellcode: In-Memory Execution of DLL - https://modexp.wordpress.com/2019/06/24/inmem-exec-dll/
* Ten Process Injection Techniques: A Technical Survey of Common and Trending Process Injection Techniques - https://www.endgame.com/blog/technical-blog/ten-process-injection-techniques-technical-survey-common-and-trending-process
* What is so special about the instance handle 0x10000000? - https://blogs.msdn.microsoft.com/oldnewthing/20121227-00/?p=5713/

## Software

* Dependencies: An open-source modern Dependency Walker
	+ https://lucasg.github.io/Dependencies/
	+ https://github.com/lucasg/Dependencies
* Dependency Walker - http://www.dependencywalker.com/
* Detours - https://www.microsoft.com/en-us/research/project/detours/
* DetoursNT: Detours with just single dependency - NTDLL
	+ https://github.com/wbenny/DetoursNT
* DLL Diagnostic Tools: Tools for diagnosing DLL dependency loading issues
	- https://github.com/adamrehn/dll-diagnostics
* DLL_to_EXE: Converts a DLL into a ready-to-use EXE. Supports both 32 and 64 bit DLLs
	+ https://github.com/hasherezade/dll_to_exe
* EasyHook
	+ https://easyhook.github.io/
	+ https://github.com/EasyHook/EasyHook
* GNU Binary Utilities - https://sourceware.org/binutils/docs/binutils/
	+ dlltool: Create files needed to build and use DLLs - https://sourceware.org/binutils/docs/binutils/dlltool.html
* InjectDLL: a Windows command line tool to inject DLLs into other processes - http://bytepointer.com/tools/index.htm#injectdll
* loadlibrary: Porting Windows Dynamic Link Libraries to Linux
	+ https://github.com/taviso/loadlibrary
* MemoryModule: Library to load a DLL from memory
	+ https://github.com/fancycode/MemoryModule
	+ https://www.joachim-bauch.de/tutorials/loading-a-dll-from-memory/
* PESecInfo: A simple tool to view important DLL Characteristics and change DEP and ASLR
	+ https://github.com/OsandaMalith/PESecInfo
	+ https://osandamalith.com/2018/10/24/pe-sec-info-a-simple-tool-to-manipulate-aslr-and-dep-flags/
* Rattler: Automated DLL Enumerator
	+ https://github.com/sensepost/rattler
	+ Rattler: Identifying and Exploiting DLL Preloading Vulnerabilities
		- https://sensepost.com/blog/2016/rattleridentifying-and-exploiting-dll-preloading-vulnerabilities/
	+ What the Dll? Finding and Exploiting DLL preloading vulnerabilities - Chris Le Roy
		- https://www.youtube.com/watch?v=xvluwoPM8v8
* Reflective DLL Injection with PowerShell - https://clymb3r.wordpress.com/2013/04/06/reflective-dll-injection-with-powershell/
* ReflectiveDLLInjection - https://github.com/stephenfewer/ReflectiveDLLInjection
* ReloadLibrary
	+ ReloadLibrary is a quick-and-dirty anti-hook library. Given the name of a .dll, it will make a temporary copy of the .dll on disk, load the copy, and overwrite the import address table with corresponding function addresses in the cloned library.
	+ https://github.com/nickcano/ReloadLibrary
* ThreadContinue: Reflective DLL injection using SetThreadContext() and NtContinue()
	+ https://github.com/zerosum0x0/ThreadContinue
	+ https://zerosum0x0.blogspot.com/2017/07/threadcontinue-reflective-injection.html

## DLL: Talks

* 2017 - Everything You Ever Wanted to Know about DLLs
	+ CppCon; James McNellis
	+ https://www.youtube.com/watch?v=JPQWQfDhICA
	+ https://github.com/CppCon/CppCon2017/blob/master/Presentations/Everything%20You%20Ever%20Wanted%20to%20Know%20about%20DLLs/
* 2017 - Memory-Based Library Loading: Someone Did That Already
	+ Derbycon; Casey Rosini
	+ http://www.irongeek.com/i.php?page=videos/derbycon7/t108-memory-based-library-loading-someone-did-that-already-casey-rosini

---

# DWARF

* DWARF Debugging Standard Website - http://dwarfstd.org/
* DWARF Debugging Standard Wiki - http://wiki.dwarfstd.org/

## Readings

* An interesting tree serialization algorithm from DWARF - https://eli.thegreenplace.net/2011/09/29/an-interesting-tree-serialization-algorithm-from-dwarf
* David A's DWARF Page - https://www.prevanders.net/dwarf.html
* Debug Information is Huge and What to do About It - https://documentation.backtrace.io/dwarf/
* Debugging formats DWARF and STAB - https://www.ibm.com/developerworks/library/os-debugging/
* DWARF Extensions for Separate Debug Information Files - https://gcc.gnu.org/wiki/DebugFission
* DWARF Package File Format - https://gcc.gnu.org/wiki/DebugFissionDWP
* Exploring the DWARF debug format information - https://www.ibm.com/developerworks/aix/library/au-dwarf-debug-format/index.html
* From Debugging-Information Based Binary-Level Type Inference to CFG Generation
	+ Conference on Data and Application Security and Privacy (CODASPY) 2018
	+ D. Zeng and G. Tan
	+ http://www.cse.psu.edu/~gxt29/papers/cfgConsMeta.pdf
* How debuggers work: Part 3 - Debugging information - http://eli.thegreenplace.net/2011/02/07/how-debuggers-work-part-3-debugging-information
* Implementing a Debugger: The Fundamentals - https://backtrace.io/blog/debugger-internals/
* Improving C++ Builds with Split DWARF - https://www.productive-cpp.com/improving-cpp-builds-with-split-dwarf/
* Introduction to the DWARF Debugging Format - http://www.dwarfstd.org/doc/Debugging%20using%20DWARF.pdf
* Programmatic access to the call stack in C++ - https://eli.thegreenplace.net/2015/programmatic-access-to-the-call-stack-in-c/
* Querying DWARF For Fun And Profit - https://developers.redhat.com/blog/2015/01/22/querying-dwarf-for-fun-and-profit/
* Reliable and Fast DWARF-based Stack Unwinding
	+ OOPSLA 2019
	+ Théophile Bastian, Stephen Kell, Francesco Zappa Nardelli
	+ https://www.di.ens.fr/~zappa/projects/frdwarf/
	+ https://2019.splashcon.org/details/splash-2019-oopsla/30/Reliable-and-Fast-DWARF-based-Stack-Unwinding
* The contents of DWARF sections - https://eli.thegreenplace.net/2011/12/26/the-contents-of-dwarf-sections
* Using COMDAT Sections to Reduce the Size of DWARF Debug Information - https://gcc.gnu.org/wiki/DwarfSeparateTypeInfo
* Where are your symbols, debuginfo and sources? - https://gnu.wildebeest.org/blog/mjw/2016/02/02/where-are-your-symbols-debuginfo-and-sources/
* Writing a Linux Debugger Part 4: Elves and dwarves - https://blog.tartanllama.xyz/writing-a-linux-debugger-elf-dwarf/

## Software

* dareog: ORC meets DWARF - https://github.com/emersion/dareog
* Debug Frame Checking: Check `.eh_frame` and `.debug_frame` information
	+ https://github.com/francesco-zappa-nardelli/eh_frame_check
* DIVA - Debug Information Visual Analyzer
	+ DIVA is a command line tool that processes DWARF debug information contained within ELF files and prints the semantics of that debug information. The DIVA output is designed to be understandable by software programmers without any low-level compiler or DWARF knowledge; as such, it can be used to report debug information bugs to the compiler provider.
	+ https://github.com/SNSystems/DIVA
	+ 2017 EuroLLVM Developers’ Meeting lightning talk
		- video: https://www.youtube.com/watch?v=SwtpXaCk2bE
		- slides: http://llvm.org/devmtg/2017-03/assets/slides/diva_debug_information_visual_analyzer.pdf
* dsymutil - manipulate archived DWARF debug symbol files
	+ https://llvm.org/docs/CommandGuide/dsymutil.html
	+ https://github.com/llvm-mirror/llvm/tree/master/tools/dsymutil
* dwarfexport: Export dwarf debug information from IDA Pro - https://github.com/ALSchwalm/dwarfexport
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
* gimli: A lazy, zero-copy parser for the DWARF debugging format
	+ https://github.com/gimli-rs/gimli
	+ Speeding Up `dwarfdump` With Rust - https://robert.ocallahan.org/2018/03/speeding-up-dwarfdump-with-rust.html
* libbacktrace: A C library that may be linked into a C/C++ program to produce symbolic backtraces
	+ As of September 2016, libbacktrace only supports ELF and PE/COFF executables with DWARF debugging information. The library is written to make it straightforward to add support for other object file and debugging formats.
	+ https://github.com/ianlancetaylor/libbacktrace
	+ https://github.com/gcc-mirror/gcc/tree/master/libbacktrace
* libdwarf - DWARF debugging information - https://sourceforge.net/projects/libdwarf/
	+ Libdwarf And Dwarfdump - http://wiki.dwarfstd.org/index.php?title=Libdwarf_And_Dwarfdump
	+ Libdwarf: Library to provide access to DWARF debugging information
		- Libdwarf meta repository that combines libdwarf with its dependency libelf
		- https://github.com/avast-tl/libdwarf
* libdwarfpp: A high-level API for accessing DWARF debugging information in C++
	+ https://github.com/stephenrkell/libdwarfpp
* libdwarfw: A C library to write DWARF debugging information
	+ https://github.com/emersion/libdwarfw
* llvm-dwarfdump - dump and verify DWARF debug information
	+ https://llvm.org/docs/CommandGuide/llvm-dwarfdump.html
* llvm-locstats - calculate statistics on DWARF debug location
	+ https://llvm.org/docs/CommandGuide/llvm-locstats.html
* Pahole and the dwarves: Debugging Information Manipulation Tools
	+ https://git.kernel.org/pub/scm/devel/pahole/pahole.git/
	+ https://github.com/acmel/dwarves
	+ https://www.spinics.net/lists/dwarves/
	+ The 7 dwarves: debugging information beyond gdb - https://landley.net/kdocs/ols/2007/ols2007v2-pages-35-44.pdf
	+ Poke-a-hole and friends - https://lwn.net/Articles/335942/
	+ pahole and other DWARF2 utilities - https://lwn.net/Articles/206805/
	+ How to avoid wasting megabytes of memory a few bytes at a time - https://developers.redhat.com/blog/2016/06/01/how-to-avoid-wasting-megabytes-of-memory-a-few-bytes-at-a-time/
* structhole: Look for holes in structs by examining DWARF debugging output - https://github.com/cemeyer/structhole

## DWARF: Talks

* 2018 - DWARF v5 Highlights - Why You Care
	+ 2018 LLVM Developers’ Meeting; Paul Robinson
	+ https://www.youtube.com/watch?v=2Pb00xz8uH8
* 2018 - FOSDEM 2018 - [Debugging Tools](https://fosdem.org/2018/schedule/track/debugging_tools/)
	+ DWARF Pieces And Other DWARF Location Woes - https://fosdem.org/2018/schedule/event/dwarfpieces/
	+ DWARF5 and GNU extensions - https://fosdem.org/2018/schedule/event/debugging_tools_dwarf5/
	+ Rust versus DWARF versus LLVM - https://fosdem.org/2018/schedule/event/debugging_tools_rust/
* 2017 - Consistent Views at Recommended Breakpoints (bis), GNU Tools Cauldron 2017
	+ https://slideslive.com/38902686/consistent-views-at-recommended-breakpoints-bis
	+ Related post: https://developers.redhat.com/blog/2017/07/11/statement-frontier-notes-and-location-views/
* 2017 - Build-ids, symbols and debuginfo tooling BoF, GNU Tools Cauldron 2017
	+ https://slideslive.com/38902681/buildids-symbols-and-debuginfo-tooling-bof
* 2017 - Debugging Debug Information - Francesco Zappa Nardelli - [Workshop on Software Correctness and Reliability 2017](http://www.srl.inf.ethz.ch/workshop2017.php)
	+ https://www.youtube.com/watch?v=lBJIrGgEP1A
	+ Tales from Binary Formats ([ENTROPY 2018](https://entropy2018.sciencesconf.org/resource/page/id/1) slides) - https://entropy2018.sciencesconf.org/data/nardelli.pdf
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
* Executable and Linkable Format: format specification - https://formats.kaitai.io/elf/
* Learning Linux Binary Analysis (2016) - Ryan O'Neill - http://www.bitlackeys.org/#research
* linux-re-101
	+ https://github.com/michalmalik/linux-re-101
	+ https://libraries.io/github/michalmalik/linux-re-101
* References - SkyFree.org - http://www.skyfree.org/linux/references/references.html

## Readings

* A Whirlwind Tutorial on Creating Really Teensy ELF Executables for Linux
	+ http://www.muppetlabs.com/~breadbox/software/tiny/teensy.html
	+ https://github.com/abraithwaite/teensy
* About ELF Auxiliary Vectors - http://articles.manugarg.com/aboutelfauxiliaryvectors
* Analyzing ELF Binaries with Malformed Headers
	- Part 1 - Emulating Tiny Programs
		- https://binaryresearch.github.io/2019/09/17/Analyzing-ELF-Binaries-with-Malformed-Headers-Part-1-Emulating-Tiny-Programs.html
	- Part 2 - Mapping Program Logic with Qiling and Graphviz
		- https://binaryresearch.github.io/2019/12/11/Analyzing-ELF-Binaries-with-Malformed-Headers-Part-2-Mapping-Program-Logic-with-Qiling-and-Graphviz.html
	- Part 3 - Automatically Solving a Corrupted Keygenme with angr
		- https://binaryresearch.github.io/2020/01/15/Analyzing-ELF-Binaries-with-Malformed-Headers-Part-3-Solving-A-Corrupted-Keygenme.html
* Anatomy of an ELF core file - https://www.gabriel.urdhr.fr/2015/05/29/core-file/
* Armouring the ELF: Binary encryption on the UNIX platform - scut & grugq - Phrack Magazine #58 (2001-12-28) - http://www.phrack.org/issues/58/5.html
* Building an ELF Parser with Frida - https://versprite.com/og/frida/
* Cheating the ELF: Subversive Dynamic Linking to Libraries - https://grugq.github.io/docs/subversiveld.pdf
* Computer Science from the Bottom Up - https://www.bottomupcs.com/
	+ Behind the process - https://www.bottomupcs.com/chapter07.xhtml
	+ Dynamic Linking - https://www.bottomupcs.com/chapter08.xhtml
* Constructing the ELF - A Magnetized Needle and a Steady Hand - http://nullprogram.com/blog/2016/11/17/
* Custom ELF program headers—what, why and how - http://www.cl.cam.ac.uk/~srk31/blog/2017/02/14/
	+ Rag-bag of utilities and scripts that do strange things with ELF files - https://github.com/stephenrkell/elftin/
* Dynamic Linking in ELF - http://dandylife.net/blog/archives/660
* ELF - No Section Header? No Problem - https://em386.blogspot.com/2006/10/elf-no-section-header-no-problem.html
* ELF Binary Mangling
	+ Part 1: Concepts - https://medium.com/@dmxinajeansuit/elf-binary-mangling-part-1-concepts-e00cb1352301
	+ Part 2: Golfin’ - https://medium.com/@dmxinajeansuit/elf-binary-mangling-pt-2-golfin-7e5c82bb482c
	+ Part 3: Weaponization - https://medium.com/@dmxinajeansuit/elf-binary-mangling-part-3-weaponization-6e11971108b3
* ELF File Format - http://resources.infosecinstitute.com/elf-file-format/
* ELF Hello World Tutorial
	+ http://www.cirosantilli.com/elf-hello-world/
	+ https://github.com/cirosantilli/cirosantilli.github.io/blob/master/elf-hello-world.md
* ELF introspection, robustly and portably - http://www.cl.cam.ac.uk/~srk31/blog/devel/elf-introspection.html
* ELF loading and dynamic linking - https://www.gabriel.urdhr.fr/2015/01/22/elf-linking/
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
* Executable and Linkable Format 101
	+ Part 1: Sections and Segments - http://www.intezer.com/executable-linkable-format-101-part1-sections-segments/
	+ Part 2: Symbols - http://www.intezer.com/executable-linkable-format-101-part-2-symbols/
	+ Part 3: Relocations - https://www.intezer.com/executable-and-linkable-format-101-part-3-relocations/
	+ Part 4: Dynamic Linking - https://www.intezer.com/executable-linkable-format-101-part-4-dynamic-linking/
* Exploiting ELF Expansion Variables - https://backtrace.io/blog/exploiting-elf-expansion-variables/
* Generating executable files from scratch - https://github.com/cameronswinoga/yabfc/wiki/Generating-executable-files-from-scratch
* GNU Hash ELF Sections
	+ https://blogs.oracle.com/ali/gnu-hash-elf-sections
	+ http://www.linker-aliens.org/blogs/ali/entry/gnu_hash_elf_sections/
* Good Practices in Library Design, Implementation, and Maintenance - https://www.akkadia.org/drepper/goodpractice.pdf
* Have fun with LIEF and Executable Formats - Play with ELF symbols - Part 2 (renaming dynamic symbols) - https://blog.quarkslab.com/have-fun-with-lief-and-executable-formats.html#elf
* How is a binary executable organized? Let's explore it! - https://jvns.ca/blog/2014/09/06/how-to-read-an-executable/
* How programs get run: ELF binaries - https://lwn.net/Articles/631631/
* How To Write Shared Libraries - https://www.akkadia.org/drepper/dsohowto.pdf
* I/O patterns on ELF binary initialization - https://glandium.org/blog/?p=1016
* Improving binary layout for progressive decompression (2011) - https://glandium.org/blog/?p=2320
* In-Memory-Only ELF Execution (Without tmpfs) - https://magisterquis.github.io/2018/03/31/in-memory-only-elf-execution.html
* In the lands of corrupted elves: Breaking ELF software with Melkor fuzzer - https://www.blackhat.com/docs/us-14/materials/arsenal/us-14-Hernandez-Melkor-Slides.pdf
* Introduction to the ELF Format
	- Part I: The ELF Header - https://blog.k3170makan.com/2018/09/introduction-to-elf-format-elf-header.html
	- Part II: Understanding Program Headers - https://blog.k3170makan.com/2018/09/introduction-to-elf-format-part-ii.html
	- Part III: The Section Headers - https://blog.k3170makan.com/2018/09/introduction-to-elf-file-format-part.html
	- Part IV: Exploring Section Types and Special Sections - https://blog.k3170makan.com/2018/10/introduction-to-elf-format-part-iv.html
	- Part V: Understanding C start up .init_array and .fini_array sections - https://blog.k3170makan.com/2018/10/introduction-to-elf-format-part-v.html
	- Part VI(1): The Symbol Table and Relocations - https://blog.k3170makan.com/2018/10/introduction-to-elf-format-part-vi.html
	- Part VI(2): The Symbol Table and Relocations - https://blog.k3170makan.com/2018/10/introduction-to-elf-format-part-vi_18.html
	- Part VI(3): More Relocation tricks - r_addend execution - https://blog.k3170makan.com/2018/10/introduction-to-elf-format-part-vi-more.html
	- Part VII: Dynamic Linking / Loading and the .dynamic section - https://blog.k3170makan.com/2018/11/introduction-to-elf-format-part-vii.html
* Inside ELF Symbol Tables
	+ https://blogs.oracle.com/ali/inside-elf-symbol-tables
	+ http://www.linker-aliens.org/blogs/ali/entry/inside_elf_symbol_tables/
* Linux Internals - Dynamic Linking Wizardry - https://0x00sec.org/t/linux-internals-dynamic-linking-wizardry/1082
* Linux Internals - The Art Of Symbol Resolution - https://0x00sec.org/t/linux-internals-the-art-of-symbol-resolution/1488
* Linux x86 Program Start Up (dynamically loaded x86 ELF files) - http://dbp-consulting.com/tutorials/debugging/linuxProgramStartup.html
* Making our own executable packer
	- What's in a Linux executable? - https://fasterthanli.me/blog/2020/whats-in-a-linux-executable/
	- Running an executable without exec - https://fasterthanli.me/blog/2020/running-an-executable-without-exec/
	- Position-independent code - https://fasterthanli.me/blog/2020/position-independent-code/
	- ELF relocations - https://fasterthanli.me/blog/2020/elf-relocations/
	- The simplest shared library - https://fasterthanli.me/blog/2020/the-simplest-shared-library/
	- Loading multiple ELF objects - https://fasterthanli.me/blog/2020/loading-multiple-elf-objects/
* Position Independent Executables - https://blog.fpmurphy.com/2008/06/position-independent-executables.html
* Programming With Ones and Zeros
	+ Part 1 - http://www.hanshq.net/ones-and-zeros.html
	+ Ones and Zeros, Part 2: Making Executable Files - http://www.hanshq.net/making-executables.html
* RE a 64bit ELF binary - Devil’s swapper write-up - https://0x00sec.org/t/re-a-64bit-elf-binary-devils-swapper-write-up/2379
* Relocations in ELF Toolchains - https://www.sifive.com/blog/2017/08/21/all-aboard-part-2-relocations/
* Resolving ELF Relocation Name / Symbols - https://em386.blogspot.com/2006/10/resolving-elf-relocation-name-symbols.html
* Secure Code Partitioning With ELF binaries (SCOP) - http://bitlackeys.org/papers/secure_code_partitioning_2018.txt
* Smallest x86 ELF Hello World - http://timelessname.com/elfbin/
* Special sections in Linux binaries - https://lwn.net/Articles/531148/
* Targeting File Parsers with S2E and Kaitai Struct - targeted symbolic execution of readelf - https://adrianherrera.github.io/post/kaitai-s2e/
* The 101 of ELF Binaries on Linux: Understanding and Analysis - https://linux-audit.com/elf-binaries-on-linux-understanding-and-analysis/
* The Anatomy of an Executable - dissection of a simple "hello world" ELF binary - https://github.com/mewrev/dissection
* The Cerberus ELF Interface - http://phrack.org/issues/61/8.html
* The Cost Of ELF Symbol Hashing
	+ https://blogs.oracle.com/ali/the-cost-of-elf-symbol-hashing
	+ http://www.linker-aliens.org/blogs/ali/entry/the_cost_of_elf_symbol/
* The ELF Object File Format by Dissection (1995) - http://www.linuxjournal.com/article/1060
* The Executable and Linkable Format (ELF)
	+ https://publicclu2.blogspot.com/2013/05/executable-and-linkable-format-elf.html
	+ https://www.cs.stevens.edu/%7Ejschauma/631A/elf.html
	+ http://web.archive.org/web/20120415084409/http://www.acsu.buffalo.edu:80/~charngda/elf.html
* The missing link: explaining ELF static linking, semantically - Stephen Kell, Dominic P. Mulligan, Peter Sewell - OOPSLA 2016
	+ http://www.cl.cam.ac.uk/~pes20/rems/papers/oopsla-elf-linking-2016.pdf
	+ https://bitbucket.org/Peter_Sewell/linksem/
* Uncovering a few SIGSEGVs in binutils' BFD and GLIBC
	+ https://chatsubo-labs.blogspot.com/2017/05/uncovering-few-sigsegvs-in-binutils-bfd.html
	+ http://brainoverflow.org/papers/BFD-GLIBC_Fuzzing/0%20Uncovering%20a%20few%20SIGSEGVs%20in%20binutils'%20BFD%20and%20GLIBC.pdf
* Understanding Linux ELF RTLD internals - http://s.eresi-project.org/inc/articles/elf-rtld.txt
* Understanding the Memory Layout of Linux Executables - https://gist.github.com/CMCDragonkai/10ab53654b2aa6ce55c11cfc5b2432a4
* 'Weird Machine' patterns - https://www.researchgate.net/publication/283630248_%27Weird_Machine%27_patterns
* Writing shared libraries - http://plan99.net/~mike/writing-shared-libraries.html

### Thread Local Storage (TLS)

- A Deep dive into (implicit) Thread Local Storage
	- https://chao-tic.github.io/blog/2018/12/25/tls
- Android ELF TLS
	- https://android.googlesource.com/platform/bionic/+/HEAD/docs/elf-tls.md
- ELF Handling For Thread-Local Storage
	- https://www.akkadia.org/drepper/tls.pdf
- Thread Local Storage (ELF Thread Local Storage ABI)
	- https://fuchsia.dev/fuchsia-src/development/threads/tls
- TLS Examples
	- https://github.com/stffrdhrn/tls-examples
	- ELF Binaries and Relocation Entries
		- http://stffrdhrn.github.io/hardware/embedded/openrisc/2019/11/29/relocs.html
	- Thread Local Storage
		- https://stffrdhrn.github.io/hardware/embedded/openrisc/2020/01/19/tls.html

### Transformation

- A Technique for Hooking Internal Functions of Dynamically-Linked ELF Binaries
	- https://binaryresearch.github.io/2019/08/29/A-Technique-for-Hooking-Internal-Functions-of-Dynamically-Linked-ELF-Binaries.html
- Honey, I Shrunk the ELFs: Lightweight Binary Tailoring of Shared Libraries
	- EMSOFT 2019
	- ACM Transactions on Embedded Computing Systems (TECS) 18, 5s, Article 102 (October 2019)
	- Andreas Ziegler, Julian Geus, Bernhard Heinloth, Timo HÖnig, Daniel Lohmann
	- https://dl.acm.org/citation.cfm?id=3358222
	- https://www4.cs.fau.de/Publications/2019/ziegler_19_emsoft.pdf
- How To Strip An ELF Object Without Fully Understanding It
	- http://www.linker-aliens.org/blogs/ali/entry/how_to_strip_an_elf/
	- https://blogs.oracle.com/ali/how-to-strip-an-elf-object-without-fully-understanding-it
- Inserting Debugging Instrumentation into an Internal Function Using Redirect-to-PLT
	- https://binaryresearch.github.io/2019/09/07/Inserting-Debugging-Instrumentation-Into-an-Internal-Function-using-Redirect-to-PLT.html
- Tweaking binaries with elfedit
	- https://ptribble.blogspot.com/2017/06/tweaking-binaries-with-elfedit.html

## Software

* ABI Dumper - a tool to dump ABI of an ELF object containing DWARF debug info - https://github.com/lvc/abi-dumper
* abidiff - compares the Application Binary Interfaces (ABI) of two shared libraries in ELF format
	+ https://sourceware.org/libabigail/manual/abidiff.html
	+ Comparing ABIs for Compatibility with libabigail – Part 1 - https://developers.redhat.com/blog/2014/10/23/comparing-abis-for-compatibility-with-libabigail-part-1/
	+ Comparing ABIs for Compatibility with libabigail – Part 2 - https://developers.redhat.com/blog/2014/10/28/comparing-abis-for-compatibility-libabigail-part-2/
	+ Talk: Libabigail: How semantic analysis of C and C++ ELF binaries can be used to analyze ABI changes (openSUSE Conference 2017)
		- https://media.ccc.de/v/1234-libabigail-how-semantic-analysis-of-c-and-c-elf-binaries-can-be-used-to-analyze-abi-changes
		- https://www.youtube.com/watch?v=wxVBuZK8Dl0
* binception: Generate hash values for functions within an ELF binary - https://github.com/enferex/binception
* binch: a light BINary patCH tool - https://github.com/tunz/binch
* core2ELF64: Recover 64 bit ELF executables from memory dump
	- https://github.com/enbarberis/core2ELF64
* dnload: Minimal binary generator for \*nix operating systems
	+ dnload.py is a script for generating minimal ELF binaries from C code. It serves no practical real-world use case, but can be utilized to aid in the creation of size-limited demoscene productions.
	+ https://github.com/faemiyah/dnload
* dress: add symbols back into a stripped ELF binary (~strip)
	+ http://van.prooyen.com/projects/#dress
	+ https://github.com/docileninja/dress
* dt_infect: ELF Shared library injector using DT_NEEDED precedence infection. Acts as a permanent LD_PRELOAD
	- https://github.com/elfmaster/dt_infect
* DynELFSymbols: Helps to create backdoor/MitM shared-object files
	+ https://github.com/magisterquis/dynelfsymbols
	+ https://github.com/magisterquis/dynelfsymbols/blob/master/QUICKSTART.md
	+ https://github.com/magisterquis/dynelfsymbols/blob/master/THEORY.md
* dynStruct: a tool using dynamoRio to monitor memory accesses of an ELF binary via a data gatherer, and use this data to recover structures of the original code
	+ https://github.com/ampotos/dynStruct
	+ dynStruct: An automatic reverse engineering tool for structure recovery and memory use analysis - Daniel Mercier - Master Thesis (2017)
		- https://kar.kent.ac.uk/58461/
	+ dynStruct: An automatic reverse engineering tool for structure recovery and memory use analysis - Mercier, Daniel and Chawdhary, Aziem and Jones, Richard E. (2017), IEEE 24th International Conference on Software Analysis, Evolution and Reengineering (SANER)
		- https://kar.kent.ac.uk/63700/
* ECFS: extended core file snapshot format
	+ https://github.com/elfmaster/ecfs
	+ DEF CON 23 - Ryan Oneill - Advances in Linux Process Forensics Using ECFS - https://www.youtube.com/watch?v=fCJJnJ84MSE
	+ an extension to the existing ELF core file format in Linux. Its job is to intercept the Linux core-dump handler, catch the core-dump before it is written to disk, and carefully reconstruct it into an ecfs-core file.
	+ execute memory snapshots so they can start running where they left off - https://github.com/elfmaster/ecfs_exec
* elf-bf-tools - https://github.com/bx/elf-bf-tools
	+ This project contains tools that can be used to coerce the gcc's runtime loader into performing interesting operations using only valid relocation entries and symbols.
* elf-parser: identifying/extracting various sections of an ELF file
	+ https://github.com/TheCodeArtist/elf-parser
* elf-strings: The better strings utility for the reverse engineer - https://github.com/LloydLabs/elf-strings
* ELF/PaX Utilities - https://github.com/gentoo/pax-utils
	+ https://en.wikibooks.org/wiki/Grsecurity/Additional_Utilities
	+ scanelf - Prints out information specific to the ELF structure of a binary - https://wiki.gentoo.org/wiki/Hardened/PaX_Utilities#Extracting_ELF_information_from_binaries
	+ dumpelf - Converts a ELF file into human readable C code that defines a structure with the same image as the original ELF file - https://wiki.gentoo.org/wiki/Hardened/PaX_Utilities#Programming_with_ELF_files
* ELF Tailoring (EMSOFT 2019)
	- see: [ELF](#elf): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-3): "Honey, I Shrunk the ELFs: Lightweight Binary Tailoring of Shared Libraries"
	- https://gitlab.cs.fau.de/i4/pub/elftailor
	+ ELF diet: Tool to shrink the tailored ELF files to a smaller size
		- https://gitlab.cs.fau.de/i4/pub/elftailor/elfdiet
	+ remove_from_elf: Tool to remove functions from ELF library interfaces and to overwrite their implementation
		- https://gitlab.cs.fau.de/i4/pub/elftailor/remove_from_elf
	+ librarytrader: Tool for static and dynamic analysis of dependencies between application(s) and shared libraries which allows us to determine unused functions
		- https://gitlab.cs.fau.de/i4/pub/elftailor/librarytrader
* ELF Tool Chain Project - https://sourceforge.net/projects/elftoolchain/
	+ A BSD-licensed implementation of compilation tools (nm, ar, as, ld, etc.) for the ELF object format.
* ELFbac: runtime intent-level ABI-granular memory protection for Linux - http://elfbac.org/
* ELFen: Extract and spell check read-only strings within ELF binaries - https://github.com/enferex/ELFen
* Elfesteem: Executable file format parser/generator - https://github.com/serpilliere/elfesteem
* Elfhack: to optimize ELF binaries for size and cold startup speed - https://github.com/mozilla/positron/tree/master/build/unix/elfhack
* ELFIO - ELF (Executable and Linkable Format) reader and producer implemented as a header only C++ library
	+ http://serge1.github.io/ELFIO 
	+ https://github.com/serge1/ELFIO
* ELFkickers (ebfc, elfls, elftoc, infect, objres, rebind, sstrip) - http://www.muppetlabs.com/~breadbox/software/elfkickers.html
* Elfkit: Rust ELF parsing, manipulation, and (re)linking toolkit - https://github.com/aep/elfkit
* ELFManip: Modify ELF executables - https://github.com/schieb/ELFManip
* elfutils
	+ a collection of utilities and libraries to read, create and modify ELF binary files, find and handle DWARF debug data, symbols, thread state and stacktraces for processes and core files on GNU/Linux
	+ https://sourceware.org/elfutils/
* Exodus - a tool that makes it easy to successfully relocate Linux ELF binaries from one system to another
	+ https://github.com/Intoli/exodus
* GNU Binary Utilities - https://sourceware.org/binutils/docs/binutils/
	+ elfedit: Update the ELF header of ELF files - https://sourceware.org/binutils/docs/binutils/elfedit.html
	+ nm: List symbols from object files - https://sourceware.org/binutils/docs/binutils/nm.html
	+ objdump: Display information from object files - https://sourceware.org/binutils/docs/binutils/objdump.html
	+ readelf: Display the contents of ELF format files - https://sourceware.org/binutils/docs/binutils/readelf.html
	+ size: List section sizes and total size - https://sourceware.org/binutils/docs/binutils/size.html
		- examples:
			- https://mcuoneclipse.com/2012/09/24/code-size-information-with-gcc-for-armkinetis/
			- https://mcuoneclipse.com/2013/04/14/text-data-and-bss-code-and-data-size-explained/
			- http://www.geeksforgeeks.org/memory-layout-of-c-program/
			- http://cs-fundamentals.com/c-programming/memory-layout-of-c-program-code-data-segments.php#size-of-code-data-bss-segments
	+ 9 essential GNU binutils tools - https://opensource.com/article/19/10/gnu-binutils
* HoloDec: Decompiler for x86 and x86-64 ELF binaries - https://github.com/cararasu/holodec
* Lepton: a Lightweight ELF Parsing Tool
	- designed specifically for analyzing and editing binaries with damaged or corrupted ELF headers
	- https://github.com/BinaryResearch/lepton
* Libelf - ELF object file access library - http://www.mr511.de/software/english.html
	+ libelf-howto - http://chris.rohlf.googlepages.com/libelf-howto.c
	+ Libelf.js: LibELF port for JavaScript - https://github.com/AlexAltea/libelf.js
* Libelfin: C++11 ELF/DWARF parser - a from-scratch C++11 library for reading ELF binaries and DWARFv4 debug information - https://github.com/aclements/libelfin
* libelfmaster: Secure ELF parsing library
	+ https://github.com/elfmaster/libelfmaster
	+ libelfmaster_examples - https://github.com/elfmaster/libelfmaster_examples
	- readelfmaster: A reimplementation of GNU readelf
		- https://github.com/Bowlslaw/readelfmaster
* Mandibule: Linux ELF injector for x86 / x86_64 / arm / arm64
	+ Doesn't use `dlopen` and can inject into statically linked targets by mapping manually the ELF in memory from syscalls only
	+ https://github.com/ixty/mandibule
* Melkor - An ELF File Format Fuzzer - https://github.com/IOActive/Melkor_ELF_Fuzzer
* objdump beautifier - https://github.com/diouziou/bod
	+ Supported Targets: elf32-littlearm, elf32-tradlittlemips, elf32-i386, elf64-x86-64
* PatchELF: A small utility to modify the dynamic linker and RPATH of ELF executables
	+ http://nixos.org/patchelf.html
	+ https://github.com/nixos/patchelf
* patchkit - https://github.com/lunixbochs/patchkit
	+ Patches an ELF binary using one or more simple Python scripts.
* pyelftools: Pure-python library for parsing ELF and DWARF - https://github.com/eliben/pyelftools
* smol: Shoddy minsize-oriented linker
	+ https://github.com/Shizmob/smol
	+ Intricacies of sizecoding on Linux - Revision 2019 Seminar
		- https://www.youtube.com/watch?v=a03HXo8a_Io
* Stasis: build static position-independant-executables without any runtime requirements (no libc or ldso)
	+ https://github.com/korhalio/stasis
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

## ELF: Talks

### ELF: Talks (2019)

- ELF Crafting: Uncovering Advanced Anti-analysis techniques for the Linux Platform
	- r2con2019; Nacho Sanmillan (ulexec)
	- https://www.youtube.com/watch?v=adYOSO0tn9M
	- https://github.com/radareorg/r2con2019/tree/master/talks/elf_crafting
- Executable Code Golf: Making Tiny Binaries for Constrained Systems
	- linux.conf.au 2019; Nathan Egge
	- https://www.youtube.com/watch?v=J5WX-wN_RKY
	- https://2019.linux.conf.au/schedule/presentation/160/
	- XLINK compressing linker
		- https://github.com/negge/xlink
- Objtool: A Hidden Gem of Executable Parsing
	- DevConf.US 2019; Matt Helsley
	- https://www.youtube.com/watch?v=I7srCw-Ns7Y

### ELF: Talks (2018)

- C++ in Elvenland
	- CppCon 2018; Serge Guelton
	- https://www.youtube.com/watch?v=CVg7CYVV3KI
	- http://serge-sans-paille.github.io/talks/cppcon2018/elvenland/elf/
	- https://github.com/serge-sans-paille/talks/blob/master/cppcon2018/elvenland/elf.rst
- The Bits Between the Bits: How We Get to main()
	- CppCon 2018; Matt Godbolt
	- https://www.youtube.com/watch?v=dOfucXtyEsU
	- Slides: https://mattgodbolt.github.io/cppcon-bits-between-bits/

### ELF: Talks (2017)

- ELF linking: what it means and why it matters
	- 2017; Stephen Kell
	- https://www.cl.cam.ac.uk/~srk31/research/talks/kell17elf-slides.pdf
- Everything You Always Wanted to Know About "Hello, World"* (*But Were Afraid To Ask)
	- FOSDEM 2017; Brooks Davis
	- https://archive.fosdem.org/2017/schedule/event/hello_world/
	- https://people.freebsd.org/~brooks/talks/fosdem2017-helloworld/?C=M&O=D
- LLD from a user's perspective
	- FOSDEM 2017; Peter Smith
	- https://archive.fosdem.org/2017/schedule/event/lld/
	- https://archive.fosdem.org/2017/schedule/event/lld/attachments/slides/1446/export/events/attachments/lld/slides/1446/FosdemLLD2017.pdf

### ELF: Talks (2016)

- Debugging debuggers!! (Symbolic Debugging with DWARF)
	- !!Con 2016; Samy Al Bahra
	- https://backtrace.io/blog/symbolic-debugging-with-dwarf/
	- https://www.youtube.com/watch?v=OEa0EfJja_Y
- Intra-Process Memory Protection for Applications on ARM and X86: Leveraging the ELF ABI
	- BlackHat USA 2016; Sergey Bratus & Maxwell Koo & Julian Bangert
	- https://www.youtube.com/watch?v=YXh2aIc9u64
	- Slides: http://www.cs.dartmouth.edu/~sergey/io/elfbac/bh16-elfbac-slides.pdf
	- Whitepaper: http://www.cs.dartmouth.edu/~sergey/io/elfbac/bh16-elfbac-whitepaper.pdf
- New LLD linker for ELF
	- 2016 EuroLLVM Developers' Meeting; Rui Ueyama
	- https://www.youtube.com/watch?v=CYCRqjVa6l4
	- https://llvm.org/devmtg/2016-03/Presentations/EuroLLVM%202016-%20New%20LLD%20linker%20for%20ELF.pdf

### ELF: Talks (2015)

- Dark Side of the ELF
	- DEF CON 23 (2015); Alessandro Di Federico, Yan Shoshitaishvili
	- https://www.youtube.com/watch?v=aGoDYa7Kbec
- How the ELF Ruined Christmas
	- USENIX Security Symposium 2015
	- Alessandro Di Federico, Amat Cama, Yan Shoshitaishvili, Christopher Kruegel, Giovanni Vigna
	- https://www.usenix.org/conference/usenixsecurity15/technical-sessions/presentation/di-frederico
	- https://sites.cs.ucsb.edu/~chris/research/doc/usenix15_elf.pdf
	- leakless: Function redirection via ELF tricks
		- https://github.com/ucsb-seclab/leakless

### ELF: Talks (2014)

- ABIs, linkers and other animals
	- 2014; Stephen Kell
	- https://www.cl.cam.ac.uk/~srk31/research/talks/kell14abis-slides.pdf

### ELF: Talks (2013)

- ELF Eccentricities
	- CONFidence 2013; Julian Bangert, Sergey Bratus
	- https://www.youtube.com/watch?v=4LU6N6THh2U
	- https://infocon.org/cons/CONFidence/CONFidence%202013/presentations/julian_bangert_sergey_bratus.pdf
- Any Input Is a Program Weird Machines in ABI
	- CONFidence 2013; Rebecca Bx Shapiro, Julian Bangert, Sergey Bratus 
	- https://www.youtube.com/watch?v=crt5gxOoUuM
	- https://infocon.org/cons/CONFidence/CONFidence%202013/presentations/julian_bangert_rebecca_shapiro_sergey_bratus.pdf
- "Weird Machines" in ELF: A Spotlight on the Underappreciated Metadata
	- USENIX  Workshop on Offensive Technologies (WOOT) 2013
	- Rebecca Shapiro, Sergey Bratus, Sean W. Smith
	- https://www.usenix.org/conference/woot13/workshop-program/presentation/shapiro
	- http://www.cs.dartmouth.edu/~sergey/wm/woot13-shapiro.pdf
	- https://www.youtube.com/watch?v=6xbirzvr-mQ

### ELF: Talks (2012)

- Programming Weird Machines with ELF Metadata
	- DEF CON 20 (2012); Rebecca "bx" Shapiro, Sergey Bratus 
	- https://www.youtube.com/watch?v=V5KsUm1KfZE
	- https://www.youtube.com/watch?v=YgtxxLCVD-o
	- http://cs.dartmouth.edu/~bx/elf-bf-tools/slides/elf-defcon20.pdf
- The Care and Feeding of Weird Machines Found in Executable Metadata
	- 29C3 (2012); Rebecca “bx” Shapiro, Sergey Bratus
	- https://media.ccc.de/v/29c3-5195-en-executable_metadata_h264
	- https://www.youtube.com/watch?v=57UtbZGEEQA
	- http://www.cs.dartmouth.edu/~bx/elf-bf-tools/slides/ELF-29c3.pdf

---

# Mach-O

* Mach-O Runtime Architecture - http://math-atlas.sourceforge.net/devel/assembly/MachORuntime.pdf
* Mach-O Programming Topics - https://developer.apple.com/library/content/documentation/DeveloperTools/Conceptual/MachOTopics/0-Introduction/introduction.html
* OS X ABI Mach-O File Format Reference
	+ https://github.com/aidansteele/osx-abi-macho-file-format-reference
	+ PDF: https://pewpewthespells.com/re/Mach-O_File_Format.pdf
* osx-re-101 - https://github.com/michalmalik/osx-re-101
* Reverse Engineering/Mac OS X - https://en.wikibooks.org/wiki/Reverse_Engineering/Mac_OS_X

## Readings

* Basics of the Mach-O file format - https://samhuri.net/posts/2010/01/basics-of-the-mach-o-file-format/
* Dynamic Linking: ELF vs. Mach-O - http://timetobleed.com/dynamic-linking-elf-vs-mach-o/
* Dynamic Linking of Imported Functions in Mach-O - https://www.apriorit.com/dev-blog/225-dynamic-linking-mach-o / https://www.codeproject.com/Articles/187181/Dynamic-Linking-of-Imported-Functions-in-Mach-O
* Dynamic symbol table duel: ELF vs Mach-O, round 2 - http://timetobleed.com/dynamic-symbol-table-duel-elf-vs-mach-o-round-2/
* DYLD Detayled - The internals of DYLD, the dynamic linker, and the `__LINKEDIT` section - http://newosxbook.com/articles/DYLD.html
* Extracting libraries from dyld_shared_cache - https://worthdoingbadly.com/dscextract/
* Friday Q&A 2012-04-27: PLCrashReporter and Unwinding the Stack With DWARF - https://www.mikeash.com/pyblog/friday-qa-2012-04-27-plcrashreporter-and-unwinding-the-stack-with-dwarf.html
* Friday Q&A 2012-05-04: PLCrashReporter and Unwinding the Stack With DWARF, Part 2 - https://www.mikeash.com/pyblog/friday-qa-2012-05-04-plcrashreporter-and-unwinding-the-stack-with-dwarf-part-2.html
* Friday Q&A 2012-11-09: dyld: Dynamic Linking On OS X - https://www.mikeash.com/pyblog/friday-qa-2012-11-09-dyld-dynamic-linking-on-os-x.html
* Friday Q&A 2012-11-30: Let's Build A Mach-O Executable - https://www.mikeash.com/pyblog/friday-qa-2012-11-30-lets-build-a-mach-o-executable.html
* Having Fun with Obfuscated Mach-O Files - https://www.pnfsoftware.com/blog/having-fun-with-obfuscated-mach-o-files/
* Hello Mach-O: Dissection of minimal Intel 32-bits, 204 bytes, Mach-O "Hello World" executable file - http://seriot.ch/hello_macho.php
* Mach-O Binaries - http://www.m4b.io/reverse/engineering/mach/binaries/2015/03/29/mach-binaries.html
* Mach-O Executables - https://www.objc.io/issues/6-build-tools/mach-o-executables/
* Parsing Mach-O files - https://lowlevelbits.org/parsing-mach-o-files/
* Playing with Mach-O binaries and dyld
	+ https://blog.lse.epita.fr/articles/82-playing-with-mach-os-and-dyld.html
	+ https://lse.epita.fr/data/lt/2017-03-14/lt-2017-03-14-Stanislas_Lejay-Playing_with_machos_and_dyld.pdf
* Redirection of Imported Functions in Mach-O - https://www.codeproject.com/Articles/187192/Redirection-of-Imported-Functions-in-Mach-O
* Running Executables on macOS From Memory - https://blog.cylance.com/running-executables-on-macos-from-memory
* Runtime binary loading via the dynamic loader on Apple Mac OS X - http://www.subreption.com/blog/2009/02/runtime-binary-loading-via-the-dynamic-loader-on-apple-mac-os-x.html
* The Mach-O Transition: Darling in the Past 5 Years - http://blog.darlinghq.org/2017/02/the-mach-o-transition-darling-in-past-5.html

## Software

* cctools-port: Apple cctools port for Linux, \*BSD and Windows (Cygwin)
	+ https://github.com/tpoechtrager/cctools-port
* jtool: (Mach-O Analyzer) - http://www.newosxbook.com/tools/jtool.html
* MacDependency: shows all dependent libraries and frameworks of a given executable, dynamic library or framework on Mac OS X
	+ https://github.com/kwin/macdependency/
* mach_override: runtime function overriding for Mac OS X - https://github.com/rentzsch/mach_override
* MachoAnalysis: collection of analysis utils - https://github.com/eeeyes/macho_analysis
* macholibre: Mach-O & Universal Binary Parser - https://github.com/aaronst/macholibre
	+ Mach-O Libre: Pile Driving Apple Malware with Static Analysis, Big-Data, and Automation - https://www.first.org/resources/papers/conf2016/FIRST-2016-130.pdf
* machO-tools - https://github.com/bx/machO-tools
* MachOExplorer - https://github.com/everettjf/MachOExplorer
* Machotools - "a small set of tools built on top of macholib to retrieve and change informations about mach-o files. Think of it as a pure python, cross-platform implementation of install_name_tool"
	+ https://github.com/enthought/machotools
* MachOView: a visual Mach-O file browser - https://sourceforge.net/projects/machoview/
* MachOView fork: https://github.com/gdbinit/MachOView
* Maloader: userland Mach-O loader for Linux - https://github.com/shinh/maloader

## Mach-O: Talks

* 2018 - Mach-O Tricks
	+ BaiJiuCon at Mobile Security Conference (MOSEC) 2018
	+ http://iokit.racing/machotricks.pdf
* 2013 - DEF CON 21 - Mach-O Malware Analysis: Combatting Mac OSX/iOS Malware with Data Visualization
	+ https://infocon.org/cons/DEF%20CON/DEF%20CON%2021/DEF%20CON%2021%20presentations/Remy%20Baumgarten/
	+ Slides: https://infocon.org/cons/DEF%20CON/DEF%20CON%2021/DEF%20CON%2021%20presentations/Remy%20Baumgarten/DEFCON-21-Baumgarten-Mach-O-Viz.pdf
	+ Paper: https://infocon.org/cons/DEF%20CON/DEF%20CON%2021/DEF%20CON%2021%20presentations/Remy%20Baumgarten/DEFCON-21-Baumgarten-Mach-O-Viz-WP.pdf
	+ Video: https://infocon.org/cons/DEF%20CON/DEF%20CON%2021/DEF%20CON%2021%20video%20and%20slides%20x265/DEF%20CON%2021%20Hacking%20Conference%20Presentation%20By%20Remy%20Baumgarten%20-%20Combatting%20Mac%20OSX%20iOS%20Malware%20with%20Data%20Visualization%20-%20Video%20and%20Slides.mp4
	+ http://macsecurity.net/view/42/
	+ http://www.securitytube.net/video/9133
* 2009 - Black Hat DC - Let your Mach-O fly - Vincenzo Iozzo
	+ Slides: http://www.blackhat.com/presentations/bh-dc-09/Iozzo/BlackHat-DC-09-Iozzo-Macho-on-the-fly.pdf
	+ Paper: http://www.blackhat.com/presentations/bh-dc-09/Iozzo/BlackHat-DC-09-Iozzo-let-your-mach0-fly-whitepaper.pdf

---

# PDB

(Program Database)

## Readings

* Binary Rewriting With Syzygy, Pt. I - https://doar-e.github.io/blog/2017/08/05/binary-rewriting-with-syzygy/
* CodeView Debug Info Format - http://llvm.org/docs/SourceLevelDebugging.html#codeview-debug-info-format
* Improving Link Time on Windows with clang-cl and lld - http://blog.llvm.org/2018/01/improving-link-time-on-windows-with.html
* Jan Gray on inventing/implementing PDB files 1990-94 - https://twitter.com/jangray/status/659916997711544320
* LLVM on Windows now supports PDB Debug Info - http://blog.llvm.org/2017/08/llvm-on-windows-now-supports-pdb-debug.html
* PDB File Format - https://github.com/google/syzygy/wiki/PdbFileFormat
* PDB Files: What Every Developer Must Know - https://www.wintellect.com/pdb-files-what-every-developer-must-know
* PDB File Internals - http://www.informit.com/articles/article.aspx?p=22685
* PDB v2.0 File Format documentation - https://reverseengineering.stackexchange.com/questions/2548/pdb-v2-0-file-format-documentation
* radare2 PDB usage - https://github.com/radare/radare2/blob/master/doc/pdb/pdb_usage
* The PDB File Format - https://llvm.org/docs/PDB/
* The PDB Info Stream (aka the PDB Stream) - http://llvm.org/docs/PDB/PdbStream.html
* PDB File Internals - http://www.informit.com/articles/article.aspx?p=22685
* PDB Info Stream - https://www.reddit.com/r/programming/comments/6ukeuk/llvm_on_windows_now_supports_pdb_debug_info/dlvtucx/
* PDB Stream Decomposition - https://moyix.blogspot.com/2007/08/pdb-stream-decomposition.html
* pdbparse - Stream Descriptions wiki - https://code.google.com/archive/p/pdbparse/wikis/StreamDescriptions.wiki
* Symbols the Microsoft Way - https://randomascii.wordpress.com/2013/03/09/symbols-the-microsoft-way/
* The Types Stream - https://moyix.blogspot.com/2007/10/types-stream.html
* What’s inside a PDB File? - https://blogs.msdn.microsoft.com/vcblog/2016/02/08/whats-inside-a-pdb-file/

## Software

* crunchersharp
	+ analyses debugger information file (PDB, so Microsoft Visual C++ only) and presents info about user defined structures (size, padding, etc.)
	+ https://github.com/msinilo/crunchersharp
	+ http://msinilo.pl/blog2/post/p425/
* cv2pdb: converter of DMD CodeView/DWARF debug information to PDB files
	- https://github.com/rainers/cv2pdb
* Debug Interface Access SDK (DIA SDK) - provides access to debug information stored in PDB files - https://docs.microsoft.com/en-us/visualstudio/debugger/debug-interface-access/debug-interface-access-sdk
* drpdb: Convert from Microsoft PDB format into a MySQL database - https://github.com/briterator/drpdb
* llvm-pdbutil - PDB File forensics and diagnostics - https://llvm.org/docs/CommandGuide/llvm-pdbutil.html - https://github.com/llvm-mirror/llvm/tree/master/tools/llvm-pdbutil
* llvm-symbolizer - convert addresses into source code locations - https://llvm.org/docs/CommandGuide/llvm-symbolizer.html - https://github.com/Microsoft/llvm/tree/master/test/tools/llvm-symbolizer/pdb
* MetadataTools:
Various tools and helpers to read assembly metadata - https://github.com/KirillOsenkov/MetadataTools
	+ Pdb - extract .pdb information from a .dll/.exe debug directory (Pdb Guid, age, path to .pdb); download the .pdb from symbol server; determine if a .dll matches a .pdb; find a matching .pdb in a folder for a given .dll - https://github.com/KirillOsenkov/MetadataTools/tree/master/Pdb
* microsoft-pdb: Information from Microsoft about the PDB format - https://github.com/Microsoft/microsoft-pdb
* MSFViewer - viewing and understanding PDB Multi-Stream File (MSF) data - https://github.com/apoch/epoch-language/tree/master/Tools/MSFViewer
* pdbex: an utility for reconstructing structures and unions from the PDB into compilable C headers
	+ https://github.com/wbenny/pdbex
* pdbinfo:  displays information about PDB symbol files (timestamp, GUID, and age) - https://github.com/randomascii/tools/tree/master/pdbinfo
* PDBparse - Python code to parse Microsoft PDB files - https://github.com/moyix/pdbparse
* PdbReader & PdbWriter - Common Compiler Infrastructure (CCI) - https://github.com/Microsoft/cci/tree/master/PDBReaderAndWriter
* SymDiff: Diff tool for comparing symbols in PDB files
	+ https://github.com/WalkingCat/SymDiff
* Syzygy Transformation Toolchain - PDB Module - https://github.com/google/syzygy/tree/master/syzygy/pdb

## PDB: Talks

* 2016 LLVM Developers’ Meeting: R. Kleckner "CodeView, the MS Debug Info Format in LLVM"
	+ https://www.youtube.com/watch?v=5twzd06NqGU
	+ http://www.llvm.org/devmtg/2016-11/Slides/Kleckner-CodeViewInLLVM.pdf

---

# PE

## Readings

* A smallest PE executable (x64) with every byte executed - https://drakopensulo.wordpress.com/2017/08/06/smallest-pe-executable-x64-with-every-byte-executed/
* An Analysis of the Windows PE Checksum Algorithm - https://www.codeproject.com/Articles/19326/An-Analysis-of-the-Windows-PE-Checksum-Algorithm
* An In-Depth Look into the Win32 Portable Executable File Format
	+ Part 1: http://reversingproject.info/wp-content/uploads/2009/05/an_in-depth_look_into_the_win32_portable_executable_file_format_part_1.pdf / http://www.delphibasics.info/home/delphibasicsarticles/anin-depthlookintothewin32portableexecutablefileformat-part1
	+ Part 2: http://reversingproject.info/wp-content/uploads/2009/05/an_in-depth_look_into_the_win32_portable_executable_file_format_part_2.pdf / http://www.delphibasics.info/home/delphibasicsarticles/anin-depthlookintothewin32portableexecutablefileformat-part2
* Binary offsets, virtual addresses and pefile - https://5d4a.wordpress.com/2017/09/21/binary-offsets-virtual-addresses-and-pefile/
* Case studies in Rich Header analysis and hunting (2018-08-09) - http://ropgadget.com/posts/richheader_hunting.html
* Common Object File Format (COFF) - https://support.microsoft.com/en-us/help/121460/common-object-file-format-coff
* Dynamic Reconstruction of Relocation Information for Stripped Binaries - http://www.cs.columbia.edu/~vpappas/papers/reloc.raid14.pdf
* Finding the Needle: A Study of the PE32 Rich Header and Respective Malware Triage
	+ https://www.sec.in.tum.de/i20/publications/finding-the-needle-a-study-of-the-pe32-rich-header-and-respective-malware-triage
	+ https://www.semanticscholar.org/paper/Finding-the-Needle-A-Study-of-the-PE32-Rich-Header-Webster-Kolosnjaji/44adfa896e6598b1723507060126125a0cad39a1
	+ Rich Header: a collection of the work performed investigating the PE32 Rich Header - https://github.com/HolmesProcessing/RichHeader-Service_Collection
* Fully undetectable backdooring PE files - https://haiderm.com/fully-undetectable-backdooring-pe-files/
* Introducing New Packing Method: First Reflective PE Packer Amber - https://pentest.blog/introducing-new-packing-method-first-reflective-pe-packer/
* Microsoft Portable Executable (PE) and Common Object File Format (COFF) Specification - https://msdn.microsoft.com/en-us/library/windows/desktop/ms680547.aspx
* Microsoft's Rich Signature (undocumented) - http://ntcore.com/Files/richsign.htm
* PE (corkami wiki) - https://corkamiwiki.github.io/PE - https://github.com/corkami/docs/blob/master/PE/PE.md
* Peering Inside the PE: A Tour of the Win32 Portable Executable File Format - https://msdn.microsoft.com/en-us/library/ms809762.aspx
* PeLib Resources about the PE format - http://www.pelib.com/resources.php
* Portable Executable File Corruption Preventing Malware From Running
	+ What types of obstructions and anomalies in the PE file can make the Windows Portable Executable Image Loader and other PE parsing programs fail to load the file or display an error message?
	+ https://toddcullumresearch.com/2017/07/16/portable-executable-file-corruption/
* Portable Executable File Format – A Reverse Engineer View - http://www.stonedcoder.org/~kd/lib/CBJ-2005-74.pdf
* Peering Inside the PE: A Tour of the Win32 Portable Executable File Format - https://msdn.microsoft.com/en-us/library/ms809762.aspx
* Resource Hacker: a resource editor for 32-bit and 64-bit Windows applications
	- http://www.angusj.com/resourcehacker/
* Resources: Microsoft Portable Executable and COFF (32-bit and 64-bit) Format - http://bytepointer.com/resources/
* Robust Static Analysis of Portable Executable Malware - Katja Hahn, Master Thesis - https://github.com/katjahahn/PortEx/tree/master/masterthesis
* The sad state of PE parsing - http://lucasg.github.io/2017/04/28/the-sad-state-of-pe-parsing/
* The Undocumented Microsoft "Rich" Header - http://bytepointer.com/articles/the_microsoft_rich_header.htm
* Tiny PE: Creating the smallest possible PE executable - http://www.phreedom.org/research/tinype/
* Undocumented PECOFF - https://media.blackhat.com/bh-us-11/Vuksan/BH_US_11_VuksanPericin_PECOFF_WP.pdf
* Why does a corrupted binary sometimes result in "Program too big to fit in memory"? - https://blogs.msdn.microsoft.com/oldnewthing/20060130-00/?p=32483
* Why is 0x00400000 the default base address for an executable? - https://blogs.msdn.microsoft.com/oldnewthing/20141003-00/?p=43923

## Software

* Adlice PEViewer - https://www.adlice.com/download/roguekillerpe/
* Amber: Reflective PE packer
	+ https://github.com/EgeBalci/Amber
* bearparser: Portable Executable parsing library - https://github.com/hasherezade/bearparser
* CFF Explorer - http://www.ntcore.com/exsuite.php
* Corkami PE files corpus - https://github.com/corkami/pocs/tree/master/PE
* ExpDiff: Diff tool for comparing export tables in PE images - https://github.com/WalkingCat/ExpDiff
* fasm_packer: PE Packer written in x86 assembly (FASM syntax) - https://github.com/DimitriFourny/resources/tree/master/fasm_packer
* Five PE Analysis Tools Worth Looking At - https://blog.malwarebytes.com/threat-analysis/2014/05/five-pe-analysis-tools-worth-looking-at/
* libpeconv: A small library for mapping and unmapping PE files
	+ https://github.com/hasherezade/libpeconv
	+ Demo: RunPE (Process Hollowing) - https://github.com/hasherezade/libpeconv/tree/master/run_pe
	+ pe_unmapper: Small tool to convert a PE from a virtual format into a raw format
	+ https://github.com/hasherezade/libpeconv/tree/master/pe_unmapper
* Malware-Analayzer PE Tools - http://www.malware-analyzer.com/pe-tools
* Manalyze, a static analyzer for PE executables - https://manalyzer.org/ - https://github.com/JusticeRage/Manalyze
* MiTeC EXE Explorer: Executable File Explorer for OS/2, NE, PE32, PE32+ and VxD file types
	+ https://www.mitec.cz/exe.html
* pefile: a Python module to read and work with PE (Portable Executable) files - https://github.com/erocarrera/pefile
* PeLib: PE file manipulation library - https://github.com/avast-tl/pelib
* PeRebuilder - https://github.com/AaLl86/retroware
	+ automatically reconstruct the PE, and save it in a form that the Windows Loader is able to run (fixing the file alignment, relocating each section, fixing the import address table, and so on...)
* pev: The PE file analysis toolkit
	+ http://pev.sf.net
	+ https://github.com/merces/pev
* PEview - http://wjradburn.com/software/
* PE Anatomist - PE files internals
	- https://rammerlabs.alidml.ru/index-eng.html
	- https://rammerlabs.alidml.ru/peanatomist-eng.html
* PE Insider - http://cerbero.io/peinsider/
* PE Tools - Portable executable (PE) manipulation toolkit 
	+ Process Viewer, PE files Editor, Dumper, Rebuilder, Comparator, Analyzer
	+ https://petoolse.github.io/petools/
	+ https://github.com/petoolse/petools
* PE-bear - https://hshrzd.wordpress.com/pe-bear/
* pe-parse - Principled, lightweight C/C++ PE parser - https://github.com/trailofbits/pe-parse 
* PE-sieve: a small tool for investigating inline hooks (and other in-memory code patches) 
	+ https://hshrzd.wordpress.com/pe-sieve/
	+ https://github.com/hasherezade/pe-sieve
* pe_armor: Metamorphic PE packer generated and assembled by a Python code - https://github.com/DimitriFourny/resources/tree/master/pe_armor
* pe_recovery_tools: Helper tools for recovering dumped PE files - https://github.com/hasherezade/pe_recovery_tools
* pedump - dump windows PE files using Ruby - http://pedump.me/ - https://github.com/zed-0xff/pedump
* pelook: PE/COFF dump and conversion tool - http://bytepointer.com/tools/index.htm#pelook
* pestudio - https://www.winitor.com/
* peupdate: update hidden PE and PDB information in Win32/64 executables - http://bytepointer.com/tools/index.htm#peupdate
* PortEx: Java library to analyse Portable Executable files with a special focus on malware analysis and PE malformation robustness
	+ https://github.com/katjahahn/PortEx/
	+ http://katjahahn.github.io/PortEx/
	+ Robust Static Analysis of Portable Executable Malware - Katja Hahn, Master Thesis - https://github.com/katjahahn/PortEx/tree/master/masterthesis
	+ Wiki - https://github.com/katjahahn/PortEx/wiki
	+ PE Visualizer - https://github.com/katjahahn/PortEx/wiki/PE-Visualizer
* PPEE: A Professional PE File Explorer - https://www.mzrst.com/
* Process Dump: Windows tool for dumping malware PE files from memory back to disk for analysis
	+ http://split-code.com/processdump.html
	+ https://github.com/glmcdona/Process-Dump
	+ An Introduction to Dumping Malware with Process Dump - https://www.youtube.com/watch?v=dCU7N-Oh3jg
* rcedit: Command line tool to edit resources of EXE file on Windows
	- https://github.com/electron/rcedit
* Reflective PE Unloader
	+ This is code that can be used within a PE file to allow it to reflectively reconstruct itself in memory at runtime. The result is a byte for byte copy of the original PE file. This can be combined with Reflective DLL Injection to allow code to reconstruct itself after being loaded through an arbitrary means.
	+ https://github.com/zeroSteiner/reflective-polymorphism
* ripPE - section extractor and profiler for PE file analysis - https://github.com/matonis/ripPE
* Sizer - Win32/64 executable size report utility
	+ https://github.com/aras-p/sizer
	+ http://aras-p.info/projSizer.html
* Sizer - Win32 executable size report utility - https://github.com/tsafin/pdb-sizer
* SymbolSort: A Utility for Measuring C++ Code Bloat
	+ https://github.com/adrianstone55/SymbolSort
	+ http://gameangst.com/?p=320

### PE Loaders

- DreamLoader: Simple 32/64-bit PEs loader
	- https://github.com/86hh/DreamLoader
- In-Memory PE Loader: A very simple PE loader for loading DLLs into memory without using LoadLibray
	- https://github.com/nettitude/SimplePELoader

## PE: Talks

* 2018 - Reflective PE Unloading
	+ BSides Cleveland 2018; Spencer McIntyre
	+ https://www.youtube.com/watch?v=GbCVVYMNUzA
	+ http://www.irongeek.com/i.php?page=videos/bsidescleveland2018/b00-reflective-pe-unloading-spencer-mcintyre
* 2018 - DEF CON 26 - Relocation Bonus
	+ A look into the Windows Portable Executable (PE) header and how it can be weaponized to destroy parsers, disassemblers, and other tools
	+ DEFCON-26-Nick-Cano-Relocation-Bonus-Attacking-the-Win-Loader.pdf
	+ https://media.defcon.org/DEF%20CON%2026/DEF%20CON%2026%20presentations/Nick%20Cano/
	+ https://github.com/nickcano/RelocBonus
	+ https://github.com/nickcano/RelocBonusSlides
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
