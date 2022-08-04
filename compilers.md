# [C++ links](README.md): compilers

See also:

- [Assembly (Arm)](assembly.arm.md), [Assembly (RISC-V)](assembly.riscv.md), [Assembly (x86)](assembly.x86.md)
- [Compilers Correctness](compilers.correctness.md)
- [Debugging](https://github.com/MattPD/cpplinks/blob/master/debugging.md): [Implementation](https://github.com/MattPD/cpplinks/blob/master/debugging.md#implementation)
- [Program Analysis](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef) - [LLVM](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef#llvm)
- [Linking and Loading](https://github.com/MattPD/cpplinks/blob/master/executables.linking_loading.md) 

# Background

- https://github.com/aalhour/awesome-compilers
- A Compiler Writing Journey
	- https://github.com/DoctorWkt/acwj
- An Incremental Approach to Compiler Construction
	- Scheme and Functional Programming 2006; Abdulaziz Ghuloum
	- http://scheme2006.cs.uchicago.edu/11-ghuloum.pdf
	- Step-by-step development of a Scheme-to-x86 compiler
		- https://github.com/namin/inc
- ChocoPy: A Programming Language for Compilers Courses
	- SPLASH-E 2019; Rohan Padhye, Koushik Sen, Paul N. Hilfinger
	- https://chocopy.org/
	- https://chocopy.org/chocopy-splashe19.pdf
	- https://chocopy.org/chocopy-splashe19-slides.pdf
- Computer Language Notes: Compilers and Interpreters
	- https://github.com/melling/ComputerLanguages/blob/master/compilers.md
- FreeCompilerCamp.org: Online Training for Extending Compilers
	- http://freecompilercamp.org/
	- https://github.com/freeCompilerCamp
	- Clang/LLVM Tutorials
		- http://freecompilercamp.org/clang-llvm-landing
		- Alok Mishra, Anjia Wang, Chunhua Liao, Yonghong Yan, Barbara Chapman
		- https://sc19.supercomputing.org/proceedings/tech_poster/tech_poster_pages/rpost138.html
		- FreeCompilerCamp.org: Training for OpenMP Compiler Development from Cloud
			- https://sc19.supercomputing.org/proceedings/workshops/workshop_pages/ws_bphpcte103.html
- Let’s Build A Simple Interpreter - https://ruslanspivak.com/lsbasi-part1/
- Notes on Graph Algorithms Used in Optimizing Compilers - Carl Offner
	- http://www.cs.umb.edu/~offner/files/flow_graph.pdf
- Resources for Amateur Compiler Writers
	- http://c9x.me/compile/bib/

## Books

- Crafting Interpreters
	- Bob Nystrom
	- http://craftinginterpreters.com/
	- https://github.com/munificent/craftinginterpreters
- Essentials of Compilation: An Incremental Approach
	- A book about compiling Racket to x86-64 assembly
	- Jeremy G. Siek, Ryan R. Newton
	- https://github.com/IUCompilerCourse/Essentials-of-Compilation
- GCC Wiki - List of compiler books
	- https://gcc.gnu.org/wiki/ListOfCompilerBooks
- Introduction to Compilers and Language Design
	- Douglas Thain
	- http://compilerbook.org/
- Jordan Rose (Swift team) recommendations
	- http://belkadan.com/blog/2015/11/Recommendations/
- Instruction Selection
	- Instruction Selection: Principles, Methods, & Applications
		- 2016 Book; Gabriel Hjort Blindell
		- http://kth.diva-portal.org/smash/record.jsf?pid=diva2:951540
	- Universal Instruction Selection
		- 2018 PhD Dissertation; Gabriel Hjort Blindell
		- http://www.diva-portal.org/smash/record.jsf?pid=diva2:1185339
		- https://github.com/gablin/ghb-thesis
		- https://github.com/gablin/ghb-thesis/blob/master/ghb-thesis.pdf
- Static Single Assignment (SSA) Book
	- draft:
		- http://web.archive.org/http://ssabook.gforge.inria.fr/latest/book-full.pdf
		- GitHub Mirror
			- https://github.com/pfalcon/ssabook
			- PDF: https://pfalcon.github.io/ssabook/latest/
	- SSA-based Compiler Design
		- 2022; Fabrice Rastello, Florent Bouchez Tichadou
		- https://link.springer.com/book/9783030805142

## LLVM

- A Tourist’s Guide to the LLVM Source Code - http://blog.regehr.org/archives/1453
- Life of an instruction in LLVM - http://eli.thegreenplace.net/2012/11/24/life-of-an-instruction-in-llvm
	- Life of an instruction in Clang / LLVM - https://github.com/thegameg/llvm-life/
- LLVM - Chris Lattner, The Architecture of Open Source Applications - http://www.aosabook.org/en/llvm.html
- LLVM Tutorial: Kaleidoscope - http://llvm.org/docs/tutorial/
	- Haskell version: http://www.stephendiehl.com/llvm/
- LLVM for Grad Students - http://adriansampson.net/blog/llvm.html
- Testing LLVM - http://blog.regehr.org/archives/1450
- Tutorial: Creating an LLVM Backend for the Cpu0 Architecture - https://jonathan2251.github.io/lbd/
- Tutorial: Creating an LLVM Toolchain for the Cpu0 Architecture - http://jonathan2251.github.io/lbt/

# Conferences

Compilers Call For Papers for Conferences, Workshops and Journals at WikiCFP - http://www.wikicfp.com/cfp/call?conference=compilers

- ASPLOS: International Conference on Architectural Support for Programming Languages and Operating Systems - https://asplos-conference.org/ - http://dblp.uni-trier.de/db/conf/asplos/
- CASES: Compilers, Architecture, and Synthesis for Embedded Systems - http://www.esweek.org/cases - http://dblp.uni-trier.de/db/conf/cases/
- CC: The International Conference on Compiler Construction - http://conf.researchr.org/series/CC - http://dblp.uni-trier.de/db/conf/cc/
- CGO: International Symposium on Code Generation and Optimization - http://cgo.org/ - http://dblp.uni-trier.de/db/conf/cgo/
- HPCA: International Symposium on High-Performance Computer Architecture - https://www.hpca-conf.org/ - http://dblp.uni-trier.de/db/conf/hpca/
- ICFP: International Conference on Functional Programming - http://icfpconference.org/ - http://dblp.uni-trier.de/db/conf/icfp/
- ISMM: International Symposium on Memory Management - http://www.sigplan.org/Conferences/ISMM/ - http://dblp.uni-trier.de/db/conf/iwmm/
- LCTES: Languages, Compilers, and Tools for Embedded Systems - https://conf.researchr.org/series/LCTES - http://dblp.uni-trier.de/db/conf/lctrts/
- OOPSLA: Object-Oriented Programming Systems, Languages and Applications - http://www.sigplan.org/Conferences/OOPSLA/ - http://www.oopsla.org/ - http://dblp.uni-trier.de/db/conf/oopsla/
- PACT: International Conference on Parallel Architecture and Compilation - http://pactconf.org/ - http://dblp.uni-trier.de/db/conf/IEEEpact/
- PLDI: Programming Language Design and Implementation - http://www.sigplan.org/Conferences/PLDI/ - http://dblp.uni-trier.de/db/conf/pldi/
- POPL: Principles of Programming Languages - http://www.sigplan.org/Conferences/POPL/ - http://dblp.uni-trier.de/db/conf/popl/
- PPoPP: ACM SIGPLAN Symposium on Principles and Practice of Parallel Programming - http://www.sigplan.org/Conferences/PPOPP/ - http://dblp.uni-trier.de/db/conf/ppopp/
- SAS: International Static Analysis Symposium - http://www.staticanalysis.org/ - http://dblp.uni-trier.de/db/conf/sas/
- SCOPES: International Workshop on Software and Compilers for Embedded Systems - https://scopesconf.org/ - http://dblp.uni-trier.de/db/conf/scopes/

# Courses

- Cornell CS 6120: Advanced Compilers
	- Fall 2020; Adrian Sampson
		- The Self-Guided Online Course: https://www.cs.cornell.edu/courses/cs6120/2020fa/self-guided/
		- https://www.cs.cornell.edu/courses/cs6120/2020fa/
		- source code: https://github.com/sampsyo/cs6120
		- lectures: https://www.cs.cornell.edu/courses/cs6120/2020fa/lesson/
			- https://vod.video.cornell.edu/channel/CS%2B6120/179754792
			- https://cornell.app.box.com/s/wb3387ebfbte9btx3weekmc8nij5glep
- IIT Delhi COL874: Advanced Compiler Techniques
	- 2020-2021; Sorav Bansal
	- https://iitd.github.io/col874/
	- Lectures: https://www.youtube.com/playlist?list=PLf3ZkSCyj1tf3rPAkOKY5hUzDrDoekAc7
	- Meetings: https://www.youtube.com/playlist?list=PLf3ZkSCyj1tfCb_3bPAaWKtrcFHS0xRdn 
- IU P423/P523: Compilers (Programming Language Implementation)
	- Fall 2020; Jeremy Siek 
	- https://iucompilercourse.github.io/IU-P423-P523-E313-E513-Fall-2020/
	- https://github.com/IUCompilerCourse/IU-P423-P523-E313-E513-Fall-2020
	- https://github.com/IUCompilerCourse/Essentials-of-Compilation
- KAIST CS420: Compiler Design
	- Spring 2020; Jeehoon Kang
		- https://github.com/kaist-cp/cs420
		- https://www.youtube.com/playlist?list=PL5aMzERQ_OZ8RWqn-XiZLXm1IJuaQbXp0
	- KECC: KAIST Educational C Compiler
		- https://github.com/kaist-cp/kecc-public
- NPTEL: Compiler Design
	- 2011; Y.N. Srikant
		- https://nptel.ac.in/courses/106108052/
		- https://www.youtube.com/playlist?list=PL3690D679B876DE6A
- SFU CMPT 886: Program Analysis and Reliability - Nick Sumner, Spring 2015
	- Playlist: https://www.youtube.com/playlist?list=PLNC6lmsIySCOPjY8IwKBtD2cqe-MMgIGM
	- Schedule & Slides: http://www.cs.sfu.ca/~wsumner/teaching/886/15/schedule.html
- Stanford OpenEdX: Compilers - Alex Aiken
	- http://online.stanford.edu/course/compilers-0
- UCB CS294-113: Virtual Machines and Managed Runtimes
	- http://www.wolczko.com/CS294/
	- A Concise and Opinionated History of Virtual Machines
		- [Virtual Machines Summer School 2016](https://soft-dev.org/events/vmss16/)
		- https://archive.org/download/vmss16/wolczko.pdf
		- https://www.youtube.com/watch?v=QnQYhrpX39M
- UCSD CSE 131: Compiler Construction
	- Fall 2019; Joseph Gibbs Politz
		- https://ucsd-cse131-f19.github.io/
		- https://podcast.ucsd.edu/watch/fa19/cse131_a00
	- Winter 2018; Ranjit Jhala
		- https://ucsd-progsys.github.io/131-web/
		- https://podcast.ucsd.edu/watch/wi18/cse131_a00
- UCSD CSE 231: Advanced Compiler Design
	- Winter 2019; Sorin Lerner
		- https://podcast.ucsd.edu/watch/wi19/cse231_a00
		- https://ucsd-pl.github.io/cse231/wi19/
- UFMG DCC888: Static Program Analysis
	- 2020; Fernando Magno Quintão Pereira
	- https://homepages.dcc.ufmg.br/~fernando/classes/dcc888/
	- https://www.youtube.com/playlist?list=PLC-dUCVQghfdu7AG5f_p4oRyKgjDuoAWU
- University of Utah: Advanced Compilers - John Regehr
	- Weeks 1 and 2: http://blog.regehr.org/archives/1419
	- Weeks 3-5: http://blog.regehr.org/archives/1428
- UW CSE CSEP 501: Compilers - Hal Perkins
	- https://courses.cs.washington.edu/courses/csep501/
	- Winter 2018
		- Homepage: https://courses.cs.washington.edu/courses/csep501/18sp/
		- Lecture Videos: https://courses.cs.washington.edu/courses/csep501/18sp/video/
	- Winter 2016
		- Homepage: https://courses.cs.washington.edu/courses/csep501/16wi/
		- Playlist: https://www.youtube.com/playlist?list=PLTPQEx-31JXhfAWGnGzwbfhB2zUB7Jd4C
		- Topics: https://courses.cs.washington.edu/courses/csep501/16wi/calendar/lecturelist.html

# Cross-compilation

- GCC and Clang compiler drivers and cross compilation - http://maskray.me/blog/2021-03-28-compiler-driver-and-cross-compilation
- How to cross compile with LLVM based tools
	- FOSDEM 2018; Peter Smith
	- https://archive.fosdem.org/2018/schedule/event/crosscompile/

# Implementations

- List of Online C++ Compilers - https://arnemertz.github.io/online-compilers/
- LLVM
	- http://llvm.org/
	- LLVM Developers' Meeting - http://llvm.org/devmtg/
	- http://blog.llvm.org/
	- http://llvmweekly.org/
	- Clang: a C language family frontend for LLVM
		- http://clang.llvm.org/
- GCC (GNU Compiler Collection)
	- https://gcc.gnu.org/
	- GNU Tools Cauldron - https://gcc.gnu.org/wiki#Events
	- https://twitter.com/gnutools/
- Visual C++ - https://www.visualstudio.com/vs/cplusplus/
	- https://devblogs.microsoft.com/cppblog/

## Detection

- Pre-defined Compiler Macros
	- https://github.com/cpredef/predef
	- https://sourceforge.net/p/predef/wiki/
	- Architectures - https://sourceforge.net/p/predef/wiki/Architectures/
	- Compilers - https://sourceforge.net/p/predef/wiki/Compilers/
	- Endianness - https://sourceforge.net/p/predef/wiki/Endianness/
	- Language Standards - https://sourceforge.net/p/predef/wiki/Standards/
	- Operating Systems - https://sourceforge.net/p/predef/wiki/OperatingSystems/
	- Standard Libraries - https://sourceforge.net/p/predef/wiki/Libraries/
- SPY: Friendly Neighborhood C++17 Constexpr Predef Wrapper
	- OS, compiler, libc, stdlib detection
	- https://github.com/jfalcou/spy

## Documentation

- Clang documentation - http://clang.llvm.org/docs/
- GCC online documentation - https://gcc.gnu.org/onlinedocs/
	- GCC Wiki - https://gcc.gnu.org/wiki
	- Cynbe's GCC Debugging Hints - http://muq.org/~cynbe/gcc/
		- Debugging Resources - http://muq.org/~cynbe/gcc/offsite-resources.html
		- Comments on the Internals Manual - http://muq.org/~cynbe/gcc/gccint.html
- LLVM documentation - http://llvm.org/docs/
- Visual C++ documentation
	- https://docs.microsoft.com/en-us/cpp/
	- https://github.com/Microsoft/cpp-docs
	- https://docs.microsoft.com/en-us/cpp/visual-cpp-in-visual-studio
- Security-related flags and options for C compilers
	- https://airbus-seclab.github.io/c-compiler-security/

## Sanitizers

- https://github.com/google/sanitizers
	- https://github.com/google/sanitizers/wiki

# Linking and Loading

See:

- [Executables](executables.md) - executable & object file formats ([DLL](https://github.com/MattPD/cpplinks/blob/master/executables.md#dll), [ELF](https://github.com/MattPD/cpplinks/blob/master/executables.md#elf), [Mach-O](https://github.com/MattPD/cpplinks/blob/master/executables.md#mach-o), [PE](https://github.com/MattPD/cpplinks/blob/master/executables.md#pe)); debugging data formats ([DWARF](https://github.com/MattPD/cpplinks/blob/master/executables.md#dwarf), [PDB](https://github.com/MattPD/cpplinks/blob/master/executables.md#pdb-program-database))
	- [Linking and Loading](https://github.com/MattPD/cpplinks/blob/master/executables.linking_loading.md) 

# Optimization

- ALIVe: Automatic LLVM InstCombine Verifier
	- http://rise4fun.com/Alive
	- https://github.com/nunoplopes/alive
	- http://blog.regehr.org/archives/1170
	- https://www.cs.utah.edu/~regehr/papers/pldi15.pdf
	- http://llvm.org/devmtg/2014-10/Slides/Menendez-Alive.pdf
- Automatic Feedback Directed Optimizer (AutoFDO)
	- https://gcc.gnu.org/wiki/AutoFDO
	- https://github.com/google/autofdo
- Compiler Optimizations for Reverse Engineers by Rolf Rolles
	- http://www.msreverseengineering.com/blog/2014/6/23/compiler-optimizations-for-reverse-engineers
	- http://www.msreverseengineering.com/s/Binary-Literacy-Static-6-Optimizations.ppt
- Compiler Optimization Options
	- GCC: https://gcc.gnu.org/onlinedocs/gcc/Optimize-Options.html
	- Clang: http://clang.llvm.org/docs/CommandGuide/clang.html#cmdoption-O0 - https://stackoverflow.com/questions/15548023/clang-optimization-levels
	- Visual C++: https://msdn.microsoft.com/en-us/library/19z1t1wy.aspx
- Devirtualization in C++ - https://hubicka.blogspot.com/search/label/devirtualization
- GoingNative 50: New Visual C++ Code Optimizer - https://channel9.msdn.com/Shows/C9-GoingNative/GoingNative-50-New-Visual-C-Code-Optimizer
- Link time optimization (LTO) - https://hubicka.blogspot.com/search/label/link-time%20optimization
- Optimizations in C++ Compilers: A practical journey
	- ACM Queue vol. 17, no. 5 (2019)
	- Matt Godbolt
	- https://queue.acm.org/detail.cfm?id=3372264

## Superoptimization

- GNU Superoptimizer Version 2 - https://github.com/embecosm/gso2
- Souper - a superoptimizer for LLVM IR - https://github.com/google/souper
- Stochastic Superoptimization - http://blog.regehr.org/archives/923
- STOKE: A stochastic superoptimizer and program synthesizer - http://stoke.stanford.edu - https://github.com/StanfordPL/stoke
- Superoptimizing Compilers - http://superoptimization.org/wiki/Superoptimizing_Compilers
- Superoptimization - James Pallister - FOSDEM 2015 - https://archive.fosdem.org/2015/schedule/event/superoptimization/

# Talks

## 2019

- An overview of Clang
	- 2019 LLVM Developers’ Meeting; Sven van Haastregt, Anastasia Stulova
	- https://www.youtube.com/watch?v=5kkMpJpIGYU
	- http://llvm.org/devmtg/2019-10/talk-abstracts.html#tut8
- GCC under the hood
	- Linaro Connect San Diego 2019; Siddhesh Poyarekar
	- https://www.youtube.com/watch?v=brxAm99w8D8
	- https://siddhesh.in/gcc-under-the-hood.pdf
	- https://siddhesh.in/posts/gcc-under-the-hood.html
	- https://linaroconnectsandiego.sched.com/event/SubD/san19-221-gcc-under-the-hood
- Introduction to LLVM
	- 2019 LLVM Developers’ Meeting; Eric Christopher & Johannes Doerfert
	- https://www.youtube.com/watch?v=J5xExRGaIIY

## 2018

- Introduction to LLVM: Building simple program analysis tools and instrumentation
	- FOSDEM 2018; Mike Shah
	- https://fosdem.org/2018/schedule/event/introduction/
	- https://www.youtube.com/watch?v=VKIv_Bkp4pk
	- slides & code: http://www.mshah.io/fosdem18.html

## 2017

- Getting started with LLVM: the TL;DR version
	- LinaroOrg Connect San Francisco 2017; Diana Picus
	- https://connect.linaro.org/resource/sfo17/sfo17-110/
- LLVM Internals #2
	- Linaro Connect Budapest 2017; Renato Golin, Peter Smith, Diana Picus, Omair Javaid, Adhemerval Zanella
	- http://connect.linaro.org/resource/bud17/bud17-302/

## 2016

- Introduction to LLVM – Projects, Components, Integration, Internals
	- Linaro Connect Las Vegas 2016; Renato Golin
	- http://connect.linaro.org/resource/las16/las16-501/
- Anders Hejlsberg on Modern Compiler Construction
	- Channel 9; May 12, 2016
	- https://channel9.msdn.com/Blogs/Seth-Juarez/Anders-Hejlsberg-on-Modern-Compiler-Construction
- STOKE: Search-Based Compiler Optimization
	- UCI CS Distinguished Lecture; April 29, 2016; Alex Aiken
	- https://www.youtube.com/watch?v=rZFeTTFp7x4

## 2015

- Understanding Compiler Optimization
	- Meeting C++ 2015; Chandler Carruth
	- https://www.youtube.com/watch?v=FnGCDLhaxKU
- Stochastic Optimization for x86 Binaries
	- Google Tech Talks; January 12, 2015; Eric Schkufza
	- https://www.youtube.com/watch?v=aD9mZDJzb58

## 2014

- Superoptimizing LLVM
	- UW CSE Colloquium; December 2, 2014; John Regehr
	- https://www.youtube.com/watch?v=Ux0YnVEaI6A
- Compiler Technologies
	- Northwest C++ Users' Group; October 15, 2014; Jim Hogg
	- http://nwcpp.org/october-2014.html

## 2013

- Compiler Confidential
	- GoingNative 2013; Eric Brumer
	- https://channel9.msdn.com/Events/GoingNative/2013/Compiler-Confidential

# Warnings

- C/C++/Objective-C compiler warning flags collection and parsers
	- https://github.com/Barro/compiler-warnings#ccobjective-c-compiler-warning-flags-collection-and-parsers
- Compiler Warnings - Ian Lance Taylor - https://www.airs.com/blog/archives/159
- leathers - Warning suppression library (C++) - https://github.com/ruslo/leathers
	- Warnings list: https://github.com/ruslo/leathers/wiki/List
- ListCppWarningOptions: A simple Perl script that prints GCC warning options you can apply to C++ code
	- https://github.com/nkakuev/list-cpp-warning-options
- Use The Tools Available - Compilers
	- https://github.com/lefticus/cppbestpractices/blob/master/02-Use_the_Tools_Available.md#compilers
- Useful GCC warning options not enabled by -Wall -Wextra
	- https://kristerw.blogspot.com/2017/09/useful-gcc-warning-options-not-enabled.html
- Warning Flags - http://www.iso-9899.info/wiki/WarningFlags
- Warning Options - https://gcc.gnu.org/onlinedocs/gcc/Warning-Options.html
