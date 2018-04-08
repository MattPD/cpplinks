# [C++ links](README.md): ARM and AArch64 Assembly

Note: see [Computer Architecture](comparch.md) -- recommended background (which makes the following significantly more approachable) includes at least an undegraduate-level course.

# Contents

* [Readings](#readings):
	+ [Concurrency](#concurrency)
	+ [Formalization, Specification, Verification](#formalization-specification-verification)
	+ [Instruction Set Architecture](#instruction-set-architecture)
	+ [Performance](#performance)
	+ [Security](#security)
	+ [Virtualization](#virtualization)
* [References](#references):
	+ [Concurrency](#concurrency)
	+ [Intrinsics, NEON, SIMD](#intrinsics-neon-simd)
	+ [Toolchains](#toolchains)
* [Software](#software):
	+ [Binary Analysis](#binary-analysis)
	+ [Debugging, Tracing](#debugging-tracing)
	+ [Emulation, Simulation](#emulation-simulation)
	+ [Lifting: Disassemblers, Decompilers, Recompilers](#lifting-disassemblers-decompilers-recompilers)
	+ [Performance](#performance-1)
* [Talks](#talks):
	+ [2018](#2018)
	+ [2017](#2017)
	+ [2016](#2016)
	+ [2015](#2015)
	+ [2014](#2014)
	+ [2012](#2012)
	+ [2011](#2011)
	+ [2010](#2010)
	+ [History](#history)
* [Tutorials, Courses](#tutorials-courses)

---

# Readings

## Concurrency

* Mixed-size Concurrency: ARM, POWER, C/C++11, and SC
	+ POPL 2017
	+ Shaked Flur, Susmit Sarkar, Christopher Pulte, Kyndylan Nienhuis, Luc Maranget, Kathryn E. Gray, Ali Sezgin, Mark Batty, Peter Sewell
	+ http://www.cl.cam.ac.uk/~pes20/popl17/
	+ http://www.cl.cam.ac.uk/~pes20/AArch64
* Modelling the ARM v8 Architecture, Operationally: Concurrency and ISA 
	+ POPL 2016
	+ Shaked Flur, Kathryn E. Gray, Christopher Pulte, Susmit Sarkar, Ali Sezgin, Luc Maranget, Will Deacon, Peter Sewell
	+ http://www.cl.cam.ac.uk/~pes20/popl16-armv8/top.pdf
	+ https://blog.acolyer.org/2016/02/02/arm-v8/
* Relaxed-Memory Concurrency - Power and ARM
	+ http://www.cl.cam.ac.uk/~pes20/weakmemory/#PA
	+ http://www.cl.cam.ac.uk/~pes20/papers/topics.html#Power_and_ARM
* RMEM
	+ a tool for exploring the relaxed-memory concurrency behaviour allowed by the ARM and IBM POWER architectures; it also has experimental support for x86-TSO and a candidate RISC-V model
	+ help page: http://www.cl.cam.ac.uk/~sf502/regressions/rmem/help.html
	+ web interface: http://www.cl.cam.ac.uk/users/pes20/rmem/
* Simplifying ARM Concurrency: Multicopy-atomic Axiomatic and Operational Models for ARMv8
	+ POPL 2018 - https://www.youtube.com/watch?v=v9uygT1d0xY
	+ Christopher Pulte, Shaked Flur, Will Deacon, Jon French, Susmit Sarkar, Peter Sewell
	+ http://www.cl.cam.ac.uk/%7Epes20/armv8-mca/
	+ http://www.cl.cam.ac.uk/%7Epes20/armv8-mca/armv8-mca-draft.pdf
* The Semantics of Power and ARM Multiprocessor Machine Code
	+ DAMP 09
	+ J. Alglave, A. Fox, S. Isthiaq, M. Myreen, S. Sarkar, P. Sewell, F. Zappa Nardelli
	+ http://www.di.ens.fr/~zappa/readings/damp09.pdf
* The Semantics of Power and ARM Multiprocessor Programs
	- http://www.cl.cam.ac.uk/~pes20/weakmemory/index4.html

## Formalization, Specification, Verification

* A Trustworthy Monadic Formalization of the ARMv7 Instruction Set Architecture
	+ Interactive Theorem Proving (ITP), 2010
	+ Anthony Fox and Magnus O. Myreen
	+ https://www.cl.cam.ac.uk/~mom22/itp10-armv7.pdf
* Alastair Reid's
	+ Blog Posts - https://alastairreid.github.io/
	+ Papers: https://alastairreid.github.io/alastairreid.github.io/papers/
	+ 2017-12-24 - Bidirectional Assembly Syntax Specifications - https://alastairreid.github.io/bidirectional-assemblers/
	+ 2017-09-24 - Formal validation of the Arm v8-M specification - https://alastairreid.github.io/validating-specs/
	+ 2017-08-19 - Are natural language specifications useful? - https://alastairreid.github.io/natural-specs/
	+ 2017-07-31 - Arm v8.3 Machine Readable Specification Released - https://alastairreid.github.io/arm-v8_3/
	+ 2017-05-07 - ASL Lexical Syntax - https://alastairreid.github.io/asl-lexical-syntax/
	+ 2017-04-29 - Dissecting ARM's Machine Readable Specification - https://alastairreid.github.io/dissecting-ARM-MRA/
	+ 2017-04-20 - ARM Releases Machine Readable Architecture Specification - https://alastairreid.github.io/ARM-v8a-xml-release/
	+ 2016-08-17 - ARM's Architecture Specification Language - https://alastairreid.github.io/specification_languages/
	+ 2016-07-30 - Limitations of ISA-Formal - https://alastairreid.github.io/isa-formal-limitations/
	+ 2016-07-26 - Verifying against the official ARM specification - https://alastairreid.github.io/using-armarm/
	+ 2016-07-18 - Finding Bugs versus Proving Absence of Bugs - https://alastairreid.github.io/finding-bugs/
	+ 2016-07-03 - Specification Terminology - https://alastairreid.github.io/spec-terminology/
* End-to-End Verification of ARM Processors with ISA-Formal
	+ CAV 2016
	+ Alastair Reid, Rick Chen, Anastasios Deligiannis, David Gilday, David Hoyes, Will Keen, Ashan Pathirane, Owen Shepherd, Peter Vrabel, Ali Zaidi
	+ https://alastairreid.github.io/papers/CAV_16/
	+ https://alastairreid.github.io/papers/cav2016_isa_formal.pdf
	+ https://alastairreid.github.io/alastairreid.github.io/papers/ISA-Formal-CAV2016.pdf
* L3: A Specification Language for Instruction Set Architectures - http://www.cl.cam.ac.uk/~acjf3/arm/
* Trustworthy Specifications of ARM v8-A and v8-M System Level Architecture
	+ FMCAD 2016
	+ Alastair Reid
	+ https://alastairreid.github.io/papers/FMCAD_16/
	+ https://alastairreid.github.io/papers/fmcad2016-trustworthy.pdf
	+ https://alastairreid.github.io/alastairreid.github.io/papers/fmcad2016-trustworthy-slides.pdf
* Who Guards the Guards? Formal Validation of the Arm v8-M Architecture Specification
	+ SPLASH 2017 OOPSLA
	+ Alastair Reid
	+ Paper: https://alastairreid.github.io/papers/oopsla2017-whoguardstheguards.pdf
	+ Post: https://alastairreid.github.io/validating-specs/
	+ Slides: https://alastairreid.github.io/papers/oopsla2017-whoguardstheguards-slides.pdf

## Instruction Set Architecture

* ARM immediate value encoding - Alisdair McDiarmid
	+ https://alisdair.mcdiarmid.org/arm-immediate-value-encoding/
* ARMv8 Shellcodes from 'A' to 'Z'
	+ ISPEC 2016
	+ Hadrien Barral, Houda Ferradi, Rémi Géraud, Georges-Axel Jaloyan, David Naccache
	+ https://arxiv.org/abs/1608.03415
* Exploring the Arm dot product instructions - https://community.arm.com/tools/b/blog/posts/exploring-the-arm-dot-product-instructions
* Introduction to Computer Organization: ARM Assembly Language Using the Raspberry Pi
	+ http://bob.cs.sonoma.edu/IntroCompOrg-RPi/intro-co-rpi.html
* Optional CRC Instructions in ARMv8 - https://wiki.linaro.org/LEG/Engineering/OPTIM/CRC
* Pointer Authentication on ARMv8.3
	+ https://www.qualcomm.com/documents/whitepaper-pointer-authentication-armv83
	+ https://www.qualcomm.com/media/documents/files/whitepaper-pointer-authentication-on-armv8-3.pdf
	+ https://www.qualcomm.com/news/onq/2017/01/10/qualcomm-releases-whitepaper-detailing-pointer-authentication-armv83

## Performance

* CoreSight, Perf and the OpenCSD Library - https://www.linaro.org/blog/core-dump/coresight-perf-and-the-opencsd-library/
* Linaro Wiki - perf
	+ https://wiki.linaro.org/KenWerner/Sandbox/perf
	+ https://wiki.linaro.org/Platform/DevPlatform/Tools/Perf
	+ ARM32/64: perf: dwarf stack frame unwinding support - https://wiki.linaro.org/LEG/Engineering/TOOLS/perf-callstack-unwinding
* On-Target Trace Using the CoreSight Access Library - https://developer.arm.com/products/software-development-tools/ds-5-development-studio/resources/tutorials/on-target-trace-using-the-coresight-access-library
* OpenCSD HOWTO - using the library with perf: https://github.com/Linaro/OpenCSD/blob/opencsd-0v002/HOWTO.md
* Statistical Profiling Extension for ARMv8-A - https://community.arm.com/processors/b/blog/posts/statistical-profiling-extension-for-armv8-a
* The ARM Scalable Vector Extension
	+ IEEE Micro, March 2017
	+ Nigel Stephens, Stuart Biles, Matthias Boettcher, Jacob Eapen, Mbou Eyole, Giacomo Gabrielli, Matt Horsnell, Grigorios Magklis, Alejandro Martinez, Nathanael Premillieu, Alastair Reid, Alejandro Rico, Paul Walker
	+ Preprint: https://alastairreid.github.io/papers/sve-ieee-micro-2017.pdf
	+ http://dx.doi.org/10.1109/MM.2017.35

## Security

* ARM Lab Environment - https://www.vulnhub.com/series/arm-lab,145/
* ARM Return Oriented Programming (ROP) - Billy Ellis
	+ Cheatsheet - https://twitter.com/bellis1000/status/929713826106396673
	+ https://billy-ellis.github.io/armintro.html
	+ https://billy-ellis.github.io/rop1.html
	+ https://billy-ellis.github.io/rop2.html
	+ https://billy-ellis.github.io/rop3.html
* ARM shellcode and exploit development
	+ BSidesMunich 2018 Workshop
	+ https://github.com/invictus1306/Workshop-BSidesMunich2018
	+ https://github.com/invictus1306/Workshop-BSidesMunich2018/blob/master/workshop_slides.pdf
* Cache Speculation Side-channels
	+ Richard Grisenthwaite
	+ https://developer.arm.com/support/security-update
	+ Compiler support for mitigations - https://developer.arm.com/support/security-update/compiler-support-for-mitigations
	+ Speculation Barrier - https://github.com/ARM-software/speculation-barrier
* Cachegrab: a tool designed to help perform and visualize trace-driven cache attacks against software in the secure world of TrustZone-enabled ARMv8 cores
	+ https://github.com/nccgroup/cachegrab
	+ https://www.nccgroup.trust/us/about-us/newsroom-and-events/blog/2017/december/34C3-Tool-Release-Cachegrab/
* Damn Vulnerable ARM Router (DVAR)
	+ http://blog.exploitlab.net/2018/01/dvar-damn-vulnerable-arm-router.html
* Exploitation on ARM-based Systems
	+ Troopers18; Sascha Schirra, Ralf Schaefer 
	+ https://github.com/sashs/arm_exploitation
* Exploring New Depths of Threat Hunting ...or How to Write ARM Shellcode in Six Minutes
	+ Security Analysts Summit (SAS) 2018
	+ https://azeria-labs.com/downloads/SAS-v1.0-Azeria.pdf
* Micro-Architectural Power Simulator for Leakage Assessment of Cryptographic Software on ARM Cortex-M3 Processors
	+ Cryptology ePrint Archive: Report 2017/1253
	+ Yann Le Corre, Johann Großschädl, Daniel Dinu
	+ https://eprint.iacr.org/2017/1253
* NORAX: Enabling Execute-Only Memory for COTS Binaries on AArch64 
	+ Security and Privacy (S&P) 2017
	+ Yaohui Chen, Dongli Zhang, Ruowen Wang, Rui Qiao, Ahmed Azab, Long Lu, Hayawardh Vijayakumar, Wenbo Shen
	+ http://seclab.cs.sunysb.edu/seclab/pubs/norax.pdf
* Pointer Authentication on ARMv8.3 - https://www.qualcomm.com/media/documents/files/whitepaper-pointer-authentication-on-armv8-3.pdf
* RevARM: A Platform-Agnostic ARM Binary Rewriter for Security Applications
	+ Annual Computer Security Applications Conference (ACSAC) 2017
	+ T. Kim, C. Kim, H. Choi, Y. Kwon, B. Saltaformaggio, X. Zhang, D. Xu
	+ https://www.cs.purdue.edu/homes/kwon58/data/revarm_acsac17.pdf
	+ https://www.acsac.org/2017/openconf/modules/request.php?module=oc_program&action=summary.php&id=201
	+ https://www.researchgate.net/publication/321506390_RevARM_A_Platform-Agnostic_ARM_Binary_Rewriter_for_Security_Applications
* TCP Bind Shell in Assembly (ARM 32-bit)
	+ https://azeria-labs.com/tcp-bind-shell-in-assembly-arm-32-bit/
* Verification of a Practical Hardware Security Architecture Through Static Information Flow Analysis (ARM TrustZone)
	+ ASPLOS 2017
	+ Andrew Ferraiuolo, Rui Xu, Danfeng Zhang, Andrew C. Myers, G. Edward Suh
	+ http://www.cs.cornell.edu/andru/papers/trustzone/

## Virtualization

* The Design, Implementation, and Evaluation of Software and Architectural Support for ARM Virtualization
	+ 2018 PhD Thesis; [Christoffer Dall](http://www.cs.columbia.edu/~cdall/)
	+ https://academiccommons.columbia.edu/catalog/ac:t1g1jwstss

# References

* ARM Architecture Documentation
	+ The Applications (‘A’) profile - https://developer.arm.com/products/architecture/a-profile/docs
	+ The Real-Time (‘R’) profile - https://developer.arm.com/products/architecture/r-profile/docs
	+ The Microcontroller (‘M’) profile - https://developer.arm.com/products/architecture/m-profile/docs
* ARM Architecture Reference Manuals - http://infocenter.arm.com/help/topic/com.arm.doc.subset.architecture.reference/index.html#reference
* A-Profile
	+ A-Profile Architectures - Exploration Tools - https://developer.arm.com/products/architecture/a-profile/exploration-tools
	+ ARM Architecture Reference Manual ARMv8, for ARMv8-A architecture profile
		- https://developer.arm.com/docs/ddi0487/latest/arm-architecture-reference-manual-armv8-for-armv8-a-architecture-profile
	+ Cortex-A57 Software Optimization Guide
		- http://infocenter.arm.com/help/index.jsp?topic=/com.arm.doc.uan0015b/
		- https://developer.arm.com/docs/uan0015/latest/cortex-a57-software-optimization-guide-software-optimization-guide
		- PDF: http://infocenter.arm.com/help/topic/com.arm.doc.uan0015b/Cortex_A57_Software_Optimization_Guide_external.pdf
	+ Programmer’s Guide for ARMv8-A: ARM® Cortex-A Series, Version: 1.0
		- http://infocenter.arm.com/help/topic/com.arm.doc.den0024a/DEN0024A_v8_architecture_PG.pdf
* ARM and Thumb-2 Instruction Set Quick Reference Card
	+ http://infocenter.arm.com/help/topic/com.arm.doc.qrc0001m/QRC0001_UAL.pdf
* ARM Assembly Basics Cheatsheet - https://azeria-labs.com/assembly-basics-cheatsheet/
* ARM architecture documentation set - http://infocenter.arm.com/help/index.jsp?topic=/com.arm.doc.set.architecture/
* ARM Info Center Reference Material - https://wiki.linaro.org/Resources/HowTo/DeveloperReferences
* ARM v8-A Architecture Specification
	+ https://github.com/meriac/archex
	+ https://meriac.github.io/archex/
* asm.thi.ng - baremetal ARM coding resources - http://asm.thi.ng/
* Instruction Sets - https://developer.arm.com/products/architecture/instruction-sets
* Linux Kernel Documentation
	+ ARM: https://www.kernel.org/doc/Documentation/arm/
	+ ARM64: https://www.kernel.org/doc/Documentation/arm64/
* Scalable Vector Extension (SVE)
	+ https://community.arm.com/processors/b/blog/posts/technology-update-the-scalable-vector-extension-sve-for-the-armv8-a-architecture
	+ https://developer.arm.com/hpc/a-sneak-peek-into-sve-and-vla-programming
	+ ARMv8-A Next Generation Vector Architecture for HPC
		- Hot Chips 28 (2016)
		- Nigel Stephens
		- https://youtu.be/egE-VKoF4ZI?t=1h9m8s
		- https://community.arm.com/cfs-file/__key/telligent-evolution-components-attachments/01-2142-00-00-00-01-20-49/ARMv8_2D00_A-SVE-technology-Hot-Chips-v12.pdf
* The ARM Instruction Set - ARM University Program (Slides)
	+ https://www.cs.purdue.edu/homes/cs250/LectureNotes/arm_inst.pdf
	+ https://www.eecs.umich.edu/courses/eecs370/eecs370.f17/resources/materials/arm_inst.pdf
* The ARM Instruction Set Architecture - Mark McDermott (Slides)
	+ http://users.ece.utexas.edu/~valvano/EE345M/Arm_EE382N_4.pdf
* Works on ARM newsletter - https://github.com/vielmetti/worksonarm-news

## Intrinsics, NEON, SIMD

* ARC SIMD Built-in Functions - https://gcc.gnu.org/onlinedocs/gcc/ARC-SIMD-Built-in-Functions.html
* ARM Intrinsics - MSDN - Microsoft - https://docs.microsoft.com/en-us/cpp/intrinsics/arm-intrinsics
* ARM NEON Intrinsics - https://gcc.gnu.org/onlinedocs/gcc-4.9.4/gcc/ARM-NEON-Intrinsics.html#ARM-NEON-Intrinsics
* NEON Intrinsics - https://developer.arm.com/technologies/neon/intrinsics
* NEON intrinsics guide - https://github.com/thenifty/neon-guide
* NEON Programmer’s Guide - http://infocenter.arm.com/help/index.jsp?topic=/com.arm.doc.den0018a/

## Toolchains

* ARM Product Manuals - Keil - http://www.keil.com/support/man_arm.htm
	+ armasm Assembler User Guide - http://www.keil.com/support/man/docs/armasm/
	+ armcc Compiler User Guide - http://www.keil.com/support/man/docs/armcc/
	+ armlink Linker User Guide - http://www.keil.com/support/man/docs/armlink/
	+ armclang Compiler Getting Started Guide - http://www.keil.com/support/man/docs/armclang_intro/
	+ armclang Compiler Reference Guide - http://www.keil.com/support/man/docs/armclang_ref/
	+ armclang Compiler Software Development Guide - http://www.keil.com/support/man/docs/armclang_dev/
	+ armclang_asm Assembler User Guide - http://www.keil.com/support/man/docs/armclang_asm/
	+ armclang_link Linker User Guide - http://www.keil.com/support/man/docs/armclang_link/
* GNU Compiler Collection (GCC)
	+ AArch64 Options - https://gcc.gnu.org/onlinedocs/gcc/AArch64-Options.html
	+ ARM Options - https://gcc.gnu.org/onlinedocs/gcc/ARM-Options.html
	+ ARM C Language Extensions (ACLE) - https://gcc.gnu.org/onlinedocs/gcc/ARM-C-Language-Extensions-_0028ACLE_0029.html
	+ Target-Specific Builtins - https://gcc.gnu.org/onlinedocs/gcc/Target-Builtins.html#Target-Builtins
* Microsoft ARM Assembler Reference - https://docs.microsoft.com/en-us/cpp/assembler/arm/arm-assembler-reference

# Software

* Arm HPC Users Group - resources for end-users and developers deploying on Arm hardware.
	+ https://gitlab.com/arm-hpc
* AMaCC (Another Mini ARM C Compiler) - Small C Compiler generating ELF executable for Arm architecture
	+ https://github.com/jserv/amacc
* mra_tools: Tools to process ARM's Machine Readable Architecture Specification
	+ https://github.com/alastairreid/mra_tools
* VIXL: AArch64 Runtime Code Generation Library
	+ https://github.com/armvixl/vixl

## Binary Analysis

* MAMBO: A Low-Overhead Dynamic Binary Modification Tool for ARM
	+ https://github.com/beehive-lab/mambo
	+ PLDI 2017 
	+ Amanieu d'Antras, Cosmin Gorgovan, Jim Garside, Mikel Lujan
	+ https://www.youtube.com/watch?v=FCf-DJ2m0FM
	+ https://pldi17.sigplan.org/event/pldi-2017-papers-low-overhead-dynamic-binary-translation-on-arm
	+ https://www.research.manchester.ac.uk/portal/files/56078084/pldi_16.pdf
	+ https://github.com/beehive-lab/mambo
* mbed-os-linker-report: d3.js based ELF Linker Statistics
	+ Post-processing of linker output to calculate and visualize memory usage for elf-sections
	+ https://github.com/ARMmbed/mbed-os-linker-report
	+ https://os.mbed.com/blog/entry/visualizing-linker-stats/

## Debugging, Tracing

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

## Emulation, Simulation

* ARM instruction evaluator - http://svr-acjf3-armie.cl.cam.ac.uk/
* ARM Lab (VM) - https://azeria-labs.com/arm-lab-vm/
* ARMulator: A emulator for ARM programs (aims to run ARM programs in x86 platform)
	+ https://github.com/x-y-z/armulator
	+ http://x-y-z.github.io/armulator/
* arm_now: arm vm working out of the box for everyone (Linux / Windows) - https://github.com/nongiach/arm_now
* ASMBits: A problem set and online judge for practicing Nios II or ARMv7 assembly language - https://asmbits.01xz.net/
* CPUlator: An in-browser full-system MIPS, Nios II, and ARMv7 simulator and debugger - https://cpulator.01xz.net/
* Debian on an emulated ARM machine
	+ https://www.aurel32.net/info/debian_arm_qemu.php
	+ https://wiki.debian.org/ArmEabiHowto
	+ https://people.debian.org/~aurel32/qemu/
* ELMO (Emulator for power Leakages for the M0): Leakage simulator for the ARM Cortex M0
	+ https://github.com/bristol-sca/ELMO
	+ Towards Practical Tools for Side Channel Aware Software Engineering: 'Grey Box' Modelling for Instruction Leakages
	+ USENIX Security '17
	+ David McCann, Elisabeth Oswald, and Carolyn Whitnall
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/mccann
* Emulate Raspberry Pi with QEMU - http://graznik.de/posts/emulate-raspberry-pi-with-qemu/
* gem5 - ARM Implementation - http://gem5.org/ARM_Implementation
* OakSim: Online ARM assembler and emulator
	+ https://wunkolo.github.io/OakSim/
	+ https://github.com/Wunkolo/OakSim
* Qemu images (ARM, MIPS, PowerPC, SPARC, AArch64) - https://blahcat.github.io/2017/06/25/qemu-images-to-play-with/
* thumbulator: Thumb (16 bit ARM) instruction set simulator - https://github.com/dwelch67/thumbulator
* VisUAL - A highly visual ARM emulator - http://salmanarif.bitbucket.org/visual/

## Lifting: Disassemblers, Decompilers, Recompilers

* Dynarmic: A dynamic recompiler for the ARMv6K architecture
	+ https://github.com/merrymage/dynarmic
* IDA script for highlighting and decoding ARM system instructions
	+ https://github.com/gdelugre/ida-arm-system-highlight
* retools: a reverse engineering toolkit for normies
	+ Collection of tools (disassembler, emulator, binary parser) aimed at reverse enginering tasks, more specifically, bug finding related. Currently we target ARMv7 and Mach-O though in the future more architectures and formats are planned.
	+ retools is somewhat unique in that most of the semantics for relevant instructions are parsed out of the specification PDFs as opposed to being generated by hand. Currently the disassembler, emulator, and binary parsers are partially done, with a symbolic execution engine and instrumentation/hooking framework to come as I get more time.
	+ https://github.com/agustingianni/retools
* Spedi: a speculative disassembler for the variable-size Thumb ISA
	+ Speculative disassembly, CFG recovery, and call-graph recovery from stripped binaries
	+ "Speculative disassembly of binary code" - CASES'16 - https://dl.acm.org/citation.cfm?doid=2968455.2968505
	+ https://github.com/abenkhadra/spedi

## Performance

* ARM Code Advisor - https://developer.arm.com/products/software-development-tools/hpc/arm-code-advisor
* ARM Math Library Functions
	+ Optimized implementations of various library functions for ARM architecture processors
	+ https://github.com/ARM-software/optimized-routines
* ARM Performance Libraries - https://developer.arm.com/products/software-development-tools/hpc/arm-performance-libraries
* Compute Library
	+ The ARM Computer Vision and Machine Learning library is a set of functions optimised for both ARM CPUs and GPUs using SIMD technologies.
	+ https://developer.arm.com/technologies/compute-library
	+ https://github.com/ARM-software/ComputeLibrary
* Ne10 Open Source Library
	+ Ne10 is a library of common, useful functions that have been heavily optimised for ARM-based CPUs equipped with NEON SIMD capabilities. It provides consistent, well-tested behaviour, allowing for painless integration into a wide variety of applications. The library currently focuses primarily around math, signal processing, image processing, and physics functions.
	+ http://projectne10.github.io/Ne10/
	+ https://github.com/projectNe10/Ne10
* Profiling Tools - https://developer.arm.com/hpc/hpc-software/categories/profiling-tools
* Streamline Performance Analyzer - https://developer.arm.com/products/software-development-tools/ds-5-development-studio/streamline

# Talks

## 2018

* Raising the Bar: New Hardware Primitives for Exploit Mitigations - BlueHat v17
	+ ARMv8.3 pointer authentication
	+ https://www.youtube.com/watch?v=PYe8W33lbAQ
	+ https://www.slideshare.net/MSbluehat/raising-the-bar-new-hardware-primitives-for-exploit-mitigations-83686492

## 2017

* A tour of the ARM architecture and its Linux support - linux.conf.au 2017
	+ https://www.youtube.com/watch?v=NNol7fRGo2E
* ARM Developer Systems/Tools – BUD17-508 - http://connect.linaro.org/resource/bud17/bud17-508/
* DynInst on arm64 – Status – BUD17-323 - http://connect.linaro.org/resource/bud17/bud17-323/
* Formal verification by the book: ISA Formal at ARM
	+ Formal Verification 2017 - Will Keen (Senior Engineer, CPU Group), ARM
	+ https://www.youtube.com/watch?v=Z7-qkYOpu7I
	+ http://www.testandverification.com/wp-content/uploads/2017/Formal_Verification/Will_Keen%20_ARM.pdf
	+ http://www.testandverification.com/conferences/formal-verification-conference/fv2017/fv2017-formal-verification-book/
* Hardware based tracing on ARM - Ralf Philipp Weinmann, ZeroNights 2017
	+ https://www.youtube.com/watch?v=xX-B7tW7E_8
* How can you trust formally verified software?
	+ 34th Chaos Communication Congress (34C3) 2017 - Alastair Reid
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
* Hardware Assisted Tracing on ARM with CoreSight and OpenCSD
	+ Embedded Linux Conference 2016
		- https://www.youtube.com/watch?v=Gm2ZXIB18PQ
		- http://events.linuxfoundation.org/sites/events/files/slides/ELC-E16.pdf
		- http://elinux.org/images/b/b3/Hardware_Assisted_Tracing_on_ARM.pdf
	+ Linaro Connect Las Vegas 2016 (LAS16) 
		- http://connect.linaro.org/resource/las16/las16-210/
		- http://www.slideshare.net/linaroorg/las16210-hardware-assisted-tracing-on-arm-with-coresight-and-opencsd
* Modelling the ARMv8 Architecture, Operationally: Concurrency and ISA - POPL 2016
	+ https://www.youtube.com/watch?v=6QU37TwRO4w
* REcon 2016 - Hardware Assisted Rootkits and Instrumentation ARM Edition (Matt Spisak)
	+ https://www.youtube.com/watch?v=Er_EwQU3lQg
	+ https://recon.cx/2016/resources/slides/RECON-0xA-Hardware-assisted-rootkits-ARM-Spisak.pdf
	+ https://www.slideshare.net/EndgameInc/hardwareassisted-rootkits-instrumentation

## 2015

* FOSDEM 2015 - perf status on ARM and ARM64
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
	+ http://events.linuxfoundation.org/sites/events/files/slides/2014-10_square_pegs.pdf

## 2012

* Advanced Software Exploitation on ARM Microprocessors | Black Hat 2012 USA
	+ https://www.youtube.com/watch?v=eM6TKcIwqI4
	+ http://2012.ruxconbreakpoint.com/assets/Uploads/bpx/Breakpoint2012-Advanced_ARM_Exploitation.pdf

## 2011

* ARMv8 Technology Preview
	+ ARM TechCon 2011
	+ Richard Grisenthwaite, ARM Lead Architect and Fellow
	+ https://www.youtube.com/playlist?list=PLB9C800D20A692D7C
	+ Part 1 of 4: https://www.youtube.com/watch?v=GBeEEfmJ3NI
	+ Part 2 of 4: https://www.youtube.com/watch?v=Vm02ZMSfdOc
	+ Part 3 of 4: https://www.youtube.com/watch?v=9ppbRPgzO_s
	+ Part 4 of 4: https://www.youtube.com/watch?v=YPGMwuDaN2k
	+ Slides: http://www.arm.com/files/downloads/ARMv8_Architecture.pdf

## 2010

* DEF CON 18 (2010) - Itzhak "zuk" Avraham - Exploitation on ARM - Technique and Bypassing Defense Mechanisms
	+ https://www.exploit-db.com/docs/14548.pdf
	+ Video (2010): https://www.youtube.com/watch?v=r4XFFV-tQMI
	+ https://media.blackhat.com/bh-dc-11/Avraham/BlackHat_DC_2011_Avraham_ARM%20Exploitation-wp.2.0.pdf
	+ http://conference.hackinthebox.org/hitbsecconf2011ams/materials/D1T3%20-%20Itzhak%20Zuk%20Avraham%20-%20Popping%20Shell%20On%20Android%20Devices.pdf
	+ https://www.defcon.org/images/defcon-18/dc-18-presentations/Avraham/DEFCON-18-Avraham-Modern%20ARM-Exploitation-WP.pdf

## History

* ARM inventor: Sophie Wilson
	+ ARM inventor (Part 1) - https://www.youtube.com/watch?v=jhwwrSaHdh8
	+ The first ARM processor in the world with Sophie Wilson (Part 2) - https://www.youtube.com/watch?v=re5xAqgKqc0
	+ ARM Instruction Set design history with Sophie Wilson (Part 3) - https://www.youtube.com/watch?v=QqxThgLTLyk
* ARM microarchitect: Steve Furber
	+ https://www.youtube.com/watch?v=_VYxIaw1kBU
* ARM Processor Evolution
	+ Keynote I, Hot Chips 23 (2011). Simon Segars, ARM 
	+ https://www.youtube.com/watch?v=ht2cDH2kcW8
* Clever solutions find inconvenient truths: A history of the ARM Architecture, and the lessons learned while building it
	+ Cambridge Science Festival 2016
	+ Richard Grisenthwaite, Lead Architect and Fellow, ARM
	+ https://soundcloud.com/university-of-cambridge/a-history-of-the-arm-architecture-and-the-lessons-learned-while-building-it
	+ https://sms.cam.ac.uk/media/2202336
	+ https://player.fm/series/cambridge-science-festival-2016/a-history-of-the-arm-architecture-and-the-lessons-learned-while-building-it
	+ Lessons from the ARM Architecture - Slides (2010): http://www.eit.lth.se/fileadmin/eit/courses/eitf20/ARM_RG.pdf
* The Future of Microprocessors, Sophie Wilson
	+ 2016 - Code Mesh - https://www.youtube.com/watch?v=_9mzmvhwMqw
	+ 2014 - Wuthering Bytes - https://www.youtube.com/watch?v=b5j_Y-ML3dg

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
	+ Episode 1: Reversing ARM applications - https://quequero.org/2017/07/arm-exploitation-iot-episode-1/
	+ Episode 2: ARM shellcoding - https://quequero.org/2017/09/arm-exploitation-iot-episode-2/
	+ Episode 3: ARM exploitations - https://quequero.org/2017/11/arm-exploitation-iot-episode-3/
* ARM lectures by Dr. Santanu Chaudhury, EE Department, IIT Delhi - https://www.youtube.com/playlist?list=PL95AFA4ABA8B28627
* ARM Shellcode - Azeria Labs
	+ Part 1: Introduction to Writing ARM Shellcode - https://azeria-labs.com/writing-arm-shellcode/
	+ Part 2: Process Memory and Memory Corruptions - https://azeria-labs.com/process-memory-and-memory-corruption/
	+ Part 3: Stack Overflow Challenges - https://azeria-labs.com/part-3-stack-overflow-challenges/
	+ Code: https://github.com/azeria-labs/ARM-assembly-examples
* arm64 assembly crash course - https://github.com/Siguza/ios-resources/blob/master/bits/arm64.md
* EECS 370 - http://www.eecs.umich.edu/courses/eecs370/eecs370.f17/resources/
	+ ARM Examples - https://www.eecs.umich.edu/courses/eecs370/eecs370.w17/resources/materials/370ARMExamples.pdf
	+ ARM Instruction Set Quick Reference Card - https://www.eecs.umich.edu/courses/eecs370/eecs370.f17/resources/materials/ARM_Instruction_Set.pdf
	+ ARM v8 Quick Reference Guide - http://www.eecs.umich.edu/courses/eecs370/eecs370.f17/resources/materials/ARM-v8-Quick-Reference-Guide.pdf
* ELEC 5260/ELEC 6260-6266: Embedded Computing Systems
	+ http://www.eng.auburn.edu/~nelson/courses/elec5260_6260/
	+ ARM Assembly Language (Knaggs & Welsh - Bournemouth Univ.)
		- http://www.eng.auburn.edu/~nelson/courses/elec5260_6260/arm/ARM_AssyLang.pdf
	+ ARM processor architecture - http://www.eng.auburn.edu/~nelson/courses/elec5260_6260/slides/Chapter2%20ARM.pdf
* Exploring AArch64 assembler - http://thinkingeek.com/category/aarch64/
	+ Chapter 1: first program - http://thinkingeek.com/2016/10/08/exploring-aarch64-assembler-chapter1/
	+ Chapter 2: register operands and immediate operands - http://thinkingeek.com/2016/10/08/exploring-aarch64-assembler-chapter-2/
	+ Chapter 3: more about register operands - http://thinkingeek.com/2016/10/23/exploring-aarch64-assembler-chapter-3/
	+ Chapter 4: arithmetic and bitwise instructions - http://thinkingeek.com/2016/10/23/exploring-aarch64-assembler-chapter-4/
	+ Chapter 5: memory - http://thinkingeek.com/2016/11/13/exploring-aarch64-assembler-chapter-5/
	+ Chapter 6: control flow - http://thinkingeek.com/2016/11/27/exploring-aarch64-assembler-chapter-6/
	+ Chapter 7: functions - http://thinkingeek.com/2017/03/19/exploring-aarch64-assembler-chapter-7/
	+ Chapter 8: the stack - http://thinkingeek.com/2017/05/29/exploring-aarch64-assembler-chapter-8/
	+ Chapter 9: control constructs - http://thinkingeek.com/2017/11/05/exploring-aarch64-assembler-chapter-9/
* Introducing ARM assembly language - http://www.toves.org/books/arm/
* Introduction to ARM
	+ Gananand Kini's class on the ARM CPU assembly and architecture
	+ http://www.opensecuritytraining.info/IntroARM.html
	+ https://www.youtube.com/playlist?list=PLUFkSN0XLZ-n91t_AX5zO007Giz1INwPd
* Introduction to ARMv8 64-bit Architecture - https://quequero.org/2014/04/introduction-to-arm-architecture/
* Shellcode: Encryption Algorithms in ARM Assembly - https://modexp.wordpress.com/2018/02/04/arm-crypto/
* Understanding ARM Assembly - Marion Cole
	+ Part 1: Processor features - https://blogs.msdn.microsoft.com/ntdebugging/2013/11/22/understanding-arm-assembly-part-1/
	+ Part 2: How Windows uses the processor - https://blogs.msdn.microsoft.com/ntdebugging/2014/05/15/understanding-arm-assembly-part-2/
	+ Part 3: Calling conventions - https://blogs.msdn.microsoft.com/ntdebugging/2014/05/29/understanding-arm-assembly-part-3/
* Whirlwind Tour of ARM Assembly - https://www.coranac.com/tonc/text/asm.htm
