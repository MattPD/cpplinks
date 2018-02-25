# [C++ links](README.md): error handling

## Blogs: Posts and Series

* Andrii Batyiev - Size cost of C++ exception handling on embedded platform
	+ Uses microbenchmarking to examine the effect of exceptions on code size.
	+ https://andriidevel.blogspot.co.uk/2016/05/size-cost-of-c-exception-handling-on.html
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
* Joseph Mansfield - Exceptions, error codes, and assertions in C++
	+ A high-level look at different error handling techniques and guidelines on when to use them.
	+ http://josephmansfield.uk/articles/exceptions-error-codes-assertions-c++.html
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
	+ Microbenchmarks and assembly examinations to show that exceptions or not as expensive as many say.
* Jussi Pakkanen - Are exceptions slower than error objects
	+ A series of microbenchmarks examining the relative cost of exceptions and error objects.
	+ http://nibblestew.blogspot.co.uk/2015/12/are-exceptions-slower-than-error-objects.html        
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
	+ http://www.flounder.com/exceptions.htm
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
* Nemanja Trifunovic - C++ Exceptions: Pros and Cons
	+ A discussion of the pros and cons of exceptions.
	+ https://www.codeproject.com/Articles/38449/C-Exceptions-Pros-and-Cons

## Documentation

* Exception Handling in LLVM
	+ http://llvm.org/docs/ExceptionHandling.html
* Using Exceptions in GCC
	+ https://gcc.gnu.org/onlinedocs/libstdc++/manual/using_exceptions.html
* Exception Handling ABI for the ARM Architecture
	+ http://infocenter.arm.com/help/topic/com.arm.doc.ihi0038b/IHI0038B_ehabi.pdf
* Itanium C++ ABI: Exception Handling
	+ https://itanium-cxx-abi.github.io/cxx-abi/abi-eh.html

## Papers

* Jason Hiser, Anh Nguyen-Tuong, William Hawkins, Matthew McGill, Michele Co, Jack Davidson
	+ Zipr++: Exceptional Binary Rewriting
	+ Forming an Ecosystem Around Software Transformation (FEAST) 2017
	+ https://dl.acm.org/citation.cfm?doid=3141235.3141240
	+ https://tc.gtisc.gatech.edu/feast17/papers/p9-hiserA.pdf
	+ cf. Section 2.2 - EH Frame IR Construction - exception handling and stack unwinding information in Linux ELF executable files
* Lawrence Crowl - Handling Disappointment in C++
	+ http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0157r0.html
* Michael Wong, Sunil Srivastava, Sean Middleditch, Patrice Roy - Report on Exception Handling Lite (Disappointment) from SG14
	+ http://open-std.org/JTC1/SC22/WG21/docs/papers/2016/p0364r0.pdf

## Talks, Videos

### 2018

* CPPDUG (Dublin C/C++ User Group) February 2018: Peter Edwards - C++ Exception Handling - The gory details of an implementation
	+ What happens when throwing an exception on modern Linux systems.
	+ Slides: https://isainmdom.com/~peadar/eximpl/
	+ Video: https://www.youtube.com/watch?v=XpRL7exdFL8

### 2017

* ACCU 2017: Niall Douglas - Mongrel Monads, Dirty, Dirty, Dirty
	+ An introduction to `Outcome` and presentation of benchmarks of it against exceptions and error codes.
	+ Slides: https://docs.google.com/presentation/d/1X_3VOxb8PMGXHBzjmzl5oVnwYVIyBpZHcY0Idv_9tSc/edit#slide=id.p
	+ Video: https://www.youtube.com/watch?v=XVofgKH-uu4
* C++ Meetup Sydney, December 6, 2017: Andrei Tarassov - A Story of One Exception
	+ A walkthrough on debugging an unknown exception from a core dump (Linux, GDB).
	+ https://www.youtube.com/watch?v=cWHO3KXcdhU
* CppCon 2017: Dave Watson - C++ Exceptions and Stack Unwinding
	+ Looks at the Itanium exception handling model and several implementations of it.
	+ Video: https://www.youtube.com/watch?v=_Ivd3qzgT7U
* Pacific++ 2017: Jason Turner - Rethinking Exceptions
	+ An examination of different error handling strategies and the code they generate.
	+ Video: https://www.youtube.com/watch?v=OkgvqjJzH_Y

### 2016

* C++Now 2016 - David Stone: Exceptional Performance
	+ "In this presentation, we will discuss exactly what effect exceptions have on the performance of an application, backed up by numbers from both benchmarks and real world applications. We will go into the details of hardware architecture and memory hierarchy to try to understand exactly why code performs the way it does."
	+ https://www.youtube.com/watch?v=0_FQIDEf7_Q
* CppCon 2016: Patrice Roy - The Exception Situation
	+ An examination of different error handling strategies and where they are appropriate.
	+ Video: https://www.youtube.com/watch?v=Fno6suiXLPs
* 2016 LLVM Developers’ Meeting: L. Hames “Error -- Structured Error Handling in LLVM”
	+ A look at how LLVM does error handling with `llvm::Error`.
	+ Documentation: http://llvm.org/docs/ProgrammersManual.html#error-handling
	+ Slides: http://www.llvm.org/devmtg/2016-11/Slides/Hames-Error.pdf
	+ Video: https://www.youtube.com/watch?v=Wq8fNK98WGw

### 2015

* CppCon 2015: Fedor Pikus - The Unexceptional Exceptions
	+ Guidelines for using exceptions effectively.
	+ Video: https://www.youtube.com/watch?v=fOV7I-nmVXw

### 2014

* CppCon 2014: Jon Kalb - Exception-Safe Code
	+ A set of guidelines for safe exception usage and solid implementation techniques, including how to transition from an exception-unsafe legacy code base.
	+ Part 1 video: https://www.youtube.com/watch?v=W7fIy_54y-w
	+ Part 2 video: https://www.youtube.com/watch?v=b9xMIKb1jMk
	+ Part 3 video: https://www.youtube.com/watch?v=MiKxfdkMJW8

## Libraries

* Boost.Exception
	+ https://github.com/boostorg/exception
* cpp_exception_handling_abi
	+ https://github.com/nicolasbrailo/cpp_exception_handling_abi
* llvm-expected: LLVM's Rich Recoverable Error Handling as a Library
	+ https://github.com/weliveindetail/llvm-expected
	+ Benchmarks for llvm::Expected vs. std::error_code
		- https://github.com/weliveindetail/BenchmarkLLVMExpected
* Outcome
	+ https://github.com/ned14/outcome
* `tl::expected` and `tl::optional`
	+ https://github.com/TartanLlama/expected
	+ https://github.com/TartanLlama/optional
* Optional-lite, expected-lite, and optional-bare
	+ https://github.com/martinmoene/optional-lite
	+ https://github.com/martinmoene/expected-lite
	+ https://github.com/martinmoene/optional-bare

## StackOverflow Questions
* Are Exceptions in C++ really slow
	+ https://stackoverflow.com/questions/13835817/are-exceptions-in-c-really-slow/13836329#13836329
* In what ways do C++ exceptions slow down code when there are no exceptions thown?
	+ https://stackoverflow.com/questions/1897940/in-what-ways-do-c-exceptions-slow-down-code-when-there-are-no-exceptions-thown

## References

* C++ Core Guidelines - Error handling
	+ https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#e-error-handling
* C++ Super-FAQ - Exceptions and Error Handling
	+ https://isocpp.org/wiki/faq/exceptions
* SG14 Mailing List - Cost of throwing a C++ exception on various compilers
	+ https://groups.google.com/a/isocpp.org/forum/#!topic/sg14/ByPnBM1I2Ig
