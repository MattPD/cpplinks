# [C++ links](README.md): debugging: articles, documentation, software, and talks.

See also:

* [Executables](executables.md):
	+ [DWARF](https://github.com/MattPD/cpplinks/blob/master/executables.md#dwarf): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-2) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-2) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#talks-2)
	+ [PDB](https://github.com/MattPD/cpplinks/blob/master/executables.md#pdb-program-database): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#readings-5) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#software-5) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#talks-5)

# Contents

* [General](#general)
* [Standard Libraries](#standard-libraries)
* [Readings](#readings): [Books](#books), [Implementation](#implementation), [Software Engineering](#software-engineering), [Transparency](#transparency)
* [Software](#software):
	+ [GDB](#gdb): [Projects](#projects), [Readings](#readings-1), [Talks](#talks)
	+ [LLDB](#lldb): [Projects](#projects-1), [Readings](#readings-2), [Talks](#talks-1)
	+ [RR](#rr)
	+ [OS-specific](#os-specific): [Linux](#linux), [macOS](#macos), [Windows](#windows) - [WinDbg](#windbg)
	+ [Stack Trace & Unwinding](#stack-trace--unwinding)
* [Talks](#talks-2): [2018](#2018), [2017](#2017), [2016](#2016), [2015](#2015), [2014](#2014)

---

# General

* Program repair: Community-driven effort to facilitate discovery, access and systematization of data related to automated program repair research
	+ http://program-repair.org/
* UNIX Debugger Translation Table: gdb, lldb, dbx, adb, sdb
	+ https://www.lurklurk.org/debuggers.html

# Standard Libraries

* GLIBC (GNU C Library)
	+ General GLIBC Debugging Techniques - http://sourceware.org/glibc/wiki/Debugging/Development_Debugging
	+ GDB pretty-printers for GLIBC - http://sourceware.org/glibc/wiki/Debugging/Pretty_Printers
	+ Debugging the Loader - https://sourceware.org/glibc/wiki/Debugging/Loader_Debugging
	+ Backtraces - http://www.gnu.org/software/libc/manual/html_node/Backtraces.html
	+ Allocation Debugging - http://www.gnu.org/software/libc/manual/html_node/Allocation-Debugging.html
* libstdc++ Debug Mode: https://gcc.gnu.org/onlinedocs/libstdc++/manual/debug_mode.html
	+ Detecting incorrect C++ STL usage (libstdc++) - https://kristerw.blogspot.com/2018/03/detecting-incorrect-c-stl-usage.html
* libc++ Debug Mode: https://libcxx.llvm.org/docs/DesignDocs/DebugMode.html
* Visual C++ Debug Iterator Support: https://docs.microsoft.com/en-us/cpp/standard-library/debug-iterator-support

---

# Readings

* Debugging - Ian Lance Taylor - https://airs.com/ian/essays/debug/debug.html
* Delta Debugging
	+ https://www.st.cs.uni-saarland.de/dd/
	+ Delta: Heuristically minimizes interesting files
		- http://delta.stage.tigris.org/
	+ Minimizing Interesting Files with Delta
		- http://delta.stage.tigris.org/using_delta.html
* Devon H. O'Dell
	+ Building a Debugging Mindset - https://9vx.org/post/building-a-debugging-mindset/
	+ Debugging: Psychology, Theory, and Application - https://9vx.org/post/debugging-psychology-theory-and-application/
	+ The Debugging Mindset - https://queue.acm.org/detail.cfm?id=3068754
	+ https://speakerdeck.com/dho/building-a-debugging-mindset
* Henrik Warne
	+ Great Programmers Write Debuggable Code - https://henrikwarne.com/2013/05/05/great-programmers-write-debuggable-code/
	+ Finding Bugs: Debugger versus Logging - https://henrikwarne.com/2014/01/01/finding-bugs-debugger-versus-logging/
	+ Learning From Your Bugs - https://henrikwarne.com/2016/04/28/learning-from-your-bugs/
* How to Debug - John Regehr - https://blog.regehr.org/archives/199
* I tend to prefer debugging with release builds instead of debug builds - Ken Johnson (Skywing) - http://www.nynaeve.net/?p=184
* When debugging a stack overflow, you want to focus on the repeating recursive part - https://blogs.msdn.microsoft.com/oldnewthing/20090107-00/?p=19573

## Books

_Books, Books Reviews_

* Effective Debugging - https://www.spinellis.gr/debugging/
* Four Books on Debugging - https://blog.regehr.org/archives/849
* Geoff Wozniak
	+ On battle scars and debugging - http://wozniak.ca/blog/2018/01/15/On-battle-scars-and-debugging/
	+ From intuition to methodology in debugging - http://wozniak.ca/blog/2018/02/04/From-intuition-to-methodology-in-debugging/
	+ Formalizing debugging - https://wozniak.ca/blog/2018/03/25/Book-review-Formalizing-debugging/
* Why Programs Fail: A Guide to Systematic Debugging - http://www.whyprogramsfail.com/

## Implementation

* An Efficient and Generic Reversible Debugger using the Virtual Machine based Approach
	+ Virtual Execution Environments VEE 2005
	+ Toshihiko Koju, Shingo Takada, Norihisa Doi
	+ https://www.usenix.org/events/vee05/full_papers/p79-koju.pdf
* Compile Once Debug Twice: Picking a Compiler for Debuggability
	+ https://backtrace.io/blog/compile-once-debug-twice-picking-a-compiler-for-debuggability-1of3/
* Debugging with the natives - Stephen Kell
	+ part 1 - http://www.cl.cam.ac.uk/~srk31/blog/2016/02/25/#native-debugging-part-1
	+ part 2 - http://www.cl.cam.ac.uk/~srk31/blog/2017/01/30/#native-debugging-part-2
* Debugging the Debugger: Why Your Debugger Doesn’t Work When You Need it To
	+ https://backtrace.io/debuggingthedebugger/
* Fast, Flexible, Polyglot Instrumentation Support for Debuggers and other Tools
	+ The Art, Science, and Engineering of Programming, 2018, Vol. 2, Issue 3, Article 14
	+ Van De Vanter, Michael; Seaton, Chris; Haupt, Michael; Humer, Christian; Würthinger, Thomas
	+ http://programming-journal.org/2018/2/14/
* Eli Bendersky - http://eli.thegreenplace.net/tag/debuggers
	+ How debuggers work
		- Part 1 - Basics - http://eli.thegreenplace.net/2011/01/23/how-debuggers-work-part-1
		- Part 2 - Breakpoints - http://eli.thegreenplace.net/2011/01/27/how-debuggers-work-part-2-breakpoints
		- Part 3 - Debugging information - http://eli.thegreenplace.net/2011/02/07/how-debuggers-work-part-3-debugging-information
	+ An interesting tree serialization algorithm from DWARF - https://eli.thegreenplace.net/2011/09/29/an-interesting-tree-serialization-algorithm-from-dwarf
	+ The contents of DWARF sections - https://eli.thegreenplace.net/2011/12/26/the-contents-of-dwarf-sections
	+ Programmatic access to the call stack in C++ - https://eli.thegreenplace.net/2015/programmatic-access-to-the-call-stack-in-c/
* Framework for Instruction-level Tracing and Analysis of Program Executions
	+ VEE 2006
	+ https://www.usenix.org/legacy/events/vee06/full_papers/p154-bhansali.pdf
* How breakpoints are set - http://majantali.net/2016/10/how-breakpoints-are-set/
* How do debuggers keep track of the threads in your program?
	+ http://timetobleed.com/how-do-debuggers-keep-track-of-the-threads-in-your-program/
* How to code debuggers - Tomasz Wegrzanowski - https://t-a-w.blogspot.com/2007/03/how-to-code-debuggers.html
* Implementing a Debugger - Backtrace
	+ The Fundamentals - http://backtrace.io/blog/blog/2016/08/11/debugger-internals/
	+ Building a Go Debugger - https://backtrace.io/blog/building-a-go-debugger/
* Writing a basic Windows debugger - https://www.codeproject.com/Articles/43682/Writing-a-basic-Windows-debugger
* Writing a Debugger - Joseph Kain - http://system.joekain.com/debugger/
* Writing a Linux Debugger - Simon Brand
	+ 1\. Setup - https://blog.tartanllama.xyz/writing-a-linux-debugger-setup/
	+ 2\. Breakpoints - https://blog.tartanllama.xyz/writing-a-linux-debugger-breakpoints/
	+ 3\. Registers and memory - https://blog.tartanllama.xyz/writing-a-linux-debugger-registers/
	+ 4\. Elves and dwarves - https://blog.tartanllama.xyz/writing-a-linux-debugger-elf-dwarf/
	+ 5\. Source and signals - https://blog.tartanllama.xyz/writing-a-linux-debugger-source-signal/
	+ 6\. Source-level stepping - https://blog.tartanllama.xyz/writing-a-linux-debugger-dwarf-step/
	+ 7\. Source-level breakpoints - https://blog.tartanllama.xyz/writing-a-linux-debugger-source-break/
	+ 8\. Stack unwinding - https://blog.tartanllama.xyz/writing-a-linux-debugger-unwinding/
	+ 9\. Handling variables - https://blog.tartanllama.xyz/writing-a-linux-debugger-variables/
	+ 10\. Advanced topics - https://blog.tartanllama.xyz/writing-a-linux-debugger-advanced-topics/
	+ minidbg: A mini x86 linux debugger for teaching purposes - https://github.com/TartanLlama/minidbg
* (Windows) Data Breakpoints - https://blogs.msdn.microsoft.com/reiley/2011/07/21/data-breakpoints/
* (Windows) Side Effects of Debugger - https://blogs.msdn.microsoft.com/reiley/2011/08/27/side-effects-of-debugger/

## Software Engineering

* Are Automated Debugging Techniques Actually Helping Programmers?
	+ International Symposium on Software Testing and Analysis (ISSTA) 2011
	+ Chris Parnin, Alessandro Orso
	+ https://dl.acm.org/citation.cfm?id=2001445
* Automated Debugging: Are We There Yet?
	+ International Conference on Software Testing, Verification and Validation Workshops (ICSTW) 2011
	+ Alex Orso
	+ http://ieeexplore.ieee.org/document/5954471/
	+ 2013 talk
		- https://www.slideshare.net/alexorso/20130204dagstuhl-alex-orso
		- https://pdfs.semanticscholar.org/2436/0dc1bd271dcf3ecb73622e2c7b1d54a008bf.pdf
		- https://www.youtube.com/watch?v=WJHQnzLpVXk
* Failure Sketching: A Technique for Automated Root Cause Diagnosis of In-Production Failures
	+ SOSP 2015
	+ Baris Kasikci, Benjamin Schubert, Cristiano Pereira, Gilles Pokam, George Candea
	+ https://www.youtube.com/watch?v=99hXVFe33w8
	+ http://dslab.epfl.ch/proj/gist/
	+ http://dslab.epfl.ch/pubs/gist.pdf
	+ https://web.eecs.umich.edu/~barisk/public/gist-slides.pdf
	+ https://blog.acolyer.org/2015/10/12/failure-sketching-a-technique-for-automated-root-cause-diagnosis-of-in-production-failures/
* Debugging Reinvented: Asking and Answering Why and Why Not Questions about Program Behavior
	+ International Conference on Software Engineering ICSE 2008
	+ Andrew J. Ko, Brad A. Myers
		- http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.159.1425
		- https://dl.acm.org/citation.cfm?id=1368130
	+ Microsoft Research Talk:
		- https://www.microsoft.com/en-us/research/video/candidate-talk-debugging-reinvented-asking-and-answering-why-and-why-not-questions-about-program-behavior/
		- https://www.youtube.com/watch?v=ScZfggGa4qs
		- https://archive.org/details/Microsoft_Research_Video_103778
	+ "Static and dynamic program slicing algorithms for extracting and answering developers questions about program output that substantially decrease fault localization time."
	+ https://blog.acolyer.org/2014/10/17/debugging-reinvented/
* Failure Sketches: A Better Way to Debug
	+ HotOS 2015
	+ Baris Kasikci, Benjamin Schubert, Cristiano Pereira, Gilles Pokam, Madan Musuvathi, George Candea 
	+ https://www.usenix.org/conference/hotos15/workshop-program/presentation/kasikci
	+ http://dslab.epfl.ch/pubs/failure-sketches.pdf
	+ https://web.eecs.umich.edu/~barisk/public/fs-slides.pdf
* On The Dichotomy of Debugging Behavior Among Programmers
	+ ICSE 2018
	+ Moritz Beller, Niels Spruit, Diomidis Spinellis, Andy Zaidman
	+ http://pure.tudelft.nl/ws/files/38319543/paper.pdf
* Where Is the Bug and How Is It Fixed? An Experiment with Practitioners
	+ European Software Engineering Conference / Foundations of Software Engineering (ESEC/FSE) 2017
	+ Marcel Böhme, Ezekiel O. Soremekun, Sudipta Chattopadhyay, Emamurho Ugherughe, Andreas Zeller
	+ https://doi.org/10.1145/3106237.3106255
	+ https://www.comp.nus.edu.sg/~mboehme/paper/FSE17.pdf
	+ DBGBench - https://dbgbench.github.io/
	+ "the correct fault locations, bug diagnoses, and software patches of 27 real errors in open-source C projects that were consolidated from hundreds of debugging sessions of professional software engineers"
* Yesterday, my program worked. Today, it does not. Why?
	+ ESEC 1999
	+ Andreas Zeller 
	+ https://www.st.cs.uni-saarland.de/publications/details/zeller-esec-1999/

## Transparency

* 2017 - Ninja: Towards Transparent Tracing and Debugging on ARM
	+ USENIX Security 2017
	+ Zhenyu Ning, Fengwei Zhang
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/ning
	+ http://www.cs.wayne.edu/fengwei/paper/ninja-usenixsecurity17.pdf
* 2016 - Towards Transparent Debugging
	+ IEEE Transactions on Dependable and Secure Computing (TDSC'16), 2016.
	+ Fengwei Zhang, Kevin Leach, Angelos Stavrou, and Haining Wang
	+ http://www.cs.wayne.edu/fengwei/paper/malt-tdsc16.pdf
* 2015 - Using Hardware Features for Increased Debugging Transparency
	+ 36th IEEE Symposium on Security and Privacy (S&P'15), 2015
	+ Fengwei Zhang, Kevin Leach, Angelos Stavrou, Haining Wang, and Kun Sun
	+ http://www.cs.wayne.edu/fengwei/paper/malt-sp15.pdf

---

# Software

* edb: a cross platform x86/x86-64 debugger
	+ https://github.com/eteran/edb-debugger
* PulseDbg: Hypervisor-based debugger
	+ https://github.com/honorarybot/PulseDBG
* PyREBox: a Python scriptable Reverse Engineering sandbox
	+ "It is based on QEMU, and its goal is to aid reverse engineering by providing dynamic analysis and debugging capabilities from a different perspective. PyREBox allows to inspect a running QEMU VM, modify its memory or registers, and to instrument its execution, by creating simple scripts in python to automate any kind of analysis. QEMU (when working as a whole-system-emulator) emulates a complete system (CPU, memory, devices...). By using VMI techniques, it does not require to perform any modification into the guest operating system, as it transparently retrieves information from its memory at run-time."
	+ https://github.com/Cisco-Talos/pyrebox
* QIRA - QEMU Interactive Runtime Analyser
	+ http://qira.me/
	+ https://github.com/BinaryAnalysisPlatform/qira/
* Radare2
	+ Radare project started as a forensics tool, a scriptable commandline hexadecimal editor able to open disk files, but later support for analyzing binaries, disassembling code, debugging programs, attaching to remote gdb servers, etc.
	+ http://www.radare.org/
	+ https://github.com/radare/radare2
* rVMI - A New Paradigm For Full System Analysis
	+ "rVMI is a debugger on steroids. It leverages Virtual Machine Introspection (VMI) and memory forensics to provide full system analysis. This means that an analyst can inspect userspace processes, kernel drivers, and preboot environments in a single tool."
	+ https://github.com/fireeye/rVMI
	+ Black Hat USA 2017
		- https://www.blackhat.com/docs/us-17/thursday/us-17-Pfoh-rVMI-A-New-Paradigm-For-Full-System-Analysis.pdf
		- https://www.youtube.com/watch?v=KtoipviVJjw
* Vivisect / Vdb / Vtrace
	+ Vivisect - interactive disassembler
	+ Vtrace - a cross-platform & cross-architecture debugging API
	+ VDB - a cross-platform & cross-architecture debugger using Vtrace
	+ http://visi.kenshoto.com/viki/MainPage
	+ https://github.com/vivisect/vivisect
	+ documentation: http://fitblip.pub/vdb-fork/sphinx/
	+ fork & documentation: http://fitblip.pub/vdb-fork/
	+ Using a Custom VDB Debugger for Exploit Analysis - https://www.fireeye.com/blog/threat-research/2013/02/custom-vdb-debugger-exploit-analysis.html
	+ Malware Analysis with Vivisect - NEST - http://nest.unm.edu/files/5514/1254/9114/Malware_Analysis_with_Vivsect.pdf
	+ Binary Vivisection
		- https://www.singlehop.com/blog/binary-vivisection-part-1/
		- https://www.singlehop.com/blog/binary-vivisection-part-2/
		- https://www.singlehop.com/blog/binary-vivisection-part-3/
* Voltron - https://github.com/snare/voltron

## GDB

* GDB: The GNU Project Debugger
	+ https://sourceware.org/gdb/
	+ https://sourceware.org/gdb/documentation/
	+ https://sourceware.org/gdb/wiki/
* GDB - The Architecture of Open Source Applications - Stan Shebs
	+ http://aosabook.org/en/gdb.html

### Projects

* CGDB: Console front-end to the GNU debugger
	+ https://github.com/cgdb/cgdb
* Gdb Assembly Informant
	+ steps through your assembly code one instruction at a time and diffs register values
	+ https://github.com/thlorenz/gai
* GDB dashboard
	+ https://github.com/cyrus-and/gdb-dashboard
	+ https://metricpanda.com/tips-for-productive-debugging-with-gdb
* gdb-tools: Various tools to improve the gdb experience
	+ https://github.com/vuvova/gdb-tools
	+ gdb tools: duel and @PrettyPrinter - https://fosdem.org/2018/schedule/event/debugging_tools_gdb_tools/
* gdbgui: A browser-based frontend for GDB
	+ https://gdbgui.com/
	+ https://github.com/cs01/gdbgui
* GEF (GDB Enhanced Features)
	+ https://github.com/hugsy/gef
	+ https://github.com/hugsy/gef-scripts
	+ https://github.com/hugsy/gef-structs
	+ GEF Tutorials - https://www.youtube.com/playlist?list=PLjAuO31Rg972WeMvdR_57Qu-aVM8T6DkQ
	+ https://blahcat.github.io/2017/08/01/gef-at-black-hat-arsenal-us-2017/
	+ https://github.com/toolswatch/blackhat-arsenal-tools/blob/master/exploitation/gef.md
* libdebugme: Automatically drop to gdb on error
	+ https://github.com/yugr/libdebugme
* OnlineGDB
	+ "OnlineGDB an online compiler and debugger tool for C/C++ languages. It is world's first online IDE which gives debugging facility with embedded gdb."
	+ http://OnlineGDB.com
* PEDA - Python Exploit Development Assistance for GDB
	+ https://github.com/longld/peda
	+ https://eugenekolo.com/blog/better-disassembly-with-gdb-peda/
	+ http://ropshell.com/peda/Linux_Interactive_Exploit_Development_with_GDB_and_PEDA_Slides.pdf
* PINCE: front-end reverse engineering tool for the GDB - https://github.com/korcankaraokcu/PINCE
* pwndbg - Exploit Development and Reverse Engineering with GDB Made Easy
	+ https://github.com/pwndbg/pwndbg
	+ https://github.com/pwndbg/pwndbg/blob/dev/FEATURES.md
* Pwngdb - https://github.com/scwuaptx/Pwngdb
* pygdbmi - Get Structured Output from GDB's Machine Interface - https://github.com/cs01/pygdbmi
* SymGDB - symbolic execution plugin for gdb - https://github.com/SQLab/symgdb

#### Editor Integration

* neogdb.vim: Vim GDB front-end for neovim - https://github.com/huawenyu/neogdb.vim

#### Memory Debugging

* pahole-gdb: pahole implementation for gdb - https://github.com/PhilArmstrong/pahole-gdb
* gdb-heap
	+ https://github.com/rogerhu/gdb-heap
	+ https://fedorahosted.org/gdb-heap/
	+ https://fedoraproject.org/wiki/Features/MemoryDebuggingTools

#### Profiling

* gdbpmp: A GDB Based Wallclock Profiler - https://github.com/markhpc/gdbpmp
* gdbprof: A wall clock time-based profiler built on GDB's Python interface
	+ https://github.com/Muon/gdbprof
	+ https://github.com/markhpc/gdbprof
* GDB profiler: Rich man's profiler, a profiler for native OCaml and other executables
	+ https://github.com/copy/gdbprofiler

### Readings

* 8 gdb tricks you should know - https://blogs.oracle.com/ksplice/8-gdb-tricks-you-should-know
* Beej's Quick Guide to GDB - https://beej.us/guide/bggdb/
* Cheatsheet - https://github.com/jshaw87/Cheatsheets/blob/master/Cheatsheet_GDB.txt
* Displaying Stack Frames in gdb with Python - http://jefftrull.github.io/c++/gdb/python/2018/03/02/print-frame.html
* GDB Basics Tutorial - https://platform.avatao.com/paths/a0dc20fc-f1b5-43c9-89fc-3a5fccfb5f0b/challenges/166366b3-2e89-49ee-86a3-023663d197b7
* gdb Debugging Full Example (Tutorial): ncurses - http://www.brendangregg.com/blog/2016-08-09/gdb-example-ncurses.html
* GDB Tutorial - https://www.gdb-tutorial.net/
* GDB Tips and Tricks - Shane Kirk
	+ 1: A Tale of Two Terminals - http://www.shanekirk.com/2017/08/gdb-tips-and-tricks-1-a-tale-of-two-terminals/
	+ 2: Setting Breakpoints with Regular Expressions - http://www.shanekirk.com/2017/08/gdb-tips-and-tricks-2-setting-breakpoints-with-regular-expressions/
	+ 3: Saving and Restoring Breakpoints Using Files - http://www.shanekirk.com/2017/09/gdb-tips-and-tricks-3-saving-and-restoring-breakpoints-using-files/
	+ 4: Reverse Debugging - http://www.shanekirk.com/2017/10/gdb-tips-and-tricks-4-reverse-debugging/
	+ 5: The Display Command - http://www.shanekirk.com/2017/12/gdb-tips-and-tricks-5-the-display-command/
	+ 6: Examining Data Types - http://www.shanekirk.com/2018/02/gdb-tips-and-tricks-6-examining-data-types/
* GDB Wiki - https://sourceware.org/gdb/wiki/
* Hitchikers Guide To The GDB - http://apoorvaj.io/hitchhikers-guide-to-the-gdb.html
* How to point GDB to your sources - https://alex.dzyoba.com/blog/gdb-source-path/
* Introduction to Debuggers - Saumil Shah - http://www.slideshare.net/saumilshah/introduction-to-debuggers
* Julia Evans
	+ Three steps to learning GDB - https://jvns.ca/blog/2014/02/10/three-steps-to-learning-gdb/
	+ How does gdb work? - https://jvns.ca/blog/2016/08/10/how-does-gdb-work/
	+ How does gdb call functions? - https://jvns.ca/blog/2018/01/04/how-does-gdb-call-functions/
* Notes on GDB - https://publicclu2.blogspot.com/2013/05/notes-on-gdb.html
* Process Injection with GDB - https://magisterquis.github.io/2018/03/11/process-injection-with-gdb.html
* Skipping standard C++ library during debug session in gdb - https://xaizek.github.io/2016-05-26/skipping-standard-library-in-gdb/
* Victor Stinner's Notes - GDB: GNU debugger - http://vstinner.readthedocs.io/gdb.html

### Talks

* A flexible GDB (GNU Debugger) target description for processor diversity – SFO17-210
	+ http://connect.linaro.org/resource/sfo17/sfo17-210/
* Become a GDB Power User - ACCU 2016 - Greg Law - https://www.youtube.com/watch?v=713ay4bZUrw
	+ including Q&A: https://www.youtube.com/watch?v=6ag7yvhDAiE
* GDB: C++ conversion & dogfooding C++
	+ Pedro Alves, GNU Tools Cauldron 2017
	+ Slides: https://gcc.gnu.org/wiki/cauldron2017?action=AttachFile&do=view&target=gdb+-+C%2B%2B+conversion+%26+dogfood.pdf
	+ Video: https://slideslive.com/38902352/gdb-c-conversion-dogfooding-c
* GDB - A Lot More Than You Knew - CppCon 2016 - Greg Law  - https://www.youtube.com/watch?v=-n9Fkq1e6sg
* Give me 15 minutes & I'll change your view of GDB - CppCon 2015 - Greg Law - https://www.youtube.com/watch?v=PorfLSr3DDI
* SecurityTube GDB Expert (SGDE)
	+ Walkthroughs: https://github.com/Kan1shka9/Securitytube-Gnu-Debugger-Expert
	+ Course Videos: http://www.securitytube.net/tags/sgde
	+ https://www.youtube.com/playlist?list=PLiP0FxVgYuUz0kdK7L7YaI5n4qkOuymue
* Your Application versus GDB - FOSDEM 2014 - Tom Tromey
	+ https://archive.fosdem.org/2014/schedule/event/your_application_versus_gdb/
	+ https://www.youtube.com/watch?v=RwDA3oIOtWw

## LLDB

### Projects

* ds2: Debug server for lldb
	+ ds2 is a debug server designed to be used with LLDB to perform remote debugging of Linux, Android, FreeBSD, Windows and Windows Phone targets. Windows/Windows Phone support is still under active development.
	+ https://github.com/facebook/ds2
	+ 2015 LLVM Developers’ Meeting: Stephane Sezer "ds2, a tiny debug server used with lldb"
	+ https://www.youtube.com/watch?v=n00EhLskJWk&list=PL_R5A0lGi1AA4Lv2bBFSwhgDaHvvpVU21&index=27
* LLDB Scripts: A collection of LLDB aliases/regexes and Python scripts to aid in your debugging sessions
	+ https://github.com/DerekSelander/LLDB
	+ https://www.raywenderlich.com/162020/custom-lldb-commands-practice
	+ https://www.raywenderlich.com/161938/assembly-register-calling-convention-tutorial
* LLDB Scripts - Debugging the Swift Compiler
	+ https://github.com/apple/swift/blob/master/docs/DebuggingTheCompiler.rst#lldb-scripts
* lldbinit: Similar implementation of .gdbinit from fG! for lldb in python
	+ https://github.com/deroko/lldbinit
* Vegvisir: A browser based GUI for LLDB Debugger - https://github.com/ant4g0nist/vegvisir

#### Editor Integration

* CodeLLDB: a LLDB front end for Visual Studio Code - https://github.com/vadimcn/vscode-lldb
* LLDB Vim Frontend - https://github.com/gilligan/vim-lldb
* LLDB Neovim Frontend - https://github.com/dbgx/lldb.nvim

### Readings

* LLDB Cheat Sheet
	+ https://www.nesono.com/content/lldb-cheat-sheet
	+ https://www.nesono.com/sites/default/files/lldb%20cheat%20sheet.pdf
* LLDB for GDB Users – Command Summary - https://developer.apple.com/library/content/documentation/General/Conceptual/lldb-guide/chapters/A3-GDB-Summary.html
* LLDB to GDB Command Map - https://lldb.llvm.org/lldb-gdb.html

### Talks

* Bringing RenderScript to LLDB
	+ 2016 EuroLLVM Developers' Meeting; Luke Drummond & Ewan Crawford, Codeplay
	+ https://www.youtube.com/watch?v=BBC61L0QKCM
	+ http://www.llvm.org/devmtg/2016-03/Presentations/EuroLLVM2016-E.Crawford_and_L.Drummond-Bringing_RenderScript_to_LLDB.pdf
* Debugging Tips and Tricks - WWDC 2016 - https://developer.apple.com/videos/play/wwdc2016/417
* Debugging with LLDB - WWDC 2012 - https://developer.apple.com/videos/play/wwdc2012/415/
* ds2: a tiny debug server used with lldb
	+ 2015 LLVM Developers’ Meeting; Stephane Sezer, Facebook
	+ https://www.youtube.com/watch?v=n00EhLskJWk
	+ https://github.com/facebook/ds2
* LLDB Tutorial: Adding debugger support for your target
	+ 2016 EuroLLVM Developers' Meeting; Deepak Panickal & Andrzej Warzynski, Codeplay
	+ https://github.com/codeplaysoftware/lldb-msp430
	+ http://www.llvm.org/devmtg/2016-03/Tutorials/LLDB-tutorial.pdf
	+ https://www.youtube.com/watch?v=9hhDZeV0fYU
* Migrating from GDB to LLDB - WWDC 2011 - https://developer.apple.com/videos/play/wwdc2011/321/

## RR

* RR: Record and Replay Framework
	+ http://rr-project.org/
	+ https://github.com/mozilla/rr
* rr Paper: "Lightweight User-Space Record And Replay"
	+ http://robert.ocallahan.org/2016/10/rr-paper-lightweight-user-space-record.html
* Control Flow Visualizer (CFViz): an rr / gdb plugin
	+ https://botondballo.wordpress.com/2017/12/22/control-flow-visualizer-cfviz-an-rr-gdb-plugin/
	+ https://bitbucket.org/botond/cfviz
* Engineering Record And Replay For Deployability
	+ USENIX ATC 2017
	+ Robert O'Callahan, Chris Jones, Nathan Froyd, Kyle Huey, Albert Noll, Nimrod Partush
	+ https://arxiv.org/abs/1705.05937
	+ https://www.usenix.org/conference/atc17/technical-sessions/presentation/ocallahan
* Improved debugging with rr - https://techtalk.intersec.com/2018/03/improved-debugging-with-rr/

## OS-specific

### Linux

* ORC (Oops Rewind Capability) Unwinder
	+ [Commit ee9f8fce9964](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=ee9f8fce99640811b2b8e79d0d1dbe8bab69ba67)
	+ [Commit 39358a033b2e](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=39358a033b2e4432052265c1fa0f36f572d8cfb5)
	+ orc-unwinder.txt - https://github.com/torvalds/linux/blob/master/Documentation/x86/orc-unwinder.txt
	+ The Linux x86 ORC Stack Unwinder - http://www.codeblueprint.co.uk/2017/07/31/the-orc-unwinder.html
	+ The ORCs are coming - https://lwn.net/Articles/728339/
	+ x86: ORC unwinder (previously undwarf) - https://lwn.net/Articles/727553/
* Notes about an odd, esoteric, yet incredibly useful library: libthread_db
	+ http://timetobleed.com/notes-about-an-odd-esoteric-yet-incredibly-useful-library-libthread_db/

### macOS

* Chisel: a collection of LLDB commands to assist debugging iOS apps - https://github.com/facebook/chisel
* Mac OS X Debugging Magic - https://developer.apple.com/library/content/technotes/tn2124/_index.html

### Windows

* ArkDasm: 64-bit interactive disassembler and debugger for Windows
	+ http://www.arkdasm.com/
* DbgShell: A PowerShell front-end for the Windows debugger engine
	+ https://github.com/Microsoft/DbgShell/
* Debug Recipes (.NET and Windows problems) - https://github.com/lowleveldesign/debug-recipes
* Debugging in Visual Studio - https://docs.microsoft.com/en-us/visualstudio/debugger/debugger-feature-tour
* Debugging Tools for Windows (WinDbg, KD, CDB, NTSD)
	+ https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/
* Windows Debugging Tools - Debugging Resources
	+ https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/debugging-resources
* makin - reveal anti-debug tricks (Windows) - https://github.com/secrary/makin
* Nanomite - Windows Debugger for x64 and x86 - https://github.com/zer0fl4g/Nanomite/
* OllyDbg - http://www.ollydbg.de/
* x64dbg
	+ https://x64dbg.com/
	+ https://github.com/x64dbg/x64dbg

#### WinDbg

* Introduction to WinDbg and debugging Windows - series by Anand George
	+ https://www.youtube.com/playlist?list=PLhx7-txsG6t6n_E2LgDGqgvJtCHPL7UFu

##### Readings

* Collection of WinDBG resources - https://blogs.msdn.microsoft.com/reiley/2012/07/28/collection-of-windbg-resources/
* Debugger Data Model, Javascript & X64 Exception Handling - https://doar-e.github.io/blog/2017/12/01/debugger-data-model/
* Debugging Tools for Windows - https://blogs.msdn.microsoft.com/windbg/
* Stupid debugger tricks: Calling functions and methods - https://blogs.msdn.microsoft.com/oldnewthing/20070427-00/?p=27083
* Tutorial: Using WinDBG to call arbitrary functions — WinDBG kung-fu series
	+ http://cfc.kizzx2.com/index.php/tutorial-using-windbg-to-call-arbitrary-functions-windbg-kung-fu-series/
* Undocumented WinDBG - https://blogs.msdn.microsoft.com/reiley/2011/10/30/undocumented-windbg/
* Use Windows Debuggers for Non-Debugging Tasks - https://blogs.msdn.microsoft.com/reiley/2011/10/23/use-windows-debuggers-for-non-debugging-tasks/
* Using Function Evaluation in WinDBG - https://blogs.msdn.microsoft.com/reiley/2012/08/18/using-function-evaluation-in-windbg/
* WinDbg, Debugger Objects, and JavaScript! Oh, My! - https://www.osr.com/blog/2017/05/18/windbg-debugger-objects-javascript-oh/
* Yet Another Hello World - https://blogs.msdn.microsoft.com/reiley/2011/09/29/yet-another-hello-world/

##### Projects

* 0CCh Windbg extension - https://github.com/0cch/0cchext
* PyKd - Python extension for WinDBG to access Debug Engine
	+ https://githomelab.ru/pykd/pykd
	+ windbg-pack: Set of python scripts for WinDBG - https://githomelab.ru/pykd/windbg-pack
* TWindbg: PEDA-like debugger UI for WinDbg - https://github.com/bruce30262/TWindbg
* WDBGARK: WinDBG Anti-RootKit extension - https://github.com/swwwolf/wdbgark
* Winbagility: a tool to connect WinDbg on non /DEBUG Windows x64 systems
	+ http://winbagility.github.io
	+ https://github.com/Winbagility/Winbagility
* WinDBGtree: A command tree based on commands and extensions for Windows Kernel Debugging
	+ https://github.com/vagnerpilar/windbgtree

##### Time Travel Debugging

* Time Travel Debugging FAQ - https://blogs.msdn.microsoft.com/windbg/2017/10/20/time-travel-debugging-faq/
* Time Travel Debugging - Overview - https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/time-travel-debugging-overview
* Time Travel Debugging - Sample App Walkthrough - https://aka.ms/ttdtutorial
* CppCon 2017: Time Travel Debugging: Root Causing Bugs in Commercial Scale Software
	+ https://www.youtube.com/watch?v=l1YJTg_A914
* Defrag Tools #186 - Time Travel Debugging - Advanced
	+ https://channel9.msdn.com/Shows/Defrag-Tools/Defrag-Tools-186-Time-Travel-Debugging-Advanced

## Stack Trace & Unwinding

* Backward-cpp: a beautiful stack trace pretty printer for C++
	+ https://github.com/bombela/backward-cpp
* Boost.Stacktrace
	+ http://boostorg.github.io/stacktrace/
	+ https://github.com/boostorg/stacktrace
	+ http://www.boost.org/doc/libs/release/doc/html/stacktrace.html
* CppCon 2017: Dave Watson “C++ Exceptions and Stack Unwinding”
	+ https://www.youtube.com/watch?v=_Ivd3qzgT7U
* libgcc_s (GNU) - https://gcc.gnu.org/onlinedocs/gccint/Libgcc.html
	+ Data Definitions for libgcc_s - https://refspecs.linuxfoundation.org/LSB_5.0.0/LSB-Core-generic/LSB-Core-generic/libgcc-s-ddefs.html
	+ Interfaces for libgcc_s - https://refspecs.linuxfoundation.org/LSB_5.0.0/LSB-Core-generic/LSB-Core-generic/libgcc-s.html
	+ Interfaces Definitions for libgcc_s - https://refspecs.linuxfoundation.org/LSB_5.0.0/LSB-Core-generic/LSB-Core-generic/libgcc-sman.html
* libunwind (nongnu.org) - http://www.nongnu.org/libunwind/
* libunwind (PathScale) - https://github.com/pathscale/libunwind
* Programmatic access to the call stack in C++ - https://eli.thegreenplace.net/2015/programmatic-access-to-the-call-stack-in-c/
* pstack: Print stack traces of running processes. Uses its own ELF and DWARF parsing
	+ https://github.com/peadar/pstack
* quickstack: a tool to take call stack traces with minimal overheads
	+ https://github.com/yoshinorim/quickstack
* Unwind specification draft for GNU/Linux/ia64 (extends the exception ABI) - https://www.kernel.org/pub/linux/devel/gcc/unwind/

---

# Talks

## 2018

* Let's Write a Debugger!
	+ linux.conf.au 2018
	+ [Levente Kurusa](https://www.doc.ic.ac.uk/~lk1015/publications.html)
	+ https://rego.linux.conf.au/schedule/presentation/91/
	+ https://www.doc.ic.ac.uk/~lk1015/research/lca2018/
	+ https://opensource.com/article/18/1/how-debuggers-really-work
	+ https://www.youtube.com/watch?v=qS51kIHWARM
	+ https://github.com/levex/debugger-talk

## 2017

* Debugging the debugger - BSDCan 2017, Samy Bahra
	+ https://www.youtube.com/watch?v=wyF-hGGPJMs
	+ Compiler debug quality suite - https://github.com/backtrace-labs/cdqs
	+ http://www.bsdcan.org/2017/schedule/events/787.en.html
* Debugging Under Fire: Keep your Head when Systems have Lost their Mind • GOTO 2017 • Bryan Cantrill
	+ https://www.youtube.com/watch?v=30jNsCVLpAE
* How C++ Debuggers work - Simon Brand - Meeting C++ 2017
	+ https://meetingcpp.com/2017/talks/items/How_Cpp_Debuggers_Work.html
	+ https://www.youtube.com/watch?v=Q3Rm95Mk03c

## 2016

* Building a Debugging Mindset - QConSF 2016 - Devon H. O'Dell
	+ video: https://www.infoq.com/presentations/debugging-mindset
	+ slides: https://speakerdeck.com/dho/building-a-debugging-mindset
	+ transcript: https://9vx.org/post/building-a-debugging-mindset/
* How do Debuggers (Really) Work - Pawel Moll
	+ Linux Piter 2016 - https://www.youtube.com/watch?v=xqrxg3hl10o
	+ ELC 2015
		- https://www.youtube.com/watch?v=N1QSEY1El9o
		- https://vimeo.com/220644951
		- http://events.linuxfoundation.org/sites/events/files/slides/slides_16.pdf
* Post-mortem Debugging: could you be the one? - Surge 2016 - Abel Mathew
	+ https://www.youtube.com/watch?v=WHhorNLa934
* Timeless Debugging - USENIX Enigma 2016 - George Hotz
	+ https://www.youtube.com/watch?v=eGl6kpSajag

## 2015

* Debugging using an exact recording of a program's execution - C++Now 2015 - Julian Smith
	+ Undo's Live Recorder
	+ https://www.youtube.com/watch?v=NWWMogzgLS4

## 2014

* The VS Debugger: How It Works + Tips and Tricks - GoingNative 28 - Gabriel Ha, Gregg Miskelly, Steve Carroll
	+ https://channel9.msdn.com/Shows/C9-GoingNative/GoingNative-28-The-VS-Debugger-How-It-Works-Tips-and-Tricks
