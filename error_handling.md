# [C++ links](README.md): error handling

# Contents

- [Readings](#readings): [Blogs](#blogs-posts-and-series), [Documentation](#documentation), [Papers](#papers), [References](#references), [StackOverflow](#stackoverflow-questions)
- [Software](#software): [Benchmarks](#benchmarks), [Libraries](#libraries), [Tools](#tools)
- [Talks](#talks): [2022](#2022), [2021](#2021), [2020](#2020), [2019](#2019), [2018](#2018), [2017](#2017), [2016](#2016), [2015](#2015), [2014](#2014)

---

# Readings

## Blogs: Posts and Series

- Akshay Kumar
	- How McSema Handles C++ Exceptions - https://blog.trailofbits.com/2019/01/21/how-mcsema-handles-c-exceptions/
- Andrii Batyiev - Size cost of C++ exception handling on embedded platform
	- Uses microbenchmarking to examine the effect of exceptions on code size.
	- https://andriidevel.blogspot.co.uk/2016/05/size-cost-of-c-exception-handling-on.html
- Andrzej Krzemieński
	- https://akrzemi1.wordpress.com/2011/09/21/destructors-that-throw/
	- https://akrzemi1.wordpress.com/2012/11/14/not-using-stdthread/
	- https://akrzemi1.wordpress.com/2013/07/18/cs-best-feature/
	- https://akrzemi1.wordpress.com/2013/08/20/noexcept-destructors/
	- https://akrzemi1.wordpress.com/2014/02/12/find-the-bug/
	- https://akrzemi1.wordpress.com/2014/03/13/find-the-bug-comments/
	- https://akrzemi1.wordpress.com/2014/04/24/noexcept-what-for/
	- https://akrzemi1.wordpress.com/2014/09/19/destructors-2-use-cases/
	- Handling errors is canceling operations - https://akrzemi1.wordpress.com/2019/04/25/handling-errors-is-canceling-operations/
	- Operation cancelling and std::fstream - https://akrzemi1.wordpress.com/2019/05/23/operation-cancelling-and-stdfstream/
	- error codes
		- Your own error code - https://akrzemi1.wordpress.com/2017/07/12/your-own-error-code/
		- Your own error condition - https://akrzemi1.wordpress.com/2017/08/12/your-own-error-condition/
		- Using error codes effectively - https://akrzemi1.wordpress.com/2017/09/04/using-error-codes-effectively/
		- error codes — some clarifications - https://akrzemi1.wordpress.com/2017/10/14/error-codes-some-clarifications/
- Arthur O’Dwyer - https://quuxplusone.github.io/blog/tags/#exception-handling
	- Copy Elision in Throw Statements - https://quuxplusone.github.io/blog/2018/04/09/elision-in-throw-statements/
	- The Lakos Rule - https://quuxplusone.github.io/blog/2018/04/25/the-lakos-rule/
	- Data race when catching by non-const reference - https://quuxplusone.github.io/blog/2018/09/16/data-race-when-catch-by-nonconst-reference/
	- MSVC can’t handle move-only exception types - https://quuxplusone.github.io/blog/2019/05/11/msvc-what-are-you-doing/
- Boris Kolpackov
	- Throwing Destructors - https://www.kolpackov.net/projects/c++/eh/dtor-1.xhtml
- "Buckaroo" - Error Handling in C++ or: Why You Should Use Eithers in Favor of Exceptions and Error-codes
	- Presents some reasons to use Eithers (A.K.A. `std::expected`) instead of other alternatives.
	- https://hackernoon.com/error-handling-in-c-or-why-you-should-use-eithers-in-favor-of-exceptions-and-error-codes-f0640912eb45
- Chris Brumme - The Exception Model
	- Windows Structured Exception Handling (SEH) and C++ exceptions
	- https://blogs.msdn.microsoft.com/cbrumme/2003/10/01/the-exception-model/
	- https://cbrumme.dev/the-exception-model
- Edaqa Mortoray
	- Everything wrong with C++ exceptions
		- Does as it says on the tin.
		- https://mortoray.com/2012/04/02/everything-wrong-with-exceptions/
	- The true cost of zero cost exceptions
		- Examines how exceptions are implemented in order to show some of the real costs of them.
		- https://mortoray.com/2013/09/12/the-true-cost-of-zero-cost-exceptions/
- Eric Lippert
	- I Take Exception To That - https://ericlippert.com/2003/10/15/i-take-exception-to-that/
	- Long jumps considered way more harmful than exceptions - https://ericlippert.com/2003/10/16/long-jumps-considered-way-more-harmful-than-exceptions/
- Fangrui Song
	- C++ exception handling ABI
	- https://maskray.me/blog/2020-12-12-c++-exception-handling-abi
- Fredrik Dahlgren
	- Finding unhandled errors using CodeQL - https://blog.trailofbits.com/2022/01/11/finding-unhandled-errors-using-codeql/
- Herb Sutter - When and How to Use Exceptions
	- Guidelines on which cases to use exceptions for.
	- http://www.drdobbs.com/when-and-how-to-use-exceptions/184401836
- Hyungjoon Koo (Kevin)
	- ELF Sections for Exception Handling - https://dandylife.net/blog/archives/686
- Ian Lance Taylor
	- GCC Exception Frames - https://www.airs.com/blog/archives/166
	- Exception Destruction - https://www.airs.com/blog/archives/257
	- .eh_frame - https://www.airs.com/blog/archives/460
	- .eh_frame_hdr - https://www.airs.com/blog/archives/462
	- .gcc_except_table - https://www.airs.com/blog/archives/464
- Jason Robert Carey Patterson - Exception Handling Considered Harmful
	- A discussion of various problems with C++ exceptions.
	- http://www.lighterra.com/papers/exceptionsharmful/
- Jeff Preshing - The Cost of Enabling Exception Handling
	- Uses microbenchmarking and assembly analysis to examine the effect of enabling exceptions.
	- http://preshing.com/20110807/the-cost-of-enabling-exception-handling/
- Joe Duffy - The Error Model - http://joeduffyblog.com/2016/02/07/the-error-model/
- Jonathan Müller
	- Exceptions vs expected: Let's find a compromise
		- A look at finding a middle ground between exceptions and `std::expected` by examining what other languages provide.
		- https://foonathan.net/2017/12/exceptions-vs-expected/
	- How to handle errors in constructors without exceptions?
		- https://foonathan.net/2017/01/exceptions-constructor/
	- Error Handling Series
		- Part 1: Choosing the right error handling strategy - https://foonathan.net/2016/09/error-handling-strategy/
		- Part 2: Flexible error handling techniques in C++ - https://foonathan.net/2016/06/flexible-error-handling/
		- Part 3: How do I implement assertions? - https://foonathan.net/2016/09/assertions/
		- Part 4: Prevent precondition errors with the C++ type system - https://foonathan.net/2016/09/error-handling-types/
- Joseph M. Newcomer - Mythology in C++: Exceptions are Expensive
	- Microbenchmarks and assembly examinations to show that exceptions are not as expensive as many say.
	- http://www.flounder.com/exceptions.htm
- Joseph Mansfield - Exceptions, error codes, and assertions in C++
	- A high-level look at different error handling techniques and guidelines on when to use them.
	- http://josephmansfield.uk/articles/exceptions-error-codes-assertions-c++.html
- Jussi Pakkanen - Are exceptions slower than error objects
	- A series of microbenchmarks examining the relative cost of exceptions and error objects.
	- Are exceptions slower than error objects - http://nibblestew.blogspot.co.uk/2015/12/are-exceptions-slower-than-error-objects.html
	- Comparing executable size of C++ exceptions vs plain C error structs - http://nibblestew.blogspot.com/2016/12/comparing-executable-size-of-c.html
	- Measuring execution performance of C++ exceptions vs error codes - http://nibblestew.blogspot.com/2017/01/measuring-execution-performance-of-c.html
	- Testing exception vs error code behaviour with real world code - http://nibblestew.blogspot.com/2017/01/testing-exception-vs-error-code.html
- Lucian Teodorescu
‏	- Exceptional exploration
		- http://lucteo.ro/2018/03/18/exceptional-exploration-1/
		- http://lucteo.ro/2018/04/21/exception-exploration-2/
- Mike Hearn - What's wrong with exceptions? Nothing.
	- A defense of exceptions in general, but contains discussion on issues with C++'s implementation of them.
	- https://blog.plan99.net/what-s-wrong-with-exceptions-nothing-cee2ed0616
- Modi Mo
	- Making C++ Exception Handling Smaller On x64
	- https://devblogs.microsoft.com/cppblog/making-cpp-exception-handling-smaller-x64/
- Nemanja Trifunovic - C++ Exceptions: Pros and Cons
	- A discussion of the pros and cons of exceptions.
	- https://www.codeproject.com/Articles/38449/C-Exceptions-Pros-and-Cons
- Nicolas Brailovsky - C++ exceptions under the hood
	- A long series of posts looking at how C++ exceptions are actually implemented.
	- https://monkeywritescode.blogspot.com/2013/02/c-exceptions-under-hood.html
	- https://monkeywritescode.blogspot.com/2013/02/c-exceptions-under-hood-ii-tiny-abi.html
	- https://monkeywritescode.blogspot.com/2013/02/c-exceptions-under-hood-3-abi-to.html
	- https://monkeywritescode.blogspot.com/2013/02/c-exceptions-under-hood-4-catching-what.html
	- https://monkeywritescode.blogspot.com/2013/03/c-exceptions-under-hood-5-magic-around.html
	- https://monkeywritescode.blogspot.com/2013/03/c-exceptions-under-hood-6.html
	- https://monkeywritescode.blogspot.com/2013/03/c-exceptions-under-hood-7-nice.html
	- https://monkeywritescode.blogspot.com/2013/03/c-exceptions-under-hood-8-two-phase.html
	- https://monkeywritescode.blogspot.com/2013/04/c-exceptions-under-hood-9-catching-our.html
	- https://monkeywritescode.blogspot.com/2013/04/c-exceptions-under-hood-10-unwind-and.html
	- https://monkeywritescode.blogspot.com/2013/04/c-exceptions-under-hood-11-reading-cfi.html
	- https://monkeywritescode.blogspot.com/2013/04/c-exceptions-under-hood-12-and-suddenly.html
	- https://monkeywritescode.blogspot.com/2013/04/c-exceptions-under-hood-13-setting.html
	- https://monkeywritescode.blogspot.com/2013/04/c-exceptions-under-hood-14-multiple.html
	- https://monkeywritescode.blogspot.com/2013/05/c-exceptions-under-hood-15-finding.html
	- https://monkeywritescode.blogspot.com/2013/05/c-exceptions-under-hood-16-finding.html
	- https://monkeywritescode.blogspot.com/2013/05/c-exceptions-under-hood-17-reflecting.html
	- https://monkeywritescode.blogspot.com/2013/05/c-exceptions-under-hood-18-getting.html
	- https://monkeywritescode.blogspot.com/2013/05/c-exceptions-under-hood-19-getting.html
	- https://monkeywritescode.blogspot.com/2013/05/c-exceptions-under-hood-20-running.html
	- https://monkeywritescode.blogspot.com/2013/06/c-exceptions-under-hood-21-summary-and.html
	- https://monkeywritescode.blogspot.com/2013/06/c-exceptions-under-hood-appendix-i-true.html
	- https://monkeywritescode.blogspot.com/2013/06/c-exceptions-under-hood-appendix-ii.html
	- https://monkeywritescode.blogspot.com/2013/07/c-exceptions-under-hood-appendix-iii.html
- Patrice Roy - Exceptions in C++ and their Costs
	- A series of microbenchmarks looking at the tradeoffs between exceptions and error codes.
	- http://h-deb.clg.qc.ca/Sujets/Developpement/Exceptions-Costs.html
- Raymond Chen - The Old New Thing
	- Decoding the parameters of a thrown C++ exception (0xE06D7363)
		- https://devblogs.microsoft.com/oldnewthing/20100730-00/?p=13273
	- Decoding the parameters of a thrown C++ exception (0xE06D7363), revisited
		- https://devblogs.microsoft.com/oldnewthing/20160915-00/?p=94316
	- Can I throw a C++ exception from a structured exception?
		- https://devblogs.microsoft.com/oldnewthing/20170728-00/?p=96706
	- The sad history of the C++ throw(…) exception specifier
		- https://devblogs.microsoft.com/oldnewthing/20180928-00/?p=99855
	- If you want to terminate on an unexpected exception, then don’t sniff at every exception; just let the process terminate
		- https://devblogs.microsoft.com/oldnewthing/20191024-00/?p=103022
	- How can I handle both structured exceptions and C++ exceptions potentially coming from the same source?
		- https://devblogs.microsoft.com/oldnewthing/20200116-00/?p=103333
	- How can I turn a structured exception into a C++ exception without having to use /EHa, if I can constrain exactly where the structured exception is coming from?
		- https://devblogs.microsoft.com/oldnewthing/20200117-00/?p=103338
- Shane Kirk - C++ Exceptions: The Good, The Bad, And The Ugly
	- A discussion of the pros and cons of exceptions.
	- http://www.shanekirk.com/2015/06/c-exceptions-the-good-the-bad-and-the-ugly/
- Simon Brand - Functional exceptionless error-handling with optional and expected
	- Demonstrates how to use `optional` and `expected` with monadic extensions.
	- https://blog.tartanllama.xyz/optional-expected/
- Stafford Horne
	- Unwinding a Bug - How C++ Exceptions Work
	- http://stffrdhrn.github.io/software/toolchain/openrisc/2020/12/13/cxx-exception-unwinding.html
- Stefan Gränitz - Series: Rich Recoverable Error Handling with llvm::Expected<T>
	- Demonstrating the motivation and use of `llvm::Expected`.
	- https://weliveindetail.github.io/blog/post/2017/10/22/llvm-expected.html
	- https://github.com/weliveindetail/llvm-expected
	- Talk - C++ User Group Berlin 2017, September 19th: Rich Polymorphic Error Handling with llvm::Expected<T>
		- Slides (PDF): https://github.com/weliveindetail/talks/raw/master/Expectify.pdf
- Theofilos Petsios - C++ Exception Handling
	- Base ABI - http://web.archive.org/web/20141209000556/http://theofilos.cs.columbia.edu/blog/2013/09/22/base_abi/
	- Level II ABI - http://web.archive.org/web/20141209000543/http://theofilos.cs.columbia.edu/blog/2013/09/27/c-exception-handling-level-ii-abi/
	- Overview - http://web.archive.org/web/20141208235659/http://theofilos.cs.columbia.edu/blog/2013/09/30/c-exception-handling/
	- Stack Frame Destruction - http://web.archive.org/web/20141208235529/http://theofilos.cs.columbia.edu/blog/2013/10/03/c-exception-handling-stack-frame-destruction/
- Vittorio Romeo - Why choose sum types over exceptions?
	- A case study of somewhere you might want to choose sum types over exceptions, along with some more general guidance.
	- https://vittorioromeo.info/index/blog/adts_over_exceptions.html

## Documentation

- Dwarf2 Exception Handler HOWTO
	- https://gcc.gnu.org/wiki/Dwarf2EHNewbiesHowto
- Exception Handling in LLVM
	- http://llvm.org/docs/ExceptionHandling.html
- Exception Handling ABI for the ARM Architecture
	- http://infocenter.arm.com/help/topic/com.arm.doc.ihi0038b/IHI0038B_ehabi.pdf
- Itanium C++ ABI: Exception Handling
	- https://itanium-cxx-abi.github.io/cxx-abi/abi-eh.html
- MSVC
	- Exception handling in MSVC
		- https://docs.microsoft.com/en-us/cpp/cpp/exception-handling-in-visual-cpp
	- x64 exception handling
		- https://docs.microsoft.com/en-us/cpp/build/exception-handling-x64
- Using Exceptions in GCC
	- https://gcc.gnu.org/onlinedocs/libstdc++/manual/using_exceptions.html
- Windows SEH
	- Windows SEH Support in LLVM
		- https://github.com/tentzen/llvm-project/wiki
		- Hardware Exception Handling (MSVC -EHa) - Part 1: FE Clang implementation
			- https://reviews.llvm.org/D80344/
		- [llvm-dev] [RFC] [Windows SEH] Local_Unwind (Jumping out of a `_finally`) and -EHa (Hardware Exception Handling)
			- https://lists.llvm.org/pipermail/llvm-dev/2020-March/140541.html
		- [llvm-dev] [RFC] [Windows SEH][-EHa] Support Hardware Exception Handling
			- https://lists.llvm.org/pipermail/llvm-dev/2020-April/140991.html

## Papers

- A Study of the Applicability of Existing Exception-handling Techniques to Component-based Real-time Software Technology
	- ACM Transactions on Programming Languages and Systems (TOPLAS) 20(2) 1998
	- Jun Lang and David B. Stewart
	- https://doi.org/10.1145/276393.276395
	- http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.33.3400&rep=rep1&type=pdf
- A Study on the Effects of Exception Usage in Open-Source C++ Systems
	- 2019 Master Thesis; Kirsten Bradley
		- http://hdl.handle.net/10012/14714
	- Source Code Analysis and Manipulation (SCAM) 2019
		- Kirsten Bradley and Mike Godfrey
		- https://plg.uwaterloo.ca/~migod/papers/2019/scam19.pdf
	- Zelda - Zee Exception Length and Destination Analyzer
		- https://github.com/k10bradley/zelda
- C++ exception handling
	- IEEE Concurrency 8(4) 2000
	- Christophe De Dinechin
	- https://doi.org/10.1109/4434.895109
- C++ Exception Handling for IA64
	- USENIX Workshop on Industrial Experiences with Systems Software (WIESS) 2000
	- Christophe de Dinechin
	- http://www.usenix.org/events/wiess2000/dinechin.html
- Exception Handling: Issues and a Proposed Notation
	- Communications of the ACM (CACM) 18(12) 1975
	- John B. Goodenough
	- https://dl.acm.org/citation.cfm?id=361230
- Exception-Safety in Generic Components: Lessons Learned from Specifying Exception-Safety for the C++ Standard Library
	- David Abrahams
	- https://www.boost.org/community/exception_safety.html
	- Error and Exception Handling - https://www.boost.org/community/error_handling.html
- Exceptional Kernel: Using C++ Exceptions in the Linux Kernel
	- 2004
	- Halldór Ísak Gylfason, Gísli Hjálmtýsson
	- http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.100.7504
	- http://web.archive.org/http://netlab.ru.is/exception/KernelExceptions.pdf
	- C++ Exceptions & the Linux Kernel (2005)
		- http://www.drdobbs.com/cpp/c-exceptions-the-linux-kernel/229100146
- Generating Precise Error Specifications for C: A Zero Shot Learning Approach
	- SPLASH 2019 OOPSLA
	- Baijun Wu, John Peter Campora III, He Yi, Alexander Schlecht, Sheng Chen
	- https://dl.acm.org/citation.cfm?id=3360586
	- https://2019.splashcon.org/details/splash-2019-oopsla/44/Generating-Precise-Error-Specifications-for-C-A-Zero-Shot-Learning-Approach
	- https://bitbucket.org/plcacs/errorspec/src/master/
- Interprocedural exception analysis for C++
	- ECOOP 2011
	- Prakash Prabhu, Naoto Maeda, Gogul Balakrishnan, Franjo Ivančić, Aarti Gupta
	- https://www.semanticscholar.org/paper/Interprocedural-Exception-Analysis-for-C%2B%2B-Prabhu-Maeda/0aa41227da8f2db0af3afc67f71b7d9ebc09fb8c
	- http://pages.cs.wisc.edu/~bgogul/Research/Papers/ecoop11.html
- Low-cost Deterministic C++ Exceptions for Embedded Systems
	- Compiler Construction (CC) 2019
	- James Renwick, Tom Spink, Björn Frank
	- https://doi.org/10.1145/3302516.3307346
	- https://www.research.ed.ac.uk/portal/en/publications/lowcost-deterministic-c-exceptions-for-embedded-systems(2cfc59d5-fa95-45e0-83b2-46e51098cf1f).html
- Model checking C++ programs with exceptions
	- Science of Computer Programming, Volume 128, 2016
	- P. Ročkai, J. Barnat, L. Brim
	- https://dl.acm.org/citation.cfm?id=2974473
	- http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.671.6441&rep=rep1&type=pdf
	- https://journal.ub.tu-berlin.de/eceasst/article/view/983
- Optimizing away C++ exception handling
	- SIGPLAN Notices 33(8) 1998
	- Jonathan L. Schilling
	- https://dl.acm.org/citation.cfm?id=286390
	- http://www.ut.sco.com/developers/products/ehopt.pdf
- Path-Based Function Embedding and Its Application to Error-Handling Specification Mining
	- European Software Engineering Conference and Symposium on the Foundations of Software Engineering (ESEC/FSE) 2018
	- Daniel DeFreez, Aditya V. Thakur, Cindy Rubio-González
	- https://doi.org/10.1145/3236024.3236059
	- http://web.cs.ucdavis.edu/~rubio/includes/fse18.pdf
- Terse Exception Messages
	- Overload Journal #127, June 2015; Chris Oldwood
	- https://accu.org/index.php/journals/2110
- The Use of C++ Exception Handling Constructs: A Comprehensive Study
	- Source Code Analysis and Manipulation (SCAM) 2015
	- Rodrigo Bonifacio, Fausto Carvalho, Guilherme N. Ramos, Uira Kulesza, Roberta Coelho
	- https://doi.org/10.1109/SCAM.2015.7335398
	- https://web.archive.org/http://rbonifacio.net/papers/scam2015/rbonifacio-scam2015.pdf
- Using Off-the-Shelf Exception Support Components in C++ Verification
	- Software Quality, Reliability and Security (QRS) 2017
	- Vladimír Štill, Petr Ročkai, Jiří Barnat
	- https://arxiv.org/abs/1703.02394
	- https://divine.fi.muni.cz/2017/exceptions/

### Papers: Binary Analysis

- On the Impact of Exception Handling Compatibility on Binary Instrumentation
	- 2020 Workshop on Forming an Ecosystem Around Software Transformation (FEAST)
	- Soumyakant Priyadarshan, Huan Nguyen, R. Sekar
	- https://doi.org/10.1145/3411502.3418428
	- http://seclab.cs.stonybrook.edu/seclab/pubs/feast20.pdf
	- https://feastworkshop.github.io/2020/papers/ExHandling.pdf
- Towards Optimal Use of Exception Handling Information for Function Detection
	- Dependable Systems and Networks (DSN) 2021
	- Chengbin Pang, Ruotong Yu, Dongpeng Xu, Eric Koskinen, Georgios Portokalidis, Jun Xu
	- https://arxiv.org/abs/2104.03168
	- FETCH (Function dETection with exCeption Handling)
		- A fast and easy-to-use tool to find function entries from x86/x64 System-V binaries (stripped or not)
		- https://github.com/ruotongyu/FETCH
- Zipr++: Exceptional Binary Rewriting
	- [Forming an Ecosystem Around Software Transformation (FEAST) 2017](https://www.sigsac.org/ccs/CCS2017/toc/FEASTToC.html)
	- Jason Hiser, Anh Nguyen-Tuong, William Hawkins, Matthew McGill, Michele Co, Jack Davidson
	- https://dl.acm.org/citation.cfm?doid=3141235.3141240
	- https://tc.gtisc.gatech.edu/feast17/papers/p9-hiserA.pdf
	- Section 2.2 - EH Frame IR Construction - exception handling and stack unwinding information in Linux ELF executable files

### Papers: Correctness

- APEx: Automated Inference of Error Specifications for C APIs
	- Automated Software Engineering (ASE) 2016
	- Yuan Jochen Kang, Baishakhi Ray, Suman Jana
	- https://yujokang.github.io/papers/apex_2016.pdf
	- APEx: Automated Tool for Generating Error Specifications
		- https://github.com/yujokang/APEx
- Ares: Inferring Error Specifications through Static Analysis
	- Automated Software Engineering (ASE) 2019
	- Li Chi, Zuxing Gu, Min Zhou, Ming Gu, Hongyu Zhang
	- https://doi.org/10.1109/ASE.2019.00130
	- https://www.youtube.com/watch?v=nf1QnFAmu8Q
	- Ares: API Related Error Specification Inference
		- https://github.com/lc3412/Ares
- Automatically Detecting Error Handling Bugs Using Error Specifications
	- USENIX Security 2016
	- Suman Jana, Yuan Kang, Samuel Roth, Baishakhi Ray
	- https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/jana
	- EPEx: Error Path Exploration for Finding Error Handling Bugs - https://github.com/yujokang/EPEx
- Automatically Diagnosing and Repairing Error Handling Bugs in C
	- ESEC/FSE 2017
	- Yuchi Tian, Baishakhi Ray
	- https://yuchi1989.github.io/papers/fse17-ErrDoc.pdf
	- ErrDoc: Tool for detecting, categorizing, and repairing error handling bugs - https://github.com/yuchi1989/ErrDoc/
- Detecting Error-Handling Bugs without Error Specification Input
	- Automated Software Engineering (ASE) 2019
	- Zhouyang Jia, Shanshan Li, Tingting Yu, Xiangke Liao, Ji Wang, Xiaodong Liu, Yunhuai Liu
	- https://doi.org/10.1109/ASE.2019.00029
	- EH-Miner: Mining Error-Handling Bugs without Error Specification Input
		- https://github.com/ZhouyangJia/EH-Miner
- Effective Error-Specification Inference via Domain-Knowledge Expansion
	- ESEC/FSE 2019
	- Daniel DeFreez, Haaken Martinson Baldwin, Cindy Rubio-González, Aditya V. Thakur
	- https://dl.acm.org/citation.cfm?id=3338960
	- https://thakur.cs.ucdavis.edu/bibliography/defreez_rubio_thakur_FSE2019.html
	- https://github.com/ucd-plse/eesi
- Fuzzing Error Handling Code in Device Drivers Based on Software Fault Injection
	- ISSRE 2019 - The 30th International Symposium on Software Reliability Engineering
	- Zu-Ming Jiang, Jia-Ju Bai, Julia Lawall, Shi-Min Hu
	- https://hal.inria.fr/hal-02389293/
- Fuzzing Error Handling Code using Context-Sensitive Software Fault Injection
	- USENIX Security 2020
	- Zu-Ming Jiang, Jia-Ju Bai, Kangjie Lu, Shi-Min Hu
	- https://www-users.cs.umn.edu/~kjlu/papers/fifuzz.pdf
	- https://www.usenix.org/conference/usenixsecurity20/presentation/jiang
- Testing Error Handling Code in Device Drivers Using Characteristic Fault Injection
	- 2016 USENIX Annual Technical Conference
	- Jia-Ju Bai, Yu-Ping Wang, Jie Yin, Shi-Min Hu
	- https://www.usenix.org/node/196270

### WG21 - C++ Standards Committee Papers

- P0157: Handling Disappointment in C++
	- 2015-11-07; Lawrence Crowl
	- https://wg21.link/P0157
- P0323: `std::expected`
	- 2016-2021; Vicente Botet, JF Bastien
	- https://wg21.link/P0323
- P0364: Report on Exception Handling Lite (Disappointment) from SG14
	- 2016-05-23; Michael Wong, Sunil Srivastava, Sean Middleditch, Patrice Roy
	- http://wg21.link/P0364
- P0709: Zero-overhead deterministic exceptions: Throwing values
	- 2018-05-02; Herb Sutter
	- https://wg21.link/P0709
- P1028: SG14 `status_code` and standard `error` object for P0709 Zero-overhead deterministic exceptions
	- 2018-05-06; Niall Douglas
	- https://wg21.link/P1028
- P1640: Error size benchmarking
	- 2019-06-03; Ben Craig
	- https://wg21.link/P1640
- P1676: Exception Optimizations. An experiment.
	- 2019-06-04; Gor Nishanov
	- https://wg21.link/P1676
- P1886: Error speed benchmarking
	- 2019-10-05; Ben Craig
	- https://wg21.link/P1886
- P1947: C++ exceptions and alternatives
	- 2019-11-18; Bjarne Stroustrup
	- https://wg21.link/P1947
- P2544: C++ exceptions are becoming more and more problematic
	- 2022-02-12; Thomas Neumann
	- http://wg21.link/P2544

## References

- C++ Core Guidelines - Error handling
	- https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#e-error-handling
- C++ Super-FAQ - Exceptions and Error Handling
	- https://isocpp.org/wiki/faq/exceptions
- How a C++ compiler implements exception handling (Visual C++)
	- https://www.codeproject.com/Articles/2126/How-a-C-compiler-implements-exception-handling
- Reversing Microsoft Visual C++ - Igor Skochinsky, 2006
	- Part I: Exception Handling - http://www.openrce.org/articles/full_view/21
- SG14 Mailing List - Cost of throwing a C++ exception on various compilers
	- https://groups.google.com/a/isocpp.org/forum/#!topic/sg14/ByPnBM1I2Ig

## StackOverflow Questions

- Are Exceptions in C++ really slow
	- https://stackoverflow.com/questions/13835817/are-exceptions-in-c-really-slow/13836329#13836329
- In what ways do C++ exceptions slow down code when there are no exceptions thrown?
	- https://stackoverflow.com/questions/1897940/in-what-ways-do-c-exceptions-slow-down-code-when-there-are-no-exceptions-thown

---

# Software

## Benchmarks

- A test on binary sizes of C error codes vs C++ exceptions
	- https://github.com/jpakkane/excsize
- C++ exception performance experiment
	- https://github.com/neumannt/exceptionperformance
	- compares different ways to implement exception handling in C++, namely: traditional C++ exceptions, std::expected, Boost::LEAF, Herbceptions, using a pure C++ approximation, Herbceptions, using inline assembly, Boost::Outcome
	- considers two scenarios:
		- The sqrt scenario perform a relatively expensive computation that might throw from time to time. This primarily stresses the unwinder.
		- The fib scenario perform thousands of recursive calls, and thus measures the calling overhead of the different approaches.
- error_bench: Micro benchmarks for various error handling mechanisms
	- https://github.com/ben-craig/error_bench
	- Error size benchmarking
		- https://wg21.link/P1640
- Exception Handling Costing Test
	- https://github.com/johnmcfarlane/ehct
- Test programs to determine the speed of exceptions vs error codes
	- https://github.com/jpakkane/exceptionspeed
- Testing real world code performance on exceptions vs error objects
	- https://github.com/jpakkane/zipexcept
- Testing the performance of C++ exceptions vs plain C error codes
	- https://github.com/jpakkane/excspeed

## Libraries

- Abseil Status
	- https://abseil.io/blog/2020-091021-status
	- https://github.com/abseil/abseil-cpp/tree/master/absl/status
	- User Guide - https://abseil.io/docs/cpp/guides/status
	- Choosing Canonical Error Codes - https://abseil.io/docs/cpp/guides/status-codes
- Boost.Exception
	- https://github.com/boostorg/exception
- cpp_exception_handling_abi
	- https://github.com/nicolasbrailo/cpp_exception_handling_abi
- LEAF: Lightweight Error Augmentation Framework
	- https://github.com/zajo/leaf
	- https://github.com/zajo/leaf/blob/master/benchmark/benchmark.md
- llvm-expected: LLVM's Rich Recoverable Error Handling as a Library
	- https://github.com/weliveindetail/llvm-expected
	- Benchmarks for llvm::Expected vs. std::error_code
		- https://github.com/weliveindetail/BenchmarkLLVMExpected
- Optional-lite, expected-lite, and optional-bare
	- https://github.com/martinmoene/optional-lite
	- https://github.com/martinmoene/expected-lite
	- https://github.com/martinmoene/optional-bare
- Outcome
	- https://github.com/ned14/outcome
	- https://www.boost.org/doc/libs/release/libs/outcome
- STX: C++ 20 error-handling and utility extensions
	- https://github.com/lamarrr/STX
- `tl::expected` and `tl::optional`
	- https://github.com/TartanLlama/expected
	- https://github.com/TartanLlama/optional

## Tools

- ErrDoc
	- Tool for detecting, categorizing, and repairing error handling bugs
	- https://github.com/yuchi1989/ErrDoc
- EPEx: Error Path Exploration for Finding Error Handling Bugs
	- Tool for detecting error handling bugs
	- https://github.com/yujokang/EPEx
- Zelda - Zee Exception Length and Destination Analyzer
	- Open-source static analysis tool to track exception usage and flow through C++ code
	- https://github.com/k10bradley/zelda

---

# Talks

## 2022

- A Practical Approach to Error Handling
	- Arno Schödl
	- ACCU 2022
		- https://www.youtube.com/watch?v=qQPLjxZ56QA
		- https://accu.digital-medium.co.uk/wp-content/uploads/2022/04/Arno-Schoedl-A-Practical-Approach-to-Error-Handling.pdf
	- CppNow 2022
		- https://www.youtube.com/watch?v=eKcmEalOBhs
- Exceptions the Other Way Round
	- CppNow 2022
	- Sean Parent
	- https://www.youtube.com/watch?v=mkkaAWNE-Ig
- The Mysterious Life of an Exception
	- REcon 2022
	- Fabian Freyer, Marius Muench
	- https://recon2022-exceptions.github.io/
	- https://cfp.recon.cx/2022/talk/38RSED/

## 2021

- Embracing `noexcept` Operators and Specifiers Safely
	- CppCon 2021; John Lakos
	- https://www.youtube.com/watch?v=veAD1dmMdvw
- Examining and mitigating the performance impact of C++ exceptions on the non-exceptional path in LLVM
	- 2021 LLVM Developers' Meeting; Modi Mo
	- https://www.youtube.com/watch?v=7iIlqkLMKqE
	- https://llvm.org/devmtg/2021-11/slides/2021-ExaminingandMitigatingthePerformanceImpactof-C-exceptionsonthe-non-exceptionalpathinLLVM.pdf
- Exceptional C++
	- Microsoft Windows structured exception handling (SEH)
	- Victor Ciura
	- C++ on Sea 2021
		- https://www.youtube.com/watch?v=hIpE0IZz6F8
		- https://ciura.ro/presentations/2021/Conferences/Exceptional%20C++%20-%20Victor%20Ciura%20-%20C++%20On%20Sea%202021.pdf
	- CPPP 2021
		- https://www.youtube.com/watch?v=PSgY2ZLSrY0
		- https://ciura.ro/presentations/2021/Conferences/Exceptional%20C++%20-%20Victor%20Ciura%20-%20CPPP%202021.pdf
- Failing Successfully: Reporting and Handling Errors
	- CppCon 2021; Robert Leahy
	- https://www.youtube.com/watch?v=KJ3jWZryl2A

## 2020

- Back to Basics: Exceptions
	- Klaus Iglberger
	- Munich C++ User Group (MUC++) 2020
		- https://www.youtube.com/watch?v=hBiDEGJxddU
	- CppCon 2020
		- https://www.youtube.com/watch?v=0ojB8c0xUd8
		- https://github.com/CppCon/CppCon2020/tree/main/Presentations/back_to_basics_exceptions
- Design Patterns for Handling/Reporting Errors in C++ - Parallel Algorithms & Executors
	- CppCon 2020; Mark Hoemmen
	- https://www.youtube.com/watch?v=DpLZ4pnrx0o
	- https://github.com/CppCon/CppCon2020/blob/main/Presentations/design_patterns_for_error_handling/
- Exceptions Under the Spotlight
	- Inbal Levi
	- Munich C++ User Group (MUC++) 2020
		- https://www.youtube.com/watch?v=7mQBfl2K-5Y
	- CppCon 2020
		- https://www.youtube.com/watch?v=N_-bUNMLGvE
		- https://github.com/CppCon/CppCon2020/tree/main/Presentations/exceptions_under_the_spotlight

## 2019

- Back to Basics: Exception Handling and Exception Safety
	- CppCon 2019; Ben Saks
	- https://www.youtube.com/watch?v=W6jZKibuJpU
- De-fragmenting C++: Making Exceptions and RTTI More Affordable and Usable
	- Herb Sutter
	- ACCU 2019: https://www.youtube.com/watch?v=os7cqJ5qlzo
	- CppCon 2019: https://www.youtube.com/watch?v=ARYP83yNAWk
- Don't write exception classes, declare exception types
	- SwedenCpp 2019; Harald Achitz
	- https://www.youtube.com/watch?v=EGJAisKmUvU
	- https://a4z.bitbucket.io/presentations/cpp2/errtypes/
- Error Handling is Cancelling Operations
	- CppCon 2019; Andrzej Krzemieński
	- https://www.youtube.com/watch?v=zte8IxkHqc4
- Exceptions Demystified
	- C++Now 2019; Andreas Weis
	- https://www.youtube.com/watch?v=kO0KVB-XIeE
	- https://github.com/ComicSansMS/presentations/releases/tag/cppnow2019
	- https://github.com/ComicSansMS/presentations/releases/download/cppnow2019/exceptions_demystified.pdf
- Internals of Exceptions
	- Adam Furmanek
	- "Do you know what is SEH, VEH and VCH in Windows? Or do you know why C# introduced exceptions filters or how to catch everything, even StackOverflowException?In this presentation I show internal mechanisms used by Windows for handling exceptions. We will see constructs used by C++ and C# languages, CLR instructions and machine code details of those."
	- Update Conference Prague 2018 - https://www.youtube.com/watch?v=ce_db4bfzls
	- NDC Sydney 2019 - https://www.youtube.com/watch?v=NUz212O79tE
- On "Exception Handling: Issues and a Proposed Notation"
	- PWL NYC 2019; Sarah Groff Palermo
	- https://www.youtube.com/watch?v=071M3PTXJeo
- The Dawn Of A New Error
	- Phil Nash
	- ACCU 2019: https://www.youtube.com/watch?v=2Jhfubg9yvA
	- Core C++ 2019: https://www.youtube.com/watch?v=7hO0LKRCw64
	- CppCon 2019: https://www.youtube.com/watch?v=ZUH8p1EQswA

## 2018

- C++ Exception Handling - The gory details of an implementation
	- CPPDUG (Dublin C/C++ User Group) February 2018; Peter Edwards
	- What happens when throwing an exception on modern Linux systems.
	- Slides: https://isainmdom.com/~peadar/eximpl/
	- Video: https://www.youtube.com/watch?v=XpRL7exdFL8
- Dealing with function failures in C++
	- code::dive 2018; Andrzej Krzemieński
	- https://www.youtube.com/watch?v=Zv7Qqf2Jks4
- Deterministic Disappointment
	- Dublin C/C++ User Group - September 2018 Meetup; Niall Douglas
	- https://www.youtube.com/watch?v=cbUTAoHy6Ls
	- Slides: https://docs.google.com/presentation/d/1fSkpD51FKmy8VEO9P86jWN6tOEaBmzHOXo14zLRkFKE/
	- Niall covers all the ways past, present and future that one can disappoint deterministically in C++.
		- Content: What is disappointment? What is determinism? The direction of C++. Future disappointment in C++? Achieving the future today (C++11 system_error, C++11 P1028 SG14 status_code, C++14 (Boost.) Outcome).
- Ensuring Exception Safety Through Testing
	- CppCon 2018; Jon Cohen
	- https://www.youtube.com/watch?v=XPzHNSUnTc4
- Error Handling in Libraries: A Case Study
	- 2018 LLVM Developers’ Meeting; James Henderson
	- https://www.youtube.com/watch?v=YSEY4pg1YB0
- How Compilers Reason About Exceptions
	- C++Now 2018; Michael Spencer
	- https://www.youtube.com/watch?v=C4gpj-MDstY
	- https://cppnow2018.sched.com/event/EC7V/how-compilers-reason-about-exceptions
- Unwinding the Stack: Exploring how C++ Exceptions work on Windows
	- CppCon 2018; James McNellis
	- https://www.youtube.com/watch?v=COEv2kq_Ht8
	- ‏https://1drv.ms/b/s!AoyrqeD9L48NknYwKYcWS0diFlRb
	- <https://github.com/CppCon/CppCon2018/tree/master/Presentations/unwinding_the_stack_exploring_how_cpp_exceptions_work_on_windows>
- What Could Possibly Go Wrong?: A Tale of Expectations and Exceptions
	- CppCon 2018; Brand & Nash
	- https://www.youtube.com/watch?v=GC4cp4U2f2E
	- https://levelofindirection.com/refs/expectations.html

## 2017

- A Story of One Exception
	- C++ Meetup Sydney, December 6, 2017; Andrei Tarassov
	- A walkthrough on debugging an unknown exception from a core dump (Linux, GDB).
	- https://www.youtube.com/watch?v=cWHO3KXcdhU
- C++ Exceptions and Stack Unwinding
	- CppCon 2017; Dave Watson
	- Looks at the Itanium exception handling model and several implementations of it.
	- Video: https://www.youtube.com/watch?v=_Ivd3qzgT7U
- Mongrel Monads, Dirty, Dirty, Dirty
	- ACCU 2017; Niall Douglas
	- An introduction to `Outcome` and presentation of benchmarks of it against exceptions and error codes.
	- Slides: https://docs.google.com/presentation/d/1X_3VOxb8PMGXHBzjmzl5oVnwYVIyBpZHcY0Idv_9tSc/edit#slide=id.p
	- Video: https://www.youtube.com/watch?v=XVofgKH-uu4
- Rethinking Exceptions
	- Pacific++ 2017; Jason Turner
	- An examination of different error handling strategies and the code they generate.
	- Video: https://www.youtube.com/watch?v=OkgvqjJzH_Y

## 2016

- Error -- Structured Error Handling in LLVM
	- 2016 LLVM Developers’ Meeting; L. Hames
	- A look at how LLVM does error handling with `llvm::Error`.
	- Documentation: http://llvm.org/docs/ProgrammersManual.html#error-handling
	- Slides: http://www.llvm.org/devmtg/2016-11/Slides/Hames-Error.pdf
	- Video: https://www.youtube.com/watch?v=Wq8fNK98WGw
- Exceptional Performance
	- C++Now 2016; David Stone
	- "In this presentation, we will discuss exactly what effect exceptions have on the performance of an application, backed up by numbers from both benchmarks and real world applications. We will go into the details of hardware architecture and memory hierarchy to try to understand exactly why code performs the way it does."
	- https://www.youtube.com/watch?v=0_FQIDEf7_Q
- The Exception Situation
	- CppCon 2016; Patrice Roy
	- An examination of different error handling strategies and where they are appropriate.
	- Video: https://www.youtube.com/watch?v=Fno6suiXLPs

## 2015

- Exception handling in LLVM, from Itanium to MSVC
	- 2015 LLVM Developers’ Meeting; Reid Kleckner & David Majnemer
	- http://www.llvm.org/devmtg/2015-10/slides/KlecknerMajnemer-ExceptionHandling.pdf
	- https://www.youtube.com/watch?v=9TlR9hNZbck&list=PL_R5A0lGi1AA4Lv2bBFSwhgDaHvvpVU21&index=15
- The Unexceptional Exceptions
	- CppCon 2015; Fedor Pikus
	- Guidelines for using exceptions effectively.
	- Slides: https://github.com/CppCon/CppCon2015/tree/master/Presentations/Unexceptional%20exceptions
	- Video: https://www.youtube.com/watch?v=fOV7I-nmVXw

## 2014

- Exception-Safe Code
	- CppCon 2014; Jon Kalb
	- A set of guidelines for safe exception usage and solid implementation techniques, including how to transition from an exception-unsafe legacy code base.
	- http://exceptionsafecode.com/
	- Part 1 video: https://www.youtube.com/watch?v=W7fIy_54y-w
	- Part 2 video: https://www.youtube.com/watch?v=b9xMIKb1jMk
	- Part 3 video: https://www.youtube.com/watch?v=MiKxfdkMJW8

## 2012

- Compiler Internals: Exceptions and RTTI
	- Recon 2012; Igor Skochinsky
	- http://www.hexblog.com/?p=704
	- https://recon.cx/2012/schedule/events/247.en.html
	- http://www.hexblog.com/wp-content/uploads/2012/06/Recon-2012-Skochinsky-Compiler-Internals.pdf
