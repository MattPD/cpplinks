# [C++ links](README.md): Program Analysis - Dynamic

See also:

- [Compilers](https://github.com/MattPD/cpplinks/blob/master/compilers.md)
- [Debugging](https://github.com/MattPD/cpplinks/blob/master/debugging.md)
- [Program Analysis](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef) - [LLVM](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef#llvm)
- [Testing](https://github.com/MattPD/cpplinks/blob/master/testing.md)
- https://en.wikipedia.org/wiki/Dynamic_program_analysis

# Contents

- [Dynamic Binary Instrumentation (DBI)](#dynamic-binary-instrumentation-dbi)
- [Dynamic Binary Translation (DBT)](#dynamic-binary-translation-dbt)
- [Software](#software):
	- [Frida](#software-frida)
	- [Pin](#software-pin)
	- [Sanitizers](#software-sanitizers)
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
	- http://deniable.org/reversing/binary-instrumentation
	- https://github.com/fdiskyou/DBI
- Optimization of Naïve Dynamic Binary Instrumentation Tools
	- 2011 Ph.D. Dissertation; Reid Kleckner
	- https://dspace.mit.edu/handle/1721.1/76984
- Security Evaluation of Dynamic Binary Instrumentation Engines
	- DBI Engine Detection Tool and all PoC code
		- https://github.com/zhechkoz/PwIN
	- 2018 Master Thesis; Zhechko Zhechev
		- https://kirschju.re/static/ma_zhechev_2018.pdf
	- REcon Montreal 2018
		- https://kirschju.re/static/recon_2018_kirsch_zhechev_pwin.pdf
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
- Using Binary Instrumentation for Vulnerability Discovery (or even mitigation!)
	- EuskalHack 2018; Joxean Koret
	- https://github.com/joxeankoret/membugtool/blob/master/docs/Using%20Binary%20Instrumentation%20for%20Vulnerability%20Discovery%20(or%20even%20mitigation!).pdf
	- https://docs.google.com/presentation/d/e/2PACX-1vQYw4HJ3kzdmjnxklyBK2nyoMV3Iftx5G6IQmaas7z1cJdP04sX9WsWZmZKqtcTOsqbYukDdUyovhXb/pub

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
- Tracer: Set of Dynamic Binary Instrumentation and visualization tools for execution traces.
	- https://github.com/SideChannelMarvels/Tracer
	- https://insinuator.net/2016/03/how-to-crack-a-white-box-without-much-effort/
	- TracerPIN: TracerPin is a Intel PIN tool for generating execution traces of a running process.
	- TracerGrind: TracerGrind is a Valgrind tool for generating execution traces of a running process.
	- TraceGraph: TraceGraph is a GUI for visualizing execution traces produced by TracerGrind and TracerPin.

---

# Dynamic Binary Translation (DBT)

- A Retargetable System-Level DBT Hypervisor
	- 2019 USENIX Annual Technical Conference
	- Tom Spink, Harry Wagstaff, Björn Franke
	- https://www.usenix.org/conference/atc19/presentation/spink
- Unleashing the Power of Learning: An Enhanced Learning-Based Approach for Dynamic Binary Translation
	- 2019 USENIX Annual Technical Conference
	- Changheng Song, Wenwen Wang, Pen-Chung Yew, Antonia Zhai, Weihua Zhang
	- https://www.usenix.org/conference/atc19/presentation/song
- Acceleration of memory accesses in dynamic binary translation
	- 2018 PhD Dissertation; Antoine Faravelon
	- https://tel.archives-ouvertes.fr/tel-02004524/
- Cross-ISA Machine Emulation for Multicores
	- Code Generation and Optimization (CGO) 2017
	- Emilio G. Cota, Paolo Bonzini, Alex Bennée, Luca P. Carloni
	- https://sld.cs.columbia.edu/pubs/cota_cgo17.pdf
- Dynamic Binary Modification: Tools, Techniques, and Applications No Access
	- 2011 Book; Kim Hazelwood
	- http://www.morganclaypool.com/doi/abs/10.2200/S00345ED1V01Y201104CAC015
- Dynamically Translating x86 to LLVM using QEMU
	- 2010 Technical Report; Vitaly Chipounov and George Candea
	- https://infoscience.epfl.ch/record/149975/files/x86-llvm-translator-chipounov_
- Efficient and Retargetable SIMD Translation in a Dynamic Binary Translator
	- Software: Practice and Experience, 48(6) 2018
	- Sheng-Yu Fu, Ding-Yong Hong, Yu-Ping Liu, Jan-Jan Wu, Wei-Chung Hsu
	- https://onlinelibrary.wiley.com/doi/abs/10.1002/spe.2573?af=R
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
	- https://carrv.github.io/papers/clark-rv8-carrv2017.pdf  
	- https://rv8.io/
	- https://github.com/rv8-io/rv8
- Scalable Emulation of Heterogeneous Systems
	- 2019 Ph.D. Dissertation; Luca Carloni
	- https://academiccommons.columbia.edu/doi/10.7916/d8-a78j-z392
	- "in this dissertation we first present a novel machine emulator design based on dynamic binary translation that makes the following improvements over the state of the art: it scales on multicore hosts while remaining memory efficient, correctly handles cross-ISA differences in atomic instruction semantics, leverages the host floating point (FP) unit to speed up FP emulation without sacrificing correctness, and can be efficiently instrumented to---among other possible uses---drive the execution of a full-system, cross-ISA simulator with support for accelerators."

---

# Software

- Dr. Memory: Memory Debugger for Windows, Linux, Mac, and Android
	- http://drmemory.org/
	- https://github.com/DynamoRIO/drmemory
	- Practical memory checking with Dr. Memory
		- Code Generation and Optimization (CGO) 2011
		- Derek Bruening, Qin Zhao
		- https://www.researchgate.net/publication/224236404_Practical_memory_checking_with_Dr_Memory
- DynamoRIO: Dynamic Instrumentation Tool Platform
	- https://dynamorio.org/
	- https://github.com/DynamoRIO/dynamorio
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
	- http://www.pintool.org/
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
	- 
https://www.researchgate.net/publication/280306016_Pinballs_Portable_and_Shareable_User-level_Checkpoints_for_Reproducible_Analysis_and_Simulation_Appeared_in_REPRODUCE_2014_Workshop_on_Reproducible_Research_Methodologies
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
- PinCTF: use Intel's Pin Tool to instrument binaries and count instructions
	- https://github.com/ChrisTheCoolHut/PinCTF

## Software: Sanitizers

- Sanitizers: AddressSanitizer, ThreadSanitizer, MemorySanitizer
	- https://github.com/google/sanitizers
	- https://github.com/google/sanitizers/wiki
- Debugging with LLVM: A quick introduction to LLDB and LLVM sanitizers
	- FOSDEM 2020
	- Andrzej Warzynski; Graham Hunter
	- https://fosdem.org/2020/schedule/event/debugging_with_llvm/
- sanitizers-cmake: CMake modules to help use sanitizers
	- https://github.com/arsenm/sanitizers-cmake

## Software: Valgrind

- Valgrind
	- http://valgrind.org/
	- Valgrind is an instrumentation framework for building dynamic analysis tools. There are Valgrind tools that can automatically detect many memory management and threading bugs, and profile your programs in detail. You can also use Valgrind to build new tools.
- Valgrind
	- Overload Journal; Paul Floyd
	- Part 1 – Introduction - https://accu.org/index.php/journals/1930
	- Valgrind Part 2 – Basic memcheck - https://accu.org/index.php/journals/1913
	- Valgrind Part 3: Advanced memcheck - https://accu.org/index.php/journals/1905
	- Valgrind Part 4: Cachegrind and Callgrind - https://accu.org/index.php/journals/1886
	- Valgrind Part 5 – Massif - https://accu.org/index.php/journals/1884
	- Valgrind Part 6 – Helgrind and DRD - https://accu.org/index.php/journals/1867
- Valgrind
	- C++ Weekly - Episode 86
	- https://www.youtube.com/watch?v=3l0BQs2ThTo
- gdb + valgrind - https://fau.re/blog/20140330_vgdb.html
- Valgrind and GDB: Tame the Wild C - http://heeris.id.au/2016/valgrind-gdb/
- Watching for software inefficiencies with Valgrind 
	- https://kristerw.blogspot.com/2020/02/watching-for-software-inefficiencies.html
	- deadstores: A Valgrind tool for finding redundant loads/stores. 
		- https://github.com/kristerw/deadstores
- CFGGrind: Dynamic Control Flow Graph Reconstruction
	- https://github.com/rimsa/CFGgrind
	- https://compilers.iecc.com/comparch/article/19-11-004
- Taintgrind: A taint-tracking plugin for the Valgrind memory checking tool
	- https://github.com/wmkhoo/taintgrind
