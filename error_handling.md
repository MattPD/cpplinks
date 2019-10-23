# [C++ links](README.md): error handling

# Contents

* [Readings](#readings): [Blogs](#blogs-posts-and-series), [Documentation](#documentation), [Papers](#papers), [References](#references), [StackOverflow](#stackoverflow-questions)
* [Software](#software): [Benchmarks](#benchmarks), [Libraries](#libraries), [Tools](#tools)
* [Talks](#talks): [2019](#2019), [2018](#2018), [2017](#2017), [2016](#2016), [2015](#2015), [2014](#2014)

---

# Readings

## Blogs: Posts and Series

* Andrii Batyiev - Size cost of C++ exception handling on embedded platform
	+ Uses microbenchmarking to examine the effect of exceptions on code size.
	+ https://andriidevel.blogspot.co.uk/2016/05/size-cost-of-c-exception-handling-on.html
* Chris Brumme - The Exception Model
	+ Windows Structured Exception Handling (SEH) and C++ exceptions
	+ https://blogs.msdn.microsoft.com/cbrumme/2003/10/01/the-exception-model/
* Joe Duffy - The Error Model - http://joeduffyblog.com/2016/02/07/the-error-model/
* Nicolas Brailovsky - C++ exceptions under the hood
	+ A long series of posts looking at how C++ exceptions are actually implemented.
	+ https://monoinfinito.wordpress.com/2013/02/05/c-exceptions-under-the-hood/
	+ https://monoinfinito.wordpress.com/2013/02/12/c-exceptions-under-the-hood-ii-a-tiny-abi/
	+ https://monoinfinito.wordpress.com/2013/02/19/c-exceptions-under-the-hood-3-an-abi-to-appease-the-linker/
	+ https://monoinfinito.wordpress.com/2013/02/26/c-exceptions-under-the-hood-4-catching-what-you-throw/
	+ https://monoinfinito.wordpress.com/2013/03/05/c-exceptions-under-the-hood-5-magic-around-__cxa_begin_catch-and-__cxa_end_catch/
	+ https://monoinfinito.wordpress.com/2013/03/12/c-exceptions-under-the-hood-6-gcc_except_table-and-the-personality-function/
	+ https://monoinfinito.wordpress.com/2013/03/19/c-exceptions-under-the-hood-7-a-nice-personality/
	+ https://monoinfinito.wordpress.com/2013/03/26/c-exceptions-under-the-hood-8-two-phase-handling/
	+ https://monoinfinito.wordpress.com/2013/04/02/c-exceptions-under-the-hood-9-catching-our-first-exception/
	+ https://monoinfinito.wordpress.com/2013/04/09/c-exceptions-under-the-hood-10-_unwind_-and-call-frame-info/
	+ https://monoinfinito.wordpress.com/2013/04/11/c-exceptions-under-the-hood-11-reading-a-cfi-table/
	+ https://monoinfinito.wordpress.com/2013/04/16/c-exceptions-under-the-hood-12-and-suddenly-reflexion-in-c/
	+ https://monoinfinito.wordpress.com/2013/04/23/c-exceptions-under-the-hood-14-multiple-landing-pads-the-teachings-of-the-guru/
	+ https://monoinfinito.wordpress.com/2013/04/25/c-exceptions-under-the-hood-13-setting-the-context-for-a-landing-pad/
	+ https://monoinfinito.wordpress.com/2013/05/02/c-exceptions-under-the-hood-15-finding-the-right-landing-pad/
	+ https://monoinfinito.wordpress.com/2013/05/07/c-exceptions-under-the-hood-16-finding-the-right-catch-in-a-landing-pad/
	+ https://monoinfinito.wordpress.com/2013/05/14/c-exceptions-under-the-hood-17-reflecting-on-an-exception-type-and-reading-gcc_except_table/
	+ https://monoinfinito.wordpress.com/2013/05/16/c-exceptions-under-the-hood-18-getting-the-right-stack-frame/
	+ https://monoinfinito.wordpress.com/2013/05/23/c-exceptions-under-the-hood-19-getting-the-right-catch-in-a-landing-pad/
	+ https://monoinfinito.wordpress.com/2013/05/28/c-exceptions-under-the-hood-20-running-destructors-while-unwinding/
	+ https://monoinfinito.wordpress.com/2013/06/04/c-exceptions-under-the-hood-21-a-summary-and-some-final-thoughts/
	+ https://monoinfinito.wordpress.com/2013/06/11/c-exceptions-under-the-hood-appendix-i-the-true-cost-of-an-exception/
	+ https://monoinfinito.wordpress.com/2013/06/13/c-exceptions-under-the-hood-appendix-ii-metaclasses-and-rtti-on-c/
	+ https://monoinfinito.wordpress.com/2013/07/25/c-exceptions-under-the-hood-appendix-iii-rtti-and-exceptions-orthogonality/
* Simon Brand - Functional exceptionless error-handling with optional and expected
	+ Demonstrates how to use `optional` and `expected` with monadic extensions.
	+ https://blog.tartanllama.xyz/optional-expected/        
* "Buckaroo" - Error Handling in C++ or: Why You Should Use Eithers in Favor of Exceptions and Error-codes
	+ Presents some reasons to use Eithers (A.K.A. `std::expected`) instead of other alternatives.
	+ https://hackernoon.com/error-handling-in-c-or-why-you-should-use-eithers-in-favor-of-exceptions-and-error-codes-f0640912eb45
* Stefan Gränitz - Series: Rich Recoverable Error Handling with llvm::Expected<T>
	+ A series of posts demonstrating the motivation and use of `llvm::Expected`.
	+ Part 1 - Motivation: https://weliveindetail.github.io/blog/post/2017/09/06/llvm-expected-basics.html
	+ Part 2 - Differentiation: https://weliveindetail.github.io/blog/post/2017/10/22/llvm-expected-differentiation.html
	+ Part 3 - All Helpers: https://weliveindetail.github.io/blog/post/2017/10/28/llvm-expected-helpers.html
	+ Talk - C++ User Group Berlin 2017, September 19th: Rich Polymorphic Error Handling with llvm::Expected<T>
		- Slides (PDF): https://github.com/weliveindetail/talks/raw/master/Expectify.pdf
* Mike Hearn - What's wrong with exceptions? Nothing.
	+ A defense of exceptions in general, but contains discussion on issues with C++'s implementation of them.
	+ https://blog.plan99.net/what-s-wrong-with-exceptions-nothing-cee2ed0616
* Shane Kirk - C++ Exceptions: The Good, The Bad, And The Ugly
	+ A discussion of the pros and cons of exceptions.
	+ http://www.shanekirk.com/2015/06/c-exceptions-the-good-the-bad-and-the-ugly/
* Boris Kolpackov
	+ Throwing Destructors - https://www.kolpackov.net/projects/c++/eh/dtor-1.xhtml
* Hyungjoon Koo (Kevin)
	+ ELF Sections for Exception Handling - http://dandylife.net/blog/archives/686
* Andrzej Krzemieński
	+ https://akrzemi1.wordpress.com/2011/09/21/destructors-that-throw/
	+ https://akrzemi1.wordpress.com/2012/11/14/not-using-stdthread/
	+ https://akrzemi1.wordpress.com/2013/07/18/cs-best-feature/
	+ https://akrzemi1.wordpress.com/2013/08/20/noexcept-destructors/
	+ https://akrzemi1.wordpress.com/2014/02/12/find-the-bug/
	+ https://akrzemi1.wordpress.com/2014/03/13/find-the-bug-comments/
	+ https://akrzemi1.wordpress.com/2014/04/24/noexcept-what-for/
	+ https://akrzemi1.wordpress.com/2014/09/19/destructors-2-use-cases/
	+ Handling errors is canceling operations - https://akrzemi1.wordpress.com/2019/04/25/handling-errors-is-canceling-operations/
	+ Operation cancelling and std::fstream - https://akrzemi1.wordpress.com/2019/05/23/operation-cancelling-and-stdfstream/
	+ error codes
		- Your own error code - https://akrzemi1.wordpress.com/2017/07/12/your-own-error-code/
		- Your own error condition - https://akrzemi1.wordpress.com/2017/08/12/your-own-error-condition/
		- Using error codes effectively - https://akrzemi1.wordpress.com/2017/09/04/using-error-codes-effectively/
		- error codes — some clarifications - https://akrzemi1.wordpress.com/2017/10/14/error-codes-some-clarifications/
* Akshay Kumar
	+ How McSema Handles C++ Exceptions - https://blog.trailofbits.com/2019/01/21/how-mcsema-handles-c-exceptions/
* Eric Lippert
	+ I Take Exception To That - https://ericlippert.com/2003/10/15/i-take-exception-to-that/
	+ Long jumps considered way more harmful than exceptions - https://ericlippert.com/2003/10/16/long-jumps-considered-way-more-harmful-than-exceptions/
* Joseph Mansfield - Exceptions, error codes, and assertions in C++
	+ A high-level look at different error handling techniques and guidelines on when to use them.
	+ http://josephmansfield.uk/articles/exceptions-error-codes-assertions-c++.html
* Modi Mo
	+ Making C++ Exception Handling Smaller On x64
	+ https://devblogs.microsoft.com/cppblog/making-cpp-exception-handling-smaller-x64/
* Edaqa Mortoray - Everything wrong with C++ exceptions
	+ Does as it says on the tin.
	+ https://mortoray.com/2012/04/02/everything-wrong-with-exceptions/
* Edaqa Mortoray - The true cost of zero cost exceptions
	+ Examines how exceptions are implemented in order to show some of the real costs of them.
	+ https://mortoray.com/2013/09/12/the-true-cost-of-zero-cost-exceptions/
* Jonathan Müller - Exceptions vs expected: Let's find a compromise
	+ A look at finding a middle ground between exceptions and `std::expected` by examining what other languages provide.
	+ http://foonathan.net/blog/2017/12/04/exceptions-vs-expected.html
* Joseph M. Newcomer - Mythology in C++: Exceptions are Expensive
	+ Microbenchmarks and assembly examinations to show that exceptions are not as expensive as many say.
	+ http://www.flounder.com/exceptions.htm
* Jussi Pakkanen - Are exceptions slower than error objects
	+ A series of microbenchmarks examining the relative cost of exceptions and error objects.
	+ Are exceptions slower than error objects - http://nibblestew.blogspot.co.uk/2015/12/are-exceptions-slower-than-error-objects.html
	+ Comparing executable size of C++ exceptions vs plain C error structs - http://nibblestew.blogspot.com/2016/12/comparing-executable-size-of-c.html
	+ Measuring execution performance of C++ exceptions vs error codes - http://nibblestew.blogspot.com/2017/01/measuring-execution-performance-of-c.html
	+ Testing exception vs error code behaviour with real world code - http://nibblestew.blogspot.com/2017/01/testing-exception-vs-error-code.html
* Jason Robert Carey Patterson - Exception Handling Considered Harmful
	+ A discussion of various problems with C++ exceptions.
	+ http://www.lighterra.com/papers/exceptionsharmful/
* Theofilos Petsios - C++ Exception Handling
	+ Base ABI - http://web.archive.org/web/20141209000556/http://theofilos.cs.columbia.edu/blog/2013/09/22/base_abi/
	+ Level II ABI - http://web.archive.org/web/20141209000543/http://theofilos.cs.columbia.edu/blog/2013/09/27/c-exception-handling-level-ii-abi/
	+ Overview - http://web.archive.org/web/20141208235659/http://theofilos.cs.columbia.edu/blog/2013/09/30/c-exception-handling/
	+ Stack Frame Destruction - http://web.archive.org/web/20141208235529/http://theofilos.cs.columbia.edu/blog/2013/10/03/c-exception-handling-stack-frame-destruction/
* Jeff Preshing - The Cost of Enabling Exception Handling
	+ Uses microbenchmarking and assembly analysis to examine the effect of enabling exceptions.
	+ http://preshing.com/20110807/the-cost-of-enabling-exception-handling/        
* Vittorio Romeo - Why choose sum types over exceptions?
	+ A case study of somewhere you might want to choose sum types over exceptions, along with some more general guidance.
	+ https://vittorioromeo.info/index/blog/adts_over_exceptions.html        
* Patrice Roy - Exceptions in C++ and their Costs
	+ A series of microbenchmarks looking at the tradeoffs between exceptions and error codes.
	+ http://h-deb.clg.qc.ca/Sujets/Developpement/Exceptions-Costs.html
* Herb Sutter - When and How to Use Exceptions
	+ Guidelines on which cases to use exceptions for.
	+ http://www.drdobbs.com/when-and-how-to-use-exceptions/184401836        
* Ian Lance Taylor
	+ GCC Exception Frames - https://www.airs.com/blog/archives/166
	+ Exception Destruction - https://www.airs.com/blog/archives/257
	+ .eh_frame - https://www.airs.com/blog/archives/460
	+ .eh_frame_hdr - https://www.airs.com/blog/archives/462
	+ .gcc_except_table - https://www.airs.com/blog/archives/464
* Lucian Teodorescu
‏	+ Exceptional exploration
		- http://lucteo.ro/2018/03/18/exceptional-exploration-1/
		- http://lucteo.ro/2018/04/21/exception-exploration-2/
* Nemanja Trifunovic - C++ Exceptions: Pros and Cons
	+ A discussion of the pros and cons of exceptions.
	+ https://www.codeproject.com/Articles/38449/C-Exceptions-Pros-and-Cons

## Documentation

* Dwarf2 Exception Handler HOWTO
	+ https://gcc.gnu.org/wiki/Dwarf2EHNewbiesHowto
* Exception Handling in LLVM
	+ http://llvm.org/docs/ExceptionHandling.html
* Exception Handling ABI for the ARM Architecture
	+ http://infocenter.arm.com/help/topic/com.arm.doc.ihi0038b/IHI0038B_ehabi.pdf
* Itanium C++ ABI: Exception Handling
	+ https://itanium-cxx-abi.github.io/cxx-abi/abi-eh.html
* Using Exceptions in GCC
	+ https://gcc.gnu.org/onlinedocs/libstdc++/manual/using_exceptions.html

## Papers

* A Study of the Applicability of Existing Exception-handling Techniques to Component-based Real-time Software Technology
	+ ACM Transactions on Programming Languages and Systems (TOPLAS) 20(2) 1998
	+ Jun Lang and David B. Stewart
	+ https://doi.org/10.1145/276393.276395
	+ http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.33.3400&rep=rep1&type=pdf
* A Study on the Effects of Exception Usage in Open-Source C++ Systems
	+ 2019 Master Thesis; Kirsten Bradley
	+ http://hdl.handle.net/10012/14714
* Automatically Detecting Error Handling Bugs Using Error Specifications
	+ USENIX Security 2016
	+ Suman Jana, Yuan Kang, Samuel Roth, Baishakhi Ray
	+ https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/jana
	+ EPEx: Error Path Exploration for Finding Error Handling Bugs - https://github.com/yujokang/EPEx
* Automatically Diagnosing and Repairing Error Handling Bugs in C
	+ ESEC/FSE 2017
	+ Yuchi Tian, Baishakhi Ray
	+ https://yuchi1989.github.io/papers/fse17-ErrDoc.pdf
	+ ErrDoc: Tool for detecting, categorizing, and repairing error handling bugs - https://github.com/yuchi1989/ErrDoc/
* C++ exception handling
	+ IEEE Concurrency 8(4) 2000
	+ Christophe De Dinechin
	+ https://doi.org/10.1109/4434.895109
* C++ Exception Handling for IA64
	+ USENIX Workshop on Industrial Experiences with Systems Software (WIESS) 2000
	+ Christophe de Dinechin
	+ http://www.usenix.org/events/wiess2000/dinechin.html 
* Effective Error-Specification Inference via Domain-Knowledge Expansion
	+ ESEC/FSE 2019
	+ Daniel DeFreez, Haaken Martinson Baldwin, Cindy Rubio-González, Aditya V. Thakur
	+ https://dl.acm.org/citation.cfm?id=3338960
	+ https://github.com/ucd-plse/eesi
* Exception Handling: Issues and a Proposed Notation
	+ Communications of the ACM (CACM) 18(12) 1975
	+ John B. Goodenough
	+ https://dl.acm.org/citation.cfm?id=361230
* Exception Optimizations. An experiment.
	+ 2019-06-04; Gor Nishanov
	+ https://wg21.link/P1676
* Exception-Safety in Generic Components: Lessons Learned from Specifying Exception-Safety for the C++ Standard Library
	+ David Abrahams
	+ https://www.boost.org/community/exception_safety.html
	+ Error and Exception Handling - https://www.boost.org/community/error_handling.html
* Exceptional Kernel: Using C++ Exceptions in the Linux Kernel
	+ 2004
	+ Halldor Isak Glyfason and Gisli Hjalmtysson
	+ http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.100.7504
	+ http://web.archive.org/http://netlab.ru.is/exception/KernelExceptions.pdf
	+ C++ Exceptions & the Linux Kernel (2005)
		- http://www.drdobbs.com/cpp/c-exceptions-the-linux-kernel/229100146
* Generating Precise Error Specifications for C: A Zero Shot Learning Approach
	+ SPLASH 2019 OOPSLA
	+ Baijun Wu, John Peter Campora III, He Yi, Alexander Schlecht, Sheng Chen
	+ https://dl.acm.org/citation.cfm?id=3360586
	+ https://2019.splashcon.org/details/splash-2019-oopsla/44/Generating-Precise-Error-Specifications-for-C-A-Zero-Shot-Learning-Approach
	+ https://bitbucket.org/plcacs/errorspec/src/master/
* Handling Disappointment in C++ - Lawrence Crowl
	+ http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0157r0.html
* Interprocedural exception analysis for C++
	+ ECOOP 2011
	+ Prakash Prabhu, Naoto Maeda, Gogul Balakrishnan, Franjo Ivančić, Aarti Gupta
	+ https://www.semanticscholar.org/paper/Interprocedural-Exception-Analysis-for-C%2B%2B-Prabhu-Maeda/0aa41227da8f2db0af3afc67f71b7d9ebc09fb8c
	+ http://pages.cs.wisc.edu/~bgogul/Research/Papers/ecoop11.html
* Low-cost Deterministic C++ Exceptions for Embedded Systems
	+ Compiler Construction (CC) 2019
	+ James Renwick, Tom Spink, Björn Frank
	+ https://doi.org/10.1145/3302516.3307346
	+ https://www.research.ed.ac.uk/portal/en/publications/lowcost-deterministic-c-exceptions-for-embedded-systems(2cfc59d5-fa95-45e0-83b2-46e51098cf1f).html
* Model checking C++ programs with exceptions
	+ Science of Computer Programming, Volume 128, 2016
	+ P. Ročkai, J. Barnat, L. Brim
	+ https://dl.acm.org/citation.cfm?id=2974473
	+ http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.671.6441&rep=rep1&type=pdf
	+ https://journal.ub.tu-berlin.de/eceasst/article/view/983
	+ http://fmt.cs.utwente.nl/conferences/avocs2014/slides/slides.pdf
* Optimizing away C++ exception handling
	+ SIGPLAN Notices 33(8) 1998
	+ Jonathan L. Schilling
	+ https://dl.acm.org/citation.cfm?id=286390
	+ http://www.ut.sco.com/developers/products/ehopt.pdf
* Path-Based Function Embedding and Its Application to Error-Handling Specification Mining
	+ European Software Engineering Conference and Symposium on the Foundations of Software Engineering (ESEC/FSE) 2018
	+ Daniel DeFreez, Aditya V. Thakur, Cindy Rubio-González
	+ https://doi.org/10.1145/3236024.3236059
	+ http://web.cs.ucdavis.edu/~rubio/includes/fse18.pdf
* Report on Exception Handling Lite (Disappointment) from SG14
	+ Michael Wong, Sunil Srivastava, Sean Middleditch, Patrice Roy
	+ http://open-std.org/JTC1/SC22/WG21/docs/papers/2016/p0364r0.pdf
* Terse Exception Messages
	+ Overload Journal #127, June 2015; Chris Oldwood
	+ https://accu.org/index.php/journals/2110
* The Use of C++ Exception Handling Constructs: A Comprehensive Study
	+ Source Code Analysis and Manipulation (SCAM) 2015
	+ Rodrigo Bonifacio, Fausto Carvalho, Guilherme N. Ramos, Uira Kulesza, Roberta Coelho
	+ http://rbonifacio.net/papers/scam2015/rbonifacio-scam2015.pdf
* Using Off-the-Shelf Exception Support Components in C++ Verification
	+ Software Quality, Reliability and Security (QRS) 2017
	+ Vladimír Štill, Petr Ročkai, Jiří Barnat
	+ https://arxiv.org/pdf/1703.02394
	+ https://divine.fi.muni.cz/2017/exceptions/
* Zero-overhead deterministic exceptions: Throwing values
	+ Herb Sutter
	+ https://wg21.link/p0709
* Zipr++: Exceptional Binary Rewriting
	+ Forming an Ecosystem Around Software Transformation (FEAST) 2017
	+ Jason Hiser, Anh Nguyen-Tuong, William Hawkins, Matthew McGill, Michele Co, Jack Davidson
	+ https://dl.acm.org/citation.cfm?doid=3141235.3141240
	+ https://tc.gtisc.gatech.edu/feast17/papers/p9-hiserA.pdf
	+ Section 2.2 - EH Frame IR Construction - exception handling and stack unwinding information in Linux ELF executable files

## References

* C++ Core Guidelines - Error handling
	+ https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#e-error-handling
* C++ Super-FAQ - Exceptions and Error Handling
	+ https://isocpp.org/wiki/faq/exceptions
* How a C++ compiler implements exception handling (Visual C++)
	+ https://www.codeproject.com/Articles/2126/How-a-C-compiler-implements-exception-handling
* Reversing Microsoft Visual C++ - Igor Skochinsky, 2006
	+ Part I: Exception Handling - http://www.openrce.org/articles/full_view/21
* SG14 Mailing List - Cost of throwing a C++ exception on various compilers
	+ https://groups.google.com/a/isocpp.org/forum/#!topic/sg14/ByPnBM1I2Ig

## StackOverflow Questions

* Are Exceptions in C++ really slow
	+ https://stackoverflow.com/questions/13835817/are-exceptions-in-c-really-slow/13836329#13836329
* In what ways do C++ exceptions slow down code when there are no exceptions thrown?
	+ https://stackoverflow.com/questions/1897940/in-what-ways-do-c-exceptions-slow-down-code-when-there-are-no-exceptions-thown

---

# Software

## Benchmarks

* A test on binary sizes of C error codes vs C++ exceptions
	+ https://github.com/jpakkane/excsize
* error_bench: Micro benchmarks for various error handling mechanisms
	+ https://github.com/ben-craig/error_bench
	+ Error size benchmarking
		- https://wg21.link/P1640
* Exception Handling Costing Test
	+ https://github.com/johnmcfarlane/ehct
* Test programs to determine the speed of exceptions vs error codes
	+ https://github.com/jpakkane/exceptionspeed
* Testing real world code performance on exceptions vs error objects
	+ https://github.com/jpakkane/zipexcept
* Testing the performance of C++ exceptions vs plain C error codes
	+ https://github.com/jpakkane/excspeed

## Libraries

* Boost.Exception
	+ https://github.com/boostorg/exception
* cpp_exception_handling_abi
	+ https://github.com/nicolasbrailo/cpp_exception_handling_abi
* llvm-expected: LLVM's Rich Recoverable Error Handling as a Library
	+ https://github.com/weliveindetail/llvm-expected
	+ Benchmarks for llvm::Expected vs. std::error_code
		- https://github.com/weliveindetail/BenchmarkLLVMExpected
* Optional-lite, expected-lite, and optional-bare
	+ https://github.com/martinmoene/optional-lite
	+ https://github.com/martinmoene/expected-lite
	+ https://github.com/martinmoene/optional-bare
* Outcome
	+ https://github.com/ned14/outcome
* `tl::expected` and `tl::optional`
	+ https://github.com/TartanLlama/expected
	+ https://github.com/TartanLlama/optional

## Tools

* ErrDoc
	+ Tool for detecting, categorizing, and repairing error handling bugs
	+ https://github.com/yuchi1989/ErrDoc
* EPEx: Error Path Exploration for Finding Error Handling Bugs
	+ Tool for detecting error handling bugs
	+ https://github.com/yujokang/EPEx

---

# Talks

## 2019

* Back to Basics: Exception Handling and Exception Safety
	+ CppCon 2019; Ben Saks
	+ https://www.youtube.com/watch?v=W6jZKibuJpU
* De-fragmenting C++: Making Exceptions and RTTI More Affordable and Usable
	+ Herb Sutter
	+ ACCU 2019: https://www.youtube.com/watch?v=os7cqJ5qlzo
	+ CppCon 2019: https://www.youtube.com/watch?v=ARYP83yNAWk
* Error Handling is Cancelling Operations
	+ CppCon 2019; Andrzej Krzemieński
	+ https://www.youtube.com/watch?v=zte8IxkHqc4
* Exceptions Demystified
	+ C++Now 2019; Andreas Weis
	+ https://www.youtube.com/watch?v=kO0KVB-XIeE
	+ https://github.com/ComicSansMS/presentations/releases/tag/cppnow2019
	+ https://github.com/ComicSansMS/presentations/releases/download/cppnow2019/exceptions_demystified.pdf
* Internals of Exceptions
	+ Update Conference Prague 2018; Adam Furmanek
	+ "Do you know what is SEH, VEH and VCH in Windows? Or do you know why C# introduced exceptions filters or how to catch everything, even StackOverflowException?In this presentation I show internal mechanisms used by Windows for handling exceptions. We will see constructs used by C++ and C# languages, CLR instructions and machine code details of those."
	+ https://www.youtube.com/watch?v=ce_db4bfzls
* On "Exception Handling: Issues and a Proposed Notation"
	+ PWL NYC 2019; Sarah Groff Palermo
	+ https://www.youtube.com/watch?v=071M3PTXJeo
* The Dawn Of A New Error
	+ Phil Nash
	+ ACCU 2019: https://www.youtube.com/watch?v=2Jhfubg9yvA
	+ Core C++ 2019: https://www.youtube.com/watch?v=7hO0LKRCw64
	+ CppCon 2019: https://www.youtube.com/watch?v=ZUH8p1EQswA

## 2018

* C++ Exception Handling - The gory details of an implementation
	+ CPPDUG (Dublin C/C++ User Group) February 2018; Peter Edwards
	+ What happens when throwing an exception on modern Linux systems.
	+ Slides: https://isainmdom.com/~peadar/eximpl/
	+ Video: https://www.youtube.com/watch?v=XpRL7exdFL8
* Dealing with function failures in C++
	+ code::dive 2018; Andrzej Krzemieński
	+ https://www.youtube.com/watch?v=Zv7Qqf2Jks4
* Deterministic Disappointment
	+ Dublin C/C++ User Group - September 2018 Meetup; Niall Douglas
	+ https://www.youtube.com/watch?v=cbUTAoHy6Ls
	+ Slides: https://docs.google.com/presentation/d/1fSkpD51FKmy8VEO9P86jWN6tOEaBmzHOXo14zLRkFKE/
	+ Niall covers all the ways past, present and future that one can disappoint deterministically in C++.
		- Content: What is disappointment? What is determinism? The direction of C++. Future disappointment in C++? Achieving the future today (C++11 system_error, C++11 P1028 SG14 status_code, C++14 (Boost.) Outcome).
* Ensuring Exception Safety Through Testing
	+ CppCon 2018; Jon Cohen
	+ https://www.youtube.com/watch?v=XPzHNSUnTc4
* Error Handling in Libraries: A Case Study
	+ 2018 LLVM Developers’ Meeting; James Henderson
	+ https://www.youtube.com/watch?v=YSEY4pg1YB0
* How Compilers Reason About Exceptions
	+ C++Now 2018; Michael Spencer
	+ https://www.youtube.com/watch?v=C4gpj-MDstY
	+ https://cppnow2018.sched.com/event/EC7V/how-compilers-reason-about-exceptions
* Unwinding the Stack: Exploring how C++ Exceptions work on Windows
	+ CppCon 2018; James McNellis
	+ https://www.youtube.com/watch?v=COEv2kq_Ht8
	+ ‏https://1drv.ms/b/s!AoyrqeD9L48NknYwKYcWS0diFlRb
	+ https://github.com/CppCon/CppCon2018/tree/master/Presentations/Unwinding%20the%20Stack%20-%20Exploring%20How%20C%2B%2B%20Exceptions%20Work%20on%20Windows
* What Could Possibly Go Wrong?: A Tale of Expectations and Exceptions
	+ CppCon 2018; Brand & Nash
	+ https://www.youtube.com/watch?v=GC4cp4U2f2E
	+ https://levelofindirection.com/refs/expectations.html

## 2017

* A Story of One Exception
	+ C++ Meetup Sydney, December 6, 2017; Andrei Tarassov
	+ A walkthrough on debugging an unknown exception from a core dump (Linux, GDB).
	+ https://www.youtube.com/watch?v=cWHO3KXcdhU
* C++ Exceptions and Stack Unwinding
	+ CppCon 2017; Dave Watson
	+ Looks at the Itanium exception handling model and several implementations of it.
	+ Video: https://www.youtube.com/watch?v=_Ivd3qzgT7U
* Mongrel Monads, Dirty, Dirty, Dirty
	+ ACCU 2017; Niall Douglas
	+ An introduction to `Outcome` and presentation of benchmarks of it against exceptions and error codes.
	+ Slides: https://docs.google.com/presentation/d/1X_3VOxb8PMGXHBzjmzl5oVnwYVIyBpZHcY0Idv_9tSc/edit#slide=id.p
	+ Video: https://www.youtube.com/watch?v=XVofgKH-uu4
* Rethinking Exceptions
	+ Pacific++ 2017; Jason Turner
	+ An examination of different error handling strategies and the code they generate.
	+ Video: https://www.youtube.com/watch?v=OkgvqjJzH_Y

## 2016

* Error -- Structured Error Handling in LLVM
	+ 2016 LLVM Developers’ Meeting; L. Hames
	+ A look at how LLVM does error handling with `llvm::Error`.
	+ Documentation: http://llvm.org/docs/ProgrammersManual.html#error-handling
	+ Slides: http://www.llvm.org/devmtg/2016-11/Slides/Hames-Error.pdf
	+ Video: https://www.youtube.com/watch?v=Wq8fNK98WGw
* Exceptional Performance
	+ C++Now 2016; David Stone
	+ "In this presentation, we will discuss exactly what effect exceptions have on the performance of an application, backed up by numbers from both benchmarks and real world applications. We will go into the details of hardware architecture and memory hierarchy to try to understand exactly why code performs the way it does."
	+ https://www.youtube.com/watch?v=0_FQIDEf7_Q
* The Exception Situation
	+ CppCon 2016; Patrice Roy
	+ An examination of different error handling strategies and where they are appropriate.
	+ Video: https://www.youtube.com/watch?v=Fno6suiXLPs

## 2015

* Exception handling in LLVM, from Itanium to MSVC
	+ 2015 LLVM Developers’ Meeting; Reid Kleckner & David Majnemer
	+ http://www.llvm.org/devmtg/2015-10/slides/KlecknerMajnemer-ExceptionHandling.pdf
	+ https://www.youtube.com/watch?v=9TlR9hNZbck&list=PL_R5A0lGi1AA4Lv2bBFSwhgDaHvvpVU21&index=15
* The Unexceptional Exceptions
	+ CppCon 2015; Fedor Pikus
	+ Guidelines for using exceptions effectively.
	+ Slides: https://github.com/CppCon/CppCon2015/tree/master/Presentations/Unexceptional%20exceptions
	+ Video: https://www.youtube.com/watch?v=fOV7I-nmVXw

## 2014

* Exception-Safe Code
	+ CppCon 2014; Jon Kalb
	+ A set of guidelines for safe exception usage and solid implementation techniques, including how to transition from an exception-unsafe legacy code base.
	+ http://exceptionsafecode.com/
	+ Part 1 video: https://www.youtube.com/watch?v=W7fIy_54y-w
	+ Part 2 video: https://www.youtube.com/watch?v=b9xMIKb1jMk
	+ Part 3 video: https://www.youtube.com/watch?v=MiKxfdkMJW8

## 2012

* Compiler Internals: Exceptions and RTTI
	+ Recon 2012; Igor Skochinsky
	+ http://www.hexblog.com/?p=704
	+ https://recon.cx/2012/schedule/events/247.en.html
	+ http://www.hexblog.com/wp-content/uploads/2012/06/Recon-2012-Skochinsky-Compiler-Internals.pdf
