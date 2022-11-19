# [C++ links](README.md): computer architecture - microarchitectural channels

See also: [Computer Architecture](comparch.md)

- Leakage channels: side channels (accidental), covert channels (deliberate).
- Storage channels (functional behavior), timing channels (temporal behavior).
- Timing-based channels (operations timing), access-based channels (direct information access), trace-based channels (program execution measurement).

# Contents

- [General](#general)
- [Defense, Mitigation, Protection](#defense-mitigation-protection)

---

- [Arithmetic Logic Unit (ALU)](#arithmetic-logic-unit-alu)
- [Branch Predictor](#branch-predictor)
- [Cache](#cache)
- [DRAM](#dram)
- [Electromagnetic (EM) Emanations](#electromagnetic-em-emanations)
- [Floating Point Unit (FPU)](#floating-point-unit-fpu)
- [FPGA](#fpga)
- [Frontend](#frontend)
- [GPU](#gpu)
- [Interconnect](#interconnect)
- [Interrupts](#interrupts)
- [Keyboard](#keyboard)
- [Magnetic](#magnetic)
- [Memory Bus](#memory-bus)
- [Memory Management Unit (MMU)](#memory-management-unit-mmu)
- [Memory Order Buffer (MOB)](#memory-order-buffer-mob)
- [Micro-Op Cache](#micro-op-cache)
- [Power](#power)
- [Prefetch](#prefetch)
- [Pseudo-Random Number Generator (PRNG)](#pseudo-random-number-generator-prng)
- [Reorder Buffer (ROB)](reorder-buffer-rob)
- [Return Stack Buffer (RSB)](#return-stack-buffer-rsb)
- [Scheduler](#scheduler)
- [SMT](#smt)
- [Speculation](#speculation)
- [Store Buffer](#store-buffer)
- [Thermal](#thermal)
- [Translation Lookaside Buffer (TLB)](#translation-lookaside-buffer-tlb)
- [Trusted Execution Environments (TEEs)](#trusted-execution-environments-tees): [Arm TrustZone](#arm-trustzone), [Intel SGX](#intel-sgx)
- [TSX](#tsx)
- [Talks](#talks)

---

# General

- MASCAB: a Micro-Architectural Side-Channel Attack Bibliography
	- Daniel Page
	- https://github.com/danpage/mascab
- Memory Systems attacks/mitigations research papers
	- Biswabandan Panda
	- https://www.cse.iitk.ac.in/users/biswap/SMS.html

## General: 2022

- Doing Research in Computer Architecture Security: A Starter Kit
	- Computer Architecture Today 2022
	- Mengjia Yan
	- https://www.sigarch.org/doing-research-in-computer-architecture-security-a-starter-kit/
- Rapid Prototyping for Microarchitectural Attacks
	- USENIX Security 2022
	- Catherine Easdon, Michael Schwarz, Martin Schwarzl, Daniel Gruss
	- https://www.cattius.com/images/rapid-prototyping.pdf
	- https://github.com/libtea/frameworks
	- libtea (Transient Execution Attack library): a framework for rapid prototyping of microarchitectural attacks on Linux, compatible with x86 (32-bit and 64-bit, Intel and AMD CPUs) and AArch64.
	- SCFirefox: a framework for rapid prototyping of browser-based microarchitectural attacks on Linux; adds libtea attack primitives to Firefox's JavaScript engine, SpiderMonkey.

## General: 2021

- Computing with Time: Microarchitectural Weird Machines
	- Architectural Support for Programming Languages and Operating Systems (ASPLOS) 2021
	- Dmitry Evtyushkin, Thomas Benjamin, Jesse Elwell, Jeffrey A. Eitel, Angelo Sapello, Abhrajit Ghosh
	- https://doi.org/10.1145/3445814.3446729
- Exploiting Microarchitectural Optimizations from Software
	- 2021 Ph.D. Dissertation
	- Moritz Lipp
	- https://mlq.me/download/phd-thesis.pdf
- Opening Pandora’s Box: A Systematic Study of New Ways Microarchitecture Can Leak Private Data
	- International Symposium on Computer Architecture (ISCA) 2021
	- Jose Rodrigo Sanchez Vicarte, Pradyumna Shome, Nandeeka Nayak, Caroline Trippel, Adam Morrison, David Kohlbrenner, Christopher W. Fletcher
	- https://www.cs.tau.ac.il/~mad/publications/isca2021-pandora.pdf
	- https://conferences.computer.org/iscapub/pdfs/ISCA2021-4ghucdBnCWYB7ES2Pe4YdT/333300a347/333300a347.pdf
	- https://github.com/FPSG-UIUC/Pandora
- Osiris: Automated Discovery of Microarchitectural Side Channels
	- USENIX Security 2021
	- Daniel Weber, Ahmad Ibrahim, Hamed Nemati, Michael Schwarz
	- https://arxiv.org/abs/2106.03470
	- https://www.usenix.org/conference/usenixsecurity21/presentation/weber
	- https://publications.cispa.saarland/3431/1/main.pdf
	- https://github.com/cispa/osiris
- SoK: In Search of Lost Time: A Review of JavaScript Timers in Browsers
	- IEEE European Symposium on Security and Privacy (EuroS&P) 2021
	- Thomas Rokicki, Clémentine Maurice, Pierre Laperdrix
	- https://hal.inria.fr/hal-03215569/
	- https://cmaurice.fr/pdf/eurosp21_rokicki.pdf
	- https://github.com/thomasrokicki/in-search-of-lost-time

## General: 2020

- Communication Model and Capacity Limits of Covert Channels Created by Software Activities
	- IEEE Transactions on Information Forensics and Security (TIFS) 2020
	- Baki Yilmaz, Milos Prvulovic, Alenka Zajic
	- https://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2020/01/T-IFS-10205-2019.R1.pdf
- Revisiting Isolated and Trusted Execution via Microarchitectural Cryptanalysis
	- 2020 PhD Dissertation
	- Daniel Moghimi
	- https://digital.wpi.edu/show/w9505326n

## General: 2019

- Software-based Side-Channel Attacks and Defenses in Restricted Environments
	- 2019 PhD Thesis
	- Michael Schwarz
	- https://misc0110.net/web/files/phd_thesis.pdf
- Survey of Microarchitectural Side and Covert Channels, Attacks, and Defenses
	- Journal of Hardware and Systems Security 3(3) 2019
	- Jakub Szefer
	- https://par.nsf.gov/biblio/10077357
	- https://caslab.csl.yale.edu/publications/szefer2018surey.pdf
	- 2016 preprint: http://eprint.iacr.org/2016/479
	- https://link.springer.com/article/10.1007/s41635-018-0046-1

## General: 2018

- A Survey of Microarchitectural Timing Attacks and Countermeasures on Contemporary Hardware
	- Q.Ge, Y. Yarom, D. Cock, and G. Heiser
	- Journal of Cryptographic Engineering 8 (1) 2018
		- http://dx.doi.org/10.1007/s13389-016-0141-6
	- Cryptology ePrint Archive, Report 2016/613
		- http://eprint.iacr.org/2016/613
		- https://ts.data61.csiro.au/publications/csiro_full_text/Ge_YCH_18.pdf
		- http://eprint.iacr.org.metacomment.io/2016/613
- A Systematic Evaluation of Transient Execution Attacks and Defenses
	- arXiv 2018
	- Claudio Canella, Jo Van Bulck, Michael Schwarz, Moritz Lipp, Benjamin von Berg, Philipp Ortner, Frank Piessens, Dmitry Evtyushkin, Daniel Gruss
	- https://arxiv.org/abs/1811.05441
- Systematic Classification of Side-Channel Attacks: A Case Study for Mobile Devices
	- IEEE Communications Surveys & Tutorials 20(1) 2018
	- Raphael Spreitzer, Veelasha Moonsamy, Thomas Korak, Stefan Mangard
	- https://arxiv.org/abs/1611.03748

## General: 2017

- A Survey of Timing Channels and Countermeasures
	- ACM Computing Surveys (CSUR) Volume 50 Issue 1 (2017)
	- Arnab Kumar Biswas, Diapk Ghosal, Shishir Nagaraja
	- https://dl.acm.org/citation.cfm?id=3023872
	- https://strathprints.strath.ac.uk/66223/1/Biswas_etal_ACM_CS_2017_A_survey_of_timing_channels_and_countermeasures.pdf
- Cross-core Microarchitectural Side Channel Attacks and Countermeasures
	- 2017 Ph.D. Dissertation
	- Gorka Irazoqui
	- https://web.wpi.edu/Pubs/ETD/Available/etd-042417-114714/unrestricted/girazoki.pdf
- Negative Result: Reading Kernel Memory From User Mode
	- 2017
	- Anders Fogh
	- https://cyber.wtf/2017/07/28/negative-result-reading-kernel-memory-from-user-mode/
- Software-based Microarchitectural Attacks
	- 2017 PhD dissertation
	- Daniel Gruss
	- https://gruss.cc/files/phd_thesis.pdf
	- slides: https://gruss.cc/files/phd_defense_slides.pdf
- Your Processor Leaks Information - and There's Nothing You Can Do About It
	- arXiv 2017
	- Qian Ge, Yuval Yarom, Frank Li, Gernot Heiser
	- https://arxiv.org/abs/1612.04474

## General: 2016

- Mastik: A Micro-Architectural Side-Channel Toolkit
	- http://cs.adelaide.edu.au/~yval/Mastik/
	- http://cryptologie.net/article/366/ches-2016-tutorial-part-1-common-criteria-certification-of-a-smartcard-a-technical-overview/
	- https://cryptologie.net/article/367/ches-2016-tutorial-part-2-micro-architectural-side-channel-attacks/
	- - Microarchitectural Side-Channel Attacks
		- CHES 2016 tutorial
		- Yuval Yarom
		- https://cs.adelaide.edu.au/~yval/Mastik/presentations/CHES16-Tutorial.pptx
		- https://cs.adelaide.edu.au/~yval/Mastik/presentations/CHES16-Tutorial2.pptx

## General: 2015

- Exploiting processor side channels to enable cross VM malicious code execution
	- 2015 Master's Thesis
	- Sophia M. D'Antoine
	- http://digitool.rpi.edu:8881/dtl_publish/15/175977.html
	- https://www.sophia.re/thesis.pdf
	- https://www.blackhat.com/docs/us-15/materials/us-15-DAntoine-Exploiting-Out-Of-Order-Execution-For-Covert-Cross-VM-Communication-wp.pdf
- Understanding contention-based channels and using them for defense
	- HPCA 2015
	- Hunger, C., Kazdagli, M., Rawat, A., Dimakis, A., Vishwanath, S., Tiwari, M.
	- http://users.ece.utexas.edu/~tiwari/pubs/HPCA-15-contention.pdf

## General: 2014

- The Last Mile: An Empirical Study of Timing Channels on seL4
	- CCS 2014
	- David Cock, Qian Ge, Toby Murray, Gernot Heiser
	- https://ts.data61.csiro.au/publications/nictaabstracts/Cock_GMH_14.abstract.html
	- http://research.davidcock.fastmail.fm/slides/lastmile.pdf
	- https://ts.data61.csiro.au/projects/TS/timeprotection/

## General: 2009

- Microarchitectural Attacks and Countermeasures
	- Cryptographic Engineering (2009)
	- Onur Acıiçmez, Çetin Kaya Koç
	- https://link.springer.com/chapter/10.1007/978-0-387-71817-0_18

## General: 1973

- A Note on the Confinement Problem
	- Communications of the ACM (CACM) 1973
	- Butler W. Lampson
	- http://bwlampson.site/11-Confinement/Abstract.html

---

# Defense, Mitigation, Protection

- Guidelines for Mitigating Timing Side Channels Against Cryptographic Implementations
	- https://software.intel.com/security-software-guidance/insights/guidelines-mitigating-timing-side-channels-against-cryptographic-implementations
- Hardware and Architectural Support for Security and Privacy (HASP)
	- http://caslab.csl.yale.edu/workshops/hasp2018/
- Hardware and Firmware Security Guidance
	- https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance
	- Meltdown and Spectre Side-Channel Vulnerability Guidance
		- https://www.us-cert.gov/ncas/alerts/TA18-004A
- Hardware Security @ UNC - https://cs.unc.edu/~csturton/HWSecurityatUNC/
	- Security Specification Mining - https://cs.unc.edu/~csturton/HWSecurityatUNC/specification_mining.html
	- Symbolic Execution for Hardware - https://cs.unc.edu/~csturton/HWSecurityatUNC/symbolic_execution.html
- IEEE International Symposium on Hardware Oriented Security and Trust (HOST)
	- http://www.hostsymposium.org/
- IACR Transactions on Cryptographic Hardware and Embedded Systems (TCHES)
	- https://tches.iacr.org/
- International Workshop on Constructive Side-Channel Analysis and Secure Design (COSADE)
	- https://www.cosade.org/
	- https://dblp.org/db/conf/cosade/
	- https://link.springer.com/conference/cosade
- Security Best Practices for Side Channel Resistance
	- https://software.intel.com/security-software-guidance/insights/security-best-practices-side-channel-resistance
- Side and Covert Channels: Attacks and Defenses
	- ISCA 2019 tutorial
	- https://sites.google.com/view/arch-sec/home
- Timing Channels - Trustworthy Systems - Data61
	- https://ts.data61.csiro.au/projects/TS/timeprotection/

## Defense: Branch Predictor

- BRB: Mitigating Branch Predictor Side-Channels
	- High-Performance Computer Architecture (HPCA) 2019
	- Ilias Vougioukas, Andreas Sandberg, Nikos Nikoleris, Stephan Diestelhorst, Bashir Al-Hashimi, Geoff Merrett
	- https://eprints.soton.ac.uk/426627/
	- complementary dataset: https://doi.org/10.5258/soton/d0739

## Defense: Cache

### Defense: Cache: 2021

- Battle for Secure Caches: Attacks and Defenses on Randomized Caches
	- 2021
	- Gururaj Saileshwar
	- https://www.sigarch.org/battle-for-secure-caches-attacks-and-defenses-on-randomized-caches/
- Detecting and Mitigating Cache-Based Side-Channels
	- 2021 PhD Dissertation; Robert Brotzman
	- http://www.cse.psu.edu/~gxt29/papers/RobBrotzman_Dissertation.pdf
- MIRAGE: Mitigating Conflict-Based Cache Attacks with a Practical Fully-Associative Design
	- USENIX Security 2021
	- Gururaj Saileshwar, Moinuddin Qureshi
	- https://arxiv.org/abs/2009.09090
	- https://github.com/gururaj-s/MIRAGE
- SpecSafe: Detecting Cache Side Channels in a Speculative World
	- Object-Oriented Programming, Systems, Languages & Applications (OOPSLA) 2021
	- Robert Brotzman, Danfeng Zhang, Gang Tan, Mahmut Kandemir
	- https://doi.org/10.1145/3485506
- Streamline: A Fast, Flushless Cache Covert-Channel Attack by Enabling Asynchronous Collusion
	- ASPLOS 2021
	- Gururaj Saileshwar, Christopher W. Fletcher, Moinuddin K. Qureshi
	- https://doi.org/10.1145/3445814.3446742
	- http://memlab.ece.gatech.edu/papers/ASPLOS_2021_1.pdf
	- https://github.com/gururaj-s/streamline
	- https://www.youtube.com/watch?v=jp7CDpxwjjQ
- Systematic Analysis of Randomization-based Protected Cache Architectures
	- IEEE Symposium on Security & Privacy (S&P) 2021
	- Antoon Purnal, Lukas Giner, Daniel Gruss, Ingrid Verbauwhede
	- https://www.esat.kuleuven.be/cosic/publications/article-3194.pdf

### Defense: Cache: 2020

- A Benchmark Suite for Evaluating Caches' Vulnerability to Timing Attacks
	- Architectural Support for Programming Languages and Operating Systems (ASPLOS) 2020
	- Shuwen Deng, Wenjie Xiong, Jakub Szefer
	- https://arxiv.org/abs/1911.08619
	- https://www.youtube.com/watch?v=Kq5KJ1NWd-s
	- https://caslab.csl.yale.edu/code/cache-security-benchmarks/
- HybCache: Hybrid Side-Channel-Resilient Caches for Trusted Execution Environments
	- USENIX Security 2020
	- Ghada Dessouky, Tommaso Frassetto, Ahmad-Reza Sadeghi
	- https://arxiv.org/abs/1909.09599
	- https://www.usenix.org/system/files/sec20spring_dessouky_prepub.pdf
- Meet the Sherlock Holmes’ of Side Channel Leakage: A Survey of Cache SCA Detection Techniques
	- IEEE Access (2020)
	- Ayaz Akram, Maria Mushtaq, Muhammad Khurram Bhatti, Vianney Lapotre, Guy Gogniat
	- https://ieeexplore.ieee.org/abstract/document/9035459/
- SmokeBomb: Effective Mitigation Against Cache Side-channel Attacks on the ARM Architecture
	- MobiSys 2020
	- Haehyun Cho, Jinbum Park, Donguk Kim, Ziming Zhao, Yan Shoshitaishvili, Adam Doupeé, Gail-Joon Ahn
	- https://doi.org/10.1145/3386901.3388888
	- https://haehyun.github.io/papers/smokebomb-mobisys20.pdf

### Defense: Cache: 2019

- An Exploration of Effective Fuzzing for Side-channel Cache Leakage
	- Software Testing, Verification and Reliability (STVR) 2019
	- Tiyash Basu, Kartik Aggarwal, Chundong Wang, Sudipta Chattopadhyay
	- https://doi.org/10.1002/stvr.1718
	- https://asset-group.github.io/papers/STVR-cache-side-channel-fuzz.pdf
	- https://github.com/tiyashbasu/Cache_Side_Channel_Tester
- Analysis of Secure Caches Using a Three-Step Model for Timing-Based Attacks
	- Journal of Hardware and Systems Security 3(4) 2019
	- Shuwen Deng, Wenjie Xiong & Jakub Szefer
	- https://eprint.iacr.org/2019/167
- Automated Software Protection for the Masses Against Side-Channel Attacks
	- HiPEAC 2019
	- Nicolas Belleville, Damien Couroussé, Karine Heydemann, Henri-Pierre Charles
	- https://dl.acm.org/citation.cfm?id=3281662
- CaSym: Cache Aware Symbolic Execution for Side Channel Detection and Mitigation
	- Security & Privacy (S&P) 2019
	- Brotzman, R L, Shen Liu, Danfeng Zhang, Gang Tan, Mahmut T. Kandemir
	- http://www.cse.psu.edu/~dbz5017/pub/oakland19.pdf
- Cyclone: Detecting Contention-Based Cache Information Leaks Through Cyclic Interference
	- MICRO-52 2019
	- Austin Harris, Shijia Wei, Prateek Sahu, Pranav Kumar, Todd Austin, Mohit Tiwari
	- https://spark.ece.utexas.edu/
	- http://spark.ece.utexas.edu/pubs/MICRO-19-cyclone.pdf
- Fooling the Sense of Cross-core Last-level Cache Eviction based Attacker by Prefetching Common Sense
	- PACT 2019
	- Biswabandan Panda
	- https://eprint.iacr.org/2019/391
	- https://www.cse.iitk.ac.in/users/biswap/BITP.pdf
- ScatterCache: Thwarting Cache Attacks via Cache Set Randomization
	- USENIX Security 2019
	- Mario Werner, Thomas Unterluggauer, Lukas Giner, Michael Schwarz, Daniel Gruss, Stefan Mangard
	- https://www.usenix.org/conference/usenixsecurity19/presentation/werner
- SecDir: Secure Directories to Defeat Directory Side Channel Attacks
	- International Symposium on Computer Architecture (ISCA) 2019
	- Mengjia Yan, Jen-Yang Wen, Christopher Fletcher, Josep Torrellas
	- http://iacoma.cs.uiuc.edu/work/comanuma.html

### Defense: Cache: 2018

- CacheShield: Protecting Legacy Processes Against Cache Attacks
	- CODASPY 2018
	- Samira Briongos, Gorka Irazoqui, Pedro Malagón, Thomas Eisenbarth
	- https://arxiv.org/abs/1709.01795
	- https://dl.acm.org/citation.cfm?id=3176258.3176320
- CEASER: Mitigating Conflict-Based Cache Attacks via Encrypted-Address and Remapping
	- MICRO 2018
	- Moinuddin K. Qureshi
	- http://memlab.ece.gatech.edu/papers/MICRO_2018_2.pdf
- DAWG: A Defense Against Cache Timing Attacks in Speculative Execution Processors
	- MICRO 2018
	- Vladimir Kiriansky, Ilia A. Lebedev, Saman P. Amarasinghe, Srinivas Devadas, Joel S. Emer
	- https://doi.org/10.1109/MICRO.2018.00083
- On the Incomparability of Cache Algorithms in Terms of Timing Leakage
	- arXiv 2018
	- Pablo Cañones, Boris Köpf, Jan Reineke
	- https://arxiv.org/abs/1807.01240

### Defense: Cache: 2017

- CacheD: Identifying Cache-Based Timing Channels in Production Software
	- USENIX Security 2017
	- Shuai Wang, Pei Wang, Xiao Liu, Danfeng Zhang, Dinghao Wu
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/wang-shuai
- Did we learn from LLC Side Channel Attacks? A Cache Leakage Detection Tool for Crypto Libraries
	- arXiv 2017
	- Gorka Irazoqui, Kai Cong, Xiaofei Guo, Hareesh Khattri, Arun Kanuparthi, Thomas Eisenbarth, Berk Sunar
	- https://arxiv.org/abs/1709.01552
- How secure is your cache against side-channel attacks?
	- MICRO 2017
	- Zecheng He, Ruby B. Lee
	- https://doi.org/10.1145/3123939.3124546
	- http://palms.ee.princeton.edu/system/files/Micro-camera-ready-final.pdf
- Secure Hierarchy-Aware Cache Replacement Policy (SHARP): Defending Against Cache-Based Side Channel Attacks
	- ISCA 2017
	- Mengjia Yan, Bhargava Gopireddy, Thomas Shull, Josep Torrellas
	- https://ieeexplore.ieee.org/abstract/document/8192484
- Strong and Efficient Cache Side-Channel Protection using Hardware Transactional Memory
	- USENIX Security Symposium 2017
	- Daniel Gruss, Julian Lettner, Felix Schuster, Olga Ohrimenko, István Haller, Manuel Costa
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/gruss
	- https://gruss.cc/files/cloak.pdf
	- https://github.com/Microsoft/msr-cloak

### Defense: Cache: 2016

- Automated Detection of Instruction Cache Leaks in Modular Exponentiation Software
	- CARDIS 2016
	- Andreas Zankl, Johann Heyszl, Georg Sigl
	- https://link.springer.com/chapter/10.1007/978-3-319-54669-8_14
	- https://github.com/falsecurity/cache-leak-detector

### Defense: Cache: 2013

- Architecting against Software Cache-Based Side-Channel Attacks
	- IEEE Transactions on Computers 62(7), July 2013
	- Jingfei Kong, O. Aciicmez, J-P Seifert, Huiyang Zhou
	- http://ieeexplore.ieee.org/document/6178238/
- CacheAudit: A Tool for the Static Analysis of Cache Side Channels
	- USENIX Security 2013
	- Goran Doychev, Dominik Feld, Boris Köpf, Laurent Mauborgne, Jan Reineke
	- https://www.usenix.org/conference/usenixsecurity13/technical-sessions/paper/doychev
	- https://github.com/cacheaudit/cacheaudit

### Defense: DRAM

- DAGguise: Mitigating Memory Timing Side Channels
	- ASPLOS 2022
	- Peter W. Deutsch, Yuheng Yang, Thomas Bourgeat, Jules Drean, Joel Emer, Mengjia Yan
	- https://doi.org/10.1145/3503222.3507747
	- https://people.csail.mit.edu/mengjia/data/DAGguise_ASPLOS22.pdf
	- https://people.csail.mit.edu/mengjia/data/DAGguise_presentation.pdf
	- https://github.com/CSAIL-Arch-Sec/DAGguise

## Defense: Floating Point Unit (FPU)

- On the effectiveness of mitigations against floating-point timing channels
	- USENIX Security 2017
	- David Kohlbrenner and Hovav Shacham
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/kohlbrenner
	- https://homes.cs.washington.edu/~dkohlbre/floats/
- Towards Verified, Constant-time Floating Point Operations
	- ACM CCS 2018
	- Marc Andrysco, Andres Nötzli, Fraser Brown, Ranjit Jhala, and Deian Stefan
	- https://dl.acm.org/citation.cfm?id=3243766
	- https://www.youtube.com/watch?v=f2y6yHXoEc0
	- https://ranjitjhala.github.io/static/ctfp-ccs18.pdf

## Defense: Hardware Design & Verification

- A Hardware Design Language for Timing-Sensitive Information-Flow Security
	- ASPLOS 2015
	- Danfeng Zhang, Yao Wang, G. Edward Suh, Andrew C. Myers
	- http://www.cs.cornell.edu/andru/papers/asplos15/
	- Meltdown, Spectre, and why hardware can be correct yet insecure
		- https://andrumyers.wordpress.com/2018/01/17/meltdown-spectre-and-how-hardware-can-be-correct-but-insecure/
- Broad-Based Side-Channel Defenses for Modern Microprocessors
	- 2019 PhD dissertation; Ashay Rane
	- https://www.cs.utexas.edu/users/lin/papers/ashay.pdf
	- https://ashay.rane.info/
- Capability Hardware Enhanced RISC Instructions (CHERI): Notes on the Meltdown and Spectre Attacks
	- http://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-916.pdf
- CheckMate: Automated Exploit Program Generation for Hardware Security Verification
	- International Symposium on Microarchitecture (MICRO) 2018
	- Caroline Trippel, Daniel Lustig, and Margaret Martonosi
	- https://www-cs.stanford.edu/~trippel/pubs/ctrippel_MICRO51.pdf
	- https://github.com/ctrippel/checkmate
- Data Oblivious ISA Extensions for Side Channel-Resistant and High Performance Computing
	- Network and Distributed System Security Symposium (NDSS) 2019
	- Jiyong Yu, Lucas Hsiung, Mohamad El Hajj, Christopher W. Fletcher
	- https://eprint.iacr.org/2018/808
- End-to-End Automated Exploit Generation for Validating the Security of Processor Designs
	- MICRO 2018
	- R. Zhang, C. Deutschbein, P. Huang, C. Sturton
	- https://cs.unc.edu/~csturton/papers/zhang2018MICRO.pdf
	- https://github.com/rzhang2285/Coppelia
- Fast and Efficient Deployment of Security Defenses via Context Sensitive Decoding
	- Government Microcircuit Applications and Critical Technology Conference (GOMACTech) 2019
	- Mohammadkazem Taram, Dean M. Tullsen, Ashish Venkat, Houman Homayoun, Sai Manoj MD,
	- http://www.cs.virginia.edu/venkat/papers/gomactech2019.pdf
- HyperFlow: A Processor Architecture for Nonmalleable, Timing-Safe Information Flow Security
	- ACM CCS 2018
	- Andrew Ferraiuolo, Mark Zhao, Andrew C. Myers, G. Edward Suh
	- https://dl.acm.org/citation.cfm?id=3243743
	- https://www.youtube.com/watch?v=JdIbR_cwjaU
	- http://www.cs.cornell.edu/andru/papers/hyperflow/
- IntroSpectre: A Pre-Silicon Framework for Discovery and Analysis of Transient Execution Vulnerabilities
	- ISCA 2021
	- Moein Ghaniyoun, Kristin Barber, Yinqian Zhang, Radu Teodorescu
	- http://web.cse.ohio-state.edu/~teodorescu.1/resources/introspectre-isca2021.pdf
	- https://moeinghaniyoun.github.io/files/IntroSpectre.pdf
	- https://moeinghaniyoun.github.io/files/IntroSpectre.ppsx
	- https://www.youtube.com/watch?v=cEjbz06RCmk
- IODINE: Verifying Constant-Time Execution of Hardware
	- USENIX Security 2019
	- Klaus von Gleissenthall, Rami Gökhan Kıcı, Deian Stefan, Ranjit Jhala
	- https://www.usenix.org/conference/usenixsecurity19/presentation/von-gleissenthall
	- https://github.com/gokhankici/iodine
- Isolating Speculative Data to Prevent Transient Execution Attacks
	- IEEE Computer Architecture Letters (CAL) 18(2) 2019
	- Kristin Barber, Anys Bacha, Li Zhou, Yinqian Zhang, Radu Teodorescu
	- https://doi.org/10.1109/LCA.2019.2916328
- Jamais Vu: Thwarting Microarchitectural Replay Attacks
	- Architectural Support for Programming Languages and Operating Systems (ASPLOS) 2021
	- Dimitrios Skarlatos, Zirui Zhao, Riccardo Paccagnella, Christopher W. Fletcher, Josep Torrellas
	- https://rp8.web.engr.illinois.edu/papers/jamaisvu-asplos2021.pdf
	- https://github.com/dskarlatos/JamaisVu
- Microarchitectural Timing Channels and their Prevention on an Open-Source 64-bit RISC-V Core
	- Design, Automation and Test in Europe (DATE) 2021
	- Nils Wistoff, Moritz Schneider, Frank K. Gürkaynak, Luca Benini, Gernot Heiser
	- https://trustworthy.systems/publications/csiro_full_text/Wistoff_SGBH_21.pdf
	- https://pulp-platform.org/docs/date2021/DATE21-nwistoff-timing-channels.pdf
	- http://hdl.handle.net/102.100.100/387380
	- L1 D$, L1 I$, TLB, BTB, BHT
- ParTI - Towards Combined Hardware Countermeasures against Side Channel and Fault Injection Attacks
	- CHES 2016, IACR-CRYPTO-2016
	- Tobias Schneider, Amir Moradi, Tim Güneysu
	- https://eprint.iacr.org/2016/648
	- https://www.youtube.com/watch?v=wTJvb6k5yp0
- Prevention of Microarchitectural Covert Channels on an Open-Source 64-bit RISC-V Core
	- 2020 Workshop on Computer Architecture Research with RISC-V (CARRV)
	- Nils Wistoff, Moritz Schneider, Frank K. Gürkaynak, Luca Benini, Gernot Heiser
	- https://arxiv.org/abs/2005.02193
	- https://microkerneldude.wordpress.com/2020/06/09/sel4-is-verified-on-risc-v/
- Principles of Secure Processor Architecture Design
	- 2019 book; Jakub Szefer
	- http://www.morganclaypoolpublishers.com/catalog_Orig/product_info.php?products_id=1315
	- Tutorials: https://caslab.csl.yale.edu/tutorials/
		- HiPEAC 2019 Tutorial: http://caslab.csl.yale.edu/tutorials/hipeac2019/
		- ASPLOS 2019 Tutorial: http://caslab.csl.yale.edu/tutorials/asplos2019/
- Provably Secure Isolation for Interruptible Enclaved Execution on Small Microprocessors
	- IEEE Computer Security Foundations Symposium (CSF) 2020
	- Matteo Busi, Job Noorman, Jo Van Bulck, Letterio Galletta, Pierpaolo Degano, Jan Tobias Mühlberg, Frank Piessens
	- https://arxiv.org/abs/2001.10881
- Securing Processors from Time Side Channels
	- Jose Renau
	- UC Santa Cruz, Tech. Rep., April 2018 - https://users.soe.ucsc.edu/~renau/docs/tleak.pdf
	- The Asilomar Microcomputer Workshop, April 2018 - https://users.soe.ucsc.edu/~renau/docs/amw18.pdf
- Side Channel Analysis Protection and Low Latency in Action - Case Study of PRINCE and Midori
	- IACR-ASIACRYPT-2016
	- Amir Moradi, Tobias Schneider
	- https://www.youtube.com/watch?v=8OyQIh3F4AU
- SMT-COP: Defeating Side-Channel Attacks on Execution Units in SMT Processors
	- Parallel Architectures and Compilation Techniques (PACT) 2019
	- Daniel Townley and Dmitry Ponomarev
	- http://www.cs.binghamton.edu/~dima/pact19.pdf
- SoK: Design Tools for Side-Channel-Aware Implementations
	- ePrint 2021/497
	- Ileana Buhan, Lejla Batina, Yuval Yarom, Patrick Schaumont
	- https://arxiv.org/abs/2104.08593
	- https://eprint.iacr.org/2021/497
- Speculative Execution and Timing Predictability in an Open Source RISC-V Core
	- IEEE Real Time Systems Symposium (RTSS) 2021
	- Alban Gruin, Thomas Carle, Hugues Cassé, Christine Rochange
	- https://ieeexplore.ieee.org/document/9622403
	- https://hal-univ-tlse3.archives-ouvertes.fr/hal-03477573
	- https://www.irit.fr/TRACES/site/minotaur-presentation-at-rtss-2021/
	- MINOTAuR (Mostly IN-Order Timing predictAble pRocessor)
		- a timing predictable open source RISC-V core based on the Ariane core
		- SystemVerilog
		- https://gitlab.irit.fr/minotaur/MINOTAuR
- Using Information Flow to Design an ISA That Controls Timing Channels
	- CSF 2019
	- Drew Zagieboylo, G. Edward Suh, Andrew C. Myers
	- http://www.cs.cornell.edu/andru/papers/hyperisa/

### Defense: Hardware Design & Verification: 2022

- CellIFT: Leveraging Cells for Scalable and Precise Dynamic Information Flow Tracking in RTL
	- USENIX Security 2022
	- Flavien Solt, Ben Gras, Kaveh Razavi
	- https://comsec.ethz.ch/research/microarch/cellift/
	- https://comsec.ethz.ch/wp-content/files/cellift_sec22.pdf
	- https://github.com/comsec-group/cellift-meta

## Defense: Power

- PARAM: A Microprocessor Hardened for Power Side-Channel Attack Resistance
	- IEEE International Symposium on Hardware Oriented Security and Trust (HOST) 2020
	- Muhammad Arsath K F, Vinod Ganesan, Rahul Bodduna, Chester Rebeiro
	- https://arxiv.org/abs/1911.08813

## Defense: SMT

- SecSMT: Securing SMT Processors against Contention-Based Covert Channels
	- USENIX Security Symposium (USENIX Security) 2022
	- Mohammadkazem Taram, Xida Ren, Ashish Venkat, Dean Tullsen
	- https://www.usenix.org/conference/usenixsecurity22/presentation/taram
	- https://mktrm.github.io/files/secsmt_usenix22.pdf
	- https://github.com/mktrm/SecSMT_Artifact

## Defense: Software

- C++ Developer Guidance for Speculative Execution Side Channels
	- https://docs.microsoft.com/en-us/cpp/security/developer-guidance-speculative-execution
- Certified Side Channels
	- USENIX Security Symposium 2020
	- 2019 arXiv
	- Cesar Pereida García, Sohaib ul Hassan, Nicola Tuveri, Iaroslav Gridin, Alejandro Cabrera Aldaya, Billy Bob Brumley
	- https://arxiv.org/abs/1909.01785
- ctgrind
	- https://www.imperialviolet.org/2010/04/01/ctgrind.html
	- https://github.com/agl/ctgrind/
- CTTK (Constant-Time Toolkit)
	- https://github.com/pornin/CTTK
- Cycle-Accurate Timing Channel Analysis of Binary Code
	- 2017 Master's Thesis; Roeland Krak
	- http://essay.utwente.nl/72321/
	- http://essay.utwente.nl/72321/1/Krak_MA_EEMCS.pdf
	- model of instruction execution time for the ARM Cortex-A7
- dudect: dude, is my code constant time?
	- https://github.com/oreparaz/dudect
- KASLR is Dead: Long Live KASLR
	- Engineering Secure Software and Systems (ESSoS) 2017
	- Daniel Gruss, Moritz Lipp, Michael Schwarz, Richard Fellner, Clémentine Maurice, Stefan Mangard
	- https://gruss.cc/files/kaiser.pdf
	- https://github.com/IAIK/KAISER
- MicroWalk: A Framework for Finding Side Channels in Binaries
	- Annual Computer Security Applications Conference (ACSAC) 2018
	- Jan Wichelmann, Ahmad Moghimi, Thomas Eisenbarth, Berk Sunar
	- https://arxiv.org/abs/1808.05575
	- https://github.com/UzL-ITS/Microwalk
- Mitigating Speculative Attacks in Crypto
	- https://github.com/HACS-workshop/spectre-mitigations/blob/master/crypto_guidelines.md
- Mitigating speculative execution side channel hardware vulnerabilities
	- https://blogs.technet.microsoft.com/srd/2018/03/15/mitigating-speculative-execution-side-channel-hardware-vulnerabilities/
- Principled Elimination of Microarchitectural Timing Channels through Operating-System Enforced Time Protection
	- 2019 PhD Thesis; Qian Ge
	- http://ts.data61.csiro.au/publications/papers/Ge:phd.pdf
	- http://handle.unsw.edu.au/1959.4/64228
- Provably Secure Countermeasures against Side-channel Attacks
	- 2015 Dissertation; Praveen Kumar Vadnala
	- https://orbilu.uni.lu/bitstream/10993/21653/2/PraveenVadnala_Thesis.pdf
- Rigorous Analysis of Software Countermeasures against Cache Attacks
	- PLDI 2017; Goran Doychev, Boris Köpf
	- https://www.youtube.com/watch?v=GMyDEnpoyoI
	- https://arxiv.org/abs/1603.02187
	- http://software.imdea.org/~bkoepf/papers/pldi17.pdf
- SafeSide: A project to understand and mitigate software-observable side-channels
	- https://github.com/google/safeside
- SideTrail: Verifying Time-Balancing of Cryptosystems
	- Verified Software: Theories, Tools, and Experiments (VSTTE) 2018
	- Konstantinos Athanasiou, Byron Cook, Michael Emmi, Colm MacCarthaigh, Daniel Schwartz-Narbonne, Serdar Tasiran
	- https://github.com/awslabs/s2n/tree/master/tests/sidetrail
	- http://www0.cs.ucl.ac.uk/staff/b.cook/VSSTE18_sidetrail.pdf
	- https://aws.amazon.com/blogs/security/how-aws-sidetrail-verifies-key-aws-cryptography-code/
- Site Isolation: Process Separation for Web Sites within the Browser
	- USENIX Security Symposium (2019)
	- Charles Reis, Alexander Moshchuk, Nasko Oskov
	- https://ai.google/research/pubs/pub48285
- Time Protection: the Missing OS Abstraction
	- EuroSys 2019
	- Qian Ge, Yuval Yarom, Tom Chothia, Gernot Heiser
	- https://ts.data61.csiro.au/publications/csiroabstracts/Ge_YCH_19.abstract.pml.html
- Towards Practical Tools for Side Channel Aware Software Engineering: "Grey Box" Modelling for Instruction Leakages
	- USENIX Security 2017
	- David McCann, Elisabeth Oswald, Carolyn Whitnall
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/mccann
- Verifying Constant-Time Implementations
	- USENIX Security 2016
	- José Bacelar Almeida, Manuel Barbosa, Gilles Barthe, François Dupressoir, Michael Emmi
	- https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/almeida
- Verifying Constant-Time Implementations by Abstract Interpretation
	- European Symposium on Research in Computer Security 2017
	- Sandrine Blazy, David Pichardie, Alix Trieu
	- https://hal.inria.fr/hal-01588444
	- https://link.springer.com/chapter/10.1007/978-3-319-66402-6_16
- Why Constant-Time Crypto?
	- https://www.bearssl.org/constanttime.html
- You Shall Not Bypass: Employing data dependencies to prevent Bounds Check Bypass
	- arXiv 2018
	- Oleksii Oleksenko, Bohdan Trach, Tobias Reiher, Mark Silberstein, Christof Fetzer
	- https://arxiv.org/abs/1805.08506

### Defense: Software: 2022

- Rosita++: Automatic Higher-Order Leakage Elimination from Cryptographic Code
	- 2021 ACM SIGSAC Conference on Computer and Communications Security (CCS)
	- Madura A. Shelton, Łukasz Chmielewski, Niels Samwel, Markus Wagner, Lejla Batina, Yuval Yarom
	- https://dl.acm.org/doi/10.1145/3460120.3485380
	- https://arxiv.org/abs/2109.11741
	- https://github.com/0xADE1A1DE/Rositaplusplus
	- https://github.com/0xADE1A1DE/tracetools
	- https://eprint.iacr.org/2021/1181

### Defense: Software: Compilation and Programming Languages

- Automatically Eliminating Speculative Leaks from Cryptographic Code with Blade
	- Principles of Programming Languages (POPL) 2021
	- Marco Vassena, Craig Disselkoen, Klaus V. Gleissenthall, Sunjay Cauligi, Rami Gökhan Kici, Ranjit Jhala, Dean Tullsen, Deian Stefan
	- https://arxiv.org/abs/2005.00294
	- https://cseweb.ucsd.edu/~dstefan/pubs/vassena:2021:blade.pdf
	- https://github.com/PLSysSec/blade
- Compiler mitigations for time attacks on modern x86 processors
	- ACM TACO 8(4) (2012)
	- Jeroen V. Cleemput, Bart Coppens, Bjorn De Sutter
	- https://doi.org/10.1145/2086696.2086702
- Compiler Strategies for Mitigating Timing Side Channel Attacks
	- 2015 PhD Dissertation; Jeroen Van Cleemput
	- http://hdl.handle.net/1854/LU-8503231
	- https://biblio.ugent.be/publication/8503231
- Constantine: Automatic Side-Channel Resistance Using Efficient Control and Data Flow Linearization
	- Computer and Communications Security (CCS) 2021
	- Pietro Borrello, Daniele Cono D'Elia, Leonardo Querzoni, Cristiano Giuffrida
	- https://arxiv.org/abs/2104.10749
	- https://download.vusec.net/papers/constantine_ccs21.pdf
	- Constantine: a compiler-based system to automatically harden programs against microarchitectural side channels
		- https://github.com/pietroborrello/constantine
- FaCT: A Flexible, Constant-Time Programming Language
	- SecDev 2017
	- Sunjay Cauligi, Gary Soeller, Fraser Brown, Brian Johannesmeyer, Yunlu Huang, Ranjit Jhala, Deian Stefan
	- https://cseweb.ucsd.edu/~dstefan/pubs/cauligi:2017:fact.pdf
	- https://github.com/PLSysSec/FaCT
- Mitigating Data Leakage by Protecting Memory-resident Sensitive Data
	- Annual Computer Security Applications Conference (ACSAC) 2019
	- Tapti Palit, Fabian Monrose, Michalis Polychronakis
	- https://doi.org/10.1145/3359789.3359815
	- https://www3.cs.stonybrook.edu/~mikepo/papers/dataencr.acsac19.pdf
- P0928: Mitigating Spectre v1 Attacks in C++
	- 2020; Devin Jeanpierre, Geoffrey Romer, Chandler Carruth
	- http://wg21.link/P0928
- Provably secure compilation of side-channel countermeasures
	- Cryptology ePrint Archive: Report 2017/1233
	- Gilles Barthe, Benjamin Grégoire, Vincent Laporte
	- https://eprint.iacr.org/2017/1233
	- https://sites.google.com/view/ctpreservation
- Secure Automatic Bounds Checking: Prevention Is Simpler Than Cure
	- CGO 2020
	- Ejebagom John Ojogbo, Mithuna Thottethodi, T. N. Vijaykumar
	- https://doi.org/10.1145/3368826.3377921
- Specfuscator: Evaluating Branch Removal as a Spectre Mitigation
	- Financial Cryptography and Data Security 2021
	- Martin Schwarzl, Claudio Alberto Canella, Daniel Gruss, Michael Schwarz
	- https://martinschwarzl.at/media/files/specfuscator.pdf
- Speculative Load Hardening (a Spectre variant #1 mitigation)
	- 2018; Chandler Carruth
	- https://llvm.org/docs/SpeculativeLoadHardening.html
	- https://lists.llvm.org/pipermail/llvm-dev/2018-March/122085.html
	- https://docs.google.com/document/d/1wwcfv3UV9ZnZVcGiGuoITT_61e_Ko3TmoCS3uXLcJR0/edit
- Swivel: Hardening WebAssembly against Spectre
	- USENIX Security Symposium 2021
	- Shravan Narayan, Craig Disselkoen, Daniel Moghimi, Sunjay Cauligi, Evan Johnson, Zhao Gang, Anjo Vahldiek-Oberwagner, Ravi Sahita, Hovav Shacham, Dean Tullsen, Deian Stefan
	- https://arxiv.org/abs/2102.12730
	- https://www.usenix.org/conference/usenixsecurity21/presentation/narayan

#### Defense: Software: Compilation and Programming Languages: 2023

- Spectre Declassified: Reading from the Right Place at the Wrong Time
	- IEEE Symposium on Security and Privacy (S&P) 2023
	- Basavesh Ammanaghatta Shivakumar, Jack Barnes, Gilles Barthe, Sunjay Cauligi, Chitchanok Chuengsatiansup, Daniel Genkin, Sioli O’Connell, Peter Schwabe, Rui Qi Sim, Yuval Yarom
	- https://doi.ieeecomputersociety.org/10.1109/SP46215.2023.00011
	- https://eprint.iacr.org/2022/426

#### Defense: Software: Compilation and Programming Languages: 2022

- Breaking and Fixing Speculative Load Hardening
	- IACR ePrint 2022/715
	- Zhiyuan Zhang, Gilles Barthe, Chitchanok Chuengsatiansup, Peter Schwabe, Yuval Yarom
	- https://eprint.iacr.org/2022/715
- Layered Binary Templating: Efficient Detection of Compiler- and Linker-introduced Leakage
	- 2022
	- Martin Schwarzl, Erik Kraft, Daniel Gruss
	- https://arxiv.org/abs/2208.02093
- SynthCT: Towards Portable Constant-Time Code
	- Network and Distributed Systems Security (NDSS) Symposium 2022
	- Sushant Dinesh, Grant Garrett-Grossman, Christopher W. Fletcher
	- https://www.ndss-symposium.org/ndss-paper/auto-draft-223/
	- https://github.com/FPSG-UIUC/synthCT
- Systematic Analysis of Programming Languages and Their Execution Environments for Spectre Attacks
	- Iternational Conference on Information Systems Security and Privacy (ICISSP) 2022
	- Amir Naseredini, Stefan Gast, Martin Schwarzl, Pedro Miguel Sousa Bernardo, Amel Smajic, Claudio Canella, Martin Berger, Daniel Gruss
	- https://arxiv.org/abs/2111.12528
	- https://www.cc0x1f.net/publications/spectre_pl_slides.pdf
	- UCL Information Security Research Seminar; February 3, 2022
		- https://www.youtube.com/watch?v=9VnwaRH9b2s

## Defense: Speculation

- Pitchfork: Detecting Spectre vulnerabilities using symbolic execution
	- https://github.com/cdisselkoen/pitchfork

### Defense: Speculation: 2022

- Kasper: Scanning for Generalized Transient Execution Gadgets in the Linux Kernel
	- NDSS 2022
	- Brian Johannesmeyer, Jakob Koschel, Kaveh Razavi, Herbert Bos, Cristiano Giuffrida
	- https://www.ndss-symposium.org/ndss-paper/auto-draft-247/
	- https://github.com/vusec/kasper
	- https://www.vusec.net/projects/kasper/
- Performance Evolution of Mitigating Transient Execution Attacks
	- EuroSys 2022
	- Jonathan Behrens, Adam Belay, M. Frans Kaashoek
	- https://doi.org/10.1145/3492321.3519559
- Understanding and Improving the Performance of Mitigating Transient Execution Attacks
	- 2022 PhD Dissertation; Jonathan Behrens
	- https://pdos.csail.mit.edu/papers/behrensj-phd-thesis.pdf

### Defense: Speculation: 2021

- BasicBlocker: ISA Redesign to Make Spectre-Immune CPUs Faster
	- RAID 2021
	- Jan Philipp Thoma, Jakob Feldtkeller, Markus Krausz, Tim Güneysu, Daniel J. Bernstein
	- https://arxiv.org/abs/2007.15919
	- https://cr.yp.to/papers/basicblocker-20210504.pdf
- DOLMA: Securing Speculation with the Principle of Transient Non-Observability
	- USENIX Security 2021
	- Kevin Loughlin, Ian Neal, Jiacheng Ma, Elisa Tsai, Ofir Weisse, Satish Narayanasamy, Baris Kasikci
	- https://www.kevinloughlin.org/dolma.pdf
	- https://github.com/efeslab/dolma
- Dynamic Process Isolation
	- 2021
	- Martin Schwarzl, Pietro Borrello, Andreas Kogler, Kenton Varda, Thomas Schuster, Daniel Gruss, Michael Schwarz
	- https://arxiv.org/abs/2110.04751
	- Dynamic Process Isolation: Research by Cloudflare and TU Graz
		- https://blog.cloudflare.com/spectre-research-with-tu-graz/
- Hardware-Software Contracts for Secure Speculation
	- IEEE Symposium on Security and Privacy (IEEE S&P) 2021
	- Marco Guarnieri, Boris Köpf, Jan Reineke, Pepe Vila
	- https://arxiv.org/abs/2006.03841
- High-Assurance Cryptography in the Spectre Era
	- IEEE Symposium on Security and Privacy (IEEE S&P) 2021
	- Gilles Barthe, Sunjay Cauligi, Benjamin Gregoire, Adrien Koutsos, Kevin Liao, Tiago Oliveira, Swarn Priya, Tamara Rezk, Peter Schwabe
	- https://eprint.iacr.org/2020/1104
- Hunting the Haunter — Efficient Relational Symbolic Execution for Spectre with Haunted RelSE
	- NDSS 2021
	- Lesly-Ann Daniel, Sébastien Bardin, Tamara Rezk
	- https://www.ndss-symposium.org/ndss-paper/hunting-the-haunter-efficient-relational-symbolic-execution-for-spectre-with-haunted-relse/
- SoK: Practical Foundations for Spectre Defenses
	- 2021
	- IEEE S&P 2022
	- Sunjay Cauligi, Craig Disselkoen, Daniel Moghimi, Gilles Barthe, Deian Stefan
	- https://arxiv.org/abs/2105.05801

### Defense: Speculation: 2020

- ConTExT: A Generic Approach for Mitigating Spectre
	- Network and Distributed Systems Security (NDSS) Symposium 2020
	- Michael Schwarz, Moritz Lipp, Claudio Canella, Robert Schilling, Florian Kargl, Daniel Gruss
	- https://misc0110.net/files/context.pdf
- Evolution of Defenses against Transient-Execution Attacks
	- GLSVLSI 2020
	- Claudio Canella, Sai Manoj Pudukotai Dinakarrao, Daniel Gruss, Khaled N. Khasawneh
	- https://gruss.cc/files/transient-defenses.pdf
- Hardware-Software Contracts for Secure Speculation
	- IEEE Symposium on Security and Privacy (IEEE S&P) 2021
	- Marco Guarnieri, Boris Köpf, Jan Reineke, Pepe Vila
	- https://arxiv.org/abs/2006.03841
- KLEESpectre: Detecting Information Leakage through Speculative Cache Attacks via Symbolic Execution
	- ACM Transactions on Software Engineering and Methodology (TOSEM) 2020
	- Guanhua Wang, Sudipta Chattopadhyay, Arnab Kumar Biswas, Tulika Mitra, Abhik Roychoudhury
	- https://arxiv.org/abs/1909.00647
	- https://github.com/winter2020/kleespectre
- MuonTrap: Preventing Cross-Domain Spectre-Like Attacks by Capturing Speculative State
	- ISCA 2020
	- Sam Ainsworth, Timothy M. Jones
	- https://arxiv.org/abs/1911.08384
- Securing the Memory Hierarchy from Speculative Side-Channel Attacks
	- 2020 Licentiate Dissertation; Christos Sakalis
	- http://www.it.uu.se/research/publications/lic/2020-003/
	- http://www.diva-portal.org/smash/get/diva2:1389898/FULLTEXT01.pdf

### Defense: Speculation: 2019

- A Formal Approach to Secure Speculation
	- 2019 IEEE 32nd Computer Security Foundations Symposium (CSF)
	- Kevin Cheang, Cameron Rasmussen, Sanjit Seshia, Pramod Subramanyan
	- https://ieeexplore.ieee.org/abstract/document/8823732
	- https://eprint.iacr.org/2019/310/20190320:103921
- Abstract Interpretation under Speculative Execution
	- Programming Language Design and Implementation (PLDI) 2019
	- Meng Wu & Chao Wang
	- https://doi.org/10.1145/3314221.3314647
	- https://pldi19.sigplan.org/event/pldi-2019-papers-abstract-interpretation-under-speculative-execution
	- https://bitbucket.org/mengwu/timingsyn
- Beyond Spectre: Confronting New Technical and Policy Challenges: Proceedings of a Workshop
	- National Academies of Sciences, Engineering, and Medicine (2019)
	- https://doi.org/10.17226/25418
	- https://www.nap.edu/catalog/25418/beyond-spectre-confronting-new-technical-and-policy-challenges-proceedings-of
- CleanupSpec: An Undo Approach to Safe Speculation
	- MICRO-52 2019
	- Gururaj Saileshwar, Moinuddin K. Qureshi
	- http://memlab.ece.gatech.edu/papers/MICRO_2019_3.pdf
- Conditional Speculation: An Effective Approach to Safeguard Out-of-Order Execution Against Spectre Attacks
	- High-Performance Computer Architecture (HPCA) 2019
	- Peinan Li, Lutan Zhao, Rui Hou; Lixin Zhang; Dan Meng
- Context-Sensitive Fencing: Securing Speculative Execution via Microcode Customization
	- Architectural Support for Programming Languages and Operating Systems (ASPLOS) 2019
	- Mohammadkazem Taram, Ashish Venkat, Dean Tullsen
	- http://www.cs.virginia.edu/~av6ds/papers/asplos2019.pdf
- MI6: Secure Enclaves in a Speculative Out-of-Order Processor
	- MICRO-52 2019
	- Thomas Bourgeat, Ilia Lebedev, Andrew Wright, Sizhuo Zhang, Arvind, Srinivas Devadas
	- https://dl.acm.org/citation.cfm?id=3358310
- NDA: Preventing Speculative Execution Attacks at Their Source
	- MICRO 2019
	- Ofir Weisse, Ian Neal, Kevin Loughlin, Thomas Wenisch, Baris Kasikci
	- http://www.ofirweisse.com/MICRO2019_NDA.pdf
- oo7: Low-overhead Defense against Spectre Attacks via Program Analysis
	- 2019 IEEE Transactions on Software Engineering (TSE)
	- Guanhua Wang, Sudipta Chattopadhyay, Ivan Gotovchits, Tulika Mitra, Abhik Roychoudhury
	- https://arxiv.org/abs/1807.05843
	- https://asset-group.github.io/papers/oo7.pdf
	- A binary analysis framework to defend against potential vulnerability to Spectre attacks
		- https://github.com/winter2020/oo7
- SafeSpec: Banishing the Spectre of a Meltdown with Leakage-Free Speculation
	- Design Automation Conference (DAC) 2019
	- Khaled N. Khasawneh, Esmaeil Mohammadian Koruyeh, Chengyu Song, Dmitry Evtyushkin, Dmitry Ponomarev, Nael Abu-Ghazaleh
	- http://www.cs.binghamton.edu/~dima/dac2019.pdf
- SPECCFI: Mitigating Spectre Attacks using CFI Informed Speculation
	- arXiv 2019; IEEE S&P 2020
	- Esmaeil Mohammadian Koruyeh, Shirin Haji Amin Shirazi, Khaled N. Khasawneh, Chengyu Song, Nael Abu-Ghazaleh
	- https://arxiv.org/abs/1906.01345
- SpecFuzz: Bringing Spectre-type vulnerabilities to the surface
	- arXiv 2019; USENIX Security 2020
	- Oleksii Oleksenko, Bohdan Trach, Mark Silberstein, Christof Fetzer
	- https://arxiv.org/abs/1905.10311
	- SpecFuzz: A tool to enable fuzzing for Spectre vulnerabilities
		- https://github.com/OleksiiOleksenko/SpecFuzz
	- FOSDEM 2020
		- https://fosdem.org/2020/schedule/event/security_specfuzz_bringing_spectre_type_vulnerabilities_to_the_surface/
- SpecShield: Shielding Speculative Data from Microarchitectural Covert Channels
	- Parallel Architectures and Compilation Techniques (PACT) 2019
	- K. Barber, A. Bacha, L. Zhou, Y. Zhang, R. Teodorescu
	- https://anysbacha.github.io/publications/barber_pact19.pdf
	- https://anysbacha.github.io/publications/barber_pact19_slides.pdf
	- http://web.cse.ohio-state.edu/~teodorescu.1/resources/papers/specshield_pact2019.pdf
- Spectre is here to stay: An analysis of side-channels and speculative execution
	- arXiv 2019
	- Ross Mcilroy, Jaroslav Sevcik, Tobias Tebbi, Ben L. Titzer, Toon Verwaest
	- https://arxiv.org/abs/1902.05178
- SpectreGuard: An Efficient Data-centric Defense Mechanism against Spectre Attacks
	- Design Automation Conference (DAC) 2019
	- Jacob Fustos, Farzad Farshchi, Heechul Yun
	- http://www.ittc.ku.edu/~heechul/papers/spectreguard-dac2019-camera.pdf
- Speculative Taint Tracking (STT): A Comprehensive Protection for Speculatively Accessed Data
	- International Symposium on Microarchitecture (MICRO) 2019
	- Jiyong Yu, Mengjia Yan, Artem Khyzha, Adam Morrison, Josep Torrellas, Christopher Fletcher
	- https://www.cs.tau.ac.il/~mad/publications/micro2019-stt.pdf
	- http://iacoma.cs.uiuc.edu/iacoma-papers/micro19_2.pdf
	- http://iacoma.cs.uiuc.edu/iacoma-papers/PRES/present_micro19_2.pdf
	- https://keystone-enclave.org/open-source-enclaves-workshop/slides/OSEW19_ChristopherFletcher_UIUC.pdf

### Defense: Speculation: 2018

- An Inside Story of Mitigating Speculative Execution Side Channel Vulnerabilities
	- Black Hat 2018; Anders Fogh, Christopher Ertl
	- https://www.youtube.com/watch?v=_J9MpK4MQWk
- InvisiSpec: Making Speculative Execution Invisible in the Cache Hierarchy
	- International Symposium on Microarchitecture (MICRO) 2018
	- Mengjia Yan, Jiho Choi, Dimitrios Skarlatos, Adam Morrison, Christopher W. Fletcher, Josep Torrellas
	- http://iacoma.cs.uiuc.edu/iacoma-papers/PRES/present_micro18.pdf
	- Paper: http://iacoma.cs.uiuc.edu/iacoma-papers/micro18.pdf
	- Poster: https://people.csail.mit.edu/mengjia/data/InvisiSpec_Poster.pdf
	- Lightning talk: https://www.youtube.com/watch?v=mAO5iejYUec
	- https://github.com/mjyan0720/InvisiSpec-1.0
- Spectector: Principled Detection of Speculative Information Flows
	- IEEE Symposium on Security & Privacy 2020
	- arXiv 2018
	- Marco Guarnieri, Boris Köpf, José F. Morales, Jan Reineke, Andrés Sánchez
	- https://spectector.github.io/
	- https://github.com/spectector/spectector
- Spectre: Secrets, Side-Channels, Sandboxes, and Security
	- CppCon 2018; Chandler Carruth
	- https://www.youtube.com/watch?v=_f7O3IfIR2k
- Spectres, Virtual Ghosts, and Hardware Support
	- Hardware and Architectural Support for Security and Privacy (HASP) 2018
	- Xiaowan Dong, Zhuojia Shen, John Criswell, Alan Cox, Sandhya Dwarkadas
	- https://dl.acm.org/citation.cfm?id=3214297
- Spectrum: Classifying, Replicating and Mitigating Spectre Attacks on a Speculating RISC-V Microarchitecture
	- 2018 Technical Report
	- Abraham Gonzalez, Ben Korpan, Ed Younis, Jerry Zhao
	- https://people.eecs.berkeley.edu/~kubitron/courses/cs262a-F18/projects/reports/project4_report.pdf

## Defense: TLB

- TLB-pilot: Mitigating TLB Contention Attack on GPUs with Microarchitecture-Aware Scheduling
	- ACM Transactions on Architecture and Code Optimization (TACO) 19(1) 2021
	- Bang Di, Daokun Hu, Zhen Xie, Jianhua Sun, Hao Chen, Jinkui Ren, Dong Li
	- https://dl.acm.org/doi/full/10.1145/3491218
	- https://github.com/qzpm7193/TLB_pilot

---

# Arithmetic Logic Unit (ALU)

- Constant-Time Multiplication - https://www.bearssl.org/ctmul.html
- Share-slicing: Friend or Foe?
	- CHES 2020
	- Si Gao, Ben Marshall, Dan Page, Elisabeth Oswald
	- https://tches.iacr.org/index.php/TCHES/article/view/8396
- When Constant-Time Source Yields Variable-Time Binary: Exploiting Curve25519-donna Built with MSVC 2015
	- Cryptology and Network Security (CANS) 2016
	- Thierry Kaufmann, Hervé Pelletier, Serge Vaudenay, Karine Villegas
	- https://infoscience.epfl.ch/record/223794/files/32_1.pdf
	- https://research.kudelskisecurity.com/2017/01/16/when-constant-time-source-may-not-save-you/
	- https://www.semanticscholar.org/paper/When-Constant-Time-Source-Yields-Variable-Time-Bin-Kaufmann-Pelletier/4207ebe6f2656c1a40149ec446ca99885ce5b2ad

---

# Branch Predictor

- Branch Prediction Attack on Blinded Scalar Multiplication
	- IEEE Transactions on Computers 69(5) 2020
	- Sarani Bhattacharya, Clémentine Maurice, Shivam Bhasin, Debdeep Mukhopadhyay
	- https://hal.inria.fr/hal-02866753
	- https://dx.doi.org/10.1109/TC.2019.2958611
- BranchScope: A New Side-Channel Attack on Directional Branch Predictor
	- ASPLOS 2018
	- Dmitry Evtyushkin, Ryan Riley, Nael Abu-Ghazaleh, Dmitry Ponomarev
	- http://www.cs.ucr.edu/~nael/pubs/asplos18.pdf
- BranchSpec: Information Leakage Attacks Exploiting Speculative Branch Instruction Executions
	- IEEE International Conference on Computer Design (ICCD) 2020
	- Md Hafizul Islam Chowdhuryy, Hang Liu, Fan Yao
	- http://fan-yao.com/paper/2020_ICCD_branchspec.pdf
	- https://github.com/fanyao/branchspec
	- https://www.youtube.com/watch?v=Yo9B_azoMBw
	- TR: Leakage of Sensitive Information through Speculative Branch Executions
		- 2021
		- Md Hafizul Islam Chowdhuryy, Fan Yao
		- http://fan-yao.com/paper/TR_branchspec.pdf
	- Leaking Secrets through Modern Branch Predictor in the Speculative World
		- 2021
		- Md Hafizul Islam Chowdhuryy, Fan Yao
		- https://arxiv.org/abs/2107.09833
- Covert Channels Through Branch Predictors: A Feasibility Study
	- Hardware and Architectural Support for Security and Privacy (HASP) 2015
	- Dmitry Evtyushkin, Dmitry Ponomarev, Nael Abu-Ghazaleh
	- http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.702.6038&rep=rep1&type=pdf
	- http://caslab.csl.yale.edu/workshops/hasp2015/slides_05_evtyushkin.pdf
- Exploiting branch target prediction
	- INFILTRATE 2018; Jann Horn
	- https://vimeo.com/270442911
- Exploring Branch Predictors for Constructing Transient Execution Trojans
	- Architectural Support for Programming Languages and Operating Systems (ASPLOS) 2020
	- Tao Zhang, Kenneth Koltermann, Dmitry Evtyushkin
	- http://www.cs.wm.edu/~dmitry/assets/files/zhang2020exploring.pdf
	- https://www.youtube.com/watch?v=OLQshI-1KBc
- Jump Over ASLR: Attacking Branch Predictors to Bypass ASLR
	- MICRO 2016
	- Dmitry Evtyushkin, Dmitry Ponomarev, Nael Abu-Ghazaleh
	- http://www.cs.binghamton.edu/~dima/micro16.pdf
	- PoC for breaking hypervisor ASLR using branch target buffer collisions
		- https://github.com/felixwilhelm/mario_baslr/
- On the Power of Simple Branch Prediction Analysis
	- ASIACCS 2007
	- Onur Aciiçmez, Çetin Kaya Koç, Jean-Pierre Seifert
	- https://eprint.iacr.org/2006/351.pdf
	- https://cetinkayakoc.net/docs/c40.pdf
- Predicting Secret Keys via Branch Prediction
	- CT-RSA 2007
	- Onur Acıiçmez, Çetin Kaya Koç, Jean-Pierre Seifert
	- https://eprint.iacr.org/2006/288.pdf
	- https://cetinkayakoc.net/docs/c39.pdf
	- MSR talk: https://www.youtube.com/watch?v=rWFj4N6MaQw
- Understanding and Mitigating Covert Channels Through Branch Predictors
	- ACM TACO 13(1): 10 (2016)
	- Dmitry Evtyushkin, Dmitry Ponomarev, Nael B. Abu-Ghazaleh
	- http://www.cs.ucr.edu/~nael/pubs/taco16_branches.pdf
	- https://dl.acm.org/citation.cfm?id=2870636
	- http://www.cs.wm.edu/~dmitry/assets/files/taco-a10-evtyushkin.pdf

## Branch Predictor: 2022

- Branch History Injection: On the Effectiveness of Hardware Mitigations Against Cross-Privilege Spectre-v2 Attacks
	- USENIX Security 2022
	- Enrico Barberis, Pietro Frigo, Marius Muench, Herbert Bos, Cristiano Giuffrida
	- https://www.vusec.net/projects/bhi-spectre-bhb/
	- https://www.intel.com/content/www/us/en/developer/articles/technical/software-security-guidance/technical-documentation/branch-history-injection.html
	- https://developer.arm.com/support/arm-security-updates/speculative-processor-vulnerability/spectre-bhb
	- Today's Spectre variant: branch history injection
		- https://lwn.net/Articles/887326
- RETBLEED: Arbitrary Speculative Code Execution with Return Instructions
	- USENIX Security 2022
	- Johannes Wikner, Kaveh Razavi
	- https://github.com/comsec-group/retbleed
	- https://comsec.ethz.ch/wp-content/files/retbleed_sec22.pdf
	- https://comsec.ethz.ch/research/microarch/retbleed/
	- The "Retbleed" speculative execution vulnerabilities
		- https://lwn.net/Articles/900917/
- The AMD Branch (Mis)predictor
	- 2022; Pawel Wieczorkiewicz
	- Part 1: Just Set it and Forget it!
		- https://grsecurity.net/amd_branch_mispredictor_just_set_it_and_forget_it
	- Part 2: Where No CPU has Gone Before (CVE-2021-26341)
		- https://grsecurity.net/amd_branch_mispredictor_part_2_where_no_cpu_has_gone_before
	- CVE-2021-26341: AMD CPUs May Transiently Execute Beyond Unconditional Direct Branch
		- https://www.amd.com/en/corporate/product-security/bulletin/amd-sb-1026
- You Cannot Always Win the Race: Analyzing the LFENCE/JMP Mitigation for Branch Target Injection
	- 2022
	- Alyssa Milburn, Ke Sun, Henrique Kawakami
	- https://arxiv.org/abs/2203.04277

---

# Cache

## Cache: 2022

- AutoCAT: Reinforcement Learning for Automated Exploration of Cache Timing-Channel Attacks
	- IEEE International Symposium on High-Performance Computer Architecture (HPCA) 2023
	- Mulong Luo, Wenjie Xiong, Geunbae Lee, Yueying Li, Xiaomeng Yang, Amy Zhang, Yuandong Tian, Hsien Hsin S. Lee, G. Edward Suh
	- https://arxiv.org/abs/2208.08025
- ÆPIC Leak: Architecturally Leaking Uninitialized Data from the Microarchitecture
	- USENIX Security 2022
	- Pietro Borrello, Andreas Kogler, Martin Schwarzl, Moritz Lipp, Daniel Gruss, Michael Schwarz
	- https://aepicleak.com
	- https://aepicleak.com/aepicleak.pdf
	- https://github.com/IAIK/AEPIC
	- leakage source: the superqueue between L2 and L3
- Targeted Deanonymization via the Cache Side Channel: Attacks and Defenses
	- USENIX Security 2022
	- Mojtaba Zaheri, Yossi Oren, Reza Curtmola
	- https://www.usenix.org/conference/usenixsecurity22/presentation/zaheri

## Cache: 2021

- iTimed: Cache Attacks on the Apple A10 Fusion SoC
	- IEEE International Symposium on Hardware Oriented Security and Trust (HOST) 2021
	- Gregor Haas, Seetal Potluri, Aydin Aysu
	- https://eprint.iacr.org/2021/464
- Prime+Probe 1, JavaScript 0: Overcoming Browser-based Side-Channel Defenses
	- USENIX Security Symposium 2021
	- Anatoly Shusterman, Ayush Agarwal, Sioli O’Connell, Daniel Genkin, Yossi Oren, Yuval Yarom
	- https://orenlab.sise.bgu.ac.il/p/PP0
	- https://github.com/Yossioren/pp0

## Cache: 2020

- Analysis and Detection of Cache-Based Exploits
	- 2020 Ph.D. Dissertation; Tsvetoslava Vateva-Gurova
	- https://doi.org/10.25534/tuprints-00009770
- CacheOut: Leaking Data on Intel CPUs via Cache Evictions
	- 2020
	- Stephan van Schaik, Marina Minkin, Andrew Kwong, Daniel Genkin, Yuval Yarom
	- https://cacheoutattack.com/
	- https://arxiv.org/abs/2006.13353
	- L1D Eviction Sampling / CVE-2020-0549 / INTEL-SA-00329
	- https://software.intel.com/security-software-guidance/software-guidance/l1d-eviction-sampling
- DABANGG: Time for Fearless Flush based Cache Attacks
	- 2020
	- Anish Saxena, Biswabndan Panda
	- https://eprint.iacr.org/2020/637
	- https://www.cse.iitk.ac.in/users/biswap/DABANGG.pdf
	- https://car3s.github.io/dabangg/
- Flushgeist: Cache Leaks from Beyond the Flush
	- 2020
	- Pepe Vila, Andreas Abel, Marco Guarnieri, Boris Köpf, Jan Reineke
	- https://arxiv.org/abs/2005.13853
- Leaking Information Through Cache LRU States
	- High-Performance Computer Architecture (HPCA) 2020
	- Wenjie Xiong, Jakub Szefer
	- https://arxiv.org/abs/1905.08348
- Pseudorandom Black Swans: Cache Attacks on CTR_DRBG
	- IEEE Symposium on Security & Privacy 2020
	- Shaanan Cohney, Andrew Kwong, Shachar Paz, Daniel Genkin, Nadia Heninger, Eyal Ronen, Yuval Yarom
	- https://eprint.iacr.org/2019/996
	- Research Post: Cache Attacks on CTR_DRBG
	- https://security.cohney.info/blackswans/
- Safecracker: Leaking Secrets through Compressed Caches
	- ASPLOS 2020
	- Po-An Tsai, Andres Sanchez, Christopher W. Fletcher, Daniel Sanchez
	- http://people.csail.mit.edu/poantsai/papers/2020.safecracker.asplos.pdf
	- https://www.youtube.com/watch?v=auKcSndPjuw
- Stealthy Tracking of Autonomous Vehicles with Cache Side Channels
	- USENIX Security 2020
	- Mulong Luo, Andrew C. Myers, G. Edward Suh
	- http://www.cs.cornell.edu/andru/papers/stealthy-tracking/
- Take A Way: Exploring the Security Implications of AMD’s Cache Way Predictors
	- ACM Asia Conference on Computer and Communications Security (ASIA CCS) 2020
	- Moritz Lipp, Vedad Hadžić, Michael Schwarz, Arthur Perais, Clémentine Maurice, Daniel Gruss
	- https://mlq.me/download/takeaway.pdf
	- https://doi.org/10.1145/3320269.3384746
- Website Fingerprinting Through the Cache Occupancy Channel and its Real World Practicality
	- IEEE Transactions on Dependable and Secure Computing (TDSC) 2020
	- Anatoly Shusterman, Zohar Avraham, Eliezer Croitoru, Yarden Haskal, Lachlan Kang, Dvir Levi, Yosef Meltser, Prateek Mittal, Yossi Oren, Yuval Yarom
	- https://orenlab.sise.bgu.ac.il/p/RobustFingerprinting-TDSC

## Cache: 2019

- Attack Directories, Not Caches: Side Channel Attacks in a Non-Inclusive World
	- IEEE Symposium on Security and Privacy (SP) 2019
	- Mengjia Yan, Read Sprabery, Bhargava Gopireddy, Christopher Fletcher, Roy Campbell, Josep Torrellas
	- http://iacoma.cs.uiuc.edu/iacoma-papers/ssp19.pdf
	- http://iacoma.cs.uiuc.edu/iacoma-papers/PRES/present_ssp19.pdf
	- http://iacoma.cs.uiuc.edu/iacoma-papers/PRES/present_HASP18.pptx
		- "We design the first cross-core Prime+Probe attack on non-inclusive caches."
		- "Using our Eviction Sets, we reverse engineer the directory structure in Skylake-X, and identify vulnerabilities in directory design that can be leveraged by cache-based side channel attacks."
		- "Based on our EV construction results, we are able to reverse engineer part of the slice hash function in the Intel Skylake-X processor. Our goal here is to show that the slice hash function is not a simple XOR operation of selected physical address bits. This design is significantly different from the one in previous Intel processors such as SandyBridge and IvyBridge. Considering that all of the previous works on reverse-engineering slice hash functions, rely on the use of a simple XOR hash function, our results identify the need for more advanced reverse-engineering approaches."
- Cache-based Side Channels: Modern Attacks and Defenses
	- 2019 Ph.D. dissertation; Mengjia Yan
	- http://iacoma.cs.uiuc.edu/iacoma-papers/mengjia_yan_thesis.pdf
- The 9 Lives of Bleichenbacher's CAT: New Cache ATtacks on TLS Implementations
	- IEEE Symposium on Security & Privacy 2019
	- Eyal Ronen, Robert Gillham, Daniel Genkin, Adi Shamir, David Wong, Yuval Yarom
	- vhttps://eprint.iacr.org/2018/1173
	- https://eyalro.net/project/cat.html
- Unveiling your keystrokes: A Cache-based Side-channel Attack on Graphics Libraries
	- NDSS 2019
	- Daimeng Wang, Ajaya Neupane, Zhiyun Qian, Nael Abu-Ghazaleh, Srikanth V. Krishnamurthy, Edward J. M. Colbert, Paul Yu
	- http://www.cs.ucr.edu/~zhiyunq/pub/ndss19_cache_keystrokes.pdf

## Cache: 2018

- Are Coherence Protocol States vulnerable to Information Leakage?
	- HPCA 2018
	- Fan Yao, Milos Doroslovacki, Guru Venkataramani
	- https://www2.seas.gwu.edu/~guruv/hpca2018.pdf
	- https://www.youtube.com/watch?v=NQQ0zC1G7p0
- MeltdownPrime and SpectrePrime: Automatically-Synthesized Attacks Exploiting Invalidation-Based Coherence Protocols
	- 2018 arXiv preprint
	- Caroline Trippel, Daniel Lustig, Margaret Martonosi
	- https://arxiv.org/abs/1802.03802
- MemJam: A False Dependency Attack against Constant-Time Crypto Implementations
	- RSA Conference 2018
	- Ahmad Moghimi, Thomas Eisenbarth, Berk Sunar
	- https://arxiv.org/abs/1711.08002
- Robust Website Fingerprinting Through the Cache Occupancy Channel
	- USENIX Security Symposium 2019; 2018 arXiv
	- Anatoly Shusterman, Lachlan Kang, Yarden Haskal, Yosef Meltser, Prateek Mittal, Yossi Oren, Yuval Yarom
	- https://arxiv.org/abs/1811.07153

## Cache: 2017

- AutoLock: Why Cache Attacks on ARM Are Harder Than You Think
	- USENIX Security 2017
	- Marc Green, Leandro Rodrigues Lima, Andreas Zankl, Gorka Irazoqui, Johann Heyszl, Thomas Eisenbarth
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/green
- Cache Side Channels: State of the Art and Research Opportunities
	- CCS 2017
	- Yinqian Zhang
	- https://dl.acm.org/citation.cfm?doid=3133956.3136064
	- https://yinqian.org/slides/tutorial17.pdf
- Hello from the Other Side: SSH over Robust Cache Covert Channels in the Cloud
	- Network and Distributed System Security Symposium (NDSS) 2017
	- Clémentine Maurice, Manuel Weber, Michael Schwarz, Lukas Giner, Daniel Gruss, Carlo Alberto Boano, Kay Römer, Stefan Mangard
	- slides: https://gruss.cc/files/hello_ndss_slides.pdf
	- https://github.com/IAIK/CJAG
	- BH Asia 2017: https://www.youtube.com/watch?v=a9sGk7FtnYk

## Cache: 2016

- A High-Resolution Side-channel attack on the Last Level Cache
	- DAC 2016 (best paper nominee)
	- Mehmet Kayaalp, Nael Abu-Ghazaleh, Dmitry Ponomarev, Aamer Jaleel
	- paper: http://www.cs.ucr.edu/~nael/pubs/dac16.pdf
	- slides: http://www.cs.ucr.edu/~nael/pubs/dac16.pptx
- A Software Approach to Defeating Side Channels in Last-Level Caches
	- CCS 2016
	- Ziqiao Zhou, Michael K. Reiter, Yinqian Zhang
	- https://arxiv.org/abs/1603.05615
	- https://www.youtube.com/watch?v=_dAnVtrtfdA
- ARMageddon: How Your Smartphone CPU Breaks Software-Level Security and Privacy
	- Black Hat Europe 2016: https://www.youtube.com/watch?v=9KsnFWejpQg
	- https://github.com/IAIK/armageddon
	- thesis: https://www.blackhat.com/docs/eu-16/materials/eu-16-Lipp-ARMageddon-How-Your-Smartphone-CPU-Breaks-Software-Level-Security-And-Privacy-wp.pdf
	- slides: https://www.blackhat.com/docs/eu-16/materials/eu-16-Lipp-ARMageddon-How-Your-Smartphone-CPU-Breaks-Software-Level-Security-And-Privacy.pdf
	- USENIX Security 2016
		- Moritz Lipp, Daniel Gruss, Raphael Spreitzer, Clémentine Maurice, Stefan Mangard
		- https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/lipp
- CacheBleed: A Timing Attack on OpenSSL Constant Time RSA
	- IACR 2016
	- Y. Yarom, D. Genkin, N. Heninger
	- https://eprint.iacr.org/2016/224
	- https://web.eecs.umich.edu/~genkin/cachebleed/
	- https://www.youtube.com/watch?v=Fjz4dkU2N3g
	- Section 2.2 (The Intel cache hierarchy), Section 2.5 (Intel L1 cache banks)
- Flush+Flush: A Fast and Stealthy Cache Attack
	- Detection of Intrusions and Malware & Vulnerability Assessment (DIMVA) 2016
	- Daniel Gruss, Clémentine Maurice, Klaus Wagner, Stefan Mangard
	- http://arxiv.org/abs/1511.04594
	- https://github.com/IAIK/flush_flush
- Return-Oriented Flush-Reload Side Channels on ARM and Their Implications for Android Devices
	- CCS 2016
	- Xiaokuan Zhang, Yuan Xiao, Yinqian Zhang
	- http://web.cse.ohio-state.edu/~xiao.465/fp0501-zhang.pdf
	- https://www.youtube.com/watch?v=tymvrJiJNl8

## Cache: 2015

- C5: Cross-Cores Cache Covert Channel
	- Detection of Intrusions and Malware, and Vulnerability Assessment (DIMVA) 2015
	- http://www.s3.eurecom.fr/docs/dimva15_clementine.pdf
	- https://link.springer.com/chapter/10.1007/978-3-319-20550-2_3
- Cache Attacks and Countermeasures: the Case of AES (Extended Version)
	- RSA Conference Cryptographers' Track (CT-RSA) 2006
	- Dag Arne Osvik, Adi Shamir and Eran Tromer
	- https://www.cs.tau.ac.il/~tromer/papers/cache.pdf
- Cache side channel attacks
	- 2015; Anders Fogh
	- https://dreamsofastone.blogspot.com/2015/09/cache-side-channel-attacks.html
- Last-Level Cache Side-Channel Attacks are Practical
	- 2015 IEEE Symposium on Security and Privacy
	- Fangfei Liu, Yuval Yarom, Qian Ge, Gernot Heiser, Ruby B. Lee
	- http://palms.ee.princeton.edu/system/files/SP_vfinal.pdf
	- https://www.youtube.com/watch?v=vpGI1ggKzC4

## Cache: 2007-2014

- An Analytical Model for Time-Driven Cache Attacks
	- Fast Software Encryption (FSE) 2007
	- Kris Tiri, Onur Aciiçmez, Michael Neve, Flemming Andersen
	- https://iacr.org/archive/fse2007/45930404/45930404.pdf
- FLUSH+RELOAD: A High Resolution, Low Noise, L3 Cache Side-Channel Attack
	- USENIX Security 2014
	- Yuval Yarom, Katrina Falkner
	- https://www.usenix.org/conference/usenixsecurity14/technical-sessions/presentation/yarom
	- https://eprint.iacr.org/2013/448
- New Results on Instruction Cache Attacks
	- Cryptographic Hardware and Embedded Systems (CHES) 2010
	- Onur Aciiçmez, Billy Bob Brumley, Philipp Grabher
	- https://www.iacr.org/archive/ches2010/62250105/62250105.pdf
- Yet Another MicroArchitectural Attack: Exploiting I-cache
	- CSAW 2007
	- Onur Aciiçmez
	- http://eprint.iacr.org/2007/164

## Cache: Data-Direct I/O (DDIO)

- NetCAT: Practical Cache Attacks from the Network
	- S&P 2020
	- Kurth, M.; Gras, B.; Andriesse, D.; Giuffrida, C.; Bos, H.; and Razavi, K.
	- https://www.vusec.net/projects/netcat/
	- Practical Cache Attacks from the Network and Bad Cat Puns
		- 36C3 (2019); Michael Kurth
		- https://media.ccc.de/v/36c3-10884-practical_cache_attacks_from_the_network_and_bad_cat_puns
- Packet Chasing: Spying on Network Packets over a Cache Side-Channel
	- arXiv 2019
	- Mohammadkazem Taram, Ashish Venkat, Dean Tullsen
	- https://arxiv.org/abs/1909.04841

---

# DRAM

- Another Flip in the Wall of Rowhammer Defenses
	- Security and Privacy S&P 2018
	- D. Gruss, M. Lipp, M. Schwarz, D. Genkin, J. Juffinger, S. O'Connell, W. Schoechl, Y. Yarom
	- https://csdl.computer.org/csdl/proceedings/sp/2018/4353/00/435301a489-abs.html
	- https://arxiv.org/abs/1710.00551
	- BlackHat USA 2018 - https://gruss.cc/files/us-18-Gruss-Another-Flip-In-The-Row.pdf
	- Tools for "Another Flip in the Wall" - https://github.com/IAIK/flipfloyd
- Connecting the Dots: Privacy Leakage via Write-Access Patterns to the Main Memory
	- Hardware Oriented Security and Trust (HOST) 2017
	- Tara Merin John, Syed Kamran Haider, Hamza Omar, Marten van Dijk
	- https://arxiv.org/abs/1702.03965
- DRAMA: How Your DRAM Becomes a Security Problem
	- slides: https://www.blackhat.com/docs/eu-16/materials/eu-16-Schwarz-How-Your-DRAM-Becomes-A-Security-Problem.pdf
	- thesis: DRAMA: Exploiting DRAM Buffers for Fun and Profit - https://www.blackhat.com/docs/eu-16/materials/eu-16-Schwarz-How-Your-DRAM-Becomes-A-Security-Problem-wp.pdf
	- Black Hat Europe 2016: https://www.youtube.com/watch?v=lSU6YzjIIiQ
	- USENIX 2016: https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/pessl
- Drammer: Deterministic Rowhammer Attacks on Mobile Platforms
	- CCS (2016)
	- Victor van der Veen, Yanick Fratantonio, Martina Lindorfer, Daniel Gruss, Clementine Maurice, Giovanni Vigna, Herbert Bos, Kaveh Razavi, Cristiano Giuffrida
	- https://gruss.cc/files/drammer.pdf
	- https://www.vusec.net/projects/drammer/
- Exploiting Correcting Codes: On the Effectiveness of ECC Memory Against Rowhammer Attacks
	- Security & Privacy (S&P) 2019
	- http://cs.vu.nl/~lcr220/ecc/ecc-rh-paper-sp2019-cr.pdf
	- https://www.vusec.net/projects/eccploit/
- Fantastic Timers and Where to Find Them: High-Resolution Microarchitectural Attacks in JavaScript
	- Financial Cryptography and Data Security (FC) 2017
	- Michael Schwarz, Clémentine Maurice, Daniel Gruss, Stefan Mangard
	- paper: https://gruss.cc/files/fantastictimers.pdf
	- slides: https://gruss.cc/files/timers_slides.pdf
- Flipping bits in memory without accessing them: an experimental study of DRAM disturbance errors
	- ISCA 2014
	- https://dl.acm.org/citation.cfm?id=2665726
	- http://users.ece.cmu.edu/%7Eyoonguk/papers/kim-isca14.pdf
	- https://github.com/CMU-SAFARI/rowhammer
- Hammertime: a software suite for testing, profiling and simulating the rowhammer DRAM defect - https://github.com/vusec/hammertime
- Nethammer: Inducing Rowhammer Faults through Network Requests
	- arXiv May 2018
	- Moritz Lipp, Misiker Tadesse Aga, Michael Schwarz, Daniel Gruss, Clémentine Maurice, Lukas Raab, Lukas Lamster
	- https://arxiv.org/abs/1805.04956
- RAMBleed: Reading Bits in Memory Without Accessing Them
	- IEEE Symposium on Security and Privacy (S&P) 2020
	- Kwong, Andrew and Genkin, Daniel and Gruss, Daniel and Yarom, Yuval
	- https://rambleed.com/
	- CVE: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-0174
- Rowhammer.js: A Remote Software-Induced Fault Attack in JavaScript
	- Detection of Intrusions and Malware & Vulnerability Assessment (DIMVA) 2016
	- http://arxiv.org/abs/1507.06955
	- https://github.com/IAIK/rowhammerjs
- Spying on Temperature using DRAM
	- Design, Automation, and Test in Europe (DATE) 2019
	- Wenjie Xiong, Nikolaos Athanasios Anagnostopoulos, André Schaller, Stefan Katzenbeisser, Jakub Szefer
	- http://caslab.csl.yale.edu/code/tempspy/
- Thermal Covert Channels Leveraging Package-on-Package DRAM
	- 2019 International Conference on Trust, Security and Privacy in Computing and Communications (TrustCom)
	- Shuai Chen, Wenjie Xiong, Yehan Xu, Bing Li, Jakub Szefer
	- https://caslab.csl.yale.edu/publications/chen2019thermal.pdf
	- https://caslab.csl.yale.edu/code/popchannels/
- Throwhammer: Rowhammer Attacks over the Network and Defenses
	- USENIX ATC (Annual Technical Conference) 2018
	- Andrei Tatar, Radhesh Krishnan, Elias Athanasopoulos, Cristiano Giuffrida, Herbert Bos, Kaveh Razavi
	- https://www.usenix.org/conference/atc18/presentation/tatar
	- https://www.vusec.net/download/?t=papers/throwhammer_atc18.pdf
- Understanding Rowhammer Attacks through the Lens of a Unified Reference Framework
	- 2019 arXiv
	- Xiaoxuan Lou, Fan Zhang, Zheng Leong Chua, Zhenkai Liang, Yueqiang Cheng, Yajin Zhou
	- https://arxiv.org/abs/1901.03538
- Whispers in the Hyper-space: High-speed Covert Channel Attacks in the Cloud
	- USENIX Security Symposium 2012
	- IEEE/ACM Transactions on Networking 23(2) 2015
	- Zhenyu Wu, Zhang Xu, Haining Wang
	- https://doi.org/10.1109/TNET.2014.2304439
	- https://www.usenix.org/conference/usenixsecurity12/technical-sessions/presentation/wu

---

# Electromagnetic (EM) Emanations

- A Method for Efficient Localization of Magnetic-field Sources Excited by the Execution of Instructions in a Processor
	- 2017 IEEE Transactions on Electromagnetic Compatibility
	- F. Werner, D. A. Chu, A. R. Djordjevic, D. I. Olcan, M. Prvulovic, and A. Zajic.
	- https://doi.org/10.1109/TEMC.2017.2742501
	- http://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2017/10/TEMC_245_2017.pdf
- A New Side-Channel Vulnerability on Modern Computers by Exploiting Electromagnetic Emanations from the Power Management Unit
	- High-Performance Computer Architecture (HPCA) 2020
	- Nader Sehatbakhsh, Baki Yilmaz, Alenka Zajic, Milos Prvulovic
	- https://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2020/01/HPCA2020_2.pdf
- A Practical Methodology for Measuring the Side-Channel Signal Available to the Attacker for Instruction-Level Events
	- MICRO-47 2014
	- Robert Callan, Alenka Zajić, Milos Prvulovic
	- https://www.cc.gatech.edu/home/milos/Papers/2014_MICRO_SAVAT.pdf
- A Survey of Electromagnetic Side-Channel Attacks and Discussion on their Case-Progressing Potential for Digital Forensics
	- Digital Investigation, Volume 29, June 2019
	- Asanka Sayakkara, Nhien-An Le-Khac, Mark Scanlon
	- https://arxiv.org/abs/1903.07703
- An Algorithm for Finding Carriers of Amplitude-modulated Electromagnetic Emanations in Computer Systems
	- 2016 10th European Conference on Antennas and Propagation (EuCAP)
	- C. Wang, R. Callan, A. Zajic, M. Prvulovic
	- https://doi.org/10.1109/EuCAP.2016.7481633
	- http://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2016/08/EUCap16.pdf
- Capacity of the EM Covert/Side-Channel Created by the Execution of Instructions in a Processor
	- 2017, IEEE Transactions on Information Forensics and Security
	- http://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2017/10/T-IFS-07378-2017.pdf
- Complete Reverse Engineering of Neural Network Architectures Through Electromagnetic Side Channels
	- USENIX Security 2019
	- Lejla Batina, Shivam Bhasin, Dirmanto Jap, Stjepan Picek
	- https://www.usenix.org/conference/usenixsecurity19/presentation/batina
- Detailed Tracking of Program Control Flow Using Analog Side-Channel Signals: A Promise for IoT Malware Detection and a Threat for Many Cryptographic Implementations
	- SPIE 2018
	- Haider Adnan Khan, Monjur Alam, Alenka Zajic, Milos Prvulovic
	- https://www.researchgate.net/publication/324584326_Detailed_Tracking_of_Program_Control_Flow_Using_Analog_Side-Channel_Signals_A_Promise_for_IoT_Malware_Detection_and_a_Threat_for_Many_Cryptographic_Implementations
- EDDIE: EM-Based Detection of Deviations in Program Execution
	- 2017, Proceedings of the 44th International Symposium on Computer Architecture (ISCA)
	- http://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2017/06/ISCA17.pdf
- Electromagnetic Side Channel Information Leakage Created by Execution of Series of Instructions in a Computer Processor
	- IEEE Transactions on Information Forensics and Security (TIFS) Vol. 15, 2020
	- Baki Berkay Yilmaz, Milos Prvulovic, Alenka Zajic
	- https://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2019/08/T-IFS-09685-2019-R2.pdf
- EMPROF: Memory Profiling via EM-Emanation in IoT and Hand-Held Devices
	- MICRO-51 (2018)
	- Moumita Dey, Alireza Nazari, Alenka Zajic, Milos Prvulovic
	- Lightning Talk - https://www.youtube.com/watch?v=GCgnEJk_LCQ
	- https://www.researchgate.net/publication/329654406_EMPROF_Memory_Profiling_Via_EM-Emanation_in_IoT_and_Hand-Held_Devices
- EMSim: A Microarchitecture-Level Simulation Tool for Modeling Electromagnetic Side-Channel Signals
	- High-Performance Computer Architecture (HPCA) 2020
	- Nader Sehatbakhsh, Baki Yilmaz, Alenka Zajic, Milos Prvulovic
	- https://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2020/01/HPCA20_1.pdf
- FASE: Finding Amplitude-modulated Side-channel Emanations
	- ISCA 2015
	- Robert Callan, Alenka Zajic, Milos Prvulovic
	- https://www.cc.gatech.edu/~milos/Papers/2015_ISCA_FASE.pdf
- MagneticSpy: Exploiting Magnetometer in Mobile Devices for Website and Application Fingerprinting
	- arXiv 2019
	- Nikolay Matyunin, Yujue Wang, Tolga Arul, Jakub Szefer, Stefan Katzenbeisser
	- https://arxiv.org/abs/1906.11117
- One & Done: A Single-Decryption EM-Based Attack on OpenSSL’s Constant-Time Blinded RSA
	- USENIX Security 2018
	- Monjur Alam, Haider Adnan Khan, Moumita Dey, Nishith Sinha, Robert Callan, Alenka Zajic, Milos Prvulovic
	- https://www.usenix.org/conference/usenixsecurity18/presentation/alam
- Quantifying Information Leakage in a Processor Caused by the Execution of Instructions
	- 2017, Proceedings of IEEE MILCOM
	- http://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2017/10/MILCOM_Capacity.pdf
- Screaming Channels: When Electromagnetic Side Channels Meet Radio Transceivers
	- ACM CCS 2018; Black Hat USA 2018
	- Giovanni Camurati, Sebastian Poeplau, Marius Muench, Tom Hayes, Aurélien Francillon
	- http://s3.eurecom.fr/tools/screaming_channels/
	- https://github.com/eurecom-s3/screaming_channels
	- ACM CCS 2018 - https://www.youtube.com/watch?v=0IafNH2WHxk
	- When Electromagnetic Side Channels Meet Radio Transceivers
		- GreHack 2018; Marius Muench
		- https://www.youtube.com/watch?v=vtcoZYS_C08
- Side-Channel-Based Code-Execution Monitoring Systems - A Survey
	- Yi Han, Ioannis Christoudis, Konstantinos I. Diamantaras, Saman A. Zonouz, Athina P. Petropulu
	- IEEE Signal Processing Magazine 36(2) 2019
	- https://ieeexplore.ieee.org/document/8653533
	- https://www.researchgate.net/publication/330225481_Side-Channel-Based_Code-Execution_Monitoring_Systems_-_A_Survey
- Software Profiling via Electromagnetic Side-Channel Signal
	- 2020 PhD Dissertation; Alireza Nazari
	- http://hdl.handle.net/1853/62720
- Spectral Profiling: Observer-Effect-Free Profiling by Monitoring EM Emanations
	- 2016, IEEE MICRO 16
	- http://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2016/08/MICRO16.pdf
- The EM Side–Channel(s): Attacks and Assessment Methodologies
	- 2002, Cryptographic Hardware and Embedded Systems (CHES)
	- https://www.cs.jhu.edu/~astubble/600.412/s-c-papers/em.pdf
	- http://citeseerx.ist.psu.edu/viewdoc/summary;?doi=10.1.1.122.1646
	- https://www.semanticscholar.org/paper/The-EM-Side-Channel-s-Attacks-and-Assessment-Metho-Agrawal-Archambeault/7d687c23e297196e4de38240f9b48eb2d31f20fe
- Watch Me, but Don't Touch Me! Contactless Control Flow Monitoring via Electromagnetic Emanations
	- 2017, Proceedings of the 2017 ACM SIGSAC Conference on Computer and Communications Security (CCS)
	- https://arxiv.org/abs/1708.09099
- Zero-Overhead Profiling via Electromagnetic (EM) Emanations
	- 2016, Proceedings of the 25th International Symposium on Software Testing and Analysis (ISSTA)
	- https://dl.acm.org/citation.cfm?id=2931065
	- https://issta2016.cispa.saarland/zero-overhead-profiling-via-em-emanations/
	- http://alenka.ece.gatech.edu/wp-content/uploads/sites/463/2016/09/ZoP.pdf

## Electromagnetic (EM) Emanations: 2021

- Let’s Take it Offline: Boosting Brute-Force Attacks on iPhone’s User Authentication through SCA
	- IACR Transactions on Cryptographic Hardware and Embedded Systems (TCHES) 2021(3)
	- Oleksiy Lisovets, David Knichel, Thorben Moos, Amir Moradi
	- https://eprint.iacr.org/2021/460
	- https://iacr.org/cryptodb/data/paper.php?pubkey=31293
	- https://www.youtube.com/watch?v=JwOJr0JEoiM

---

# Floating Point Unit (FPU)

- LazyFP: Leaking FPU Register State using Microarchitectural Side-Channels
	- 2018; Julian Stecklina, Thomas Prescher
	- https://arxiv.org/abs/1806.07480
	- Intel LazyFP vulnerability: Exploiting lazy FPU state switching
		- http://blog.cyberus-technology.de/posts/2018-06-06-intel-lazyfp-vulnerability.html
- On Subnormal Floating Point and Abnormal Timing
	- IEEE Security and Privacy (“Oakland”) 2015
	- Marc Andrysco, David Kohlbrenner Keaton Mowery, Ranjit Jhala, Sorin Lerner, Hovav Shacham
	- http://www.ieee-security.org/TC/SP2015/papers-archived/6949a623.pdf
	- https://cseweb.ucsd.edu/~dkohlbre/papers/subnormal.pdf
	- https://homes.cs.washington.edu/~dkohlbre/papers/subnormal.pdf
	- https://hovav.net/ucsd/papers/akmjls15.html
	- https://github.com/kmowery/libfixedtimefixedpoint

---

# FPGA

- Physical Side-Channel Attacks and Covert Communication on FPGAs: A Survey
	- Field Programmable Logic and Applications (FPL) 2019
	- Seyedeh Sharareh Mirzargar, Mirjana Stojilovic
	- https://dx.doi.org/10.1109/FPL.2019.00039
	- https://infoscience.epfl.ch/record/272348?ln=en
	- https://fpl2019.bsc.es/sites/default/files/uploaded/A32.FPL2019-slides-PhysicalSideChannelAttacks.pdf
- Recent Attacks and Defenses on FPGA-based Systems
	- ACM Transactions on Reconfigurable Technology and Systems 12(3) 2019
	- Jiliang Zhang, Gang Qu
	- https://doi.org/10.1145/3340557
	- http://hardwaresecurity.cn/FPGAsecurity.pdf

## FPGA remote attacks

(through (partial) access on configuration/bitstream)

- An Inside Job: Remote Power Analysis Attacks on FPGAs
	- Cryptology ePrint Archive: Report 2018/012
	- Falk Schellenberg, Dennis R.E. Gnad, Amir Moradi, Mehdi B. Tahoori
	- https://eprint.iacr.org/2018/012
- C3APSULe: Cross-FPGA Covert-Channel Attacks through Power Supply Unit Leakage
	- 2020 IEEE Symposium on Security and Privacy (S&P)
	- Ilias Giechaskiel, Kasper Bonne Rasmussen, Jakub Szefer
	- https://www.computer.org/csdl/proceedings-article/sp/2020/349700a890/1i0rIjF42ic
	- https://ilias.giechaskiel.com/papers/capsule-sp-preprint.pdf
- FPGAhammer: Remote Voltage Fault Attacks on Shared FPGAs, suitable for DFA on AES
	- IACR Transactions on Cryptographic Hardware and Embedded Systems, 2018(3), 44-68.
	- Jonas Krautter, Dennis R.E. Gnad, Mehdi B. Tahoori
	- https://tches.iacr.org/index.php/TCHES/article/view/7268
- FPGA Side Channel Attacks without Physical Access
	- FCCM 2018
	- C. Ramesh, S. B. Patil, S. N. Dhanuskodi, G. Provelengios, S. Pillement, D. Holcomb, R. Tessier
	- http://www.ecs.umass.edu/ece/tessier/ramesh-fccm18.pdf
- FPGA-Based Remote Power Side-Channel Attacks
	- IEEE Symposium on Security and Privacy (S&P) 2018
	- Mark Zhao, G. Edward Suh
	- https://csdl.computer.org/csdl/proceedings/sp/2018/4353/00/435301a805-abs.html
	- https://sites.coecis.cornell.edu/edsuh/files/2018/04/SP2018-FPGA-2m12dnp.pdf
- FPGA Viruses
	- 1999 9th International Workshop on Field Programmable Logic and Applications (FPL)
	- I Hadzic, S Udani, J M Smith
	- https://repository.upenn.edu/cgi/viewcontent.cgi?article=1096&amp;context=cis_reports
	- http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.43.9135
	- https://link.springer.com/chapter/10.1007/978-3-540-48302-1_30
	- https://dl.acm.org/citation.cfm?id=739074
- JackHammer: Efficient Rowhammer on Heterogeneous FPGA-CPU Platforms
	- 2019 arXiv
	- IACR Transactions on Cryptographic Hardware and Embedded Systems (TCHES), Volume 2020, Issue 3
	- Zane Weissman, Thore Tiemann, Daniel Moghimi, Evan Custodio, Thomas Eisenbarth, Berk Sunar
	- https://arxiv.org/abs/1912.11523
- Leaky Wires: Information Leakage and Covert Communication Between FPGA Long Wires
	- AsiaCCS 2018
	- Ilias Giechaskiel, Kasper B. Rasmussen, Ken Eguro
	- http://arxiv.org/abs/1611.08882
	- http://www.cs.ox.ac.uk/files/9835/fpga.pdf
- Measuring Long Wire Leakage with Ring Oscillators in Cloud FPGAs
	- International Conference on Field−Programmable Logic and Applications (FPL) 2019
	- Ilias Giechaskiel‚ Kasper Rasmussen and Jakub Szefer
	- https://www.cs.ox.ac.uk/publications/publication12562-abstract.html
- Reading Between the Dies: Cross-SLR Covert Channels on Multi-Tenant Cloud FPGAs
	- International Conference on Computer Design (ICCD) 2019
	- Ilias Giechaskiel, Kasper Rasmussen, Jakub Szefer
	- https://ilias.giechaskiel.com/papers/slr-iccd-preprint.pdf
	- https://caslab.csl.yale.edu/code/slr-covert-channel/
- Remote Inter-Chip Power Analysis Side-Channel Attacks at Board-Level
	- Cryptology ePrint Archive: Report 2018/881
	- Falk Schellenberg, Dennis R.E. Gnad, Amir Moradi, Mehdi B. Tahoori
	- https://eprint.iacr.org/2018/881
- Temperature-based covert channel in FPGA systems
	- 2011 6th International Workshop on Reconfigurable Communication-Centric Systems-on-Chip (ReCoSoC)
	- Taras Iakymchuk, Maciej Nikodem, Krzysztof Kepa
	- https://ieeexplore.ieee.org/abstract/document/5981510
- Temporal Thermal Covert Channels in Cloud FPGAs
	- International Symposium on Field-Programmable Gate Arrays (FPGA) 2019
	- Shanquan Tian, Jakub Szefer
	- https://caslab.csl.yale.edu/publications/tian2019temporal.pdf
	- https://dl.acm.org/citation.cfm?doid=3289602.3293920
	- https://new.isfpga.org/past/fpga2019/slides/Tian_TemporalThermalCovertChannelsinCloudFPGAs.pptx
	- http://caslab.csl.yale.edu/code/temporalthermalcc/
- Timing Violation Induced Faults in Multi-Tenant FPGAs
	- 2019 Design, Automation & Test in Europe Conference & Exhibition (DATE)
	- Dina Mahmoud, Mirjana Stojilovic
	- https://ieeexplore.ieee.org/abstract/document/8715263
- Voltage drop-based fault attacks on FPGAs using valid bitstreams
	- 2017 27th International Conference on Field Programmable Logic and Applications (FPL)
	- Dennis R. E. Gnad, Fabian Oboril, Mehdi B. Tahoori
	- https://ieeexplore.ieee.org/abstract/document/8056840

## FPGA local attacks

(with physical access or within close proximity)

- Breakthrough Silicon Scanning Discovers Backdoor in Military Chip
	- Cryptographic Hardware and Embedded Systems (CHES) 2012
	- Sergei Skorobogatov, Christopher Woods
	- https://www.cl.cam.ac.uk/~sps32/ches2012-backdoor.pdf
	- https://www.cl.cam.ac.uk/~sps32/ches2012_slides.pdf
- Electromagnetic Side-channel Attack against 28-nm FPGA Device
	- WISA (2012)
	- Yohei Hori, Toshihiro Katashita, Akihiko Sasaki, Akashi Satoh
	- https://staff.aist.go.jp/hori.y/articles/hori_wisa2012.pdf
- Improved Side-Channel Analysis Attacks on Xilinx Bitstream Encryption of 5, 6, and 7 Series
	- Constructive Side-Channel Analysis and Secure Design (COSADE) 2016
	- Amir Moradi, Tobias Schneider
	- https://www.emsec.rub.de/media/attachments/files/2017/04/AmirTalk_2016-04-14_COSADE.pdf
	- https://eprint.iacr.org/2016/249
- Side Channel Attack on Low Power FPGA Platform
	- 2016 Master Thesis; Mustafa Faraj
	- https://uwspace.uwaterloo.ca/bitstream/handle/10012/10769/Faraj_Mustafa.pdf?sequence=3

## FPGA attacks countermeasures

- Active Fences against Voltage-based Side Channels in Multi-Tenant FPGAs
	- ICCAD 2019
	- Jonas Krautter, Dennis R.E. Gnad, Falk Schellenberg, Amir Moradi, Mehdi B. Tahoori
	- https://eprint.iacr.org/2019/1152
- Checking for Electrical Level Security Threats in Bitstreams for Multi-Tenant FPGAs
	- 2018 International Conference on Field-Programmable Technology (FPT)
	- Dennis R.E. Gnad, S. Rapp, J. Krautter, Mehdi B. Tahoori
	- https://cdnc.itec.kit.edu/downloads/Papers/bitstream_checking.pdf
- Generic side-channel countermeasures for reconfigurable devices
	- International Workshop on Cryptographic Hardware and Embedded Systems (CHES) 2011
	- Tim Güneysu and Amir Moradi
	- https://www.emsec.ruhr-uni-bochum.de/media/crypto/veroeffentlichungen/2012/01/30/GSCC-CHES11.pdf
	- https://iacr.org/archive/ches2011/69170033/69170033.pdf
	- https://link.springer.com/chapter/10.1007/978-3-642-23951-9_3
- Moats and drawbridges: An isolation primitive for reconfigurable hardware based systems
	- IEEE Symposium on Security and Privacy (S&P) 2007
	- Ted Huffmire, Brett Brotherton, Gang Wang, Timothy Sherwood, Ryan Kastner, Timothy Levin, Thuy Nguyen, Cynthia Irvine
	- http://cs.ucsb.edu/~sherwood/pubs/IEEESP-moats.pdf
	- https://ieeexplore.ieee.org/abstract/document/4223233/
- Side-channel resistant crypto for less than 2,300 GE
	- Journal of Cryptology 24, no. 2 (2011)
	- Axel Poschmann, Amir Moradi, Khoongming Khoo, Chu-Wee Lim, Huaxiong Wang, San Ling
	- https://www.emsec.ruhr-uni-bochum.de/media/crypto/veroeffentlichungen/2011/01/15/side_channel_2010.pdf
	- https://link.springer.com/article/10.1007/s00145-010-9086-6

---

# Frontend

- Leaky Frontends: Security Vulnerabilities in Processor Frontends
	- International Symposium on High-Performance Computer Architecture (HPCA) 2022
	- Shuwen Deng, Bowen Huang, Jakub Szefer
	- https://arxiv.org/abs/2105.12224
	- https://caslab.csl.yale.edu/code/leaky-frontends/

---

# GPU

- A complete key recovery timing attack on a GPU
	- High Performance Computer Architecture (HPCA) 2016
	- Zhen Hang Jiang, Yunsi Fei, David Kaeli
	- https://doi.org/10.1109/HPCA.2016.7446081
- A Novel Side-Channel Timing Attack on GPUs
	- Great Lakes Symposium on VLSI (GLSVLSI) 2017
	- Zhen Hang Jiang, Yunsi Fei, David Kaeli
	- https://doi.org/10.1145/3060403.3060462
- Confidentiality Issues on a GPU in a Virtualized Environment
	- FC 2014: Financial Cryptography and Data Security
	- Clémentine Maurice, Christoph Neumann, Olivier Heen, Aurélien Francillon
	- https://doi.org/10.1007/978-3-662-45472-5_9
	- https://www.eurecom.fr/publication/4205
	- http://s3.eurecom.fr/docs/fc14_maurice.pdf
- Constructing and Characterizing Covert Channels on GPGPUs
	- MICRO-50, 2017
	- Hoda Naghibijouybari, Khaled N. Khasawneh, Nael Abu-Ghazaleh
	- http://www.cs.ucr.edu/~kkhas001/pubs/micro17-gpu.pdf
- CUDA Leaks: Information Leakage in GPU Architectures
	- ACM Transactions on Embedded Computing Systems (TECS) 2016
	- Roberto Di Pietro, Flavio Lombardi, Antonio Villani
	- https://arxiv.org/abs/1305.7383
	- https://dl.acm.org/citation.cfm?id=2801153
- Exploiting Bank Conflict-based Side-channel Timing Leakage of GPUs
	- ACM Transactions on Architecture and Code Optimization (TACO) 16(4) 2019
	- Jiang Zhen Hang, Fei Yunsi, Kaeli David
	- https://doi.org/10.1145/3361870
- GPU Security Exposed: Exploiting Shared Memory
	- Black Hat Europe 2016
	- Justin Taft
	- https://www.blackhat.com/docs/eu-16/materials/eu-16-Taft-GPU-Security-Exposed.pdf
- GPUGuard: Mitigating Contention Based Side and Covert Channel Attacks on GPUs
	- International Conference on Super-computing (ICS) 2019
	- Qiumin Xu, Hoda Naghibijouybari, Shibo Wang, Nael Abu-Ghazaleh, Mu-rali Annavaram
	- https://doi.org/10.1145/3330345.3330389
- Grand Pwning Unit: Accelerating Microarchitectural Attacks with the GPU
	- S&P 2018
	- P. Frigo, C. Giuffrida, H. Bos, K. Razavi
	- https://www.vusec.net/projects/glitch/
	- https://www.vusec.net/wp-content/uploads/2018/05/glitch.pdf
- Network-on-Chip Microarchitecture-based Covert Channel in GPUs
	- MICRO 2021
	- Jaeguk Ahn, Jiho Kim, Hans Kasan, Leila Delshadtehrani, Wonjun Song, Ajay Joshi, John Kim
	- https://dl.acm.org/doi/10.1145/3466752.3480093
- Practical Microarchitectural Attacks from Integrated GPU
	- 2017 Master’s Thesis; 2017 Pietro Frigo
	- https://repository.tudelft.nl/islandora/object/uuid:c0d3c629-4c67-4741-9776-05802d89872f
- RCoal: Mitigating GPU Timing Attack via Subwarp-based Randomized Coalescing Technique
	- Proceedings of the 24th International Symposium on High-Performance Computer Architecture (HPCA), 2018
	- Gurunath Kadam, [Danfeng Zhang](http://www.cse.psu.edu/~dbz5017/publication.html), [Adwait Jog](http://adwaitjog.github.io/pubs.html)
	- http://adwaitjog.github.io/docs/pdf/rcoal-hpca18.pdf
	- http://www.cse.psu.edu/~dbz5017/pub/hpca18.pdf
- Rendered Insecure: GPU Side Channel Attacks are Practical
	- Computer and Communications Security (CCS) 2018
	- Hoda Naghibijouybari, Ajaya Neupane, Zhiyun Qian, and Nael Abu-Ghazaleh
	- https://doi.org/10.1145/3243734.3243831
	- http://www.cs.ucr.edu/~zhiyunq/pub/ccs18_gpu_side_channel.pdf
	- http://www.cs.ucr.edu/~nael/pubs/ccs18.pdf
	- https://www.youtube.com/watch?v=lFspD48dahc
- Side Channel Attacks on GPUs
	- IEEE Transactions on Dependable and Secure Computing (TDSC) 2019
	- H. NaghibiJouybari, A. Neupane, Z. Qian, N. Abu-Ghazaleh
	- http://dx.doi.org/10.1109/TDSC.2019.2944624

---

# Interconnect

## Interconnect: 2022

- Don't Mesh Around: Side-Channel Attacks and Mitigations on Mesh Interconnects
	- USENIX Security 2022
	- Miles Dai, Riccardo Paccagnella, Miguel Gomez-Garcia, John McCalpin, Mengjia Yan
	- https://www.usenix.org/conference/usenixsecurity22/presentation/dai
	- https://github.com/CSAIL-Arch-Sec/dont-mesh-around

## Interconnect: 2021

- Calibration Done Right: Noiseless Flush+Flush Attacks
	- Detection of Intrusions and Malware & Vulnerability Assessment (DIMVA) 2021
	- Guillaume Didier, Clémentine Maurice
	- https://cmaurice.fr/pdf/dimva21_didier.pdf
	- https://github.com/MIAOUS-group/calibration-done-right
	- "Flush+Flush is a stealthy and fast one [attack] that uses the timing of the `clflush` instruction depending on whether a line is cached. We show that the CPU interconnect plays a bigger role than previously thought in these timings and in Flush+Flush error rate."
- Lord of the Ring(s): Side Channel Attacks on the CPU On-Chip Ring Interconnect Are Practical
	- USENIX Security 2021
	- Riccardo Paccagnella, Licheng Luo, Christopher W. Fletcher
	- https://arxiv.org/abs/2103.03443
	- https://github.com/FPSG-UIUC/lotr

---

# Interrupts

- An Empirical Bandwidth Analysis of Interrupt-Related Covert Channels
	- IJSSE 2015
	- Richard Gay, Heiko Mantel, Henning Sudbrock
	- https://www.semanticscholar.org/paper/An-Empirical-Bandwidth-Analysis-of-Interrupt-Relat-Gay-Mantel/d81d95e8969edd37a3f47335b98a9b6ce9e3942f
	- http://www.mais.informatik.tu-darmstadt.de/WebBibPHP/papers/2013/2013-GayMantelSudbrock-EmpiricalIRCC.pdf
- Nemesis: Studying Microarchitectural Timing Leaks in Rudimentary CPU Interrupt Logic
	- Computer & Communications Security (CCS) 2018
	- Jo Van Bulck, Frank Piessens, Raoul Strackx
	- https://github.com/jovanbulck/nemesis
	- https://people.cs.kuleuven.be/~jo.vanbulck/ccs18.pdf
	- https://distrinet.cs.kuleuven.be/software/sancus/publications/ccs18.pdf
	- https://distrinet.cs.kuleuven.be/software/sancus/publications/ccs18-slides.pdf
	- https://www.youtube.com/watch?v=njE9Vg8HOqk

---

# Keyboard

- SoK: Keylogging Side Channels
	- IEEE Symposium on Security and Privacy (S&P) 2018
	- John V. Monaco
	- https://csdl.computer.org/csdl/proceedings/sp/2018/4353/00/435301a420-abs.html
	- https://oaklandsok.github.io/papers/monaco2018.pdf
- KeyDrown: Eliminating Software-Based Keystroke Timing Side-Channel Attacks
	- NDSS 2018
	- Michael Schwarz, Moritz Lipp, Daniel Gruss, Samuel Weiser, Clémentine Maurice, Raphael Spreitzer, Stefan Mangard
	- https://arxiv.org/abs/1706.06381
	- https://www.ndss-symposium.org/wp-content/uploads/2018/02/ndss2018_04B-1_Schwarz_paper.pdf
	- https://www.ndss-symposium.org/wp-content/uploads/2018/03/NDSS2018_04B-1_Schwarz_Slides.pdf
	- https://www.youtube.com/watch?v=limElEZNdS8

---

# Magnetic

- MAGNETO: Covert Channel between Air-Gapped Systems and Nearby Smartphones via CPU-Generated Magnetic Fields
	- https://cyber.bgu.ac.il/advanced-cyber/airgap
	- Mordechai Guri, Andrey Daidakulov, Yuval Elovici
	- https://arxiv.org/abs/1802.02317
	- Paper: https://arxiv.org/abs/1802.02317
	- Video: https://www.youtube.com/watch?v=yz8E5n1Tzlo
- ODINI: Escaping Sensitive Data from Faraday-Caged, Air-Gapped Computers via Magnetic Fields
	- https://cyber.bgu.ac.il/advanced-cyber/airgap
	- Mordechai Guri, Boris Zadov, Andrey Daidakulov, Yuval Elovici
	- Paper: https://arxiv.org/abs/1802.02700
	- Video: https://www.youtube.com/watch?v=h07iXD-aSCA

---

# Memory Bus

- An Off-Chip Attack on Hardware Enclaves via the Memory Bus
	- USENIX Security Symposium 2020
	- Dayeol Lee, Dongha Jung, Ian T. Fang, Chia-Che Tsai, Raluca Ada Popa
	- https://arxiv.org/abs/1912.01701
- GSMem: Data Exfiltration from Air-Gapped Computers over GSM Frequencies
	- USENIX Security 2015
	- Mordechai Guri, Assaf Kachlon, Ofer Hasson, Gabi Kedma, Yisroel Mirsky, Yuval Elovici
	- https://www.usenix.org/conference/usenixsecurity15/technical-sessions/presentation/guri
	- System Bus Radio: Transmits AM radio on computers without radio transmitting hardware
		- https://github.com/fulldecent/system-bus-radio
- Whispers in the hyper-space: high-speed covert channel attacks in the cloud, USENIX Security 2012
	- https://www.usenix.org/conference/usenixsecurity12/technical-sessions/presentation/wu
	- https://www.youtube.com/watch?v=d2TU_Q4U9DA

---

# Memory Management Unit (MMU)

- ASLR on the Line: Practical Cache Attacks on the MMU
	- NDSS 2017
	- B. Gras, K. Razavi, E. Bosman, H. Bos, C. Giuffrida
	- https://www.vusec.net/download/?t=papers/anc_ndss17.pdf
	- 34C3 (2017)
		- https://media.ccc.de/v/34c3-9135-aslr_on_the_line
		- https://github.com/brainsmoke/pub-archive/raw/master/slides/aotl-34c3-slides.pdf
- Binoculars: Contention-Based Side-Channel Attacks Exploiting the Page Walker
	- USENIX Security 2022
	- Zirui Neil Zhao, Adam Morrison, Christopher Fletcher, Josep Torrellas
	- https://www.usenix.org/conference/usenixsecurity22/presentation/zhao-zirui
	- https://github.com/zzrcxb/binoculars
- Malicious Management Unit: Why Stopping Cache Attacks in Software is Harder Than You Think
	- USENIX Security 2018
	- Stephan van Schaik, Cristiano Giuffrida, Herbert Bos, Kaveh Razavi
	- https://github.com/vusec/xlate
	- https://www.vusec.net/projects/xlate/
	- https://www.usenix.org/conference/usenixsecurity18/presentation/van-schaik
- PThammer: Cross-User-Kernel-Boundary Rowhammer through Implicit Accesses
	- International Symposium on Microarchitecture (MICRO) 2020
	- Zhi Zhang, Yueqiang Cheng, Dongxi Liu, Surya Nepal, Zhi Wang, Yuval Yarom
	- https://arxiv.org/abs/2007.08707
- RevAnC: A Framework for Reverse Engineering Hardware Page Table Caches
	- EuroSec 2017
	- 2017 Technical Report: Reverse Engineering Hardware Page Table Caches Using Side-Channel Attacks on the MMU
	- S. van Schaik, K. Razavi, B. Gras, H. Bos, C. Giuffrida
	- https://www.vusec.net/projects/anc
	- https://www.vusec.net/download/?t=papers/revanc_ir-cs-77.pdf
- Telling Your Secrets without Page Faults: Stealthy Page Table-Based Attacks on Enclaved Execution
	- USENIX Security Symposium 2017
	- Jo Van Bulck, Nico Weichbrodt, Rüdiger Kapitza, Frank Piessens, Raoul Strackx
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/van-bulck
	- https://github.com/jovanbulck/sgx-pte

---

# Memory Order Buffer (MOB)

- Microarchitectural Minefields: 4K-Aliasing Covert Channel and Multi-Tenant Detection in IaaS Clouds
	- NDSS 2018
	- Dean Sullivan, Orlando Arias, Travis Meade, Yier Jin
	- https://www.ndss-symposium.org/wp-content/uploads/2018/02/ndss2018_06A-3_Sullivan_paper.pdf
	- https://www.ndss-symposium.org/wp-content/uploads/2018/03/NDSS2018-06A-3_Sullivan_Slides.pdf
	- https://www.youtube.com/watch?v=0KIojo5nk2s
- SPOILER: Speculative Load Hazards Boost Rowhammer and Cache Attacks
	- USENIX Security 2019
	- Saad Islam, Ahmad Moghimi, Ida Bruhns, Moritz Krebbel, Berk Gulmezoglu, Thomas Eisenbarth, Berk Sunar
	- https://arxiv.org/abs/1903.00446

---

# Micro-Op Cache

- I See Dead µops: Leaking Secrets via Intel/AMD Micro-Op Caches
	- IEEE International Symposium on Computer Architecture (ISCA) 2021
	- Xida Ren, Logan Moody, Mohammadkazem Taram, Matthew Jordan, Dean M. Tullsen, Ashish Venkat
	- https://www.cs.virginia.edu/venkat/papers/isca2021a.pdf
	- "Modern Intel, AMD, and ARM processors translate complex instructions into simpler internal micro-ops that are then cached in a dedicated on-chip structure called the micro-op cache. This work presents an in-depth characterization study of the micro-op cache, reverse-engineering many undocumented features, and further describes attacks that exploit the micro-op cache as a timing channel to transmit secret information. In particular, this paper describes three attacks – (1) a same thread cross-domain attack that leaks secrets across the user-kernel boundary, (2) a cross-SMT thread attack that transmits secrets across two SMT threads via the micro-op cache, and (3) transient execution attacks that have the ability to leak an unauthorized secret accessed along a misspeculated path, even before the transient instruction is dispatched to execution, breaking several existing invisible speculation and fencing-based solutions that mitigate Spectre."
- UC-Check: Characterizing Micro-operation Caches in x86 Processors and Implications in Security and Performance
	- MICRO 2021
	- Joonsung Kim, Hamin Jang, Hunjun Lee, Seungho Lee, Jangwoo Kim
	- https://dl.acm.org/doi/10.1145/3466752.3480079
	- https://github.com/SNU-HPCS/UC-Check
	- https://www.youtube.com/watch?v=1jvHDjxscoo

---

# Power

- A New Class of Covert Channels Exploiting Power Management Vulnerabilities
	- IEEE Computer Architecture Letters (2018)
	- S. K. Khatamifard, L. Wang, S. Kose, U. R. Karpuzcu
	- http://doi.ieeecomputersociety.org/10.1109/LCA.2018.2860006
	- http://people.ece.umn.edu/~ukarpuzc/Karpuzcu_files/calSec.pdf
	- https://experts.umn.edu/en/publications/a-new-class-of-covert-channels-exploiting-power-management-vulner
- CLKSCREW: Exposing the Perils of Security-Oblivious Energy Management
	- 2017 26th USENIX Security Symposium
	- Adrian Tang, Simha Sethumadhavan, and Salvatore Stolfo
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/tang
- Hertzbleed: Turning Power Side-Channel Attacks Into Remote Timing Attacks on x86
	- USENIX Security 2022
	- Yingchen Wang, Riccardo Paccagnella, Elizabeth He, Hovav Shacham, Christopher W. Fletcher, David Kohlbrenner
	- https://www.hertzbleed.com/
	- https://github.com/FPSG-UIUC/hertzbleed
	- https://www.hertzbleed.com/herzbleed.pdf
- IChannels: Exploiting Current Management Mechanisms to Create Covert Channels in Modern Processors
	- ISCA 2021
	- Jawad Haj-Yahya, Jeremie S. Kim, A. Giray Yaglikci, Ivan Puddu, Lois Orosa, Juan Gómez Luna, Mohammed Alser, Onur Mutlu
	- https://arxiv.org/abs/2106.05050
	- http://people.inf.ethz.ch/omutlu/pub/IChannels-covert-channels_isca21.pdf
	- https://youtube.com/watch?v=Why4Ffn5bRY
- Leaky Noise: New Side-Channel Attack Vectors in Mixed-Signal IoT Devices
	- IACR Transactions on Cryptographic Hardware and Embedded Systems, 2019(3), 305-339.
	- Dennis R. E. Gnad, Jonas Krautter, Mehdi B. Tahoori
	- https://tches.iacr.org/index.php/TCHES/article/view/8297
- MIRACLE: MIcRo-ArChitectural Leakage Evaluation
	- The SCARV Miracle study aims to provide a rigorous and systematic evaluation of micro-architectural power side-channel leakage effects found in common embedded CPUs and micro-controllers.
	- Ben Marshall, Daniel Page, James Webb
	- https://eprint.iacr.org/2021/261
	- https://github.com/scarv/miracle
	- https://miracle.scarv.org/
- On Code Execution Tracking via Power Side-Channel
	- Conference on Computer and Communications Security (CCS) 2016
	- Yannan Liu, Lingxiao Wei, Zhe Zhou, Kehuan Zhang, Wenyuan Xu, Qiang Xu
	- https://dl.acm.org/citation.cfm?id=2978299
	- https://www.youtube.com/watch?v=YwL_p3TxhlA
- PLATYPUS: Software-based Power Side-Channel Attacks on x86
	- 2020; IEEE Symposium on Security & Privacy (S&P) 2021
	- Moritz Lipp, Andreas Kogler, David Oswald, Michael Schwarz, Catherine Easdon, Claudio Canella, Daniel Gruss
	- https://platypusattack.com/
- POWERT Channels: A Novel Class of Covert Communication Exploiting Power Management Vulnerabilities
	- High-Performance Computer Architecture (HPCA) 2019
	- S. K. Khatamifard, L. Wang, S. Köse, and U. R. Karpuzcu
	- https://doi.org/10.1109/HPCA.2019.00045
	- http://hajim.rochester.edu/ece/sites/kose/files/conferences/hpca_19.pdf
	- PoC (Lorenzo Masciullo): https://github.com/lore-masc/POWERTChannel_Thesis

---

# Prefetch

- Harmful prefetch on Intel
	- 2017; Enrique Nissim
	- http://blog.ioactive.com/2017/01/harmful-prefetch-on-intel.html
- PAPP: Prefetcher-Aware Prime and Probe Side-channel Attack
	- Design Automation Conference (DAC) 2019
	- Daimeng Wang, Zhiyun Qian, Nael Abu-Ghazaleh, Srikanth V. Krishnamurthy
	- http://www.cs.ucr.edu/~zhiyunq/pub/dac19_cpu_preferter.pdf
- Prefetch Side-Channel Attacks: Bypassing SMAP and Kernel ASLR
	- Conference on Computer and Communications Security (CCS) 2016
	- Daniel Gruss, Anders Fogh, Clémentine Maurice, Moritz Lipp, Stefan Mangard
	- https://gruss.cc/files/prefetch.pdf
	- https://www.youtube.com/watch?v=TJTQbs3oJx8
- Reverse Engineering the Stream Prefetcher for Profit
	- SILM 2020 Workshop on Software/Hardware Security @ Euro S&P 2020
	- Aditya Rohan, Biswabandan Panda, Prakhar Agarwal
	- https://www.cse.iitk.ac.in/users/biswap/streamer.pdf
- Unveiling Hardware-based Data Prefetcher, a Hidden Source of Information Leakage
	- Computer and Communications Security (CCS) 2018
	- Youngjoo Shin, Hyung Chan Kim, Dokeun Kwon, Ji Hoon Jeong, Junbeom Hur
	- https://dl.acm.org/citation.cfm?doid=3243734.3243736
	- https://ccs.korea.ac.kr/board/bbs/board.php?bo_table=cssa_news&wr_id=61
- Using Undocumented CPU Behavior to See Into Kernel Mode and Break KASLR in the Process
	- BlackHat USA 2016
	- Anders Fogh & Daniel Gruss
	- https://www.youtube.com/watch?v=Pwq0vv4X7m4
	- https://www.blackhat.com/docs/us-16/materials/us-16-Fogh-Using-Undocumented-CPU-Behaviour-To-See-Into-Kernel-Mode-And-Break-KASLR-In-The-Process.pdf

## Prefetch: 2022

- AMD Prefetch Attacks through Power and Time
	- USENIX Security 2022
	- Moritz Lipp, Daniel Gruss, Michael Schwarz
	- https://mlq.me/download/amdprefetch.pdf
	- https://github.com/amdprefetch/amd-prefetch-attacks
- Augury: Using Data Memory-Dependent Prefetchers to Leak Data at Rest
	- IEEE Symposium on Security and Privacy (S&P) 2022
	- Jose Rodrigo Sanchez Vicarte, Michael Flanders, Riccardo Paccagnella, Grant Garrett-Grossman, Adam Morrison, Christopher W. Fletcher, David Kohlbrenner
	- https://www.prefetchers.info/
	- https://github.com/FPSG-UIUC/augury
	- https://doi.ieeecomputersociety.org/10.1109/SP46214.2022.00089

---

# Pseudo-Random Number Generator (PRNG)

- Covert Channels through Random Number Generator: Mechanisms, Capacity Estimation and Mitigations
	- CCS 2016
	- Dmitry Evtyushkin, Dmitry V. Ponomarev
	- http://www.cs.binghamton.edu/~dima/ccs16.pdf
	- https://www.youtube.com/watch?v=G1xzG43mkZU

---

# Reorder Buffer (ROB)

- "It's a Trap!"-How Speculation Invariance Can Be Abused with Forward Speculative Interference
	- IEEE International Symposium On Secure And Private Execution Enviroment Design (SEED) 2021
	- Pavlos Aimoniotis, Christos Sakalis, Magnus Själander, Stefanos Kaxiras
	- https://arxiv.org/abs/2109.10774
- Reorder Buffer Contention: A Forward Speculative Interference Attack for Speculation Invariant Instructions
	- IEEE Computer Architecture Letters 20(2) 2021
	- Pavlos Aimoniotis, Christos Sakalis, Magnus Själander, Stefanos Kaxiras
	- https://doi.ieeecomputersociety.org/10.1109/LCA.2021.3123408
	- https://www.computer.org/csdl/journal/ca/5555/01/09591413/1y2Fj3E6wSY

---

# Return Stack Buffer (RSB)

- CPU side-channels vs. virtualization rootkits: the good, the bad, or the ugly
	- ToorCon Seattle 2008; Yuriy Bulygin
	- http://www.c7zero.info/stuff/hyper-channel_toorcon_seattle.ppt
	- Detecting virtualization using CPU Return Stack Buffer - https://youtube.com/watch?v=UN8iXdMZP2s
- Reinforcing Meltdown Attack by Using a Return Stack Buffer
	- IEEE Access, Volume 7, 2019
	- Taehyun Kim, Young-joo Shin
	- https://ieeexplore.ieee.org/abstract/document/8937554
- ret2spec: Speculative Execution Using Return Stack Buffers
	- ACM CCS 2018
	- Giorgi Maisuradze, Christian Rossow
	- https://christian-rossow.de/publications/ret2spec-ccs2018.pdf
	- https://www.youtube.com/watch?v=c0iIifQSC80
- Spectre Returns! Speculation Attacks using the Return Stack Buffer
	- USENIX Workshop on Offensive Technologies (WOOT) 2018
	- Esmaeil Mohammadian Koruyeh, Khaled N. Khasawneh, Chengyu Song, Nael Abu-Ghazaleh
	- https://arxiv.org/abs/1807.07940
	- https://www.usenix.org/conference/woot18/presentation/koruyeh
- Spring: Spectre Returning in the Browser with Speculative Load Queuing and Deep Stacks
	- Workshop On Offensive Technologies (WOOT) 2022
	- Johannes Wikner, Cristiano Giuffrida, Herbert Bos, Kaveh Razavi
	- https://comsec.ethz.ch/research/microarch/spring/
	- https://comsec.ethz.ch/wp-content/files/spring_woot22.pdf

---

# Scheduler

- SQUIP: Exploiting the Scheduler Queue Contention Side Channel
	- IEEE S&P 2023
	- Stefan Gast, Jonas Juffinger, Martin Schwarzl, Gururaj Saileshwar, Andreas Kogler, Simone Franza, Markus Köstl, Daniel Gruss
	- https://stefangast.eu/papers/squip.pdf

---

# SMT

## SMT: 2022

- HyperDegrade: From GHz to MHz Effective CPU Frequencies
	- USENIX Security 2022
	- Alejandro Cabrera Aldaya, Billy Bob Brumley
	- https://www.usenix.org/conference/usenixsecurity22/presentation/aldaya
- Port Contention Goes Portable: Port Contention Side Channels in Web Browsers
	- AsiaCCS 2022
	- Thomas Rokicki, Clémentine Maurice, Marina Botvinnik, Yossi Oren
	- https://doi.org/10.1145/3488932.3517411
	- https://people.irisa.fr/Thomas.Rokicki/publications/wpc.pdf
	- https://github.com/MIAOUS-group/web-port-contention

## SMT: 2020

- ABSynthe: Automatic Blackbox Side-channel Synthesis on Commodity Microarchitectures
	- Network and Distributed Systems Security (NDSS) Symposium 2020
	- Ben Gras, Cristiano Giuffrida, Michael Kurth, Herbert Bos, Kaveh Razavi
	- https://download.vusec.net/papers/absynthe_ndss20.pdf

## SMT: 2019

- SMoTherSpectre: exploiting speculative execution through port contention
	- CCS 2019
	- Atri Bhattacharyya, Alexandra Sandulescu, Matthias Neugschwandtner, Alessandro Sorniotti, Babak Falsafi, Mathias Payer, Anil Kurmus
	- https://arxiv.org/abs/1903.01843
	- http://nebelwelt.net/blog/20190306-SMoTherSpectre.html
	- https://github.com/HexHive/SMoTherSpectre

## SMT: 2005-2018

- Cache missing for fun and profit
	- BSDCan 2005; Colin Percival
	- http://www.daemonology.net/papers/cachemissing.pdf
- Cheap Hardware Parallelism Implies Cheap Security
	- Fault Diagnosis and Tolerance in Cryptography (FDTC) 2007
	- Onur Acıçmez, Jean-Pierre Seifert
	- http://conferenze.dei.polimi.it/FDTC07/Aciicmez.pdf
- Covert Shotgun: Automatically finding covert channels in SMT
	- 2016; Anders Fogh
	- https://cyber.wtf/2016/09/27/covert-shotgun/
- Port Contention for Fun and Profit
	- Cryptology ePrint Archive, Paper 2018/1060
	- Security & Privacy (S&P) 2019
	- Alejandro Cabrera Aldaya, Billy Bob Brumley, Sohaib ul Hassan, Cesar Pereida García, Nicola Tuveri
	- https://eprint.iacr.org/2018/1060
	- PortSmash (CVE-2018-5407): side-channel vulnerability on SMT/Hyper-Threading architectures
		- https://github.com/bbbrumley/portsmash

---

# Speculation

Transient execution attacks  
Classification tree - http://transient.fail/  
Proof-of-Concept Repository - https://github.com/IAIK/transientfail/

Refined Speculative Execution Terminology  
https://software.intel.com/security-software-guidance/insights/refined-speculative-execution-terminology

- Bypassing KPTI Using the Speculative Behavior of the SWAPGS Instruction
	- Andrei Vlad Luțaș, Dan Horea Luțaș
	- https://labs.bitdefender.com/2019/08/bypassing-kpti-using-the-speculative-behavior-of-the-swapgs-instruction/
	- https://businessresources.bitdefender.com/bypassing-kpti-speculative-behavior-swapgs-instruction
	- Black Hat 2019
		- https://www.youtube.com/watch?v=XUwZUdOHT1c
		- https://www.blackhat.com/eu-19/briefings/schedule/#bypassing-kpti-using-the-speculative-behavior-of-the-swapgs-instruction-18045
- Code That Never Ran: Modeling Attacks on Speculative Evaluation
	- IEEE Symposium on Security & Privacy 2019
	- Disselkoen, C., Jagadeesan, R., Jeffrey, A., Riely, J.
	- https://cseweb.ucsd.edu/~cdisselk/papers/code-that-never-ran.pdf
	- https://github.com/chicago-relaxed-memory/spec-eval
- Covert and Side Channels due to Processor Architecture
	- Annual Computer Security Applications Conference ACSAC 2006
	- Zhenghong Wang, Ruby B. Lee
	- http://ieeexplore.ieee.org/document/4041191/
	- http://www.acsac.org/2006/papers/127.pdf
- ExSpectre: Hiding Malware in Speculative Execution
	- Network and Distributed Systems Security (NDSS) 2019
	- Jack Wampler, Ian Martiny, Eric Wustrow
	- https://www.ndss-symposium.org/wp-content/uploads/2019/02/ndss2019_02B-5_Wampler_paper.pdf
- Foreshadow & L1 Terminal Fault (L1TF)
	- Foreshadow: Breaking the Virtual Memory Abstraction with Transient Out-of-Order Execution
		- USENIX Security 2018
		- Jo Van Bulck, Frank Piessens, Raoul Strackx; Marina Minkin, Mark Silberstein, Ofir Weisse, Daniel Genkin, Baris Kasikci, Thomas F. Wenisch, Yuval Yarom
		- https://www.usenix.org/conference/usenixsecurity18/presentation/bulck
		- https://foreshadowattack.eu/
	- A deeper look at L1 Terminal Fault aka Foreshadow - https://www.redhat.com/en/blog/deeper-look-l1-terminal-fault-aka-foreshadow
	- Analysis and mitigation of L1 Terminal Fault (L1TF) - https://blogs.technet.microsoft.com/srd/2018/08/14/analysis-and-mitigation-of-l1-terminal-fault-l1tf/
	- Breaking Virtual Memory Protection and the SGX Ecosystem with Foreshadow
		- IEEE Micro 39(3) 2019
		- Jo Van Bulck, Marina Minkin, Ofir Weisse, Daniel Genkin, Baris Kasikci, Frank Piessens, Mark Silberstein, Thomas F. Wenisch, Yuval Yarom, Raoul Strackx
		- https://doi.org/10.1109/MM.2019.2910104
	- L1 Terminal Fault Vulnerability - https://www.cyberus-technology.de/posts/2018-08-14-l1-terminal-fault.html
	- Hyper-V HyperClear Mitigation for L1 Terminal Fault - https://blogs.technet.microsoft.com/virtualization/2018/08/14/hyper-v-hyperclear/
- Load Value Injection
	- CVE-2020-0551 / INTEL-SA-00334
	- LVI: Hijacking Transient Execution through Microarchitectural Load Value Injection
		- IEEE Symposium on Security and Privacy (S&P) 2020
		- Jo Van Bulck, Daniel Moghimi, Michael Schwarz, Moritz Lipp, Marina Minkin, Daniel Genkin, Yuval Yarom, Berk Sunar, Daniel Gruss, Frank Piessens
			- https://lviattack.eu/
	- https://software.intel.com/security-software-guidance/software-guidance/load-value-injection
	- https://software.intel.com/security-software-guidance/insights/deep-dive-load-value-injection
	- https://software.intel.com/security-software-guidance/insights/optimized-mitigation-approach-load-value-injection
	- [llvm-dev] Load Value Injection (LVI) Mitigation for X86
		- https://lists.llvm.org/pipermail/llvm-dev/2020-March/139842.html
	- [llvm-dev] [RFC] Speculative Execution Side Effect Suppression for Mitigating Load Value Injection
		- https://lists.llvm.org/pipermail/llvm-dev/2020-March/139843.html
- Meltdown & Spectre
	- Meltdown - https://meltdownattack.com/
		- USENIX Security 2018
		- Moritz Lipp, Michael Schwarz, Daniel Gruss, Thomas Prescher, Werner Haas, Stefan Mangard, Paul Kocher, Daniel Genkin, Yuval Yarom, Mike Hamburg
		- https://meltdownattack.com/meltdown.pdf
		- https://arxiv.org/abs/1801.01207
		- Meltdown Proof-of-Concept - https://github.com/IAIK/meltdown
		- http://blog.cyberus-technology.de/posts/2018-01-03-meltdown.html
		- Black Hat USA 2018 - https://mlq.me/download/bhusa2018_meltdown_slides.pdf
		- KASLR: Break It, Fix It, Repeat
			- ACM Asia Conference on Computer and Communications Security (ASIA CCS) 2020
			- Claudio Canella, Michael Schwarz, Martin Haubenwallner, Martin Schwarzl, Daniel Gruss
			- https://doi.org/10.1145/3320269.3384747
			- http://cc0x1f.net/publications/kaslr.pdf
			- FLARE (Fake Load Address REsponse) - https://github.com/IAIK/FLARE
	- Spectre Attacks: Exploiting Speculative Execution - https://spectreattack.com/
		- S&P 2019
		- Paul Kocher, Daniel Genkin, Daniel Gruss, Werner Haas, Mike Hamburg, Moritz Lipp, Stefan Mangard, Thomas Prescher, Michael Schwarz, Yuval Yarom
		- https://spectreattack.com/spectre.pdf
		- https://arxiv.org/abs/1801.01203
	- Reading privileged memory with a side-channel - Jann Horn
		- https://googleprojectzero.blogspot.com/2018/01/reading-privileged-memory-with-side.html
		- Google Project Zero PoC: https://bugs.chromium.org/p/project-zero/issues/detail?id=1272
	- Spectre and Meltdown: Data leaks during speculative execution - Real World Crypto 2018, Jann Horn (Google Project Zero)
		- https://www.youtube.com/watch?v=6O8LTwVfTVs
	- Paul Kocher: Spectre Mitigations in Microsoft's C/C++ Compiler
		- https://www.paulkocher.com/doc/MicrosoftCompilerSpectreMitigation.html
	- ARM Whitepaper "Cache Speculation Side-channels" - https://developer.arm.com/support/security-update/download-the-whitepaper
	- Behind the scenes of a bug collision - https://cyber.wtf/2018/01/05/behind-the-scene-of-a-bug-collision/
	- CPU security bugs caused by speculative execution - https://github.com/marcan/speculation-bugs
	- Intel Analysis of Speculative Execution Side Channels - https://newsroom.intel.com/wp-content/uploads/sites/11/2018/01/Intel-Analysis-of-Speculative-Execution-Side-Channels.pdf
	- meltdownspectre-patches: summary of the patch status - https://github.com/hannob/meltdownspectre-patches
	- Mitigating Spectre variant 2 with Retpoline on Windows - https://techcommunity.microsoft.com/t5/Windows-Kernel-Internals/Mitigating-Spectre-variant-2-with-Retpoline-on-Windows/ba-p/295618
	- More details about mitigations for the CPU Speculative Execution issue - https://security.googleblog.com/2018/01/more-details-about-mitigations-for-cpu_4.html
	- Retpoline: a software construct for preventing branch-target-injection - https://support.google.com/faqs/answer/7625886
	- How Performance Optimizations Shatter Security Boundaries
		- QCon London 2018; Moritz Lipp
		- https://www.infoq.com/presentations/spectre-meltdown-security
	- The Microarchitecture Behind Meltdown - http://blog.stuffedcow.net/2018/05/meltdown-microarchitecture/
- Microarchitectural Data Sampling (MDS)
	- CVE-2018-12126 - Microarchitectural Store Buffer Data Sampling (MSBDS) - Fallout
	- CVE-2018-12127 - Microarchitectural Load Port Data Sampling (MLPDS) - RIDL
	- Meltdown-MCA (microcode assists) - Zombieload
	- Meltdown-US-LFB (line fill buffer) - CVE-2018-12130 - Microarchitectural Fill Buffer Data Sampling (MFBDS) - RIDL, ZombieLoad Variant 1
	- Meltdown-P-LFB - CVE-2019-11091 - Microarchitectural Data Sampling Uncacheable Memory (MDSUM) - RIDL
	- Meltdown-MCA-AD (accessed or dirty bit) - ZombieLoad Variant 3
	- https://cpu.fail/
	- https://mdsattacks.com/
	- https://zombieloadattack.com/
	- Fallout: Reading Kernel Writes From User Space
		- 2019 arXiv
		- Marina Minkin, Daniel Moghimi, Moritz Lipp, Michael Schwarz, Jo Van Bulck, Daniel Genkin, Daniel Gruss, Frank Piessens, Berk Sunar, Yuval Yarom
		- https://arxiv.org/abs/1905.12701
	- Medusa: Microarchitectural Data Leakage via Automated Attack Synthesis
		- USENIX Security 2020
		- Daniel Moghimi, Moritz Lipp, Berk Sunar, Michael Schwarz
		- https://moghimi.org/papers/usenixsec20-Medusa.pdf
		- https://www.usenix.org/conference/usenixsecurity20/presentation/moghimi-medusa
		- Transynther: Fuzz Testing Meltdown-style attacks
			- https://github.com/VernamLab/medusa/tree/master/Transynther
		- Data Sampling on MDS-resistant 10th Generation Intel Core (Ice Lake)
			- 2020
			- Daniel Moghimi
			- https://moghimi.org/papers/techreport2020-IceLakeMDS.pdf
			- https://github.com/danielmgmi/IceBreak
	- RIDL: Rogue In-Flight Data Load
		- IEEE Symposium on Security and Privacy (S&P) 2019
		- Stephan van Schaik, Alyssa Milburn, Sebastian Österlund, Pietro Frigo, Giorgi Maisuradze, Kaveh Razavi, Herbert Bos, and Cristiano Giuffrida
		- https://mdsattacks.com/files/ridl.pdf
		- Addendum 1: TSX Asynchronous Abort (TAA)
			- https://mdsattacks.com/#ridl-ng
		- Addendum 2: L1D Eviction Sampling (L1DES), Vector Register Sampling (VRS)
			- https://mdsattacks.com/#ridl-nng
		- RIDL: Rogue In Flight Data Load
			- HITB+ CyberWeek 2019; Stephan van Schaik, Sebastian Osterlund
			- https://www.youtube.com/watch?v=vJfXu9Q_DmI
		- Escaping the Chrome Sandbox with RIDL
			- https://googleprojectzero.blogspot.com/2020/02/escaping-chrome-sandbox-with-ridl.html
		- CrossTalk: Speculative Data Leaks Across Cores Are Real
			- IEEE Symposium on Security & Privacy (S&P) 2021
			- Ragab, H.; Milburn, A.; Razavi, K.; Bos, H.; Giuffrida, C.
			- https://www.vusec.net/projects/crosstalk/
			- https://github.com/vusec/ridl
			- Special Register Buffer Data Sampling - https://software.intel.com/security-software-guidance/insights/deep-dive-special-register-buffer-data-sampling
			- SRBDS (CVE-2020-0543) - https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-0543
	- ZombieLoad: Cross-Privilege-Boundary Data Sampling
		- Computer and Communications Security (CCS) 2019
		- Michael Schwarz, Moritz Lipp, Daniel Moghimi, Jo Van Bulck, Julian Stecklina, Thomas Prescher, Daniel Gruss
		- https://arxiv.org/abs/1905.05726
		- ZombieLoad Attack: Leaking Your Recent Memory Operations on Intel CPUs
			- 36C3 (2019); Michael Schwarz, Moritz Lipp, Daniel Gruss
			- https://media.ccc.de/v/36c3-10754-zombieload_attack
		- ZombieLoad: Leaking Data on Intel CPUs
			- ToorCon 21 (2019); Daniel Moghimi
			- https://www.youtube.com/watch?v=M0W92rEJziI
			- https://talks.toorcon.net/toorcon21/talk/CVYNXS/
	- Additional readings:
		- https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling
		- https://access.redhat.com/security/vulnerabilities/mds
		- https://www.redhat.com/en/blog/understanding-mds-vulnerability-what-it-why-it-works-and-how-mitigate-it
		- https://www.cyberus-technology.de/posts/2019-05-14-zombieload.html
		- Intel Security Advisory for MDS - https://www.intel.com/content/www/us/en/security-center/advisory/intel-sa-00233.html
		- Deep dive: Intel Analysis of Microarchitectural Data Sampling - https://software.intel.com/security-software-guidance/insights/deep-dive-intel-analysis-microarchitectural-data-sampling
		- Microarchitectural Data Sampling vulnerabilities/mitigations - https://software.intel.com/security-software-guidance/software-guidance/microarchitectural-data-sampling
		- https://www.intel.com/content/www/us/en/architecture-and-technology/mds.html
		- https://www.kernel.org/doc/html/latest/x86/mds.html
		- https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/mds.html
		- CPU Introspection: Intel Load Port Snooping
			- https://gamozolabs.github.io/metrology/2019/12/30/load-port-monitor.html
- NetSpectre: Read Arbitrary Memory over Network
	- arXiv 2018; Michael Schwarz, Martin Schwarzl, Moritz Lipp, Daniel Gruss
	- https://misc0110.net/web/files/netspectre.pdf
- On the Spectre and Meltdown Processor Security Vulnerabilities
	- IEEE Micro Special Issue on Hot Chips 2018 (2019)
	- Mark D. Hill, Jon Masters, Parthasarathy Ranganathan, Paul Turner, John Hennessy
	- https://doi.org/10.1109/MM.2019.2897677
	- https://ieeexplore.ieee.org/document/8634886
	- http://www.cs.wisc.edu/~markhill/papers/ieeemicro19_spectre_meltdown_2019_01_30
- Out-of-Order Execution and Its Applications
	- DeepSec 2017; Sophia D'Antoine
	- https://www.sophia.re/ROOTS/
	- https://deepsec.net/docs/Slides/2017/Out-Of-Order_Execution_and_its_applications_Sophia_dAntoine.pdf
	- https://deepsec.net/docs/Slides/2017/Out-Of-Order_Execution_and_its_applications_Sophia_dAntoine.pptx
- Speculative Buffer Overflows: Attacks and Defenses
	- CVE-2018-3693: Bounds Check Bypass Store (BCBS)
	- Vladimir Kiriansky, Carl Waldspurger
	- https://people.csail.mit.edu/vlk/spectre11.pdf
	- https://arxiv.org/abs/1807.03757
- Speculator: Tool to Analyze Speculative Execution Attacks and Mitigations
	- ACSAC 2019
	- Andrea Mambretti, Matthias Neugschwandtner, Alessandro Sorniotti, Engin Kirda, William Robertson, Anil Kurmus
	- https://github.com/ibm-research/speculator
	- https://andreamambretti.com/files/papers/acsac2019_speculator.pdf
	- https://dl.acm.org/citation.cfm?id=3359837
	- Let’s Not Speculate: Discovering and Analyzing Speculative Execution Attacks
		- 2018 IBM Technical Report RZ3933
		- https://domino.research.ibm.com/library/cyberdig.nsf/1e4115aea78b6e7c85256b360066f0d4/d66e56756964d8998525835200494b74
- Speculose: Analyzing the Security Implications of Speculative Execution in CPUs
	- arXiv 2018
	- Giorgi Maisuradze, Christian Rossow
	- https://arxiv.org/abs/1801.04084
- Two methods for exploiting speculative control flow hijacks.
	- WOOT @ USENIX Security Symposium 2019
	- Andrea Mambretti, Alexandra Sandulescu, Matthias Neugschwandtner, Alessandro Sorniotti, Anil Kurmus
	- http://ale.sopit.net/pdf/woot.pdf

## Speculation: 2022

- Revizor: Testing Black-box CPUs against Speculation Contracts
	- Architectural Support for Programming Languages and Operating Systems (ASPLOS) 2022
	- Oleksii Oleksenko, Christof Fetzer, Boris Köpf, Mark Silberstein
	- https://arxiv.org/abs/2105.06872
	- Revizor: a microarchitectural fuzzer
		- https://github.com/hw-sw-contracts/revizor
		- https://github.com/microsoft/sca-fuzzer

## Speculation: 2021

- Bypassing memory safety mechanisms through speculative control flow hijacks
	- IEEE EuroS&P 2021
	- Andrea Mambretti, Alexandra Sandulescu, Alessandro Sorniotti, William Robertson, Engin Kirda, Anil Kurmus
	- https://arxiv.org/abs/2003.05503
- Rage Against the Machine Clear: A Systematic Analysis of Machine Clears and Their Implications for Transient Execution Attacks
	- USENIX Security Symposium 2021
	- Hany Ragab, Enrico Barberis, Herbert Bos, Cristiano Giuffrida
	- https://download.vusec.net/papers/fpvi-scsb_sec21.pdf
	- https://github.com/vusec/fpvi-scsb
	- https://www.vusec.net/projects/fpvi-scsb/
	- Floating Point Value Injection (FPVI): CVE-2021-0086
	- Speculative Code Store Bypass (SCSB): CVE-2021-0089
- Reproducing Spectre Attack with gem5, How To Do It Right?
	- EuroSec 2021
	- Pierre Ayoub, Clémentine Maurice
	- https://hal.inria.fr/hal-03215326/
	- https://cmaurice.fr/pdf/eurosec21_ayoub.pdf
	- https://pierreay.github.io/reproduce-spectre-gem5/
- Speculative Interference Attacks: Breaking Invisible Speculation Schemes
	- Architectural Support for Programming Languages and Operating Systems (ASPLOS) 2021
	- Mohammad Behnia, Prateek Sahu, Riccardo Paccagnella, Jiyong Yu, Zirui Zhao, Xiang Zou, Thomas Unterluggauer, Josep Torrellas, Carlos Rozas, Adam Morrison, Frank Mckeen, Fangfei Liu, Ron Gabor, Christopher W. Fletcher, Abhishek Basak, Alaa Alameldeen
	- https://arxiv.org/abs/2007.11818

## Speculation: 2020

- SpecROP: Speculative Exploitation of ROP Chains
	- Research in Attacks, Intrusions and Defenses (RAID) 2020
	- Atri Bhattacharyya, Andrés Sánchez, Esmaeil M. Koruyeh, Nael Abu-Ghazaleh, Chengyu Song, Mathias Payer
	- https://www.usenix.org/conference/raid2020/presentation/bhattacharyya
	- https://github.com/HexHive/specrop/
- Speculative Dereferencing of Registers: Reviving Foreshadow
	- 2020; Financial Cryptography and Data Security 2021
	- Martin Schwarzl, Thomas Schuster, Michael Schwarz, Daniel Gruss
	- https://arxiv.org/abs/2008.02307
	- Extended Version (2021): https://martinschwarzl.at/media/files/spec_deref_extended.pdf
- Speculative Probing: Hacking Blind in the Spectre Era
	- ACM Conference on Computer and Communications Security (CCS) 2020
	- Enes Göktaş, Kaveh Razavi, Georgios Portokalidis, Herbert Bos, Cristiano Giuffrida
	- https://www.vusec.net/projects/blindside/
- SpeechMiner: A Framework for Investigating and Measuring Speculative Execution Vulnerabilities
	- NDSS 2020
	- Yuan Xiao, Yinqian Zhang, Radu Teodorescu
	- https://arxiv.org/abs/1912.00329
- Survey of Transient Execution Attacks and Their Mitigations
	- Wenjie Xiong, Jakub Szefer
	- 2020
		- https://arxiv.org/abs/2005.13435
	- ACM Computing Surveys 2021 Vol 54(3)
		- https://dl.acm.org/doi/abs/10.1145/3442479
- The Evolution of Transient-Execution Attacks
	- GLSVLSI 2020
	- Claudio Canella, Khaled N. Khasawneh, Daniel Gruss
	- https://gruss.cc/files/transient-attacks.pdf
- Transient-Execution Attacks and Defenses
	- 2020 Habilitation Thesis; Daniel Gruss
	- https://gruss.cc/files/habil.pdf
	- https://gruss.cc/files/habil_part1_only.pdf

---

# Store Buffer

- Fallout: Reading Kernel Writes From User Space
	- 2019 arXiv
	- Marina Minkin, Daniel Moghimi, Moritz Lipp, Michael Schwarz, Jo Van Bulck, Daniel Genkin, Daniel Gruss, Frank Piessens, Berk Sunar, Yuval Yarom
	- https://arxiv.org/abs/1905.12701
	- CVE-2018-12126 - Microarchitectural Store Buffer Data Sampling (MSBDS) - Fallout

---

# Thermal

- On the capacity of thermal covert channels in multicores - https://dl.acm.org/citation.cfm?id=2901322
- Thermal Covert Channels on Multi-core Platforms - https://www.usenix.org/conference/usenixsecurity15/technical-sessions/presentation/masti

---

# Translation Lookaside Buffer (TLB)

- Store-to-Leak Forwarding: Leaking Data on Meltdown-resistant CPUs
	- 2019 arXiv
	- Michael Schwarz, Claudio Canella, Lukas Giner, Daniel Gruss
	- https://arxiv.org/abs/1905.05725
	- Store-to-Leak Forwarding: There and Back Again
		- Black Hat Asia 2020
		- https://www.blackhat.com/asia-20/briefings/schedule/#store-to-leak-forwarding-there-and-back-again-18610
- TagBleed: Breaking KASLR on the Isolated Kernel Address Space Using Tagged TLBs
	- Euro S&P 2020
	- Jakob Koschel, Cristiano Giuffrida, Herbert Bos, Kaveh Razavi
	- https://download.vusec.net/papers/tagbleed_eurosp20.pdf
- TLB Poisoning Attacks on AMD Secure Encrypted Virtualization
	- Annual Computer Security Applications Conference (ACSAC) 2021
	- Mengyuan Li, Yinqian Zhang, Huibo Wang, Kang Li, Yueqiang Cheng
	- https://doi.org/10.1145/3485832.3485876
	- https://yinqian.org/papers/acsac21.pdf
- TLB;DR: Enhancing TLB-based Attacks with TLB Desynchronized Reverse Engineering
	- USENIX Security 2022
	- Andrei Tatar, Daniël Trujillo, Cristiano Giuffrida, Herbert Bos
	- https://download.vusec.net/papers/tlbdr_sec22.pdf
- Translation Leak-aside Buffer: Defeating Cache Side-channel Protections with TLB Attacks
	- Ben Gras, Kaveh Razavi, Herbert Bos, Cristiano Giuffrida
	- https://www.vusec.net/projects/tlbleed/
	- USENIX Security 2018
		- https://www.usenix.org/conference/usenixsecurity18/presentation/gras
	- TLBleed: When Protecting Your CPU Caches Is Not Enough
		- Black Hat 2018
			- https://www.youtube.com/watch?v=ZBq7VMIkgPk
			- https://www.blackhat.com/us-18/briefings/schedule/#tlbleed-when-protecting-your-cpu-caches-is-not-enough-10149
		- Hardwear.io 2018
			- https://www.youtube.com/watch?v=PQzbtrxaYWQ
			- https://media.hardwear.io/tlbleed-when-protecting-your-cpu-caches-is-not-enough/

---

# Trusted Execution Environments (TEEs)

- A Tale of Two Worlds: Assessing the Vulnerability of Enclave Shielding Runtimes
	- Computer and Communications Security (CCS) 2019
	- Jo Van Bulck, David Oswald, Eduard Marin, Abdulla Aldoseri, Flavio D.Garcia, Frank Piessens
	- https://people.cs.kuleuven.be/~jo.vanbulck/ccs19-tale.pdf
	- https://github.com/jovanbulck/0xbadc0de
- How Trusted Execution Environments Fuel Research on Microarchitectural Attacks
	- IEEE Security & Privacy 2020
	- Michael Schwarz, Daniel Gruss
	- https://gruss.cc/files/tee_fuel.pdf

## Arm TrustZone

- Hardware-Backed Heist: Extracting ECDSA Keys from Qualcomm’s TrustZone
	- NCC Group Whitepaper (2019); Keegan Ryan
	- https://www.nccgroup.trust/us/our-research/private-key-extraction-qualcomm-keystore/

## Intel SGX

- A Survey of Published Attacks on Intel SGX
	- 2020
	- Alexander Nilsson, Pegah Nikbakht Bideh, Joakim Brorsson
	- https://arxiv.org/abs/2006.13598
- Cache Attacks on Intel SGX
	- EuroSec 2017
	- Johannes Götzfried, Moritz Eckert, Sebastian Schinzel, Tilo Müller
	- https://www1.informatik.uni-erlangen.de/filepool/projects/sgx-timing/sgx-timing.pdf
- CacheZoom: How SGX Amplifies The Power of Cache Attacks
	- Cryptographic Hardware and Embedded Systems (CHES) 2017
	- Ahmad Moghimi, Gorka Irazoqui, Thomas Eisenbarth
	- https://arxiv.org/abs/1703.06986
- CopyCat: Controlled Instruction-Level Attacks on Enclaves
	- USENIX Security Symposium 2020
	- Daniel Moghimi, Jo Van Bulck, Nadia Heninger, Frank Piessens, Berk Sunar
	- https://arxiv.org/abs/2002.08437
	- https://www.usenix.org/conference/usenixsecurity20/presentation/moghimi-copycat
- Exploitable Hardware Features and Vulnerabilities Enhanced Side-Channel Attacks on Intel SGX and Their Countermeasures
	- 2019 PhD Dissertation; Chen, Guoxing
	- http://rave.ohiolink.edu/etdc/view?acc_num=osu1554949268465917
- Inferring Fine-grained Control Flow Inside SGX Enclaves with Branch Shadowing
	- USENIX Security 2017
	- https://arxiv.org/abs/1611.06952
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/lee-sangho
	- Skylake's BTB parameters, use of Intel PT and LBR
- Leaky Cauldron on the Dark Land: Understanding Memory Side-Channel Hazards in SGX
	- CCS 2017
	- Wenhao Wang, Guoxing Chen, Xiaorui Pan, Yinqian Zhang, XiaoFeng Wang, Vincent Bindschaedler, Haixu Tang, Carl A. Gunter
	- https://yinqian.org/papers/ccs17b.pdf
	- https://acmccs.github.io/papers/p2421-wangA.pdf
- Malware Guard Extension: Using SGX to Conceal Cache Attacks
	- DIMVA 2017
	- Michael Schwarz, Samuel Weiser, Daniel Gruss, Clémentine Maurice, Stefan Mangard
	- https://arxiv.org/abs/1702.08719
- Microarchitectural Side-Channel Attacks for Privileged Software Adversaries
	- 2020 PhD Dissertation
	- Jo Van Bulck
	- https://lirias.kuleuven.be/3047121
	- https://jovanbulck.github.io/files/phd-thesis.pdf
- MicroScope: Enabling Microarchitectural Replay Attacks
	- International Symposium on Computer Architecture (ISCA) 2019
	- Dimitrios Skarlatos, Mengjia Yan, Bhargava Gopireddy, Read Sprabery, Josep Torrellas, Christopher Fletcher
	- http://iacoma.cs.uiuc.edu/iacoma-papers/isca19_3.pdf
	- http://skarlat2.web.engr.illinois.edu/publications/microScope_isca19.pdf
	- https://github.com/dskarlatos/MicroScope
- Off-Limits: Abusing Legacy x86 Memory Segmentation to Spy on Enclaved Execution
	- Engineering Secure Software and Systems (ESSoS) 2018
	- Gyselinck J., Van Bulck J., Piessens F., Strackx R.
	- https://people.cs.kuleuven.be/~jo.vanbulck/essos18.pdf
	- https://distrinet.cs.kuleuven.be/software/off-limits/
- Racing in Hyperspace: Closing Hyper-Threading Side Channels on SGX with Contrived Data Races
	- IEEE S&P (Oakland) 2018
	- Guoxing Chen, Wenhao Wang, Tianyu Chen, Sanchuan Chen, Yinqian Zhang, XiaoFeng Wang, Ten-Hwang Lai, Dongdai Lin
	- https://yinqian.org/papers/sp18a.pdf
	- https://csdl.computer.org/csdl/proceedings/sp/2018/4353/00/435301a388.pdf
- Security Vulnerabilities of SGX and Countermeasures: A Survey
	- ACM Computing Surveys 54(6) 2021
	- Shufan Fei, Zheng Yan, Wenxiu Ding, Haomeng Xie
	- https://doi.org/10.1145/3456631
- SGX-Step: A Practical Attack Framework for Precise Enclave Execution Control
	- SysTEX 2017
	- Jo Van Bulck, Frank Piessens, Raoul Strackx
	- https://github.com/jovanbulck/sgx-step
- SGAxe: How SGX Fails in Practice
	- 2020
	- Stephan van Schaik, Andrew Kwong, Daniel Genkin, Yuval Yarom
	- https://sgaxe.com/
	- https://cacheoutattack.com/files/SGAxe.pdf
- SGXlinger: A New Side-Channel Attack Vector Based on Interrupt Latency Against Enclave Execution
	- International Conference on Computer Design (ICCD) 2018
	- Wenjian He, Wei Zhang, Sanjeev Das, Yang Liu
	- https://github.com/HE-Wenjian/SGXlinger
- SgxPectre Attacks: Leaking Enclave Secrets via Speculative Execution
	- 2018 arXiv; 2019 IEEE European Symposium on Security and Privacy (EuroS&P)
	- Guoxing Chen, Sanchuan Chen, Yuan Xiao, Yinqian Zhang, Zhiqiang Lin, Ten H. Lai
	- https://arxiv.org/abs/1802.09085
	- https://github.com/osusecLab/SgxPectre
- Side-Channel Attacks on Intel SGX: How SGX Amplifies The Power of Cache Attacks
	- 2017 Master's Thesis
	- Ahmad Moghimi
	- https://digitalcommons.wpi.edu/etd-theses/399
- TSX-based Defenses Against SGX Side-channel Attacks - https://gts3.org/2018/tsgx-defense.html
- Tutorial: Uncovering and mitigating side-channel leakage in Intel SGX enclaves
	- Security, Privacy, and Applied Cryptography Engineering (SPACE) 2018
	- Jo Van Bulck, Frank Piessens
	- https://github.com/jovanbulck/sgx-tutorial-space18
	- https://people.cs.kuleuven.be/~jo.vanbulck/space18.pdf
- Varys: Protecting SGX Enclaves from Practical Side-Channel Attacks
	- USENIX ATC 2018
	- Oleksii Oleksenko, Bohdan Trach, Robert Krahn, Mark Silberstein, Christof Fetzer
	- https://www.usenix.org/conference/atc18/presentation/oleksenko

### Intel SGX: Defense

- Defeating Speculative-Execution Attacks on SGX with HyperRace
	- IEEE Conference on Dependable and Secure Computing 2019
	- Guoxing Chen, Mengyuan Li, Fengwei Zhang, Yinqian Zhang
	- https://yinqian.org/papers/idsc19.pdf
- Repurposing Segmentation as a Practical LVI-NULL Mitigation in SGX
	- USENIX 2022
	- Lukas Giner, Andreas Kogler, Claudio Canella, Michael Schwarz, Daniel Gruss
	- https://ginerlukas.com/publications/papers/lvinull.pdf
	- https://github.com/redrabbyte/LVI-NULLify

## RISC-V Physical Memory Protection (PMP)

- Bypassing Isolated Execution on RISC-V using Side-Channel-Assisted Fault-Injection and Its Countermeasure
	- IACR Transactions on Cryptographic Hardware and Embedded Systems, 2022(1)
	- Shoei Nashimoto, Daisuke Suzuki, Rei Ueno, Naofumi Homma
	- https://tches.iacr.org/index.php/TCHES/article/view/9289
	- https://doi.org/10.46586/tches.v2022.i1.28-68

---

# TSX

- Breaking Kernel Address Space Layout Randomization with Intel TSX
	- Computer and Communications Security (CCS 2016)
	- Yeongjin Jang, Sangho Lee, Taesoo Kim
	- https://www.microsoft.com/en-us/research/publication/breaking-kernel-address-space-layout-randomization-with-intel-tsx/
	- https://sslab.gtisc.gatech.edu/assets/papers/2016/jang:drk-ccs.pdf
	- https://gts3.org/assets/papers/2016/jang:drk-ccs.pdf
	- https://github.com/sslab-gatech/DrK
	- decoded icache (caches decoded micro-ops) - inside L1 icache, virtually-indexed and virtually tagged (VIVT), does not require an iTLB access for address translation
- Meltdown-MCA-TAA
	- Meltdown-MCA-TAA (microcode assist caused by transactional asynchronous abort) - [ZombieLoad](https://zombieloadattack.com/) Variant 2
	- CVE-2019-11135 - Transactional Synchronization Extensions (TSX) Asynchronous Abort (TAA)
	- https://mdsattacks.com/files/ridl-addendum.pdf
	- https://software.intel.com/security-software-guidance/software-guidance/intel-transactional-synchronization-extensions-intel-tsx-asynchronous-abort
	- https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/tsx_async_abort.html
	- https://access.redhat.com/solutions/tsx-asynchronousabort
- Prime+Abort: A Timer-Free High-Precision L3 Cache Attack using Intel TSX
	- USENIX Security 2017
	- Craig Disselkoen, David Kohlbrenner, Leo Porter, Dean Tullsen
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/disselkoen

---

# Talks

## Talks: 2022

- Tutorial: Microarchitectural Side Channel Attacks
	- International Solid-State Circuits Conference (ISSCC) 2022
	- Todd Austin
	- https://www.youtube.com/watch?v=dLkyuUrAuzg

## Talks: 2021

- A Practical Introduction to Transient Execution Attacks
	- European Symposium on Research in Computer Security (ESORICS) 2021
	- Michael Schwarz
	- https://www.youtube.com/watch?v=xteiXOpEjXs
	- https://esorics2021.athene-center.de/tutorial-07-28.php

## Talks: 2020

- Cryptographic Software in a Post-Spectre World
	- Real World Crypto 2020; Chandler Carruth
	- https://chandlerc.blog/talks/2020_post_spectre_crypto/post_spectre_crypto.html
- Improving protections against speculative execution side channel
	- FOSDEM 2020; David Stewart
	- https://fosdem.org/2020/schedule/event/speculative_execution/
- Principled Secure Processor Design
	- [UW-Madison Virtual Computer Architecture Seminar for Fall 2020](http://pages.cs.wisc.edu/~markhill/includes/seminar2020.html)
	- Chris Fletcher (Illinois)
	- https://www.youtube.com/watch?v=2lTkNk3HZ-c
	- http://pages.cs.wisc.edu/~markhill/seminar2020/fletcher2020_09_principled_secure_processor_design.pdf

## Talks: 2019

- AcuTherm: A Hybrid Attack on Password Entry Based on Both Acoustic and Thermal Side-Channels
	- Black Hat Asia 2019
	- Ercan Ozturk, Gene Tsudik, Tyler Kaczmarek, Pier Paolo Tricomi
	- https://www.blackhat.com/asia-19/briefings/schedule/#acutherm-a-hybrid-attack-on-password-entry-based-on-both-acoustic-and-thermal-side-channels-13927
- Are Microarchitectural Attacks still possible on Flawless Hardware?
	- RuhrSec 2019
	- Erik Kraft & Michael Schwarz
	- https://www.youtube.com/watch?v=t9qOTIFO7Uw
- Broad-Based Side-Channel Defenses for Modern Processor Architectures
	- Ashay Rane
	- Microsoft Research; February 25, 2019
	- https://www.microsoft.com/en-us/research/video/broad-based-side-channel-defenses-for-modern-processor-architectures/
- Ghosts in a Nutshell
	- Black Hat Asia 2019
	- Claudio Canella, Moritz Lipp
	- https://www.blackhat.com/asia-19/briefings/schedule/#ghosts-in-a-nutshell-13755
- Hardware Is the New Software: Finding Exploitable Bugs in Hardware Designs
	- 2019 USENIX Enigma Conference; Cynthia Sturton
	- https://www.usenix.org/conference/enigma2019/presentation/sturton
- NetSpectre: A Truly Remote Spectre Variant
	- Black Hat Asia 2019
	- Michael Schwarz, Martin Schwarzl
	- https://www.blackhat.com/asia-19/briefings/schedule/#netspectre-a-truly-remote-spectre-variant-13757
	- https://misc0110.net/web/files/netspectre_blackhat_slides.pdf
- Oh No! KPTI Defeated, Unauthorized Data Leakage is Still Possible
	- Black Hat Asia 2019
	- Yueqiang Cheng, Zhaofeng Chen, Yulong Zhang, Yu Ding, Tao Wei
	- https://www.blackhat.com/asia-19/briefings/schedule/index.html#oh-no-kpti-defeated-unauthorized-data-leakage-is-still-possible-13945
- Spectre/C++: Preventing Spectre One Branch at a Time: The Design and Implementation of Fine Grained Spectre v1 Mitigation APIs
	- CppCon 2019; Zola Bridges, Devin Jeanpierre
	- https://www.youtube.com/watch?v=ehNkhmEg0bw
- Speculation & leakage: Timing side channels & multi-tenant computing
	- AWS re:Invent 2019; Eric Brandwine
	- https://www.youtube.com/watch?v=kQ4H6XO-iao
	- https://www.portal.reinvent.awsevents.com/connect/sessionDetail.ww?SESSION_ID=99692
- What Spectre Means for Language Implementers
	- Programming Language Implementation Summer School (PLISS) 2019
	- Ben Titzer
	- https://www.youtube.com/watch?v=FGX-KD5Nh2g
	- https://pliss2019.github.io/ben_titzer_spectre_slides.pdf
- Winter is Coming Back: Defeating the Most Advanced Rowhammer Defenses to Gain Root and Kernel Privileges
	- Black Hat Asia 2019
	- Yueqiang Cheng, Zhi Zhang, Surya Nepal, Zhi Wang
	- https://www.blackhat.com/asia-19/briefings/schedule/#winter-is-coming-back-defeating-the-most-advanced-rowhammer-defenses-to-gain-root-and-kernel-privileges-13524
- Writing PoCs for processor software side-channels
	- ToorCon 21 (2019); Volodymyr Pikhur
	- https://www.youtube.com/watch?v=pdgCGyrRpAw
	- https://talks.toorcon.net/toorcon21/talk/KE9SYU/

## Talks: 2018

- A Christmas Carol - The Spectres of the Past, Present, and Future
	- 35c3 (2018)
	- Moritz Lipp, Michael Schwarz, Daniel Gruss and Claudio Canella
	- https://media.ccc.de/v/35c3-9893-a_christmas_carol_-_the_spectres_of_the_past_present_and_future
- Behind the Speculative Curtain: The True Story of Fighting Meltdown and Spectre
	- Black Hat USA 2018
	- Eric Doerr, Matt Linton, Art Manion, Christopher Robinson
	- https://www.blackhat.com/us-18/briefings/schedule/index.html#behind-the-speculative-curtain-the-true-story-of-fighting-meltdown-and-spectre-11755
	- https://www.youtube.com/watch?v=7KdDuqh2bgw
- Beyond Belief: The Case of Spectre and Meltdown
	- [BlueHatIL](http://www.bluehatil.com/abstracts.html) 2018
	- Daniel Gruss, Moritz Lipp, Michael Schwarz
	- https://www.youtube.com/watch?v=_4O0zMW-Zu4
	- http://www.bluehatil.com/files/Beyond%20Belief%20-%20The%20Case%20of%20Spectre%20and%20Meltdown.pdf
- Exploiting modern microarchitectures: Meltdown, Spectre, and other hardware attacks
	- Jon Masters, Red Hat, Stanford EE380, Jan 31 2018
	- https://www.youtube.com/watch?v=zuBw1HFJMsM
	- http://web.stanford.edu/class/ee380/Abstracts/180131.html
	- http://web.stanford.edu/class/ee380/Abstracts/180131-slides.pdf
- Peering Behind the Turing Mirror
	- SPLASH-I 2018; Ben L. Titzer
	- https://www.youtube.com/watch?v=CXR0XwI9Yt4
	- https://2018.splashcon.org/event/splash-2018-splash-i-peering-behind-the-turing-mirror
- Spectre: Exploiting Speculative Execution
	- SiFive Tech Talk: Paul Kocher
	- January 31, 2018
	- https://www.youtube.com/watch?v=hqIavX_SCWc
- Spectre/Meltdown and What It Means for Future Chip Design
	- Hot Chips 30 (2018) Keynote 1
	- John Hennessy, Paul Turner, Jon Masters, Mark Hill
	- https://www.youtube.com/watch?v=d5XzVF0sAZo
	- https://www.hotchips.org/hc30/1conf/1.07_Hotchips_Security_Keynote.pdf
- Wrangling with the Ghost: An Inside Story of Mitigating Speculative Execution Side Channel Vulnerabilities
	- Black Hat USA 2018
	- Matt Miller, Anders Fogh, Christopher Ertl
	- https://github.com/Microsoft/MSRC-Security-Research/blob/master/presentations/2018_08_BlackHatUSA/us-18-Fogh-Ertl-Wrangling-with-the-Ghost-An-Inside-Story-of-Mitigating-Speculative-Execution-Side-Channel-Vulnerabilities.pdf

## Talks: 2017

- Android Security Symposium 2017 - Drammer: Flip Feng Shui goes mobile (Victor van der Veen)
	- https://www.youtube.com/watch?v=Zyqq2hj9zrc
- HackPra 2017 - Anders Fogh: "Covert shotgun: Automatically finding covert channels in SMT"
	- https://www.youtube.com/watch?v=oVmPQCT5VkY
	- https://cyber.wtf/2016/09/27/covert-shotgun/
- HackPra 2017 - Victor van der Veen: "Drammer: The Making-Of" - https://www.youtube.com/watch?v=DF0k9yKYwfo
- hardwear.io 2017 - Shaking Trust in Hardware - Ben Gras & Kaveh Razavi
	- https://www.vusec.net/2017/12/recorded-talk-trusting-hardware-ffs-anc/
	- https://www.youtube.com/watch?v=CWXL3tX00aU
- HITB2017AMS D1T1 - Drammer: The Making Of - Victor van der Veen
	- https://www.youtube.com/watch?v=_oCEpfw1IPM
- Papers We Love Singapore #026 (2017) - Row Hammer: Flipping Bits in Memory Without Accessing Them
	- https://www.youtube.com/watch?v=1iBpLhFN_OA
	- https://speakerdeck.com/burnflare/row-hammer-papers-we-love
- RuhrSec 2017: "A new categorization system for Side-channel attacks on mobile devices & more", Dr. Veelasha Moonsamy
	- https://www.youtube.com/watch?v=YxikZkZ6KuE
- RuhrSec 2017: "Rowhammer Attacks: A Walkthrough Guide", Dr. Clémentine Maurice & Daniel Gruss
	- https://www.youtube.com/watch?v=-33gCDrSl_Q
- RuhrSec 2017: "Using Microarchitectural Design to Break KASLR and More", Anders Fogh
	- https://www.youtube.com/watch?v=LyiB1jlUdN8
- USENIX Security '17 - Strong and Efficient Cache Side-Channel Protection using Hardware Transactional Memory
	- https://www.youtube.com/watch?v=4_-c7ueHHqc
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/gruss

## Talks: 2016

- Black Hat 2016 - ARMageddon: How Your Smartphone CPU Breaks Software-Level Security and Privacy - https://www.youtube.com/watch?v=9KsnFWejpQg
- Black Hat 2016 - Side-Channel Attacks on Everyday Applications - Taylor Hornby
	- https://github.com/defuse/flush-reload-attacks
	- https://www.blackhat.com/docs/us-16/materials/us-16-Hornby-Side-Channel-Attacks-On-Everyday-Applications.pdf
	- https://www.blackhat.com/docs/us-16/materials/us-16-Hornby-Side-Channel-Attacks-On-Everyday-Applications-wp.pdf
	- https://www.youtube.com/watch?v=GPwNFrpd1KU
- CCS 2016 - CREDAL: Towards Locating a Memory Corruption Vulnerability with Your Core Dump - https://www.youtube.com/watch?v=jOL4oElUKjA
- CCS 2016 - Drammer: Deterministic Rowhammer Attacks on Mobile Platforms - https://www.youtube.com/watch?v=lTaMvBN1PoA
- CCS 2016 - ECDSA Key Extraction from Mobile Devices via Nonintrusive Physical Side Channels - https://www.youtube.com/watch?v=0SQUQbth5vU
- CCS 2016 - On Code Execution Tracking via Power Side-Channel - https://www.youtube.com/watch?v=YwL_p3TxhlA
- CHES 2016 - Curious case of Rowhammer Flipping Secret Exponent Bits using Timing Analysis - https://www.youtube.com/watch?v=8x2qodFfY5s
- Clémentine Maurice: "Reverse-engineering CPUs for fun and profit" - https://www.youtube.com/watch?v=IT6PFSRrvsU
- Daniel Gruss – Microarchitectural Incontinence - You would leak too if you were so fast! - https://www.youtube.com/watch?v=cAWmNp3Ukqk
- DEF CON 24 2016 Side channel attacks on high security electronic safe locks - https://www.youtube.com/watch?v=vJ9NdvKYxeg
- HITB2016AMS CLOSING KEYNOTE - Hardware Side Channels in Virtualized Environments - Sophia D'Antoine - https://www.youtube.com/watch?v=1KteO7FPXYw
- HITB2016AMS D2T1 - Cache Side Channel Attacks: CPU Design As A Security Problem - Anders Fogh
	- https://www.youtube.com/watch?v=UH6dFbiX_hM
	- https://conference.hitb.org/hitbsecconf2016ams/materials/D2T1%20-%20Anders%20Fogh%20-%20Cache%20Side%20Channel%20Attacks.pdf
- Fastly Security Speaker Series 2016 - Jasper van Woudenberg on Side channel analysis and fault injection - https://www.youtube.com/watch?v=bu59ya8nOBM
- Return-Oriented Flush-Reload Side Channels on ARM and Their Implications for Android Devices - https://www.youtube.com/watch?v=tymvrJiJNl8
- RuhrSec 2016: "Cache Side-Channel Attacks and the case of Rowhammer", Daniel Gruss - https://www.youtube.com/watch?v=gxsguH5opsM
- Side-Channel Attacks on Everyday Applications - https://www.youtube.com/watch?v=GPwNFrpd1KU
- Three lessons that I learnt from Rowhammer - with implications for future security research - Thomas Dullien (Halvar Flake) - Null Singapore - https://www.youtube.com/watch?v=fkDD2ea7SD8
- Using Undocumented CPU Behavior to See Into Kernel Mode and Break KASLR in the Process
	- https://www.youtube.com/watch?v=Pwq0vv4X7m4
- What could possibly go wrong with {insert x86 instruction here}? [33c3] - https://www.youtube.com/watch?v=wue4QomGE74

## Talks: 2015

- Clémentine Maurice, Daniel Gruss: Rowhammer.js: Root privileges for web apps? - https://www.youtube.com/watch?v=9L5MJ43nbkI
- Controlled-Channel Attacks: Deterministic Side Channels for Untrusted Operating Systems - https://www.youtube.com/watch?v=fwUaN5ik8zE
- DEF CON 23 - Etienne Martineau - The art of cache timing covert channel on x86 multi core - https://www.youtube.com/watch?v=7X772EBdvnM
- Exploiting Out-of-Order Execution For Covert Cross-VM Communication - Black Hat 2015
	- https://www.youtube.com/watch?v=SjcKqVRjNHc
	- https://www.blackhat.com/docs/us-15/materials/us-15-DAntoine-Exploiting-Out-Of-Order-Execution-For-Covert-Cross-VM-Communication.pdf
- Exploiting the DRAM Rowhammer Bug to Gain Kernel Privileges - Mark Seaborn, Halvar Flake - Black Hat 2015
	- https://www.youtube.com/watch?v=0U7511Fb4to
- Last-Level Cache Side-Channel Attacks are Practical - https://www.youtube.com/watch?v=vpGI1ggKzC4
- REcon 2015 - Exploiting Out of Order Execution (Sophia D'Antoine)
	- https://www.youtube.com/watch?v=AbRoWa_xrzA
	- https://recon.cx/2015/slides/recon2015-06-sophia-d-antoine-Exploiting-Out-of-Order-Execution.pdf
- S$A: A Shared Cache Attack That Works across Cores and Defies VM Sandboxing -- and Its Application to AES - https://www.youtube.com/watch?v=mwMjn8niX-Y
- Side-Channel Attacks by Differential Power Analysis - Nathaniel Graff - https://www.youtube.com/watch?v=bHncSnHQleY

## Talks: 2014

- MIT 6.858 Computer Systems Security, Fall 2014 - Lecture 16. Side-Channel Attacks - https://www.youtube.com/watch?v=PuVMkSEcPiI

## Talks: 2009

- Defcon 17 - Sniff Keystrokes With Lasers/Voltmeters - Side Channel Attacks Using Optical Sampling
	- paper: https://www.defcon.org/images/defcon-17/dc-17-presentations/Andrea_Barisani-Daniele_%20Bianco/defcon-17-barisani-bianco-sniff_keystrokes-wp.pdf
	- slides: https://www.defcon.org/images/defcon-17/dc-17-presentations/defcon-17-barisani-bianco-sniff_keystrokes.pdf
	- video: https://www.youtube.com/watch?v=Amnv4ncqKtA
