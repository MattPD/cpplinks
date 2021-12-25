# [C++ links](README.md): ARM and AArch64 Assembly

See also: [Computer Architecture](comparch.md) -- recommended background (which makes the following significantly more approachable) includes an undergraduate-level course.

# Contents

- [Readings](#readings):
	- [Binary Analysis](#readings-binary-analysis)
	- [Concurrency](#readings-concurrency)
	- [Formalization, Specification, Verification](#formalization-specification-verification)
	- [Instruction Set Architecture](#instruction-set-architecture)
	- [Performance](#performance)
	- [Security](#security):
		- [Memory Tagging Extension (MTE)](#memory-tagging-extension-mte)
		- [Pointer Authentication](#pointer-authentication)
		- [TrustZone](#trustzone)
	- [Simulation](#simulation)
	- [Virtualization](#virtualization)
- [References](#references):
	- [Intrinsics & SIMD](#intrinsics--simd)
	- [Microarchitecture](#references-microarchitecture)
	- [OS](#references-os)
	- [Toolchains](#references-toolchains)
- [Software](#software):
	- [Assembly](#software-assembly)
	- [Binary Analysis](#software-binary-analysis)
	- [Concurrency](#software-concurrency)
	- [Debugging, Tracing](#software-debugging-tracing)
	- [Emulation, Simulation](#software-emulation-simulation): [x86, x86-64]((#software-emulation-simulation-x86-x86-64)
	- [Lifting: Disassemblers, Decompilers, Recompilers](#software-lifting)
	- [Performance](#software-performance): [SIMD](#software-performance-simd)
	- [Virtualization](#software-virtualization)
- [Talks](#talks): [2019](#2019), [2018](#2018), [2017](#2017), [2016](#2016), [2015](#2015), [2014](#2014), [2012](#2012), [2011](#2011), [2010](#2010), [History](#history)
- [Tutorials, Courses](#tutorials-courses): [AArch64](#aarch64), [Thumb-2](#thumb-2)

---

# Readings

## Readings: Binary Analysis

See also: [Software: Binary Analysis](https://github.com/MattPD/cpplinks/blob/master/assembly.arm.md#software-binary-analysis)

- A Retargetable Static Binary Translator for the ARM Architecture
	- ACM Transactions on Architecture and Code Optimization, 11(2) 2014
	- Shen, B.-Y., Hsu, W.-C., & Yang, W.
	- https://doi.org/10.1145/2629335
- An Empirical Study on ARM Disassembly Tools
	- International Symposium on Software Testing and Analysis (ISSTA) 2020
	- Muhui Jiang, Yajin Zhou, Xiapu Luo, Ruoyu Wang, Yang Liu, Kui Ren
	- https://yajin.org/papers/issta20.pdf
	- https://github.com/valour01/arm_disasssembler_study
- ArmWrestling: efficient binary rewriting for ARM
	- 2021 Master's Thesis
	- Luca Di Bartolomeo
	- https://doi.org/10.3929/ethz-b-000474088
	- https://hexhive.epfl.ch/theses/20-dibartolomeo-thesis.pdf
- Balancing Performance and Productivity for the Development of Dynamic Binary Instrumentation Tools: A Case Study on Arm Systems
	- Compiler Construction (CC) 2020
	- Cosmin Gorgovan, Guillermo Callaghan, Mikel Luján
	- https://doi.org/10.1145/3377555.3377895
	- https://www.research.manchester.ac.uk/portal/files/158729354/mambo_api_cc2020_cr_authors.pdf
- Exploiting SIMD Asymmetry in ARM-to-x86 Dynamic Binary Translation
	- ACM Transactions on Architecture and Code Optimization (TACO) 2019
	- Yu-Ping Liu, Ding-Yong Hong, Jan-Jan Wu, Sheng-Yu Fu, Wei-Chung Hsu
	- http://dl.acm.org/citation.cfm?id=3301488
- Exploiting Vector Processing in Dynamic Binary Translation
	- 2019 International Conference on Parallel Processing (ICPP)
	- Chih-Min Lin, Sheng-Yu Fu, Ding-Yong Hong, Yu-Ping Liu, Jan-Jan Wu, Wei-Chung Hsu
	- https://doi.org/10.1145/3337821.3337844
- Optimising Dynamic Binary Modification across 64-bit Arm Microarchitectures
	- VEE 2020
	- Guillermo Callaghan, Cosmin Gorgovan, Mikel Lujan
	- https://doi.org/10.1145/3381052.3381322
	- https://conf.researchr.org/details/vee-2020/vee-2020-papers/8/Optimising-Dynamic-Binary-Modification-across-64-bit-Arm-Microarchitectures
	- https://www.youtube.com/watch?v=3jxLu1zGpV0
- RevARM: A Platform-Agnostic ARM Binary Rewriter for Security Applications
	- Annual Computer Security Applications Conference (ACSAC) 2017
	- T. Kim, C. Kim, H. Choi, Y. Kwon, B. Saltaformaggio, X. Zhang, D. Xu
	- <https://saltaformaggio.ece.gatech.edu/publications/ACSAC_17.pdf>
	- <https://www.acsac.org/2017/openconf/modules/request.php?module=oc_program&action=summary.php&id=201>
	- <https://www.researchgate.net/publication/321506390_RevARM_A_Platform-Agnostic_ARM_Binary_Rewriter_for_Security_Applications>
- Translating AArch64 Floating-Point Instruction Set to the x86-64 Platform
	- 2019 International Conference on Parallel Processing: Workshops (ICPP)
	- Yi-Ping You, Tsung-Chun Lin, and Wuu Yang
	- https://doi.org/10.1145/3339186.3339192

## Readings: Concurrency

- Atomics in AArch64
	- 2021; Jim Cownie
	- https://cpufun.substack.com/p/atomics-in-aarch64
- Formalising the ARMv8 Memory Consistency Model
	- Will Deacon, ARM, Keynote, OpenSHMEM 2018
	- https://www.csm.ornl.gov/workshops/openshmem2018/presentations/mm-openshmem2018.pdf
- Isla-axiomatic: combines Sail ISA specifications with axiomatic memory models with an SMT solver
	- Isla: a symbolic execution engine for Sail
		- Executes instruction set architecture (ISA) specifications written in Sail, such as Sail ARMv8 model translated from ARM’s machine readable specification, or Sail RISC-V. It can be used to evaluate the relaxed-memory behavior of instruction set architectures specified in Sail, using an axiomatic memory model specified in a subset of the cat language used by the herd7 tools.
		- https://github.com/rems-project/isla
	- Isla-axiomatic: combines Sail ISA specifications with axiomatic memory models written in a subset of the cat language used by the diy tool suite (and in particular the memory model simulation tool herd7), with an SMT solver like z3 or CVC4.
		- https://isla-axiomatic.cl.cam.ac.uk/
		- https://isla-axiomatic.cl.cam.ac.uk/help_standalone.html
	- Isla: Integrating Full-Scale ISA Semantics and Axiomatic Concurrency Models
		- Computer Aided Verification (CAV) 2021
		- Alasdair Armstrong, Brian Campbell, Ben Simner, Christopher Pulte, Peter Sewell
		- https://link.springer.com/chapter/10.1007/978-3-030-81685-8_14
- Mixed-size Concurrency: ARM, POWER, C/C++11, and SC
	- POPL 2017
	- Shaked Flur, Susmit Sarkar, Christopher Pulte, Kyndylan Nienhuis, Luc Maranget, Kathryn E. Gray, Ali Sezgin, Mark Batty, Peter Sewell
	- http://www.cl.cam.ac.uk/~pes20/popl17/
	- http://www.cl.cam.ac.uk/~pes20/AArch64
- Modelling the ARM v8 Architecture, Operationally: Concurrency and ISA
	- POPL 2016
	- Shaked Flur, Kathryn E. Gray, Christopher Pulte, Susmit Sarkar, Ali Sezgin, Luc Maranget, Will Deacon, Peter Sewell
	- http://www.cl.cam.ac.uk/~pes20/popl16-armv8/top.pdf
	- https://blog.acolyer.org/2016/02/02/arm-v8/
- No Barrier in the Road: A Comprehensive Study and Optimization of ARM Barriers
	- Principles and Practice of Parallel Programming (PPoPP) 2020
	- Nian Liu, Binyu Zang, Haibo Chen
	- https://doi.org/10.1145/3332466.3374535
	- https://ipads.se.sjtu.edu.cn/_media/publications/liuppopp20.pdf
- Relaxed-Memory Concurrency - Power and ARM
	- http://www.cl.cam.ac.uk/~pes20/weakmemory/#PA
	- <http://www.cl.cam.ac.uk/~pes20/papers/topics.html#Power_and_ARM>
- RMEM
	- a tool for exploring the relaxed-memory concurrency behaviour allowed by the ARM and IBM POWER architectures; it also has experimental support for x86-TSO and a candidate RISC-V model
	- help page: http://www.cl.cam.ac.uk/~sf502/regressions/rmem/help.html
	- web interface: http://www.cl.cam.ac.uk/users/pes20/rmem/
- Simplifying ARM Concurrency: Multicopy-atomic Axiomatic and Operational Models for ARMv8
	- POPL 2018 - https://www.youtube.com/watch?v=v9uygT1d0xY
	- Christopher Pulte, Shaked Flur, Will Deacon, Jon French, Susmit Sarkar, Peter Sewell
	- http://www.cl.cam.ac.uk/%7Epes20/armv8-mca/
	- http://www.cl.cam.ac.uk/%7Epes20/armv8-mca/armv8-mca-draft.pdf
- The ARMv8 Application Level Memory Model
	- https://developer.arm.com/architectures/cpu-architecture/a-profile/memory-model-tool
	- Herd - http://diy.inria.fr/www/?record=aarch64
	- [ARMv8 ARM](https://developer.arm.com/docs/ddi0487/latest/arm-architecture-reference-manual-armv8-for-armv8-a-architecture-profile), section B2.3
	- How to use the Memory Model Tool
		- https://community.arm.com/developer/ip-products/processors/b/processors-ip-blog/posts/how-to-use-the-memory-model-tool
- The Semantics of Power and ARM Multiprocessor Machine Code
	- DAMP 09
	- J. Alglave, A. Fox, S. Isthiaq, M. Myreen, S. Sarkar, P. Sewell, F. Zappa Nardelli
	- http://www.di.ens.fr/~zappa/readings/damp09.pdf
- The Semantics of Power and ARM Multiprocessor Programs
	- http://www.cl.cam.ac.uk/~pes20/weakmemory/index4.html

## Formalization, Specification, Verification

- A Trustworthy Monadic Formalization of the ARMv7 Instruction Set Architecture
	- Interactive Theorem Proving (ITP), 2010
	- Anthony Fox and Magnus O. Myreen
	- https://www.cl.cam.ac.uk/~mom22/itp10-armv7.pdf
- Alastair Reid's
	- Blog Posts - https://alastairreid.github.io/
	- Papers: https://alastairreid.github.io/alastairreid.github.io/papers/
	- 2020-01-01 - Using ASLi with Arm's v8.6-A ISA specification - https://alastairreid.github.io/using-asli/
	- 2019-02-17 - Generating multiple solutions with SMT - https://alastairreid.github.io/tracing-smt3/
	- 2019-02-09 - Using SMT to check specifications for errors - https://alastairreid.github.io/tracing-smt2/
	- 2019-02-02 - Generating SMT from traces - https://alastairreid.github.io/tracing-smt/
	- 2017-12-24 - Bidirectional Assembly Syntax Specifications - https://alastairreid.github.io/bidirectional-assemblers/
	- 2017-09-24 - Formal validation of the Arm v8-M specification - https://alastairreid.github.io/validating-specs/
	- 2017-08-19 - Are natural language specifications useful? - https://alastairreid.github.io/natural-specs/
	- 2017-07-31 - Arm v8.3 Machine Readable Specification Released - <https://alastairreid.github.io/arm-v8_3/>
	- 2017-05-07 - ASL Lexical Syntax - https://alastairreid.github.io/asl-lexical-syntax/
	- 2017-04-29 - Dissecting ARM's Machine Readable Specification - https://alastairreid.github.io/dissecting-ARM-MRA/
	- 2017-04-20 - ARM Releases Machine Readable Architecture Specification - https://alastairreid.github.io/ARM-v8a-xml-release/
	- 2016-08-17 - ARM's Architecture Specification Language - <https://alastairreid.github.io/specification_languages/>
	- 2016-07-30 - Limitations of ISA-Formal - https://alastairreid.github.io/isa-formal-limitations/
	- 2016-07-26 - Verifying against the official ARM specification - https://alastairreid.github.io/using-armarm/
	- 2016-07-18 - Finding Bugs versus Proving Absence of Bugs - https://alastairreid.github.io/finding-bugs/
	- 2016-07-03 - Specification Terminology - https://alastairreid.github.io/spec-terminology/
- ARMv8-A System Semantics: Instruction Fetch in Relaxed Architectures
	- ESOP 2020: European Symposium on Programming
	- Ben Simner, Shaked Flur, Christopher Pulte, Alasdair Armstrong, Jean Pichon-Pharabod, Luc Maranget, Peter Sewell
	- https://www.cl.cam.ac.uk/~pes20/iflat/
- ASL Interpreter
	- Example implementation of Arm's Architecture Specification Language (ASL).
	- https://github.com/ARM-software/asl-interpreter
- End-to-End Verification of ARM Processors with ISA-Formal
	- CAV 2016
	- Alastair Reid, Rick Chen, Anastasios Deligiannis, David Gilday, David Hoyes, Will Keen, Ashan Pathirane, Owen Shepherd, Peter Vrabel, Ali Zaidi
	- <https://alastairreid.github.io/papers/CAV_16/>
- Formal Semantics Extraction from Natural Language Specifications for ARM
	- FM 2019: 23rd International Symposium on Formal Methods
	- Anh V. Vu and Mizuhito Ogawa
	- https://www.cl.cam.ac.uk/~vv301/papers/fm19.pdf
	- Corana: Dynamic Symbolic Execution Engine for ARM Cortex-M
		- https://github.com/anhvvcs/corana
	- Formal Semantics Extraction from Natural Language Specifications for ARM
		- 2018 Master’s Thesis; Viet Anh Vu
		- http://www.jaist.ac.jp/~mizuhito/masterthesis/VuVietAnh.pdf
- hs-arm: (Dis)assembler and analyzer generated from the machine-readable ARMv8.3-A specification
	- https://github.com/nspin/hs-arm
	- library for (dis)assembling and analyzing ARMv8.3-A code, part of which is generated from the MRAS.
	- implementation of ARM ASL (architecture specification language)
- ISA Semantics for ARMv8-A, RISC-V, and CHERI-MIPS
	- POPL 2019
	- Alasdair Armstrong, Thomas Bauereiss, Brian Campbell, Alastair Reid, Kathryn E. Gray, Robert M. Norton, Prashanth Mundkur, Mark Wassell, Jon French, Christopher Pulte, Shaked Flur, Ian Stark, Neel Krishnaswami, Peter Sewell
	- <https://alastairreid.github.io/papers/POPL_19/>
- L3: A Specification Language for Instruction Set Architectures
	- https://github.com/8l/L3
	- https://web.archive.org/https://www.cl.cam.ac.uk/~acjf3/l3/
- Low-level program verification under cached address translation
	- 2019 PhD Dissertation; Hira Taqdees Syeda
	- "In this thesis, we present a formal model of the memory management unit (MMU) in the interactive proof assistant Isabelle/HOL for the ARMv7-A architecture which includes the TLB, its maintenance operations, and its derived properties. We integrate this specification into the Cambridge ARM model. We derive sufficient conditions for TLB consistency, and we abstract away the functional details of the MMU using data refinement for simpler reasoning about executions in the presence of cached address translation, including complete and partial walks."
	- <https://www.unsworks.unsw.edu.au/permalink/f/a5fmj0/unsworks_60079>
	- http://unsworks.unsw.edu.au/fapi/datastream/unsworks:60079/SOURCE02?view=true
- Renee: ARMv8 binary verification project
	- The Renee project is investigating the formalization of ARMv8 instruction semantics and reasoning and verification of ARMv8 binaries including their security properties.
	- https://ssrg-vt.github.io/Renee/
- sail-arm: Sail version of the ARMv8.5-A ISA definition
	- https://github.com/rems-project/sail-arm
- Scapula: Compare ARM CPUs Against ARM's Machine Parsable Architecture Reference Manual
	- tools for performing testing and verification of ARM CPUs against a machine parsable version of the ARMv8-A Architecture Reference Manual
	- https://github.com/ainfosec/scapula
		- Scapula: An Open-Source Toolkit For Model-Based Fuzzing and Verification of ARM CPUs
			- HITB+ CyberWeek 2019; Jared Wright
			- https://www.youtube.com/watch?v=v8SYv3GP3cs
- Trustworthy Specifications of ARM v8-A and v8-M System Level Architecture
	- FMCAD 2016
	- Alastair Reid
	- <https://alastairreid.github.io/papers/FMCAD_16/>
	- https://alastairreid.github.io/papers/fmcad2016-trustworthy.pdf
	- https://alastairreid.github.io/alastairreid.github.io/papers/fmcad2016-trustworthy-slides.pdf
- Weak Persistency Semantics from the Ground Up: Formalising the Persistency Semantics of ARMv8 and Transactional Models
	- OOPSLA 2019
	- Azalea Raad, John Wickerson, Viktor Vafeadis
	- "PARMv8 persistency model, formalising the persistency semantics of the ARMv8 architecture for the first time"
	- http://www.soundandcomplete.org/papers/OOPSLA2019/PARM/PARM-OOPSLA-2019.pdf
	- http://www.soundandcomplete.org/papers/OOPSLA2019/PARM/PARM-OOPSLA-2019-Talk.pdf
	- https://plv.mpi-sws.org/pmem/
- Who Guards the Guards? Formal Validation of the Arm v8-M Architecture Specification
	- SPLASH 2017 OOPSLA
	- Alastair Reid
	- Paper: https://alastairreid.github.io/papers/oopsla2017-whoguardstheguards.pdf
	- Post: https://alastairreid.github.io/validating-specs/
	- Slides: https://alastairreid.github.io/papers/oopsla2017-whoguardstheguards-slides.pdf

## Instruction Set Architecture

- ARM Assembly Language Programming - Pete Cockerell (historical)
	- http://www.peter-cockerell.net/aalp/
- ARMv8 A64 Quick Reference
	- Instruction Set Quick Reference Sheets: https://github.com/flynd/asmsheets
		- https://github.com/flynd/asmsheets/blob/master/aarch32.tex
		- https://github.com/flynd/asmsheets/blob/master/aarch64.tex
		- PDF: https://courses.cs.washington.edu/courses/cse469/18wi/Materials/arm64.pdf
- Exploring the Arm dot product instructions - https://community.arm.com/tools/b/blog/posts/exploring-the-arm-dot-product-instructions
- Introduction to Computer Organization: ARM Assembly Language Using the Raspberry Pi
	- http://bob.cs.sonoma.edu/IntroCompOrg-RPi/intro-co-rpi.html
- Learn the Architecture
	- https://developer.arm.com/architectures/learn-the-architecture
- REPICA: Rewriting Position Independent Code of ARM
	- IEEE Access 6 (2018)
	- Dongsoo Ha, Wenhui Jin, Heekuck Oh
	- https://doi.org/10.1109/access.2018.2868411

### Encoding, Shellcode

- Alphanumeric ARM Shellcode
	- March 15, 2018
	- https://vishnudevtj.github.io/notes/arm-alphanumeric-shellcode
- Alphanumeric RISC ARM Shellcode
	- Phrack Magazine #66 (2009-11-06)
	- Yves Younan, Pieter Philippaerts
	- http://www.phrack.org/archives/issues/66/12.txt
	- http://www.phrack.org/issues/66/12.html#article
- Alphanumeric Shellcode Generator for ARM Architecture
	- SPACE 2013: Security, Privacy, and Applied Cryptography Engineering
	- Pratik Kumar, Nagendra Chowdary, Anish Mathuria
	- <https://link.springer.com/chapter/10.1007/978-3-642-41224-0_3>
- ARM Assembly and Shellcode Basics
	- 44CON 2017; Saumil Shah
	- https://www.youtube.com/watch?v=BhjJBuX0YCU
- ARM immediate value encoding - 2014 - Alisdair McDiarmid
	- https://alisdair.mcdiarmid.org/arm-immediate-value-encoding/
- ARM Shellcode - Azeria Labs
	- Code: https://github.com/azeria-labs/ARM-assembly-examples
	- Introduction to Writing ARM Shellcode - https://azeria-labs.com/writing-arm-shellcode/
	- TCP Bind Shell (ARM 32-bit) - https://azeria-labs.com/tcp-bind-shell-in-assembly-arm-32-bit/
	- TCP Reverse Shell (ARM 32-bit) - https://azeria-labs.com/tcp-reverse-shell-in-assembly-arm-32-bit/
	- Process Memory and Memory Corruptions - https://azeria-labs.com/process-memory-and-memory-corruption/
	- Stack Overflow Challenges - https://azeria-labs.com/part-3-stack-overflow-challenges/
	- Process Continuation Shellcode - https://azeria-labs.com/process-continuation-shellcode/
	- Heap Exploitation Part 1: Understanding the Glibc Heap Implementation - https://azeria-labs.com/heap-exploitation-part-1-understanding-the-glibc-heap-implementation/
- ARM shellcode and exploit development
	- BSidesMunich 2018 Workshop; Andrea Sindoni
	- https://github.com/invictus1306/Workshop-BSidesMunich2018
	- <https://github.com/invictus1306/Workshop-BSidesMunich2018/blob/master/workshop_slides.pdf>
- ARMv8 Shellcodes from 'A' to 'Z'
	- ISPEC 2016
	- Hadrien Barral, Houda Ferradi, Rémi Géraud, Georges-Axel Jaloyan, David Naccache
	- https://arxiv.org/abs/1608.03415
- Encoding of immediate values on AArch64 - 2017 - Dominik Inführ
	- https://dinfuehr.github.io/blog/encoding-of-immediate-values-on-aarch64/
- Exploring New Depths of Threat Hunting ...or How to Write ARM Shellcode in Six Minutes
	- Security Analysts Summit (SAS) 2018
	- https://www.youtube.com/watch?v=DGJZBDlhIGU
	- https://azeria-labs.com/downloads/SAS-v1.0-Azeria.pdf
- Filter-resistant Code Injection on ARM
	- CCS 2009
	- Yves Younan, Pieter Philippaerts, Frank Piessens, Wouter Joosen, Sven Lachmund, Thomas Walter
	- <http://amnesia.gtisc.gatech.edu/~moyix/CCS_09/docs/p11.pdf>
- Make ARM Shellcode Great Again
	- Saumil Shah
	- Hack.lu 2018 - https://www.youtube.com/watch?v=9tx293lbGuc
	- 44CON 2018 - https://www.youtube.com/watch?v=pkhla6_2Kl0
- Shellcode: Encryption Algorithms in ARM Assembly
	- https://modexp.wordpress.com/2018/02/04/arm-crypto/
	- https://github.com/odzhan/shellcode

### A-profile

* BFloat16 extensions for Armv8-A
	- <https://community.arm.com/developer/ip-products/processors/b/ml-ip-blog/posts/bfloat16-processing-for-neural-networks-on-armv8_2d00_a>

### M-profile

- A Tourist's Guide to the ARM Cortex M3
	- BSides Knoxville 2020
	- Travis Goodspeed and Ryan Speers
	- https://www.youtube.com/watch?v=ilNhCW8ShlY
- A Tourist’s Phrasebook for Reversing Embedded ARM in the Dialect of the Cortex M Series
	- PoC||GTFO Issue 0x11 March 2016
	- Travis Goodspeed and Ryan Speers
	- https://www.riverloopsecurity.com/projects/pocgtfo_tourist_armcortexm/
- Code-Generation for the Arm M-profile Vector Extension
	- 2019 LLVM Developers’ Meeting; Sjoerd Meijer, Sam Parker
	- https://www.youtube.com/watch?v=TUDWpAhLjBU
	- http://llvm.org/devmtg/2019-10/talk-abstracts.html#tech2
- Helium – Arm Developer
	- https://developer.arm.com/architectures/instruction-sets/simd-isas/helium
	- Helium Intrinsics
		- <https://developer.arm.com/architectures/instruction-sets/intrinsics/#f:@navigationhierarchiessimdisa=[Helium]>
	- Helium Programmer's Guide
		- https://developer.arm.com/architectures/instruction-sets/simd-isas/helium/helium-programmers-guide
- Making Helium
	- Why not just add Neon? (1/4) - https://community.arm.com/arm-research/b/articles/posts/making-helium-why-not-just-add-neon
	- Sudoku, registers and rabbits (2/4) - https://community.arm.com/developer/research/b/articles/posts/making-helium-sudoku-registers-and-rabbits
	- Going around in circles (3/4) - https://community.arm.com/developer/research/b/articles/posts/making-helium-going-around-in-circles
	- Bringing Amdahl's law to heel (4/4) - https://community.arm.com/developer/research/b/articles/posts/making-helium-bringing-amdahl-s-law-to-heel
- Profiling Firmware on Cortex-M
	- https://interrupt.memfault.com/blog/profiling-firmware-on-cortex-m

## Performance

- An Instruction Level Energy Characterization of ARM Processors
	- 2015 Technical Report (FORTH-ICS/TR-450); Evangelos Vasilakis
	- https://www.ics.forth.gr/carv/greenvm/files/tr450.pdf
- CoreSight, Perf and the OpenCSD Library
	- https://www.linaro.org/blog/coresight-perf-and-the-opencsd-library/
- Linaro Wiki - perf
	- https://web.archive.org/https://wiki.linaro.org/KenWerner/Sandbox/perf
	- https://web.archive.org/https://wiki.linaro.org/Platform/DevPlatform/Tools/Perf
- On-Target Trace Using the CoreSight Access Library
	- https://developer.arm.com/products/software-development-tools/ds-5-development-studio/resources/tutorials/on-target-trace-using-the-coresight-access-library
- OpenCSD HOWTO - using the library with perf
	- https://github.com/Linaro/OpenCSD/blob/master/HOWTO.md
- Statistical Profiling Extension for ARMv8-A
	- https://community.arm.com/processors/b/blog/posts/statistical-profiling-extension-for-armv8-a
- Using Perf and its friend eBPF on Arm platform
	- Linaro Connect San Diego 2019; Leo Yan
	- https://connect.linaro.org/resources/san19/san19-223/

### Performance: Numerics

* ARM Floating Point 2019: Latency, Area, Power
	+ 2019 IEEE 26th Symposium on Computer Arithmetic (ARITH)
	+ David Lutz
	+ https://doi.org/10.1109/ARITH.2019.00025
* LLVM and the Automatic Vectorization of Loops Invoking Math Routines: `-fsimdmath`
	+ 2018 IEEE/ACM 5th Workshop on the LLVM Compiler Infrastructure in HPC (LLVM-HPC)
	+ Francesco Petrogalli, Paul Walker
	+ <https://sc18.supercomputing.org/proceedings/workshops/workshop_files/ws_llvmf106s2-file1.pdf>

## Security

* ARM Lab Environment - https://www.vulnhub.com/series/arm-lab,145/
* ARM Return Oriented Programming (ROP) - Billy Ellis
	+ Cheatsheet - https://twitter.com/bellis1000/status/929713826106396673
	+ https://web.archive.org/https://billy-ellis.github.io/armintro.html
	+ https://web.archive.org/https://billy-ellis.github.io/rop1.html
	+ https://web.archive.org/https://billy-ellis.github.io/rop2.html
	+ https://web.archive.org/https://billy-ellis.github.io/rop3.html
* Cache Speculation Side-channels
	+ Richard Grisenthwaite
	+ https://developer.arm.com/support/security-update
	+ Compiler support for mitigations - https://developer.arm.com/support/security-update/compiler-support-for-mitigations
	+ Speculation Barrier - https://github.com/ARM-software/speculation-barrier
* Damn Vulnerable ARM Router (DVAR)
	+ http://blog.exploitlab.net/2018/01/dvar-damn-vulnerable-arm-router.html
* Exploitation on ARM-based Systems
	+ Troopers18; Sascha Schirra, Ralf Schaefer
	+ <https://github.com/sashs/arm_exploitation>
* Micro-Architectural Power Simulator for Leakage Assessment of Cryptographic Software on ARM Cortex-M3 Processors
	+ Cryptology ePrint Archive: Report 2017/1253
	+ Yann Le Corre, Johann Großschädl, Daniel Dinu
	+ https://eprint.iacr.org/2017/1253
* NORAX: Enabling Execute-Only Memory for COTS Binaries on AArch64
	+ Security and Privacy (S&P) 2017
	+ Yaohui Chen, Dongli Zhang, Ruowen Wang, Rui Qiao, Ahmed Azab, Long Lu, Hayawardh Vijayakumar, Wenbo Shen
	+ http://seclab.cs.sunysb.edu/seclab/pubs/norax.pdf
* RevARM: A Platform-Agnostic ARM Binary Rewriter for Security Applications
	+ Annual Computer Security Applications Conference (ACSAC) 2017
	+ T. Kim, C. Kim, H. Choi, Y. Kwon, B. Saltaformaggio, X. Zhang, D. Xu
	+ <https://saltaformaggio.ece.gatech.edu/publications/ACSAC_17.pdf>
	+ <https://www.acsac.org/2017/openconf/modules/request.php?module=oc_program&action=summary.php&id=201>
	+ <https://www.researchgate.net/publication/321506390_RevARM_A_Platform-Agnostic_ARM_Binary_Rewriter_for_Security_Applications>
* Safe and Efficient Implementation of a Security System on ARM using Intra-level Privilege Separation
	- ACM Transactions on Privacy and Security (TOPS) 22(2) 2019
	- Donghyun Kwon, Hayoon Yi, Yeongpil Cho, Yunheung Paek
	- https://doi.org/10.1145/3309698
* Smashing the ARM Stack: ARM Exploitation Part 1
	+ https://web.archive.org/https://www.merckedsecurity.com/blog/smashing-the-arm-stack-part-1
* TCP Bind Shell in Assembly (ARM 32-bit)
	+ https://azeria-labs.com/tcp-bind-shell-in-assembly-arm-32-bit/
* Understanding the Security of ARM Debugging Features
	+ Security & Privacy (S&P) 2019
	+ Zhenyu Ning, Fengwei Zhang
	+ https://compass.cs.wayne.edu/nailgun/
	+ http://webpages.eng.wayne.edu/~fy8421/paper/nailgun-sp19.pdf

### Memory Tagging Extension (MTE)

- ARM Memory Tagging Extension and How It Improves C/C++ Memory Safety
	- USENIX ;login: Vol. 44, No. 2 Summer 2019
	- Kostya Serebryany
	- https://www.usenix.org/publications/login/summer2019/serebryany
	- <https://github.com/google/sanitizers/blob/master/hwaddress-sanitizer/login_summer19_03_serebryany.pdf>
- Hardware-assisted AddressSanitizer (HWASAN)
	- Design Documentation - https://clang.llvm.org/docs/HardwareAssistedAddressSanitizerDesign.html
	- Talks - https://github.com/google/sanitizers/tree/master/hwaddress-sanitizer
		- Hardware Memory Tagging to make C/C++ memory safe(r)
			- iSecCon 2018; Kostya Serebryany
			- https://github.com/google/sanitizers/blob/master/hwaddress-sanitizer/MTE-iSecCon-2018.pdf
		- Towards a fully sanitizable C++, with the help from hardware
			- PLEMM 2019; Kostya Serebryany
			- https://github.com/google/sanitizers/blob/master/hwaddress-sanitizer/plemm-2019.pdf
- Memory Tagging and how it improves C/C++ memory safety
	- 2018
	- Kostya Serebryany, Evgenii Stepanov, Aleksey Shlyapnikov, Vlad Tsyrklevich, Dmitry Vyukov
	- https://arxiv.org/abs/1802.09517
	- https://research.google/pubs/pub46800/
- Memory Tagging, how it improves C++ memory safety, and what does it mean for compiler optimizations
	- 2018 LLVM Developers’ Meeting
	- Kostya Serebryany, Evgenii Stepanov, Vlad Tsyrklevich
	- https://llvm.org/devmtg/2018-10/talk-abstracts.html#talk16
- scudo: Add initial memory tagging support
	- https://reviews.llvm.org/D70762
- Security analysis of memory tagging
	- 2020; Joe Bialek, Ken Johnson, Matt Miller, Tony Chen
	- https://github.com/microsoft/MSRC-Security-Research/blob/master/papers/2020/Security%20analysis%20of%20memory%20tagging.pdf

### Pointer Authentication

- arm64e: An ABI for Pointer Authentication
	- 2019 LLVM Developers’ Meeting; Ahmed Bougacha, John McCall
	- https://www.youtube.com/watch?v=C1nZvpEBfYA
	- http://llvm.org/devmtg/2019-10/talk-abstracts.html#tech15
	- https://github.com/apple/llvm-project/blob/apple/main/clang/docs/PointerAuthentication.rst
- Examining Pointer Authentication on the iPhone XS
	- 2019; Brandon Azad
	- https://googleprojectzero.blogspot.com/2019/02/examining-pointer-authentication-on.html
- LLVM-based Implementations
	- [llvm-dev] [RFC] Pointer authentication for arm64e
		- http://lists.llvm.org/pipermail/llvm-dev/2019-October/136091.html
	- [LLVM and Clang] Upstream arm64e and Pointer Authentication support #14
		- https://github.com/apple/llvm-project/pull/14
	- Add arm64e and pointer authentication support for Swift #30112
		- https://github.com/apple/swift/pull/30112
- PAC it up: Towards Pointer Integrity using ARM Pointer Authentication
	- USENIX Security 2019
	- Hans Liljestrand, Thomas Nyman, Kui Wang, Carlos Chinea Perez, Jan-Erik Ekberg, N. Asokan
	- https://www.usenix.org/conference/usenixsecurity19/presentation/liljestrand
	- https://github.com/pointer-authentication
- Pointer Authentication on ARMv8.3: Design and Analysis of the New Software Security Instructions
	- 2017
	- https://www.qualcomm.com/documents/whitepaper-pointer-authentication-armv83
	- https://www.qualcomm.com/media/documents/files/whitepaper-pointer-authentication-on-armv8-3.pdf
	- https://www.qualcomm.com/news/onq/2017/01/10/qualcomm-releases-whitepaper-detailing-pointer-authentication-armv83
- Raising the Bar: New Hardware Primitives for Exploit Mitigations
	- BlueHat v17 (2017); Rob Turner
	- ARMv8.3 pointer authentication
	- https://www.youtube.com/watch?v=PYe8W33lbAQ
	- https://www.slideshare.net/MSbluehat/raising-the-bar-new-hardware-primitives-for-exploit-mitigations-83686492

### TrustZone

- A Deep Dive Into Samsung's TrustZone
	- Part 1: Detailed overview of Samsung's TrustZone components
		- https://blog.quarkslab.com/a-deep-dive-into-samsungs-trustzone-part-1.html
	- Part 2: Tools development for reverse-engineering and vulnerability research
		- https://blog.quarkslab.com/a-deep-dive-into-samsungs-trustzone-part-2.html
	- Part 3: Vulnerability exploitation to reach code execution in EL3 on a Samsung device
		- https://blog.quarkslab.com/a-deep-dive-into-samsungs-trustzone-part-3.html
- Attacking the ARM's TrustZone
	- https://blog.quarkslab.com/attacking-the-arms-trustzone.html
- Azeria Labs
	- TrustZone Research
		- Trusted Execution Environments and Arm TrustZone
			- https://azeria-labs.com/trusted-execution-environments-tee-and-trustzone/
		- Trustonic’s Kinibi TEE Implementation
			- https://azeria-labs.com/trustonics-kinibi-tee-implementation/
- Breaking Samsung's ARM TrustZone
	- Black Hat USA 2019
	- Maxime Peterlin, Alexandre Adamski, Joffrey Guilbon
	- https://www.blackhat.com/us-19/briefings/schedule/#breaking-samsungs-arm-trustzone-14932
	- https://www.youtube.com/watch?v=uXH5LJGRwXI
- Cachegrab: a tool designed to help perform and visualize trace-driven cache attacks against software in the secure world of TrustZone-enabled ARMv8 cores
	- https://github.com/nccgroup/cachegrab
	- https://www.nccgroup.trust/us/about-us/newsroom-and-events/blog/2017/december/34C3-Tool-Release-Cachegrab/
- Demystifying Arm TrustZone: A Comprehensive Survey
	- ACM Computing Surveys 51(6) 2019
	- Sandro Pinto and Nuno Santos
	- https://www.gsd.inesc-id.pt/~nsantos/papers/pinto_acsur19.pdf
- Hardware-assisted Transparent Tracing and Debugging on ARM
	- IEEE Transactions on Information Forensics & Security (TIFS) 2018
	- Zhenyu Ning, Fengwei Zhang
	- https://doi.org/10.1109/TIFS.2018.2883027
	- http://webpages.eng.wayne.edu/~fy8421/paper/ninja-tifs19.pdf
- Introduction to Trusted Execution Environment: ARM's TrustZone
	- https://blog.quarkslab.com/introduction-to-trusted-execution-environment-arms-trustzone.html
- Introduction to Trusted Execution Environment and ARM's TrustZone
	- https://embeddedbits.org/introduction-to-trusted-execution-environment-tee-arm-trustzone/
- Ninja: Towards Transparent Tracing and Debugging on ARM
	- USENIX Security 2017
	- Zhenyu Ning, Fengwei Zhang
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/ning
- PARTEMU: Enabling Dynamic Analysis of Real-World TrustZone Software Using Emulation
	- USENIX Security 2020
	- Lee Harrison, Hayawardh Vjayakumar, Rohan Padhye, Koushik Sen, Michael Grace
	- https://people.eecs.berkeley.edu/~rohanpadhye/files/partemu-usenixsec20.pdf
- Running Trusted Firmware-A on gem5
	- https://community.arm.com/developer/research/b/articles/posts/running-trusted-firmware-a-on-gem5
- SoK: Understanding the Prevailing Security Vulnerabilities in TrustZone-assisted TEE Systems
	- IEEE Symposium on Security and Privacy (S&P) 2020
	- David Cerdeira, Nuno Santos, Pedro Fonseca, Sandro Pinto
	- https://www.cs.purdue.edu/homes/pfonseca/papers/sp2020-tees.pdf
- TEE-reversing: A curated list of public TEE resources for learning how to reverse-engineer and achieve trusted code execution on ARM devices
	- https://github.com/enovella/TEE-reversing
- Verification of a Practical Hardware Security Architecture Through Static Information Flow Analysis (ARM TrustZone)
	- ASPLOS 2017
	- Andrew Ferraiuolo, Rui Xu, Danfeng Zhang, Andrew C. Myers, G. Edward Suh
	- http://www.cs.cornell.edu/andru/papers/trustzone/
- vTZ: Virtualizing ARM TrustZone
	- USENIX Security 2017
	- Zhichao Hua, Jinyu Gu, Yubin Xia, Haibo Chen, Binyu Zang, and Haibing Guan
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/hua

## Simulation

* Simulation of ARM and x86 microprocessors using in-order and out-of-order CPU models with Gem5 simulator
	+ International Conference on Electrical and Electronic Engineering (ICEEE) 2018
	+ Anas Ahmad Abudaqa, Talal M. Al-Kharoubi, Muhamed F. Mudawar, Armin Kobilica
	+ https://ieeexplore.ieee.org/document/8391354/
* Simulation of 64-bit ARM Systems: Implementation, Validation and Design Space Exploration
	+ 2018 MSc dissertation
	+ Juan Miguel de Haro Ruiz
	+ https://upcommons.upc.edu/handle/2117/127677

## Virtualization

- ARM Virtualization: Performance and Architectural Implications
	- ACM SIGOPS Operating Systems Review 52(1) 2018
	- Christoffer Dall, Shih-Wei Li, Jin Tack Lim, and Jason Nieh
	- https://dl.acm.org/citation.cfm?id=3273987
- Hiding in the Shadows: Empowering ARM for Stealthy Virtual Machine Introspection
	- Annual Computer Security Applications Conference (ACSAC) 2018
	- Sergej Proskurin, Tamas Lengyel, Marius Momeu, Claudia Eckert, Apostolis Zarras
	- https://dl.acm.org/citation.cfm?id=3274698
	- https://www.sec.in.tum.de/i20/publications/hiding-in-the-shadows-empowering-arm-for-stealthy-virtual-machine-introspection
	- DRAKVUF on ARM
		- https://github.com/drakvuf-on-arm
- Hypervisor Necromancy; Reanimating Kernel Protectors, or On emulating hypervisors; a Samsung RKP case study
	- Phrack 2020-02-14; Aris Thallas
	- http://phrack.org/papers/emulating_hypervisors_samsung_rkp.html
- Optimizing the Design and Implementation of the Linux ARM Hypervisor
	- 2017 USENIX Annual Technical Conference
	- Christoffer Dall, Shih-Wei Li, Jason Nieh
	- https://www.usenix.org/conference/atc17/technical-sessions/presentation/dall
- The Design, Implementation, and Evaluation of Software and Architectural Support for ARM Virtualization
	- 2018 PhD Thesis; [Christoffer Dall](http://www.cs.columbia.edu/~cdall/)
	- https://academiccommons.columbia.edu/catalog/ac:t1g1jwstss

---

# References

- ARM Architecture Documentation
	- A-Profile: The Applications profile - https://developer.arm.com/products/architecture/a-profile/docs
		- A-Profile Architectures - Exploration Tools - https://developer.arm.com/products/architecture/a-profile/exploration-tools
		- ARM Architecture Reference Manual ARMv8, for ARMv8-A architecture profile
			- https://developer.arm.com/docs/ddi0487/latest/arm-architecture-reference-manual-armv8-for-armv8-a-architecture-profile
		- Programmer’s Guide for ARMv8-A: ARM® Cortex-A Series, Version: 1.0
			- <http://infocenter.arm.com/help/topic/com.arm.doc.den0024a/DEN0024A_v8_architecture_PG.pdf>
	- R-Profile: The Real-Time profile - https://developer.arm.com/products/architecture/r-profile/docs
	- M-Profile: The Microcontroller profile - https://developer.arm.com/products/architecture/m-profile/docs
- Application Binary Interface for the Arm® Architecture
	- https://github.com/ARM-software/abi-aa
- ARM and Thumb-2 Instruction Set Quick Reference Card
	- <http://infocenter.arm.com/help/topic/com.arm.doc.qrc0001m/QRC0001_UAL.pdf>
- ARM Assembly Basics Cheatsheet - https://azeria-labs.com/assembly-basics-cheatsheet/
- ARM architecture documentation set - http://infocenter.arm.com/help/index.jsp?topic=/com.arm.doc.set.architecture/
- Arm A64 Instruction Set Architecture: Armv8-A - Base Instructions (alphabetic order)
	- https://developer.arm.com/docs/ddi0596/h/base-instructions-alphabetic-order
- asm.thi.ng - baremetal ARM coding resources - http://asm.thi.ng/
- Instruction Sets - https://developer.arm.com/products/architecture/instruction-sets
- The ARM Machinists Atlas
	- https://www.youtube.com/watch?v=PRaJQepIf44
	- https://xlogicx.net/ARM_Atlas.html
- Works on ARM newsletter - https://github.com/vielmetti/worksonarm-news

## References: Microarchitecture

- A-Profile
	- Cortex-A57 Software Optimization Guide
		- http://infocenter.arm.com/help/index.jsp?topic=/com.arm.doc.uan0015b/
		- https://developer.arm.com/docs/uan0015/latest/cortex-a57-software-optimization-guide-software-optimization-guide
		- PDF: <http://infocenter.arm.com/help/topic/com.arm.doc.uan0015b/Cortex_A57_Software_Optimization_Guide_external.pdf>
- Apple
	- Apple M1 CPU Microarchitectures Research by Dougall Johnson
		- Research on the Apple M1 CPU microarchitectures (Firestorm and Icestorm), with instruction tables describing throughput, latency, and uops for most instructions, and detailed experiments and measurements.
			- https://dougallj.github.io/applecpu/firestorm.html
			- https://github.com/dougallj/applecpu
		- Counting cycles and instructions on the Apple M1 processor
			- https://lemire.me/blog/2021/03/24/counting-cycles-and-instructions-on-the-apple-m1-processor/
		- Apple M1: Load and Store Queue Measurements
			- https://dougallj.wordpress.com/2021/04/08/apple-m1-load-and-store-queue-measurements/
- Fujitsu
	- Fujitsu A64FX - https://github.com/fujitsu/A64FX

## References: OS

- Linux
	- Linux Kernel Documentation
		- ARM: https://www.kernel.org/doc/Documentation/arm/
		- ARM64: https://www.kernel.org/doc/Documentation/arm64/
- macOS
	- Apple Silicon - Apple Developer Documentation
		- https://developer.apple.com/documentation/apple_silicon
- Windows
	- System call dispatching on Windows ARM64
		- https://gracefulbits.wordpress.com/2018/07/26/system-call-dispatching-for-windows-on-arm64/

## Intrinsics & SIMD

- Arm Intrinsics reference search engine
	- https://developer.arm.com/architectures/instruction-sets/intrinsics/
- Arm C Language Extensions (ACLE)
	- the source material for the ACLE specifications
	- https://github.com/ARM-software/acle
- ARC SIMD Built-in Functions - https://gcc.gnu.org/onlinedocs/gcc/ARC-SIMD-Built-in-Functions.html
- ARM Intrinsics - MSDN - Microsoft - https://docs.microsoft.com/en-us/cpp/intrinsics/arm-intrinsics
- SIMD ISAs – Arm Developer
	- https://developer.arm.com/architectures/instruction-sets/simd-isas
- Vectorization cost modeling for NEON, AVX, and SVE
	- Performance Evaluation 140–141 (2020)
	- Angela Pohl, Biagio Cosenza, Ben Juurlink
	- https://doi.org/10.1016/j.peva.2020.102106
	- http://www.cosenza.eu/papers/PohlPEJ20.pdf

### Neon

- Neon – Arm Developer
	- https://developer.arm.com/architectures/instruction-sets/simd-isas/neon
	- Neon Programmer's Guide for Armv8-A
		- https://developer.arm.com/architectures/instruction-sets/simd-isas/neon/neon-programmers-guide-for-armv8-a
- Neon Intrinsics - <https://developer.arm.com/architectures/instruction-sets/intrinsics/#f:@navigationhierarchiessimdisa=[Neon]>
- Neon intrinsics guide - https://github.com/thenifty/neon-guide
- Neon Programmer’s Guide - http://infocenter.arm.com/help/index.jsp?topic=/com.arm.doc.den0018a/
- Porting and Optimizing HPC Applications for Arm Documentation
	- https://developer.arm.com/docs/101725/0200
	- Coding for Neon
		- https://developer.arm.com/docs/101725/0200/coding-for-neontm
- ARM Neon Intrinsics - https://gcc.gnu.org/onlinedocs/gcc-4.9.4/gcc/ARM-NEON-Intrinsics.html#ARM-NEON-Intrinsics
- Branch Free - Geoff Langdale
	- An Intel Programmer Jumps Over the Wall: First Impressions of ARM SIMD Programming
		- https://branchfree.org/2019/03/26/an-intel-programmer-jumps-over-the-wall-first-impressions-of-arm-simd-programming/
	- Fitting My Head Through The ARM Holes or: Two Sequences to Substitute for the Missing PMOVMSKB Instruction on ARM NEON
		- https://branchfree.org/2019/04/01/fitting-my-head-through-the-arm-holes-or-two-sequences-to-substitute-for-the-missing-pmovmskb-instruction-on-arm-neon/
- Control Flow Vectorization for ARM NEON
	- International Workshop on Software and Compilers for Embedded Systems (SCOPES) 2018
	- Angela Pohl, Biagio Cosenza, Ben Juurlink
	- http://www.cosenza.eu/papers/PohlSCOPES18.pdf
- Porting Intel Intrinsics to Arm Neon Intrinsics
	- https://www.codeproject.com/Articles/5301747/Porting-Intel-Intrinsics-to-Arm-Neon-Intrinsics

### Scalable Vector Extension (SVE)

- Arm Intrinsics reference search engine
	- SVE: <https://developer.arm.com/architectures/instruction-sets/intrinsics/#f:@navigationhierarchiessimdisa=[sve]>
	- SVE2: <https://developer.arm.com/architectures/instruction-sets/intrinsics/#f:@navigationhierarchiessimdisa=[sve2]>
	- SVE & SVE2: <https://developer.arm.com/architectures/instruction-sets/intrinsics/#f:@navigationhierarchiessimdisa=[sve,sve2]>
- Arm HPC tools for SVE
	- https://developer.arm.com/tools-and-software/server-and-hpc/compile/arm-instruction-emulator/resources/tutorials/sve
- Arm SVE Tools Training
	- https://gitlab.com/arm-hpc/training/arm-sve-tools
- Asvie: A Timing-Agnostic SVE Optimization Methodology
	- Methodology for ArmIE SVE
		- <https://github.com/ARM-software/Methodology_for_ArmIE_SVE>
	- Asvie: A Timing-Agnostic SVE Optimization Methodology
		- Programming and Performance Visualization Tools (ProTools) 2019
		- Miguel Tairum Cruz, Daniel Ruiz, Roxana Rusitoru
		- https://doi.org/10.1109/ProTools49597.2019.00007
- Porting and Optimizing HPC Applications for Arm SVE Documentation
	- https://developer.arm.com/documentation/101726
- How to use LLDB to debug SVE enabled applications
	- https://www.linaro.org/blog/how-to-use-lldb-to-debug-sve-enabled-applications/
- Introduction to Arm SVE
	- HiPEAC 2021; John Linford
	- https://www.youtube.com/watch?v=mVdeE2Qbm2I
	- https://montblanc-project.eu/wp-content/uploads/2021/01/MB2020-HiPEAC_2021-JLinford-SVE.pdf
- Mastering the Arm HPC ecosystem
	- CEA-RIKEN HPC school (June 2019)
	- https://indico.math.cnrs.fr/event/4705/
- Scalable Vector Extension (SVE)
	- https://community.arm.com/processors/b/blog/posts/technology-update-the-scalable-vector-extension-sve-for-the-armv8-a-architecture
	- https://developer.arm.com/hpc/a-sneak-peek-into-sve-and-vla-programming
	- ARMv8-A Next Generation Vector Architecture for HPC
		- Hot Chips 28 (2016)
		- Nigel Stephens
		- https://youtu.be/egE-VKoF4ZI?t=1h9m8s
		- <https://community.arm.com/cfs-file/__key/telligent-evolution-components-attachments/01-2142-00-00-00-01-20-49/ARMv8_2D00_A-SVE-technology-Hot-Chips-v12.pdf>
- Scalable Vector Extension support for AArch64 Linux
	- https://www.kernel.org/doc/html/latest/arm64/sve.html
- SVE Programming Examples
	- https://developer.arm.com/documentation/dai0548/latest/
- The ARM Scalable Vector Extension
	- IEEE Micro, March 2017
	- Nigel Stephens, Stuart Biles, Matthias Boettcher, Jacob Eapen, Mbou Eyole, Giacomo Gabrielli, Matt Horsnell, Grigorios Magklis, Alejandro Martinez, Nathanael Premillieu, Alastair Reid, Alejandro Rico, Paul Walker
	- Preprint: https://alastairreid.github.io/papers/sve-ieee-micro-2017.pdf
	- http://dx.doi.org/10.1109/MM.2017.35

#### Scalable Vector Extension (SVE): Applications

- Evaluating the Effectiveness of a Vector-Length-Agnostic Instruction Set
	- Euro-Par 2020: Parallel Processing
	- Andrei Poenaru, Simon McIntosh-Smith
	- https://doi.org/10.1007/978-3-030-57675-2_7
	- https://www.youtube.com/watch?v=oX_SD43qrWA
	- Emulated SVE Analysis Tools
		- Scripts used to characterise performance of applications using the Arm Instruction Emulator (ArmIE)
		- https://github.com/UoB-HPC/sve-analysis-tools/tree/euro-par-2020
- FFTE on SVE: SPIRAL-Generated Kernels
	- International Conference on High Performance Computing in Asia-Pacific Region (HPC Asia) 2020
	- Daisuke Takahashi and Franz Franchetti
	- https://dl.acm.org/doi/abs/10.1145/3368474.3368488
	- https://www.spiral.net/doc/papers/ffte-spiral.pdf
- Using Arm Scalable Vector Extension to Optimize OPEN MPI
	- Cluster, Cloud and Internet Computing (CCGRID) 2020
	- Zhong, Dong, Pavel Shamis, Qinglei Cao, George Bosilca, Shinji Sumimoto, Kenichi Miura, Jack Dongarra
	- https://ieeexplore.ieee.org/document/9139622
	- https://www.icl.utk.edu/publications/using-arm-scalable-vector-extension-optimize-open-mpi
- Using Arm’s scalable vector extension on stencil codes
	- The Journal of Supercomputing (2019)
	- Armejach, Adrià, Helena Caminal, Juan M. Cebrian, Rubén Langarita, Rekai González-Alberquilla, Chris Adeniyi-Jones, Mateo Valero, Marc Casas, Miquel Moretó
	- https://doi.org/10.1007/s11227-019-02842-5

#### Scalable Vector Extension (SVE): LLVM Implementation

* Road to SVE enablement in LLDB
	- Linaro Connect San Diego 2019; Omair Javaid
	- https://connect.linaro.org/resources/san19/san19-204/
* Scalable Vectorization for LLVM
	- 2016 LLVM Developers’ Meeting; Amara Emerson & Graham Hunter, ARM
	- https://www.youtube.com/watch?v=0up2hJk7k94
	- http://llvm.org/devmtg/2016-11/Slides/Emerson-ScalableVectorizationinLLVMIR.pdf
* SVE/SVE2 Patches on Phabricator
	- https://docs.google.com/document/d/1ph1l1KhrrHgBlrKeEnuoIPrVO9jTjHvcwUlz61QWNMA

## References: Toolchains

* ARM Product Manuals - Keil - <http://www.keil.com/support/man_arm.htm>
	+ armasm Assembler User Guide - http://www.keil.com/support/man/docs/armasm/
	+ armcc Compiler User Guide - http://www.keil.com/support/man/docs/armcc/
	+ armlink Linker User Guide - http://www.keil.com/support/man/docs/armlink/
	+ armclang Compiler Getting Started Guide - <http://www.keil.com/support/man/docs/armclang_intro/>
	+ armclang Compiler Reference Guide - <http://www.keil.com/support/man/docs/armclang_ref/>
* Demystifying ARM Floating Point Compiler Options - https://embeddedartistry.com/blog/2017/10/9/r1q7pksku2q3gww9rpqef0dnskphtc
* GNU Compiler Collection (GCC)
	+ AArch64 Options - https://gcc.gnu.org/onlinedocs/gcc/AArch64-Options.html
	+ ARM Options - https://gcc.gnu.org/onlinedocs/gcc/ARM-Options.html
	+ ARM C Language Extensions (ACLE) - <https://gcc.gnu.org/onlinedocs/gcc/ARM-C-Language-Extensions-_0028ACLE_0029.html>
	+ Target-Specific Builtins - https://gcc.gnu.org/onlinedocs/gcc/Target-Builtins.html#Target-Builtins
* Microsoft ARM Assembler Reference - https://docs.microsoft.com/en-us/cpp/assembler/arm/arm-assembler-reference

---

# Software

- Arm HPC Users Group - resources for end-users and developers deploying on Arm hardware.
	- https://gitlab.com/arm-hpc
- AMaCC (Another Mini ARM C Compiler) - Small C Compiler generating ELF executable for Arm architecture
	- https://github.com/jserv/amacc
- libopencm3: Open source ARM Cortex-M microcontroller library
	- http://libopencm3.org/
	- https://github.com/libopencm3/libopencm3
- mra_tools: Tools to process ARM's Machine Readable Architecture Specification
	- <https://github.com/alastairreid/mra_tools>

## Software: Assembly

- AZM - Live ARM Assembler and Syntax Checker
	- https://azeria-labs.com/azm/
- Lightening: Just-in-time code generation library derived from GNU Lightning
	- Lightening can generate code for the x86-64, i686, ARMv7, and AArch64 architectures.  It supports the calling conventions of MS Windows, GNU/Linux, and Mac OS.
	- https://gitlab.com/wingo/lightening
	- https://wingolog.org/archives/2019/05/24/lightening-run-time-code-generation
- Xbyak_aarch64: JIT assembler for AArch64 CPUs in C++
	- https://github.com/fujitsu/xbyak_aarch64
- Xbyak_translator_aarch64: A translator which generates JIT functions for ARMv8 with SVE from JIT functions for x86
	- https://github.com/fujitsu/xbyak_translator_aarch64
- VIXL: ARMv8 Runtime Code Generation Library
	- https://git.linaro.org/arm/vixl.git/about/
	- Programmatic assemblers to generate A64, A32 or T32 code at runtime. The assemblers abstract some of the constraints of each ISA; for example, most instructions support any immediate.
	- Disassemblers that can print any instruction emitted by the assemblers.
	- A simulator that can simulate any instruction emitted by the A64 assembler. The simulator allows generated code to be run on another architecture without the need for a full ISA model.

## Software: Binary Analysis

See also: [Readings: Binary Analysis](https://github.com/MattPD/cpplinks/blob/master/assembly.arm.md#readings-binary-analysis)

- MAMBO: A Low-Overhead Dynamic Binary Modification Tool for ARM
	- https://github.com/beehive-lab/mambo
	- Low Overhead Dynamic Binary Translation on ARM
		- PLDI 2017
		- Amanieu d'Antras, Cosmin Gorgovan, Jim Garside, Mikel Lujan
		- https://www.youtube.com/watch?v=FCf-DJ2m0FM
		- https://pldi17.sigplan.org/event/pldi-2017-papers-low-overhead-dynamic-binary-translation-on-arm
		- <https://www.research.manchester.ac.uk/portal/files/56078084/pldi_16.pdf>
	- Optimising Dynamic Binary Modification across ARM microarchitectures
		- 2017 Ph.D. Thesis; Cosmin Gorgovan
		- <http://apt.cs.manchester.ac.uk/publications/thesis/gorgovan17_phd.php>
		- https://www.escholar.manchester.ac.uk/api/datastream?publicationPid=uk-ac-man-scw:307942&datastreamId=FULL-TEXT.PDF
	- Optimising Dynamic Binary Modification Across ARM Microarchitectures
		- International Conference on Performance Engineering (ICPE) 2018
		- Cosmin Gorgovan, Amanieu d'Antras, Mikel Luján
		- https://dl.acm.org/citation.cfm?id=3184425
	- Dynamic Binary Instrumentation and Modification with MAMBO
		- HiPEAC 2018
		- <https://www.research.manchester.ac.uk/portal/files/65557332/cosmin_mambo_icpe2018.pdf>
		- <https://github.com/beehive-lab/mambo/releases/download/1/mambo_tutorial_hipeac_2018.pdf>
		- <https://www.dropbox.com/s/3pfg9eovj1y9cw9/mambo_tutorial_hipeac_2018.pdf?dl=0>
- mbed-os-linker-report: d3.js based ELF Linker Statistics
	- Post-processing of linker output to calculate and visualize memory usage for elf-sections
	- https://github.com/ARMmbed/mbed-os-linker-report
	- https://os.mbed.com/blog/entry/visualizing-linker-stats/

## Software: Concurrency

- PROGRESS64: a C library of scalable functions for concurrent programs, primarily focused on networking applications
	- https://github.com/ARM-software/progress64

## Software: Debugging, Tracing

* Coresight Access Library
	+ https://github.com/ARM-software/CSAL
	+ https://developer.arm.com/products/software-development-tools/ds-5-development-studio/resources/tutorials/on-target-trace-using-the-coresight-access-library
* OpenCSD - Open CoreSight Decoder library
	+ https://github.com/Linaro/OpenCSD
* ptm2human: ARM PTM (and ETMv4) trace to human-readable format
	+ ARM PTM decoder, and ARM ETM v4 decoder. ptm2human is a decoder for trace data outputted by Program Trace Macrocell (PTM) and Embedded Trace Macrocell (ETMv4).
	+ https://github.com/hwangcc23/ptm2human
* Statically compiled ARM binaries for debugging and runtime analysis
	+ https://github.com/therealsaumil/static-arm-bins/
* Troll
	+ A source level debugger for C programs running on ARM Cortex-M parts. Utilizes the *blackmagic* probe and the *Qt* framework
	+ https://github.com/stoyan-shopov/troll

## Software: Emulation, Simulation

- Arm Instruction Emulator (ArmIE)
	- https://developer.arm.com/tools-and-software/server-and-hpc/compile/arm-instruction-emulator
- ARM instruction evaluator - http://svr-acjf3-armie.cl.cam.ac.uk/
- ARM Lab (VM) - https://azeria-labs.com/arm-lab-vm/
- ARMulator: A emulator for ARM programs (aims to run ARM programs in x86 platform)
	- https://github.com/x-y-z/armulator
	- http://x-y-z.github.io/armulator/
- ARM-X Firmware Emulation Framework
	- The ARM-X Firmware Emulation Framework is a collection of scripts, kernels and filesystems to be used with QEMU to emulate ARM/Linux IoT devices. ARM-X is aimed to facilitate IoT research by virtualising as much of the physical device as possible. It is the closest we can get to an actual IoT VM.
	- https://armx.exploitlab.net/
	- https://github.com/therealsaumil/armx/
	- Introducing ARM-X: The ARM IoT Firmware Emulation Framework
		- HITB+ CyberWeek 2019; Saumil Shah
		- https://www.youtube.com/watch?v=NVl6uJiEaoI
- arm_now: arm vm working out of the box for everyone (Linux / Windows) - https://github.com/nongiach/arm_now
- ASMBits: A problem set and online judge for practicing Nios II or ARMv7 assembly language - https://asmbits.01xz.net/
- CPUlator: An in-browser full-system MIPS, Nios II, and ARMv7 simulator and debugger - https://cpulator.01xz.net/
- Debian on an emulated ARM machine
	- https://www.aurel32.net/info/debian_arm_qemu.php
	- https://wiki.debian.org/ArmEabiHowto
	- https://people.debian.org/~aurel32/qemu/
- ELMO (Emulator for power Leakages for the M0): Leakage simulator for the ARM Cortex M0
	- https://github.com/bristol-sca/ELMO
	- Towards Practical Tools for Side Channel Aware Software Engineering: 'Grey Box' Modelling for Instruction Leakages
	- USENIX Security '17
	- David McCann, Elisabeth Oswald, and Carolyn Whitnall
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/mccann
- Emulate Raspberry Pi with QEMU - http://graznik.de/posts/emulate-raspberry-pi-with-qemu/
- gem5
	- ARM Implementation
		- http://www.gem5.org/documentation/general_docs/architecture_support/arm_implementation/
		- http://old.gem5.org/ARM_Implementation.html
	- Building ARM Kernel - http://www.gem5.org/documentation/general_docs/fullsystem/building_arm_kernel
	- Extending gem5 for ARM - http://www.gem5.org/documentation/learning_gem5/part1/extending_configs
- OakSim: Online ARM assembler and emulator
	- https://wunkolo.github.io/OakSim/
	- https://github.com/Wunkolo/OakSim
- Qemu images (ARM, MIPS, PowerPC, SPARC, AArch64) - https://blahcat.github.io/2017/06/25/qemu-images-to-play-with/
- SimEng (the Simulation Engine): a framework for building modern cycle-accurate processor simulators
	- A fast, easy to use and modify cycle-level simulator for CPUs. Its initial focus is on simulating single Arm cores in server CPUs, and so the instruction set architecture (ISA) target is initially Armv8.4-A+SVE. Later versions of the Arm ISA, and other ISAs such as RISC-V, will be supported in future releases.
	- CPU models in SimEng include: Marvell ThunderX2, Fujitsu A64FX
	- https://github.com/UoB-HPC/SimEng
	- https://uob-hpc.github.io/SimEng/
- thumbulator: Thumb (16 bit ARM) instruction set simulator - https://github.com/dwelch67/thumbulator
- VisUAL - A highly visual ARM emulator - http://salmanarif.bitbucket.org/visual/

### Software: Emulation, Simulation: x86, x86-64

- FEX-Emu: A fast linux usermode x86 and x86-64 emulator for AArch64 devices
	- https://fex-emu.org
	- https://github.com/FEX-Emu/FEX

## Software: Lifting

Disassemblers, Decompilers, Recompilers

- bad64: Binja Arm64 Disassembler
	- bindings to the Binary Ninja arm64 architecture/disassembler plugin: https://github.com/Vector35/arch-arm64
	- https://github.com/yrp604/bad64
- Dynarmic: A dynamic recompiler for the ARMv6K architecture
	- https://github.com/merrymage/dynarmic
- IDA script for highlighting and decoding ARM system instructions
	- https://github.com/gdelugre/ida-arm-system-highlight
- REIL: A C++ translation/emulation library for the AArch64 instruction set to REIL
	- https://github.com/googleprojectzero/reil
- retools: a reverse engineering toolkit for normies
	- Collection of tools (disassembler, emulator, binary parser) aimed at reverse enginering tasks, more specifically, bug finding related. Currently we target ARMv7 and Mach-O though in the future more architectures and formats are planned.
	- retools is somewhat unique in that most of the semantics for relevant instructions are parsed out of the specification PDFs as opposed to being generated by hand. Currently the disassembler, emulator, and binary parsers are partially done, with a symbolic execution engine and instrumentation/hooking framework to come as I get more time.
	- https://github.com/agustingianni/retools
- Spedi: a speculative disassembler for the variable-size Thumb ISA
	- Speculative disassembly, CFG recovery, and call-graph recovery from stripped binaries
	- "Speculative disassembly of binary code" - CASES'16 - https://dl.acm.org/citation.cfm?doid=2968455.2968505
	- https://github.com/abenkhadra/spedi

## Software: Performance

See also: [Performance Tools](performance.tools.md)

- Arm HPC tools and libraries
	- https://developer.arm.com/tools-and-software/server-and-hpc
	- Arm Allinea Studio
		- https://www.arm.com/products/development-tools/server-and-hpc/allinea-studio
	- Arm Performance Libraries
		- https://developer.arm.com/tools-and-software/server-and-hpc/compile/arm-compiler-for-linux/arm-performance-libraries
	- Profiling Tools
		- https://developer.arm.com/hpc/hpc-software/categories/profiling-tools
- Streamline Performance Analyzer
	- https://developer.arm.com/tools-and-software/embedded/arm-development-studio/components/streamline-performance-analyzer

### Software: Performance: Benchmarking

- LIKWID: Performance monitoring and benchmarking suite
	- https://github.com/RRZE-HPC/likwid
	- https://hpc.fau.de/research/tools/likwid/
- Microbenchmarks for Cortex A53
	- https://github.com/thomwiggers/microbenchmark-aarch64/
	- Energy-Efficient ARM64 Cluster with Cryptanalytic Applications
	- LATINCRYPT 2017; Thom Wiggers
	- https://thomwiggers.nl/publication/armcluster/

### Software: Performance: Events

- HWCPipe: a simple and extensible interface for reading CPU and GPU hardware counters
	- https://github.com/ARM-software/HWCPipe
- Linux: ARMv8 PMU Performance Events
	- https://github.com/torvalds/linux/tree/master/tools/perf/pmu-events/arch/arm64
	- https://github.com/torvalds/linux/blob/master/arch/arm64/include/asm/perf_event.h
	- https://github.com/torvalds/linux/blob/master/arch/arm64/kernel/perf_event.c
- Machine-readable data: JSON descriptions of hardware performance events for Arm cores
	- https://github.com/ARM-software/data
- User-mode access to ARMv7 PMU cycle counters
	- https://github.com/thoughtpolice/enable_arm_pmu
	- User-mode performance counters for ARM/Linux
		- http://neocontra.blogspot.com/2013/05/user-mode-performance-counters-for.html
- User-mode access to ARMv8 PMU cycle counters
	- https://github.com/rdolbeau/enable_arm_pmu

### Software: Performance: Libraries

- Arm Optimized Routines
	- Optimized implementations of various library functions for ARM architecture processors
	- https://github.com/ARM-software/optimized-routines
- Compute Library
	- The ARM Computer Vision and Machine Learning library is a set of functions optimised for both ARM CPUs and GPUs using SIMD technologies.
	- https://developer.arm.com/technologies/compute-library
	- https://github.com/ARM-software/ComputeLibrary

### Software: Performance: SIMD

- SIMDe (SIMD Everywhere): Implementations of SIMD instruction sets for systems which don't natively support them
	- The SIMDe header-only library provides fast, portable implementations of SIMD intrinsics on hardware which doesn't natively support them, such as calling SSE functions on ARM. There is no performance penalty if the hardware supports the native implementation (e.g., SSE/AVX runs at full speed on x86, NEON on ARM, etc.).
	- https://github.com/simd-everywhere/simde
	- https://github.com/simd-everywhere/simde#related-projects

#### Software: Performance: SIMD: Neon

- Arm Neon reference tests
	- Tests for Arm Neon instructions, useful for compilers and simulators.
	- https://github.com/christophe-lyon/arm-neon-tests
- AvxToNeon
	- AVX intrinsics implemented with NEON SIMD intrinsics
	- https://github.com/kunpengcompute/AvxToNeon
- Ne10 Open Source Library
	- Ne10 is a library of common, useful functions that have been heavily optimised for ARM-based CPUs equipped with NEON SIMD capabilities. It provides consistent, well-tested behaviour, allowing for painless integration into a wide variety of applications. The library currently focuses primarily around math, signal processing, image processing, and physics functions.
	- http://projectne10.github.io/Ne10/
	- https://github.com/projectNe10/Ne10
- sse2neon: A C/C++ header file that converts Intel SSE intrinsics to Arm/Aarch64 Neon intrinsics
	- https://github.com/DLTcollab/sse2neon
	- https://github.com/DLTcollab/sse2neon#related-projects

#### Software: Performance: SIMD: SVE

- Farm-SVE: A scalar C++ implementation of the ARM® Scalable Vector Extension (SVE)
	- Naive/scalar implementation of the ARM C language extensions (ACLE) for the ARM Scalable Vector Extension (SVE) in standard C++.
	- https://gitlab.inria.fr/bramas/farm-sve

## Software: Virtualization

- NOVA Microhypervisor
	- http://hypervisor.org/
	- https://github.com/udosteinberg/NOVA
	- NOVA Microhypervisor on ARMv8-A
		- FOSDEM 2020; Udo Steinberg
		- https://fosdem.org/2020/schedule/event/uk_nova/

---

# Talks

## 2019

* Arm/AArch64 BoF
	+ [GNU Tools Cauldron 2019](https://gcc.gnu.org/wiki/cauldron2019#cauldron2019talks.The_Arm_AArch64_BoF); Kyrill Tkachov
	+ https://www.youtube.com/watch?v=PBaYzcydliQ
	+ https://gcc.gnu.org/wiki/cauldron2019talks?action=AttachFile&do=view&target=Arm-BoF-Cauldron2019.pdf
* The Definitive Guide to Make Software Fail on ARM64
	+ SREcon19 Asia/Pacific
	+ Ignat Korchagin
	+ https://www.youtube.com/watch?v=B5pmy1OI7uo
	+ https://www.usenix.org/conference/srecon19asia/presentation/korchagin

## 2018

* Arm/AArch64 BoF
	+ [GNU Tools Cauldron 2018](https://gcc.gnu.org/wiki/cauldron2018#arm-bof); Ramana Radhakrishnan & Richard Earnshaw
	+ https://www.youtube.com/watch?v=WEUPBc9QORE
* Arm Architecture Enhancements in 2018
	+ Linaro Connect Vancouver 2018 (YVR18)
	+ https://connect.linaro.org/resources/yvr18/sessions/yvr18-104/
* ARMaHYDAN - Misadventures of ARM instruction encodings
	+ CactusCon 2018
	+ https://www.youtube.com/watch?v=qEfWt2naCx4
	+ https://github.com/XlogicX/ARMaHYDAN
* Introduction To Return Oriented Exploitation On ARM64
	+ BSidesMCR 2018; Billy Ellis
	+ https://www.youtube.com/watch?v=-_LGrrKv61c
* The Path to Fast Data on Arm - Brian Brooks
	+ FD.io Mini-Summit: KubeCon + CloudNativeCon EU 2018
		- https://www.youtube.com/watch?v=n8Yl3Tw7XLg
	+ FD.io Mini Summit: Open Networking Summit North America 2018
		- https://onsna18.sched.com/event/EC21/fdio-mini-summit-the-path-to-fast-data-on-arm
		- https://schd.ws/hosted_files/onsna18/6c/ons_fdio_brooks.pdf
		- https://events.linuxfoundation.org/events/open-networking-summit-north-america-2018/program/schedule/
* Using perf On Arm platforms
	+ Linaro Connect Vancouver 2018 (YVR18)
	+ https://www.youtube.com/watch?v=xV4UHWLH_7Y
	+ https://connect.linaro.org/resources/yvr18/yvr18-416/

## 2017

* A tour of the ARM architecture and its Linux support
	- linux.conf.au 2017; Thomas Petazzoni
	- https://www.youtube.com/watch?v=NNol7fRGo2E
* ARM Assembly and Shellcode Basics
	+ 44CON 2017 Workshop; Saumil Shah
	+ https://www.youtube.com/watch?v=BhjJBuX0YCU
* ARM Developer Systems/Tools – BUD17-508 - http://connect.linaro.org/resource/bud17/bud17-508/
* DynInst on arm64 – Status – BUD17-323 - http://connect.linaro.org/resource/bud17/bud17-323/
* Formal verification by the book: ISA Formal at ARM
	+ Formal Verification 2017; Will Keen (Senior Engineer, CPU Group), ARM
	+ https://www.youtube.com/watch?v=Z7-qkYOpu7I
	+ http://www.testandverification.com/wp-content/uploads/2017/Formal_Verification/Will_Keen%20_ARM.pdf
	+ http://www.testandverification.com/conferences/formal-verification-conference/fv2017/fv2017-formal-verification-book/
* Hardware based tracing on ARM
	- ZeroNights 2017; Ralf Philipp Weinmann
	- https://www.youtube.com/watch?v=xX-B7tW7E_8
* How can you trust formally verified software?
	+ 34th Chaos Communication Congress (34C3) 2017; Alastair Reid
	+ https://fahrplan.events.ccc.de/congress/2017/Fahrplan/events/8915.html
	+ https://media.ccc.de/v/34c3-8915-how_can_you_trust_formally_verified_software
	+ Slides: https://fahrplan.events.ccc.de/congress/2017/Fahrplan/system/event_attachments/attachments/000/003/393/original/How_can_you_trust_formally_verified_software_-_34C3_27_December_2017.pdf
* Introducing LLDB for linux on Arm and AArch64 – BUD17-310 - http://connect.linaro.org/resource/bud17/bud17-310/
* MAMBO: A Low-Overhead Dynamic Binary Modification Tool for ARM
	+ PLDI 2017
	+ Amanieu d'Antras, Cosmin Gorgovan, Jim Garside, Mikel Lujan
	+ https://www.youtube.com/watch?v=FCf-DJ2m0FM
	+ https://pldi17.sigplan.org/event/pldi-2017-papers-low-overhead-dynamic-binary-translation-on-arm
	+ https://www.research.manchester.ac.uk/portal/files/56078084/pldi_16.pdf
	+ https://github.com/beehive-lab/mambo
* Microarchitectural Attacks on Trusted Execution Environments
	 + 34th Chaos Communication Congress (34C3) 2017 - Keegan Ryan
	 + https://media.ccc.de/v/34c3-8950-microarchitectural_attacks_on_trusted_execution_environments
	 + https://www.youtube.com/watch?v=G8-3G_cep4M
* Navigating the ABI for the ARM Architecture – BUD17-318 - http://connect.linaro.org/resource/bud17/bud17-318/
* Towards Practical Tools for Side Channel Aware Software Engineering: 'Grey Box' Modelling for Instruction Leakages
	+ USENIX Security '17
	+ David McCann, Elisabeth Oswald, and Carolyn Whitnall
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/mccann
* TrustZone is not enough: Hijacking debug components for embedded security
	+ 34th Chaos Communication Congress (34C3) 2017 - Pascal Cotret
	+ https://media.ccc.de/v/34c3-8831-trustzone_is_not_enough

## 2016

* ARM Research
	+ SAMOS’16
	+ Eric Hennenhoefer
	+ http://samos-conference.com/Resources_Samos_Websites/Files_Repository_SAMOS/SAMOS_XVI_Keynote_Hennenhoefer.pdf
* ARMv8-A Next Generation Vector Architecture for HPC
	+ Hot Chips 28 (2016)
	+ Nigel Stephens
	+ https://youtu.be/egE-VKoF4ZI?t=1h9m8s
	+ https://community.arm.com/cfs-file/__key/telligent-evolution-components-attachments/01-2142-00-00-00-01-20-49/ARMv8_2D00_A-SVE-technology-Hot-Chips-v12.pdf
* Hardware Assisted Rootkits and Instrumentation ARM Edition
	+ REcon 2016; Matt Spisak
	+ https://www.youtube.com/watch?v=Er_EwQU3lQg
	+ https://recon.cx/2016/resources/slides/RECON-0xA-Hardware-assisted-rootkits-ARM-Spisak.pdf
	+ https://www.slideshare.net/EndgameInc/hardwareassisted-rootkits-instrumentation
* Hardware Assisted Tracing on ARM with CoreSight and OpenCSD
	+ Embedded Linux Conference 2016
		- https://www.youtube.com/watch?v=Gm2ZXIB18PQ
		- https://elinux.org/images/b/b3/Hardware_Assisted_Tracing_on_ARM.pdf
	+ Linaro Connect Las Vegas 2016 (LAS16)
		- http://connect.linaro.org/resource/las16/las16-210/
		- http://www.slideshare.net/linaroorg/las16210-hardware-assisted-tracing-on-arm-with-coresight-and-opencsd
* Modelling the ARMv8 Architecture, Operationally: Concurrency and ISA
	+ POPL 2016
	+ https://www.youtube.com/watch?v=6QU37TwRO4w

## 2015

* perf status on ARM and ARM64
	+ FOSDEM 2015
	+ https://archive.fosdem.org/2015/schedule/event/arm_perf/
	+ Slides (PDF): https://archive.fosdem.org/2015/schedule/event/arm_perf/attachments/slides/601/export/events/attachments/arm_perf/slides/601/Fosdem_2015_perf_status_on_ARM_and_ARM64.pdf

## 2014

* Cycle Accurate Profiling With Perf
	+ Embedded Linux Conference Europe 2014
	+ Pawel Moll, ARM
	+ https://www.elinux.org/File:Moll--cycle_accurate_profiling_with_perf.pdf
	+ http://elinux.org/images/d/d0/Moll--cycle_accurate_profiling_with_perf.pdf
* Square Pegs in Round holes, or System Level Performance Data and perf
	+ Embedded Linux Conference Europe 2014
	+ Pawel Moll, ARM
	+ https://events.static.linuxfound.org/sites/events/files/slides/2014-10_square_pegs.pdf

## 2012

* Advanced Software Exploitation on ARM Microprocessors
	+ Black Hat 2012 USA
	+ Video: https://media.blackhat.com/us-12/video/us-12-Ridley-Advanced-ARM-Exploitation.mp4
	+ http://2012.ruxconbreakpoint.com/assets/Uploads/bpx/Breakpoint2012-Advanced_ARM_Exploitation.pdf
* The AArch64 backend: status and plans
	+ 2012 LLVM Developers’ Meeting; Tim Northover
	+ https://llvm.org/devmtg/2012-11/Northover-AArch64.pdf
	+ https://www.youtube.com/watch?v=rvrHmrtZz-g

## 2011

* ARMv8 Technology Preview
	+ ARM TechCon 2011
	+ Richard Grisenthwaite, ARM Lead Architect and Fellow
	+ https://www.youtube.com/playlist?list=PLB9C800D20A692D7C
	+ Part 1 of 4: https://www.youtube.com/watch?v=GBeEEfmJ3NI
	+ Part 2 of 4: https://www.youtube.com/watch?v=Vm02ZMSfdOc
	+ Part 3 of 4: https://www.youtube.com/watch?v=9ppbRPgzO_s
	+ Part 4 of 4: https://www.youtube.com/watch?v=YPGMwuDaN2k
	+ Slides:
		- http://aarch64.me/public/documents/cpu/arm/ARMv8_Techonology_Preview_Richard.pdf
		- http://web.archive.org/web/20180918053004/https://www.arm.com/files/downloads/ARMv8_Architecture.pdf

## 2010

* Exploitation on ARM - Technique and Bypassing Defense Mechanisms
	+ DEF CON 18 (2010); Itzhak "zuk" Avraham
	+ Video (2010): https://www.youtube.com/watch?v=r4XFFV-tQMI
	+ https://media.blackhat.com/bh-dc-11/Avraham/BlackHat_DC_2011_Avraham_ARM%20Exploitation-wp.2.0.pdf
	+ http://conference.hackinthebox.org/hitbsecconf2011ams/materials/D1T3%20-%20Itzhak%20Zuk%20Avraham%20-%20Popping%20Shell%20On%20Android%20Devices.pdf
	+ https://www.defcon.org/images/defcon-18/dc-18-presentations/Avraham/DEFCON-18-Avraham-Modern%20ARM-Exploitation-WP.pdf

## History

- ARM inventor: Sophie Wilson
	- 2015 Charbax
	- ARM inventor (Part 1) - https://www.youtube.com/watch?v=jhwwrSaHdh8
	- The first ARM processor in the world with Sophie Wilson (Part 2) - https://www.youtube.com/watch?v=re5xAqgKqc0
	- ARM Instruction Set design history with Sophie Wilson (Part 3) - https://www.youtube.com/watch?v=QqxThgLTLyk
- ARM microarchitect: Steve Furber
	- 2016 Charbax
	- https://www.youtube.com/watch?v=_VYxIaw1kBU
- ARM Microprocessor Rise and Fall
	- 2019 Talks at Google; Dave Jaggar
	- https://www.youtube.com/watch?v=_6sh097Dk5k
- ARM Processor Evolution
	- Keynote I, Hot Chips 23 (2011); Simon Segars, ARM
	- https://www.youtube.com/watch?v=ht2cDH2kcW8
- ARM Processor - Sowing the Seeds of Success
	- 2015 Computerphile; Steve Furber
	- https://www.youtube.com/watch?v=1jOJl8gRPyQ
- Clever solutions find inconvenient truths: A history of the ARM Architecture, and the lessons learned while building it
	- Cambridge Science Festival 2016
	- Richard Grisenthwaite, Lead Architect and Fellow, ARM
	- https://soundcloud.com/university-of-cambridge/a-history-of-the-arm-architecture-and-the-lessons-learned-while-building-it
	- https://sms.cam.ac.uk/media/2202336
	- https://player.fm/series/cambridge-science-festival-2016/a-history-of-the-arm-architecture-and-the-lessons-learned-while-building-it
	- Lessons from the ARM Architecture - Slides (2010): http://www.eit.lth.se/fileadmin/eit/courses/eitf20/ARM_RG.pdf
- Historic ARM Presentation to Apple Computer (ARM 610 processor)
	- 1992
	- https://www.youtube.com/watch?v=ZV1NdS_w4As
- The Future of Microprocessors, Sophie Wilson
	- 2016 - Code Mesh - https://www.youtube.com/watch?v=_9mzmvhwMqw
	- 2014 - Wuthering Bytes - https://www.youtube.com/watch?v=b5j_Y-ML3dg
- The Ultimate Acorn Archimedes talk: Everything about the Archimedes computer (with zero 'Eureka!' jokes)
	- 36th Chaos Communication Congress (2019); Matt Evans
	- https://media.ccc.de/v/36c3-10703-the_ultimate_acorn_archimedes_talk
	- https://www.youtube.com/watch?v=Hf67JYkUCHQ

---

# Tutorials, Courses

* ARM assembler in Raspberry Pi - http://thinkingeek.com/arm-assembler-raspberry-pi/
	+ 1\. Introduction - http://thinkingeek.com/2013/01/09/arm-assembler-raspberry-pi-chapter-1/
	+ 2\. Registers and basic arithmetic - http://thinkingeek.com/2013/01/10/arm-assembler-raspberry-pi-chapter-2/
	+ 3\. Memory, addresses; load and store - http://thinkingeek.com/2013/01/11/arm-assembler-raspberry-pi-chapter-3/
	+ 4\. GDB - http://thinkingeek.com/2013/01/12/arm-assembler-raspberry-pi-chapter-4/
	+ 5\. Branches - http://thinkingeek.com/2013/01/19/arm-assembler-raspberry-pi-chapter-5/
	+ 6\. Control structures - http://thinkingeek.com/2013/01/20/arm-assembler-raspberry-pi-chapter-6/
	+ 7\. Indexing modes - http://thinkingeek.com/2013/01/26/arm-assembler-raspberry-pi-chapter-7/
	+ 8\. Arrays and structures and more indexing modes - http://thinkingeek.com/2013/01/27/arm-assembler-raspberry-pi-chapter-8/
	+ 9\. Functions (I) - http://thinkingeek.com/2013/02/02/arm-assembler-raspberry-pi-chapter-9/
	+ 10\. Functions (II); the stack - http://thinkingeek.com/2013/02/07/arm-assembler-raspberry-pi-chapter-10/
	+ 11\. Predication - http://thinkingeek.com/2013/03/16/arm-assembler-raspberry-pi-chapter-11/
	+ 12\. Loops and the status register - http://thinkingeek.com/2013/03/28/arm-assembler-raspberry-pi-chapter-12/
	+ 13\. Floating point numbers - http://thinkingeek.com/2013/05/12/arm-assembler-raspberry-pi-chapter-13/
	+ 14\. Matrix multiply - http://thinkingeek.com/2013/05/12/arm-assembler-raspberry-pi-chapter-14/
	+ 15\. Integer division - http://thinkingeek.com/2013/08/11/arm-assembler-raspberry-pi-chapter-15/
	+ 16\. Switch control structure - http://thinkingeek.com/2013/08/23/arm-assembler-raspberry-pi-chapter-16/
	+ 17\. Passing data to functions - http://thinkingeek.com/2013/11/20/arm-assembler-raspberry-pi-chapter-17/
	+ 18\. Local data and the frame pointer - http://thinkingeek.com/2014/05/11/arm-assembler-raspberry-pi-chapter-18/
	+ 19\. The operating system - http://thinkingeek.com/2014/05/24/arm-assembler-raspberry-pi-chapter-19/
	+ 20\. Indirect calls - http://thinkingeek.com/2014/08/20/arm-assembler-raspberry-pi-chapter-20/
	+ 21\. Subword data - http://thinkingeek.com/2014/08/23/arm-assembler-raspberry-pi-chapter-21/
	+ 22\. The Thumb instruction set - http://thinkingeek.com/2014/12/20/arm-assembler-raspberry-pi-chapter-22/
	+ 23\. Nested functions - http://thinkingeek.com/2015/01/02/arm-assembler-raspberry-pi-chapter-23/
	+ 24\. Trampolines - http://thinkingeek.com/2015/01/09/arm-assembler-raspberry-pi-chapter-24/
	+ 25\. Integer SIMD - http://thinkingeek.com/2015/07/04/arm-assembler-raspberry-pi-chapter-25/
	+ 26\. A primer about linking - http://thinkingeek.com/2016/10/30/arm-assembler-raspberry-pi-chapter-26/
	+ 27\. Dynamic linking - http://thinkingeek.com/2017/04/17/arm-assembler-raspberry-pi-chapter-27/
* ARM Assembly Basics - Azeria Labs
	+ Part 1: Introduction to ARM Assembly Basics - https://azeria-labs.com/writing-arm-assembly-part-1/
	+ Part 2: Data Types - https://azeria-labs.com/arm-data-types-and-registers-part-2/
	+ Part 3: ARM & Thumb - https://azeria-labs.com/arm-instruction-set-part-3/
	+ Part 4: Memory Instructions: Load and Store - https://azeria-labs.com/memory-instructions-load-and-store-part-4/
	+ Part 5: Load/Store Multiple - https://azeria-labs.com/load-and-store-multiple-part-5/
	+ Part 6: Conditional Execution - https://azeria-labs.com/arm-conditional-execution-and-branching-part-6/
	+ Part 7: Stack and Functions - https://azeria-labs.com/functions-and-the-stack-part-7/
	+ Assembly Basics Cheatsheet: https://azeria-labs.com/assembly-basics-cheatsheet/
* ARM Assembly Language - Isfahan University of Technology (Slides)
	+ http://www.googoolia.com/micro/lecture/arm_assembly.pdf
* ARM Assembly Language Programming (AALP) - http://www.peter-cockerell.net/aalp/
* ARM by David Thomas - http://www.davespace.co.uk/arm/
	+ Introduction to ARM - http://www.davespace.co.uk/arm/introduction-to-arm/
	+ Efficient C for ARM - http://www.davespace.co.uk/arm/efficient-c-for-arm/
* ARM Challenges - "Root Me" Learning Platform - https://www.root-me.org/?page=recherche&lang=en&recherche=ARM
* ARM exploitation for IoT
	+ Episode 1: Reversing ARM applications - https://web.archive.org/https://quequero.org/2017/07/arm-exploitation-iot-episode-1/
	+ Episode 2: ARM shellcoding - https://web.archive.org/https://quequero.org/2017/09/arm-exploitation-iot-episode-2/
	+ Episode 3: ARM exploitations - https://web.archive.org/https://quequero.org/2017/11/arm-exploitation-iot-episode-3/
* ARM lectures by Dr. Santanu Chaudhury, EE Department, IIT Delhi - https://www.youtube.com/playlist?list=PL95AFA4ABA8B28627
* EECS 370 - http://www.eecs.umich.edu/courses/eecs370/ - http://www.eecs.umich.edu/courses/eecs370/eecs370/resources/
	+ ARM Examples - https://www.eecs.umich.edu/courses/eecs370/eecs370.f20/resources/materials/370ARMExamples.pdf
	+ ARM Instruction Set Quick Reference Card - https://www.eecs.umich.edu/courses/eecs370/eecs370.f20/resources/materials/ARM_Instruction_Set.pdf
	+ ARM v8 Quick Reference Guide - http://www.eecs.umich.edu/courses/eecs370/eecs370.f20/resources/materials/ARM-v8-Quick-Reference-Guide.pdf
* ELEC 5260/ELEC 6260-6266: Embedded Computing Systems
	+ http://www.eng.auburn.edu/~nelson/courses/elec5260_6260/
	+ ARM Assembly Language (Knaggs & Welsh - Bournemouth Univ.)
		- http://www.eng.auburn.edu/~nelson/courses/elec5260_6260/arm/ARM_AssyLang.pdf
	+ ARM processor architecture - http://www.eng.auburn.edu/~nelson/courses/elec5260_6260/slides/Chapter2%20ARM.pdf
* Introducing ARM assembly language - http://www.toves.org/books/arm/
* Introduction to ARM
	+ Gananand Kini's class on the ARM CPU assembly and architecture
	+ http://www.opensecuritytraining.info/IntroARM.html
	+ https://www.youtube.com/playlist?list=PLUFkSN0XLZ-n91t_AX5zO007Giz1INwPd
* Understanding ARM Assembly - Marion Cole
	+ Part 1: Processor features - https://blogs.msdn.microsoft.com/ntdebugging/2013/11/22/understanding-arm-assembly-part-1/
	+ Part 2: How Windows uses the processor - https://blogs.msdn.microsoft.com/ntdebugging/2014/05/15/understanding-arm-assembly-part-2/
	+ Part 3: Calling conventions - https://blogs.msdn.microsoft.com/ntdebugging/2014/05/29/understanding-arm-assembly-part-3/
* Whirlwind Tour of ARM Assembly - https://www.coranac.com/tonc/text/asm.htm
* Windows on ARM - An assembly language primer - http://www.codemachine.com/article_armasm.html

## AArch64

- A Guide to ARM64 / AArch64 Assembly on Linux with Shellcodes and Cryptography
	- https://modexp.wordpress.com/2018/10/30/arm64-assembly/
- ARM AArch64 Assembly Language Lectures
	- Princeton COS 217 (Spring 2020)
	- https://www.cs.princeton.edu/courses/archive/spr20/cos217/schedule.html
	- Assembly Language 1
		- https://www.youtube.com/watch?v=w--9Zm55C0o
		- https://www.cs.princeton.edu/courses/archive/spr20/cos217/lectures/13_Assembly1.pdf
	- Assembly Language 2
		- https://www.youtube.com/watch?v=JDCPs-m-3Dw
		- https://www.cs.princeton.edu/courses/archive/spr20/cos217/lectures/14_Assembly2.pdf
	- Assembly Language Functions
		- https://www.youtube.com/watch?v=HkGldSflDwM
		- https://www.cs.princeton.edu/courses/archive/spr20/cos217/lectures/15_AssemblyFunctions.pdf
	- Machine Language Instructions
		- https://www.youtube.com/watch?v=guXTCGlL50A
		- https://www.cs.princeton.edu/courses/archive/spr20/cos217/lectures/17_MachineLang.pdf
	- Assembler and Linker
		- https://www.youtube.com/watch?v=ZYV6pAhvX_M
		- https://www.cs.princeton.edu/courses/archive/spr20/cos217/lectures/17_MachineLang.pdf#page=37
- arm64 assembly crash course - https://github.com/Siguza/ios-resources/blob/master/bits/arm64.md
- Armv8-A Instruction Set Architecture (ISA)
	- https://developer.arm.com/architectures/learn-the-architecture/armv8-a-instruction-set-architecture
- Exploring AArch64 assembler - https://thinkingeek.com/categories/aarch64/
	- Chapter 1: first program - http://thinkingeek.com/2016/10/08/exploring-aarch64-assembler-chapter1/
	- Chapter 2: register operands and immediate operands - http://thinkingeek.com/2016/10/08/exploring-aarch64-assembler-chapter-2/
	- Chapter 3: more about register operands - http://thinkingeek.com/2016/10/23/exploring-aarch64-assembler-chapter-3/
	- Chapter 4: arithmetic and bitwise instructions - http://thinkingeek.com/2016/10/23/exploring-aarch64-assembler-chapter-4/
	- Chapter 5: memory - http://thinkingeek.com/2016/11/13/exploring-aarch64-assembler-chapter-5/
	- Chapter 6: control flow - http://thinkingeek.com/2016/11/27/exploring-aarch64-assembler-chapter-6/
	- Chapter 7: functions - http://thinkingeek.com/2017/03/19/exploring-aarch64-assembler-chapter-7/
	- Chapter 8: the stack - http://thinkingeek.com/2017/05/29/exploring-aarch64-assembler-chapter-8/
	- Chapter 9: control constructs - http://thinkingeek.com/2017/11/05/exploring-aarch64-assembler-chapter-9/
- Introduction to ARMv8 64-bit Architecture - https://web.archive.org/https://quequero.org/2014/04/introduction-to-arm-architecture/
- Programming with 64-Bit ARM Assembly Language
	- https://www.apress.com/us/book/9781484258804
	- https://github.com/Apress/programming-with-64-bit-ARM-assembly-language
	- HelloSilicon: third-party Apple Silicon version
		- https://github.com/below/HelloSilicon

## Thumb-2

- ARM-ASM-Tutorial - Thumb-2 (T32) - Niklas Gürtler
	- https://www.mikrocontroller.net/articles/ARM-ASM-Tutorial
- The ARM processor (Thumb-2) - Raymond Chen
	- part 1: Introduction: https://devblogs.microsoft.com/oldnewthing/20210531-00/?p=105265
	- part 2: Differences between classic ARM and Thumb-2: https://devblogs.microsoft.com/oldnewthing/20210601-00/?p=105267
	- part 3: Addressing modes: https://devblogs.microsoft.com/oldnewthing/20210602-00/?p=105271
	- part 4: Single-instruction constants: https://devblogs.microsoft.com/oldnewthing/20210603-00/?p=105276
	- part 5: Arithmetic: https://devblogs.microsoft.com/oldnewthing/20210604-00/?p=105280
	- part 6: The lie hiding inside the CMN instruction: https://devblogs.microsoft.com/oldnewthing/20210607-00/?p=105288
	- part 7: Bitwise operations: https://devblogs.microsoft.com/oldnewthing/20210608-00/?p=105290
	- part 8: Bit shifting and bitfield access: https://devblogs.microsoft.com/oldnewthing/20210609-00/?p=105293
	- part 9: Sign and zero extension: https://devblogs.microsoft.com/oldnewthing/20210610-00/?p=105295
	- part 10: Memory access and alignment: https://devblogs.microsoft.com/oldnewthing/20210611-00/?p=105299
	- part 11: Atomic access and barriers: https://devblogs.microsoft.com/oldnewthing/20210614-00/?p=105307
	- part 12: Control transfer: https://devblogs.microsoft.com/oldnewthing/20210615-00/?p=105311
	- part 13: Trampolines: https://devblogs.microsoft.com/oldnewthing/20210616-00/?p=105314
	- part 14: Manipulating flags: https://devblogs.microsoft.com/oldnewthing/20210617-00/?p=105317
	- part 15: Miscellaneous instructions: https://devblogs.microsoft.com/oldnewthing/20210618-00/?p=105324
	- part 16: The calling convention: https://devblogs.microsoft.com/oldnewthing/20210621-00/?p=105327
	- part 17: Prologues and epilogues: https://devblogs.microsoft.com/oldnewthing/20210622-00/?p=105332
	- part 18: Other kinds of prologues and epilogues: https://devblogs.microsoft.com/oldnewthing/20210623-00/?p=105351
	- part 19: Common patterns: https://devblogs.microsoft.com/oldnewthing/20210624-46/?p=105355
	- part 20: Code walkthrough: https://devblogs.microsoft.com/oldnewthing/20210625-00/?p=105369
