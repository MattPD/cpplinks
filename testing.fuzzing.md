# [C++ links](README.md): Fuzzing

See also:

- [Testing](https://github.com/MattPD/cpplinks/blob/master/testing.md): [Continuous Integration](https://github.com/MattPD/cpplinks/blob/master/testing.md#continuous-integration)
- [Compilers Correctness](https://github.com/MattPD/cpplinks/blob/master/compilers.correctness.md): [Testing](https://github.com/MattPD/cpplinks/blob/master/compilers.correctness.md#testing)

# Contents

- [General](#general)
- [Readings](#readings): [Books](#readings-books), [General](#readings-general), [Practice](#readings-practice)
- [Software](#software)
	- [Software: AFL](#software-afl)
	- [Software: libFuzzer](#software-libfuzzer)
	- [Software: Benchmarking](#software-benchmarking)
	- [Software: OS: Linux](#software-os-linux)
	- [Software: OS: Windows](#software-os-windows)
	- [Software: Performance](#software-performance)
- [Talks](#talks): [2020](#talks-2020), [2019](#talks-2019), [2018](#talks-2018), [2017](#talks-2017), [2016](#talks-2016), [2015](#talks-2015), [2007](#talks-2007)

---

# General

- Awesome Fuzzing
	- https://github.com/secfigo/Awesome-Fuzzing
- Google Fuzzing Forum
	- Tutorials, examples, discussions, research proposals, and other resources related to fuzzing
	- https://github.com/google/fuzzing
- https://www.reddit.com/r/fuzzing/
- The Fuzzing Project
	- https://fuzzing-project.org/

---

# Readings

## Readings: Books

- Generating Software Tests: Breaking Software for Fun and Profit
	- https://www.fuzzingbook.org/

## Readings: General

- Evaluating Fuzz Testing
	- ACM Conference on Computer and Communications Security (CCS) 2018
	- George T. Klees, Andrew Ruef, Benjamin Cooper, Shiyi Wei, Michael Hicks
	- http://www.cs.umd.edu/~mwh/papers/klees2018fuzzeval.html
	- https://arxiv.org/abs/1808.09700
	- https://www.youtube.com/watch?v=ID8XtoMn43I
	- Evaluating Empirical Evaluations (for Fuzz Testing)
		- http://www.pl-enthusiast.net/2018/08/23/evaluating-empirical-evaluations-for-fuzz-testing/
	- How to Spot Good Fuzzing Research
		- https://blog.trailofbits.com/2018/10/05/how-to-spot-good-fuzzing-research/
	- Fuzzing and how to evaluate it
		- ISSISP 2018; Michael Hicks
		- https://cs.anu.edu.au/cybersec/issisp2018/assets/slides/hicks-fuzz-testing-eval.pdf
- FuzzingPaper: Recent Papers Related To Fuzzing
	- https://github.com/wcventure/FuzzingPaper
- Fuzzing: a survey
	- Cybersecurity 2018
	- Jun Li, Bodong Zhao and Chao Zhang
	- https://cybersecurity.springeropen.com/articles/10.1186/s42400-018-0002-y
- Fuzzing: Hack, Art, and Science
	- Communications of the ACM (CACM) 63(2) 2020
	- Patrice Godefroid
	- https://doi.org/10.1145/3363824
	- https://cacm.acm.org/magazines/2020/2/242350-fuzzing
	- https://patricegodefroid.github.io/public_psfiles/Fuzzing-101-CACM2020.pdf
- Fuzzing: On the Exponential Cost of Vulnerability Discovery
	- ESEC/FSE 2020
	- Marcel Böhme, Brandon Falk
	- https://mboehme.github.io/paper/FSE20.EmpiricalLaw.pdf
- The Art, Science, and Engineering of Fuzzing: A Survey
	- IEEE Transactions on Software Engineering (2019)
	- Valentin J.M. Manes, HyungSeok Han, Choongwoo Han, Sang Kil Cha, Manuel Egele, Edward J. Schwartz, Maverick Woo
	- https://arxiv.org/abs/1812.00140
	- https://www.jiliac.com/publication/survey/
	- Genealogy Database of Fuzzers
		- https://github.com/SoftSec-KAIST/Fuzzing-Survey
		- https://fuzzing-survey.org/
- The Fuzzing Hype-Train: How Random Testing Triggers Thousands of Crashes
	- IEEE Security & Privacy, 17(1) 2019
	- Mathias Payer
	- https://ieeexplore.ieee.org/document/8674043

## Readings: Practice

- Billions and billions of constraints: Whitebox fuzz testing in production
	- International Conference on Software Engineering ICSE 2013
	- E. Bounimova, P. Godefroid, D. Molnar
	- https://www.microsoft.com/en-us/research/publication/billions-and-billions-of-constraints-whitebox-fuzz-testing-in-production/
	- https://patricegodefroid.github.io/public_psfiles/icse2013.pdf
	- https://courses.cs.washington.edu/courses/cse484/14au/slides/whitebox-fuzzing.pdf
	- Interview with Patrice Godefroid - https://www.coursera.org/learn/software-security/lecture/SItpe/interview-with-patrice-godefroid
- Building an ARM-based Fuzzing Cluster
	- https://baerli.github.io/arm-fuzzingcluster/
- Circumventing Fuzzing Roadblocks with Compiler Transformations
	- https://lafintel.wordpress.com/2016/08/15/circumventing-fuzzing-roadblocks-with-compiler-transformations/
	- LAF LLVM Passes - https://gitlab.com/laf-intel/laf-llvm-pass
- Fuzzers love assertions
	- Jesse Ruderman 
	- http://www.squarefree.com/2014/02/03/fuzzers-love-assertions/
- Fuzzing with AFL workshop
	- SteelCon 2017, BSides London and Bristol 2019
	- Michael Macnair
	- Exercises to learn how to fuzz with American Fuzzy Lop
	- https://github.com/mykter/afl-training
- Fuzzing workflows: a fuzz job from start to finish
	- https://foxglovesecurity.com/2016/03/15/fuzzing-workflows-a-fuzz-job-from-start-to-finish/
- John Regehr
	- Who Fuzzes the Fuzzer? - https://blog.regehr.org/archives/501
	- Better Random Testing by Leaving Features Out - https://blog.regehr.org/archives/591
	- Swarm Testing
		- ISSTA 2012; Alex Groce, Chaoqiang Zhang, Eric Eide, Yang Chen, John Regehr
		- http://www.cs.utah.edu/~regehr/papers/swarm12.pdf
		- Draft Paper about Better Fuzzing - https://blog.regehr.org/archives/595
	- Tricking a Whitebox Testcase Generator - https://blog.regehr.org/archives/672
	- How to Fuzz an ADT Implementation - https://blog.regehr.org/archives/896
	- Fuzzers Need Taming - https://blog.regehr.org/archives/925
	- Levels of Fuzzing - https://blog.regehr.org/archives/1039
	- A New Compiler Fuzzing Paper - https://blog.regehr.org/archives/1061
	- What afl-fuzz Is Bad At - https://blog.regehr.org/archives/1238
	- API Fuzzing vs. File Fuzzing: A Cautionary Tale - https://blog.regehr.org/archives/1269
	- Reducers are Fuzzers - https://blog.regehr.org/archives/1284
	- Write Fuzzable Code - https://blog.regehr.org/archives/1687
	- Helping Generative Fuzzers Avoid Looking Only Where the Light is Good, Part 1 - https://blog.regehr.org/archives/1700
- One Weird Trick for Finding More Crashes: crasher recycling
	- https://insights.sei.cmu.edu/cert/2013/09/one-weird-trick-for-finding-more-crashes-1.html
- Statistical Evaluation of a Fuzzing Dictionary
	- https://bshastry.github.io/2018/10/01/Evaluating-Dictionary-For-Fuzzing.html
	- Static Program Analysis as a Fuzzing Aid
		- https://link.springer.com/chapter/10.1007/978-3-319-66332-6_2
	- Orthrus: A tool to manage, conduct, and assess dictionary-based fuzz testing
		- https://github.com/test-pipeline/Orthrus
- The Art of Fuzzing – Slides and Demos
	- 2017; René Freingruber
	- AFL & WinAFL, Taint Analysis, Reversing Tricks for Fuzzing, in-memory fuzzing, DynamoRio
	- https://sec-consult.com/en/blog/2017/11/the-art-of-fuzzing-slides-and-demos/
	- https://sec-consult.com/wp-content/uploads/files/vulnlab/the_art_of_fuzzing_slides.pdf
- What You Corrupt Is Not What You Crash: Challenges in Fuzzing Embedded Devices
	- NDSS 2018
	- M. Muench, J. Stijohann, F. Kargl, A. Francillon, Davide Balzarotti
	- http://s3.eurecom.fr/docs/ndss18_muench.pdf
	- https://github.com/avatartwo/ndss18_wycinwyc

---

# Software

- Angora: a mutation-based fuzzer
	- increase branch coverage by solving path constraints without symbolic execution
	- https://github.com/AngoraFuzzer/Angora
	- Angora: Efficient Fuzzing by Principled Search
		- Security and Privacy (S&P) 2018
		- Peng Chen, Hao Chen
		- https://arxiv.org/abs/1803.01307
- ClusterFuzz: a scalable fuzzing infrastructure which finds security and stability issues in software
	- https://github.com/google/clusterfuzz
	- https://opensource.googleblog.com/2019/02/open-sourcing-clusterfuzz.html
- DeepState: A unit test-like interface for fuzzing and symbolic execution
	- DeepState is a framework that provides C and C++ developers with a common interface to various symbolic execution and fuzzing engines. Users can write one test harness using a Google Test-like API, then execute it using multiple backends without having to learn the complexities of the underlying engines. It supports writing unit tests and API sequence tests, as well as automatic test generation.
	- https://github.com/trailofbits/deepstate
	- DeepState: Symbolic Unit Testing for C and C++
		- NDSS 18 Workshop on Binary Analysis Research
		- Peter Goodman and Alex Groce
		- https://www.cefns.nau.edu/~adg326/bar18.pdf
	- Fuzzing an API with DeepState
		- Part 1: https://blog.trailofbits.com/2019/01/22/fuzzing-an-api-with-deepstate-part-1/
		- Part 2: https://blog.trailofbits.com/2019/01/23/fuzzing-an-api-with-deepstate-part-2/
- FuzzFactory: Domain-Specific Fuzzing with Waypoints
	- https://github.com/rohanpadhye/FuzzFactory
	- SPLASH 2019 OOPSLA
		- Rohan Padhye, Caroline Lemieux, Koushik Sen, Laurent Simon, Hayawardh Vijayakumar
		- https://2019.splashcon.org/details/splash-2019-oopsla/57/FuzzFactory-Domain-Specific-Fuzzing-with-Waypoints
		- https://people.eecs.berkeley.edu/~ksen/papers/fuzzfactory.pdf
		- https://people.eecs.berkeley.edu/~rohanpadhye/files/fuzzfactory-oopsla19.pdf
- Grammarinator: ANTLRv4 grammar-based test generator
	- https://github.com/renatahodovan/grammarinator
- Honggfuzz
	- Security oriented fuzzer with powerful analysis options. Supports evolutionary, feedback-driven fuzzing based on code coverage (software- and hardware-based)
	- https://honggfuzz.dev/
	- https://github.com/google/honggfuzz
	- Feedback-driven fuzzing - https://github.com/google/honggfuzz/blob/master/docs/FeedbackDrivenFuzzing.md
	- Fuzzing TCP servers - http://blog.swiecki.net/2018/01/fuzzing-tcp-servers.html
	- Internals of Hongfuzz - Intel PT - https://tunnelshade.in/blog/2018/09/hongfuzz-intel-pt-instrumentation/
- JFS (JIT Fuzzing Solver)
	- Constraint solver based on coverage-guided fuzzing
	- https://github.com/delcypher/jfs
	- Just Fuzz It: Solving Floating-Point Constraints using Coverage-Guided Fuzzing
		- ESEC/FSE 2019
		- Daniel Liew, Cristian Cadar, Alastair F. Donaldson, and J. Ryan Stinnett.
		- https://srg.doc.ic.ac.uk/files/papers/jfs-esecfse-19.pdf
- MoonLight: Fuzzing Corpus Design and Construction
	- https://gitlab.anu.edu.au/lunar/moonlight
- Nautilus: Fishing for Deep Bugs with Grammars
	- https://github.com/RUB-SysSec/nautilus
	- Network and Distributed System Security Symposium (NDSS) 2019
		- Cornelius Aschermann, Tommaso Frassetto, Thorsten Holz, Patrick Jauernig, Ahmad-Reza Sadeghi, Daniel Teuchert
		- https://www.syssec.ruhr-uni-bochum.de/research/publications/nautilus/
- Orthrus
	- https://github.com/test-pipeline/orthrus
	- Orthrus is a tool for managing, conducting, and assessing dictionary-based security (fuzz) testing for autotools projects. At the moment, it supports Clang/LLVM instrumentation and the AFL ecosystem (afl-fuzz, afl-utils, afl-cov). The ultimate aim is for Orthrus to be a generic wrapper around state-of-the-art fuzz and instrumentation tools on the one hand, and disparate build systems on the other.
	- Static Program Analysis as a Fuzzing Aid
		- RAID 2017
		- Bhargava Shastry, Markus Leutner, Tobias Fiebig, Kashyap Thimmaraju, Fabian Yamaguchi, Konrad Rieck, Stefan Schmid, Jean-Pierre Seifert, Anja Feldmann
		- https://aperture-labs.org/pdf/raid2017.pdf
		- http://users.sec.t-labs.tu-berlin.de/~bshastry/raid17_slidedeck.pdf
		- https://link.springer.com/chapter/10.1007/978-3-319-66332-6_2
	- Static Exploration of Taint-Style Vulnerabilities Found by Fuzzing
		- USENIX WOOT 2017
		- Bhargava Shastry, Federico Maggi, Fabian Yamaguchi, Konrad Rieck, Jean-Pierre Seifert
		- https://arxiv.org/abs/1706.00206
- QSYM: A Practical Concolic Execution Engine Tailored for Hybrid Fuzzing
	- USENIX Security 2018
	- Insu Yun, Sangho Lee, Meng Xu, Yeongjin Jang, Taesoo Kim
	- https://github.com/sslab-gatech/qsym/
	- https://www.usenix.org/conference/usenixsecurity18/presentation/yun
- Radamsa
	- a general-purpose fuzzer
	- https://gitlab.com/akihe/radamsa
- RamFuzz: Combining Unit Tests, Fuzzing, and AI
	- A fuzzer for individual method parameters
	- RamFuzz is a fuzzer for individual method parameters in unit tests. A unit test can use RamFuzz to generate random parameter values for methods under test. The values are logged, and the log can be replayed to repeat the exact same test scenario. But RamFuzz also allows mutation of the replay, where some parts of the log are replayed while others are replaced by newly generated values. The new run is also logged, yielding a mutated test scenario and allowing the classic fuzzing evolution process of progressively mutating the input until a bug is triggered.
	- https://github.com/dekimir/RamFuzz
	- RamFuzz: A Framework for C++ Test Generation via Deep Learning - https://github.com/dekimir/RamFuzz/blob/master/sci/ramfuzz.md
- RapidFuzz
	- An experiment of hacking around RapidCheck to combine RapidCheck's property-based testing with libFuzzer.
	- It was very much influenced by Dan Luu's post which suggested exactly this combination: http://danluu.com/testing/
	- https://github.com/unapiedra/rapidfuzz
- TriforceAFL: AFL/QEMU fuzzing with full-system emulation.
	- https://github.com/nccgroup/triforceafl
	- https://github.com/timnewsham/TriforceAFL
	- https://www.nccgroup.trust/uk/about-us/newsroom-and-events/blogs/2016/june/project-triforce-run-afl-on-everything/
- zzuf: a transparent application input fuzzer
	- https://github.com/samhocevar/zzuf
	- http://caca.zoy.org/wiki/zzuf

## Software: AFL

- american fuzzy lop (AFL)
	- http://lcamtuf.coredump.cx/afl/
	- Technical "whitepaper" for afl-fuzz
		- http://lcamtuf.coredump.cx/afl/technical_details.txt
	- Automatically inferring file syntax with afl-analyze
		- https://lcamtuf.blogspot.com/2016/02/say-hello-to-afl-analyze.html
- AFL++
	- afl++ is afl 2.56b with community patches, AFLfast power schedules, qemu 3.1 upgrade + laf-intel support, MOpt mutators, InsTrim instrumentation, unicorn_mode, Redqueen and a lot more!
	- https://aflplus.plus/
	- https://github.com/AFLplusplus/AFLplusplus
- AFL-based-fuzzers-overview
	- https://github.com/google/fuzzing/blob/master/docs/afl-based-fuzzers-overview.md
- afl-utils
	- Utilities for automated crash sample processing/analysis, easy afl-fuzz job management and corpus optimization
	- https://gitlab.com/rc0r/afl-utils
- afl-cov - AFL Fuzzing Code Coverage
	- https://github.com/mrash/afl-cov
- afl-cov: AFL fuzzing coverage CFG visualization
	- https://github.com/axt/afl-cov
- afl-fuzz on different file systems
	- https://barro.github.io/2018/06/afl-fuzz-on-different-file-systems/
- AFL-Mutation-Chain
	- Recovers an approximation of the mutation chain that led to a particular seed in an AFL queue. Outputs the chain in either JSON or Graphviz DOT format.
	- https://github.com/adrianherrera/afl-mutation-chain
- AFLGo: Directed Greybox Fuzzing
	- https://github.com/aflgo/aflgo
	- Directed Greybox Fuzzing
		- Conference on Computer and Communications Security (CCS) 2017
		- Marcel Böhme, Van-Thuan Pham, Manh-Dung Nguyen, Abhik Roychoudhury
		- http://www.comp.nus.edu.sg/~abhik/pdf/CCS17.pdf
- Awesome-AFL
	- A curated list of different AFL forks and AFL inspired fuzzers with detailed equivalent academic papers with AFL-fuzzing tutorials
	- https://github.com/Microsvuln/Awesome-AFL
- Driller: augmenting AFL with symbolic execution!
	- https://github.com/shellphish/driller
	- Driller: Augmenting fuzzing through selective symbolic execution
		- NDSS 2016
		- N. Stephens, J. Grosen, C. Salls, A. Dutcher, R. Wang, J. Corbetta, Y. Shoshitaishvili, C. Kruegel, G. Vigna
		- https://www.cs.ucsb.edu/~vigna/publications/2016_NDSS_Driller.pdf
- Internals of AFL fuzzer - Compile Time Instrumentation
	- https://tunnelshade.in/blog/2018/01/afl-internals-compile-time-instrumentation/
- WinAFL: A fork of AFL for fuzzing Windows binaries
	- https://github.com/googleprojectzero/winafl
- Zoo AFL: AFL utilities and modifications
	- https://habr.com/en/company/dsec/blog/449134/

## Software: libFuzzer

- libFuzzer – a library for coverage-guided fuzz testing.
	- http://llvm.org/docs/LibFuzzer.html
	- http://tutorial.libFuzzer.info
- Deconstructing LibProtobuf/Mutator Fuzzing
	- https://bshastry.github.io/2019/01/18/Deconstructing-LPM.html
- Efficient Fuzzing Guide
	- https://chromium.googlesource.com/chromium/src/testing/libfuzzer/+/HEAD/efficient_fuzzing.md
- Fuzzing arbitrary functions in ELF binaries using LIEF and LibFuzzer
	- https://blahcat.github.io/2018/03/11/fuzzing-arbitrary-functions-in-elf-binaries/
- Introduction to using libFuzzer with llvm-toolset
	- https://developers.redhat.com/blog/2019/03/05/introduction-to-using-libfuzzer-with-llvm-toolset/
- libfuzzer-workshop
	- Materials of "Modern fuzzing of C/C++ Projects" workshop
	- https://github.com/Dor1s/libfuzzer-workshop
- libfuzzerfication
	- LibFuzzerfication project uses libFuzzer for fuzzing popular applications and libraries.
	- https://github.com/ouspg/libfuzzerfication
- libprotobuf-mutator
	- a library to randomly mutate protobuffers; can be used together with guided fuzzing engines, such as libFuzzer
	- https://github.com/google/libprotobuf-mutator

## Software: Benchmarking

- fuzzer-test-suite: Set of tests for fuzzing engines
	- https://github.com/google/fuzzer-test-suite
- FuzzBench: Fuzzer Benchmarking as a Service
	- https://github.com/google/FuzzBench
	- https://security.googleblog.com/2020/03/fuzzbench-fuzzer-benchmarking-as-service.html
	- https://opensource.googleblog.com/2020/03/fuzzbench-fuzzer-benchmarking-as-service.html

## Software: OS: Linux

- difuze: Fuzzer for Linux Kernel Drivers
	- https://github.com/ucsb-seclab/difuze
	- DIFUZE: Interface Aware Fuzzing for Kernel Drivers - CCS 2017
	- https://acmccs.github.io/papers/p2123-corinaA.pdf
	- http://seclist.us/difuze-fuzzer-for-linux-kernel-drivers.html
- syzkaller: an unsupervised, coverage-guided kernel fuzzer
	- https://github.com/google/syzkaller
	- Coverage-guided kernel fuzzing with syzkaller - https://lwn.net/Articles/677764/

## Software: OS: Windows

- Sienna Locomotive: A user-friendly fuzzing and crash triage tool for Windows
	- https://github.com/trailofbits/sienna-locomotive
	- User-Friendly Fuzzing with Sienna Locomotive
		- https://blog.trailofbits.com/2019/04/08/user-friendly-fuzzing-with-sienna-locomotive/

## Software: Performance

Fuzzing applied to software performance.

- PerfFuzz: Automatically Generate Pathological Inputs for C/C++ programs
	- ISSTA 2018
	- Caroline Lemieux, Rohan Padhye, Koushik Sen, and Dawn Song
	- https://github.com/carolemieux/perffuzz
	- https://people.eecs.berkeley.edu/~rohanpadhye/files/PerfFuzz-issta18.pdf
- perf fuzzer: Targeted fuzzing of the perf_event_open() system call
	- Technical Report, University of Maine, Tech. Rep., 2015
	- V. M. Weaver and D. Jones
	- http://web.eece.maine.edu/~vweaver/projects/perf_events/fuzzer/2015_perf_fuzzer_tr.pdf
	- perf_fuzzer perf_event syscall fuzzer
		- http://web.eece.maine.edu/~vweaver/projects/perf_events/fuzzer/
	- perf_event Validation Tests
		- http://web.eece.maine.edu/~vweaver/projects/perf_events/validation/
		- https://github.com/deater/perf_event_tests
- SlowFuzz: Automated Domain-Independent Detection of Algorithmic Complexity Vulnerabilities
	- A spin on libFuzzer so as to favor inputs incurring a slowdown. The key modifications consist of changing the fitness function, to favor inputs that excercise more basic block edges, as well as introducing probabilities in the selection of mutations to be performed, so as to preserve "locality" of the created inputs.
	- https://github.com/nettrino/slowfuzz
	- ACM CCS 2017
		- Theofilos Petsios, Jason Zhao, Angelos D. Keromytis, Suman Jana
		- https://arxiv.org/abs/1708.08437
		- https://www.youtube.com/watch?v=ZuWWs64UTts

---

# Talks

## Talks: 2020

- Lightning in a Bottle: 25 Years of Fuzzing
	- FuzzCon 2020; Richard Johnson
	- https://docs.google.com/presentation/d/1L3ZmbCxdkZZCCrZ1gBI5Kj32rAnNNho3rZVzQXjnCvs

## Talks: 2019

- C++ Sanitizers and Fuzzing for the Windows Platform Using New Compilers, Visual Studio, and Azure
	- CppCon 2019: Jim Radigan 
	- https://www.youtube.com/watch?v=0EsqxGgYOQU
	- https://github.com/CppCon/CppCon2019/tree/master/Presentations/address_sanitizers__cloud_at_microsoft
- Fuzzing for developers
	- StockholmCpp::0x15 - Pi Day 2019; Paul Dreik
	- https://www.youtube.com/watch?v=e_Oc9SkCo5s
- Going Beyond Coverage-Guided Fuzzing with Structured Fuzzing
	- Black Hat 2019; Jonathan Metzman
	- https://www.youtube.com/watch?v=S8JvzWDnjc0
	- https://www.blackhat.com/us-19/briefings/schedule/#going-beyond-coverage-guided-fuzzing-with-structured-fuzzing-16110
- Make your programs more reliable with Fuzzing
	- ACCU 2019; Marshall Clow
	- https://www.youtube.com/watch?v=x0FQkAPokfE
- Modern Source Fuzzing
	- OffensiveCon19; Ned Williamson
	- https://www.youtube.com/watch?v=xzG0pLM4Q64
- Testing Legacy Code - Fuzzing for Better Input Data
	- Meeting C++ 2019; Tina Ulbrich, Niel Waldren
	- https://meetingcpp.com/mcpp/slides/2019/Testing%20Legacy%20Code%20-%20Fuzzing%20for%20Better%20Input%20Data.pdf
-  What the Fuzz
	- Black Hat Europe 2019; Cornelius Aschermann and Sergej Schumilo 
	- https://www.youtube.com/watch?v=Wy7qY5ms3qY
	- https://www.blackhat.com/eu-19/briefings/schedule/#what-the-fuzz-18031

## Talks: 2018

- Adventures in Fuzzing
	- NYU Talk 2018; Brandon Falk
	- https://www.youtube.com/watch?v=SngK4W4tVc0
	- https://github.com/gamozolabs/adventures_in_fuzzing
- Finding security vulnerabilities with modern fuzzing techniques
	- RuhrSec 2018; Rene Freingruber
	- https://www.youtube.com/watch?v=KFmeHz_vxfo
- Fuzzing Corpus Optimization - Moonwalking with Moonbeams
	- CSides Canberra 2018; Shane Magrath
	- https://github.com/DSTCyber/presentations/tree/master/2018-fuzzing-corpus-distillation
	- https://gitlab.anu.edu.au/lunar/moonlight
- Fuzzing with AFL
	- NDC TechTown 2018; Erlend Oftedal
	- https://www.youtube.com/watch?v=DFQT1YxvpDo
	- https://vimeo.com/292689978
- Making Your Library More Reliable with Fuzzing
	- C++Now 2018; Marshall Clow 
	- https://www.youtube.com/watch?v=LlLJRHToyUk
	- https://github.com/boostcon/cppnow_presentations_2018/blob/master/05-10-2018_thursday/making_your_library_more_reliable_with_fuzzing__marshall_clow__cppnow_05182018.pdf
- Seems Exploitable: Exposing Hidden Exploitable Behaviors Using Extended Differential Fuzzing
	- HITB2018AMS; Fernando Arnaboldi
	- https://conference.hitb.org/hitbsecconf2018ams/sessions/seems-exploitable-exposing-hidden-exploitable-behaviors-using-extended-differential-fuzzing/
- Structure aware fuzzing
	- Meeting C++ 2018; Réka Kovács 
	- https://www.youtube.com/watch?v=wTWNmOSKfD4
	- https://meetingcpp.com/mcpp/slides/2018/Structured%20fuzzing.pdf
- Want more stable kernel? Fuzz it!
	- DevConf.cz 2018; Hangbin Liu
	- https://www.youtube.com/watch?v=XlPQpVlC37A

## Talks: 2017

- Between Testing and Formal Verification
	- SecAppDev, March 2017; Jan Tobias Mühlberg
	- https://handouts.secappdev.org/handouts/2017/Jan%20Tobias%20Muehlberg/201705-secappdev-muehlberg.pdf
	- https://www.youtube.com/watch?v=tjkLPErCFW0
	- https://github.com/verifast/verifast
- Finding Security Vulnerabilities by Fuzzing and Dynamic Code Analysis
	- Verification Futures 2017; Richard Storer
	- http://www.testandverification.com/wp-content/uploads/2017/Verification_Futures/Richard_Storer_MathEmbedded.pdf
	- https://www.youtube.com/watch?v=vCLLA7C5Afg
- Fuzz or lose: why and how to make fuzzing a standard practice for C++
	- CppCon 2017; Kostya Serebryany
	- https://www.youtube.com/watch?v=k-Cv8Q3zWNQ
- Fuzz Testing
	- C++ Weekly 85; Jason Turner
	- https://www.youtube.com/watch?v=gO0KBoqkOoU
- Fuzzing with AFL
	- Circle City Con 2017; Adam DC949
	- http://www.irongeek.com/i.php?page=videos/circlecitycon2017/106-fuzzing-with-afl-adam-dc949
- Modern Fuzzing of Media-Processing Projects
	- FOSDEM 2017; Max Moroz
	- https://archive.fosdem.org/2017/schedule/event/om_fuzzing/
	- https://www.youtube.com/watch?v=QQs82BdoA9c

## Talks: 2016

- Effective File Format Fuzzing – Thoughts, Techniques and Results
	- Black Hat Europe 2016; Mateusz Jurczyk
	- https://www.youtube.com/watch?v=qTTwqFRD1H8
	- https://www.blackhat.com/eu-16/briefings/schedule/#effective-file-format-fuzzing--thoughts-techniques-and-results-4879
	- https://j00ru.vexillium.org/talks/blackhat-eu-effective-file-format-fuzzing-thoughts-techniques-and-results/
	- https://www.blackhat.com/docs/eu-16/materials/eu-16-Jurczyk-Effective-File-Format-Fuzzing-Thoughts-Techniques-And-Results.pdf
- Fuzz Smarter Not Harder: An afl fuzz Primer
	- BSides San Francisco 2016; Craig Young
	- https://www.youtube.com/watch?v=29RbO5bftwo
- The Smart Fuzzer Revolution
	- BSides Lisbon 2016; Dan Guido
	- https://www.youtube.com/watch?v=g1E2Ce5cBhI

## Talks: 2015

- Automated Software Testing for the 21st Century
	- TCE 2015; Patrice Godefroid
	- https://patricegodefroid.github.io/public_psfiles/talk-tce2015.pdf
	- https://www.youtube.com/watch?v=HbIrWdjbX8Y

## Talks: 2007

- Revolutionizing the Field of Grey-box Attack Surface Testing with Evolutionary Fuzzing
	- DEFCON 2007; Jared DeMott, Richard Enbody, William Punch
	- http://www.blackhat.com/presentations/bh-usa-07/DeMott_Enbody_and_Punch/Presentation/bh-usa-07-demott_enbody_and_punch.pdf
	- https://www.blackhat.com/presentations/bh-usa-07/DeMott_Enbody_and_Punch/Whitepaper/bh-usa-07-demott_enbody_and_punch-WP.pdf
	- https://www.vdalabs.com/tools/EFS.pdf
	- https://www.youtube.com/watch?v=g7uFJnbvjNg
	- https://www.youtube.com/watch?v=G7sX7RhJ_2w
