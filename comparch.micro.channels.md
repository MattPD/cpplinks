# [C++ links](README.md): computer architecture - microarchitectural channels

See also: [Computer Architecture](comparch.md)

* Leakage channels: side channels (accidental), covert channels (deliberate).
* Storage channels (functional behavior), timing channels (temporal behavior).
* Timing-based channels (operations timing), access-based channels (direct information access), trace-based channels (program execution measurement).

# Contents

+ [General](#general)
+ [Defense, Mitigation, Protection](#defense-mitigation-protection)

* [Arithmetic Logic Unit (ALU)](#arithmetic-logic-unit-alu)
* [Branch Predictor](#branch-predictor)
* [Cache](#cache)
* [DRAM](#dram)
* [Electromagnetic (EM) Emanations](#electromagnetic-em-emanations)
* [Floating Point Unit (FPU)](#floating-point-unit-fpu)
* [FPGA](#fpga)
* [GPU](#gpu)
* [Interrupts](#interrupts)
* [Magnetic](#magnetic)
* [Memory Bus](#memory-bus)
* [Memory Order Buffer (MOB)](#memory-order-buffer-mob)
* [Memory Management Unit (MMU)](#memory-management-unit-mmu)
* [Power](#power)
* [Prefetch](#prefetch)
* [Pseudo-Random Number Generator (PRNG)](#pseudo-random-number-generator-prng)
* [SGX](#sgx)
* [SMT](#smt)
* [Speculation](#speculation)
* [Thermal](#thermal)
* [Translation Lookaside Buffer (TLB)](#translation-lookaside-buffer-tlb)
* [TSX](#tsx)
* [Talks](#talks)

---

# General

* A Survey of Microarchitectural Timing Attacks and Countermeasures on Contemporary Hardware
	+ Q.Ge, Y. Yarom, D. Cock, and G. Heiser, Cryptology ePrint Archive, Report 2016/613
	+ http://eprint.iacr.org/2016/613
	+ https://ts.data61.csiro.au/publications/nictaabstracts/9074.pdf
	+ http://eprint.iacr.org.metacomment.io/2016/613
* A Note on the Confinement Problem
	+ Butler W. Lampson, Communications of the ACM (CACM) 1973
	+ http://bwlampson.site/11-Confinement/Abstract.html
* Cross-core Microarchitectural Side Channel Attacks and Countermeasures
	+ 2017 Dissertation; Gorka Irazoqui
	+ https://web.wpi.edu/Pubs/ETD/Available/etd-042417-114714/unrestricted/girazoki.pdf
* Cycle-Accurate Timing Channel Analysis of Binary Code - Roeland Krak, 2017
	+ http://essay.utwente.nl/72321/
	+ http://essay.utwente.nl/72321/1/Krak_MA_EEMCS.pdf
	+ model of instruction execution time for the ARM Cortex-A7
* Exploiting processor side channels to enable cross VM malicious code execution
	+ 2015 Thesis, Sophia M. D'Antoine
	+ http://digitool.rpi.edu:8881/dtl_publish/15/175977.html
	+ https://www.sophia.re/thesis.pdf
	+ https://www.blackhat.com/docs/us-15/materials/us-15-DAntoine-Exploiting-Out-Of-Order-Execution-For-Covert-Cross-VM-Communication-wp.pdf
* MASCAB: a Micro-Architectural Side-Channel Attack Bibliography - https://github.com/danpage/mascab
	+ YouTube playlist: https://www.youtube.com/playlist?list=PLcjiHk8Sl-KK1qY4JOzTDu095TscjcEVa
* Mastik: A Micro-Architectural Side-Channel Toolkit
	+ http://cs.adelaide.edu.au/~yval/Mastik/
	+ http://cryptologie.net/article/366/ches-2016-tutorial-part-1-common-criteria-certification-of-a-smartcard-a-technical-overview/
	+ https://cryptologie.net/article/367/ches-2016-tutorial-part-2-micro-architectural-side-channel-attacks/
* Microarchitectural Side-Channel Attacks - CHES 2016 tutorial
	+ http://cs.adelaide.edu.au/~yval/CHES16/
	+ http://cs.adelaide.edu.au/~yval/CHES16/CHES16-tutorial.pptx
	+ http://cs.adelaide.edu.au/~yval/CHES16/CHES16-tutorial2.pptx
	+ http://www.chesworkshop.org/ches2016/presentations/CHES16-Tutorial2_1.pdf
	+ http://www.chesworkshop.org/ches2016/presentations/CHES16-Tutorial2_2.pdf
	+ https://cryptologie.net/article/367/ches-2016-tutorial-part-2-micro-architectural-side-channel-attacks/
* Negative Result: Reading Kernel Memory From User Mode
	+ 2017, Anders Fogh
	+ https://cyber.wtf/2017/07/28/negative-result-reading-kernel-memory-from-user-mode/
* Software-based Microarchitectural Attacks - Daniel Gruss, PhD thesis, 2017
	+ https://gruss.cc/files/phd_thesis.pdf
	+ slides: https://gruss.cc/files/phd_defense_slides.pdf
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

* A Hardware Design Language for Timing-Sensitive Information-Flow Security
	+ ASPLOS 2015
	+ Danfeng Zhang, Yao Wang, G. Edward Suh, Andrew C. Myers
	+ http://www.cs.cornell.edu/andru/papers/asplos15/
	+ Meltdown, Spectre, and why hardware can be correct yet insecure
		- https://andrumyers.wordpress.com/2018/01/17/meltdown-spectre-and-how-hardware-can-be-correct-but-insecure/
* Architecting against Software Cache-Based Side-Channel Attacks
	+ IEEE Transactions on Computers 62(7), July 2013
	+ Jingfei Kong, O. Aciicmez, J-P Seifert, Huiyang Zhou
	+ http://ieeexplore.ieee.org/document/6178238/
* Automated Detection of Instruction Cache Leaks in Modular Exponentiation Software
	+ CARDIS 2016
	+ Andreas Zankl, Johann Heyszl, Georg Sigl
	+ https://link.springer.com/chapter/10.1007/978-3-319-54669-8_14
	+ https://github.com/falsecurity/cache-leak-detector
* CacheAudit: A Tool for the Static Analysis of Cache Side Channels 
	+ USENIX Security 2013
	+ Goran Doychev, Dominik Feld, Boris Köpf, Laurent Mauborgne, Jan Reineke
	+ https://www.usenix.org/conference/usenixsecurity13/technical-sessions/paper/doychev
	+ https://github.com/cacheaudit/cacheaudit
* CacheD: Identifying Cache-Based Timing Channels in Production Software
	+ USENIX Security 2017
	+ Shuai Wang, Pei Wang, Xiao Liu, Danfeng Zhang, Dinghao Wu
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/wang-shuai
* CacheShield: Protecting Legacy Processes Against Cache Attacks
	+ 2017; Samira Briongos, Gorka Irazoqui, Pedro Malagón, Thomas Eisenbarth
	+ https://arxiv.org/abs/1709.01795
* Capability Hardware Enhanced RISC Insns (CHERI): Notes on the Meltdown and Spectre Attacks
	+ http://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-916.pdf
* ctgrind
	+ https://www.imperialviolet.org/2010/04/01/ctgrind.html
	+ https://github.com/agl/ctgrind/
* CTTK (Constant-Time Toolkit)
	+ https://github.com/pornin/CTTK
* Did we learn from LLC Side Channel Attacks? A Cache Leakage Detection Tool for Crypto Libraries
	+ 2017; Gorka Irazoqui, Kai Cong, Xiaofei Guo, Hareesh Khattri, Arun Kanuparthi, Thomas Eisenbarth, Berk Sunar
	+ https://arxiv.org/abs/1709.01552
* dudect: dude, is my code constant time? - https://github.com/oreparaz/dudect
* FaCT: A Flexible, Constant-Time Programming Language
	+ SecDev 2017
	+ Sunjay Cauligi, Gary Soeller, Fraser Brown, Brian Johannesmeyer, Yunlu Huang, Ranjit Jhala, Deian Stefan
	+ https://cseweb.ucsd.edu/~dstefan/pubs/cauligi:2017:fact.pdf
	+ https://github.com/PLSysSec/FaCT
* KASLR is Dead: Long Live KASLR
	+ Engineering Secure Software and Systems (ESSoS) 2017
	+ Daniel Gruss, Moritz Lipp, Michael Schwarz, Richard Fellner, Clémentine Maurice, Stefan Mangard 
	+ https://gruss.cc/files/kaiser.pdf
	+ https://github.com/IAIK/KAISER
* Mitigating Speculative Attacks in Crypto
	+ https://github.com/HACS-workshop/spectre-mitigations/blob/master/crypto_guidelines.md
* Mitigating speculative execution side channel hardware vulnerabilities
	+ https://blogs.technet.microsoft.com/srd/2018/03/15/mitigating-speculative-execution-side-channel-hardware-vulnerabilities/
* ParTI - Towards Combined Hardware Countermeasures against Side Channel and Fault Injection Attacks - CHES 2016 
	+ https://www.youtube.com/watch?v=wTJvb6k5yp0
* Provably secure compilation of side-channel countermeasures
	+ Cryptology ePrint Archive: Report 2017/1233
	+ Gilles Barthe, Benjamin Grégoire, Vincent Laporte
	+ https://eprint.iacr.org/2017/1233
	+ https://sites.google.com/view/ctpreservation
* Provably Secure Countermeasures against Side-channel Attacks
	+ 2015 Dissertation; Praveen Kumar Vadnala
	+ https://orbilu.uni.lu/bitstream/10993/21653/2/PraveenVadnala_Thesis.pdf
* Rigorous Analysis of Software Countermeasures against Cache Attacks
	+ PLDI 2017; Goran Doychev, Boris Köpf
	+ https://www.youtube.com/watch?v=GMyDEnpoyoI
	+ https://arxiv.org/abs/1603.02187
	+ http://software.imdea.org/~bkoepf/papers/pldi17.pdf
* Side Channel Analysis Protection and Low Latency in Action - Case Study of PRINCE and Midori
	+ https://www.youtube.com/watch?v=8OyQIh3F4AU
* Strong and Efficient Cache Side-Channel Protection using Hardware Transactional Memory - https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/gruss
* Towards Practical Tools for Side Channel Aware Software Engineering: "Grey Box" Modelling for Instruction Leakages
	+ USENIX Security 2017
	+ David McCann, Elisabeth Oswald, Carolyn Whitnall
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/mccann
* Why Constant-Time Crypto? - https://www.bearssl.org/constanttime.html
* Verifying Constant-Time Implementations
	+ USENIX Security 2016
	+ José Bacelar Almeida, Manuel Barbosa, Gilles Barthe, François Dupressoir, Michael Emmi
	+ https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/almeida
* Verifying Constant-Time Implementations by Abstract Interpretation
	+ European Symposium on Research in Computer Security 2017
	+ Sandrine Blazy, David Pichardie, Alix Trieu
	+ https://hal.inria.fr/hal-01588444
	+ https://link.springer.com/chapter/10.1007/978-3-319-66402-6_16

---

# Arithmetic Logic Unit (ALU)

* Constant-Time Multiplication - https://www.bearssl.org/ctmul.html
* When Constant-Time Source Yields Variable-Time Binary: Exploiting Curve25519-donna Built with MSVC 2015
	+ Cryptology and Network Security (CANS) 2016
	+ Thierry Kaufmann, Hervé Pelletier, Serge Vaudenay, Karine Villegas
	+ https://infoscience.epfl.ch/record/223794/files/32_1.pdf
	+ https://research.kudelskisecurity.com/2017/01/16/when-constant-time-source-may-not-save-you/
	+ https://www.semanticscholar.org/paper/When-Constant-Time-Source-Yields-Variable-Time-Bin-Kaufmann-Pelletier/4207ebe6f2656c1a40149ec446ca99885ce5b2ad

# Branch Predictor

* BranchScope: A New Side-Channel Attack on Directional Branch Predictor
	+ ASPLOS 2018
	+ Dmitry Evtyushkin, Ryan Riley, Nael Abu-Ghazaleh, Dmitry Ponomarev
	+ http://www.cs.ucr.edu/~nael/pubs/asplos18.pdf
* Covert Channels Through Branch Predictors: A Feasibility Study
	+ Hardware and Architectural Support for Security and Privacy (HASP) 2015
	+ Dmitry Evtyushkin, Dmitry Ponomarev, Nael Abu-Ghazaleh
	+ http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.702.6038&rep=rep1&type=pdf
	+ http://caslab.csl.yale.edu/workshops/hasp2015/slides_05_evtyushkin.pdf
* Jump Over ASLR: Attacking Branch Predictors to Bypass ASLR - http://www.cs.binghamton.edu/~dima/micro16.pdf
* On the Power of Simple Branch Prediction Analysis
	+ ASIACCS 2007
	+ Onur Aciiçmez, Çetin Kaya Koç, Jean-Pierre Seifert
	+ https://eprint.iacr.org/2006/351.pdf
	+ https://koclab.cs.ucsb.edu/docs/koc/c40.pdf
* PoC for breaking hypervisor ASLR using branch target buffer collisions - https://github.com/felixwilhelm/mario_baslr/
* Predicting Secret Keys via Branch Prediction
	+ CT-RSA 2007
	+ Onur Acıiçmez, Çetin Kaya Koç, Jean-Pierre Seifert
	+ https://eprint.iacr.org/2006/288.pdf
	+ https://koclab.cs.ucsb.edu/docs/koc/c39.pdf
	+ MSR talk: https://www.youtube.com/watch?v=rWFj4N6MaQw
* Understanding and Mitigating Covert Channels Through Branch Predictors
	+ TACO 13(1): 10 (2016)
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
* An Analytical Model for Time-Driven Cache Attacks
	+ Fast Software Encryption (FSE) 2007
	+ Kris Tiri, Onur Aciiçmez, Michael Neve, Flemming Andersen
	+ https://iacr.org/archive/fse2007/45930404/45930404.pdf
* ARMageddon: How Your Smartphone CPU Breaks Software-Level Security and Privacy
	+ Black Hat Europe 2016: https://www.youtube.com/watch?v=9KsnFWejpQg
	+ https://github.com/IAIK/armageddon
	+ thesis: https://www.blackhat.com/docs/eu-16/materials/eu-16-Lipp-ARMageddon-How-Your-Smartphone-CPU-Breaks-Software-Level-Security-And-Privacy-wp.pdf
	+ slides: https://www.blackhat.com/docs/eu-16/materials/eu-16-Lipp-ARMageddon-How-Your-Smartphone-CPU-Breaks-Software-Level-Security-And-Privacy.pdf
	+ https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/lipp
* C5: Cross-Cores Cache Covert Channel, 2015
	+ Detection of Intrusions and Malware, and Vulnerability Assessment
	+ http://www.s3.eurecom.fr/docs/dimva15_clementine.pdf
	+ https://link.springer.com/chapter/10.1007/978-3-319-20550-2_3
* Cache Attacks and Countermeasures: the Case of AES (Extended Version)
	+ RSA Conference Cryptographers' Track (CT-RSA) 2006
	+ Dag Arne Osvik, Adi Shamir and Eran Tromer
	+ https://www.cs.tau.ac.il/~tromer/papers/cache.pdf
* Cache side channel attacks - https://dreamsofastone.blogspot.com/2015/09/cache-side-channel-attacks.html
* Cache Side Channels: State of the Art and Research Opportunities
	+ CCS 2017
	+ Yinqian Zhang
	+ https://dl.acm.org/citation.cfm?doid=3133956.3136064
	+ http://web.cse.ohio-state.edu/~zhang.834/slides/tutorial17.pdf
* Flush+Flush: A Fast and Stealthy Cache Attack
	+ Detection of Intrusions and Malware & Vulnerability Assessment (DIMVA) 2016
	+ Daniel Gruss, Clémentine Maurice, Klaus Wagner, Stefan Mangard
	+ http://arxiv.org/abs/1511.04594
	+ https://github.com/IAIK/flush_flush
* FLUSH+RELOAD: A High Resolution, Low Noise, L3 Cache Side-Channel Attack 
	+ USENIX Security 2014
	+ Yuval Yarom, Katrina Falkner
	+ https://www.usenix.org/conference/usenixsecurity14/technical-sessions/presentation/yarom
	+ https://eprint.iacr.org/2013/448
* Hello from the Other Side: SSH over Robust Cache Covert Channels in the Cloud
	+ Network and Distributed System Security Symposium (NDSS) 2017
	+ Clémentine Maurice, Manuel Weber, Michael Schwarz, Lukas Giner, Daniel Gruss, Carlo Alberto Boano, Kay Römer, Stefan Mangard
	+ slides: https://gruss.cc/files/hello_ndss_slides.pdf
	+ https://github.com/IAIK/hello
	+ BH Asia 2017: https://www.youtube.com/watch?v=a9sGk7FtnYk
* Last-Level Cache Side-Channel Attacks are Practical
	+ 2015 IEEE Symposium on Security and Privacy
	+ Fangfei Liu, Yuval Yarom, Qian Ge, Gernot Heiser, Ruby B. Lee
	+ http://palms.ee.princeton.edu/system/files/SP_vfinal.pdf
	+ https://www.youtube.com/watch?v=vpGI1ggKzC4
* MeltdownPrime and SpectrePrime: Automatically-Synthesized Attacks Exploiting Invalidation-Based Coherence Protocols
	+ 2018 arXiv preprint
	+ Caroline Trippel, Daniel Lustig, Margaret Martonosi
	+ https://arxiv.org/abs/1802.03802
* MemJam: A False Dependency Attack against Constant-Time Crypto Implementations
	+ RSA Conference 2018
	+ Ahmad Moghimi, Thomas Eisenbarth, Berk Sunar
	+ https://arxiv.org/abs/1711.08002
* New Results on Instruction Cache Attacks
	+ Cryptographic Hardware and Embedded Systems (CHES) 2010
	+ Onur Aciiçmez, Billy Bob Brumley, Philipp Grabher
	+ https://www.iacr.org/archive/ches2010/62250105/62250105.pdf
* Return-Oriented Flush-Reload Side Channels on ARM and Their Implications for Android Devices
	+ CCS 2016
	+ Xiaokuan Zhang, Yuan Xiao, Yinqian Zhang
	+ http://web.cse.ohio-state.edu/~xiao.465/fp0501-zhang.pdf
	+ https://www.youtube.com/watch?v=tymvrJiJNl8
* Strong and Efficient Cache Side-Channel Protection using Hardware Transactional Memory - https://gruss.cc/files/cloak.pdf
* Yet Another MicroArchitectural Attack: Exploiting I-cache
	+ CSAW 2007
	+ Onur Aciiçmez
	+ http://eprint.iacr.org/2007/164

# DRAM

* Another Flip in the Wall of Rowhammer Defenses
	+ Security and Privacy S&P 2018
	+ D. Gruss, M. Lipp, M. Schwarz, D. Genkin, J. Juffinger, S. O'Connell, W. Schoechl, Y. Yarom
	+ https://csdl.computer.org/csdl/proceedings/sp/2018/4353/00/435301a489-abs.html
	+ https://arxiv.org/abs/1710.00551
	+ Tools for "Another Flip in the Wall" - https://github.com/IAIK/flipfloyd
* Connecting the Dots: Privacy Leakage via Write-Access Patterns to the Main Memory
	+ Hardware Oriented Security and Trust (HOST) 2017
	+ Tara Merin John, Syed Kamran Haider, Hamza Omar, Marten van Dijk
	+ https://arxiv.org/abs/1702.03965
* DRAMA: How Your DRAM Becomes a Security Problem
	+ slides: https://www.blackhat.com/docs/eu-16/materials/eu-16-Schwarz-How-Your-DRAM-Becomes-A-Security-Problem.pdf
	+ thesis: DRAMA: Exploiting DRAM Buffers for Fun and Profit - https://www.blackhat.com/docs/eu-16/materials/eu-16-Schwarz-How-Your-DRAM-Becomes-A-Security-Problem-wp.pdf
	+ Black Hat Europe 2016: https://www.youtube.com/watch?v=lSU6YzjIIiQ
	+ USENIX 2016: https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/pessl
* Drammer: Deterministic Rowhammer Attacks on Mobile Platforms
	+ CCS (2016)
	+ Victor van der Veen, Yanick Fratantonio, Martina Lindorfer, Daniel Gruss, Clementine Maurice, Giovanni Vigna, Herbert Bos, Kaveh Razavi, Cristiano Giuffrida 
	+ https://gruss.cc/files/drammer.pdf
	+ https://www.vusec.net/projects/drammer/
* Fantastic Timers and Where to Find Them: High-Resolution Microarchitectural Attacks in JavaScript
	+ Financial Cryptography and Data Security (FC) 2017
	+ Michael Schwarz, Clémentine Maurice, Daniel Gruss, Stefan Mangard
	+ paper: https://gruss.cc/files/fantastictimers.pdf
	+ slides: https://gruss.cc/files/timers_slides.pdf
* Flipping bits in memory without accessing them: an experimental study of DRAM disturbance errors
	+ ISCA 2014
	+ https://dl.acm.org/citation.cfm?id=2665726
	+ http://users.ece.cmu.edu/%7Eyoonguk/papers/kim-isca14.pdf
	+ https://github.com/CMU-SAFARI/rowhammer
* Hammertime: a software suite for testing, profiling and simulating the rowhammer DRAM defect - https://github.com/vusec/hammertime
* Rowhammer.js: A Remote Software-Induced Fault Attack in JavaScript
	+ Detection of Intrusions and Malware & Vulnerability Assessment (DIMVA) 2016
	+ http://arxiv.org/abs/1507.06955
	+ https://github.com/IAIK/rowhammerjs
* Throwhammer: Rowhammer Attacks over the Network and Defenses
	+ USENIX ATC (Annual Technical Conference) 2018
	+ Andrei Tatar, Radhesh Krishnan, Elias Athanasopoulos, Cristiano Giuffrida, Herbert Bos, Kaveh Razavi
	+ https://www.usenix.org/conference/atc18/presentation/tatar
	+ https://www.vusec.net/download/?t=papers/throwhammer_atc18.pdf
* Whispers in the Hyper-space: High-speed Covert Channel Attacks in the Cloud - https://www.usenix.org/conference/usenixsecurity12/technical-sessions/presentation/wu

# Electromagnetic (EM) Emanations

* A Method for Efficient Localization of Magnetic-field Sources Excited by the Execution of Instructions in a Processor
	+ 2017, IEEE Transactions on Electromagnetic Compatibility
	+ http://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2017/10/TEMC_245_2017.pdf
* Capacity of the EM Covert/Side-Channel Created by the Execution of Instructions in a Processor
	+ 2017, IEEE Transactions on Information Forensics and Security
	+ http://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2017/10/T-IFS-07378-2017.pdf
* Detailed Tracking of Program Control Flow Using Analog Side-Channel Signals: A Promise for IoT Malware Detection and a Threat for Many Cryptographic Implementations
	+ SPIE 2018
	+ Haider Adnan Khan, Monjur Alam, Alenka Zajic, Milos Prvulovic
	+ https://www.researchgate.net/publication/324584326_Detailed_Tracking_of_Program_Control_Flow_Using_Analog_Side-Channel_Signals_A_Promise_for_IoT_Malware_Detection_and_a_Threat_for_Many_Cryptographic_Implementations
* EDDIE: EM-Based Detection of Deviations in Program Execution
	+ 2017, Proceedings of the 44th International Symposium on Computer Architecture (ISCA)
	+ http://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2017/06/ISCA17.pdf
* Quantifying Information Leakage in a Processor Caused by the Execution of Instructions
	+ 2017, Proceedings of IEEE MILCOM
	+ http://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2017/10/MILCOM_Capacity.pdf
* Spectral Profiling: Observer-Effect-Free Profiling by Monitoring EM Emanations
	+ 2016, IEEE MICRO 16
	+ http://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2016/08/MICRO16.pdf
* The EM Side–Channel(s): Attacks and Assessment Methodologies
	+ 2002, Cryptographic Hardware and Embedded Systems (CHES)
	+ https://www.cs.jhu.edu/~astubble/600.412/s-c-papers/em.pdf
	+ http://citeseerx.ist.psu.edu/viewdoc/summary;?doi=10.1.1.122.1646
	+ https://www.semanticscholar.org/paper/The-EM-Side-Channel-s-Attacks-and-Assessment-Metho-Agrawal-Archambeault/7d687c23e297196e4de38240f9b48eb2d31f20fe
* Watch Me, but Don't Touch Me! Contactless Control Flow Monitoring via Electromagnetic Emanations
	+ 2017, Proceedings of the 2017 ACM SIGSAC Conference on Computer and Communications Security (CCS)
	+ https://arxiv.org/abs/1708.09099
* Zero-Overhead Profiling via Electromagnetic (EM) Emanations
	+ 2016, Proceedings of the 25th International Symposium on Software Testing and Analysis (ISSTA)
	+ https://dl.acm.org/citation.cfm?id=2931065
	+ https://issta2016.cispa.saarland/zero-overhead-profiling-via-em-emanations/
	+ http://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2016/09/ZoP.pdf

# Floating Point Unit (FPU)

* On Subnormal Floating Point and Abnormal Timing
	+ http://www.ieee-security.org/TC/SP2015/papers-archived/6949a623.pdf
	+ https://cseweb.ucsd.edu/~dkohlbre/papers/subnormal.pdf
	+ http://cseweb.ucsd.edu/~hovav/papers/akmjls15.html
	+ https://github.com/kmowery/libfixedtimefixedpoint
* On the effectiveness of mitigations against floating-point timing channels
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/kohlbrenner
	+ https://cseweb.ucsd.edu/~dkohlbre/floats/

# FPGA

* An Inside Job: Remote Power Analysis Attacks on FPGAs
	+ Cryptology ePrint Archive: Report 2018/012
	+ Falk Schellenberg, Dennis R.E. Gnad, Amir Moradi, Mehdi B. Tahoori
	+ https://eprint.iacr.org/2018/012
* Breakthrough Silicon Scanning Discovers Backdoor in Military Chip
	+ Cryptographic Hardware and Embedded Systems (CHES) 2012
	+ Sergei Skorobogatov, Christopher Woods
	+ https://www.cl.cam.ac.uk/~sps32/ches2012-backdoor.pdf
	+ https://www.cl.cam.ac.uk/~sps32/ches2012_slides.pdf
* Electromagnetic Side-channel Attack against 28-nm FPGA Device
	+ WISA (2012)
	+ Yohei Hori, Toshihiro Katashita, Akihiko Sasaki, Akashi Satoh
	+ https://staff.aist.go.jp/hori.y/articles/hori_wisa2012.pdf
* FPGA Side Channel Attacks without Physical Access
	+ FCCM 2018
	+ C. Ramesh, S. B. Patil, S. N. Dhanuskodi, G. Provelengios, S. Pillement, D. Holcomb, R. Tessier
	+ http://www.ecs.umass.edu/ece/tessier/ramesh-fccm18.pdf
* FPGA-Based Remote Power Side-Channel Attacks
	+ Security and Privacy S&P 2018
	+ Mark Zhao, G. Edward Suh
	+ https://csdl.computer.org/csdl/proceedings/sp/2018/4353/00/435301a805-abs.html
* Improved Side-Channel Analysis Attacks on Xilinx Bitstream Encryption of 5, 6, and 7 Series
	+ Constructive Side-Channel Analysis and Secure Design (COSADE) 2016
	+ Amir Moradi, Tobias Schneider
	+ https://www.emsec.rub.de/media/attachments/files/2017/04/AmirTalk_2016-04-14_COSADE.pdf
	+ https://eprint.iacr.org/2016/249
* Leaky Wires: Information Leakage and Covert Communication Between FPGA Long Wires
	+ AsiaCCS 2018
	+ Ilias Giechaskiel, Kasper B. Rasmussen, Ken Eguro
	+ http://arxiv.org/abs/1611.08882
	+ http://www.cs.ox.ac.uk/files/9835/fpga.pdf
* Side Channel Attack on Low Power FPGA Platform
	+ 2016 Master Thesis; Mustafa Faraj
	+ https://uwspace.uwaterloo.ca/bitstream/handle/10012/10769/Faraj_Mustafa.pdf?sequence=3

# GPU

* A complete key recovery timing attack on a GPU
	+ High Performance Computer Architecture (HPCA) 2016
	+ Zhen Hang Jiang, Yunsi Fei, David Kaeli
	+ https://doi.org/10.1109/HPCA.2016.7446081
* A Novel Side-Channel Timing Attack on GPUs
	+ Great Lakes Symposium on VLSI (GLSVLSI) 2017
	+ Zhen Hang Jiang, Yunsi Fei, David Kaeli
	+ https://doi.org/10.1145/3060403.3060462
* Confidentiality Issues on a GPU in a Virtualized Environment
	+ FC 2014: Financial Cryptography and Data Security
	+ Clémentine Maurice, Christoph Neumann, Olivier Heen, Aurélien Francillon
	+ http://www.eurecom.fr/en/publication/4205/detail/confidentiality-issues-on-a-gpu-in-a-virtualized-environment
* Constructing and Characterizing Covert Channels on GPGPUs
	+ MICRO-50, 2017
	+ Hoda Naghibijouybari, Khaled N. Khasawneh, Nael Abu-Ghazaleh
	+ http://www.cs.ucr.edu/~kkhas001/pubs/micro17-gpu.pdf
* CUDA Leaks: Information Leakage in GPU Architectures
	+ ACM Transactions on Embedded Computing Systems (TECS) 2016
	+ Roberto Di Pietro, Flavio Lombardi, Antonio Villani
	+ https://arxiv.org/abs/1305.7383
	+ https://dl.acm.org/citation.cfm?id=2801153
* GPU Security Exposed: Exploiting Shared Memory
	+ Black Hat Europe 2016
	+ Justin Taft
	+ https://www.blackhat.com/docs/eu-16/materials/eu-16-Taft-GPU-Security-Exposed.pdf
* RCoal: Mitigating GPU Timing Attack via Subwarp-based Randomized Coalescing Technique
	+ Proceedings of the 24th International Symposium on High-Performance Computer Architecture (HPCA), 2018
	+ Gurunath Kadam, [Danfeng Zhang](http://www.cse.psu.edu/~dbz5017/publication.html), [Adwait Jog](http://adwaitjog.github.io/pubs.html)
	+ http://adwaitjog.github.io/docs/pdf/rcoal-hpca18.pdf
	+ http://www.cse.psu.edu/~dbz5017/pub/hpca18.pdf

# Interrupts

* An Empirical Bandwidth Analysis of Interrupt-Related Covert Channels
	+ IJSSE 2015
	+ Richard Gay, Heiko Mantel, Henning Sudbrock
	+ https://www.semanticscholar.org/paper/An-Empirical-Bandwidth-Analysis-of-Interrupt-Relat-Gay-Mantel/d81d95e8969edd37a3f47335b98a9b6ce9e3942f
	+ http://www.mais.informatik.tu-darmstadt.de/WebBibPHP/papers/2013/2013-GayMantelSudbrock-EmpiricalIRCC.pdf

# Keyboard
* SoK: Keylogging Side Channels
	+ Security and Privacy S&P 2018
	+ J. Monaco
	+ https://csdl.computer.org/csdl/proceedings/sp/2018/4353/00/435301a420-abs.html
* KeyDrown: Eliminating Software-Based Keystroke Timing Side-Channel Attacks
	+ NDSS 2018
	+ Michael Schwarz, Moritz Lipp, Daniel Gruss, Samuel Weiser, Clémentine Maurice, Raphael Spreitzer, Stefan Mangard
	+ https://arxiv.org/abs/1706.06381
	+ https://www.ndss-symposium.org/wp-content/uploads/sites/25/2018/02/ndss2018_04B-1_Schwarz_paper.pdf
	+ http://wp.internetsociety.org/ndss/wp-content/uploads/sites/25/2018/03/NDSS2018_04B-1_Schwarz_Slides.pdf
	+ https://www.youtube.com/watch?v=limElEZNdS8

# Magnetic

* MAGNETO: Covert Channel between Air-Gapped Systems and Nearby Smartphones via CPU-Generated Magnetic Fields
	+ https://cyber.bgu.ac.il/advanced-cyber/airgap
	+ Mordechai Guri, Andrey Daidakulov, Yuval Elovici
	+ https://arxiv.org/abs/1802.02317
	+ Paper: https://arxiv.org/abs/1802.02317
	+ Video: https://www.youtube.com/watch?v=yz8E5n1Tzlo
* ODINI : Escaping Sensitive Data from Faraday-Caged, Air-Gapped Computers via Magnetic Fields
	+ https://cyber.bgu.ac.il/advanced-cyber/airgap
	+ Mordechai Guri, Boris Zadov, Andrey Daidakulov, Yuval Elovici 
	+ Paper: https://cyber.bgu.ac.il/advanced-cyber/system/files/ODINI_1.pdf
	+ Video: https://www.youtube.com/watch?v=h07iXD-aSCA

# Memory Bus

* GSMem: Data Exfiltration from Air-Gapped Computers over GSM Frequencies
	+ USENIX Security 2015
	+ Mordechai Guri, Assaf Kachlon, Ofer Hasson, Gabi Kedma, Yisroel Mirsky, Yuval Elovici
	+ https://www.usenix.org/conference/usenixsecurity15/technical-sessions/presentation/guri
	+ System Bus Radio: Transmits AM radio on computers without radio transmitting hardware
		- https://github.com/fulldecent/system-bus-radio
* Whispers in the hyper-space: high-speed covert channel attacks in the cloud, USENIX Security 2012
	+ https://www.usenix.org/conference/usenixsecurity12/technical-sessions/presentation/wu
	+ https://www.youtube.com/watch?v=d2TU_Q4U9DA

# Memory Order Buffer (MOB)

* Microarchitectural Minefields: 4K-Aliasing Covert Channel and Multi-Tenant Detection in IaaS Clouds
	+ NDSS 2018
	+ Dean Sullivan, Orlando Arias, Travis Meade, Yier Jin
	+ http://wp.internetsociety.org/ndss/wp-content/uploads/sites/25/2018/02/ndss2018_06A-3_Sullivan_paper.pdf
	+ http://wp.internetsociety.org/ndss/wp-content/uploads/sites/25/2018/03/NDSS2018-06A-3_Sullivan_Slides.pdf
	+ https://www.youtube.com/watch?v=0KIojo5nk2s

# Memory Management Unit (MMU)

* ASLR on the Line: Practical Cache Attacks on the MMU
	+ B. Gras, K. Razavi, E. Bosman, H. Bos, C. Giuffrida; NDSS, 2017
	+ https://www.vusec.net/download/?t=papers/anc_ndss17.pdf
	+ 34C3 (2017)
		- https://media.ccc.de/v/34c3-9135-aslr_on_the_line
		- https://github.com/brainsmoke/pub-archive/raw/master/slides/aotl-34c3-slides.pdf
* Malicious Management Unit: Why Stopping Cache Attacks in Software is Harder Than You Think
	+ van Schaik, S.; Giuffrida, C.; Bos, H.; Razavi, K.
	+ USENIX Security 2018
	+ https://bibbase.org/network/publication/vanschaik-giuffrida-bos-razavi-maliciousmanagementunitwhystoppingcacheattacksinsoftwareisharderthanyouthink-2018
* Reverse Engineering Hardware Page Table Caches Using Side-Channel Attacks on the MMU
	+ S. van Schaik, K. Razavi, B. Gras, H. Bos, C. Giuffrida, VU Amsterdam, 2017.
	+ https://www.vusec.net/download/?t=papers/revanc_ir-cs-77.pdf
* Telling Your Secrets without Page Faults: Stealthy Page Table-Based Attacks on Enclaved Execution
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/van-bulck
	+ https://github.com/jovanbulck/sgx-pte

# Power

* On Code Execution Tracking via Power Side-Channel
	+ Conference on Computer and Communications Security (CCS) 2016
	+ Yannan Liu, Lingxiao Wei, Zhe Zhou, Kehuan Zhang, Wenyuan Xu, Qiang Xu
	+ https://dl.acm.org/citation.cfm?id=2978299
	+ https://www.youtube.com/watch?v=YwL_p3TxhlA

# Prefetch

* Harmful prefetch on Intel - http://blog.ioactive.com/2017/01/harmful-prefetch-on-intel.html
* Prefetch Side-Channel Attacks: Bypassing SMAP and Kernel ASLR
	+ Conference on Computer and Communications Security (CCS) 2016
	+ Daniel Gruss, Anders Fogh, Clémentine Maurice, Moritz Lipp, Stefan Mangard 
	+ https://gruss.cc/files/prefetch.pdf
	+ https://www.youtube.com/watch?v=TJTQbs3oJx8
* Using Undocumented CPU Behavior to See Into Kernel Mode and Break KASLR in the Process
	+ https://www.youtube.com/watch?v=Pwq0vv4X7m4
	+ https://www.blackhat.com/docs/us-16/materials/us-16-Fogh-Using-Undocumented-CPU-Behaviour-To-See-Into-Kernel-Mode-And-Break-KASLR-In-The-Process.pdf

# Pseudo-Random Number Generator (PRNG)

* Covert Channels through Random Number Generator: Mechanisms, Capacity Estimation and Mitigations
	+ http://www.cs.binghamton.edu/~dima/ccs16.pdf
	+ CCS 2016: https://www.youtube.com/watch?v=G1xzG43mkZU

# SGX

* Cache Attacks on Intel SGX - https://www1.informatik.uni-erlangen.de/filepool/projects/sgx-timing/sgx-timing.pdf
* CacheZoom: How SGX Amplifies The Power of Cache Attacks 
	+ 2017; Ahmad Moghimi, Gorka Irazoqui, Thomas Eisenbarth
	+ https://arxiv.org/abs/1703.06986
* Inferring Fine-grained Control Flow Inside SGX Enclaves with Branch Shadowing
	+ USENIX Security 2017
	+ Skylake's BTB parameters, use of Intel PT and LBR
	+ https://arxiv.org/abs/1611.06952
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/lee-sangho
* Leaky Cauldron on the Dark Land: Understanding Memory Side-Channel Hazards in SGX
	+ CCS 2017
	+ Wenhao Wang, Guoxing Chen, Xiaorui Pan, Yinqian Zhang, XiaoFeng Wang, Vincent Bindschaedler, Haixu Tang, Carl A. Gunter
	+ http://web.cse.ohio-state.edu/~zhang.834/papers/ccs17b.pdf
	+ https://acmccs.github.io/papers/p2421-wangA.pdf
* Malware Guard Extension: Using SGX to Conceal Cache Attacks - https://arxiv.org/abs/1702.08719
* Racing in Hyperspace: Closing Hyper-Threading Side Channels on SGX with Contrived Data Races 
	+ IEEE S&P (Oakland) 2018
	+ Guoxing Chen, Wenhao Wang, Tianyu Chen, Sanchuan Chen, Yinqian Zhang, XiaoFeng Wang, Ten-Hwang Lai, Dongdai Lin
	+ https://web.cse.ohio-state.edu/~zhang.834/papers/sp18.pdf
	+ https://csdl.computer.org/csdl/proceedings/sp/2018/4353/00/435301a388.pdf
* SgxPectre Attacks: Leaking Enclave Secrets via Speculative Execution
	+ 2018 arXiv; Guoxing Chen, Sanchuan Chen, Yuan Xiao, Yinqian Zhang, Zhiqiang Lin, Ten H. Lai
	+ https://arxiv.org/abs/1802.09085
	+ https://github.com/osusecLab/SgxPectre
* Side Channels on Intel SGX - https://web.cse.ohio-state.edu/~zhang.834/projects/sgx-side-channels.html

# SMT

* Cache missing for fun and profit
	+ BSDCan 2005; Colin Percival
	+ http://www.daemonology.net/papers/cachemissing.pdf
* Cheap Hardware Parallelism Implies Cheap Security
	+ Fault Diagnosis and Tolerance in Cryptography (FDTC) 2007
	+ Onur Acıçmez, Jean-Pierre Seifert
	+ http://conferenze.dei.polimi.it/FDTC07/Aciicmez.pdf
* Covert Shotgun: Automatically finding covert channels in SMT - https://cyber.wtf/2016/09/27/covert-shotgun/

# Speculation

* Covert and Side Channels due to Processor Architecture
	+ Annual Computer Security Applications Conference ACSAC 2006
	+ Zhenghong Wang, Ruby B. Lee
	+ http://ieeexplore.ieee.org/document/4041191/
	+ http://www.acsac.org/2006/papers/127.pdf
* Meltdown & Spectre (2018)
	+ Meltdown - https://meltdownattack.com/
		- Moritz Lipp, Michael Schwarz, Daniel Gruss, Thomas Prescher, Werner Haas, Stefan Mangard, Paul Kocher, Daniel Genkin, Yuval Yarom, Mike Hamburg
		- https://meltdownattack.com/meltdown.pdf
		- https://arxiv.org/abs/1801.01207
		- Meltdown Proof-of-Concept - https://github.com/IAIK/meltdown
		- http://blog.cyberus-technology.de/posts/2018-01-03-meltdown.html
	+ Spectre Attacks: Exploiting Speculative Execution - https://spectreattack.com/
		- Paul Kocher, Daniel Genkin, Daniel Gruss, Werner Haas, Mike Hamburg, Moritz Lipp, Stefan Mangard, Thomas Prescher, Michael Schwarz, Yuval Yarom
		- https://spectreattack.com/spectre.pdf
		- https://arxiv.org/abs/1801.01203
	+ Reading privileged memory with a side-channel - Jann Horn
		- https://googleprojectzero.blogspot.com/2018/01/reading-privileged-memory-with-side.html
		- Google Project Zero PoC: https://bugs.chromium.org/p/project-zero/issues/detail?id=1272
	+ Spectre and Meltdown: Data leaks during speculative execution - Real World Crypto 2018, Jann Horn (Google Project Zero)
		- https://www.youtube.com/watch?v=6O8LTwVfTVs
	+ Paul Kocher: Spectre Mitigations in Microsoft's C/C++ Compiler
		- https://www.paulkocher.com/doc/MicrosoftCompilerSpectreMitigation.html
	+ ARM Whitepaper "Cache Speculation Side-channels" - https://developer.arm.com/support/security-update/download-the-whitepaper 
	+ Behind the scenes of a bug collision - https://cyber.wtf/2018/01/05/behind-the-scene-of-a-bug-collision/
	+ CPU security bugs caused by speculative execution - https://github.com/marcan/speculation-bugs
	+ Intel Analysis of Speculative Execution Side Channels - https://newsroom.intel.com/wp-content/uploads/sites/11/2018/01/Intel-Analysis-of-Speculative-Execution-Side-Channels.pdf
	+ meltdownspectre-patches: summary of the patch status - https://github.com/hannob/meltdownspectre-patches
	+ More details about mitigations for the CPU Speculative Execution issue - https://security.googleblog.com/2018/01/more-details-about-mitigations-for-cpu_4.html
	+ Retpoline: a software construct for preventing branch-target-injection - https://support.google.com/faqs/answer/7625886
	+ How Performance Optimizations Shatter Security Boundaries
		- QCon London 2018; Moritz Lipp
		- https://www.infoq.com/presentations/spectre-meltdown-security
* Out-of-Order Execution and Its Applications - Sophia D'Antoine, DeepSec 2017
	+ https://www.sophia.re/ROOTS/
	+ https://deepsec.net/docs/Slides/2017/Out-Of-Order_Execution_and_its_applications_Sophia_dAntoine.pdf
	+ https://deepsec.net/docs/Slides/2017/Out-Of-Order_Execution_and_its_applications_Sophia_dAntoine.pptx

# Thermal

* On the capacity of thermal covert channels in multicores - https://dl.acm.org/citation.cfm?id=2901322
* Thermal Covert Channels on Multi-core Platforms - https://www.usenix.org/conference/usenixsecurity15/technical-sessions/presentation/masti

# Translation Lookaside Buffer (TLB)

* Translation Leak-aside Buffer: Defeating Cache Side-channel Protections with TLB Attacks
	+ Gras, B.; Razavi, K.; Bos, H.; Giuffrida, C.
	+ USENIX Security 2018
	+ https://bibbase.org/network/publication/gras-razavi-bos-giuffrida-translationleakasidebufferdefeatingcachesidechannelprotectionswithtlbattacks-2018

# TSX

* Breaking Kernel Address Space Layout Randomization with Intel TSX
	+ https://sslab.gtisc.gatech.edu/assets/papers/2016/jang:drk-ccs.pdf
	+ http://www.cc.gatech.edu/~yjang37/assets/papers/2016/jang:drk-ccs.pdf
	+ decoded icache (caches decoded micro-ops) - inside L1 icache, virtually-indexed and virtually tagged (VIVT), does not require an iTLB access for address translation
* Prime+Abort: A Timer-Free High-Precision L3 Cache Attack using Intel TSX
	+ USENIX Security 2017
	+ Craig Disselkoen, David Kohlbrenner, Leo Porter, Dean Tullsen
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/disselkoen

# Talks

## 2018

* Beyond Belief: The Case of Spectre and Meltdown
	+ [BlueHatIL](http://www.bluehatil.com/abstracts.html) 2018
	+ Daniel Gruss, Moritz Lipp, Michael Schwarz
	+ https://www.youtube.com/watch?v=_4O0zMW-Zu4
	+ http://www.bluehatil.com/files/Beyond%20Belief%20-%20The%20Case%20of%20Spectre%20and%20Meltdown.pdf
* Exploiting modern microarchitectures: Meltdown, Spectre, and other hardware attacks
	+ Jon Masters, Red Hat, Stanford EE380, Jan 31 2018
	+ https://www.youtube.com/watch?v=zuBw1HFJMsM
	+ http://web.stanford.edu/class/ee380/Abstracts/180131.html
	+ http://web.stanford.edu/class/ee380/Abstracts/180131-slides.pdf
* Spectre: Exploiting Speculative Execution
	+ SiFive Tech Talk: Paul Kocher
	+ January 31, 2018
	+ https://www.youtube.com/watch?v=hqIavX_SCWc

## 2017

* Android Security Symposium 2017 - Drammer: Flip Feng Shui goes mobile (Victor van der Veen)
	+ https://www.youtube.com/watch?v=Zyqq2hj9zrc
* HackPra 2017 - Anders Fogh: "Covert shotgun: Automatically finding covert channels in SMT"
	+ https://www.youtube.com/watch?v=oVmPQCT5VkY
	+ https://cyber.wtf/2016/09/27/covert-shotgun/
* HackPra 2017 - Victor van der Veen: "Drammer: The Making-Of" - https://www.youtube.com/watch?v=DF0k9yKYwfo
* hardwear.io 2017 - Shaking Trust in Hardware - Ben Gras & Kaveh Razavi
	+ https://www.vusec.net/2017/12/recorded-talk-trusting-hardware-ffs-anc/
	+ https://www.youtube.com/watch?v=CWXL3tX00aU
* HITB2017AMS D1T1 - Drammer: The Making Of - Victor van der Veen
	+ https://www.youtube.com/watch?v=_oCEpfw1IPM
* Papers We Love Singapore #026 (2017) - Row Hammer: Flipping Bits in Memory Without Accessing Them
	+ https://www.youtube.com/watch?v=1iBpLhFN_OA
	+ https://speakerdeck.com/burnflare/row-hammer-papers-we-love
* RuhrSec 2017: "A new categorization system for Side-channel attacks on mobile devices & more", Dr. Veelasha Moonsamy
	+ https://www.youtube.com/watch?v=YxikZkZ6KuE
* RuhrSec 2017: "Rowhammer Attacks: A Walkthrough Guide", Dr. Clémentine Maurice & Daniel Gruss
	+ https://www.youtube.com/watch?v=-33gCDrSl_Q
* RuhrSec 2017: "Using Microarchitectural Design to Break KASLR and More", Anders Fogh
	+ https://www.youtube.com/watch?v=LyiB1jlUdN8
* USENIX Security '17 - Strong and Efficient Cache Side-Channel Protection using Hardware Transactional Memory
	+ https://www.youtube.com/watch?v=4_-c7ueHHqc
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/gruss

## 2016

* Black Hat 2016 - ARMageddon: How Your Smartphone CPU Breaks Software-Level Security and Privacy - https://www.youtube.com/watch?v=9KsnFWejpQg
* Black Hat 2016 - Side-Channel Attacks on Everyday Applications - Taylor Hornby
	+ https://github.com/defuse/flush-reload-attacks
	+ https://www.blackhat.com/docs/us-16/materials/us-16-Hornby-Side-Channel-Attacks-On-Everyday-Applications.pdf
	+ https://www.blackhat.com/docs/us-16/materials/us-16-Hornby-Side-Channel-Attacks-On-Everyday-Applications-wp.pdf
	+ https://www.youtube.com/watch?v=GPwNFrpd1KU
* CCS 2016 - CREDAL: Towards Locating a Memory Corruption Vulnerability with Your Core Dump - https://www.youtube.com/watch?v=jOL4oElUKjA
* CCS 2016 - Drammer: Deterministic Rowhammer Attacks on Mobile Platforms - https://www.youtube.com/watch?v=lTaMvBN1PoA
* CCS 2016 - ECDSA Key Extraction from Mobile Devices via Nonintrusive Physical Side Channels - https://www.youtube.com/watch?v=0SQUQbth5vU
* CCS 2016 - On Code Execution Tracking via Power Side-Channel - https://www.youtube.com/watch?v=YwL_p3TxhlA
* CHES 2016 - Curious case of Rowhammer Flipping Secret Exponent Bits using Timing Analysis - https://www.youtube.com/watch?v=8x2qodFfY5s
* Clémentine Maurice: "Reverse-engineering CPUs for fun and profit" - https://www.youtube.com/watch?v=IT6PFSRrvsU
* Daniel Gruss – Microarchitectural Incontinence - You would leak too if you were so fast! - https://www.youtube.com/watch?v=cAWmNp3Ukqk
* DEF CON 24 2016 Side channel attacks on high security electronic safe locks - https://www.youtube.com/watch?v=vJ9NdvKYxeg
* HITB2016AMS CLOSING KEYNOTE - Hardware Side Channels in Virtualized Environments - Sophia D'Antoine - https://www.youtube.com/watch?v=1KteO7FPXYw
* HITB2016AMS D2T1 - Cache Side Channel Attacks: CPU Design As A Security Problem - Anders Fogh
	+ https://www.youtube.com/watch?v=UH6dFbiX_hM
	+ https://conference.hitb.org/hitbsecconf2016ams/materials/D2T1%20-%20Anders%20Fogh%20-%20Cache%20Side%20Channel%20Attacks.pdf
* Fastly Security Speaker Series 2016 - Jasper van Woudenberg on Side channel analysis and fault injection - https://www.youtube.com/watch?v=bu59ya8nOBM
* Return-Oriented Flush-Reload Side Channels on ARM and Their Implications for Android Devices - https://www.youtube.com/watch?v=tymvrJiJNl8
* RuhrSec 2016: "Cache Side-Channel Attacks and the case of Rowhammer", Daniel Gruss - https://www.youtube.com/watch?v=gxsguH5opsM
* Side-Channel Attacks on Everyday Applications - https://www.youtube.com/watch?v=GPwNFrpd1KU
* Three lessons that I learnt from Rowhammer - with implications for future security research - Thomas Dullien (Halvar Flake) - Null Singapore - https://www.youtube.com/watch?v=fkDD2ea7SD8
* Using Undocumented CPU Behavior to See Into Kernel Mode and Break KASLR in the Process - https://www.youtube.com/watch?v=Pwq0vv4X7m4 - 
* What could possibly go wrong with {insert x86 instruction here}? [33c3] - https://www.youtube.com/watch?v=wue4QomGE74

## 2015

* Clémentine Maurice, Daniel Gruss: Rowhammer.js: Root privileges for web apps? - https://www.youtube.com/watch?v=9L5MJ43nbkI
* Controlled-Channel Attacks: Deterministic Side Channels for Untrusted Operating Systems - https://www.youtube.com/watch?v=fwUaN5ik8zE
* DEF CON 23 - Etienne Martineau - The art of cache timing covert channel on x86 multi core - https://www.youtube.com/watch?v=7X772EBdvnM
* Exploiting Out-of-Order Execution For Covert Cross-VM Communication - Black Hat 2015
	+ https://www.youtube.com/watch?v=SjcKqVRjNHc
	+ https://www.blackhat.com/docs/us-15/materials/us-15-DAntoine-Exploiting-Out-Of-Order-Execution-For-Covert-Cross-VM-Communication.pdf
* Exploiting the DRAM Rowhammer Bug to Gain Kernel Privileges - Mark Seaborn, Halvar Flake - Black Hat 2015
	+ https://www.youtube.com/watch?v=0U7511Fb4to
* Last-Level Cache Side-Channel Attacks are Practical - https://www.youtube.com/watch?v=vpGI1ggKzC4
* REcon 2015 - Exploiting Out of Order Execution (Sophia D'Antoine)
	+ https://www.youtube.com/watch?v=AbRoWa_xrzA
	+ https://recon.cx/2015/slides/recon2015-06-sophia-d-antoine-Exploiting-Out-of-Order-Execution.pdf
* S$A: A Shared Cache Attack That Works across Cores and Defies VM Sandboxing -- and Its Application to AES - https://www.youtube.com/watch?v=mwMjn8niX-Y
* Side-Channel Attacks by Differential Power Analysis - Nathaniel Graff - https://www.youtube.com/watch?v=bHncSnHQleY

## 2014

* MIT 6.858 Computer Systems Security, Fall 2014 - Lecture 16. Side-Channel Attacks - https://www.youtube.com/watch?v=PuVMkSEcPiI

## 2009

* Defcon 17 - Sniff Keystrokes With Lasers/Voltmeters - Side Channel Attacks Using Optical Sampling
	+ paper: https://www.defcon.org/images/defcon-17/dc-17-presentations/Andrea_Barisani-Daniele_%20Bianco/defcon-17-barisani-bianco-sniff_keystrokes-wp.pdf
	+ slides: https://www.defcon.org/images/defcon-17/dc-17-presentations/defcon-17-barisani-bianco-sniff_keystrokes.pdf
	+ video: https://www.youtube.com/watch?v=Amnv4ncqKtA
