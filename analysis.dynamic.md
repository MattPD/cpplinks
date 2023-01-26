# [C++ links](README.md): Program Analysis - Dynamic

See also:

- [Compilers](https://github.com/MattPD/cpplinks/blob/master/compilers.md)
- [Debugging](https://github.com/MattPD/cpplinks/blob/master/debugging.md)
- [Program Analysis](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef)
	- [Static Program Analysis](analysis.static.md) - static analysis (static checkers and compilers) and verification
	- [Symbolic Execution](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef#symbolic-execution)
	- [LLVM](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef#llvm)
		- [LLVM - Verification](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef#llvm---verification)
- [Testing](https://github.com/MattPD/cpplinks/blob/master/testing.md)
	- [Fuzzing](https://github.com/MattPD/cpplinks/blob/master/testing.fuzzing.md)

# Contents

- [Dynamic Binary Instrumentation (DBI)](#dynamic-binary-instrumentation-dbi)
	- [Readings](https://github.com/MattPD/cpplinks/blob/master/analysis.dynamic.md#dynamic-binary-instrumentation-dbi-readings)
	- [Software](https://github.com/MattPD/cpplinks/blob/master/analysis.dynamic.md#dynamic-binary-instrumentation-dbi-software)
- [Dynamic Binary Translation (DBT)](#dynamic-binary-translation-dbt)
- [Software](#software):
	- [Frida](#software-frida)
	- [Pin](#software-pin)
		- [Readings](https://github.com/MattPD/cpplinks/blob/master/analysis.dynamic.md#software-pin-readings)
		- [Projects](https://github.com/MattPD/cpplinks/blob/master/analysis.dynamic.md#software-pin-projects)
	- [Sanitizers](#software-sanitizers)
		- [Readings](https://github.com/MattPD/cpplinks/blob/master/analysis.dynamic.md#software-sanitizers-readings)
			- [Research](https://github.com/MattPD/cpplinks/blob/master/analysis.dynamic.md#software-sanitizers-readings-research)
		- [Projects](https://github.com/MattPD/cpplinks/blob/master/analysis.dynamic.md#software-sanitizers-projects)
		- [Talks](https://github.com/MattPD/cpplinks/blob/master/analysis.dynamic.md#software-sanitizers-talks)
	- [Valgrind](#software-valgrind)

---

# Dynamic Binary Instrumentation (DBI)

## Dynamic Binary Instrumentation (DBI): Readings

- Cross-ISA Machine Instrumentation using Fast and Scalable Dynamic Binary Translation
	- Virtual Execution Environments (VEE) 2019
	- Emilio G. Cota, Luca P. Carloni
	- http://www.cs.columbia.edu/~cota/pubs/cota_vee19.pdf
	- https://www.sld.cs.columbia.edu/qemu-vee.html
- Dynamic Binary Instrumentation Primer
	- http://deniable.org/posts/binary-instrumentation/
	- https://github.com/fdiskyou/DBI
- Optimization of Naïve Dynamic Binary Instrumentation Tools
	- 2011 Ph.D. Dissertation; Reid Kleckner
	- https://dspace.mit.edu/handle/1721.1/76984
- Security Evaluation of Dynamic Binary Instrumentation Engines
	- DBI Engine Detection Tool and all PoC code
		- https://github.com/zhechkoz/PwIN
	- 2018 Master Thesis; Zhechko Zhechev
		- https://web.archive.org/https://kirschju.re/static/ma_zhechev_2018.pdf
	- REcon Montreal 2018
		- https://web.archive.org/https://kirschju.re/static/recon_2018_kirsch_zhechev_pwin.pdf
		- https://infocondb.org/con/recon/recon-2018/pwning-intel-pin-reconsidering-intel-pin-in-context-of-security
		- https://recon.cx/2018/montreal/schedule/events/145.html
	- Pwning Intel piN – Why DBI is unsuitable for security applications
		- ESORICS 2018
		- Julian Kirsch, Zhechko Zhechev, Bruno Bierbaumer, Thomas Kittel
		- https://link.springer.com/chapter/10.1007/978-3-319-99073-6_18
- SoK: Using Dynamic Binary Instrumentation for Security (And How You May Get Caught Red Handed)
	- Asia Conference on Computer and Communications Security (AsiaCCS) 2019
	- Daniele Cono D’Elia, Emilio Coppa, Simone Nicchi, Federico Palmaro, Lorenzo Cavallaro
	- https://doi.org/10.1145/3321705.3329819
	- https://www.diag.uniroma1.it/~delia/papers/asiaccs2019.pdf
	- https://github.com/season-lab/sok-dbi-security/
- Unravelling Code Injection in Binaries
	- 2016; Suchakra Sharma
	- https://suchakra.wordpress.com/2016/07/03/unravelling-code-injection-in-binaries/
- Using Binary Instrumentation for Vulnerability Discovery (or even mitigation!)
	- EuskalHack 2018; Joxean Koret
	- https://github.com/joxeankoret/membugtool/blob/master/docs/Using%20Binary%20Instrumentation%20for%20Vulnerability%20Discovery%20(or%20even%20mitigation!).pdf
	- https://docs.google.com/presentation/d/e/2PACX-1vQYw4HJ3kzdmjnxklyBK2nyoMV3Iftx5G6IQmaas7z1cJdP04sX9WsWZmZKqtcTOsqbYukDdUyovhXb/pub
- Valgrind Research Papers
	- http://valgrind.org/docs/pubs.html

## Dynamic Binary Instrumentation (DBI): Software

- Avatar²: an open source framework for dynamic instrumentation and analysis of binary firmware
	- https://github.com/avatartwo/avatar2
	- Avatar²: Towards an open source binary firmware analysis framework
		- 34C3 (2017)
		- https://media.ccc.de/v/34c3-9195-avatar
		- https://www.youtube.com/watch?v=cRxmxapS8N4
		- https://events.ccc.de/congress/2017/Fahrplan/events/9195.html
	- Avatar²: A Multi-target Orchestration Platform
		- http://s3.eurecom.fr/docs/bar18_muench.pdf
	- Dynamic Binary Firmware Analysis: Challenges & Solutions
		- 2019 PhD Dissertation; Marius Muench
		- https://www.eurecom.fr/publication/5969
- DynamoRIO: Dynamic Instrumentation Tool Platform
	- https://dynamorio.org/
	- https://github.com/DynamoRIO/dynamorio
- dynamorio_pin_escape
	- Escaping DynamoRIO and Pin - or why it's a worse-than-you-think idea to run untrusted code or to input untrusted data
	- Cosmin Gorgovan (2014)
	- https://github.com/lgeek/dynamorio_pin_escape
- Dyninst: Tools for binary instrumentation, analysis, and modification.
	- http://www.dyninst.org/
	- https://github.com/dyninst/dyninst
	- dumpcfgs: Dump (extract) CFGs statically from binary programs using DynInst API
		-https://github.com/rimsa/dumpcfgs
	- Parallelizing Binary Code Analysis
		- Xiaozhu Meng, Jonathon M. Anderson, John Mellor-Crummey, Mark W. Krentel, Barton P. Miller, Srđan Milaković
		- 2020 arXiv
		- https://arxiv.org/abs/2001.10621
- Instrew: Leveraging LLVM for High Performance Dynamic Binary Instrumentation
	- https://github.com/aengelke/instrew
	- VEE 2020
		- Alexis Engelke, Martin Schulz
		- https://conf.researchr.org/details/vee-2020/vee-2020-papers/5/Instrew-Leveraging-LLVM-for-High-Performance-Dynamic-Binary-Instrumentation
- QBDI (QuarkslaB Dynamic binary Instrumentation): A Dynamic Binary Instrumentation framework based on LLVM
	- https://qbdi.quarkslab.com
	- https://github.com/quarkslab/QBDI
	- Implementing an LLVM based Dynamic Binary Instrumentation framework
		- 34C3 (2017)
		- https://events.ccc.de/congress/2017/Fahrplan/events/9006.html
	- Example: plugging Triton on top of QBDI - http://shell-storm.org/repo/Notepad/qbdi_with_triton.txt
	- A Preliminary Test of QBDI - https://web.archive.org/web/20181019164425/https://www.johnfxgalea.com/2018/01/13/a-preliminary-test-of-qbdi/
	- Example: SRAC - a Simple Return Address Checker - https://github.com/johnfxgalea/SRAC
- TinyInst: A lightweight dynamic instrumentation library
	- https://github.com/googleprojectzero/TinyInst
- Tracer: Set of Dynamic Binary Instrumentation and visualization tools for execution traces.
	- https://github.com/SideChannelMarvels/Tracer
	- https://insinuator.net/2016/03/how-to-crack-a-white-box-without-much-effort/
	- TracerPIN: TracerPin is a Intel PIN tool for generating execution traces of a running process.
	- TracerGrind: TracerGrind is a Valgrind tool for generating execution traces of a running process.
	- TraceGraph: TraceGraph is a GUI for visualizing execution traces produced by TracerGrind and TracerPin.
- Triton: a Dynamic Binary Analysis (DBA) framework
	- Provides internal components like a Dynamic Symbolic Execution (DSE) engine, a dynamic taint engine, AST representations of the x86, x86-64, ARM32 and AArch64 Instructions Set Architecture (ISA), SMT simplification passes, an SMT solver interface and, the last but not least, Python bindings.
	- https://github.com/JonathanSalwan/Triton
	- Triton v0.8 and ARMv7: A Guideline for Adding New Architectures
		- https://blog.quarkslab.com/triton-v08-and-armv7-a-guideline-for-adding-new-architectures.html

---

# Dynamic Binary Translation (DBT)

- A Retargetable System-Level DBT Hypervisor
	- Tom Spink, Harry Wagstaff, Björn Franke
	- 2019 USENIX Annual Technical Conference
		- https://www.usenix.org/conference/atc19/presentation/spink
	- ACM Transactions on Computer Systems 36(4) 2020
		- https://doi.org/10.1145/3386161
		- https://www.research.ed.ac.uk/portal/en/publications/a-retargetable-systemlevel-dbt-hypervisor(5807dfc5-6f47-4de6-af05-f0a575960b8d).html
- Acceleration of memory accesses in dynamic binary translation
	- 2018 PhD Dissertation; Antoine Faravelon
	- https://tel.archives-ouvertes.fr/tel-02004524/
- Cross-ISA Machine Emulation for Multicores
	- Code Generation and Optimization (CGO) 2017
	- Emilio G. Cota, Paolo Bonzini, Alex Bennée, Luca P. Carloni
	- https://sld.cs.columbia.edu/pubs/cota_cgo17.pdf
- Dynamic Binary Modification: Tools, Techniques, and Applications
	- 2011 Book; Kim Hazelwood
	- http://www.morganclaypool.com/doi/abs/10.2200/S00345ED1V01Y201104CAC015
- Dynamically Translating x86 to LLVM using QEMU
	- 2010 Technical Report; Vitaly Chipounov and George Candea
	- https://infoscience.epfl.ch/record/149975/files/x86-llvm-translator-chipounov_
- Efficient and Retargetable SIMD Translation in a Dynamic Binary Translator
	- Software: Practice and Experience, 48(6) 2018
	- Sheng-Yu Fu, Ding-Yong Hong, Yu-Ping Liu, Jan-Jan Wu, Wei-Chung Hsu
	- https://onlinelibrary.wiley.com/doi/abs/10.1002/spe.2573?af=R
- Efficient LLVM-Based Dynamic Binary Translation
	- VEE 2021
	- Alexis Engelke, Dominik Okwieka, Martin Schulz
	- https://doi.org/10.1145/3453933.3454022
	- https://conf.researchr.org/details/vee-2021/vee-2021-papers/6/Efficient-LLVM-Based-Dynamic-Binary-Translation
- Enhancing Atomic Instruction Emulation for Cross-ISA Dynamic Binary Translation
	- Code Generation and Optimization (CGO) 2021
	- Ziyi Zhao, Zhang Jiang, Xiaoli Gong, Ying Chen, Wenwen Wang, Pen-Chung Yew
	- https://github.com/NKU-EmbeddedSystem/ABA-LLSC
	- https://tr0py.github.io/assets/materials/QEMU-ABA-CGO2021.pdf
	- https://tr0py.github.io/assets/materials/QEMU-ABA-CGO2021-slides.pdf
- Fast and Correct Load Link/Store Conditional Instruction Handling in DBT Systems
	- 2020 International Conference on Compilers, Architecture, and Synthesis for Embedded Systems (CASES)
	- Martin Kristien, Tom Spink, Brian Campbell, Susmit Sarkar, Ian Stark, Björn Franke, Igor Böhm, Nigel Topham
	- http://hdl.handle.net/10023/20838
	- _How to emulate LL/SC instructions on hosts that only support Compare-And-Swap (e.g. x86)_
- Helper Function Inlining in Dynamic Binary Translation
	- Compiler Construction (CC) 2021
	- Wenwen Wang
	- https://dl.acm.org/doi/10.1145/3446804.3446851
	- https://homepage.iis.sinica.edu.tw/papers/dyhong/19657-F.pdf
- Hermes: A fast cross-ISA binary translator with post-optimization
	- Code Generation and Optimization (CGO) 2015
	- Xiaochun Zhang, Qi Guo, Yunji Chen, Tianshi Chen, Weiwu Hu
	- http://ieeexplore.ieee.org/document/7054204/
	- https://dl.acm.org/citation.cfm?id=2738631
- Improving Dynamically-Generated Code Performance on Dynamic Binary Translators
	- Virtual Execution Environments VEE 2018
	- Wenwen Wang, Jiacheng Wu, Xiaoli Gong, Tao Li, Pen-Chung Yew
	- https://dl.acm.org/citation.cfm?id=3186413
- Improving SIMD Parallelism via Dynamic Binary Translation
	- Ding-Yong Hong, Yu-Ping Liu, Sheng-Yu Fu, Jan-Jan Wu, Wei-Chung Hsu
	- ACM Transactions on Embedded Computing Systems (TECS) 17(3) 2018
	- https://www.researchgate.net/publication/323149934_Improving_SIMD_Parallelism_via_Dynamic_Binary_Translation
	- https://www.researchgate.net/publication/323865399_Improving_Dynamically-Generated_Code_Performance_on_Dynamic_Binary_Translators
- libdetox: A Framework for Online Program Transformation
	- Forming an Ecosystem Around Software Transformation FEAST 2016
	- Mathias Payer
	- https://nebelwelt.net/publications/files/16FEAST.pdf
	- https://github.com/HexHive/libdetox
- Optimizing Binary Translation of Dynamically Generated Code
	- Code Generation and Optimization (CGO) 2015
	- Byron Hawkins, Brian Demsky, Derek Bruening, Qin Zhao
	- https://research.google.com/pubs/archive/46470.pdf
	- http://demsky.eecs.uci.edu/~bhawkins/papers/cgo-2015.slides.pdf
- Optimizing indirect branches in a system-level dynamic binary translator
	- SYSTOR 2012
	- Toshihiko Koju, Xin Tong, Ali Ijaz Sheikh, Moriyoshi Ohara, Toshio Nakatani
	- http://doi.acm.org/10.1145/2367589.2367599
- Processor-Tracing Guided Region Formation in Dynamic Binary Translation
	- ACM Transactions on Architecture and Code Optimization, Vol. 15, No. 4, Article 52, 2018
	- Ding-Yong Hong, Jan-Jan Wu, Yu-Ping Liu, Sheng-Yu Fu, Wei-Chung Hsu
	- http://dl.acm.org/citation.cfm?id=3281664
- Requirements for Fast Binary Translation
	- Mathias Payer, Thomas R. Gross
	- AMAS-BT: Workshop on Architectural and Microarchitectural Support for Binary Translation 2009
	- https://nebelwelt.net/publications/files/09AMAS-BT.pdf
	- https://nebelwelt.net/publications/files/09AMAS-BT-presentation.pdf
- rv8: a high performance RISC-V to x86 binary translator
	- Workshop on Computer Architecture Research with RISC-V (CARRV) 2017
	- Michael Clark and Bruce Hoult
	- https://anarch128.org/~mclark/rv8-carrv.pdf
	- https://carrv.github.io/2017/papers/clark-rv8-carrv2017.pdf
	- https://rv8.io/
	- https://github.com/rv8-io/rv8
- Scalable Emulation of Heterogeneous Systems
	- 2019 Ph.D. Dissertation; Luca Carloni
	- https://academiccommons.columbia.edu/doi/10.7916/d8-a78j-z392
	- "in this dissertation we first present a novel machine emulator design based on dynamic binary translation that makes the following improvements over the state of the art: it scales on multicore hosts while remaining memory efficient, correctly handles cross-ISA differences in atomic instruction semantics, leverages the host floating point (FP) unit to speed up FP emulation without sacrificing correctness, and can be efficiently instrumented to---among other possible uses---drive the execution of a full-system, cross-ISA simulator with support for accelerators."
- Unleashing the Power of Learning: An Enhanced Learning-Based Approach for Dynamic Binary Translation
	- 2019 USENIX Annual Technical Conference
	- Changheng Song, Wenwen Wang, Pen-Chung Yew, Antonia Zhai, Weihua Zhang
	- https://www.usenix.org/conference/atc19/presentation/song

---

# Software

- Dr. Memory: Memory Debugger for Windows, Linux, Mac, and Android
	- http://drmemory.org/
	- https://github.com/DynamoRIO/drmemory
	- Practical memory checking with Dr. Memory
		- Code Generation and Optimization (CGO) 2011
		- Derek Bruening, Qin Zhao
		- https://www.researchgate.net/publication/224236404_Practical_memory_checking_with_Dr_Memory
		- http://www.burningcutlery.com/derek/docs/drmem-CGO11.pdf
- PANDA: Platform for Architecture-Neutral Dynamic Analysis
	- https://github.com/panda-re/panda

## Software: Frida

- Frida: Dynamic instrumentation toolkit for developers, reverse-engineers, and security researchers.
	- Inject JavaScript to explore native apps on Windows, Mac, Linux, iOS, Android, and QNX.
	- https://www.frida.re/
	- https://github.com/frida/frida
- Awesome Frida - A curated list of Frida resources
	- https://github.com/dweinstein/awesome-frida
- MemREPL: Memory inspection REPL interface
	- https://github.com/agustingianni/memrepl

## Software: Pin

- Pin - A Dynamic Binary Instrumentation Tool
	- https://www.intel.com/software/pintool
	- https://en.wikipedia.org/wiki/Pin_(computer_program)

### Software: Pin: Readings

- Analyzing Parallel Programs With Pin
	- IEEE Computer 43(3) 2010
	- Moshe Bach, Mark Charney, Robert Cohn, Elena Demikhovsky, Tevi Devor, Kim Hazelwood, Aamer Jaleel, Chi-Keung Luk, Gail Lyons, Harish Patil, Ady Tal
	- https://doi.org/10.1109/mc.2010.60
- Pin: Building Customized Program Analysis Tools with Dynamic Instrumentation
	- PLDI 2005
	- Chi-Keung Luk, Robert Cohn, Robert Muth, Harish Patil, Artur Klauser, Geoff Lowney, Steven Wallace, Vijay Janapa Reddi, Kim Hazelwood
	- https://doi.org/10.1145/1065010.1065034
- Controlling Program Execution through Binary Instrumentation
	- SIGARCH Computer Architecture News 33(5) 2005
	- Heidi Pan, Krste Asanović, Robert Cohn, Chi-Keung Luk
	- https://doi.org/10.1145/1127577.1127587
	- http://scale.eecs.berkeley.edu/papers/pin-wbia.pdf
- Deterministic PinPoints: Representative and Repeatable Simulation Region Selection with PinPlay and Sniper
	- HPCA 2013 Tutorial
	- Harish Patil, Trevor E. Carlson
	- https://snipersim.org/w/Tutorial:HPCA_2013_PinPoints
- Dynamic Binary Analysis with Intel Pin
	- https://blog.netspi.com/dynamic-binary-analysis-intel-pin/
	- https://github.com/NetSPI/Pin
- Pinballs: Portable and Shareable User-level Checkpoints for Reproducible Analysis and Simulation
	- REPRODUCE 2014: Workshop on Reproducible Research Methodologies
	- Harish Patil, Trevor E. Carlson
	- https://www.researchgate.net/publication/280306016_Pinballs_Portable_and_Shareable_User-level_Checkpoints_for_Reproducible_Analysis_and_Simulation_Appeared_in_REPRODUCE_2014_Workshop_on_Reproducible_Research_Methodologies
- PinPlay: a framework for deterministic replay and reproducible analysis of parallel programs
	- Code Generation and Optimization (CGO) 2010
	- Harish Patil, Cristiano Pereira, Mack Stallcup, Gregory Lueck, James Cownie
	- https://doi.org/10.1145/1772954.1772958
- PinPlay: Using PinPlay for Reproducible Analysis and Replay Debugging
	- PLDI 2015 Tutorial
	- Harish Patil, Milind Chabbi
	- https://pldi15.sigplan.org/details/pldi2015-workshops/6/PINPLAY-Using-PinPlay-for-Reproducible-Analysis-and-Replay-Debugging
	- https://sites.google.com/site/pinplaypldi2015tutotial/
- PinPoints: Pinpointing Representative Portions of Large Intel® Itanium® Programs with Dynamic Instrumentation
	- MICRO 2004
	- H. Patil, R. Cohn, M. Charney, R. Kapoor, A. Sun, A. Karunanidhi
	- https://doi.org/10.1109/MICRO.2004.28
	- https://software.intel.com/en-us/articles/pin-a-binary-instrumentation-tool-pinpoints
- PinPoints: Simulation Region Selection with PinPlay and Sniper
	- ISCA 2014 Tutorial
	- Harish Patil, Mack Stallcup
	- https://sites.google.com/site/pinpointstutorialisca14/
- Some thoughts about code-coverage measurement with Pin
	- https://doar-e.github.io/blog/2013/08/31/some-thoughts-about-code-coverage-measurement-with-pin/

### Software: Pin: Projects

- Ablation: Augmenting Static Analysis Using Pintool
	- https://github.com/paulmehta/Ablation
	- Black Hat 2016; Paul Mehta
	- https://www.youtube.com/watch?v=wHIlNRK_HiQ
- BasicBlocks: Pin tool for printing the address of each basic block executed in a program.
	- https://github.com/chokepoint/BasicBlocks
- MICA: Microarchitecture-Independent Characterization of Applications
	- a Pin tool for collecting microarchitecture-independent workload characteristics
	- https://github.com/boegel/MICA
- Pin++: A C++ template meta-programmable framework for authoring Pintools
	- https://github.com/SEDS/PinPP
	- Pin++: A Object-oriented Framework for Writing Pintools
		- Generative Programming: Concepts and Experiences (GPCE) 2014
		- James H. Hill and Dennis C. Feiock
		- https://core.ac.uk/download/pdf/46962422.pdf
- pinball2elf: a tool to create stand-alone Linux binaries from checkpoints for arbitrary portions of execution of other Linux programs
	- https://github.com/intel/pinball2elf
	- ELFies: Executable Region Checkpoints for Performance Analysis and Simulation
		- CGO 2021
		- Harish Patil, Alexander Isaev, Wim Heirman, Alen Sabu, Ali Hajiabadi, Trevor E. Carlson
		- https://conf.researchr.org/details/cgo-2021/cgo-2021-papers/11/ELFies-Executable-Region-Checkpoints-for-Performance-Analysis-and-Simulation
		- https://heirman.net/papers/patil2021elfies.pdf
- PinCTF: use Intel's Pin Tool to instrument binaries and count instructions
	- https://github.com/ChrisTheCoolHut/PinCTF

## Software: Sanitizers

- Sanitizers: AddressSanitizer, ThreadSanitizer, MemorySanitizer
	- https://github.com/google/sanitizers
	- https://github.com/google/sanitizers/wiki
- Compilers
	- Clang
		- AddressSanitizer - https://clang.llvm.org/docs/AddressSanitizer.html
		- DataFlowSanitizer - https://clang.llvm.org/docs/DataFlowSanitizer.html
		- Hardware-assisted AddressSanitizer Design Documentation - https://clang.llvm.org/docs/HardwareAssistedAddressSanitizerDesign.html
		- LeakSanitizer - https://clang.llvm.org/docs/LeakSanitizer.html
		- MemorySanitizer - https://clang.llvm.org/docs/MemorySanitizer.html
		- SanitizerCoverage - https://clang.llvm.org/docs/SanitizerCoverage.html
			- SanCov: Above and Below the Sanitizer Interface
				- https://calabi-yau.space/blog/sanitizer-coverage-interface.html
		- SanitizerStats - https://clang.llvm.org/docs/SanitizerStats.html
		- Sanitizer special case list - https://clang.llvm.org/docs/SanitizerSpecialCaseList.html
		- ThreadSanitizer - https://clang.llvm.org/docs/ThreadSanitizer.html
		- UndefinedBehaviorSanitizer - https://clang.llvm.org/docs/UndefinedBehaviorSanitizer.html
			- `-fsanitize=pointer-overflow`
				- Pointer Overflow Checking is in LLVM - https://blog.regehr.org/archives/1518
				- Catching pointer overflow bugs - https://wdtz.org/catching-pointer-overflow-bugs.html
	- GCC
		- https://gcc.gnu.org/onlinedocs/gcc/Instrumentation-Options.html
		- Address and Thread Sanitizers in GCC
			- https://developers.redhat.com/blog/2014/12/02/address-and-thread-sanitizers-gcc/
		- Useful GCC address sanitizer checks not enabled by default
			- https://kristerw.blogspot.com/2018/06/useful-gcc-address-sanitizer-checks-not.html
	- MSVC
		- AddressSanitizer - https://docs.microsoft.com/en-us/cpp/sanitizers/asan
- DRace: Data-race detector for Windows applications built on top of DynamoRIO
	- shipped with the following detector backends: tsan (internal ThreadSanitizer), fasttrack, dummy (no detection at all), printer (print all calls to the detector)
	- https://github.com/siemens/drace
	- Dynamic Instrumentation of Code for Data-Race Detection
		- MUC++ 2020; Felix Mößbauer
		- https://www.youtube.com/watch?v=zWVipIkcypU
	- High Performance Dynamic Threading Analysis for Hybrid Applications
		- 2019 Master Thesis; Felix Mößbauer
		- https://doi.org/10.5282/ubm/epub.60621
- Kernel Concurrency Sanitizer (KCSAN)
	- https://github.com/google/ktsan/wiki/KCSAN
	- Concurrency bugs should fear the big bad data-race detector
		- part 1: https://lwn.net/Articles/816850/
		- part 2: https://lwn.net/Articles/816854/
- Kernel Thread Sanitizer (KTSAN)
	- https://github.com/google/ktsan
	- https://github.com/google/ktsan/wiki

### Software: Sanitizers: Readings

- Adding Clang Sanitizers to a CMake Build
	- https://genbattle.bitbucket.io/blog/2018/01/05/Dev-Santa-Claus-Part-1/
		- https://old.reddit.com/r/cpp/comments/7qzqlg/dev_santa_claus_pt1_adding_clang_sanitizers_to_a/
- All about sanitizer interceptors
	- 2023; MaskRay (Fangrui Song)
	- https://maskray.me/blog/2023-01-08-all-about-sanitizer-interceptors
- Creating an LLVM Sanitizer from Hopes and Dreams
	- https://blog.trailofbits.com/2019/06/25/creating-an-llvm-sanitizer-from-hopes-and-dreams/
	- llvm-sanitizer-tutorial and documentation
		- https://github.com/trailofbits/llvm-sanitizer-tutorial
- GWP-ASan: Sampling heap memory error detection in-the-wild
	- 2019; Vlad Tsyrklevich
	- https://sites.google.com/a/chromium.org/dev/Home/chromium-security/articles/gwp-asan
- Memory error checking in C and C++: Comparing Sanitizers and Valgrind
	- https://developers.redhat.com/blog/2021/05/05/memory-error-checking-in-c-and-c-comparing-sanitizers-and-valgrind/
- SoK: Sanitizing for Security
	- IEEE Symposium on Security and Privacy (S&P) 2019
	- Dokyung Song, Julian Lettner, Prabhu Rajasekaran, Yeoul Na, Stijn Volckaert, Per Larsen, Michael Franz
	- https://ieeexplore.ieee.org/document/8835294
	- https://github.com/securesystemslab/sanitizing-for-security-benchmarks

#### Software: Sanitizers: Readings: Research

- AddressSanitizer: A Fast Address Sanity Checker
	- 2012 USENIX Annual Technical Conference (ATC)
	- Konstantin Serebryany, Derek Bruening, Alexander Potapenko, Dmitry Vyukov
	- https://www.usenix.org/conference/atc12/technical-sessions/presentation/serebryany
	- https://research.google/pubs/pub37752/
- MemorySanitizer: fast detector of uninitialized memory use in C++
	- Code Generation and Optimization (CGO) 2015
	- Evgeniy Stepanov and Konstantin Serebryany
	- https://research.google.com/pubs/archive/43308.pdf
- TypeSanitizer: Practical Type Confusion Detection
	- Computer and Communications Security (CCS) 2016
	- Istvan Haller, Yuseok Jeon, Hui Peng, Mathias Payer, Herbert Bos, Cristiano Giuffrida, Erik van der Kouwe
	- https://nebelwelt.net/publications/files/16CCS2.pdf
	- TypeSan checks casts in C++ code - code released for CCS 2016
		- https://github.com/vusec/typesan

##### Software: Sanitizers: Readings: Research: 2017

- DangSan: Scalable Use-after-free Detection
	- European Conference on Computer Systems (EuroSys) 2017
	- Erik van der Kouwe, Vinod Nigade, Cristiano Giuffrida
	- http://www.cs.vu.nl/~giuffrida/papers/dangsan_eurosys17.pdf
	- https://github.com/vusec/dangsan
- HexType: Efficient Detection of Type Confusion Errors for C++
	- ACM Conference on Computer and Communication Security (CCS) 2017
	- Yuseok Jeon, Priyam Biswas, Scott A. Carr, Byoungyoung Lee, and Mathias Payer.
	- Paper (PDF): https://nebelwelt.net/publications/files/17CCS.pdf
	- Slides (PDF): http://nebelwelt.net/publications/files/17CCC-presentation.pdf
	- 34C3 (2017)
		- https://media.ccc.de/v/34c3-8848-type_confusion_discovery_abuse_and_protection
		- https://www.youtube.com/watch?v=jbglFfkRYQs
	- HexType: Efficient Detection of Type Confusion Errors for C++
		- https://github.com/HexHive/HexType
- HexVASAN: Venerable Variadic Vulnerabilities Vanquished
	- USENIX Security Symposium 2017
	- Priyam Biswas, Alessandro Di Federico, Scott A. Carr, Prabhu Rajasekaran, Stijn Volckaert, Yeoul Na, Michael Franz, and Mathias Payer.
	- https://nebelwelt.net/publications/files/17SEC.pdf
	- https://nebelwelt.net/publications/files/17SEC-presentation.pdf
	- https://github.com/HexHive/HexVASAN

##### Software: Sanitizers: Readings: Research: 2018

- CastSan: Efficient Detection of Polymorphic C++ Object Type Confusions with LLVM
	- European Symposium on Research in Computer Security (ESORICS) 2018
	- Muntean P., Wuerl S., Grossklags J., Eckert C.
	- https://link.springer.com/chapter/10.1007/978-3-319-99073-6_1
	- https://www.docdroid.net/INWYBF7/castsan-esorics18.pdf
- CUP: Comprehensive User-Space Protection for C/C++
	- AsiaCCS 2018
	- Nathan Burow, Derrick McKee, Scott A. Carr, Mathias Payer
	- https://hexhive.github.io/publications/files/18AsiaCCS.pdf
	- https://github.com/HexHive/CUP
- EffectiveSan: Type and Memory Error Detection using Dynamically Typed C/C++
	- PLDI 2018
	- Gregory J. Duck, Roland H. C. Yap
	- https://arxiv.org/abs/1710.06125
	- https://github.com/GJDuck/EffectiveSan
	- https://pldi18.sigplan.org/event/pldi-2018-papers-effectivesan-type-and-memory-error-detection-using-dynamically-typed-c-c-
- PartiSan: Fast and Flexible Sanitization via Run-time Partitioning
	- Research in Attacks, Intrusions and Defenses (RAID) 2018
	- Julian Lettner, Dokyung Song, Taemin Park, Stijn Volckaert, Per Larsen, Michael Franz
	- https://arxiv.org/abs/1711.08108

##### Software: Sanitizers: Readings: Research: 2020

- A Preliminary Study on Open-Source Memory Vulnerability Detectors
	- International Conference on Software Analysis, Evolution, and Reengineering (SANER), ERA track, 2020
	- Yu Nong and Haipeng Cai
	- http://chapering.github.io/pubs/saner20-a.pdf
	- AddressSanitizer, CBMC, DrMemory, MemorySanitizer, Valgrind
	- Research questions:
		- RQ1: How effective are these detectors in terms of precision, recall, and accuracy?
		- RQ2: How efficient are the detectors in terms of their cost for detecting vulnerabilities?
		- RQ3: How do these detectors compare in terms of their detection accuracy?
- Debugging and Detecting Numerical Errors in Computation with Posits
	- PLDI 2020
	- Sangeeta Chowdhary, Jay P. Lim, Santosh Nagarakatte
	- https://doi.org/10.1145/3385412.3386004
	- https://www.cs.rutgers.edu/~santosh.nagarakatte/papers/PositDebug-PLDI-2020-preprint.pdf
	- FPSanitizer: A debugger to detect and diagnose numerical errors in floating point programs
		- https://github.com/rutgers-apl/fpsanitizer
	- PositDebug: A debugger to detect numerical errors in applications using posits
		- https://github.com/rutgers-apl/PositDebug
- FuZZan: Efficient Sanitizer Metadata Design for Fuzzing
	- USENIX Annual Technical Conference (USENIX ATC) 2020
	- Yuseok Jeon, WookHyun Han, Nathan Burow, Mathias Payer
	- https://nebelwelt.net/files/20ATC.pdf
	- https://github.com/HexHive/FuZZan
- ParmeSan: Sanitizer-guided Greybox Fuzzing
	- USENIX Security 2020
	- Sebastian Österlund, Kaveh Razavi, Herbert Bos, Cristiano Giuffrida
	- https://github.com/vusec/parmesan
	- https://www.usenix.org/conference/usenixsecurity20/presentation/osterlund

##### Software: Sanitizers: Readings: Research: 2021

- NSan: A Floating-Point Numerical Sanitizer
	- Compiler Construction (CC) 2021
	- Clement Courbet
	- https://dl.acm.org/doi/abs/10.1145/3446804.3446848
	- https://arxiv.org/abs/2102.12782
	- https://reviews.llvm.org/D97854
- Parallel Shadow Execution to Accelerate the Debugging of Numerical Errors
	- ESEC/FSE 2021
	- Sangeeta Chowdhary, Santosh Nagarakatte
	- https://doi.org/10.1145/3468264.3468585
	- https://www.cs.rutgers.edu/~santosh.nagarakatte/papers/fse-2021-final-preprint.pdf
	- https://people.cs.rutgers.edu/~sn349/papers/fse-2021-final-preprint.pdf
	- https://2021.esec-fse.org/details/fse-2021-papers/54/Parallel-Shadow-Execution-to-Accelerate-the-Debugging-of-Numerical-Errors
	- PFPSanitizer: A Parallel Shadow Execution Tool for Debugging Numerical Errors
		-https://github.com/rutgers-apl/PFPSanitizer
- SanRazor: Reducing Redundant Sanitizer Checks in C/C++ Programs
	- USENIX Symposium on Operating Systems  Design and Implementation (OSDI) 2021
	- Jiang Zhang, Shuai Wang, Manuel Rigger, Pinjia He, Zhendong Su
	- https://www.usenix.org/conference/osdi21/presentation/zhang
	- https://github.com/SanRazor-repo/SanRazor
- UAFSan: An Object-Identifier-Based Dynamic Approach for Detecting Use-After-Free Vulnerabilities
	- ISSTA 2021
	- Binfa Gui, Wei Song, Jeff Huang
	- https://doi.org/10.1145/3460319.3464835
	- UAFSan: a sanitizer that can detect UAFs (including double frees) in C/C++ software at runtime
		- https://github.com/wsong-nj/UAFSan

##### Software: Sanitizers: Readings: Research: 2022

- Debloating Address Sanitizer
	- USENIX Security Symposium 2022
	- Yuchen Zhang, Chengbin Pang, Georgios Portokalidis, Nikos Triandopoulos, Jun Xu
	- https://www.usenix.org/system/files/sec22summer_zhang-yuchen.pdf
	- https://github.com/junxzm1990/ASAN--
- Efficient Greybox Fuzzing to Detect Memory Errors
	- Automated Software Engineering (ASE) 2022
	- Jinsheng Ba, Gregory J. Duck, Abhik Roychoudhury
	- https://arxiv.org/abs/2204.02773
	- ReZZan: RET+Fuzzing+Sanitizer
		- a fast memory error sanitizer for fuzzing C/C++ code
		- https://github.com/bajinsheng/ReZZan
- SafePM: A Sanitizer for Persistent Memory
	- EuroSys 2022
	- Kartal Kaan Bozdoğan, Dimitrios Stavrakakis, Shady Issa, Pramod Bhatotia
	- https://dse.in.tum.de/wp-content/uploads/2022/04/final_digital_version.pdf
	- https://dse.in.tum.de/wp-content/uploads/2022/04/SafePM_eurosys22_presentation.pdf
	- SafePM: Memory Safety for Persistent Memory
	- https://github.com/TUM-DSE/safepm
- SymSan: Time and Space Efficient Concolic Execution via Dynamic Data-Flow Analysis
	- USENIX Security 2022
	- Ju Chen, Wookhyun Han, Mingjun Yin, Haochen Zeng, Chengyu Song, Byoungyong Lee, Heng Yin, and Insik Shin
	- https://www.usenix.org/conference/usenixsecurity22/presentation/chen-ju
	- An LLVM Sanitizer for Symbolic Tracing
		- https://github.com/R-Fuzz/symsan

### Software: Sanitizers: Projects

- QASan: QEMU-AddressSanitizer
	- a custom QEMU that detects memory errors in the guest using AddressSanitizer
	- https://github.com/andreafioraldi/qasan
	- Sanitized Emulation with QASan
		- https://andreafioraldi.github.io/articles/2019/12/20/sanitized-emulation-with-qasan.html
	- Fuzzing binaries for memory safety errors with QASan
		- IEEE Secure Development Conference (SecDev) 2020
		- Andrea Fioraldi, Daniele Cono D’Elia, Leonardo Querzoni
		- https://andreafioraldi.github.io/assets/qasan-secdev20.pdf
		- https://andreafioraldi.github.io/assets/qasan-secdev20-slides.pdf
		- https://youtube.com/watch?v=UtFXU7Nkd8g
- sanitizers-cmake: CMake modules to help use sanitizers
	- https://github.com/arsenm/sanitizers-cmake
- TypeART: LLVM-based type and memory allocation tracking sanitizer
	- https://github.com/tudasc/TypeART
	- Compiler-aided Type Tracking for Correctness Checking of MPI Applications
		- International Workshop on Software Correctness for HPC Applications (Correctness) 2018
		- Alexander Hück, Jan-Patrick Lehr, Sebastian Kreutzer, Joachim Protze, Christian Terboven, Christian Bischof, Matthias S. Müller
		- https://doi.org/10.1109/Correctness.2018.00011
		- https://correctness-workshop.github.io/2018/papers/lehr.pdf

### Software: Sanitizers: Talks

- AddressSanitizer, ThreadSanitizer and MemorySanitizer -- Dynamic Testing Tools for C++
	- GTAC 2013; Kostya Serebryany
	- https://www.youtube.com/watch?v=Q2C2lP8_tNE
- Address and Thread Sanitizer in GCC: State of the Onion
	- GNU Tools Cauldron 2013; Dodji Seketeli
	- https://gcc.gnu.org/wiki/cauldron2013?action=AttachFile&do=view&target=asan.pdf
	- https://www.youtube.com/watch?v=41_WZk6AePY
- C++ Sanitizers
	- C++ Weekly; Ep. 84 (2017)
	- https://www.youtube.com/watch?v=MB6NPkB4YVs
- Debugging with LLVM: A quick introduction to LLDB and LLVM sanitizers
	- FOSDEM 2020
	- Andrzej Warzynski; Graham Hunter
	- https://fosdem.org/2020/schedule/event/debugging_with_llvm/
- Finding races and memory errors with LLVM instrumentation
	- 2011 LLVM Developers’ Meeting; Konstantin Serebryany
	- https://www.youtube.com/watch?v=sJqQTUtV6GY
- Finding races and memory errors with compiler instrumentation: AddressSanitizer, ThreadSanitizer
	- GNU Tools Cauldron 2012; Konstantin Serebryany, Dmitry Vyukov
	- https://gcc.gnu.org/wiki/cauldron2012?action=AttachFile&do=get&target=kcc.pdf
	- https://gcc.gnu.org/wiki/cauldron2012#Finding_races_and_memory_errors_with_GCC_instrumentation_.28AddressSanitizer.29
- MemorySanitizer, ThreadSanitizer: Scalable run-time detection of uninitialized memory reads and data races with LLVM instrumentation
	- 2012 LLVM Developers’ Meeting; Kostya Serebryany
	- https://www.youtube.com/watch?v=HDgttiIvMxA
- New Address Sanitizer Features
	- 2013 LLVM Developers’ Meeting
	- Kostya Serebryany, Alexey Samsonov
	- https://www.youtube.com/watch?v=ldZvZE8fWwA
	- https://llvm.org/devmtg/2013-11/slides/Serebryany-ASAN.pdf
- News from Sanitizers
	- GNU Tools Cauldron 2014; Evgeniy Stepanov, Kostya Serebryany
	- https://docs.google.com/presentation/d/1QG2qlzpxlsdDsX4uHhTLWAoUmbzbhedFMoMvviud0Us
	- https://www.youtube.com/watch?v=Ek7z_oC0dak
- Run-time tracking of uninitialized data with MemorySanitizer
	- 2013 EuroLLVM Developers’ Meeting; Evgeniy Stepanov
	- https://www.youtube.com/watch?v=2Y0T-1AB-gY
- The Type Sanitizer: Free Yourself from -fno-strict-aliasing
	- 2017 LLVM Developers’ Meeting; Hal Finkel
	- https://www.youtube.com/watch?v=vAXJeN7k32Y
- ThreadSanitizer APIs for external libraries
	- 2017 LLVM Developers’ Meeting; Kuba Mracek
	- https://www.youtube.com/watch?v=-J9bMpqfc7A

## Software: Valgrind

- Valgrind
	- http://valgrind.org/
	- Valgrind is an instrumentation framework for building dynamic analysis tools. There are Valgrind tools that can automatically detect many memory management and threading bugs, and profile your programs in detail. You can also use Valgrind to build new tools.
- Valgrind
	- Overload Journal; Paul Floyd
	- Part 1 – Introduction - https://accu.org/index.php/journals/1930
	- Part 2 – Basic memcheck - https://accu.org/index.php/journals/1913
	- Part 3 – Advanced memcheck - https://accu.org/index.php/journals/1905
	- Part 4 – Cachegrind and Callgrind - https://accu.org/index.php/journals/1886
	- Part 5 – Massif - https://accu.org/index.php/journals/1884
	- Part 6 – Helgrind and DRD - https://accu.org/index.php/journals/1867
- Valgrind
	- C++ Weekly - Episode 86
	- https://www.youtube.com/watch?v=3l0BQs2ThTo
- Valgrind Memcheck: Different ways to lose your memory
	- https://developers.redhat.com/blog/2021/04/23/valgrind-memcheck-different-ways-to-lose-your-memory/
- gdb + valgrind - https://fau.re/blog/20140330_vgdb.html
- Valgrind and GDB: Tame the Wild C - https://heeris.id.au/2016/valgrind-gdb/
- Watching for software inefficiencies with Valgrind
	- https://kristerw.blogspot.com/2020/02/watching-for-software-inefficiencies.html
	- deadstores: A Valgrind tool for finding redundant loads/stores.
		- https://github.com/kristerw/deadstores
- CFGGrind: Dynamic Control Flow Graph Reconstruction
	- https://github.com/rimsa/CFGgrind
	- https://compilers.iecc.com/comparch/article/19-11-004
	- Practical Dynamic Reconstruction of Control Flow Graphs
		- Software: Practice and Experience, 2020
		- Andrei Rimsa, José Nelson Amaral, Fernando Magno Quintão Pereira
		- https://homepages.dcc.ufmg.br/~fernando/publications/papers/RimsaSPE20.pdf
- InstrGrind: A dynamic instruction counter plugin for Valgrind
	- https://github.com/rimsa/instrgrind
	- Instruction Visibility in SPEC CPU2017
		- Journal of Computer Languages, Volume 66, 2021
		- Andrei Rimsa Álvares, José Nelson Amaral, Fernando Magno Quintão Pereira
		- https://doi.org/10.1016/j.cola.2021.101062
		- https://homepages.dcc.ufmg.br/~fernando/publications/papers/AlvaresJCL21.pdf
- Taintgrind: A taint-tracking plugin for the Valgrind memory checking tool
	- https://github.com/wmkhoo/taintgrind
- Use Valgrind Memcheck with a custom memory manager
	- https://developers.redhat.com/articles/2022/03/23/use-valgrind-memcheck-custom-memory-manager
