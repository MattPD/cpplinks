# [C++ links](README.md): computer architecture - micro-architectural channels

Note: see [Computer Architecture](comparch.md)

# General

* A Survey of Microarchitectural Timing Attacks and Countermeasures on Contemporary Hardware
	+ Q.Ge, Y. Yarom, D. Cock, and G. Heiser, Cryptology ePrint Archive, Report 2016/613
	+ http://eprint.iacr.org/2016/613
	+ https://ts.data61.csiro.au/publications/nictaabstracts/9074.pdf
	+ http://eprint.iacr.org.metacomment.io/2016/613
* Cycle-Accurate Timing Channel Analysis of Binary Code" - Roeland Krak, 2017
	+ http://essay.utwente.nl/72321/
	+ http://essay.utwente.nl/72321/1/Krak_MA_EEMCS.pdf
	+ model of instruction execution time for the ARM Cortex-A7
* Software-based Microarchitectural Attacks - Daniel Gruss, PhD thesis, 2017
	+ https://gruss.cc/files/phd_thesis.pdf
	+ slides: https://gruss.cc/files/phd_defense_slides.pdf
* MASCAB: a Micro-Architectural Side-Channel Attack Bibliography - https://github.com/danpage/mascab
- YouTube playlist: https://www.youtube.com/playlist?list=PLcjiHk8Sl-KK1qY4JOzTDu095TscjcEVa
* Microarchitectural Side-Channel Attacks - CHES 2016 tutorial
	+ http://cs.adelaide.edu.au/~yval/CHES16/
	+ http://cs.adelaide.edu.au/~yval/CHES16/CHES16-tutorial.pptx
	+ http://cs.adelaide.edu.au/~yval/CHES16/CHES16-tutorial2.pptx
	+ http://www.chesworkshop.org/ches2016/presentations/CHES16-Tutorial2_1.pdf
	+ http://www.chesworkshop.org/ches2016/presentations/CHES16-Tutorial2_2.pdf
	+ https://cryptologie.net/article/367/ches-2016-tutorial-part-2-micro-architectural-side-channel-attacks/
* Mastik: A Micro-Architectural Side-Channel Toolkit
	+ http://cs.adelaide.edu.au/~yval/Mastik/
	+ http://cryptologie.net/article/366/ches-2016-tutorial-part-1-common-criteria-certification-of-a-smartcard-a-technical-overview/
	+ https://cryptologie.net/article/367/ches-2016-tutorial-part-2-micro-architectural-side-channel-attacks/
* Survey of Microarchitectural Side and Covert Channels, Attacks, and Defenses - Jakub Szefer 
	+ http://eprint.iacr.org/2016/479
* Systematic Classification of Side-Channel Attacks: A Case Study for Mobile Devices - https://arxiv.org/abs/1611.03748
* The Last Mile: An Empirical Study of Timing Channels on seL4
	+ http://research.davidcock.fastmail.fm/slides/lastmile.pdf
	+ https://ts.data61.csiro.au/publications/nictaabstracts/8295.pdf
	+ http://ts.data61.csiro.au/projects/TS/timingchannels.pml
* Understanding contention-based channels and using them for defense, HPCA 2015
	+ Hunger, C., Kazdagli, M., Rawat, A., Dimakis, A., Vishwanath, S., and Tiwari, M.
	+ http://users.ece.utexas.edu/~tiwari/pubs/HPCA-15-contention.pdf
* Your Processor Leaks Information - and There's Nothing You Can Do About It, 2017
	+ https://arxiv.org/abs/1612.04474

# Defense, Mitigation, Protection

* CacheD: Identifying Cache-Based Timing Channels in Production Software - https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/wang-shuai
* ParTI - Towards Combined Hardware Countermeasures against Side Channel and Fault Injection Attacks - CHES 2016 
	+ https://www.youtube.com/watch?v=wTJvb6k5yp0
* Side Channel Analysis Protection and Low Latency in Action - Case Study of PRINCE and Midori
	+ https://www.youtube.com/watch?v=8OyQIh3F4AU
* Strong and Efficient Cache Side-Channel Protection using Hardware Transactional Memory - https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/gruss
* Towards Practical Tools for Side Channel Aware Software Engineering: 'Grey Box' Modelling for Instruction Leakages - https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/mccann

# Branch Predictor

* Covert Channels Through Branch Predictors: A Feasibility Study, HASP 2015
http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.702.6038&rep=rep1&type=pdf
http://caslab.csl.yale.edu/workshops/hasp2015/slides_05_evtyushkin.pdf
* Jump Over ASLR: Attacking Branch Predictors to Bypass ASLR - http://www.cs.binghamton.edu/~dima/micro16.pdf
* PoC for breaking hypervisor ASLR using branch target buffer collisions - https://github.com/felixwilhelm/mario_baslr/
* Understanding and Mitigating Covert Channels Through Branch Predictors, TACO 13(1): 10 (2016)
	+ Dmitry Evtyushkin, Dmitry Ponomarev, Nael B. Abu-Ghazaleh
	+ http://www.cs.ucr.edu/~nael/pubs/taco16_branches.pdf
	+ https://dl.acm.org/citation.cfm?id=2870636
	+ http://www.cs.wm.edu/~dmitry/assets/files/taco-a10-evtyushkin.pdf

# Cache

* A High-Resolution Side-channel attack on the Last Level Cache, DAC'16 (best paper nominee)
	+ paper: http://www.cs.ucr.edu/~nael/pubs/dac16.pdf
	+ slides: http://www.cs.ucr.edu/~nael/pubs/dac16.pptx
* A Software Approach to Defeating Side Channels in Last-Level Caches
	+ https://arxiv.org/abs/1603.05615
	+ CCS 2016: https://www.youtube.com/watch?v=_dAnVtrtfdA
* ARMageddon: How Your Smartphone CPU Breaks Software-Level Security and Privacy
	+ Black Hat Europe 2016: https://www.youtube.com/watch?v=9KsnFWejpQg
	+ https://github.com/IAIK/armageddon
	+ thesis: https://www.blackhat.com/docs/eu-16/materials/eu-16-Lipp-ARMageddon-How-Your-Smartphone-CPU-Breaks-Software-Level-Security-And-Privacy-wp.pdf
	+ slides:   https://www.blackhat.com/docs/eu-16/materials/eu-16-Lipp-ARMageddon-How-Your-Smartphone-CPU-Breaks-Software-Level-Security-And-Privacy.pdf
	+ https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/lipp
* C5: Cross-Cores Cache Covert Channel, 2015
	+ Detection of Intrusions and Malware, and Vulnerability Assessment
	+ http://www.s3.eurecom.fr/docs/dimva15_clementine.pdf
	+ https://link.springer.com/chapter/10.1007/978-3-319-20550-2_3
* Cache side channel attacks - https://dreamsofastone.blogspot.com/2015/09/cache-side-channel-attacks.html
* Strong and Efficient Cache Side-Channel Protection using Hardware Transactional Memory - https://gruss.cc/files/cloak.pdf
* Yet Another MicroArchitectural Attack: Exploiting I-cache - http://eprint.iacr.org/2007/164

# DRAM

* Another Flip in the Wall of Rowhammer Defenses - https://arxiv.org/abs/1710.00551
* DRAMA: How Your DRAM Becomes a Security Problem
	+ slides: https://www.blackhat.com/docs/eu-16/materials/eu-16-Schwarz-How-Your-DRAM-Becomes-A-Security-Problem.pdf
	+ thesis: DRAMA: Exploiting DRAM Buffers for Fun and Profit
	+ Black Hat Europe 2016: https://www.youtube.com/watch?v=lSU6YzjIIiQ
* Hammertime: a software suite for testing, profiling and simulating the rowhammer DRAM defect - https://github.com/vusec/hammertime
* Whispers in the Hyper-space: High-speed Covert Channel Attacks in the Cloud - https://www.usenix.org/conference/usenixsecurity12/technical-sessions/presentation/wu

# Electromagnetic Emanations (EM)

The EM Side–Channel(s): Attacks and Assessment Methodologies, 2003
	+ https://www.cs.jhu.edu/~astubble/600.412/s-c-papers/em.pdf
	+ http://citeseerx.ist.psu.edu/viewdoc/summary;?doi=10.1.1.122.1646
	+ https://www.semanticscholar.org/paper/The-EM-Side-Channel-s-Attacks-and-Assessment-Metho-Agrawal-Archambeault/7d687c23e297196e4de38240f9b48eb2d31f20fe
* Zero-Overhead Profiling via Electromagnetic (EM) Emanations
	+ https://dl.acm.org/citation.cfm?id=2931065
	+ https://issta2016.cispa.saarland/zero-overhead-profiling-via-em-emanations/

# Floating Point Unit (FPU)

* On Subnormal Floating Point and Abnormal Timing
	+ http://www.ieee-security.org/TC/SP2015/papers-archived/6949a623.pdf
	+ https://cseweb.ucsd.edu/~dkohlbre/papers/subnormal.pdf
	+ http://cseweb.ucsd.edu/~hovav/papers/akmjls15.html
	+ https://github.com/kmowery/libfixedtimefixedpoint
* On the effectiveness of mitigations against floating-point timing channels
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/kohlbrenner
	+ https://cseweb.ucsd.edu/~dkohlbre/floats/

# GPU

* Constructing and Characterizing Covert Channels on GPGPUs, MICRO-50, 2017 - http://www.cs.ucr.edu/~kkhas001/pubs/micro17-gpu.pdf

# Memory Bus

* Whispers in the hyper-space: high-speed covert channel attacks in the cloud, USENIX Security 2012
	+ https://www.usenix.org/conference/usenixsecurity12/technical-sessions/presentation/wu
	+ https://www.youtube.com/watch?v=d2TU_Q4U9DA

# MMU

* ASLR on the Line: Practical Cache Attacks on the MMU
	+ B. Gras, K. Razavi, E. Bosman, H. Bos, C. Giuffrida, in: NDSS, 2017.
	+ https://www.vusec.net/download/?t=papers/anc_ndss17.pdf
* Reverse Engineering Hardware Page Table Caches Using Side-Channel Attacks on the MMU
	+ S. van Schaik, K. Razavi, B. Gras, H. Bos, C. Giuffrida, VU Amsterdam, 2017.
	+ https://www.vusec.net/download/?t=papers/revanc_ir-cs-77.pdf
* Telling Your Secrets without Page Faults: Stealthy Page Table-Based Attacks on Enclaved Execution
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/van-bulck
	+ https://github.com/jovanbulck/sgx-pte

# Power

* On Code Execution Tracking via Power Side-Channel
	+ https://dl.acm.org/citation.cfm?id=2978299
	+ https://www.youtube.com/watch?v=YwL_p3TxhlA

# Prefetch

* Prefetch Side-Channel Attacks: Bypassing SMAP and Kernel ASLR - https://gruss.cc/files/prefetch.pdf
* Using Undocumented CPU Behavior to See Into Kernel Mode and Break KASLR in the Process
	+ https://www.youtube.com/watch?v=Pwq0vv4X7m4
	+ https://www.blackhat.com/docs/us-16/materials/us-16-Fogh-Using-Undocumented-CPU-Behaviour-To-See-Into-Kernel-Mode-And-Break-KASLR-In-The-Process.pdf

# Pseudo-Random Number Generator (PRNG)

* Covert Channels through Random Number Generator: Mechanisms, Capacity Estimation and Mitigations
	+ http://www.cs.binghamton.edu/~dima/ccs16.pdf
	+ CCS 2016: https://www.youtube.com/watch?v=G1xzG43mkZU

# SGX

* Cache Attacks on Intel SGX - https://www1.informatik.uni-erlangen.de/filepool/projects/sgx-timing/sgx-timing.pdf
* Inferring Fine-grained Control Flow Inside SGX Enclaves with Branch Shadowing
	+ Skylake's BTB parameters, use of Intel PT and LBR
	+ https://arxiv.org/abs/1611.06952
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/lee-sangho
* Malware Guard Extension: Using SGX to Conceal Cache Attacks - https://arxiv.org/abs/1702.08719

# SMT

* Covert Shotgun: Automatically finding covert channels in SMT - https://cyber.wtf/2016/09/27/covert-shotgun/

# Thermal

* On the capacity of thermal covert channels in multicores - https://dl.acm.org/citation.cfm?id=2901322
* Thermal Covert Channels on Multi-core Platforms - https://www.usenix.org/conference/usenixsecurity15/technical-sessions/presentation/masti

# TSX

* Breaking Kernel Address Space Layout Randomization with Intel TSX
	+ https://sslab.gtisc.gatech.edu/assets/papers/2016/jang:drk-ccs.pdf
	+ http://www.cc.gatech.edu/~yjang37/assets/papers/2016/jang:drk-ccs.pdf
	+ decoded icache (caches decoded micro-ops) - inside L1 icache, virtually-indexed and virtually tagged (VIVT), does not require an iTLB access for address translation
* Prime+Abort: A Timer-Free High-Precision L3 Cache Attack using Intel TSX - https://www.usenix.org/node/203659

# Talks

## 2017

* Anders Fogh: "Covert shotgun: Automatically finding covert channels in SMT" - HackPra
	+ https://www.youtube.com/watch?v=oVmPQCT5VkY
	+ https://cyber.wtf/2016/09/27/covert-shotgun/
* RuhrSec 2017: "A new categorization system for Side-channel attacks on mobile devices & more", Dr. Veelasha Moonsamy
	+ https://www.youtube.com/watch?v=YxikZkZ6KuE
* Victor van der Veen: "Drammer: The Making-Of" - https://www.youtube.com/watch?v=DF0k9yKYwfo

## 2016

* ARMageddon: How Your Smartphone CPU Breaks Software-Level Security and Privacy - https://www.youtube.com/watch?v=9KsnFWejpQg
* CCS 2016 - CREDAL: Towards Locating a Memory Corruption Vulnerability with Your Core Dump - https://www.youtube.com/watch?v=jOL4oElUKjA&t=955s
* CCS 2016 - ECDSA Key Extraction from Mobile Devices via Nonintrusive Physical Side Channels - https://www.youtube.com/watch?v=0SQUQbth5vU
* CCS 2016 - On Code Execution Tracking via Power Side-Channel - https://www.youtube.com/watch?v=YwL_p3TxhlA
* Clémentine Maurice: "Reverse-engineering CPUs for fun and profit" - https://www.youtube.com/watch?v=IT6PFSRrvsU
* Daniel Gruss – Microarchitectural Incontinence - You would leak too if you were so fast! - https://www.youtube.com/watch?v=cAWmNp3Ukqk
* DEF CON 24 2016 Side channel attacks on high security electronic safe locks - https://www.youtube.com/watch?v=vJ9NdvKYxeg
* HITB2016AMS CLOSING KEYNOTE - Hardware Side Channels in Virtualized Environments - Sophia D'Antoine - https://www.youtube.com/watch?v=1KteO7FPXYw
* HITB2016AMS D2T1 - Cache Side Channel Attacks: CPU Design As A Security Problem - Anders Fogh
	+ https://www.youtube.com/watch?v=UH6dFbiX_hM
	+ https://conference.hitb.org/hitbsecconf2016ams/materials/D2T1%20-%20Anders%20Fogh%20-%20Cache%20Side%20Channel%20Attacks.pdf
* Return-Oriented Flush-Reload Side Channels on ARM and Their Implications for Android Devices - https://www.youtube.com/watch?v=tymvrJiJNl8
* RuhrSec 2016: "Cache Side-Channel Attacks and the case of Rowhammer", Daniel Gruss - https://www.youtube.com/watch?v=gxsguH5opsM
* Side-Channel Attacks on Everyday Applications - https://www.youtube.com/watch?v=GPwNFrpd1KU&t=9s
* Using Undocumented CPU Behavior to See Into Kernel Mode and Break KASLR in the Process - https://www.youtube.com/watch?v=Pwq0vv4X7m4 - 
* What could possibly go wrong with {insert x86 instruction here}? [33c3] - https://www.youtube.com/watch?v=wue4QomGE74&t=122s

## 2015

* Clémentine Maurice, Daniel Gruss: Rowhammer.js: Root privileges for web apps? - https://www.youtube.com/watch?v=9L5MJ43nbkI
* Controlled-Channel Attacks: Deterministic Side Channels for Untrusted Operating Systems - https://www.youtube.com/watch?v=fwUaN5ik8zE
* DEF CON 23 - Etienne Martineau - The art of cache timing covert channel on x86 multi core - https://www.youtube.com/watch?v=7X772EBdvnM
* Exploiting Out-of-Order Execution For Covert Cross-VM Communication - Black Hat 2015
	+ https://www.youtube.com/watch?v=SjcKqVRjNHc
	+ https://www.blackhat.com/docs/us-15/materials/us-15-DAntoine-Exploiting-Out-Of-Order-Execution-For-Covert-Cross-VM-Communication.pdf
* Last-Level Cache Side-Channel Attacks are Practical - https://www.youtube.com/watch?v=vpGI1ggKzC4
* REcon 2015 - Exploiting Out of Order Execution (Sophia D'Antoine)
	+ https://www.youtube.com/watch?v=AbRoWa_xrzA
	+ https://recon.cx/2015/slides/recon2015-06-sophia-d-antoine-Exploiting-Out-of-Order-Execution.pdf
* S$A: A Shared Cache Attack That Works across Cores and Defies VM Sandboxing -- and Its Application to AES - https://www.youtube.com/watch?v=mwMjn8niX-Y
* Side-Channel Attacks by Differential Power Analysis - Nathaniel Graff - https://www.youtube.com/watch?v=bHncSnHQleY

## 2014

* MIT 6.858 Computer Systems Security, Fall 2014 - Lecture 16. Side-Channel Attacks - https://www.youtube.com/watch?v=PuVMkSEcPiI

## 2012

* Defcon 17 - Sniff Keystrokes With Lasers/Voltmeters - Side Channel Attacks Using Optical Sampling - https://www.youtube.com/watch?v=9zq9DQAbWmU

## 2011

* 22C3: Covert channels in TCP/IP: attack and defense - https://www.youtube.com/watch?v=jeRGZAJyMH8
