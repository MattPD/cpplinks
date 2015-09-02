C++ links: atomics, lock free, memory model

# Blogs: Posts and Series

Anthony Williams
https://www.justsoftwaresolutions.co.uk/threading/implementing_dekkers_algorithm_with_fences.html
https://www.justsoftwaresolutions.co.uk/threading/memory_models_and_synchronization.html
https://www.justsoftwaresolutions.co.uk/threading/intel-memory-ordering-and-c++-memory-model.html
https://www.justsoftwaresolutions.co.uk/threading/intel-and-amd-memory-ordering-defined.html
https://www.justsoftwaresolutions.co.uk/threading/non_blocking_lock_free_and_wait_free.html

Bartosz Milewski
http://bartoszmilewski.com/2008/11/11/who-ordered-sequential-consistency/
http://bartoszmilewski.com/2008/12/01/c-atomics-and-memory-ordering/
https://corensic.wordpress.com/category/sequential-consistency/

Comparison: Lockless programming with atomics in C++ 11 vs. mutex and RW-locks
https://www.arangodb.com/2015/02/comparing-atomic-mutex-rwlocks/

Fast Bounded-Concurrency Hash Tables
http://backtrace.io/blog/blog/2015/03/13/workload-specialization/

Jeff Preshing
http://preshing.com/20111118/locks-arent-slow-lock-contention-is/
http://preshing.com/20120515/memory-reordering-caught-in-the-act/
http://preshing.com/20120612/an-introduction-to-lock-free-programming/
http://preshing.com/20120625/memory-ordering-at-compile-time/
http://preshing.com/20120710/memory-barriers-are-like-source-control-operations/
http://preshing.com/20120913/acquire-and-release-semantics/
http://preshing.com/20120930/weak-vs-strong-memory-models/
http://preshing.com/20121019/this-is-why-they-call-it-a-weakly-ordered-cpu/
http://preshing.com/20130505/introducing-mintomic-a-small-portable-lock-free-api/
http://preshing.com/20130529/a-lock-free-linear-search/
http://preshing.com/20130605/the-worlds-simplest-lock-free-hash-table/
http://preshing.com/20130618/atomic-vs-non-atomic-operations
http://preshing.com/20130702/the-happens-before-relation/
http://preshing.com/20130823/the-synchronizes-with-relation/
http://preshing.com/20130922/acquire-and-release-fences/
http://preshing.com/20130930/double-checked-locking-is-fixed-in-cpp11/
http://preshing.com/20131125/acquire-and-release-fences-dont-work-the-way-youd-expect/
http://preshing.com/20140709/the-purpose-of-memory_order_consume-in-cpp11/
http://preshing.com/20141124/fixing-gccs-implementation-of-memory_order_consume/
http://preshing.com/20150402/you-can-do-any-kind-of-atomic-read-modify-write-operation/

Kukuryku Hub Series
http://kukuruku.co/hub/cpp/lock-free-data-structures-introduction
http://kukuruku.co/hub/cpp/lock-free-data-structures-basics-atomicity-and-atomic-primitives
http://kukuruku.co/hub/cpp/lock-free-data-structures-memory-model-part-3
http://kukuruku.co/hub/cpp/lock-free-data-structures-the-inside-memory-management-schemes
http://kukuruku.co/hub/cpp/lock-free-data-structures-the-inside-rcu
http://kukuruku.co/hub/cpp/lock-free-data-structures-the-evolution-of-a-stack
http://kukuruku.co/hub/cpp/lock-free-data-structures-yet-another-treatise
http://kukuruku.co/hub/cpp/lock-free-data-structures-exploring-queues

"Moody Camel" Series:
http://moodycamel.com/blog/2013/a-fast-lock-free-queue-for-c++
http://moodycamel.com/blog/2014/a-fast-general-purpose-lock-free-queue-for-c++
http://moodycamel.com/blog/2014/detailed-design-of-a-lock-free-queue
http://moodycamel.com/blog/2014/solving-the-aba-problem-for-lock-free-free-lists

PSA: you should use WTF::Lock and WTF::Condition instead of WTF::SpinLock, WTF::Mutex, WTF::ThreadCondition, std::mutex, std::condition_variable, or std::condition_variable_any
http://permalink.gmane.org/gmane.os.opendarwin.webkit.devel/27578

The difficulty of lock-free programming: a bug in lockfree stack
http://mdf356.blogspot.com/2015/06/the-difficulty-of-lock-free-programming.html

Trip Report: Ad-Hoc Meeting on Threads in C++
http://www.artima.com/cppsource/threads_meeting.html

# Courses

CS/ECE 7810 Advanced Computer Architecture 
http://www.eng.utah.edu/~cs7810/
Lecture 11: Consistency Models: [Slides (pdf)](http://www.eng.utah.edu/~cs7810/pres/14-7810-11.pdf)
YouTube videos on consistency models:
[YouTube Video 68](http://www.youtube.com/watch?v=VfIeD_B4YhM) (Example multi-threaded programs and sequentially consistent results)
[YouTube Video 69](http://www.youtube.com/watch?v=DzGk1FXrQEo) (Hardware support for sequential consistency, example of how SC is violated if program order is violated)
[YouTube Video 70](http://www.youtube.com/watch?v=AOhRBI7GyZU) (Example on how a coherence protocol may violate write atomicity and sequential consistency, hardware support for sequential consistency, safe optimizations to speed up the hardware)
[YouTube Video 71](http://www.youtube.com/watch?v=JjRnHP_u-aY) (A hardware-software approach to improving performance with relaxed consistency models and fences)

# Papers

## Papers - Data Structures

Shared memory consistency models tutorial (Adve and Gharachorloo) 
http://www.hpl.hp.com/techreports/Compaq-DEC/WRL-95-7.pdf

Treiber’s lock-free stack
R. Treiber. Systems programming: Coping with parallelism. Technical report, IBM Almaden Research Center, 1986.
http://domino.research.ibm.com/library/cyberdig.nsf/papers/58319A2ED2B1078985257003004617EF/$File/rj5118.pdf

Keir Fraser. Practical lock freedom. Cambridge University Technical Report UCAM-CL-TR-579.
https://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-579.pdf
Practical lock-free data structures
https://www.cl.cam.ac.uk/research/srg/netos/projects/lock-free/

## Papers - Implementation

Common Compiler Optimisations are Invalid in the C11 Memory Model and what we can do about it
http://www.di.ens.fr/~zappa/readings/c11comp.pdf

N4455 No Sane Compiler Would Optimize Atomics
http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4455.html

## Papers - Memory Model

AutoMO: Automatic Inference of Memory Order Parameters for C/C++11 | SPLASH 2015 OOPSLA
http://plrg.eecs.uci.edu/publications/oopsla15inference.pdf

Common Compiler Optimisations are Invalid in the C11 Memory Model and what we can do about it 
http://plv.mpi-sws.org/c11comp/popl15.pdf

C++ Memory Model, Martin Kempf
http://wiki.ifs.hsr.ch/SemProgAnTr/files/CppMemoryModel_26_12_12.pdf

Foundations of the C++ Concurrency Memory Model
http://rsim.cs.illinois.edu/Pubs/08PLDI.pdf

Memory Barriers: a Hardware View for Software Hackers
http://irl.cs.ucla.edu/~yingdi/web/paperreading/whymb.2010.06.07c.pdf

Memory Model = Instruction Reordering + Store Atomicity
http://csg.csail.mit.edu/pubs/memos/Memo-493/memo-493.pdf

Memory Models: A Case for Rethinking Parallel Languages and Hardware
http://cacm.acm.org/magazines/2010/8/96610-memory-models-a-case-for-rethinking-parallel-languages-and-hardware/fulltext

Programming with Threads: Questions Frequently Asked by C and C++ Programmers
http://www.hboehm.info/c++mm/user-faq.html

Shared Memory Consistency Models: A Tutorial
http://rsim.cs.illinois.edu/~sadve/Publications/computer96.pdf

Simple and Efficient Semantics for Concurrent Programming Languages
http://web.cs.ucla.edu/~todd/research/memmodels.html
- The Silently Shifting Semicolon (SNAPL 2015) - http://web.cs.ucla.edu/~todd/research/snapl15.pdf - proposes the designation "Weak DRF0 (WDRF0)" for the C++ memory model:
"C/C++ has settled for a memory model weaker than DRF0, which we call Weak DRF0 (WDRF0). DRF programs are not guaranteed SC semantics in WDRF0. To get SC, programmers have to additionally avoid the use of the so-called low-level atomic primitives. The weak semantics of DRF programs in C++ is similar in complexity to the semantics of non-DRF programs in Java."

The x86 Memory Model
http://www.msully.net/blog/2015/02/25/the-x86-memory-model/

Threads Basics, HP Labs Technical Report 2009-259.
Updated: First Published: Nov. 17, 2008; Last revised: January 16, 2011 
http://www.hboehm.info/c++mm/threadsintro.html

Threads Cannot be Implemented as a Library
http://www.hpl.hp.com/techreports/2004/HPL-2004-209.pdf
LtU:  http://lambda-the-ultimate.org/node/950

x86-TSO: A Rigorous and Usable Programmer’s Model for x86 Multiprocessors
https://www.cl.cam.ac.uk/~pes20/weakmemory/cacm.pdf

You Don't Know Jack about Shared Variables of Memory Models: Data Races are Evil
https://queue.acm.org/detail.cfm?id=2088916

# References, Resources

1024cores
http://www.1024cores.net/
http://www.1024cores.net/home/lock-free-algorithms

A Primer on Memory Consistency and Cache Coherence
http://www.morganclaypool.com/doi/abs/10.2200/S00346ED1V01Y201104CAC016?journalCode=cac

Atomics, Madhusudhan Srikkanth
http://www.mssrikkanth.com/index.php/c/c-11-14/concurrency/62-atomics

c++ atomic lib : rules for implementation
http://david.jobet.free.fr/wiclear-blog/index.php?title=2010-10-17-c%2B%2B-atomic-lib-impl-rules

C++11 Language Extensions — Concurrency
https://isocpp.org/wiki/faq/cpp11-language-concurrency

C++11 Standard Library Extensions — Concurrency
https://isocpp.org/wiki/faq/cpp11-library-concurrency

C/C++11 mappings to processors
C/C++11 atomic operations to x86, PowerPC, ARMv7, ARMv8, and Itanium instruction sequences
https://www.cl.cam.ac.uk/~pes20/cpp/cpp0xmappings.html

Concurrency memory model compiler consequences
http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2007/n2338.html

GCC Wiki - Atomic: https://gcc.gnu.org/wiki/Atomic/
GCC Wiki - The C++11 Memory Model and GCC: https://gcc.gnu.org/wiki/Atomic/GCCMM

Is Parallel Programming Hard, And If So, What Can You Do About It?, Paul E. McKenney
http://www.rdrop.com/~paulmck/
https://kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html

Linux kernel memory barriers
https://www.kernel.org/doc/Documentation/memory-barriers.txt

LLVM Atomic Instructions and Concurrency Guide
http://llvm.org/docs/Atomics.html

Lock-free stuff
http://david.jobet.free.fr/wiclear-blog/?fr/2010-01-04-lock-free-stuff

Memory model
http://en.cppreference.com/w/cpp/language/memory_model

N1276: A Less Formal Explanation of the Proposed C++ Concurrency Memory Model
http://www.open-std.org/jtc1/sc22/wg14/www/docs/n1276.htm

Relaxed-Memory Concurrency
https://www.cl.cam.ac.uk/~pes20/weakmemory/

Some notes on lock-free and wait-free algorithms
http://www.rossbencina.com/code/lockfree

Threads and memory model for C++
http://hboehm.info/c++mm/

Why the "volatile" type class should not be used
https://www.kernel.org/doc/Documentation/volatile-considered-harmful.txt

# Slides

Concurrency Kit talks
http://concurrencykit.org/slides.html
Lock-Free Algorithms: An Introduction, Introduction to Lock-Free Algorithms: Through a case study, Safe Memory Reclamation: Epoch Reclamation, Towards accessible non-blocking technology for C, Fast Bounded-Concurrency Hash Tables

Foundations of the C++ Concurrency Memory Model
http://www.cs.rice.edu/~johnmc/comp522/lecture-notes/COMP522-2014-Lecture11-C++-MemoryModel.pdf

"Memory Consistency Models", Sarita Adve
http://rsim.cs.uiuc.edu/~sadve/JavaWorkshop00/talk.pdf

Memory Management in C++14 and Beyond
Chicago C++ Meetup July 7, 2015
Info: http://www.meetup.com/Chicago-C-CPP-Users-Group/events/223318263/
Slides: http://ccug.chicago.il.us/Spertus7jul2015.pdf

Memory models: Making sense of thread level parallelism and shared memory access
http://www.cs.rice.edu/~johnmc/comp522/lecture-notes/COMP522-2014-Lecture8-MemoryModels.pdf

# Software, Tools

Boost.Lockfree
http://www.boost.org/doc/libs/release/doc/html/lockfree.html

CDS C++ library
https://github.com/khizmax/libcds
The Concurrent Data Structures (CDS) library is a collection of concurrent containers that don't require external (manual) synchronization for shared access, and safe memory reclamation (SMR) algorithms like Hazard Pointer and user-space RCU. CDS is mostly header-only template library. Only SMR core implementation is segregated to .so/.dll file.

CDSChecker: A Model Checker for C11 and C++11 Atomics
http://demsky.eecs.uci.edu/c11modelchecker.html
http://plrg.eecs.uci.edu/publications/c11modelcheck.pdf

Concurrency Kit
Concurrency primitives, safe memory reclamation mechanisms and non-blocking (including lock-free) data structures designed to aid in the research, design and implementation of high performance concurrent systems.
https://github.com/concurrencykit/ck

CppMem: Interactive C/C++ memory model
http://svr-pes20-cppmem.cl.cam.ac.uk/cppmem/

moodycamel::ConcurrentQueue (MPMC): https://github.com/cameron314/concurrentqueue
moodycamel::ReaderWriterQueue (SPSC): SPSC: https://github.com/cameron314/readerwriterqueue
http://moodycamel.com/blog/2013/a-fast-lock-free-queue-for-c++
http://moodycamel.com/blog/2014/a-fast-general-purpose-lock-free-queue-for-c++
http://moodycamel.com/blog/2014/detailed-design-of-a-lock-free-queue
http://moodycamel.com/blog/2014/solving-the-aba-problem-for-lock-free-free-lists

Relacy Race Detector 
http://www.1024cores.net/home/relacy-race-detector

# Talks, Videos

ACCU 2015: Atomic Counters or A Lesson on Performance and Hardware Concurrency
Info: http://accu.org/index.php/conferences/accu_conference_2015/accu2015_sessions#atomic_counters_or_a_lesson_on_performance_and_hardware_concurrency
Slides: http://accu.org/content/conf2015/DetlefVollmann-Atomic%20Counters.pdf
Slides: http://www.vollmann.ch/en/presentations/atomic-counters-accu-2015.pdf
Video: http://www.infoq.com/presentations/atomic-counters

ACCU 2015: Safety: off. How not to shoot yourself in the foot with C++ atomics
Info: http://accu.org/index.php/conferences/accu_conference_2015/accu2015_sessions#safety-off._how_not_to_shoot_yourself_in_the_foot_with_c_atomics
Slides: http://accu.org/content/conf2015/AnthonyWilliams-safety_off.pdf

ACCU 2015: The Dos and Don'ts of Multithreading
Info: http://accu.org/index.php/conferences/accu_conference_2015/accu2015_sessions#the_dos_and_don_ts_of_multithreading
Slides: http://accu.org/content/conf2015/HubertMatthews-Multithreading%20Dos%20And%20Donts.pdf
Video: http://www.infoq.com/presentations/multithreading
Note: more on atomics & memory ordering compared to the NDC 2014 version.

Atmosphere 2014: Lockless programming - Tomasz Baranski
https://www.youtube.com/watch?v=JUeaCfhwvHE

Black Hat USA 2013 - Shattering Illusions in Lock-Free Worlds: Compiler/Hardware Behaviors OSes/VMs
https://www.youtube.com/watch?v=wYFADkO-ZsA

BoostCon 2010: Tony Van Eerd: The Basics of Lock-free Programming
https://www.youtube.com/watch?v=LbOB_moUa94

BoostCon 2010: Tony Van Eerd: Lockfree Programming Part 2: Data Structures
https://www.youtube.com/watch?v=O4Jdq4PtfPA
(Part 2: continuing from where BoostCon 2010 left off)
Slides: https://github.com/boostcon/2011_presentations/raw/master/wed/lockfree_2011_slides.pdf

C++ and Beyond 2012: atomic Weapons: The C++ Memory Model and Modern Hardware
https://channel9.msdn.com/Shows/Going+Deep/Cpp-and-Beyond-2012-Herb-Sutter-atomic-Weapons-1-of-2
https://channel9.msdn.com/Shows/Going+Deep/Cpp-and-Beyond-2012-Herb-Sutter-atomic-Weapons-2-of-2

C++Now! 2013 Tony Van Eerd: Low Level Threading with C++11
https://www.youtube.com/watch?v=dKLAwNaNvAY

C++ Wroclaw 0x03: Volodymyr Volkov - std::atomic explained
http://www.cppwroclaw.pl/dokuwiki/spotkania/003/info
https://vimeo.com/80599339

CppCon 2014: Herb Sutter, "Lock-Free Programming (or, Juggling Razor Blades)"
http://herbsutter.com/2014/10/18/my-cppcon-talks-2/
Part 1: http://youtu.be/c1gO9aB9nbs - Lazy initialization with DCL vs. call_once vs. function local statics, and lock-free mailbox algorithms
Part 2: http://youtu.be/CmxkPChOcvw - Lock-free linked lists, the ABA problem, and atomic smart pointers

CppCon 2014: Jeff Preshing, "How Ubisoft Develops Games for Multicore - Before and After C++11"
Code: https://gist.github.com/preshing/4d28abad8da4e40cb1d4
Video: https://www.youtube.com/watch?v=X1T3IQ4N-3g

CppCon 2014: Paul E. McKenney, "C++ Memory Model Meets High-Update-Rate Data Structures"
https://www.youtube.com/watch?v=1Q-RH2tiyt0

CppCon 2014: Tony Van Eerd, "Lock-free by Example"
https://www.youtube.com/watch?v=Xf35TLFKiO8
https://channel9.msdn.com/Events/CPP/C-PP-Con-2014/Lock-free-by-Example

ECOOP 2015: Brijesh Dongol - "Defining Correctness Conditions for Concurrent Objects in Multicore Architectures"
https://www.youtube.com/watch?v=PDQXpKE_Kao

GoingNative 2012: Hans Boehm, "Threads and Shared Variables in C++11"
https://channel9.msdn.com/Events/GoingNative/GoingNative-2012/Threads-and-Shared-Variables-in-C-11

LLVM Developers' Meeting 2014: Blowing up the (C++11) atomic barrier - Optimizing C++11 atomics in LLVM
Slides: http://llvm.org/devmtg/2014-10/Slides/Morisset-AtomicsPresentation.pdf
Video (Google Tech Talk): https://www.youtube.com/watch?v=hE4HW1Y2Dao
Video (720p): http://llvm.org/devmtg/2014-10/Videos/Blowing%20up%20the%20Atomic%20Barrier-720.mov
Video (360p): http://llvm.org/devmtg/2014-10/Videos/Blowing%20up%20the%20Atomic%20Barrier-360.mov

LLVM Developers' Meeting 2015: European LLVM Conference
Keynote: "C Concurrency: Still Tricky", Francesco Zappa Nardelli
Video HD: http://llvm.org/devmtg/2015-04/Videos/HD/Day%201/Francesco%20Zappa%20Nardelli%20(keynote).mp4
Video SD: http://llvm.org/devmtg/2015-04/Videos/SD/Day%201/Francesco%20Zappa%20Nardelli%20(keynote)_1.mp4
Slides: http://llvm.org/devmtg/2015-04/slides/CConcurrency_EuroLLVM2015.pdf

Hans-J. Boehm: C++11 Threads Surprises
Slides: https://parasol.tamu.edu/bjarnefest/program/boehm-slides.PDFs
Video (slides not visible): https://www.youtube.com/watch?v=UWx4EA2uBzs / https://www.youtube.com/watch?v=TnCWTPuWzIk

Meeting C++ 2014: The C++ Memory Model - Valentin Ziegler
https://www.youtube.com/watch?v=gpsz8sc6mNU

NDC 2014: Hubert Matthews - The Dos and Don'ts of Multithreaded Programming
https://vimeo.com/113725137

NDC 2014: Mike Long - The C++ memory model
https://vimeo.com/97419179
https://www.youtube.com/watch?v=BiLX7n_z9s4
https://github.com/meekrosoft/cppmemmodel
Slides: https://meekrosoft.github.io/cppmemmodel/

NDC 2015: Chris Shore - Memory Access Ordering in Complex Embedded Systems
https://vimeo.com/131637104
