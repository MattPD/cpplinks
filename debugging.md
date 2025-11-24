# [C++ links](README.md): debugging: articles, documentation, software, and talks.

See also:

- [Debugging - tracing](https://github.com/MattPD/cpplinks/blob/master/debugging.tracing.md): [Readings](https://github.com/MattPD/cpplinks/blob/master/debugging.tracing.md#readings); [Software](https://github.com/MattPD/cpplinks/blob/master/debugging.tracing.md#software); [Talks](https://github.com/MattPD/cpplinks/blob/master/debugging.tracing.md#talks)
- [Executables](executables.md):
	- [DWARF](https://github.com/MattPD/cpplinks/blob/master/executables.md#dwarf): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#dwarf-readings) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#dwarf-software) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#dwarf-talks)
	- [PDB](https://github.com/MattPD/cpplinks/blob/master/executables.md#pdb): [Readings](https://github.com/MattPD/cpplinks/blob/master/executables.md#pdb-readings) - [Software](https://github.com/MattPD/cpplinks/blob/master/executables.md#pdb-software) - [Talks](https://github.com/MattPD/cpplinks/blob/master/executables.md#pdb-talks)

# Contents

- [General](#general)
- [Standard Libraries](#standard-libraries)
- [Readings](#readings):
	- [Books](#books)
	- [Concurrency](#concurrency)
	- [Implementation](#implementation): [Correctness](#correctness)
	- [Reverse Debugging](#reverse-debugging)
	- [Software Engineering](#software-engineering)
	- [Transparency](#transparency)
- [Software](#software):
	- [GDB](#gdb): [Projects](#gdb-projects), [Readings](#gdb-readings), [Talks](#gdb-talks)
	- [LLDB](#lldb): [Projects](#lldb-projects), [Readings](#lldb-readings), [Talks](#lldb-talks)
	- [RR](#rr): [Projects](#rr-projects), [Readings](#rr-readings)
	- [OS-specific](#os-specific): [iOS](#iOS), [Linux](#linux), [macOS](#macos), [Windows](#windows) - [WinDbg](#windbg)
	- [Crash Analysis & Reporting](#crash-analysis--reporting)
- [Stack Trace & Unwinding](#stack-trace--unwinding)
- [Talks](#talks): [2023](#2023), [2021](#2021), [2019](#2019), [2018](#2018), [2017](#2017), [2016](#2016), [2015](#2015), [2014](#2014)

---

# General

- Program repair: Community-driven effort to facilitate discovery, access and systematization of data related to automated program repair research
	- https://program-repair.org/
- UNIX Debugger Translation Table: gdb, lldb, dbx, adb, sdb
	- https://www.lurklurk.org/debuggers.html
- Debug Adapter Protocol (DAP)
	- defines the abstract protocol used between a development tool (e.g., IDE or editor) and a debugger
	- https://microsoft.github.io/debug-adapter-protocol/
	- https://github.com/microsoft/debug-adapter-protocol

---

# Standard Libraries

- GLIBC (GNU C Library)
	- General GLIBC Debugging Techniques - http://sourceware.org/glibc/wiki/Debugging/Development_Debugging
	- GDB pretty-printers for GLIBC
		- http://sourceware.org/glibc/wiki/Debugging/Pretty_Printers
	- Debugging the Loader - https://sourceware.org/glibc/wiki/Debugging/Loader_Debugging
	- Backtraces - http://www.gnu.org/software/libc/manual/html_node/Backtraces.html
	- Allocation Debugging - http://www.gnu.org/software/libc/manual/html_node/Allocation-Debugging.html
- libstdc++ Debug Mode: https://gcc.gnu.org/onlinedocs/libstdc++/manual/debug_mode.html
	- Detecting incorrect C++ STL usage (libstdc++) - https://kristerw.blogspot.com/2018/03/detecting-incorrect-c-stl-usage.html
- libc++
	- Debug Mode: https://libcxx.llvm.org/docs/DesignDocs/DebugMode.html
	- GDB pretty-printers for libc++
		- https://github.com/llvm/llvm-project/blob/main/libcxx/utils/gdb/libcxx/printers.py
		- https://github.com/koutheir/libcxx-pretty-printers
- Skipping boring functions in debuggers
	- https://maskray.me/blog/2024-12-30-skipping-boring-functions-in-debuggers
- Visual C++ Debug Iterator Support: https://docs.microsoft.com/en-us/cpp/standard-library/debug-iterator-support

---

# Readings

- Debugging - Ian Lance Taylor - https://airs.com/ian/essays/debug/debug.html
- Debugging in the (Very) Large: Ten Years of Implementation and Experience
	- Symposium on Operating Systems Principles (SOSP) 2009
	- Kirk Glerum, Kinshuman Kinshumann, Steve Greenberg, Gabriel Aul, Vince Orgovan, Greg Nichols, David Grant, Gretchen Loihle, Galen Hunt
	- https://www.microsoft.com/en-us/research/publication/debugging-in-the-very-large-ten-years-of-implementation-and-experience/
	- https://www.sigops.org/sosp/sosp09/papers/glerum-sosp09.pdf
	- https://www.sigops.org/sosp/sosp09/slides/glerum-slides-sosp09.pdf
- debugging-stories: A collection of debugging stories
	- https://github.com/danluu/debugging-stories
	- http://danluu.com/teach-debugging/
- Delta Debugging
	- https://www.st.cs.uni-saarland.de/dd/
	- Delta: Heuristically minimizes interesting files
		- https://github.com/dsw/delta
	- Yesterday, my program worked. Today, it does not. Why?
		- ESEC 1999
		- Andreas Zeller
		- https://www.st.cs.uni-saarland.de/publications/details/zeller-esec-1999/
	- Picireny: Hierarchical Delta Debugging Framework
		- https://github.com/renatahodovan/picireny
	- Simplifying and Isolating Failure-Inducing Input
		- IEEE Transactions on Software Engineering 28(2) 2002
		- Andreas Zeller, Ralf Hildebrandt
		- https://www.st.cs.uni-saarland.de/publications/details/zeller-tse-2002/
		- https://blog.acolyer.org/2015/11/16/simplifying-and-isolating-failure-inducing-input/
		- Simplifying and Isolating Failure-Inducing Input: A Retrospective on Delta Debugging
			- IEEE Transactions on Software Engineering 51(3) 2025
			- Andreas Zeller, Ralf Hildebrandt
			- https://doi.ieeecomputersociety.org/10.1109/TSE.2025.3537167
	- HDD: Hierarchical Delta Debugging
		- ICSE 2006
		- Ghassan Misherghi, Zhendong Su
		- https://dl.acm.org/citation.cfm?id=1134307
		- https://blog.acolyer.org/2015/11/17/hierarchical-delta-debugging/
	- Generalizing and Criticizing Delta Debugging
		- 2011; John Regehr
		- https://blog.regehr.org/archives/527
	- Debugging Inputs
		- International Conference on Software Engineering (ICSE) 2020
		- Lukas Kirschner, Ezekiel Soremekun, and Andreas Zeller
		- https://www.dropbox.com/s/ddn3fe55lws1rdr/icse2020-ddmax.pdf
		- https://publications.cispa.saarland/3060/1/camera-ready-submission.pdf
		- https://conf.researchr.org/details/icse-2020/icse-2020-papers/119/Debugging-Inputs
		- ddmax implementations & experimental data: https://tinyurl.com/DebuggingInputs
- Devon H. O'Dell
	- Building a Debugging Mindset
		- https://9vx.org/post/building-a-debugging-mindset/
		- https://www.infoq.com/presentations/debugging-mindset
		- https://speakerdeck.com/dho/building-a-debugging-mindset
	- Debugging: Psychology, Theory, and Application - https://9vx.org/post/debugging-psychology-theory-and-application/
	- The Debugging Mindset - https://queue.acm.org/detail.cfm?id=3068754
- Henrik Warne
	- Great Programmers Write Debuggable Code - https://henrikwarne.com/2013/05/05/great-programmers-write-debuggable-code/
	- Finding Bugs: Debugger versus Logging - https://henrikwarne.com/2014/01/01/finding-bugs-debugger-versus-logging/
	- Learning From Your Bugs - https://henrikwarne.com/2016/04/28/learning-from-your-bugs/
- How to Debug - John Regehr - https://blog.regehr.org/archives/199
- I tend to prefer debugging with release builds instead of debug builds - Ken Johnson (Skywing) - http://www.nynaeve.net/?p=184
- Introduction to Procedural Debugging through Binary Libification
	- USENIX WOOT Conference on Offensive Technologies (WOOT) 2024
	- Jonathan Brossard
	- https://www.usenix.org/conference/woot24/presentation/brossard
	- WCC: The Witchcraft Compiler Collection
		- https://github.com/endrazine/wcc
- The Inflection Point Hypothesis: A Principled Debugging Approach for Locating the Root Cause of a Failure
	- Symposium on Operating Systems Principles (SOSP) 2019
	- Yongle Zhang, Kirk Rodrigues, Yu Luo, Michael Stumm, Ding Yuan
	- https://dl.acm.org/citation.cfm?id=3359650
	- https://blog.acolyer.org/2019/11/08/the-inflection-point-hypothesis/
- Unstripping Stripped Binaries
	- 2022; Tavis Ormandy
	- using STABS to debug stripped code
	- http://lock.cmpxchg8b.com/symbols.html
- What does debugging a program look like? - Julia Evans - https://jvns.ca/blog/2019/06/23/a-few-debugging-resources/
- When debugging a stack overflow, you want to focus on the repeating recursive part - Raymond Chen
	- https://devblogs.microsoft.com/oldnewthing/20090107-00/?p=19573

## Books

_Books, Books Reviews_

- Effective Debugging - https://www.spinellis.gr/debugging/
- Four Books on Debugging - https://blog.regehr.org/archives/849
- Geoff Wozniak
	- On battle scars and debugging - https://wozniak.ca/blog/2018/01/15/1/
	- From intuition to methodology in debugging - https://wozniak.ca/blog/2018/02/04/1/
	- Formalizing debugging - https://wozniak.ca/blog/2018/03/25/1/
	- The puzzling empathy of debugging - https://wozniak.ca/blog/2018/05/07/1/
	- Retro debugging - https://wozniak.ca/blog/2019/01/04/1/
- The Debugging Book: Tools and Techniques for Automated Software Debugging
	- Andreas Zeller
	- https://www.debuggingbook.org/
- Why Programs Fail: A Guide to Systematic Debugging - http://www.whyprogramsfail.com/

## Concurrency

- Debug Info for Concurrency in LLVM
	- 2023 LLVM Developers' Meeting
	- Adrian Prantl
	- https://www.youtube.com/watch?v=g4fei6Vl7o8
	- https://llvm.org/devmtg/2023-10/slides/quicktalks/Prantl-DebugInfoForConcurrency.pdf
- Interactive Debugging of Concurrent Programs under Relaxed Memory Models
	- CGO 2020
	- Aakanksha Verma, Pankaj Kumar Kalita, Awanish Pandey, and Subhajit Roy
	- Gambit: GDB Assisted Memory Behavior and Interference Tester
	- https://doi.org/10.1145/3368826.3377910

### Probe Effect

- A probe effect in concurrent programs
	- Software: Practice and Experience 16 (3)(1986)
	- J. Gait
	- https://doi.org/10.1002/spe.4380160304
- Debugging Concurrent Programs
	- ACM Computing Surveys (CSUR) 21(4) 1989
	- C. E. McDowell, D. P. Helmbold
	- https://users.soe.ucsc.edu/~dph/mypubs/debugConcProg89.pdf

## Implementation

- An Efficient and Generic Reversible Debugger using the Virtual Machine based Approach
	- Virtual Execution Environments (VEE) 2005
	- Toshihiko Koju, Shingo Takada, Norihisa Doi
	- https://www.usenix.org/events/vee05/full_papers/p79-koju.pdf
- Debin: Predicting Debug Information in Stripped Binaries
	- ACM CCS 2018
	- Jingxuan He, Pesho Ivanov, Petar Tsankov, Veselin Raychev, Martin Vechev
	- https://dl.acm.org/citation.cfm?id=3243866
	- https://www.youtube.com/watch?v=x1x_KtS-5Hs
	- https://github.com/eth-sri/debin
	- https://files.sri.inf.ethz.ch/website/papers/ccs18-debin.pdf
- Debuggers for Programming Languages
	- 2002 Book Chapter in "The Compiler Design Handbook: Optimizations and Machine Code Generation"
	- Sanjeev Kumar Aggarwal, M. Sarath Kumar
	- https://www.taylorfrancis.com/books/9781420040579/chapters/10.1201%2F9781420040579-12
- Debugging with the natives - Stephen Kell
	- part 1 - http://www.cl.cam.ac.uk/~srk31/blog/2016/02/25/#native-debugging-part-1
	- part 2 - http://www.cl.cam.ac.uk/~srk31/blog/2017/01/30/#native-debugging-part-2
- Debugging Native Extensions of Dynamic Languages
	- International Conference on Managed Languages & Runtimes (ManLang) 2018
	- Jacob Kreindl, Manuel Rigger, Hanspeter Mössenböck
	- https://doi.org/10.1145/3237009.3237017
	- http://ssw.jku.at/General/Staff/Kreindl/papers/ManLang_2018_SulongDebugging.pdf
- Debugging with Intelligence via Probabilistic Inference
	- Zhaogui Xu, Shiqing Ma, Xiangyu Zhang, Shuofei Zhu, Baowen Xu
	- International Conference on Software Engineering (ICSE) 2018
	- https://www.cs.rutgers.edu/~sm2283/papers/ICSE18.pdf
	- https://blog.acolyer.org/2018/06/19/debugging-with-intelligence-via-probabilistic-inference/
- Debugopt: Debugging fully optimized natively compiled programs using multistage instrumentation
	- Science of Computer Programming 169 (2019)
	- Jie Yin, Gang Tan, Hao Li, Xiaolong Bai, Yu Ping Wang, Shi Min Hu
	- https://www.sciencedirect.com/science/article/pii/S0167642318303629
	- https://oslab.cs.tsinghua.edu.cn/debugopt/debugopt.html
- Demystifying Debuggers - Ryan Fleury
	- https://www.rfleury.com/p/posts-table-of-contents#demystifying-debuggers-series
	- Part 1: A Busy Intersection
		- 2024-12-16
		- https://www.rfleury.com/p/demystifying-debuggers-part-1-a-busy
	- Part 2: The Anatomy Of A Running Program
		- 2024-12-22
		- https://www.rfleury.com/p/demystifying-debuggers-part-2-the
	- Part 3: Debugger-Kernel Interaction
		- 2024-12-28
		- https://www.rfleury.com/p/demystifying-debuggers-part-3-kernel
- Eli Bendersky - http://eli.thegreenplace.net/tag/debuggers
	- How debuggers work
		- Part 1 - Basics - http://eli.thegreenplace.net/2011/01/23/how-debuggers-work-part-1
		- Part 2 - Breakpoints - http://eli.thegreenplace.net/2011/01/27/how-debuggers-work-part-2-breakpoints
		- Part 3 - Debugging information - http://eli.thegreenplace.net/2011/02/07/how-debuggers-work-part-3-debugging-information
	- An interesting tree serialization algorithm from DWARF - https://eli.thegreenplace.net/2011/09/29/an-interesting-tree-serialization-algorithm-from-dwarf
	- The contents of DWARF sections - https://eli.thegreenplace.net/2011/12/26/the-contents-of-dwarf-sections
	- Programmatic access to the call stack in C++ - https://eli.thegreenplace.net/2015/programmatic-access-to-the-call-stack-in-c/
- Fast, Flexible, Polyglot Instrumentation Support for Debuggers and other Tools
	- The Art, Science, and Engineering of Programming, 2018, Vol. 2, Issue 3, Article 14
	- Van De Vanter, Michael; Seaton, Chris; Haupt, Michael; Humer, Christian; Würthinger, Thomas
	- http://programming-journal.org/2018/2/14/
- Framework for Instruction-level Tracing and Analysis of Program Executions
	- Virtual Execution Environments (VEE) 2006
	- https://www.usenix.org/legacy/events/vee06/full_papers/p154-bhansali.pdf
	- iDNA: Time Travel Debugging
		- Instruction-level Tracing: Framework & Applications
		- Sanjay Bhansali
		- http://www.cs.wisc.edu/areas/pl/seminar/fall05/Bhansali.ppt
- How breakpoints are set - http://majantali.net/2016/10/how-breakpoints-are-set/
- How Debuggers Work - Michał Górny
	- Getting and Setting x86 Registers, Part 1 - https://www.moritz.systems/blog/how-debuggers-work-getting-and-setting-x86-registers-part-1/
	- Getting and Setting x86 Registers, Part 2: XSAVE - https://www.moritz.systems/blog/how-debuggers-work-getting-and-setting-x86-registers-part-2/
- How do debuggers keep track of the threads in your program?
	- https://web.archive.org/http://timetobleed.com/how-do-debuggers-keep-track-of-the-threads-in-your-program/
- How to code debuggers - Tomasz Wegrzanowski - https://t-a-w.blogspot.com/2007/03/how-to-code-debuggers.html
- Making a low level (Linux) debugger
	- part 1: assembly - https://web.archive.org/https://blog.asrpo.com/making_a_low_level_debugger
	- part 2: C - https://web.archive.org/https://blog.asrpo.com/making_a_low_level_debugger_part_2
	- part 3: our first program - https://web.archive.org/https://blog.asrpo.com/making_a_low_level_debugger_part_3
- Making an AMDGPU debugger
	- Marcell Kiss
	- part I - The Plan: https://martty.github.io/posts/radbg_part_1/
	- part II - The Devk: https://martty.github.io/posts/radbg_part_2/
	- part III - Trap handler: https://martty.github.io/posts/radbg_part_3/
	- part IV - Grand finale: https://martty.github.io/posts/radbg_part_4/
- On-Stack Replacement, Distilled
	- Programming Language Design and Implementation (PLDI) 2018
	- Daniele Cono D'Elia and Camil Demetrescu
	- https://pldi18.sigplan.org/event/pldi-2018-papers-on-stack-replacement-distilled
	- http://season-lab.github.io/papers/osr-distilled-pldi18.pdf
	- https://github.com/dcdelia/tinyvm
	- "As a novel application of OSR, we present a feasibility study on debugging of optimized code, showing how our techniques can be used to fix variables holding incorrect values at breakpoints due to optimizations."
- Samy Al Bahra, Backtrace
	- Compiler debug quality suite - https://github.com/backtrace-labs/cdqs
	- Compile Once Debug Twice: Picking a Compiler for Debuggability
		- https://engineering.backtrace.io/compile-once-debug-twice/
	- Debugging the Debugger: Why Your Debugger Doesn’t Work When You Need it To
		- BSDCan 2017; Samy Al Bahra
		- https://www.bsdcan.org/2017/schedule/events/787.en.html
		- https://www.youtube.com/watch?v=wyF-hGGPJMs
	- Implementing a Debugger - Backtrace
		- The Fundamentals - https://engineering.backtrace.io/2016-08-11-debugger-internals/
		- Building a Go Debugger - https://engineering.backtrace.io/2016-11-23-building-a-go-debugger/
- Writing a basic Windows debugger - https://www.codeproject.com/Articles/43682/Writing-a-basic-Windows-debugger
- Writing a Debugger - Joseph Kain - http://system.joekain.com/debugger/
- Writing a Debugger From Scratch - DbgRs - Tim Misiak
	- DbgRs: A Windows debugger written in Rust, for educational purposes
		- https://github.com/TimMisiak/dbgrs
	- Part 1 - Attaching to a Process
		- https://www.timdbg.com/posts/writing-a-debugger-from-scratch-part-1/
	- Part 2 - Register State and Stepping
		- https://www.timdbg.com/posts/writing-a-debugger-from-scratch-part-2/
	- Part 3 - Reading Memory
		- https://www.timdbg.com/posts/writing-a-debugger-from-scratch-part-3/
	- Part 4 - Exports and Private Symbols
		- https://www.timdbg.com/posts/writing-a-debugger-from-scratch-part-4/
	- Part 5 - Breakpoints
		- https://www.timdbg.com/posts/writing-a-debugger-from-scratch-part-5/
	- Part 6 - Stacks
		- https://www.timdbg.com/posts/writing-a-debugger-from-scratch-part-6/
	- Part 7 - Disassembly
		- https://www.timdbg.com/posts/writing-a-debugger-from-scratch-part-7/
	- Part 8 - Source and Symbols
		- https://www.timdbg.com/posts/writing-a-debugger-from-scratch-part-8/
- Writing a Linux Debugger - Simon Brand
	- 1\. Setup - https://blog.tartanllama.xyz/writing-a-linux-debugger-setup/
	- 2\. Breakpoints - https://blog.tartanllama.xyz/writing-a-linux-debugger-breakpoints/
	- 3\. Registers and memory - https://blog.tartanllama.xyz/writing-a-linux-debugger-registers/
	- 4\. Elves and dwarves - https://blog.tartanllama.xyz/writing-a-linux-debugger-elf-dwarf/
	- 5\. Source and signals - https://blog.tartanllama.xyz/writing-a-linux-debugger-source-signal/
	- 6\. Source-level stepping - https://blog.tartanllama.xyz/writing-a-linux-debugger-dwarf-step/
	- 7\. Source-level breakpoints - https://blog.tartanllama.xyz/writing-a-linux-debugger-source-break/
	- 8\. Stack unwinding - https://blog.tartanllama.xyz/writing-a-linux-debugger-unwinding/
	- 9\. Handling variables - https://blog.tartanllama.xyz/writing-a-linux-debugger-variables/
	- 10\. Advanced topics - https://blog.tartanllama.xyz/writing-a-linux-debugger-advanced-topics/
	- minidbg: A mini x86 linux debugger for teaching purposes - https://github.com/TartanLlama/minidbg
- (Windows) Data Breakpoints - https://blogs.msdn.microsoft.com/reiley/2011/07/21/data-breakpoints/
- (Windows) Side Effects of Debugger - https://blogs.msdn.microsoft.com/reiley/2011/08/27/side-effects-of-debugger/

### Implementation: 2025

- Implementation of the Debugging Support for the LLVM Outlining Optimization
	- Sinteza 2025: International Scientific Conference on Information Technology, Computer Science, and Data Science
	- Vojislav Tomašević, Đorđe Todorović, Maja Vukasović
	- https://doi.org/10.15308/sinteza-2025-233-240
	- https://portal.sinteza.singidunum.ac.rs/Media/files/2025/233-240.pdf
- Writing a Windows ARM64 Debugger for Reverse Engineering: KoiDbg
	- 2025-05-03
	- João Vitor
	- https://keowu.re/posts/Writing-a-Windows-ARM64-Debugger-for-Reverse-Engineering-KoiDbg/
	- KoiDbg: Windows ARM64 Debugger for Reverse Engineering
		- https://github.com/keowu/koidbg

### Implementation: 2023

- D2X: An eXtensible conteXtual Debugger for Modern DSLs
	- CGO 2023
	- Ajay Brahmakshatriya, Saman Amarasinghe
	- https://dl.acm.org/doi/abs/10.1145/3579990.3580014
	- http://groups.csail.mit.edu/commit/papers/2023/ajay-cgo23-d2x.pdf
	- https://zenodo.org/record/7459640

### Correctness

- A data-driven approach to debug info quality
	- 2024 LLVM Developers' Meeting
	- Emil Pedersen
	- https://www.youtube.com/watch?v=zluvVkxK6oY
	- https://llvm.org/devmtg/2024-10/slides/studenttalks/Pedersen-DataDrivenApproachToDebugInfoQuality.pdf
- Accurate Coverage Metrics for Compiler-Generated Debugging Information
	- ACM SIGPLAN International Conference on Compiler Construction (CC) 2024
	- J. Ryan Stinnett, Stephen Kell
	- https://arxiv.org/abs/2402.04811
	- https://dl.acm.org/doi/10.1145/3640537.3641578
	- EuroLLVM 2024
		- https://convolv.es/talks/debug-info-metrics/
		- https://www.youtube.com/watch?v=LePAdLTRa4Q
		- https://convolv.es/talks/2024/EuroLLVM/Debug%20info%20metrics.pdf
- Automatic Generation of Debug Headers through BlackBox Equivalence Checking
	- International Symposium on Code Generation and Optimization (CGO) 2022
	- Vaibhav Kiran Kurhe, Pratik Karia, Shubhani Gupta, Abhishek Rose, Sorav Bansal
	- https://doi.org/10.1109/CGO53902.2022.9741273
	- https://doi.org/10.5281/zenodo.5788478
	- https://sorav.compiler.ai/pubs/debugheaders.pdf
- Compilation Consistency Modulo Debug Information
	- ASPLOS 2023
	- Theodore Luo Wang, Yongqiang Tian, Yiwen Dong, Zhenyang Xu, Chengnian Sun
	- https://dl.acm.org/doi/10.1145/3575693.3575740
	- https://chengniansun.bitbucket.io/public/publication/asplos23/
	- https://doi.org/10.5281/zenodo.7217505
- Debugging Debug Information with Neural Networks
	- IEEE Access (2022)
	- Fiorella Artuso, Giuseppe Antonio Di Luna, Leonardo Querzoni
	- https://ieeexplore.ieee.org/abstract/document/9779237
- Debug Information Validation for Optimized Code
	- PLDI 2020
	- Yuanbo Li, Shuo Ding, Qirun Zhang, Davide Italiano
	- https://helloqirun.github.io/papers/pldi20_yuanbo1.pdf
	- https://www.cc.gatech.edu/~qrzhang/projects/debug/debug.html
	- https://pldi20.sigplan.org/details/pldi-2020-papers/60/Debug-Information-Validation-for-Optimized-Code
	- Debugging Information Testing
		- A Python reimplementation for the debug-information testing framework for the paper
		- https://github.com/yuanboli233/debug-info-testing
- DTD: Comprehensive and Scalable Testing for Debuggers
	- ACM International Conference on the Foundations of Software Engineering (FSE) 2024
	- Hongyi Lu, Zhibo Liu, Shuai Wang, Fengwei Zhang
	- https://doi.org/10.1145/3643779
	- https://jwnhy.github.io/papers/dtd-fse24.pdf
	- https://github.com/jwnhy/DTD
- GCC gOlogy: studying the impact of optimizations on debugging
	- 2018; Alexandre Oliva
	- https://www.fsfla.org/~lxoliva/writeups/gOlogy/gOlogy.txt
	- GNU Tools Cauldron 2018 slides: https://www.fsfla.org/~lxoliva/writeups/gOlogy/slides.pdf
- Improving debug locations for variables in memory in optimized code
	- 2022 EuroLLVM Developers' Meeting
	- Orlando Cazalet-Hyams
	- https://www.snsystems.com/technology/tech-blog/improving-debug-locations-for-variables-in-memory
	- https://llvm.org/devmtg/2022-05/slides/2022EuroLLVM-ImprovingDebugLocations-for-Variables-in-Memory.pdf
	- https://www.youtube.com/watch?v=wSmveKsWSSY
- Improving debug variable location coverage by using even more SSA
	- 2021 LLVM Developers' Meeting
	- Jeremy Morse
	- https://www.youtube.com/watch?v=yxuwfNnp064
	- https://llvm.org/devmtg/2021-11/slides/2021-ImprovingDebugVariableLocations.pdf
	- https://www.snsystems.com/technology/tech-blog/improving-debug-variable-location-coverage-by-using-even-more-ssa
- Improving optimized code line table quality
	- 2024 LLVM Developers' Meeting
	- Orlando Cazalet-Hyams
	- https://www.youtube.com/watch?v=yj1EUzXVP1I
	- https://llvm.org/devmtg/2024-10/slides/techtalk/Cazalet-Hyams-Improving-optimized-code-line-table-quality.pdf
	- https://discourse.llvm.org/t/rfc-proposed-update-to-handling-debug-locations-in-llvm/79244
	- https://discourse.llvm.org/t/rfc-improving-is-stmt-placement-for-better-interactive-debugging/82668
- LLVM and debug information quality
	- Triplefault 2020; Djordje Todorovic
	- https://www.youtube.com/watch?v=GpMLt1oecOk
- Possible issues with debugging and inspecting compiler-optimized binaries
	- 2020; William Cohen
	- https://developers.redhat.com/blog/2020/03/13/possible-issues-with-debugging-and-inspecting-compiler-optimized-binaries/
- Robustifying Debug Information Updates in LLVM via Control-Flow Conformance Analysis
	- 2025 ACM SIGPLAN Conference on Programming Language Design and Implementation (PLDI)
	- Shan Huang, Jingjing Liang, Ting Su, Qirun Zhang
	- https://doi.org/10.1145/3729267
	- https://github.com/ecnusse/MetaLoc
	- https://www.youtube.com/watch?v=n_Kkaa4wJCo
- Secure Delivery of Program Properties Through Optimizing Compilation
	- ACM International Conference on Compiler Construction (CC) 2020
	- Son Tuan Vu, Karine Heydemann, Arnaud de Grandmaison, Albert Cohen
	- https://research.google/pubs/pub48841/
	- "We propose an approach to encode, translate, and preserve the semantics of both functional and non-functional properties along the optimizing compilation of C to machine code. The approach involves (1) capturing and translating source-level properties through lowering passes and intermediate representations, such that data and control flow optimizations will preserve their consistency with the transformed program, and (2) carrying properties and their translation as debug information down to machine code."
	- "A fortunate side-effect of inserting artificial definitions is to prevent most optimization passes from harming the observed variables’ debug information."
- Source-Level Debugging of Compiler-Optimised Code: Ill-Posed, but Not Impossible
	- 2024 ACM SIGPLAN International Symposium on New Ideas, New Paradigms, and Reflections on Programming and Software (Onward!)
	- Stephen Kell and J. Ryan Stinnett
	- https://doi.org/10.1145/3689492.3690047
	- https://convolv.es/papers/2024/Onward!/debug-info-vision.pdf
- Testing Debug Info of Optimised Programs
	- KLEE Workshop 2022
	- J. Ryan Stinnett, Stephen Kell
	- https://srg.doc.ic.ac.uk/klee22/talks/Stinnett-Testing-Debug-Info.pdf
	- https://www.youtube.com/watch?v=SIYPYP06fY0
	- https://convolv.es/talks/testing-debug-info/
	- https://github.com/jryans/debug-info-issues
- Where Did My Variable Go? Poking Holes in Incomplete Debug Information
	- ASPLOS 2023
	- Cristian Assaiante, Daniele Cono D'Elia, Giuseppe Antonio Di Luna, Leonardo Querzoni
	- https://arxiv.org/abs/2211.09568
	- https://dl.acm.org/doi/10.1145/3575693.3575720
	- https://github.com/cristianassaiante/incomplete-debuginfo
- Who is Debugging the Debuggers? Exposing Debug Information Bugs in Optimized Binaries
	- ASPLOS 2021
	- Giuseppe Antonio Di Luna, Davide Italiano, Luca Massarelli, Sebastian Osterlund, Cristiano Giuffrida, Leonardo Querzoni
	- https://arxiv.org/abs/2011.13994

#### Correctness: 2000-2009

- A Fully-Non-transparent Solution to the Code Location Problem
	- International Workshop on Software and Compilers for Embedded Systems (SCOPES) 2008
	- Hugo Venturini
	- https://doi.org/10.1145/1361096.1361108
	- https://scopesconf.org/scopes-08/presentations/13_slides.pdf
- A Practical, Robust Method for Generating Variable Range Tables
	- CC 2001: Compiler Construction
	- Caroline Tice, Susan L. Graham
	- https://link.springer.com/chapter/10.1007/3-540-45306-7_8
	- https://bitsavers.org/pdf/dec/tech_reports/SRC-RR-165.pdf
- Key Instructions: Solving the Code Location Problem for Optimized Code
	- 2000 Compaq Systems Research Center Research Report 164
	- Caroline Tice, Susan L. Graham
	- https://www.hpl.hp.com/techreports/Compaq-DEC/SRC-RR-164.html
- Proving the Correctness of Algorithmic Debugging for Functional Programs
	- Trends in Functional Programming (TFP) 2006
	- Olaf Chitil, Yong Luo
	- https://www.cs.kent.ac.uk/pubs/2007/2863/content.pdf

#### Correctness: 1990-1999

- A New Approach to Debugging Optimized Code
	- PLDI 1992
	- Gary Brooks, Gilbert J. Hansen, Steve Simmons
	- https://doi.org/10.1145/143095.143108
- An Annotated Bibliography on Debugging Optimized Code
	- Digital Technical Journal, Volume 10, Number 1, 1998
	- Ronald F. Brender
	- http://web.archive.org/web/20050329205642/http://research.compaq.com:80/wrl/DECarchives/DTJ/DTJT07/DTJT07BIHM.HTM
- Correctness Proofs of Compilers and Debuggers: an Approach Based on Structural Operational Semantics
	- 1992 Ph.D. dissertation; Fabio Q. B. da Silva
	- http://hdl.handle.net/1842/13542
	- http://www.lfcs.inf.ed.ac.uk/reports/92/ECS-LFCS-92-241/
- Debugging Optimized Code with Dynamic Deoptimization
	- PLDI 1992
	- Urs Hölzle, Craig Chambers, David Ungar
	- https://dl.acm.org/doi/10.1145/143103.143114
	- https://bibliography.selflanguage.org/dynamic-deoptimization.html
- Debugging Optimized Code Without Being Misled
	- ACM Transactions on Programming Languages and Systems (TOPLAS) 16(3) 1994
	- Max Copperman
	- https://people.eecs.berkeley.edu/~fateman/264/papers/copperman.pdf
- Debugging Optimized Code: Concepts and Implementation on DIGITAL Alpha Systems
	- Digital Technical Journal, Volume 10, Number 1, 1998
	- Ronald F. Brender, Jeffrey E. Nelson, Mark E. Arsenault
	- https://www.hpl.hp.com/hpjournal/dtj/vol10num1/vol10num1art7.pdf
- Formally Defining Debuggers: A Comparison of Three Approaches
	- International Workshop on Automated Debugging (AADEBUG) 1995
	- Karen L. Bernstein, Eugene W. Stark
	- http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.2511
- Non-Transparent Debugging of Optimized Code
	- 1999 Ph.D. dissertation; Caroline Mae Tice
	- https://www2.eecs.berkeley.edu/Pubs/TechRpts/1999/6232.html
- Operational Semantics of a Focusing Debugger
	- Electronic Notesin Theoretical Computer Science 1 (1995)
	- Karen L. Bernstein, Eugene W.Stark
	- http://dx.doi.org/10.1016/S1571-0661(04)80002-1
- OPTVIEW: A New Approach for Examining Optimized Code
	- ACM SIGPLAN Workshop on Program Analysis for Software Tools and Engineering (PASTE) 1998
	- Caroline Tice and Susan L. Graham
	- https://doi.org/10.1145/277631.277636
- Source-Level Debugging of Scalar Optimized Code
	- PLDI 1996
	- Ali-Reza Adl-Tabatabai, Thomas Gross
	- https://dl.acm.org/doi/10.1145/249069.231388

#### Testing

- Comparing The Quality Of Debug Information Produced By Clang And GCC
	- https://robert.ocallahan.org/2018/11/comparing-quality-of-debug-information.html
	- debuginfo-quality: Evaluate the quality of debuginfo in an ELF binary
		- https://github.com/rocallahan/debuginfo-quality
- Continuous integration with GDB Buildbot
	- https://developers.redhat.com/blog/2020/02/17/continuous-integration-with-gdb-buildbot/
- Debug Frame Checking: Check `.eh_frame` and `.debug_frame` information
	- https://github.com/francesco-zappa-nardelli/eh_frame_check
- DExTer (Debugging Experience Tester)
	- https://github.com/llvm/llvm-project/tree/main/cross-project-tests/debuginfo-tests/dexter
	- https://github.com/SNSystems/dexter
	- Measuring the User Debugging Experience
		- 2018 European LLVM Developers Meeting; Greg Bedwell
		- https://www.youtube.com/watch?v=XRT_GmpGjXE
		- https://llvm.org/devmtg/2018-04/slides/Bedwell-Measuring_the_User_Debugging_Experience.pdf
		- https://llvm.org/devmtg/2018-04/slides/Bedwell-Measuring_the_User_Debugging_Experience_poster.png
		- https://www.snsystems.com/technology/tech-blog/measuring-the-user-debug-experience
- Feedback-Directed Differential Testing of Interactive Debuggers
	- ESEC/FSE 2018
	- Daniel Lehmann, Michael Pradel
	- http://software-lab.org/publications/fse2018.pdf
	- https://github.com/sola-da/DifferentialDebuggerTesting
- Interactive Metamorphic Testing of Debuggers
	- ISSTA 2019
	- Sandro Tolksdorf, Daniel Lehmann, Michael Pradel
	- https://conf.researchr.org/event/issta-2019/issta-2019-technical-papers-interactive-metamorphic-testing-of-debuggers
- llvm-debuginfo-analyzer: Print a logical representation of low-level debug information
	- llvm-debuginfo-analyzer parses debug and text sections in binary object files and prints their contents in a logical view, which is a human readable representation that closely matches the structure of the original user source code. Supported object file formats include ELF, Mach-O, PDB and COFF.
	- https://llvm.org/docs/CommandGuide/llvm-debuginfo-analyzer.html
	- https://github.com/llvm/llvm-project/tree/main/llvm/tools/llvm-debuginfo-analyzer
	- https://github.com/SNSystems/llvm-debuginfo-analyzer
	- (original tool, not maintained) DIVA - Debug Information Visual Analyzer
		- DIVA is a command line tool that processes DWARF debug information contained within ELF files and prints the semantics of that debug information. The DIVA output is designed to be understandable by software programmers without any low-level compiler or DWARF knowledge; as such, it can be used to report debug information bugs to the compiler provider.
		- https://github.com/SNSystems/DIVA
		- 2017 EuroLLVM Developers’ Meeting lightning talk
			- video: https://www.youtube.com/watch?v=SwtpXaCk2bE
			- slides: http://llvm.org/devmtg/2017-03/assets/slides/diva_debug_information_visual_analyzer.pdf
- lldb-eval fuzzer: Finding bugs in an LLDB-based expression evaluator
	- 2021 LLVM Developers' Meeting; Tonko Sabolčec
	- https://www.youtube.com/watch?v=dJ9k7-pmwvM
	- https://llvm.org/devmtg/2021-11/slides/2021-LLDB-eval-fuzzer-Finding-Bugs-In-LLDB-based-expression-evaluator.pdf
- lldb-repro: a utility to transparently capture and replay debugger sessions through the command line driver
	- used to test the reproducers by running the test suite twice
	- https://github.com/llvm/llvm-project/tree/main/lldb/utils/lldb-repro
	- An Introduction to LLDB Reproducers
		- https://pspdfkit.com/blog/2020/an-introduction-to-lldb-reproducers/
- Samy Al Bahra, Backtrace
	- Compiler debug quality suite - https://github.com/backtrace-labs/cdqs

## Reverse Debugging

See also: [RR](#rr), [WinDbg - Time Travel Debugging](https://github.com/MattPD/cpplinks/blob/master/debugging.md#time-travel-debugging)

- A Review of Reverse Debugging
	- System, Software, SoC and Silicon Debug Conference (S4D) 2012
	- Jakob Engblom
	- https://ieeexplore.ieee.org/document/6338149/
	- http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.338.3420&rep=rep1&type=pdf
- A Taxonomy of Execution Replay Systems
	- 2003 International Conference on Advances in Infrastructure for Electronic Business, Education, Science, Medicine, and Mobile Technologies on the Internet
	- Frank Cornelis, Andy Georges, Mark Christiaens, Michiel Ronsse, Tom Ghesquiere, Koen De Bosschere
	- https://www.researchgate.net/publication/244149898_A_Taxonomy_of_Execution_Replay_Systems
- An Interactive Debugging Approach Based on Time-traveling Queries
	- 2023 PhD Dissertation
	- Maximilian Ignacio Willembrinck Santander
	- https://theses.hal.science/tel-04512544
	- https://github.com/Willembrinck/2023-Selective-Time-Traveling-Thesis
- Deterministic Replay: A Survey
	- ACM Computing Surveys 48(2) 2015
	- Yunji Chen, Shijin Zhang, Qi Guo, Ling Li, Ruiyang Wu, Tianshi Chen
	- https://doi.org/10.1145/2790077
- Don’t Panic: Reverse Debugging of Kernel Drivers
	- Foundations of Software Engineering (ESEC/FSE) 2015
	- Pavel Dovgalyuk, Denis Dmitriev, Vladimir Makarov
	- https://dl.acm.org/citation.cfm?doid=2786805.2803179
	- Review (Jakob Engblom): Reverse Debug with Hardware in the Loop - http://jakob.engbloms.se/archives/2432
- Efficient Algorithms for Bidirectional Debugging
	- Programming Language Design and Implementation (PLDI) 2000
	- B. Boothe
	- https://dl.acm.org/citation.cfm?id=349339
- Expositor: Scriptable Time-Travel Debugging with First Class Traces
	- International Conference on Software Engineering (ICSE) 2013
	- Yit Phang Khoo, Jeffrey S. Foster, Michael Hicks
	- http://www.cs.umd.edu/~mwh/papers/khoo13expositor.html
	- full version - http://www.cs.umd.edu/~mwh/papers/khoo13expositor-journal.html
- Implementation of Live Reverse Debugging in LLDB
	- 2021
	- Anthony Savidis, Vangelis Tsiatsianas
	- https://arxiv.org/abs/2105.12819
	- https://github.com/vangelists/llvm-project/wiki/Reverse-Debugging
- Improving the performance of reverse debugging
	- Programming and Computer Software 43(1) 2017
	- Klimushenkova, M.A. & Dovgalyuk, P.M.
	- https://link.springer.com/article/10.1134/S0361768817010042
- POMP: Postmortem Program Analysis with Hardware-Enhanced Post-Crash Artifacts
	- USENIX Security 2017
	- Jun Xu, Dongliang Mu, Xinyu Xing, Peng Liu, Ping Chen, Bing Mao
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/xu-jun
	- https://github.com/junxzm1990/pomp
- Processor-Oblivious Record and Replay
	- Robert Utterback, Kunal Agrawal, I-Ting Angelina Lee, Milind Kulkarni
	- ACM SIGPLAN Symposium on Principles and Practice of Parallel Programming (PPoPP) 2017
		- https://dl.acm.org/doi/10.1145/3018743.3018764
	- ACM Transactions on Parallel Computing (TOPC) 6(4) 2019
		- https://dl.acm.org/doi/abs/10.1145/3365659
	- PORRidge: Processor Obvivious Record and Replay
		- A runtime system to deterministically record lock acquires and replay them on an arbitrary number of cores
		- https://github.com/wustl-pctg/PORRidge
- REPT: Reverse Debugging of Failures in Deployed Software
	- USENIX Symposium on Operating Systems Design and Implementation (OSDI) 2018
	- Weidong Cui, Xinyang Ge, Baris Kasikci, Ben Niu, Upamanyu Sharma, Ruoyu Wang, Insu Yun
	- https://www.usenix.org/conference/osdi18/presentation/weidong
	- https://www.microsoft.com/en-us/research/publication/rept-reverse-debugging-of-failures-in-deployed-software/
- Reverse Debugging of Kernel Failures in Deployed Systems
	- USENIX Annual Technical Conference (ATC) 2020
	- Xinyang Ge, Ben Niu, Weidong Cui
	- https://www.microsoft.com/en-us/research/publication/reverse-debugging-of-kernel-failures-in-deployed-systems/
- Reverse History
	- Part One – Background - http://jakob.engbloms.se/archives/1547
	- Part Two – Research - http://jakob.engbloms.se/archives/1554
	- Part Three – Products - http://jakob.engbloms.se/archives/1564
- Transition Watchpoints: Teaching Old Debuggers New Tricks
	- The Art, Science, and Engineering of Programming, 2017, Vol. 1, Issue 2, Article 16
	- Kapil Arya, Tyler Denniston, Ariel Rabkin, Gene Cooperman
	- http://programming-journal.org/2017/1/16/

### Reverse Debugging: Talks

- How do Time Travel Debuggers Work? - Design and Implementation of a Time Travel Debugger
	- C++Now 2024
	- Greg Law
	- https://www.youtube.com/watch?v=NiGzdv84iDE
	- https://github.com/boostcon/cppnow_presentations_2024/blob/main/Presentations/How_do_Time_Travel_Debuggers_Work.pdf

## Software Engineering

- A Survey on Software Fault Localization
	- IEEE Transactions on Software Engineering 42(8) (2016)
	- W. Eric Wong, Ruizhi Gao, Yihao Li, Rui Abreu, Franz Wotawa
	- https://www.researchgate.net/publication/291951202_A_Survey_on_Software_Fault_Localization
- Are Automated Debugging Techniques Actually Helping Programmers?
	- International Symposium on Software Testing and Analysis (ISSTA) 2011
	- Chris Parnin, Alessandro Orso
	- https://dl.acm.org/citation.cfm?id=2001445
	- ISSTA 2021 Impact Paper Award Talk
		- https://www.youtube.com/watch?v=W6os29gTA3I
- Automated Debugging: Are We There Yet?
	- International Conference on Software Testing, Verification and Validation Workshops (ICSTW) 2011
	- Alex Orso
	- http://ieeexplore.ieee.org/document/5954471/
	- 2013 talk
		- https://www.slideshare.net/alexorso/20130204dagstuhl-alex-orso
		- https://pdfs.semanticscholar.org/2436/0dc1bd271dcf3ecb73622e2c7b1d54a008bf.pdf
		- https://www.youtube.com/watch?v=WJHQnzLpVXk
- Debugging Reinvented: Asking and Answering Why and Why Not Questions about Program Behavior
	- International Conference on Software Engineering ICSE 2008
	- Andrew J. Ko, Brad A. Myers
		- http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.159.1425
		- https://dl.acm.org/citation.cfm?id=1368130
	- Microsoft Research Talk:
		- https://www.microsoft.com/en-us/research/video/candidate-talk-debugging-reinvented-asking-and-answering-why-and-why-not-questions-about-program-behavior/
		- https://www.youtube.com/watch?v=ScZfggGa4qs
		- https://archive.org/details/Microsoft_Research_Video_103778
	- "Static and dynamic program slicing algorithms for extracting and answering developers questions about program output that substantially decrease fault localization time."
	- https://blog.acolyer.org/2014/10/17/debugging-reinvented/
- On The Dichotomy of Debugging Behavior Among Programmers
	- ICSE 2018
	- Moritz Beller, Niels Spruit, Diomidis Spinellis, Andy Zaidman
	- https://dl.acm.org/doi/10.1145/3180155.3180175
	- https://inventitech.com/assets/publications/2018_beller_spruit_spinellis_zaidman_on_the_dichotomy_of_debugging_behavior_among_programmers.pdf
- Where Is the Bug and How Is It Fixed? An Experiment with Practitioners
	- European Software Engineering Conference / Foundations of Software Engineering (ESEC/FSE) 2017
	- Marcel Böhme, Ezekiel O. Soremekun, Sudipta Chattopadhyay, Emamurho Ugherughe, Andreas Zeller
	- https://doi.org/10.1145/3106237.3106255
	- https://mboehme.github.io/paper/FSE17.pdf
	- DBGBench
		- https://dbgbench.github.io/
		- "the correct fault locations, bug diagnoses, and software patches of 27 real errors in open-source C projects that were consolidated from hundreds of debugging sessions of professional software engineers"

## Transparency

- Ninja: Towards Transparent Tracing and Debugging on ARM
	- USENIX Security 2017
	- Zhenyu Ning, Fengwei Zhang
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/ning
- Towards Transparent Debugging
	- IEEE Transactions on Dependable and Secure Computing (TDSC) 2016
	- Fengwei Zhang, Kevin Leach, Angelos Stavrou, and Haining Wang
	- https://doi.org/10.1109/TDSC.2016.2545671
	- https://compass.sustech.edu.cn/paper/malt-tdsc18.pdf
- Using Hardware Features for Increased Debugging Transparency
	- 36th IEEE Symposium on Security and Privacy (S&P) 2015
	- Fengwei Zhang, Kevin Leach, Angelos Stavrou, Haining Wang, and Kun Sun
	- https://doi.org/10.1109/SP.2015.11
	- https://compass.sustech.edu.cn/paper/malt-sp15.pdf

---

# Software

- Blinkenlights: a command line debugger that focuses on visualizing how software changes memory
	- able to emulate statically linked i8086 and x86_64-pc-linux-gnu programs on the Linux, Mac, Windows, FreeBSD, NetBSD, and OpenBSD platforms
	- https://justine.lol/blinkenlights/
- dbg: A macro for printf-style debugging fans
	- https://github.com/sharkdp/dbg-macro
- Debug Break: break into the debugger programmatically
	- debugbreak.h allows you to put breakpoints in your C/C++ code with a call to debug_break()
	- Supports GCC, Clang and MSVC.
	- Works well on ARM, AArch64, i686, x86-64, POWER and has a fallback code path for other architectures.
	- https://github.com/scottt/debugbreak
- IDD: A System for Differential Debugging
	- https://github.com/compiler-research/idd
	- Debugging Regressions: Interactive Differential Debugging
		- 2025 EuroLLVM Developers' Meeting
		- Vipul Cariappa, Martin Vassilev
		- https://www.youtube.com/watch?v=sI-jxB0tGpM
		- https://llvm.org/devmtg/2025-04/slides/technical_talk/cariappa_Debugging.pdf
- ppstep: Interactive C/C++ preprocessor macro debugger
	- https://github.com/notfoundry/ppstep
- QIRA: QEMU Interactive Runtime Analyser
	- http://qira.me/
	- https://github.com/BinaryAnalysisPlatform/qira/
- Radare2: Libre Reversing Framework for Unix Geeks
	- Radare project started as a forensics tool, a scriptable commandline hexadecimal editor able to open disk files, but later support for analyzing binaries, disassembling code, debugging programs, attaching to remote gdb servers, etc.
	- http://www.radare.org/
	- https://github.com/radare/radare2
- ret-sync: Reverse-Engineering Tools SYNChronization
	- A set of plugins to synchronize a debugging session (WinDbg/GDB/LLDB/OllyDbg/OllyDbg2/x64dbg) with IDA/Ghidra disassemblers.
	- https://github.com/bootleg/ret-sync
- Vivisect / Vdb / Vtrace
	- Vivisect: interactive disassembler
	- Vtrace: a cross-platform & cross-architecture debugging API
	- VDB: a cross-platform & cross-architecture debugger using Vtrace
	- https://github.com/vivisect/vivisect
	- documentation: http://fitblip.pub/vdb-fork/sphinx/
	- fork & documentation: http://fitblip.pub/vdb-fork/
	- Using a Custom VDB Debugger for Exploit Analysis
		- https://web.archive.org/web/20210921035401/https://www.fireeye.com/blog/threat-research/2013/02/custom-vdb-debugger-exploit-analysis.html
	- Malware Analysis with Vivisect
		- Colin Williams; NEST
		- https://web.archive.org/http://nest.unm.edu/files/5514/1254/9114/Malware_Analysis_with_Vivsect.pdf
	- Binary Vivisection
		- http://www.singlehop.com/blog/binary-vivisection-part-1/
		- http://www.singlehop.com/blog/binary-vivisection-part-2/
		- http://www.singlehop.com/blog/binary-vivisection-part-3/
	- FireEye Labs Query-Oriented Debugger
		- Command-line and Python debugger for instrumenting and modifying native software behavior on Windows and Linux
		- https://github.com/fireeye/flare-qdb
		- Querying Dynamic State using the FireEye Labs Query-Oriented Debugger (flare-qdb)
			- https://www.fireeye.com/blog/threat-research/2017/01/flare_script_series.html
- Voltron: A hacky debugger UI for hackers
	- "Voltron is an extensible debugger UI toolkit written in Python. It aims to improve the user experience of various debuggers (LLDB, GDB, VDB and WinDbg) by enabling the attachment of utility views that can retrieve and display data from the debugger host. By running these views in other TTYs, you can build a customised debugger user interface to suit your needs."
	- https://github.com/snare/voltron

## Software: Editor Integration

- nvim-dap: Debug Adapter Protocol client implementation for Neovim
	- https://github.com/mfussenegger/nvim-dap
- vimspector: A multi-language debugging system for Vim
	- https://github.com/puremourning/vimspector

## Software: Virtual Machine Introspection

- LibVMI: Simplified Virtual Machine Introspection
	- "LibVMI is a virtual machine introspection library. This means that it helps you access the memory of a running virtual machine. LibVMI provides primitives for accessing this memory using physical or virtual addresses and kernel symbols. LibVMI also supports accessing memory from a physical memory snapshot, which is helpful for debugging or forensic analysis."
	- https://github.com/libvmi/libvmi
- PulseDbg: Hypervisor-based debugger
	- https://github.com/honorarybot/PulseDBG
- PyREBox: a Python scriptable Reverse Engineering sandbox
	- "It is based on QEMU, and its goal is to aid reverse engineering by providing dynamic analysis and debugging capabilities from a different perspective. PyREBox allows to inspect a running QEMU VM, modify its memory or registers, and to instrument its execution, by creating simple scripts in python to automate any kind of analysis. QEMU (when working as a whole-system-emulator) emulates a complete system (CPU, memory, devices...). By using VMI techniques, it does not require to perform any modification into the guest operating system, as it transparently retrieves information from its memory at run-time."
	- https://github.com/Cisco-Talos/pyrebox
	- http://blog.talosintelligence.com/2017/07/pyrebox.html
- pyvmidbg: LibVMI-based debug server, implemented in Python
	- Building a guest aware, stealth and agentless full-system debugger
	- https://github.com/Wenzel/pyvmidbg
	- Building a Flexible Hypervisor-Level Debugger
		- Insomni'hack 2019; Mathieu Tarral
		- https://drive.google.com/open?id=1ZMUszfwWDOljdDfPOJgkEfSabNy0UAJR
- r2vmi: Hypervisor-Level Debugger based on Radare2 / LibVMI, using VMI IO and debug plugins
	- https://github.com/Wenzel/r2vmi
	- Hack.lu 2018: Hypervisor-Level Debugger: Benefits And Challenges - Mathieu Tarral
		- https://www.youtube.com/watch?v=NnWYT-kCx_s
	- r2con2018 - Hypervisor Level Debugger with r2 - Mathieu Tarral
		- https://www.youtube.com/watch?v=JOJMgWa7E6A
		- https://github.com/radareorg/r2con2018/tree/master/talks/10-hypervisor-level-debugger
- rVMI: A New Paradigm For Full System Analysis
	- "rVMI is a debugger on steroids. It leverages Virtual Machine Introspection (VMI) and memory forensics to provide full system analysis. This means that an analyst can inspect userspace processes, kernel drivers, and preboot environments in a single tool."
	- https://github.com/fireeye/rVMI
	- https://www.fireeye.com/blog/threat-research/2017/09/rvmi-full-system-analysis.html
	- Black Hat USA 2017
		- https://www.blackhat.com/docs/us-17/thursday/us-17-Pfoh-rVMI-A-New-Paradigm-For-Full-System-Analysis.pdf
		- https://www.youtube.com/watch?v=tEVevKVLs3s
- xendbg: A modern Xen debugger
	- "`xendbg` is a feature-complete reference implementation of a modern Xen VMI debugger, superseding Xen's own limited and rarely-maintained [`gdbsx`](https://github.com/mirage/xen/tree/master/tools/debugger/gdbsx). It can debug both paravirtualized (PV) and hardware virtualized (HVM) guests, and provides both a standalone REPL and an LLDB server mode."
	- https://github.com/nccgroup/xendbg
	- Xendbg: A Full-Featured Debugger for the Xen Hypervisor
		- https://www.nccgroup.trust/us/about-us/newsroom-and-events/blog/2019/january/xendbg-a-full-featured-debugger-for-the-xen-hypervisor/
- Virtual Machine Introspection: Modular and extensible library for Virtual Machine Introspection
	- https://github.com/vmi-rs/vmi

## GDB

- GDB: The GNU Project Debugger
	- https://sourceware.org/gdb/
	- https://sourceware.org/gdb/documentation/
	- https://sourceware.org/gdb/wiki/
- GDB - The Architecture of Open Source Applications - Stan Shebs
	- http://aosabook.org/en/gdb.html

### GDB: Projects

- asm2cfg: GDB extension to add commands to view and save disassembled functions as a dot control-flow graphs
	- https://github.com/Kazhuu/asm2cfg
- CGDB: Console front-end to the GNU debugger
	- https://github.com/cgdb/cgdb
- Gdb Assembly Informant
	- steps through your assembly code one instruction at a time and diffs register values
	- https://github.com/thlorenz/gai
- GDB dashboard
	- https://github.com/cyrus-and/gdb-dashboard
	- https://metricpanda.com/tips-for-productive-debugging-with-gdb
- GDB helper scripts
	- https://github.com/tromey/gdb-helpers
- gdb-command: Library for manipulating gdb in batch mode
	- Rust
	- Execution of target program (Local type)
	- Opening core of target program (Core type)
	- Attaching to remote process (Remote type)
	- https://github.com/anfedotoff/gdb-command
- gdb-gui: A gdb gui written in Python, running inside gdb itself
	- https://github.com/tromey/gdb-gui
- gdb-helpers: GDB helper scripts
	- https://github.com/tromey/gdb-helpers
- gdb-tools: Various tools to improve the gdb experience
	- https://github.com/vuvova/gdb-tools
	- gdb tools: duel and @PrettyPrinter - https://fosdem.org/2018/schedule/event/debugging_tools_gdb_tools/
- gdb-walkers: Bring mdb walkers to gdb, also add other helpful commands.
	- https://github.com/hardenedapple/gdb-walkers
	- GDB pipelines -- convenience iteration over inferior data structures
		- Bringing MDB's "walkers" to GDB
		- FOSDEM 2020; Matthew Malcomson
		- https://fosdem.org/2020/schedule/event/debugging_gdb_pipelines/
- GDBFrontend
	- "an easy, flexible and extensionable gui debugger"
	- https://github.com/rohanrhu/gdb-frontend
- gdbgui: A browser-based frontend for GDB
	- https://gdbgui.com/
	- https://github.com/cs01/gdbgui
- GdbShellPipe: Enable piping of internal command output to external commands
	- https://github.com/hq6/GdbShellPipe
- GDBundle: Plugin Manager for GDB and LLDB
	- https://github.com/memfault/gdbundle
	- gdbundle - GDB and LLDB's Missing Plugin Manager
		- https://interrupt.memfault.com/blog/gdbundle-plugin-manager
- Gede: a graphical frontend (GUI) to GDB written in Qt
	- http://gede.acidron.com/
	- mirror: https://github.com/Nanoseb/gede
- GEF (GDB Enhanced Features)
	- https://github.com/hugsy/gef
	- https://github.com/hugsy/gef-scripts
	- https://github.com/hugsy/gef-structs
	- GEF Tutorials - https://www.youtube.com/playlist?list=PLjAuO31Rg972WeMvdR_57Qu-aVM8T6DkQ
	- https://blahcat.github.io/posts/2017/08/01/gef-at-black-hat-arsenal-us-2017.html
	- https://github.com/toolswatch/blackhat-arsenal-tools/blob/master/exploitation/gef.md
- gf: A GDB Frontend
	- A GDB frontend for Linux.
	- https://github.com/nakst/gf
- libdebugme: Automatically drop to gdb on error
	- https://github.com/yugr/libdebugme
- OnlineGDB
	- "OnlineGDB an online compiler and debugger tool for C/C++ languages. It is world's first online IDE which gives debugging facility with embedded gdb."
	- http://OnlineGDB.com
- PEDA - Python Exploit Development Assistance for GDB
	- https://github.com/longld/peda
	- https://web.archive.org/web/20160126173234/https://eugenekolo.com/blog/better-disassembly-with-gdb-peda/
	- http://ropshell.com/peda/Linux_Interactive_Exploit_Development_with_GDB_and_PEDA_Slides.pdf
- PINCE: front-end reverse engineering tool for the GDB - https://github.com/korcankaraokcu/PINCE
- pwndbg - Exploit Development and Reverse Engineering with GDB Made Easy
	- https://github.com/pwndbg/pwndbg
	- https://github.com/pwndbg/pwndbg/blob/dev/FEATURES.md
- Pwngdb - https://github.com/scwuaptx/Pwngdb
- pygdbmi - Get Structured Output from GDB's Machine Interface - https://github.com/cs01/pygdbmi
- QuickPatch: a GDB plug-in to patch an ELF file
	- https://github.com/invictus1306/QuickPatch
	- https://invictus1306.github.io/vulnerabilities/2019/10/20/quickpatch.html
- Seer - a GUI frontend to gdb
	- https://github.com/epasveer/seer
- SymGDB - symbolic execution plugin for gdb
	- https://github.com/SQLab/symgdb

#### GDB: Projects: Decompilation

- decomp2dbg: A plugin to introduce a generic API for decompiler support in GDB
	- https://github.com/mahaloz/decomp2dbg

#### GDB: Projects: Editor Integration

- GDB-MI: a package by Nick Roberts which makes Emacs use GDB/MI interface to talk with the GNU Debugger
	- https://www.emacswiki.org/emacs/GDB-MI
- GDB graphical interface for GNU Emacs
	- https://github.com/weirdNox/emacs-gdb
- Native Debug
	- GDB & LLDB Debugger support for VSCode
	- https://marketplace.visualstudio.com/items?itemName=webfreak.debug
	- https://github.com/WebFreak001/code-debug
- neogdb.vim: Vim GDB front-end for neovim
	- https://github.com/huawenyu/neogdb.vim
- nvim-gdb: Neovim thin wrapper for GDB, LLDB, PDB/PDB++, and BashDB
	- https://github.com/sakhnik/nvim-gdb
- RealGUD: An extensible, modular GNU Emacs front-end for interacting with external debuggers
	- https://github.com/realgud/realgud

#### GDB: Projects: Memory Debugging

- pahole-gdb: pahole implementation for gdb - https://github.com/PhilArmstrong/pahole-gdb
- gdb-heap
	- https://github.com/rogerhu/gdb-heap
	- https://fedorahosted.org/gdb-heap/
	- https://fedoraproject.org/wiki/Features/MemoryDebuggingTools

#### GDB: Projects: Plotting

- GDBplotlib: Plotting and exporting of variables from GDB
	- https://github.com/X-Neon/gdbplotlib
- gdb-plot
	- a set of utils for: plotting from the gdb command line, saving c data to .mat files from gdb command line, exploring the stack frame
	- https://github.com/bthcode/gdb-plot

#### GDB: Projects: Profiling

- gdbpmp: A GDB Based Wallclock Profiler - https://github.com/markhpc/gdbpmp
- gdbprof: A wall clock time-based profiler built on GDB's Python interface
	- https://github.com/Muon/gdbprof
	- https://github.com/markhpc/gdbprof
- GDB profiler: Rich man's profiler, a profiler for native OCaml and other executables
	- https://github.com/copy/gdbprofiler

### GDB: Readings

- 8 gdb tricks you should know - https://blogs.oracle.com/ksplice/8-gdb-tricks-you-should-know
- Beej's Quick Guide to GDB - https://beej.us/guide/bggdb/
- Debugging binaries invoked from scripts with GDB
	- https://developers.redhat.com/articles/2022/12/27/debugging-binaries-invoked-scripts-gdb
- Extending gdbserver to support an strace client
	- https://developers.redhat.com/blog/2020/03/16/extending-gdbserver-to-support-an-strace-client/
- Fast Tracing with GDB - https://suchakra.wordpress.com/2016/06/29/fast-tracing-with-gdb/
- Faster debugging with watchpoints
	- https://interrupt.memfault.com/blog/cortex-m-watchpoints
- gdb Debugging Full Example (Tutorial): ncurses - http://www.brendangregg.com/blog/2016-08-09/gdb-example-ncurses.html
- GDB JIT Interface 101
	- https://weliveindetail.github.io/blog/post/2022/11/27/gdb-jit-interface-101.html
- GDB Tips and Tricks - Shane Kirk
	- 1: A Tale of Two Terminals - http://www.shanekirk.com/2017/08/gdb-tips-and-tricks-1-a-tale-of-two-terminals/
	- 2: Setting Breakpoints with Regular Expressions - http://www.shanekirk.com/2017/08/gdb-tips-and-tricks-2-setting-breakpoints-with-regular-expressions/
	- 3: Saving and Restoring Breakpoints Using Files - http://www.shanekirk.com/2017/09/gdb-tips-and-tricks-3-saving-and-restoring-breakpoints-using-files/
	- 4: Reverse Debugging - http://www.shanekirk.com/2017/10/gdb-tips-and-tricks-4-reverse-debugging/
	- 5: The Display Command - http://www.shanekirk.com/2017/12/gdb-tips-and-tricks-5-the-display-command/
	- 6: Examining Data Types - http://www.shanekirk.com/2018/02/gdb-tips-and-tricks-6-examining-data-types/
- GDB Tutorial - https://www.gdb-tutorial.net/
- GDB Wiki - https://sourceware.org/gdb/wiki/
- gdbWatchPoint: GDB tips & tricks
	- https://undo.io/resources/gdb-watchpoint/
	- https://www.youtube.com/playlist?list=PLrADU7tRzDD4xHv_zVoLKYg9mXYjXGhjG
- GDBWave - A Post-Simulation Waveform-Based RISC-V GDB Debugging Server
	- https://tomverbeure.github.io/2022/02/20/GDBWave-Post-Simulation-RISCV-SW-Debugging.html
	- GDBWave: GDB server to debug CPU simulation waveform traces
		- https://github.com/tomverbeure/gdbwave
- Hitchikers Guide To The GDB - http://apoorvaj.io/hitchhikers-guide-to-the-gdb.html
- How to debug stack frames and recursion in GDB
	- https://developers.redhat.com/articles/2022/06/07/how-debug-stack-frames-and-recursion-gdb
- How to point GDB to your sources - https://alex.dzyoba.com/blog/gdb-source-path/
- Howto: GDB Remote Serial Protocol
	- https://www.embecosm.com/appnotes/ean4/embecosm-howto-rsp-server-ean4-issue-2.html
- Introduction to Debuggers - Saumil Shah - http://www.slideshare.net/saumilshah/introduction-to-debuggers
- Julia Evans
	- Three steps to learning GDB - https://jvns.ca/blog/2014/02/10/three-steps-to-learning-gdb/
	- How does gdb work? - https://jvns.ca/blog/2016/08/10/how-does-gdb-work/
	- How does gdb call functions? - https://jvns.ca/blog/2018/01/04/how-does-gdb-call-functions/
- Notes on GDB - https://publicclu2.blogspot.com/2013/05/notes-on-gdb.html
- Printf-style debugging using GDB
	- 2021; Kevin Buettner
	- Part 1: dprintf
		- https://developers.redhat.com/articles/2021/10/05/printf-style-debugging-using-gdb-part-1
	- Part 2: save commands and output
		- https://developers.redhat.com/articles/2021/10/13/printf-style-debugging-using-gdb-part-2
	- Part 3: interact with C and C++ functions and automate GDB behavior
		- https://developers.redhat.com/articles/2021/12/09/printf-style-debugging-using-gdb-part-3
- Process Injection with GDB - https://magisterquis.github.io/2018/03/11/process-injection-with-gdb.html
- RevEngE is a dish served cold: Debug-Oriented Malware Decompilation and Reassembly
	- Reversing and Offensive-oriented Trends Symposium (ROOTS) 2019
	- Marcus Botacin, Lucas Galante, Paulo de Geus, André Grégio
	- https://lasca.ic.unicamp.br/paulo/papers/2019-ROOTS-marcus.botacin-lucas.galante-RevEngE.pdf
	- https://corvus.inf.ufpr.br/
	- RevEngE: Reverse Engineering Engine
		- Explore debugging extensions and malware decompilation capabilities based on dynamic GDB debugging sessions.
		- https://github.com/marcusbotacin/Reverse.Engineering.Engine
- The GDB developer’s GNU Debugger tutorial
	- Part 1: Getting started with the debugger
		- https://developers.redhat.com/blog/2021/04/30/the-gdb-developers-gnu-debugger-tutorial-part-1-getting-started-with-the-debugger/
	- Part 2: All about debuginfo 
		- https://developers.redhat.com/articles/2022/01/10/gdb-developers-gnu-debugger-tutorial-part-2-all-about-debuginfo
- Victor Stinner's Notes - GDB: GNU debugger - http://vstinner.readthedocs.io/gdb.html
- Why your errno value isn't printing in GDB—and what to do about it
	- https://developers.redhat.com/articles/2024/06/05/why-your-errno-value-isnt-printing-gdb-and-what-do-about-it

#### GDB: Readings: Pretty Printing

- Visualizing boost::unordered_map in GDB, with pretty-printer customization points
	- 2024-08-16; Braden Ganetsky
	- https://blog.ganets.ky/PrettyPrinter/
	- https://github.com/boostorg/unordered/blob/develop/extra/boost_unordered_printers.py

#### GDB: Readings: Python API

- GDB Custom Commands: Dynamic Arrays
	- https://portal.testfit.io/devblog/gdb_custom_commands_dynamic_arrays
- GDB Debugging Automation with Python: Implementing a memory leak detector
	- https://web.archive.org/https://nativecoding.wordpress.com/2016/07/31/gdb-debugging-automation-with-python/
- GDB Scripting and Indirect Functions
	- https://fasterthanli.me/blog/2020/gdb-scripting-and-indirect-functions/
- Jeff Trull
	- Displaying Stack Frames in gdb with Python - http://jefftrull.github.io/c++/gdb/python/2018/03/02/print-frame.html
	- Improving C++ backtraces with the gdb Python API - http://jefftrull.github.io/c++/gdb/python/2018/04/24/improved-backtrace.html
	- Skipping library code in gdb with help from libClang - http://jefftrull.github.io/c++/gdb/python/libclang/llvm/2018/04/30/stepping-with-libclang.html
- Object Inspection in GDB
	- https://hgad.net/posts/object-inspection-in-gdb/
- Python Interpreter in GNU Debugger
	- https://www.pythonsheets.com/appendix/python-gdb.html
- Skipping standard C++ library during debug session in gdb
	- https://xaizek.github.io/2016-05-26/skipping-standard-library-in-gdb/
- The GDB Python API
	- https://developers.redhat.com/blog/2017/11/10/gdb-python-api/

##### GDB: Readings: Python API: TUI

- Add custom windows to GDB: Programming the TUI in Python
	- https://developers.redhat.com/articles/2022/08/03/add-custom-windows-gdb-programming-tui-python
- Display dynamic content from GDB in a custom window
	- https://developers.redhat.com/articles/2022/06/06/display-dynamic-content-gdb-custom-window

#### GDB: Readings: Reverse Debugging

- Using GDB to time travel
	- https://developers.redhat.com/articles/2024/08/08/using-gdb-time-travel
- Advanced time manipulation with GDB
	- https://developers.redhat.com/articles/2025/06/04/advanced-time-manipulation-gdb

### GDB: Talks

- A flexible GDB (GNU Debugger) target description for processor diversity – SFO17-210
	- Linaro Connect San Francisco 2017; Yao Qi
	- http://connect.linaro.org/resource/sfo17/sfo17-210/
- Become a GDB Power User
	- ACCU 2016; Greg Law
	- https://www.youtube.com/watch?v=713ay4bZUrw
- Cool New Stuff in GDB 9, GDB 10, and GDB 11
	- CppCon 2021; Greg Law
	- https://www.youtube.com/watch?v=Ege7dKrGomU
- Debugging Embedded Devices using GDB
	- Embedded Linux Conference Europe 2020
	- Chris Simmonds
	- https://elinux.org/images/0/01/Debugging-with-gdb-csimmonds-elce-2020.pdf
	- https://www.youtube.com/watch?v=JGhAgd2a_Ck
- Debugging Embedded Devices Using GDB - A Review of Some Lessons Learned
	- Embedded Linux Conference North America 2020
	- Mike Anderson
	- https://elinux.org/Tools_and_Debugging_Presentations#Tutorial:_Debugging_Embedded_Devices_Using_GDB_-_A_Review_of_Some_Lessons_Learned_.5BELC_2020.5D
	- https://www.youtube.com/watch?v=FnfuxDVFcWE
- Debugging Linux C++
	- CppCon 2018; Greg Law
	- https://www.youtube.com/watch?v=V1t6faOKjuQ
- GDB: C++ conversion & dogfooding C++
	- GNU Tools Cauldron 2017; Pedro Alves
	- Slides: https://gcc.gnu.org/wiki/cauldron2017?action=AttachFile&do=view&target=gdb+-+C%2B%2B+conversion+%26+dogfood.pdf
	- Video: https://slideslive.com/38902352/gdb-c-conversion-dogfooding-c
- GDB - A Lot More Than You Knew
	- CppCon 2016 - Greg Law
	- https://www.youtube.com/watch?v=-n9Fkq1e6sg
- Getting the Most Out of GDB
	- C++ on Sea 2022
	- Mark Williamson & Greg Law
	- https://www.youtube.com/watch?v=to8KkFQn7jE
- Getting the most out of GDB: Cool stuff about GDB you didn't know
	- Meeting C++ 2022
	- Greg Law, Chris Croft-White
	- https://www.youtube.com/watch?v=IqH3Mh-OI-8
	- https://meetingcpp.com/mcpp/slides/2022/GDB_Pro_20229084.pdf
- Give me 15 minutes & I'll change your view of GDB
	- CppCon 2015 - Greg Law
	- https://www.youtube.com/watch?v=PorfLSr3DDI
- How custom GDB commands help in C++ development
	- Munich C++ User Group 2018 (Lightning Talk); Michael Krasnyk
	- https://www.youtube.com/watch?v=QtTYXE1wSVs
- Improving Debuggability with GDB's Python API
	- C++Now 2018 - Jeff Trull
	- https://www.youtube.com/watch?v=mLPp1x_1h3g
- Liberating the Debugging Experience with the GDB Python API
	- ACCU Bay Area Meetup 2018; Jeff Trull
	- https://github.com/accuBayArea/Slides/blob/master/slides/2018-08-08-jeff.pdf
	- CppCon 2018 - https://www.youtube.com/watch?v=ck_jCH_G7pA
	- gdb_python_api: Experiments with the GDB Python API
		- https://github.com/jefftrull/gdb_python_api
- More GDB wizardry and 8 other essential Linux application debugging tools
	- ACCU 2019; Greg Law
	- https://www.youtube.com/watch?v=Yq6g_kvyvPU
- Programmatic Debugging with GDB and Python
	- PyCon APAC/Taiwan 2015; Scott Tsai
	- https://www.youtube.com/watch?v=oAYbt2PsKng
	- https://docs.google.com/presentation/d/15qOKBh9FDjCeGS-xAHXZSJDS5_aoZk0Caz12FL_f294/
- ROCgdb, GDB, and AMDGPU debugging
	- FOSDEM 2024
	- Lancelot SIX
	- https://fosdem.org/2024/schedule/event/fosdem-2024-2392-rocgdb-gdb-and-amdgpu-debugging/
- SecurityTube GDB Expert (SGDE)
	- Walkthroughs: https://github.com/chaitanyakrishna/Securitytube-Gnu-Debugger-Expert
	- Course Videos: http://www.securitytube.net/tags/sgde
	- https://www.youtube.com/playlist?list=PLiP0FxVgYuUz0kdK7L7YaI5n4qkOuymue
- The GDB Text User Interface
	- FOSDEM 2020; Tom Tromey
	- https://fosdem.org/2020/schedule/event/debugging_gdb_tui/
- Understanding, Scripting, and Extending GDB 
	- 2017; Kevin Pouget, Jean-François Méhaut, Fabrice Rastell
	- https://mcgdb.0x972.info/team/
	- https://github.com/kpouget/tuto-gdb.py
	- Slides: https://mcgdb.0x972.info/files/tuto-gdb-py.presentation.pdf
- Your Application versus GDB
	- FOSDEM 2014 - Tom Tromey
	- https://archive.fosdem.org/2014/schedule/event/your_application_versus_gdb/
	- https://www.youtube.com/watch?v=RwDA3oIOtWw

## LLDB

- The LLDB Debugger - https://lldb.llvm.org/

### LLDB: Projects

- ds2: Debug server for lldb
	- ds2 is a debug server designed to be used with LLDB to perform remote debugging of Linux, Android, FreeBSD, Windows and Windows Phone targets. Windows/Windows Phone support is still under active development.
	- https://github.com/facebook/ds2
	- 2015 LLVM Developers’ Meeting: Stephane Sezer "ds2, a tiny debug server used with lldb"
	- https://www.youtube.com/watch?v=n00EhLskJWk&list=PL_R5A0lGi1AA4Lv2bBFSwhgDaHvvpVU21&index=27
- GALA: GDB API over LLDB API
	- An adapter package which enables GDB Python API in LLDB
	- https://github.com/sivachandra/gala
- GDBundle: Plugin Manager for GDB and LLDB
	- https://github.com/memfault/gdbundle
	- gdbundle - GDB and LLDB's Missing Plugin Manager
		- https://interrupt.memfault.com/blog/gdbundle-plugin-manager
- LLEF: LLDB Enhanced Features
	- https://github.com/foundryzero/llef
- LLDB Scripts: A collection of LLDB aliases/regexes and Python scripts to aid in your debugging sessions
	- https://github.com/DerekSelander/LLDB
	- https://www.raywenderlich.com/162020/custom-lldb-commands-practice
	- https://www.raywenderlich.com/161938/assembly-register-calling-convention-tutorial
- lldb-eval: blazing fast debug expression evaluation
	- https://github.com/google/lldb-eval/
	- Blazing fast expression evaluation for C++ in LLDB
		- https://werat.dev/blog/blazing-fast-expression-evaluation-for-c-in-lldb/
	- Building a faster expression evaluator for LLDB
		- LLVM Developers’ Meeting 2021
		- Andy Yankovsky
		- https://www.youtube.com/watch?v=9aThSRGjYdA
		- https://llvm.org/devmtg/2021-11/slides/2021-Buildingafaster-expression-evaluatorforLLDB.pdf
- lldbinit: Similar implementation of .gdbinit from fG! for lldb in python
	- https://github.com/deroko/lldbinit
- LLDBINIT: A gdbinit clone for LLDB
	- https://github.com/gdbinit/lldbinit
	- https://www.zerodayinitiative.com/blog/2020/4/20/mindshare-using-lldbinit-to-enhance-the-lldb-debugger
- Vegvisir: A browser based GUI for LLDB Debugger
	- https://github.com/ant4g0nist/vegvisir
- vplot: C++ container graph visualization for lldb
	- https://github.com/egladysh/vplot

#### LLDB: Projects: Editor Integration

- CodeLLDB: a LLDB front end for Visual Studio Code - https://github.com/vadimcn/vscode-lldb
- LLDB Neovim Frontend - https://github.com/dbgx/lldb.nvim
- LLDB Vim Frontend - https://github.com/gilligan/vim-lldb
- Native Debug
	- GDB & LLDB Debugger support for VSCode
	- https://marketplace.visualstudio.com/items?itemName=webfreak.debug
	- https://github.com/WebFreak001/code-debug
- nvim-gdb: Neovim thin wrapper for GDB, LLDB, PDB/PDB++, and BashDB
	- https://github.com/sakhnik/nvim-gdb

### LLDB: Readings

- LLDB Cheat Sheet
	- https://www.nesono.com/content/lldb-cheat-sheet
	- https://www.nesono.com/sites/default/files/lldb%20cheat%20sheet.pdf
- LLDB for GDB Users – Command Summary
	- https://developer.apple.com/library/content/documentation/General/Conceptual/lldb-guide/chapters/A3-GDB-Summary.html
- LLDB Scripts - Debugging the Swift Compiler
	- https://github.com/apple/swift/blob/main/docs/DebuggingTheCompiler.md#debugging-the-compiler-using-lldb-scripts
- LLDB to GDB Command Map - https://lldb.llvm.org/lldb-gdb.html
- Beyond Debug Information: Improving Program Reconstruction in LLDB using C++ Modules
	- 2019 Master’s Thesis; Raphael Isemann
	- https://hdl.handle.net/20.500.12380/300037
- Debugging SIMD in LLDB
	- 2024-03-30
	- Bartosz Taudul
	- https://wolf.nereid.pl/posts/simd-debugging/
- How to Extend LLDB to Provide a Better Debugging Experience
	- https://pspdfkit.com/blog/2018/how-to-extend-lldb-to-provide-a-better-debugging-experience/
- LLDB support for fork(2) and vfork(2)
	- https://www.moritz.systems/blog/lldb-support-for-fork-and-vfork/
- Tips for writing LLDB pretty printers
	- https://offlinemark.com/2022/10/13/tips-for-writing-lldb-pretty-printers/

### LLDB: Talks

- Better C++ debugging using Clang Modules in LLDB
	- 2019 LLVM Developers’ Meeting; Raphael Isemann
	- https://www.youtube.com/watch?v=vuNZLlHhy0k
	- http://llvm.org/devmtg/2019-10/talk-abstracts.html#tech13
- Bringing RenderScript to LLDB
	- 2016 EuroLLVM Developers' Meeting; Luke Drummond & Ewan Crawford, Codeplay
	- https://www.youtube.com/watch?v=BBC61L0QKCM
	- http://www.llvm.org/devmtg/2016-03/Presentations/EuroLLVM2016-E.Crawford_and_L.Drummond-Bringing_RenderScript_to_LLDB.pdf
- Debugging Tips and Tricks
	- WWDC 2016; Kate Stone, Enrico Granata, Sean Callanan, Jim Ingham
	- https://developer.apple.com/videos/play/wwdc2016/417
- Debugging with LLDB
	- WWDC 2012; Greg Clayton
	- https://developer.apple.com/videos/play/wwdc2012/415/
- Debugging with LLVM: A quick introduction to LLDB and LLVM sanitizers
	- FOSDEM 2020; Andrzej Warzynski; Graham Hunter
	- https://fosdem.org/2020/schedule/event/debugging_with_llvm/
- ds2: a tiny debug server used with lldb
	- 2015 LLVM Developers’ Meeting; Stephane Sezer, Facebook
	- https://www.youtube.com/watch?v=n00EhLskJWk
	- https://github.com/facebook/ds2
- LLDB - a new C++ debugger
	- DevConf.CZ 2019; Jan Kratochvíl
	- https://www.youtube.com/watch?v=2BjKNaiB3yM
	- https://devconfcz2019.sched.com/event/Jcht
- LLDB Reproducers
	- 2019 EuroLLVM Developers’ Meeting; Jonas Devlieghere
	- https://www.youtube.com/watch?v=ygdzXnfyvbg
	- http://llvm.org/devmtg/2019-04/talks.html#Talk_12
- LLDB Tutorial: Adding debugger support for your target
	- 2016 EuroLLVM Developers' Meeting; Deepak Panickal & Andrzej Warzynski, Codeplay
	- https://github.com/codeplaysoftware/lldb-msp430
	- http://www.llvm.org/devmtg/2016-03/Tutorials/LLDB-tutorial.pdf
	- https://www.youtube.com/watch?v=9hhDZeV0fYU
- LLDB: Beyond "po"
	- WWDC 2019; Davide Italiano, Jonas Devlieghere
	- https://developer.apple.com/videos/play/wwdc2019/429/
	- https://www.raywenderlich.com/3868932-wwdc-2019-top-10-videos#toc-anchor-011
- Migrating from GDB to LLDB
	- WWDC 2011; Jim Ingham
	- https://developer.apple.com/videos/play/wwdc2011/321/
- Support for mini-debuginfo in LLDB
	- How to read the .gnu_debugdata section.
	- FOSDEM 2020; Konrad Kleine
	- https://fosdem.org/2020/schedule/event/debugging_mini/
- Why should I use LLDB?
	- 2015 EuroLLVM Developers’ Meeting; Deepak Panickal and Ewan Crawford
	- https://www.youtube.com/watch?v=JtpQZw9NpIU
	- https://llvm.org/devmtg/2015-04/slides/Why_should_I_use_LLDB.pdf

## RR

- RR: Record and Replay Framework
	- http://rr-project.org/
	- https://github.com/mozilla/rr

### RR: Projects

- Control Flow Visualizer (CFViz): an rr / gdb plugin
	- https://botondballo.wordpress.com/2017/12/22/control-flow-visualizer-cfviz-an-rr-gdb-plugin/
	- https://bitbucket.org/botond/cfviz
- rr-dataflow: An 'origin' command that continues to the origin of a piece of data in rr
	- https://github.com/jrmuizel/rr-dataflow
	- Using rr-dataflow: Why and How? - https://www.mgaudet.ca/technical/2018/10/18/using-rr-dataflow-why-and-how

### RR: Readings

- Engineering Record And Replay For Deployability
	- USENIX ATC 2017
	- Robert O'Callahan, Chris Jones, Nathan Froyd, Kyle Huey, Albert Noll, Nimrod Partush
	- https://arxiv.org/abs/1705.05937
	- https://www.usenix.org/conference/atc17/technical-sessions/presentation/ocallahan
- Lightweight User-Space Record And Replay
	- 2016
	- Robert O'Callahan, Chris Jones, Nathan Froyd, Kyle Huey, Albert Noll, Nimrod Partush
	- https://robert.ocallahan.org/2016/10/rr-paper-lightweight-user-space-record.html
	- https://arxiv.org/abs/1610.02144
- Improved debugging with rr
	- https://techtalk.intersec.com/2018/03/improved-debugging-with-rr/
- Instant replay: Debugging C and C++ programs with rr
	- https://developers.redhat.com/blog/2021/05/03/instant-replay-debugging-c-and-c-programs-with-rr/
- Timeless Debugging of Complex Software: Root Cause Analysis of a Non-Deterministic JavaScriptCore Bug
	- http://blog.ret2.io/2018/06/19/pwn2own-2018-root-cause-analysis/

## OS-specific

### iOS

- Chisel: a collection of LLDB commands to assist debugging iOS apps
	- https://github.com/facebook/chisel
- KTRW: An iOS kernel debugger based on a KTRR bypass for A11 iPhones that works with LLDB
	- https://github.com/googleprojectzero/ktrw
	- KTRW: The journey to build a debuggable iPhone
		- https://googleprojectzero.blogspot.com/2019/10/ktrw-journey-to-build-debuggable-iphone.html

### Linux

- AFLTriage: A tool to triage crashing input files with a debugger (GDB, Linux)
	- https://github.com/quic/AFLTriage
- Crash Utility: Linux kernel crash utility
	- https://github.com/crash-utility/crash
	- https://crash-utility.github.io/
- crash-python: a semantic debugger for the Linux kernel
	- https://github.com/jeffmahoney/crash-python
- debuginfod
	- elfutils debuginfod is a client/server in elfutils 0.178+ that automatically distributes elf/dwarf/source-code from servers to clients such as debuggers across HTTP
		- https://sourceware.org/elfutils/Debuginfod.html
	- Deploying debuginfod servers for your developers
		- https://developers.redhat.com/blog/2019/12/17/deploying-debuginfod-servers-for-your-developers/
	- The elfutils debuginfod server
		- FOSDEM 2020; Mark Wielaard, Frank Ch. Eigler
		- https://fosdem.org/2020/schedule/event/debugging_debuginfod/
	- Introducing debuginfod, the elfutils debuginfo server
		- https://developers.redhat.com/blog/2019/10/14/introducing-debuginfod-the-elfutils-debuginfo-server/
	- elfutils debuginfo-server
		- GNU Tools Cauldron 2019; Frank Ch. Eigler, Aaron Merey
		- https://www.youtube.com/watch?v=cyOXWT_EBJ0
		- https://gcc.gnu.org/wiki/cauldron2019talks?action=AttachFile&do=view&target=dbgserver.pdf
- drgn: Scriptable debugger library
	- https://github.com/osandov/drgn/
	- https://drgn.readthedocs.io/
	- A kernel debugger in Python: drgn
		- 2019-05-29; Jake Edge
		- https://lwn.net/Articles/789641/
	- Introducing CTF Support in Drgn for Oracle Linux
		- 2024-10-03; Stephen Brennan
		- https://blogs.oracle.com/linux/post/introducing-ctf-support-in-drgn-for-oracle-linux
- edb: a cross platform x86/x86-64 debugger
	- https://github.com/eteran/edb-debugger
- Hermit: A reproducible container
	- Hermit launches Linux x86_64 programs in a special, hermetically isolated sandbox to control their execution. Hermit translates normal, nondeterministic behavior, into deterministic, repeatable behavior. This can be used for various applications, including replay-debugging, reproducible artifacts, chaos mode concurrency testing and bug analysis.
	- https://github.com/facebookexperimental/hermit
	- Hermit: Deterministic Linux for Controlled Testing and Software Bug-finding
		- https://developers.facebook.com/blog/post/2022/11/22/hermit-deterministic-linux-testing/
- ich: Linux crash harness with runtime process instrumentation
	- https://github.com/zznop/ich
- kdress: Transform vmlinuz into a fully debuggable vmlinux that can be used with /proc/kcore
	- https://github.com/elfmaster/kdress
- libkdumpfile: Kernel coredump file access
	- https://github.com/ptesarik/libkdumpfile
- libthread_db
	- Notes about an odd, esoteric, yet incredibly useful library: libthread_db
		- https://web.archive.org/http://timetobleed.com/notes-about-an-odd-esoteric-yet-incredibly-useful-library-libthread_db/
- LIKE-DBG (LInux-KErnel-DeBuGger): Fully dockerized Linux kernel debugging environment
	- https://github.com/0xricksanchez/like-dbg
- makedumpfile: Make Linux crash dump small by filtering and compressing pages
	- https://github.com/makedumpfile/makedumpfile
- nnd: A debugger for Linux
	- https://github.com/al13n321/nnd
- ORC (Oops Rewind Capability) Unwinder
	- [Commit ee9f8fce9964](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=ee9f8fce99640811b2b8e79d0d1dbe8bab69ba67)
	- [Commit 39358a033b2e](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=39358a033b2e4432052265c1fa0f36f572d8cfb5)
	- ORC unwinder - https://github.com/torvalds/linux/blob/master/Documentation/x86/orc-unwinder.rst
	- The Linux x86 ORC Stack Unwinder - http://www.codeblueprint.co.uk/2017/07/31/the-orc-unwinder.html
	- The ORCs are coming - https://lwn.net/Articles/728339/
	- x86: ORC unwinder (previously undwarf) - https://lwn.net/Articles/727553/
	- Unwinding a Stack by Hand with Frame Pointers and ORC
		- 2022
		- Stephen Brennan
		- https://blogs.oracle.com/linux/post/unwinding-stack-frame-pointers-and-orc
- PageBuster: dump all executable pages of packed processes
	- https://github.com/revng/pagebuster
	- PageBuster: stealthily dump all the code ever executed
		- https://rev.ng/blog/pagebuster/post.html
- plutonium-dbg: A kernel-based debugger for Linux applications
	- https://github.com/plutonium-dbg/plutonium-dbg
	- Kernel-Assisted Debugging of Linux Applications
		- Reversing and Offensive-oriented Trends Symposium (ROOTS) 2018
		- Tobias Holl, Philipp Klocke, Fabian Franzen, and Julian Kirsch
		- https://vimeo.com/307238462
		- https://dl.acm.org/citation.cfm?id=3289596
- Reverie: An ergonomic and safe syscall interception framework for Linux
	- Reverie is a user space system-call interception framework for Linux. It can be used to intercept, modify, or elide a syscall before the kernel executes it. In essence, Reverie sits at the boundary between user space and kernel space.
	- https://github.com/facebookexperimental/reverie
- Scout - Instruction based research debugger
	- an extendable basic debugger designed for use in those cases that there is no built-in debugger / gdb-stub in the debugee process / firmware
	- https://github.com/CheckPointSW/Scout
	- https://scout-debugger.readthedocs.io/
- sdb: The Slick/Simple Debugger
	- A postmortem and live debugger
	- https://github.com/delphix/sdb
	- Debugging ZFS: From Illumos to Linux
		- OpenZFS Developer Summit 2019; Serapheim Dimitropoulos
		- https://drive.google.com/file/d/1oho9X5bkW-I-yJ-pVD8VqkaloxhGepzT/view
- symbol-scrapers: A bunch of scripts to scrape symbols from Linux distributions
	- https://github.com/gabrielesvelto/symbol-scrapers/
- vmlinux-to-elf: A tool to recover a fully analyzable ELF from a raw kernel, through extracting the kernel symbol table (kallsyms)
	- https://github.com/marin-m/vmlinux-to-elf

#### Linux: Readings

- Live Debugging Techniques for the Linux Kernel
	- Part 1: setting up an Oracle Linux virtual machine
		- https://blogs.oracle.com/linux/post/live-kernel-debugging-1
	- Part 2: basic techniques utilizing gdb & QEMU's gdbserver, gdb Python
		- https://blogs.oracle.com/linux/post/live-kernel-debugging-2
	- Part 3: advanced techniques: kdb and kgdboc, crash
		- https://blogs.oracle.com/linux/post/live-kernel-debugging-3
- The Definitive Guide to Linux Process Injection
	- 2024; Ori David
	- https://www.akamai.com/blog/security-research/the-definitive-guide-to-linux-process-injection
	- Linux Process Injection: proof-of-concept implementations of various Linux process injection primitives
	- https://github.com/akamai/Linux-Process-Injection
- Under Linux, libSegFault and addr2line are underrated
	- https://lemire.me/blog/2023/05/01/under-linux-libsegfault-and-addr2line-are-underrated/
- What's Inside a Linux Kernel Core Dump
  - 2024-02-08; Stephen Brennan
  - https://blogs.oracle.com/linux/post/whats-inside-a-linux-kernel-core-dump
  - vmcoreinfo: tools related to vmcoreinfo: findvmcoreinfo.py, editvmcoreinfo.c, get_vmcoreinfo.c, vmcoreinfosize.py
    - https://github.com/brenns10/kernel_stuff/tree/master/vmcoreinfo

#### Linux: Talks

- Linux Debuginfo Formats - DWARF, ELF, dwo, dwp - What are They All?
	- CppCon 2022
	- Greg Law
	- https://www.youtube.com/watch?v=l3h7F9za_pc
- Linux Kernel Debugging: Going Beyond Printk Messages
	- Embedded Linux Conference Europe (ELCE) 2019; Sergio Prado
	- https://www.youtube.com/watch?v=NDXYpR_m1CU
	- https://elinux.org/images/1/14/Linuxkerneldebugging.pdf
	- https://e-labworks.com/talks/elce2019

### macOS

- LLDBagility
	- https://github.com/quarkslab/LLDBagility/
	- a tool for debugging macOS virtual machines with the aid of the Fast Debugging Protocol (FDP)
	- https://blog.quarkslab.com/an-overview-of-macos-kernel-debugging.html
	- https://blog.quarkslab.com/lldbagility-practical-macos-kernel-debugging.html
- Mac OS X Debugging Magic - https://developer.apple.com/library/content/technotes/tn2124/_index.html

### Windows

- BugChecker: SoftICE-like kernel debugger for Windows
	- Windows XP to 11, x86 and x64
	- https://github.com/vitoplantamura/BugChecker
- DbgShell: A PowerShell front-end for the Windows debugger engine
	- https://github.com/Microsoft/DbgShell/
- DuBStep (Dynamic Breakpoint API): A Library for creating hardware execution and data breakpoints at runtime on Win32/Win64
	- https://github.com/justinboswell/dubstep
- HyperDbg: an open-source, user mode and kernel mode Windows debugger with a focus on using hardware technologies
	- https://hyperdbg.com
	- https://github.com/HyperDbg/HyperDbg
- IceBox: Virtual Machine Introspection, Tracing & Debugging
	- https://github.com/thalium/icebox
- kdmp-parser: Windows kernel dump C++ parser
	- https://github.com/0vercl0k/kdmp-parser
- makin - reveal anti-debug tricks (Windows)
	- https://github.com/secrary/makin
- Nanomite - Windows Debugger for x64 and x86
	- https://github.com/zer0fl4g/Nanomite/
- OllyDbg
	- http://www.ollydbg.de/
- ScyllaHide: Advanced usermode anti-anti-debugger
	- https://github.com/x64dbg/ScyllaHide
- TitanHide: Hiding kernel-driver for x86/x64
	- a driver intended to hide debuggers from certain processes
	- https://github.com/mrexodia/TitanHide
- udmp-parser: A Cross-Platform C++ parser library for Windows user minidumps
	- https://github.com/0vercl0k/udmp-parser
- WubbabooMark: Debugger Anti-Detection Benchmark
	- https://github.com/hfiref0x/WubbabooMark
- x64dbg
	- https://x64dbg.com/
	- https://github.com/x64dbg/x64dbg

#### Windows: Readings

- An RPC Debugging Framework with Visual Studio
	- http://donw.io/post/rpc-debugging-vs/
- Anti-Debug Tricks
	- This encyclopedia contains the description of anti-debug tricks which work on the latest Windows releases with the most popular debuggers (such as OllyDbg, WinDbg, x64dbg).
	- https://anti-debug.checkpoint.com/
	- https://github.com/CheckPointSW/Anti-Debug-DB
- Creating a Public Symbol Server, Easily
	- https://randomascii.wordpress.com/2020/03/14/creating-a-public-symbol-server-easily/
- Debug Recipes (.NET and Windows problems) - https://github.com/lowleveldesign/debug-recipes
- Debugging in Visual Studio - https://docs.microsoft.com/en-us/visualstudio/debugger/debugger-feature-tour
- Debugging Tools for Windows (WinDbg, KD, CDB, NTSD)
	- https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/
- Hardware breakpoints and exceptions on Windows
	- https://ling.re/hardware-breakpoints/
- Showing Variables Using the Windows Debugging API
	- Overload 29(165) October 2021
	- Roger Orr
	- https://accu.org/journals/overload/29/165/orr/
	- https://github.com/rogerorr/articles/tree/main/Debugging_Optimised_Code
- Windows Debugging Tools - Debugging Resources
	- https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/debugging-resources

#### Visual Studio Debugger

- https://docs.microsoft.com/en-us/visualstudio/debugger/
- https://devblogs.microsoft.com/visualstudio/tag/debug/
- A Debugging Tip: Write Custom Visualizers in Visual Studio
	- https://www.cppstories.com/2021/natvis-dbg-tip/
	- https://github.com/fenbf/articles/tree/master/DebuggingTipsSamples

#### WinDbg

- Introduction to WinDbg and debugging Windows - series by Anand George
	- https://www.youtube.com/playlist?list=PLhx7-txsG6t6n_E2LgDGqgvJtCHPL7UFu
- Modern Debugging with WinDbg Preview
	- DEFCON 27 (2019) Workshop Materials
	- https://github.com/hugsy/defcon_27_windbg_workshop/
	- WinDbg cheatsheet
		- https://github.com/hugsy/defcon_27_windbg_workshop/blob/master/windbg_cheatsheet.md
- Time Travel Debugging - James McNellis
	- Meeting C++ 2018 - https://www.youtube.com/watch?v=MyVQnP-U_ho
	- Pacific++ 2018 - https://www.youtube.com/watch?v=BVslyei0804
- WinDbg Basics for Malware Analysis
	- https://www.youtube.com/watch?v=QuFJpH3My7A
- WinDbg: time to put the @ back in the bag
	- vOPCDE #6 2020; Yarden Shafir
	- https://www.youtube.com/watch?v=eONddXQjy2k

##### WinDbg: Readings

- Collection of WinDbg resources - https://blogs.msdn.microsoft.com/reiley/2012/07/28/collection-of-windbg-resources/
- Break On Process Creation in WinDbg
	- https://shakreiner.com/posts/break-on-process-windbg/
- Debugger Data Model, Javascript & X64 Exception Handling - https://doar-e.github.io/blog/2017/12/01/debugger-data-model/
- Debugger Lies: Stack Corruption
	- https://www.timdbg.com/posts/debugger-lies-part-1/
- Debugging Tools for Windows - https://blogs.msdn.microsoft.com/windbg/
- Exploiting flaws in WinDbg: how to escape or fool debuggers from existing flaws
	- Journal of Computer Virology and Hacking Techniques (2020)
	- François Plumerault, Baptiste David
	- http://dx.doi.org/10.1007/s11416-020-00347-x
- JavaScript bridge makes malware analysis with WinDbg easier
	- https://blog.talosintelligence.com/2019/02/windbg-malware-analysis-with-javascript.html
- Stupid debugger tricks: Calling functions and methods - https://blogs.msdn.microsoft.com/oldnewthing/20070427-00/?p=27083
- Time travel debugging: It’s a blast! (from the past)
	- https://msrc.microsoft.com/blog/2019/05/time-travel-debugging-its-a-blast-from-the-past/
- Tips & Tricks for better debugging with WinDbg
	- REcon 2024
	- Chris Alladoum
	- https://cfp.recon.cx/recon2024/talk/GK8YDV/
	- https://github.com/hugsy/recon_2024_windbg_workshop
- Tutorial: Using WinDbg to call arbitrary functions — WinDBG kung-fu series
	- http://cfc.kizzx2.com/index.php/tutorial-using-windbg-to-call-arbitrary-functions-windbg-kung-fu-series/
- Undocumented WinDbg - https://blogs.msdn.microsoft.com/reiley/2011/10/30/undocumented-windbg/
- Use Windows Debuggers for Non-Debugging Tasks - https://blogs.msdn.microsoft.com/reiley/2011/10/23/use-windows-debuggers-for-non-debugging-tasks/
- Using Function Evaluation in WinDbg - https://blogs.msdn.microsoft.com/reiley/2012/08/18/using-function-evaluation-in-windbg/
- What's the Debugger Data Model? (And Why?)
	- 2022; Tim Misiak
	- https://www.timdbg.com/posts/whats-the-data-model/
- What's the Target Model? (And Why?)
	- 2022; Tim Misiak
	- https://www.timdbg.com/posts/whats-the-target-model/
- WinDbg automation and extensions - https://web.archive.org/https://nativecoding.wordpress.com/2016/01/10/automate-attach-to-process-on-windows-with-windbg/
- WinDbg Malware Analysis Cheat Sheet
	- https://web.archive.org/https://oalabs.openanalysis.net/2019/02/18/windbg-for-malware-analysis/
- WinDbg — the Fun Way
	- Part 1: the basics of the new debugger data model — Using the new objects, having custom registers, searching and filtering output, declaring anonymous types and parsing lists and arrays
		- https://medium.com/@yardenshafir2/windbg-the-fun-way-part-1-2e4978791f9b
	- Part 2: how to use legacy commands with dx, the new disassembler, create synthetic methods and types, the changes to breakpoints and use the filesystem from within the debugger
		- https://medium.com/@yardenshafir2/windbg-the-fun-way-part-2-7a904cba5435
- WinDbg, Debugger Objects, and JavaScript! Oh, My! - https://www.osr.com/blog/2017/05/18/windbg-debugger-objects-javascript-oh/
- Yet Another Hello World - https://blogs.msdn.microsoft.com/reiley/2011/09/29/yet-another-hello-world/

##### WinDbg: Projects

- 0CCh WinDbg extension - https://github.com/0cch/0cchext
- DbgModelCppLib: A header-only C++ library for producing and consuming data from the debugger data model
	- https://github.com/Microsoft/WinDbg-Libraries/tree/master/DbgModelCppLib
	- https://github.com/Microsoft/WinDbg-Samples/tree/master/DataModelHelloWorld/Cpp
- TWindbg: PEDA-like debugger UI for WinDbg - https://github.com/bruce30262/TWindbg
- WDBGARK: WinDbg Anti-RootKit extension - https://github.com/swwwolf/wdbgark
- Winbagility: a tool to connect WinDbg on non /DEBUG Windows x64 systems
	- http://winbagility.github.io
	- https://github.com/Winbagility/Winbagility
- WinDbg-Samples: Sample extensions, scripts, and API uses for WinDbg
	- https://github.com/Microsoft/WinDbg-Samples
- WinDbgCookbook: small, useful scripts, extensions, and debugger data model "dx" queries
	- https://github.com/TimMisiak/WinDbgCookbook
- WinDBGtree: A command tree based on commands and extensions for Windows Kernel Debugging
	- https://github.com/vagnerpilar/windbgtree

##### WinDbg: Talks

- A first look into how WinDbg works
	- 2022; Tim Misiak
	- https://www.youtube.com/watch?v=QStC084UrgY

##### WinDbg: Time Travel Debugging

- Time Travel Debugging FAQ - https://blogs.msdn.microsoft.com/windbg/2017/10/20/time-travel-debugging-faq/
- Time Travel Debugging - Overview - https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/time-travel-debugging-overview
- Time Travel Debugging - Sample App Walkthrough - https://aka.ms/ttdtutorial
- Time Travel Debugging: Root Causing Bugs in Commercial Scale Software
	- CppCon 2017
	- James McNellis, Jordi Mola, Ken Sykes
	- https://www.youtube.com/watch?v=l1YJTg_A914
- Time Travel Debugging - Advanced
	- Defrag Tools #186 (2017)
	- Andrew Richards, JCAB (Juan Carlos Arevalo Baeza), Jordi Mola
	- https://learn.microsoft.com/en-us/shows/defrag-tools/186-time-travel-debugging-advanced
- TTD-Bindings: Bindings for Microsoft WinDbg Time Travel Debugging (TTD)
	- https://github.com/commial/ttd-bindings

## Crash Analysis & Reporting

- Breakpad: a set of client and server components which implement a crash-reporting system
	- https://github.com/google/breakpad
- CASR: Crash Analysis and Severity Report
	- Collect crash reports, triage, and estimate severity
	- https://github.com/ispras/casr
	- "CASR is a set of tools that allows you to collect crash reports in different ways. Use casr-core binary to deal with coredumps. Use casr-san to analyze ASAN reports or casr-ubsan to analyze UBSAN reports. Try casr-gdb to get reports from gdb."
	- "Crash report contains many useful information: severity (like exploitable), OS and package versions, command line, stack trace, register values, disassembly, and even source code fragment where crash appeared. Reports are stored in JSON format. casr-cli is meant to provide TUI for viewing reports. Reports triage (deduplication, clustering) is done by casr-cluster. Triage is based on stack trace comparison from gdb-command. casr-afl is used to triage crashes found by AFL++."
	- Casr-Cluster: Crash Clustering for Linux Applications
		- ISPRAS 2021
		- Georgy Savidov, Andrey Fedotov
		- https://www.doi.org/10.1109/ISPRAS53967.2021.00012
	- Sydr-Fuzz: Continuous Hybrid Fuzzing and Dynamic Analysis for Security Development Lifecycle
		- ISPRAS 2022
		- Alexey Vishnyakov, Daniil Kuts, Vlada Logunova, Darya Parygina, Eli Kobrin, Georgy Savidov, Andrey Fedotov
		- https://arxiv.org/abs/2211.11595
- Core Explorer: A DWARF parser and core dump analyzer that runs in your browser
	- A static analyzer for dynamic memory. Analyze core dumps to find ODR violations, memory leaks, and use-after-free hazards. List all objects, types, allocations, and threads and visualize the relationships between them.
	- https://github.com/core-explorer/core-explorer/
- Crashpad: a crash-reporting system
	- https://github.com/chromium/crashpad
	- Backtrace fork of Crashpad
		- A fork of Crashpad with file attachment support and other improvements.
		- https://github.com/backtrace-labs/crashpad
- dump_syms: Rewrite of breakpad dump_syms tools in Rust
	- a command-line utility for parsing the debugging information the compiler provides (whether as DWARF or STABS sections in an ELF file or as stand-alone PDB files) and writing that information back out in the Breakpad symbol file format.
	- https://github.com/mozilla/dump_syms
- llvm-crash-analyzer: A Tool for the Program Analysis of Corefiles
	- designed to observe/triage the root cause of the crash
	- as an outcome it will point to a blame function, machine instruction, and line of source code of the problematic piece of the program
	- https://github.com/cisco-open/llvm-crash-analyzer
	- 2022 LLVM Performance Workshop at CGO
		- Djordje Todorovic, Bharathi Seshadri, Ananthakrishna Sowda, Nikola Tesic, Ivan Baev
		- https://www.youtube.com/watch?v=Y4TkdYZfarA
		- https://llvm.org/devmtg/2022-04-03/slides/llvm-crash-analyzer.pdf
- rust-minidump: Type definitions, parsing, and analysis for the minidump file format
	- "fairly heavily modeled after Google Breakpad for historical reasons, but there is no fundamental interoperability requirement between the two beyond the fact that they fundamentally handle the same inputs."
	- https://github.com/rust-minidump/rust-minidump
	- Everything Is Broken: Shipping rust-minidump at Mozilla
		- https://hacks.mozilla.org/2022/06/everything-is-broken-shipping-rust-minidump-at-mozilla/
	- Fuzzing rust-minidump for Embarrassment and Crashes – Part 2
		- https://hacks.mozilla.org/2022/06/fuzzing-rust-minidump-for-embarrassment-and-crashes/

# Stack Trace & Unwinding

## Stack Trace & Unwinding: Readings

- Fast Call-Stack Backtrace
	- 2025-10-20; Branimir Karadžić
	- https://bkaradzic.github.io/posts/fast-call-stack-backtrace/
- Limitations of frame pointer unwinding
	- Serhei Makarov
	- https://developers.redhat.com/articles/2024/10/30/limitations-frame-pointer-unwinding
- Programmatic access to the call stack in C++
	- https://eli.thegreenplace.net/2015/programmatic-access-to-the-call-stack-in-c/
- <stacktrace>
	- Draft C++ Standard: Stacktrace
		- https://eel.is/c++draft/stacktrace
		- https://timsong-cpp.github.io/cppwp/stacktrace
	- Standard library header <stacktrace> (C++23)
		- https://en.cppreference.com/w/cpp/header/stacktrace
	- P0881: A Proposal to Add a Stacktrace Library
		- https://wg21.link/P0881
	- C++23: The stacktrace library
		- https://www.sandordargo.com/blog/2022/09/21/cpp23-stacktrace-library
- Stack unwinding
	- MaskRay (Fangrui Song)
	- https://maskray.me/blog/2020-11-08-stack-unwinding
- Unwind specification draft for GNU/Linux/ia64 (extends the exception ABI)
	- https://www.kernel.org/pub/linux/devel/gcc/unwind/
- Unwinding the stack the hard way
	- 2023; Kévin Lesénéchal
	- Tutorial on how to make a stack trace or backtrace manually unwinding the stack using ELF’s .eh_frame and call frame information (CFI)
	- https://lesenechal.fr/en/linux/unwinding-the-stack-the-hard-way

## Stack Trace & Unwinding: Software

- BacktraceResolver: Very fast backtraces resolver
	- https://github.com/markpapadakis/BacktraceResolver
- Backward-cpp: a beautiful stack trace pretty printer for C++
	- https://github.com/bombela/backward-cpp
- Boost.Stacktrace
	- https://github.com/boostorg/stacktrace
	- http://www.boost.org/doc/libs/release/doc/html/stacktrace.html
- cpptrace: Lightweight, zero-configuration-required, and cross-platform stacktrace library for C++
	- supports C++11 and greater on Linux, macOS, and Windows including MinGW and Cygwin environments
	- https://github.com/jeremy-rifkin/cpptrace
- libgcc_s (GNU) - https://gcc.gnu.org/onlinedocs/gccint/Libgcc.html
	- Data Definitions for libgcc_s - https://refspecs.linuxfoundation.org/LSB_5.0.0/LSB-Core-generic/LSB-Core-generic/libgcc-s-ddefs.html
	- Interfaces for libgcc_s - https://refspecs.linuxfoundation.org/LSB_5.0.0/LSB-Core-generic/LSB-Core-generic/libgcc-s.html
	- Interfaces Definitions for libgcc_s - https://refspecs.linuxfoundation.org/LSB_5.0.0/LSB-Core-generic/LSB-Core-generic/libgcc-sman.html
- libunwind (nongnu.org) - http://www.nongnu.org/libunwind/
- pstack: Print stack traces of running processes. Uses its own ELF and DWARF parsing
	- https://github.com/peadar/pstack
- quickstack: a tool to take call stack traces with minimal overheads
	- https://github.com/yoshinorim/quickstack

## Stack Trace & Unwinding: Talks

- Advanced Usage of the C++23 Stacktrace Library
	- ACCU 2024
	- James Pascoe
	- https://www.youtube.com/watch?v=rynny8wP3M4
	- https://github.com/jamespascoe/accu2024-example-code
	- https://github.com/jamespascoe/accu2024-stacktrace/tree/gh-pages
- C++ Exceptions and Stack Unwinding
	- CppCon 2017: Dave Watson
	- https://www.youtube.com/watch?v=_Ivd3qzgT7U
- Profiling framepointer-less code with elfutils stacktrace
	- GNU Tools Cauldron 2024
	- Serhei Makarov
	- https://www.youtube.com/watch?v=IjHWbo_ZF-E
	- http://serhei.io/files/cauldron2024-slides.pdf
	- https://gcc.gnu.org/wiki/cauldron2024#cauldron2024talks.profiling_framepointerless_code_with_elfutils_stacktrace

---

# Talks

## 2023

- Back to Basics: Debugging in Cpp
	- CppCon 2023
	- Greg Law
	- https://www.youtube.com/watch?v=qgszy9GquRs
	- https://github.com/CppCon/CppCon2023/blob/main/Presentations/B2B_Debugging_CppCon_2023.pdf
- Debugging C++ Code： A Practical and Interactive Guide
	- Sebastian Theophil
	- https://www.think-cell.com/assets/en/career/talks/pdf/think-cell_talk_debugging.pdf
	- CppNow 2023
		- https://www.youtube.com/watch?v=jB09yTXtFUo
		- https://github.com/boostcon/cppnow_presentations_2023/blob/main/cppnow_slides/Nobody_Can_Program_Correctly.pdf
	- Core C++ 2023
		- https://www.youtube.com/watch?v=ogV0olQJax4

## 2021

- Debugging Techniques
	- Bob Steagall
	- MUC++ 2021
		- https://www.youtube.com/watch?v=LBs3RqyKI5c
		- https://github.com/BobSteagall/MeetupTalks/blob/main/2021-10-07_debugging_techniques__bob_steagall__muc%2B%2B.pdf
	- CppCon 2021
		- https://www.youtube.com/watch?v=02WsP5gTJCg
		- https://github.com/BobSteagall/CppCon2021/tree/main/DebuggingTechniques
		- https://cppcon.digital-medium.co.uk/wp-content/uploads/2021/11/back_to_basics_classic_stl__bob_steagall__cppcon_2021.pdf
- Modern Linux C++ Debugging Tools: Under the Covers
	- ACCU 2021; Greg Law & Dewang Li
	- https://www.youtube.com/watch?v=qYbGDDIsH4M

## 2019

- Modern Linux C++ Debugging Tools: Under the Covers
	- CppCon 2019; Greg Law & Dewang Li
	- https://www.youtube.com/watch?v=WoRmXjVxuFQ
	- https://github.com/CppCon/CppCon2019/tree/master/Presentations/modern_linux_cpp_debugging_tools__under_the_covers

## 2018

- GNU Tools Cauldron 2018
	- gOlogy: impact of -O* on -g
		- Alexandre Oliva
		- https://www.fsfla.org/~lxoliva/writeups/gOlogy/slides.pdf
		- https://www.fsfla.org/~lxoliva/writeups/gOlogy/gOlogy.txt
	- A collection of debug info improvements for the GNU Compiler Collection
		- Alexandre Oliva, Mark J. Wielaard
		- https://gnu.wildebeest.org/~mark/cauldron-2018/DebuginfoImprovements.pdf
- Let's Write a Debugger!
	- linux.conf.au 2018 - Levente Kurusa
	- https://www.slideshare.net/LeventeKurusa/lets-write-a-debugger
	- https://opensource.com/article/18/1/how-debuggers-really-work
	- https://www.youtube.com/watch?v=qS51kIHWARM
	- https://github.com/levex/debugger-talk

## 2017

- Debugging the debugger - BSDCan 2017, Samy Bahra
	- https://www.youtube.com/watch?v=wyF-hGGPJMs
	- Compiler debug quality suite - https://github.com/backtrace-labs/cdqs
	- http://www.bsdcan.org/2017/schedule/events/787.en.html
- Debugging Under Fire: Keep your Head when Systems have Lost their Mind • GOTO 2017 • Bryan Cantrill
	- https://www.youtube.com/watch?v=30jNsCVLpAE
- How C++ Debuggers work - Simon Brand
	- C++ Edinburgh 2018
		- https://www.youtube.com/watch?v=UiW24hzLy1M
	- Meeting C++ 2017
		- https://meetingcpp.com/2017/talks/items/How_Cpp_Debuggers_Work.html
		- https://www.youtube.com/watch?v=Q3Rm95Mk03c

## 2016

- Building a Debugging Mindset - QConSF 2016 - Devon H. O'Dell
	- video: https://www.infoq.com/presentations/debugging-mindset
	- slides: https://speakerdeck.com/dho/building-a-debugging-mindset
	- transcript: https://9vx.org/post/building-a-debugging-mindset/
- How do Debuggers (Really) Work - Pawel Moll
	- Linux Piter 2016
		- https://www.youtube.com/watch?v=xqrxg3hl10o
		- https://ostconf.com/system/attachments/files/000/001/198/original/Pawel_Moll.pdf
	- ELC 2015
		- https://vimeo.com/220644951
		- https://events.static.linuxfound.org/sites/events/files/slides/slides_16.pdf
- Post-mortem Debugging: could you be the one? - Surge 2016 - Abel Mathew
	- https://www.youtube.com/watch?v=WHhorNLa934
- Timeless Debugging - USENIX Enigma 2016 - George Hotz
	- https://www.youtube.com/watch?v=eGl6kpSajag

## 2015

- Debugging using an exact recording of a program's execution - C++Now 2015 - Julian Smith
	- Undo's Live Recorder
	- https://www.youtube.com/watch?v=NWWMogzgLS4

## 2014

- The VS Debugger: How It Works + Tips and Tricks - GoingNative 28 - Gabriel Ha, Gregg Miskelly, Steve Carroll
	- https://learn.microsoft.com/en-us/shows/c9-goingnative/goingnative-28-vs-debugger-how-it-works-tips-tricks

## 2011

- Forensic Debugging: How to Autopsy, Repair, and Reanimate a Release-built Game
	- GDC 2011; Elan Ruskin
	- https://www.gdcvault.com/play/1014351/Forensic-Debugging-How-to-Autopsy
