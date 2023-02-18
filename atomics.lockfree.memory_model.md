# [C++ links](README.md): atomics, lock free, memory model

# Contents

- [Data Structures](#data-structures): [Readings](#data-structures-readings), [Software](#data-structures-software), [Talks](#data-structures-talks)
- [Readings](#readings)
- [References](#references)
- [Software](#software): [Performance](#software-performance)
- [Talks](#talks)

---

# Data Structures: Readings

- Lock-Free Locks Revisited
	- PPoPP 2022
	- Naama Ben-David, Guy E. Blelloch, Yuanhao Wei
	- https://arxiv.org/abs/2201.00813
	- https://dl.acm.org/doi/10.1145/3503221.3508433
	- https://www.youtube.com/watch?v=1bH0yy6Wo4w
	- _We have implemented a C++ library called Flock based on the ideas. Flock allows lock-based data structures to run in either lock-free or blocking (traditional locks) mode. We implemented a variety of tree and list-based data structures with Flock and compare the performance of the lock-free and blocking modes under a variety of workloads. The lock-free mode is almost as fast as blocking mode under almost all workloads, and significantly faster when threads are over-subscribed (more threads than processors). We also compare with several existing lock-based and lock-free alternatives._
	- Flock: A library for lock-free locks
		- a C++ library supporting lock-free locks as described in the paper
		- https://github.com/cmuparlay/flock
- On the Nature of Progress
	- OPODIS 2011: International Conference On Principles Of Distributed Systems
	- Maurice Herlihy, Nir Shavit
	- http://hdl.handle.net/1721.1/73900
	- http://www.cs.tau.ac.il/~shanir/progress.pdf
- Practical lock freedom
	- 2004 Cambridge University Technical Report UCAM-CL-TR-579; Keir Fraser
	- https://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-579.pdf
- Practical lock-free data structures
	- https://www.cl.cam.ac.uk/research/srg/netos/projects/archive/lock-free/
- Systems programming: Coping with parallelism
	- 1986 Technical report, IBM Almaden Research Center; R. Treiber
	- https://dominoweb.draco.res.ibm.com/58319a2ed2b1078985257003004617ef.html
	- https://dominoweb.draco.res.ibm.com/reports/rj5118.pdf
	- Includes Treiber's lock-free stack.
- References: Synchrobench 30+ data structures papers
	- https://github.com/gramoli/synchrobench#data-structures
	- Evaluated in Synchrobench: V. Gramoli. More than You Ever Wanted to Know about Synchronization. PPoPP 2015
		- https://sites.google.com/site/synchrobench/
- References: CDS C++ library data structures
	- (lock-free lock-free stack, queues, unordered set/map, skip-list)
	- https://github.com/khizmax/libcds#references

## Data Structures: Readings: Queues

- Mechanized Verification of a Fine-Grained Concurrent Queue from Meta’s Folly Library
	- Certified Programs and Proofs (CPP) 2022
	- Simon Friis Vindum, Lars Birkedal, Dan Frumin
	- https://popl22.sigplan.org/details/CPP-2022-papers/16/Mechanized-Verification-of-a-Fine-Grained-Concurrent-Queue-from-Meta-s-Folly-Library
	- MPMCQueue: a high-performance bounded concurrent queue that supports multiple producers, multiple consumers, and optional blocking
		- https://github.com/facebook/folly/blob/main/folly/MPMCQueue.h

# Data Structures: Software

- ASCYLIB
	- https://github.com/LPD-EPFL/ASCYLIB
	- ASCYLIB is a concurrent-search data-structure library with over 30 implementantions of linked lists, hash tables, skip lists, and binary search trees.
	- Asynchronized Concurrency: The Secret to Scaling Concurrent Search Data Structures
		- ASPLOS 2015
		- Tudor David, Rachid Guerraoui, Vasileios Trigonakis
		- http://infoscience.epfl.ch/record/207109/files/ascy_asplos15.pdf
		- Adrian Colyer's "The Morning Paper" summary: http://blog.acolyer.org/2015/04/17/asynchronized-concurrency-the-secret-to-scaling-concurrent-search-data-structures/
- Boost.Lockfree
	- http://www.boost.org/doc/libs/release/doc/html/lockfree.html
- CDS C++ library
	- https://github.com/khizmax/libcds
	- The Concurrent Data Structures (CDS) library is a collection of concurrent containers that don't require external (manual) synchronization for shared access, and safe memory reclamation (SMR) algorithms like Hazard Pointer and user-space RCU. CDS is mostly header-only template library. Only SMR core implementation is segregated to .so/.dll file.
- ConcurrencyFreaks
	- https://github.com/pramalhe/ConcurrencyFreaks
	- A library of concurrent data structures and synchronization mechanisms.
- Concurrency Kit
	- Concurrency primitives, safe memory reclamation mechanisms and non-blocking (including lock-free) data structures designed to aid in the research, design and implementation of high performance concurrent systems.
	- https://github.com/concurrencykit/ck
- Concurrent data structures
	- Compilation of concurrent data structures with at least lock-free or wait-free properties.
	- https://github.com/jfuentes/concurrent-data-structures
- moodycamel::ConcurrentQueue (MPMC): https://github.com/cameron314/concurrentqueue
	- moodycamel::ReaderWriterQueue (SPSC): SPSC: https://github.com/cameron314/readerwriterqueue
	- http://moodycamel.com/blog/2013/a-fast-lock-free-queue-for-c++
	- http://moodycamel.com/blog/2014/a-fast-general-purpose-lock-free-queue-for-c++
	- http://moodycamel.com/blog/2014/detailed-design-of-a-lock-free-queue
	- http://moodycamel.com/blog/2014/solving-the-aba-problem-for-lock-free-free-lists
- xenium: a collection of concurrent data structures and memory reclamation algorithms (a header-only library)
	- https://github.com/mpoeter/xenium
	- Effective Memory Reclamation for Lock-Free Data Structures in C++
		- 2018 Master's thesis; Manuel Pöter
		- http://katalog.ub.tuwien.ac.at/AC14552708
		- http://www.ub.tuwien.ac.at/dipl/VL/51367.pdf
		- https://github.com/mpoeter/emr

# Data Structures: Talks

## Data Structures: Talks: 2022

- Scalable and Low Latency Lock-free Data Structures in C++
	- CppCon 2022
	- Alexander Krizhanovsky
	- https://www.youtube.com/watch?v=_dS4Z6JifPs

## Data Structures: Talks: 2021

- Building a Lock-Free Multi-Producer, Multi-Consumer Queue for tcmalloc
	- CppCon 2021
	- Matt Kulukundis
	- https://www.youtube.com/watch?v=_qaKkHuHYE0
	- https://fowles.github.io/building-a-lock-free-mpmc-queue/

---

# Readings

## Blogs

- Anthony Williams
	- Implementing Dekker's algorithm with Fences
		- https://www.justsoftwaresolutions.co.uk/threading/implementing_dekkers_algorithm_with_fences.html
	- Memory Models and Synchronization
		- https://www.justsoftwaresolutions.co.uk/threading/memory_models_and_synchronization.html
	- The Intel x86 Memory Ordering Guarantees and the C++ Memory Model
		- https://www.justsoftwaresolutions.co.uk/threading/intel-memory-ordering-and-c++-memory-model.html
	- Intel and AMD Define Memory Ordering
		- https://www.justsoftwaresolutions.co.uk/threading/intel-and-amd-memory-ordering-defined.html
	- Definitions of Non-blocking, Lock-free and Wait-free
		- https://www.justsoftwaresolutions.co.uk/threading/non_blocking_lock_free_and_wait_free.html
	- Can non-overlapping spinlocks deadlock in C++?
		- https://www.justsoftwaresolutions.co.uk/cplusplus/can_spinlocks_deadlock.html
- Bartosz Milewski
	- http://bartoszmilewski.com/2008/11/11/who-ordered-sequential-consistency/
	- http://bartoszmilewski.com/2008/12/01/c-atomics-and-memory-ordering/
	- https://corensic.wordpress.com/category/sequential-consistency/
- Concurrency Freaks
	- http://concurrencyfreaks.blogspot.com/
	- https://github.com/pramalhe/ConcurrencyFreaks/
- Comparison: Lockless programming with atomics in C++ 11 vs. mutex and RW-locks
	- https://www.arangodb.com/2015/02/comparing-atomic-mutex-rwlocks/
- Fabian “ryg” Giesen
	- Cache coherency primer - https://fgiesen.wordpress.com/2014/07/07/cache-coherency/
- Fast Bounded-Concurrency Hash Tables
	- https://backtrace.io/blog/backtrace/workload-specialization/
- Jeff Preshing
	- http://preshing.com/20111118/locks-arent-slow-lock-contention-is/
	- http://preshing.com/20120515/memory-reordering-caught-in-the-act/
	- http://preshing.com/20120612/an-introduction-to-lock-free-programming/
	- http://preshing.com/20120625/memory-ordering-at-compile-time/
	- http://preshing.com/20120710/memory-barriers-are-like-source-control-operations/
	- http://preshing.com/20120913/acquire-and-release-semantics/
	- http://preshing.com/20120930/weak-vs-strong-memory-models/
	- http://preshing.com/20121019/this-is-why-they-call-it-a-weakly-ordered-cpu/
	- http://preshing.com/20130505/introducing-mintomic-a-small-portable-lock-free-api/
	- http://preshing.com/20130529/a-lock-free-linear-search/
	- http://preshing.com/20130605/the-worlds-simplest-lock-free-hash-table/
	- http://preshing.com/20130618/atomic-vs-non-atomic-operations
	- http://preshing.com/20130702/the-happens-before-relation/
	- http://preshing.com/20130823/the-synchronizes-with-relation/
	- http://preshing.com/20130922/acquire-and-release-fences/
	- http://preshing.com/20130930/double-checked-locking-is-fixed-in-cpp11/
	- http://preshing.com/20131125/acquire-and-release-fences-dont-work-the-way-youd-expect/
	- http://preshing.com/20140709/the-purpose-of-memory_order_consume-in-cpp11/
	- http://preshing.com/20141124/fixing-gccs-implementation-of-memory_order_consume/
	- http://preshing.com/20150402/you-can-do-any-kind-of-atomic-read-modify-write-operation/
- John Regehr
	- Proposal to Stress-Test Implementations of C++11 Concurrency - https://blog.regehr.org/archives/658
	- Race Condition vs. Data Race - https://blog.regehr.org/archives/490
	- Simplest Program Showing the Difference Between Sequential Consistency and TSO - https://blog.regehr.org/archives/898
- John Wickerson
	- Memory Consistency Models, and how to compare them automatically - https://johnwickerson.wordpress.com/2016/11/11/comparing-memory-consistency-models/
	- Ribbon Diagrams for Weak Memory - https://johnwickerson.wordpress.com/2017/04/17/ribbon-diagrams-for-weak-memory/
- Kukuryku Hub Series
	- http://kukuruku.co/hub/cpp/lock-free-data-structures-introduction
	- http://kukuruku.co/hub/cpp/lock-free-data-structures-basics-atomicity-and-atomic-primitives
	- http://kukuruku.co/hub/cpp/lock-free-data-structures-memory-model-part-3
	- http://kukuruku.co/hub/cpp/lock-free-data-structures-the-inside-memory-management-schemes
	- http://kukuruku.co/hub/cpp/lock-free-data-structures-the-inside-rcu
	- http://kukuruku.co/hub/cpp/lock-free-data-structures-the-evolution-of-a-stack
	- http://kukuruku.co/hub/cpp/lock-free-data-structures-yet-another-treatise
	- http://kukuruku.co/hub/cpp/lock-free-data-structures-exploring-queues
- "Moody Camel" Series:
	- http://moodycamel.com/blog/2013/a-fast-lock-free-queue-for-c++
	- http://moodycamel.com/blog/2014/a-fast-general-purpose-lock-free-queue-for-c++
	- http://moodycamel.com/blog/2014/detailed-design-of-a-lock-free-queue
	- http://moodycamel.com/blog/2014/solving-the-aba-problem-for-lock-free-free-lists
- Peter Veentjer
	- TSO and IBM System/370
		- https://pveentjer.blogspot.com/2021/07/ibm-370.html
- PSA: you should use WTF::Lock and WTF::Condition instead of WTF::SpinLock, WTF::Mutex, WTF::ThreadCondition, std::mutex, std::condition_variable, or std::condition_variable_any
	- https://lists.webkit.org/pipermail/webkit-dev/2015-August/027615.html
- Raymond Chen
	- What’s up with compare_exchange_weak anyway?
		- https://devblogs.microsoft.com/oldnewthing/20180329-00/?p=98375
	- How do I choose between the strong and weak versions of compare-exchange?
		- https://devblogs.microsoft.com/oldnewthing/20180330-00/?p=98395
- Russ Cox
	- Hardware Memory Models - https://research.swtch.com/hwmm
	- Programming Language Memory Models - https://research.swtch.com/plmm
- Sam Westrick
	- Race Conditions Can Be Useful for Parallelism - https://shwestrick.github.io/2022/09/27/useful-races.html
- The difficulty of lock-free programming: a bug in lockfree stack
	- http://mdf356.blogspot.com/2015/06/the-difficulty-of-lock-free-programming.html
- The x86 Memory Model
	- http://www.msully.net/blog/2015/02/25/the-x86-memory-model/
- Travis Downs
	- A Concurrency Cost Hierarchy
		- https://travisdowns.github.io/blog/2020/07/06/concurrency-costs.html
		- https://github.com/travisdowns/concurrency-hierarchy-bench
- Trip Report: Ad-Hoc Meeting on Threads in C++
	- 2006; Eric Niebler
	- http://www.artima.com/cppsource/threads_meeting.html

## Dissertations

- Compiler optimisations and relaxed memory consistency models
	- 2017 Ph.D. Dissertation; Robin Morisset
	- http://www.theses.fr/en/2017PSLEE050
	- https://tel.archives-ouvertes.fr/tel-01823521/
	- https://www.di.ens.fr/~zappa/students/morisset-phd.pdf
- Correct Compilation of Relaxed Memory Concurrency
	- 2019 Ph.D. Dissertation; Soham Chakraborty
	- http://plv.mpi-sws.org/soham/thesis/
	- https://kluedo.ub.uni-kl.de/frontdoor/index/index/docId/5697
- Designing Memory Consistency Models For Shared-Memory Multiprocessors
	- 1993 Ph.D. Dissertation; Sarita V. Adve
	- ftp://ftp.cs.wisc.edu/markhill/Theses/sarita_adve.pdf
	- http://digital.library.wisc.edu/1793/59824
- Memory Consistency Models for Shared-Memory Multiprocessors
	- 1995 Ph.D. Dissertation; Kourosh Gharachorloo
	- http://www.hpl.hp.com/techreports/Compaq-DEC/WRL-95-9.pdf
- Progressive Automated Formal Verification of Memory Consistency in Parallel Processors
	- 2020 Ph.D. Dissertation; Yatin A. Manerkar
	- https://www.cs.princeton.edu/research/techreps/TR-007-20
	- https://mrmgroup.cs.princeton.edu/papers/manerkar_thesis.pdf
- The C11 and C++11 Concurrency Model
	- 2014 Ph.D. Dissertation; Mark Batty
	- https://www.cs.kent.ac.uk/people/staff/mjb211/docs/toc.pdf
	- [2015 SIGPLAN John C. Reynolds Doctoral Dissertation award citation](http://www.sigplan.org/Awards/Dissertation/#2015): "Mark Batty’s dissertation makes significant contributions to the understanding of memory models for C and C++. The ISO C++ committee proposed a design for C and C++ concurrency that was not up to the task of capturing a realistic relaxed-memory concurrency model. Batty’s work uncovered a number of subtle and serious flaws in the design, and produced an improved design in completely rigorous and machine-checked mathematics. Using software tools to explore the consequences of the design, derived directly from the mathematics, it showed that it has the desired behavior on many examples, and developed mechanized proofs that the design meets some of the original goals, showing that for programs in various subsets of the language one can reason in simpler models. The standards committee have adopted this work in their C11, C++11, and C++14 standards. The members of the award committee were impressed with the quality of the work, the impact it has had on the standardization process for C++, and the clarity of the presentation."
- The Semantics of Multicopy Atomic ARMv8 and RISC-V
	- 2019 Ph.D. Dissertation; Christopher Pulte
	- https://doi.org/10.17863/CAM.39379
	- https://www.repository.cam.ac.uk/handle/1810/292229

## Papers - Implementation

- Common Compiler Optimisations are Invalid in the C11 Memory Model and what we can do about it
	- POPL 2015
	- Viktor Vafeiadis, Thibaut Balabonski, Soham Chakraborty, Robin Morisset, Francesco Zappa Nardelli
	- http://www.di.ens.fr/~zappa/readings/c11comp.pdf
- N4455: No Sane Compiler Would Optimize Atomics
	- http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4455.html
- Partially Redundant Fence Elimination for x86, ARM, and Power Processors
	- CC 2017
	- Robin Morisset, Francesco Zappa Nardelli
	- https://conf.researchr.org/event/CC-2017/cc-2017-papers-partially-redundant-fence-elimination-for-x86-arm-and-power-processors
- Sequential Reasoning for Optimizing Compilers under Weak Memory Concurrency
	- Programming Language Design and Implementation (PLDI) 2022
	- Minki Cho, Sung-Hwan Lee, Dongjae Lee, Chung-Kil Hur, Ori Lahav
	- https://doi.org/10.1145/3519939.3523718
	- https://sf.snu.ac.kr/promising-seq/
	- https://www.youtube.com/watch?v=Er-BI2SOe5A
	- https://github.com/snu-sf/promising-seq-coq

## Papers - Memory Model

- A Promising Semantics for Relaxed-Memory Concurrency
	- POPL 2017
	- Jeehoon Kang, Chung-Kil Hur, Ori Lahav, Viktor Vafeiadis, Derek Dreyer
	- https://sf.snu.ac.kr/promise-concurrency/
	- https://people.mpi-sws.org/~viktor/papers/popl2017-promising.pdf
	- https://popl17.sigplan.org/details/POPL-2017-papers/38/A-Promising-Semantics-for-Relaxed-Memory-Concurrency
	- https://www.youtube.com/watch?v=MDaWaPCs74U
- AutoMO: Automatic Inference of Memory Order Parameters for C/C++11
	- OOPSLA 2015
	- Peizhao Ou, Brian Demsky
	- http://plrg.ics.uci.edu/automo/
	- http://plrg.eecs.uci.edu/publications/oopsla15inference.pdf
- C++ Memory Model
	- 2012; Martin Kempf
	- https://wiki.ifs.hsr.ch/SemProgAnTr/SeminarHS12
	- https://wiki.ifs.hsr.ch/SemProgAnTr/files/CppMemoryModel_26_12_12.pdf
- Concurrency memory model compiler consequences
	- http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2007/n2338.html
- Foundations of the C++ Concurrency Memory Model
	- PLDI 2008; Hans-J. Boehm and Sarita V. Adve
	- http://rsim.cs.illinois.edu/Pubs/08PLDI.pdf
- Memory Barriers: a Hardware View for Software Hackers
	- 2010; Paul E. McKenney
	- http://www.rdrop.com/users/paulmck/scalability/paper/whymb.2010.07.23a.pdf
- Memory Model = Instruction Reordering + Store Atomicity
	- ACM SIGARCH Computer Architecture News 34(2) 2006
	- Arvind and J.-W. Maessen
	- http://csg.csail.mit.edu/pubs/memos/Memo-493/memo-493.pdf
	- 2006 MSR talk: https://www.microsoft.com/en-us/research/video/memory-model-instruction-reordering-store-atomicity/
- Memory Models for C/C++ Programmers
	- 2018; Manuel Pöter, Jesper Larsson Träff
	- https://arxiv.org/abs/1803.04432
- Memory Models: A Case for Rethinking Parallel Languages and Hardware
	- CACM 2010
	- Sarita V. Adve, Hans-J. Boehm
	- http://cacm.acm.org/magazines/2010/8/96610-memory-models-a-case-for-rethinking-parallel-languages-and-hardware/fulltext
- Programming Languages & Verification – MPI SWS
	- https://www.mpi-sws.org/research-areas/programming-languages-and-verification/
	- 2018 - Effective stateless model checking for C/C++ concurrency - http://plv.mpi-sws.org/rcmc/
	- 2017 - Formalizing the Concurrency Semantics of an LLVM Fragment - http://plv.mpi-sws.org/llvmcs/
	- 2017 - Repairing Sequential Consistency in C/C++11
		- PLDI 2017
		- Ori Lahav, Viktor Vafeiadis, Jeehoon Kang, Chung-Kil Hur, Derek Dreyer
		- https://plv.mpi-sws.org/scfix/
	- 2016 - Explaining Relaxed Memory Models with Program Transformations - http://plv.mpi-sws.org/trns/
	- 2016 - Validating Optimizations of Concurrent C/C++ Programs - http://plv.mpi-sws.org/validc/
	- 2015 - Reasoning about C11 Program Transformations - http://plv.mpi-sws.org/c11comp/
- Shared Memory Consistency Models: A Tutorial
	- IEEE Computer 29(12) 1996
	- Sarita V. Adve, Kourosh Gharachorloo
	- http://www.hpl.hp.com/techreports/Compaq-DEC/WRL-95-7.pdf
	- http://www.ai.mit.edu/projects/aries/papers/consistency/computer_29_12_dec1996_p66.pdf
- Simple and Efficient Semantics for Concurrent Programming Languages
	- http://web.cs.ucla.edu/~todd/research/memmodels.html
- Synthesizing Memory Models from Framework Sketches and Litmus Tests
	- PLDI 2017
	- James Bornholt and Emina Torlak
	- MemSynth: Synthesis-Aided Memory Model Development
		- http://memsynth.uwplse.org/
- The Silently Shifting Semicolon
	- SNAPL 2015
	- Daniel Marino, Todd D. Millstein, Madanlal Musuvathi, Satish Narayanasamy, Abhayendra Singh, Madan Musuvathi
	- https://www.microsoft.com/en-us/research/publication/the-silently-shifting-semicolon/
	- http://web.cs.ucla.edu/~todd/research/snapl15.pdf
	- Proposes the designation "Weak DRF0 (WDRF0)" for the C++ memory model: "C/C++ has settled for a memory model weaker than DRF0, which we call Weak DRF0 (WDRF0). DRF programs are not guaranteed SC semantics in WDRF0. To get SC, programmers have to additionally avoid the use of the so-called low-level atomic primitives. The weak semantics of DRF programs in C++ is similar in complexity to the semantics of non-DRF programs in Java."
- Threads Basics
	- HP Labs Technical Report 2009-259; Hans-J. Boehm
	- First Published: Nov. 17, 2008; Last revised: January 16, 2011
	- http://www.hboehm.info/c++mm/threadsintro.html
- Threads Cannot be Implemented as a Library
	- PLDI 2005; Hans-J. Boehm
	- http://www.hpl.hp.com/techreports/2004/HPL-2004-209.pdf
	- http://www.hboehm.info/misc_slides/pldi05_threads.pdf
	- LtU: http://lambda-the-ultimate.org/node/950
- x86-TSO: A Rigorous and Usable Programmer’s Model for x86 Multiprocessors
	- CACM 2010
	- Peter Sewell, Susmit Sarkar, Scott Owens, Francesco Zappa Nardelli, Magnus O. Myreen
	- https://www.cl.cam.ac.uk/~pes20/weakmemory/cacm.pdf
- You Don't Know Jack about Shared Variables or Memory Models: Data Races are Evil
	- CACM 2012, ACM Queue 2011
	- Hans-J. Boehm, Sarita V. Adve
	- https://queue.acm.org/detail.cfm?id=2088916

### Papers - Memory Model: 2019

- Bridging the Gap Between Programming Languages and Hardware Weak Memory Models
	- POPL 2019
	- Anton Podkopaev, Ori Lahav, Viktor Vafeiadis
	- https://popl19.sigplan.org/event/popl-2019-research-papers-bridging-the-gap-between-programming-languages-and-hardware-weak-memory-models
- On Library Correctness under Weak Memory Consistency
	- POPL 2019
	- Azalea Raad, Marko Doko, Lovro Rožić, Ori Lahav, Viktor Vafeiadis
	- https://popl19.sigplan.org/event/popl-2019-research-papers-on-library-correctness-under-weak-memory-consistency
- Promising-ARM/RISC-V: A Simpler and Faster Operational Concurrency Model
	- PLDI 2019
	- Christopher Pulte, Jean Pichon-Pharabod, Jeehoon Kang, Sung-Hwan Lee, Chung-Kil Hur
	- https://dl.acm.org/doi/10.1145/3314221.3314624
	- https://sf.snu.ac.kr/promising-arm-riscv/
	- https://github.com/snu-sf/promising-arm
	- https://github.com/promising-arm-riscv/promising-arm-riscv
	- https://www.youtube.com/watch?v=0oHpVr1IFN0
- Verifying C11 Programs Operationally
	- Principles and Practice of Parallel Programming (PPoPP) 2019
	- Simon Doherty, Brijesh Dongol, Heike Wehrheim, John Derrick
	- https://arxiv.org/abs/1811.09143
	- https://ppopp19.sigplan.org/event/ppopp-2019-papers-verifying-c11-programs-operationally

### Papers - Memory Model: 2020

- Foundations of Empirical Memory Consistency Testing
	- OOPSLA 2020
	- Tyler Sorensen, Esin Tureci, Jake Kirkham, Margaret R. Martonosi
	- https://2020.splashcon.org/details/splash-2020-oopsla/102/Foundations-of-Empirical-Memory-Consistency-Testing
	- https://users.soe.ucsc.edu/~tsorensen/files/oopsla2020.pdf
- Owicki-Gries Reasoning for C11 RAR
	- ECOOP 2020
	- Sadegh Dalvandi, Simon Doherty, Brijesh Dongol, Heike Wehrheim
	- https://2020.ecoop.org/details/ecoop-2020-papers/11/Owicki-Gries-Reasoning-for-C11-RAR
	- https://brijeshdongol.github.io/full-version/ECOOP20.pdf
	- C11 RAR memory model (a fragment of C11 with both relaxed and release-acquire accesses)
- Reconciling Event Structures with Modern Multiprocessors
	- ECOOP 2020
	- Evgenii Moiseenko, Anton Podkopaev, Ori Lahav, Orestis Melkonian, Viktor Vafeiadis
	- http://plv.mpi-sws.org/weakestmoToImm/
	- https://arxiv.org/abs/1911.06567
	- https://2020.ecoop.org/details/ecoop-2020-papers/5/Reconciling-Event-Structures-with-Modern-Multiprocessors

### Papers - Memory Model: 2021

- A Survey of Programming Language Memory Models
	- Programming and Computer Software, Vol. 47, No. 6, 2021
	- Evgenii Moiseenko, Anton Podkopaev, Dmitrii Koznov
	- https://media.githubusercontent.com/media/anlun/publicFiles/master/papers/Moiseenko-al-Programming21-full.pdf
- Verifying Observational Robustness against a C11-Style Memory Model
	- POPL 2021
	- Roy Margalit, Ori Lahav
	- https://www.cs.tau.ac.il/~orilahav/papers/popl21_robustness.pdf
	- https://www.cs.tau.ac.il/~orilahav/papers/popl21_robustness_full.pdf
	- https://popl21.sigplan.org/details/POPL-2021-research-papers/4/Verifying-Observational-Robustness-Against-a-C11-style-Memory-Model
	- Rocker: Robustness Checker
		- a tool to verify robustness of programs written in TPL against C11 semantics.
		- https://github.com/rymrg/rocker

### Papers - Memory Model: 2022

- Mixed-Proxy Extensions for the NVIDIA PTX Memory Consistency Model
	- International Symposium on Computer Architecture (ISCA), Industry Track, 2022
	- Daniel Lustig, Simon Cooksey, Olivier Giroux
	- https://github.com/NVlabs/mixedproxy
	- https://doi.org/10.1145/3470496.3533045
	- > In this work, we describe the "proxy" extensions added to version 7.5 of NVIDIA's PTX ISA for GPUs. A proxy is an extra tag abstractly applied to every memory or fence operation. Proxies generalize the notion of address translation and specialized non-coherent cache hierarchies into an abstraction that cleanly describes the resulting non-standard behavior. The goal of proxies is to facilitate integration of these specialized memory accesses into the general-purpose PTX programming model in a fully composable manner. 
- The Leaky Semicolon: Compositional Semantic Dependencies for Relaxed-Memory Concurrency
	- POPL 2022
	- Alan Jeffrey, James Riely, Mark Batty, Simon Cooksey, Anton Podkopaev
	- https://github.com/weakmemory/weakmemory.github.io/blob/master/pwt.md
	- https://popl22.sigplan.org/details/POPL-2022-popl-research-papers/54/The-Leaky-Semicolon-Compositional-Semantic-Dependencies-for-Relaxed-Memory-Concurren
	- JetBrains Research Rus 2021
		- https://www.youtube.com/watch?v=AsrckMUlIjY

---

# References

- 1024cores
	- http://www.1024cores.net/
	- http://www.1024cores.net/home/lock-free-algorithms
- C++ Standard
	- [atomics] Atomic operations library
		- https://eel.is/c++draft/#atomics
	- [basic.exec] Program execution
		- https://eel.is/c++draft/basic.exec
	- C++11 Language Extensions — Concurrency
		- https://isocpp.org/wiki/faq/cpp11-language-concurrency
	- C++11 Standard Library Extensions — Concurrency
		- https://isocpp.org/wiki/faq/cpp11-library-concurrency
- C/C++11 mappings to processors
	- C/C++11 atomic operations to x86, PowerPC, ARMv7, ARMv8, and Itanium instruction sequences
	- https://www.cl.cam.ac.uk/~pes20/cpp/cpp0xmappings.html
- GCC Wiki - Atomic: https://gcc.gnu.org/wiki/Atomic/
- GCC Wiki - The C++11 Memory Model and GCC: https://gcc.gnu.org/wiki/Atomic/GCCMM
- glibc wiki: Concurrency
	- https://sourceware.org/glibc/wiki/Concurrency
- Linux kernel memory barriers
	- https://www.kernel.org/doc/Documentation/memory-barriers.txt
- LLVM Atomic Instructions and Concurrency Guide
	- http://llvm.org/docs/Atomics.html
- Memory model - http://en.cppreference.com/w/cpp/language/memory_model
- N1276: A Less Formal Explanation of the Proposed C++ Concurrency Memory Model
	- http://www.open-std.org/jtc1/sc22/wg14/www/docs/n1276.htm
- Programming with Threads: Questions Frequently Asked by C and C++ Programmers
	- Hans-J. Boehm & Paul McKenney
	- http://www.hboehm.info/c++mm/user-faq.html
- REMS: Rigorous Engineering for Mainstream Systems
	- https://www.cl.cam.ac.uk/~pes20/rems/
	- Relaxed-Memory Concurrency
		- https://www.cl.cam.ac.uk/~pes20/weakmemory/
- Some notes on lock-free and wait-free algorithms
	- http://www.rossbencina.com/code/lockfree
- The Check Tool Suite: Programmability, Correctness and Security Issues in Heterogeneous Multiprocessor and Mobile Systems
	- Martonosi Research Group - http://mrmgroup.cs.princeton.edu/
	- http://check.cs.princeton.edu/
- Threads and memory model for C++
	- http://hboehm.info/c++mm/
- What every systems programmer should know about lockless concurrency
	- 2018; Matt Kline
	- https://assets.bitbashing.io/papers/lockless.pdf
- Why the "volatile" type class should not be used
	- https://www.kernel.org/doc/Documentation/process/volatile-considered-harmful.rst

## Books

- A Primer on Memory Consistency and Cache Coherence, Second Edition
	- Synthesis Lectures on Computer Architecture 15:1 (2020)
	- Vijay Nagarajan, Daniel J. Sorin, Mark D. Hill, David A. Wood
	- https://doi.org/10.2200/S00962ED2V01Y201910CAC049
- Is Parallel Programming Hard, And If So, What Can You Do About It?
	- [Paul E. McKenney](http://www.rdrop.com/~paulmck/)
	- https://kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html

## Courses

- Advanced Computer Architecture - University of Utah - CS/ECE 7810
	- http://www.eng.utah.edu/~cs7810/
	- Lecture 11: Consistency Models: [Slides (pdf)](http://www.eng.utah.edu/~cs7810/pres/14-7810-11.pdf)
	- [YouTube Video 68](http://www.youtube.com/watch?v=VfIeD_B4YhM) (Example multi-threaded programs and sequentially consistent results)
	- [YouTube Video 69](http://www.youtube.com/watch?v=DzGk1FXrQEo) (Hardware support for sequential consistency, example of how SC is violated if program order is violated)
	- [YouTube Video 70](http://www.youtube.com/watch?v=AOhRBI7GyZU) (Example on how a coherence protocol may violate write atomicity and sequential consistency, hardware support for sequential consistency, safe optimizations to speed up the hardware)
	- [YouTube Video 71](http://www.youtube.com/watch?v=JjRnHP_u-aY) (A hardware-software approach to improving performance with relaxed consistency models and fences)
- Parallel Computer Architecture - CMU - 18-742
	- http://www.archive.ece.cmu.edu/~ece742/f12/doku.php?id=lectures
	- https://www.youtube.com/playlist?list=PLSEZzvupP7hNjq3Tuv2hiE5VvR-WRYoW4

---

# Software

- act: automagic compiler tormentor
	- act is a toolbox for finding concurrency memory model discrepancies between C code and its compiled assembly.
	- It can use memalloy as a test-case generator, and generates litmus tests that can be used with herd7.
	- https://github.com/MattWindsor91/act/
- C11Tester: A Testing tool for C11 and C++11 Atomics
	- a testing tool for C11/C++11 which randomly explores the behaviors of code under the C/C++ memory model
	- http://plrg.ics.uci.edu/c11tester/
	- C11Tester: A Fuzzer for C/C++ Atomics
		- Architectural Support for Programming Languages and Operating Systems (ASPLOS) 2021
		- Weiyu Luo, Brian Demsky
		- C11Tester: A Race Detector for C/C++ Atomics Technical Report
			- https://arxiv.org/abs/2102.07901
	- Probabilistic Concurrency Testing for Weak Memory (PCTWM)
		- https://github.com/GMYMingyu/C11_PCT_PCTWM
		- https://github.com/GMYMingyu/pctwm_c11
		- Probabilistic Concurrency Testing for Weak Memory Programs
			- ASPLOS 2023
			- Mingyu Gao, Soham Chakraborty, Burcu Kulahcioglu Ozkan
			- https://dl.acm.org/doi/10.1145/3575693.3575729
			- https://zenodo.org/record/7225459
		- Probabilistic Testing for Weak Memory Concurrency
			- 2022 Master's Thesis
			- Mingyu Gao
			- https://repository.tudelft.nl/islandora/object/uuid:28878472-f58d-42ad-b889-ef5e23d3d129
- CDSChecker: A Model Checker for C11 and C++11 Atomics
	- http://demsky.eecs.uci.edu/c11modelchecker.html
	- http://plrg.eecs.uci.edu/publications/c11modelcheck.pdf
- CppMem: Interactive C/C++ memory model
	- http://svr-pes20-cppmem.cl.cam.ac.uk/cppmem/
	- https://www.modernescpp.com/index.php/cppmem-an-overview
- diy
	- The sofware suite diy provides tools to design and test weak memory models. It handles ARMv8 (AArch64), ARMv7 (ARM), Power (PPC) and X86 assembly models, plus a generic (LISA) assembly language.
	- http://diy.inria.fr/
	- herd, a memory model simulator
		- http://diy.inria.fr/herd/
		- http://diy.inria.fr/doc/herd.html
		- https://github.com/herd/herdtools7
- MemSynth: An advanced automated reasoning tool for memory consistency model specifications.
	- https://github.com/uwplse/memsynth
	- Build an x86 memory model!
		- https://demo.memsynth.org/
- Nidhugg: a bug-finding tool which targets bugs caused by concurrency and relaxed memory consistency in concurrent programs
	- It works on the level of LLVM internal representation, which means that it can be used for programs written in languages such as C or C++.
	- Currently Nidhugg supports the SC, TSO, PSO, POWER and ARM memory models.
	- Target programs should use pthreads for concurrency, and each thread should be deterministic when run in isolation.
	- https://github.com/nidhugg/nidhugg
- Relacy Race Detector
	- http://www.1024cores.net/home/relacy-race-detector
- RMEM
	- a tool for exploring the relaxed-memory concurrency behaviour allowed by the instruction set architectures
	- ARM, POWER, RISC-V, x86
	- help page: http://www.cl.cam.ac.uk/~sf502/regressions/rmem/help.html
	- web interface: http://www.cl.cam.ac.uk/users/pes20/rmem/

## Software: Performance

- CircusTent: Atomic Memory Operation System Benchmarks
	- Memory system characterization benchmarks using atomic operations
	- https://github.com/tactcomplabs/circustent
- Synchrobench
	- https://github.com/gramoli/synchrobench
	- A benchmark to compare synchronization techniques for multicore programming

---

# Talks

## Slides

- COMP 522: Multicore Computing - Presentations
	- https://www.cs.rice.edu/~johnmc/comp522/lecture-notes/
- Concurrency Kit talks
	- http://concurrencykit.org/slides.html
	- Lock-Free Algorithms: An Introduction, Introduction to Lock-Free Algorithms: Through a case study, Safe Memory Reclamation: Epoch Reclamation, Towards accessible non-blocking technology for C, Fast Bounded-Concurrency Hash Tables
- Memory Management in C++14 and Beyond
	- Chicago C++ Meetup; July 7, 2015
	- Info: http://www.meetup.com/Chicago-C-CPP-Users-Group/events/223318263/
	- Slides: http://ccug.chicago.il.us/Spertus7jul2015.pdf
- Modern concurrent code in C/C++
	- GNU Tools Cauldron 2015; Torvald Riegel
	- https://gcc.gnu.org/wiki/cauldron2015?action=AttachFile&do=get&target=Torvald+Riegel_+Modern+concurrent+code+in+C.pdf
- Updating glibc concurrency
	- GNU Tools Cauldron 2015; Torvald Riegel
	- https://gcc.gnu.org/wiki/cauldron2015?action=AttachFile&do=get&target=Torvald+Riegel_+Updating+glibc+concurrency.pdf
-  Sarita Adve's Research Group - Talks
	- http://rsim.cs.illinois.edu/pubs.html#talks

## Videos

### 2022

- A lock-free `std::atomic<std::shared_ptr>`
	- Timur Doumler
	- 2022-09-13 - CppCon 2022
		- https://www.youtube.com/watch?v=gTpubZ8N0no
	- 2022-09-01 - NDC TechTown 2022
		- https://www.youtube.com/watch?v=WHe-8Nzx9Ag
	- 2022-04-06 - ACCU 2022
		- https://www.youtube.com/watch?v=a10JpqI-CvU
		- https://accu.org/conf-docs/PDFs_2022/timur_doumler_a_lockfree_atomic_shared_ptr.pdf
- Concurrency in C++: A Programmer’s Overview
	- CppNow 2022; Fedor Pikus
	- part 1 of 2: https://www.youtube.com/watch?v=ywJ4cq67-uc
	- part 2 of 2: https://www.youtube.com/watch?v=R0V4xJ9HZpA

### 2021

- Hazard Pointer Synchronous Reclamation Beyond Concurrency TS2
	- CppCon 2021; Maged Michael
	- https://www.youtube.com/watch?v=HKCN_0f04b8
	- Working Draft, Extensions to C++ for Concurrency Version 2
		- http://wg21.link/N4895
- Memory Architectures for Programmable Forward-Looking Systems
	- ISPASS 2021 Keynote Address; Dan Lustig
	- https://www.youtube.com/watch?v=YVsYn3NDOYk
- The Foundation of C++ Atomics: The Knowledge You Need to Correctly Use C++ Atomics
	- Filipe Mulonde
	- CppCon 2021: https://www.youtube.com/watch?v=BfEnMRWLjgQ
	- CPPP 2021: https://github.com/CpppFr/CPPP-21/tree/main/the_foundation_of_cxx_atomics_the_knowledge_you_need_to_correctly_use_cxx_atomics-filipe_mulonde
	- Meeting C++ 2021: https://www.youtube.com/watch?v=zE5IiaViVxk
- The Upcoming Concurrency TS Version 2 for Low-Latency and Lockless Synchronization
	- CppCon 2021
	- Maged Michael, Michael Wong, Paul E. McKenney
	- https://www.youtube.com/watch?v=ZrQ7dk5OXJU&list=PLHTh1InhhwT6vjwMy3RG5Tnahw0G9qIx6&index=48

### 2020

- A Relaxed Guide to memory_order_relaxed
	- CppCon 2020
	- Paul E. McKenney & Hans Boehm
	- https://www.youtube.com/watch?v=cWkUqK71DZ0
	- https://github.com/CppCon/CppCon2020/tree/main/Presentations/a_relaxed_guide_to_memory_order_relaxed

### 2019

- Atomics, Locks, and Tasks
	- CppCon 2019; Rainer Grimm
	- part 1: https://www.youtube.com/watch?v=o0i2fc0Keo8
	- part 2: https://www.youtube.com/watch?v=_eaB69ta_ig
- Concurrency in C++20 and Beyond
	- CppCon 2019; Anthony Williams
	- https://www.youtube.com/watch?v=jozHW_B3D4U
- The C++ memory model: an intuition
	- StockholmCpp 2019; Arvid Norberg
	- https://www.youtube.com/watch?v=OyNG4qiWnmU
- The C++20 Synchronization Library
	- Bryce Adelstein Lelbach
	- CppCon 2019
		- https://www.youtube.com/watch?v=Zcqwb3CWqs4
	- Meeting C++ 2019
		- https://www.youtube.com/watch?v=zoMZAV6FEbc
		- https://meetingcpp.com/mcpp/slides/2019/cpp20_synchronization_library__r5__2019_meeting_cpp3598.pdf
	- https://github.com/brycelelbach/cpp20_mini_tasking_runtime
	- https://github.com/brycelelbach/cpp20_synchronization_library
	- `std::atomic::wait`/`std::atomic::notify_*`; `std::atomic_ref`; `std::counting_semaphore`; `std::latch`, `std::barrier`
- The One-Decade Task: Putting std::atomic in CUDA
	- CppCon 2019; Olivier Giroux
	- https://www.youtube.com/watch?v=VogqOscJYvk
- Wait-free data structures and wait-free transactions
	- Hydra: Distributed Computing Conference 2019; Pedro Ramalhete
	- https://www.youtube.com/watch?v=oDfr9w9p8XY
	- https://2019.hydraconf.com/2019/talks/1jwmdzkmjcalsclwavttxk
- Weak Memory Concurrency in C/C++11
	- Hydra: Distributed Computing Conference 2019; Ori Lahav
	- https://www.youtube.com/watch?v=mOqu8vGSysc
	- http://www.cs.tau.ac.il/~orilahav/papers/lahav_c11.pdf
	- https://2019.hydraconf.com/2019/talks/143pbdxfvijthb8rg3qk6e

### 2018

- A “Post-ISA” Era in Computer Systems: Challenges and Opportunities
	- PLDI 2018; Margaret Martonosi
	- https://pldi18.sigplan.org/event/pldi-2018-pldi-invited-speakers-margaret-martonosi-talk
- The C++ Execution Model
	- CppCon 2018; Bryce Adelstein Lelbach
	- https://www.youtube.com/watch?v=FJIn1YhPJJc

### 2017

- C++ atomics, from basic to advanced. What do they really do?
	- CppCon 2017; Fedor Pikus
	- https://youtu.be/ZQFzMfHIxng
- An Interesting Lock-free Queue - Part 2 of N
	- CppCon 2017; Tony Van Eerd
	- https://github.com/CppCon/CppCon2017/tree/master/Presentations/A%20Not%20So%20Complicated%20Lockfree%20Queue
	- https://www.youtube.com/watch?v=HP2InVqgBFM
- Coherence, Consistency, & Déjà vu: Memory Hierarchies in the Era of Specialization
	- HiPEAC 2017; Sarita Adve
	- Slides: http://rsim.cs.illinois.edu/Talks/17-hipeac.pdf
	- Video: https://www.youtube.com/watch?v=kjFjL_vTUWU
- Multicore Synchronization: The Lesser-Known Primitives
	- C++Now 2017; Samy Bahra
	- https://www.youtube.com/watch?v=OfTy3ymDwWE
	- http://cppcast.com/2017/08/samy-bahra/

### 2016

- The speed of concurrency (is lock-free faster?)
	- CppCon 2016; Fedor Pikus
	- Slides: https://github.com/CppCon/CppCon2016/tree/master/Presentations/The%20speed%20of%20concurrency
	- Video: https://channel9.msdn.com/Events/CPP/CppCon-2016/CppCon-2016-Fedor-Pikus-The-speed-of-concurrency-is-lock-free-faster
	- Video: https://www.youtube.com/watch?v=9hJkWwHDDxs

### 2015

- Atomic Counters or A Lesson on Performance and Hardware Concurrency
	- ACCU 2015
	- Info: http://accu.org/index.php/conferences/accu_conference_2015/accu2015_sessions#atomic_counters_or_a_lesson_on_performance_and_hardware_concurrency
	- Slides: https://accu.org/conf-docs/PDFs_2015/DetlefVollmann-Atomic%20Counters.pdf
	- Slides: http://www.vollmann.ch/en/presentations/atomic-counters-accu-2015.pdf
	- Video: http://www.infoq.com/presentations/atomic-counters
- Safety: off. How not to shoot yourself in the foot with C++ atomics
	- ACCU 2015
	- Info: http://accu.org/index.php/conferences/accu_conference_2015/accu2015_sessions#safety-off._how_not_to_shoot_yourself_in_the_foot_with_c_atomics
	- Slides: https://accu.org/conf-docs/PDFs_2015/AnthonyWilliams-safety_off.pdf
- The Dos and Don'ts of Multithreading
	- ACCU 2015
	- Info: http://accu.org/index.php/conferences/accu_conference_2015/accu2015_sessions#the_dos_and_don_ts_of_multithreading
	- Slides: https://accu.org/conf-docs/PDFs_2015/HubertMatthews-Multithreading%20Dos%20And%20Donts.pdf
	- Video: http://www.infoq.com/presentations/multithreading
	- Note: more on atomics & memory ordering compared to the NDC 2014 version.
- Live Lock-Free or Deadlock (Practical Lock-free Programming)
	- CppCon 2015; Fedor Pikus
	- Part 1: https://www.youtube.com/watch?v=lVBvHbJsg5Y
	- Part 2: https://www.youtube.com/watch?v=1obZeHnAwz4
- C++11/14/17 Atomics the Deep dive: the gory details, before the story consumes you!
	- CppCon 2015: Michael Wong
	- https://www.youtube.com/watch?v=DS2m7T6NKZQ
- C++ Atomics: The Sad Story of memory_order_consume: A Happy Ending At Last?
	- CppCon 2015: Paul E. McKenney
	- https://www.youtube.com/watch?v=ZrNQKpOypqU
- How to make your data structures wait-free for reads
	- CppCon 2015; Pedro Ramalhete
	- https://www.youtube.com/watch?v=FtaD0maxwec
- C++ in the Audio Industry
	- CppCon 2015; Timur Doumler
	- https://www.youtube.com/watch?v=boPEO2auJj4
- Defining Correctness Conditions for Concurrent Objects in Multicore Architectures
	- ECOOP 2015; Brijesh Dongol
	- https://www.youtube.com/watch?v=PDQXpKE_Kao
- C Concurrency: Still Tricky
	- LLVM Developers' Meeting 2015; Francesco Zappa Nardelli
	- Video: https://www.youtube.com/watch?v=g8DUN8-AKgs
	- Slides: http://llvm.org/devmtg/2015-04/slides/CConcurrency_EuroLLVM2015.pdf
- Memory Access Ordering in Complex Embedded Systems
	- NDC 2015: Chris Shore
	- https://vimeo.com/131637104

### 2014

- Lockless programming
	- Atmosphere 2014; Tomasz Baranski
	- https://www.youtube.com/watch?v=JUeaCfhwvHE
- Lock-Free Programming (or, Juggling Razor Blades)
	- CppCon 2014; Herb Sutter
	- http://herbsutter.com/2014/10/18/my-cppcon-talks-2/
	- Part 1: Lazy initialization with DCL vs. call_once vs. function local statics, and lock-free mailbox algorithms
		- http://youtu.be/c1gO9aB9nbs
	- Part 2: Lock-free linked lists, the ABA problem, and atomic smart pointers
		- http://youtu.be/CmxkPChOcvw
- How Ubisoft Develops Games for Multicore - Before and After C++11
	- CppCon 2014; Jeff Preshing
	- Code: https://gist.github.com/preshing/4d28abad8da4e40cb1d4
	- Video: https://www.youtube.com/watch?v=X1T3IQ4N-3g
- C++ Memory Model Meets High-Update-Rate Data Structures
	- CppCon 2014; Paul E. McKenney
	- https://www.youtube.com/watch?v=1Q-RH2tiyt0
- Lock-free by Example
	- CppCon 2014; Tony Van Eerd
	- https://www.youtube.com/watch?v=Xf35TLFKiO8
	- https://channel9.msdn.com/Events/CPP/C-PP-Con-2014/Lock-free-by-Example
- Blowing up the (C++11) atomic barrier - Optimizing C++11 atomics in LLVM
	- LLVM Developers' Meeting 2014; Robin Morisset
	- Slides: http://llvm.org/devmtg/2014-10/Slides/Morisset-AtomicsPresentation.pdf
	- Video (Google Tech Talk): https://www.youtube.com/watch?v=hE4HW1Y2Dao
	- Video: https://www.youtube.com/watch?v=cDM6Gr_XzGI
- The C++ Memory Model
	- Meeting C++ 2014; Valentin Ziegler
	- https://www.youtube.com/watch?v=gpsz8sc6mNU
- The Dos and Don'ts of Multithreaded Programming
	- NDC 2014; Hubert Matthews
	- https://vimeo.com/113725137
- The C++ memory model
	- NDC 2014; Mike Long
	- https://vimeo.com/97419179
	- https://github.com/meekrosoft/cppmemmodel
	- Slides: https://meekrosoft.github.io/cppmemmodel/

### 2013

- Shattering Illusions in Lock-Free Worlds: Compiler/Hardware Behaviors OSes/VMs
	- Black Hat USA 2013; Marc Blanchou
	- https://www.youtube.com/watch?v=wYFADkO-ZsA
- Low Level Threading with C++11
	- C++Now! 2013; Tony Van Eerd
	- https://www.youtube.com/watch?v=dKLAwNaNvAY
- std::atomic explained
	- C++ Wroclaw 0x03 (2013); Volodymyr Volkov
	- https://vimeo.com/80599339
- Everything you always wanted to know about synchronization but were afraid to ask
	- Symposium on Operating Systems Principles (SOSP) 2013
	- Tudor David, Rachid Guerraoui, and Vasileios Trigonakis
	- Video: https://www.youtube.com/watch?v=Dfagg__PuKw
	- Paper: http://sigops.org/sosp/sosp13/papers/p33-david.pdf

### 2012

- atomic Weapons: The C++ Memory Model and Modern Hardware
	- C++ and Beyond 2012; Herb Sutter
	- https://herbsutter.com/2013/02/11/atomic-weapons-the-c-memory-model-and-modern-hardware/
	- https://channel9.msdn.com/Shows/Going+Deep/Cpp-and-Beyond-2012-Herb-Sutter-atomic-Weapons-1-of-2
	- https://channel9.msdn.com/Shows/Going+Deep/Cpp-and-Beyond-2012-Herb-Sutter-atomic-Weapons-2-of-2
- Don't Try This at Work -- Low Level Threading with C++11
	- C++Now! 2012; Tony Van Eerd
	- https://www.youtube.com/watch?v=b9wWC5uSqLE&list=PL_AKIMJc4roWXECUOVFsSTn6zs-145shM&index=20
- Threads and Shared Variables in C++11
	- GoingNative 2012; Hans Boehm
	- https://channel9.msdn.com/Events/GoingNative/GoingNative-2012/Threads-and-Shared-Variables-in-C-11
- C++11 Threads Surprises
	- 2012 Hans-J. Boehm
	- Slides: https://parasol.tamu.edu/bjarnefest/program/boehm-slides.pdf
	- Video (slides not visible):
		- https://www.youtube.com/watch?v=UWx4EA2uBzs
		- https://www.youtube.com/watch?v=TnCWTPuWzIk

### 2011

- Lockfree Programming Part 2: Data Structures
	- BoostCon 2011; Tony Van Eerd
	- https://www.youtube.com/watch?v=O4Jdq4PtfPA
	- (Part 2: continuing from where BoostCon 2010 left off)
	- Slides: https://github.com/boostcon/2011_presentations/raw/master/wed/lockfree_2011_slides.pdf

### 2010

- The Basics of Lock-free Programming
	- BoostCon 2010; Tony Van Eerd
	- https://www.youtube.com/watch?v=LbOB_moUa94
