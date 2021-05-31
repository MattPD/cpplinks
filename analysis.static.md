# [C++ links](README.md): Program Analysis - Static

See also:

- [Compilers](https://github.com/MattPD/cpplinks/blob/master/compilers.md)
- [Debugging](https://github.com/MattPD/cpplinks/blob/master/debugging.md)
- [Program Analysis](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef)
	- [Dynamic Program Analysis](analysis.dynamic.md) - instrumentation, translation, sanitizers
	- [Symbolic Execution](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef#symbolic-execution)
	- [LLVM - Verification](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef#llvm---verification)
- [Testing](https://github.com/MattPD/cpplinks/blob/master/testing.md)
	- [Fuzzing](https://github.com/MattPD/cpplinks/blob/master/testing.fuzzing.md)

# Contents

- [Readings](#readings)
	- [Books](#readings-books)
	- [Research](#readings-research)
		- [Correctness](#readings-research-correctness)
- [Benchmarking](#benchmarking)
- [Verification](#verification): Verification & Model Checking
	- [Software](#verification-software): Verification Software
- [Software](#software):
	- [Compilers](#software-compilers): Clang, GCC, Visual C++ - static analysis support

---

# Readings

- Static Analysis Roadmap
	- https://tpiazza.me/posts/2017-11-01-static-analysis-roadmap.html
- Best Practices for the use of Static Code Analysis within a Real-World Secure Development Lifecycle
	- 2015; Jeremy Boone
	- https://www.nccgroup.trust/us/our-research/best-practices-for-the-use-of-static-code-analysis-within-a-real-world-secure-development-lifecycle/
- Bill Torpey - [static analysis posts](http://btorpey.github.io/blog/categories/static-analysis/)
	- Static Analysis with Clang - http://btorpey.github.io/blog/2015/04/27/static-analysis-with-clang/
	- Mo' Static - http://btorpey.github.io/blog/2016/04/07/mo-static/
	- Even Mo' Static - http://btorpey.github.io/blog/2016/11/12/even-mo-static/
	- Lots o' static - http://btorpey.github.io/blog/2017/09/17/lotso-static/
- OASIS Static Analysis Results Interchange Format (SARIF) TC
	- Defining a standard output format for static analysis tools
	- https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=sarif
	- https://github.com/oasis-tcs/sarif-spec
	- Static Analysis Results: A Format and a Protocol: SARIF & SASP
		- https://blogs.grammatech.com/static-analysis-results-a-format-and-a-protocol-sarif-sasp
	- Integration of the Static Analysis Results Interchange Format in CogniCrypt
		- 2019 arXiv
		- Sriteja Kummita, Goran Piskachev
		- https://arxiv.org/abs/1907.02558
- On the Relationship Between Static Analysis and Type Theory
	- https://semantic-domain.blogspot.com/2019/08/on-relationship-between-static-analysis.html

## Readings: Books

- Static Program Analysis
	- Anders Møller, Michael I. Schwartzbach
	- https://cs.au.dk/~amoeller/spa/

## Readings: Research

- Static Analysis Symposia Central Site
	- http://staticanalysis.org/
- A Few Billion Lines of Code Later: Using Static Analysis to Find Bugs in the Real World
	- Communications of the ACM, Vol. 53 No. 2, 2010
	- Al Bessey, Ken Block, Ben Chelf, Andy Chou, Bryan Fulton, Seth Hallem, Charles Henri-Gros, Asya Kamsky, Scott McPeak, Dawson Engler
	- https://cacm.acm.org/magazines/2010/2/69354-a-few-billion-lines-of-code-later/fulltext
- Automated Program Transformation for Improving Software Quality
	- 2019 PhD Dissertation; Rijnard van Tonder
	- https://rijnard.com/pdfs/dissertation-rijnard.pdf
- How to Build Static Checking Systems Using Orders of Magnitude Less Code
	- ASPLOS 2016
	- Fraser Brown, Andres Nötzli, Dawson Engler
	- https://web.stanford.edu/~mlfbrown/paper.pdf
	- http://lambda-the-ultimate.org/node/5348
	- https://blog.acolyer.org/2016/05/31/how-to-build-static-checking-systems-using-orders-of-magnitude-less-code/
- Lessons from Building Static Analysis Tools at Google
	- Communications of the ACM, Vol. 61 No. 4, 2018
	- Caitlin Sadowski, Edward Aftandilian, Alex Eagle, Liam Miller-Cushon, Ciera Jaspan
	- https://cacm.acm.org/magazines/2018/4/226371-lessons-from-building-static-analysis-tools-at-google/abstract
	- https://research.google.com/pubs/pub46576.html
- Object Model Construction for Inheritance in C++ and Its Applications to Program Analysis
	- Compiler Construction (CC) 2012
	- Yang, Jing, Gogul Balakrishnan, Naoto Maeda, Franjo Ivancic, Aarti Gupta, Nishant Sinha, Sriram Sankaranarayanan, Naveen Sharma
	- https://dl.acm.org/citation.cfm?id=2259241
	- http://pages.cs.wisc.edu/~bgogul/Research/Papers/cc12.html
	- https://www.semanticscholar.org/paper/Object-Model-Construction-for-Inheritance-in-C%2B%2B-a-Yang-Balakrishnan/510501c7051c03d5e2a70089deeda8dfc3a7304f
	- https://www.cs.colorado.edu/~srirams/papers/cc12-final.pdf
	- http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.225.2429
- Scaling Static Analyses at Facebook
	- Dino Distefano, Manuel Fähndrich, Francesco Logozzo, Peter W. O'Hearn
	- Communications of the ACM, Vol. 62 No. 8, 2019
	- https://cacm.acm.org/magazines/2019/8/238344-scaling-static-analyses-at-facebook/fulltext
- Source Language Representation of Function Summaries in Static Analysis
	- ICOOOLPS / ECOOP 2016
	- Gábor Horváth, Norbert Pataki
	- https://2016.ecoop.org/event/icooolps-2016-source-language-representation-of-function-summaries-in-static-analysis
- Sys: a Static/Symbolic Tool for Finding Good Bugs in Good (Browser) Code
	- USENIX Security Symposium 2020
	- Fraser Brown, Deian Stefan, Dawson Engler
	- https://cseweb.ucsd.edu/~dstefan/pubs/brown:2020:sys.pdf
	- https://sys.programming.systems/
	- Sys: a Static/Symbolic Tool for Finding Good Bugs in Good (Browser) Code
		- https://github.com/PLSysSec/sys
- Tailoring Programs for Static Analysis via Program Transformation
	- International Conference on Software Engineering (ICSE) 2020
	- Rijnard van Tonder and Claire Le Goues
	- https://rijnard.com/pdfs/tailoring-analysis-icse-2020.pdf
- Toward Full Elasticity in Distributed Static Analysis
	- 2016 Microsoft Research Technical Report: MSR-TR-2015-88
	- Diego Garbervetsky, Edgardo Zoppi, Thomas Ball, Ben Livshits
	- https://www.microsoft.com/en-us/research/publication/toward-full-elasticity-distributed-static-analysis/
- Undecidability of static analysis
	- ACM Letters on Programming Languages and Systems (LOPLAS) Volume 1 Issue 4, Dec. 1992
	- William Landi
	- https://dl.acm.org/citation.cfm?id=161501
	- "Two fundamental static-analysis problems are may alias and must alias. The former is not recursive (is undecidable), and the latter is not recursively enumerable (is uncomputable), even when all paths are executable in the program being analyzed for languages with if statements, loops, dynamic storage, and recursive data structures."

## Readings: Research: Correctness

_Testing, Validation, Verification_

See also: [Compilers Correctness](https://github.com/MattPD/cpplinks/blob/master/compilers.correctness.md)

- Differentially testing soundness and precision of program analyzers
	- International Symposium on Software Testing and Analysis 2019
	- Christian Klinger, Maria Christakis, Valentin Wüstholz
	- https://arxiv.org/abs/1812.05033
- Quickchecking Static Analysis Properties
	- Testing, Verification and Reliability 27(6) 2017
	- Jan Midtgaard, Anders Møller
	- http://janmidtgaard.dk/papers/Midtgaard-Moeller%3aSTVR17.pdf
- Test suites for benchmarks of static analysis tools
	- Software Reliability Engineering Workshops (ISSREW) 2015
	- Shinichi Shiraishi, Veena Mohan, Hemalatha Marimuthu
	- http://ieeexplore.ieee.org/document/7392027/
- Testing Static Analyses for Precision and Soundness
	- CGO 2020
	- Jubi Taneja, Zhengyang Liu, and John Regehr
	- https://doi.org/10.1145/3368826.3377927
- Testing Static Analyzers with Randomly Generated Programs
	- NFM 2012: NASA Formal Methods
	- Pascal Cuoq, Benjamin Monate, Anne Pacalet, Virgile Prevosto, John Regehr, Boris Yakobowski, Xuejun Yang
	- https://www.cs.utah.edu/~regehr/papers/nfm12.pdf
- Towards Scalable Translation Validation of Static Analyzers
	- ROSAEC Technical Report ROSAEC-2014-003, Nov 2014
	- Jeehoon Kang, Sungkeun Cho, Joonwon Choi, Chung-Kil Hur, Kwangkeun Yi
	- http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.698.4724
	- http://rosaec.snu.ac.kr/publish/2014/techmemo/ROSAEC-2014-003.pdf
- Systematic Approaches for Increasing Soundness and Precision of Static Analyzers
	- State Of the Art in Program Analysis (SOAP) 2017
	- Esben Sparre Andreasen, Anders Møller, Benjamin Barslev Nielsen
	- https://pldi17.sigplan.org/event/soap-2017-papers-systematic-approaches-for-increasing-soundness-and-precision-of-static-analyzers
	- https://cs.au.dk/~amoeller/papers/tajsexperience/paper.pdf
- Verasco, a formally verified C static analyzer
	- A Formally-Verified C Static Analyzer
		- POPL 2015
		- Jacques-Henri Jourdan, Vincent Laporte, Sandrine Blazy, Xavier Leroy, David Pichardie
		- https://hal.inria.fr/hal-01078386
		- https://xavierleroy.org/publi/verasco-popl2015.pdf
	- Microsoft Research 2016; Jacques Henri Jourdan
		- "the design and soundness proof of Verasco, a formally verified static analyzer for most of the ISO C99 language (excluding recursion and dynamic allocation), developed using the Coq proof assistant."
		- https://www.youtube.com/watch?v=0pUueg3Dslo
	- Checking a Checker - Verasco: a Formally Verified C Static Analyzer
		- 2016 PhD Dissertation; Jacques-Henri Jourdan
		- https://jhjourdan.mketjh.fr/thesis_jhjourdan.pdf
- Verified Translation Validation of Static Analyses
	- Computer Security Foundations Symposium 2017
	- Gilles Barthe, Sandrine Blazy, Vincent Laporte, David Pichardie, Alix Trieu
	- https://hal.inria.fr/hal-01588422/

---

# Benchmarking

_Benchmarks & comparisons_

- A Comparison of Static Analysis Tools for Vulnerability Detection in C/C++ Code
	- SYNASC 2017
	- Andrei Arusoaie, Ștefan Ciobâcă, Vlad Crăciun, Dragoș Gavriluț, Dorel Lucanu
	- https://profs.info.uaic.ro/~stefan.ciobaca/synasc2017.pdf
- Analyzing the State of Static Analysis: A Large-Scale Evaluation in Open Source Software
	- Software Analysis, Evolution, and Reengineering (SANER) 2016
	- http://ieeexplore.ieee.org/document/7476667/
	- https://www.slideshare.net/inventitech/analyzing-the-state-of-static-analysis-a-largescale-evaluation-in-open-source-software-60473247
	- 2015 Master’s Thesis: https://repository.tudelft.nl/islandora/object/uuid:3d834130-8dd7-420a-9af9-6e77761cdad6/
- Automated Customized Bug-Benchmark Generation
	- IEEE SCAM 2019
	- Vineeth Kashyap, Jason Ruchti, Lucja Kot, Emma Turetsky, Rebecca Swords, David Melski, Eric Schulte
	- https://arxiv.org/abs/1901.02819
	- https://www.dropbox.com/sh/f3p1wbomv93fz78/AABzXcLzqp5zkx75nQym6gJPa
- Benchmark Software for Evaluation of Software Analysis Tools
	- http://web.archive.org/web/20180611162911/https://github.com/Toyota-ITC-SSD/Software-Analysis-Benchmark
	- Static analysis benchmarks from Toyota ITC - https://github.com/regehr/itc-benchmarks
- How Toyota Picks Software Tools
	- EETimes, August 11, 2015; Bernard Cole
	- http://web.archive.org/web/20150815120014/http://www.eetimes.com/author.asp?section_id=36&doc_id=1327387
- Quantitative Evaluation of Static Analysis Tools
	- Software Reliability Engineering Workshops (ISSREW) 2014
	- Shinichi Shiraishi, Veena Mohan, Hemalatha Marimuthu
	- https://dl.acm.org/citation.cfm?id=2706360
- Software Assurance Reference Dataset (SARD)
	- https://samate.nist.gov/SARD/
	- Test Suites - https://samate.nist.gov/SRD/testsuite.php
- Static Analysis Benchmarks
	- https://blog.regehr.org/archives/1217
- Test Suites for Benchmarks of Static Analysis Tools
	- IEEE International Symposium on Software Reliability Engineering (ISSRE) 2015
	- Shinichi Shiraishi, Veena Mohan, and Hemalatha Marimuthu
	- https://www.researchgate.net/publication/283548090_Test_Suites_for_Benchmarks_of_Static_Analysis_Tools
- Towards Automatically Generating a Sound and Complete Dataset for Evaluating Static Analysis Tools
	- NDSS Workshop on Binary Analysis Research (BAR) 2019
	- Aravind Machiry, Nilo Redini, Eric Gustafson, Hojjat Aghakhani, Christopher Kruegel, Giovanni Vigna
	- https://ruoyuwang.me/bar2019/pdfs/bar2019-final90.pdf
	- https://github.com/ucsb-seclab/autofacts
- Toyota ITC Benchmark
	- https://runtimeverification.com/match/1.0-SNAPSHOT/docs/benchmark/
- Using Benchmarks to Assess Static Analysis Tools
	- http://blogs.grammatech.com/using-benchmarks-to-assess-static-analysis-tools

---

# Software

- BDE Verify: A Static Checker for C++
	- https://github.com/bloomberg/bde_verify
	- https://bloomberg.github.io/bde_verify/
- CodeChecker: an analyzer tooling, defect database and viewer extension for the Clang Static Analyzer and Clang Tidy
	- https://github.com/Ericsson/codechecker
- Cppcheck: A tool for static C/C++ code analysis
	- http://cppcheck.sourceforge.net/
	- https://github.com/danmar/cppcheck
- cpplint: static code checker for C++
	- https://github.com/cpplint/cpplint
- Crab: A Language-Agnostic Library for Static Analysis
	- https://github.com/seahorn/crab
	- Crab-llvm: Abstract Interpretation of LLVM bitcode
		- https://github.com/seahorn/crab-llvm
- IKOS: Inference Kernel for Open Static Analyzers
	- Static analyzer for C/C++ based on the theory of Abstract Interpretation.
	- https://github.com/NASA-SW-VnV/ikos
- Infer Static Analyzer: A static analyzer for Java, C, C++, and Objective-C
	- http://fbinfer.com/
	- https://github.com/facebook/infer
- Phasar: A LLVM-based static code analysis framework
	- http://phasar.org/
	- https://github.com/secure-software-engineering/phasar
	- Static Analysis for C++ with Phasar
		- https://pldi18.sigplan.org/event/pldi-2018-pldi-tutorials-static-analysis-for-c-with-phasar
	- PhASAR: An Inter-Procedural Static Analysis Framework for C/C++
		- TACAS 2019
		- Philipp D. Schubert, Ben Hermann, Eric Bodden
		- http://www.thewhitespace.de/publications/shb19-phasar.pdf
- Semmle QL
	- https://github.com/Semmle/ql
	- Vulnerability hunting with Semmle QL, part 1
		- https://blogs.technet.microsoft.com/srd/2018/08/16/vulnerability-hunting-with-semmle-ql-part-1/
- SPARTA: a library that provides the basic blocks for building high-performance static code analyzers based on Abstract Interpretation
	- https://github.com/facebookincubator/SPARTA
	- SPARTA: a C++ library of software components for building high-performance static analyzers
		- https://code.fb.com/open-source/sparta/
	- Easy Abstract Interpretation with SPARTA
		- Strange Loop 2019; Arnaud Venet and Jez Ng
		- https://www.youtube.com/watch?v=_fA7vkVJhF8
		- https://thestrangeloop.com/2019/easy-abstract-interpretation-with-sparta.html
- Verasco: a formally verified C static analyzer
	- static analyzer for the CompCert subset of ISO C 1999 that establishes the absence of run-time errors in analyzed programs
	- entirely specified and proved sound using the Coq proof assistant
	- http://compcert.inria.fr/verasco/

## Software: Compilers

- Clang
	- Clang Static Analyzer
		- http://clang-analyzer.llvm.org/
		- Checker Developer Manual
			- http://clang-analyzer.llvm.org/checker_dev_manual.html
		- A survey of dataflow analyses in Clang
			- 2020; Kristóf Umann
			- https://lists.llvm.org/pipermail/cfe-dev/2020-October/066937.html
		- An in-depth look at Liveness Analysis in the Clang Static Analyzer
			- 2020; Kristóf Umann
			- http://lists.llvm.org/pipermail/cfe-dev/2020-July/066330.html
		- Clang Static Analysis
			- Meeting C++ 2016; Gabor Horvath
			- https://www.youtube.com/watch?v=UcxF6CVueDM
		- Clang Static Analyzer - A Checker Developer's Guide.
			- https://github.com/haoNoQ/clang-analyzer-guide
		- Detecting Uninitialized Variables in C++ with the Clang Static Analyzer
			- Acta Cybernetica 2020
			- Kristóf Umann, Zoltán Porkoláb
			- https://doi.org/10.14232/actacyb.282900
			- https://clang.llvm.org/docs/analyzer/checkers.html#optin-cplusplus-uninitializedobject-c
		- Faster, Stronger C++ Analysis with the Clang Static Analyzer
			- 2018 LLVM Developers’ Meeting; George Karpenkov, Artem Dergachev
			- https://www.youtube.com/watch?v=4n3l-ZcDJNY
		- Using the Clang Static Analyzer to Find Bugs
			- 2020 LLVM Developers’ Meeting; Vince Bridgers
			- https://www.youtube.com/watch?v=nTslG8HtKeA
			- https://llvm.org/devmtg/2020-09/slides/Using_the_clang_static_ananalyzer_to_find_bugs.pdf
	- Clang-Tidy: Clang-based C++ “linter” tool
		- http://clang.llvm.org/extra/clang-tidy/
		- Clang-Tidy - KDAB
			- part 1: Modernize your source code using C++11/C++14 - https://www.kdab.com/clang-tidy-part-1-modernize-source-code-using-c11c14/
			- part 2: Integrate qmake and other build systems using Bear - https://www.kdab.com/clang-tidy-part-2-integrate-qmake-and-other-build-systems-using-bear/
		- How to use Clang Tidy to automatically correct code
			- https://github.com/KratosMultiphysics/Kratos/wiki/How-to-use-Clang-Tidy-to-automatically-correct-code
		- Intro to clang-tidy - C++ Weekly - Ep 3
			- https://www.youtube.com/watch?v=OchPaGEH4TE
			- Using Clang-Tidy for Customized Checkers and Large Scale Source Tree Refactoring
				- 2020 LLVM Developers’ Meeting; Vince Bridgers
				- https://www.youtube.com/watch?v=UfLH7dORav8
				- https://llvm.org/devmtg/2020-09/slides/LLVM-Virtual-Presentation-Clang-Tidy.pdf
	- Clang Thread Safety Analysis
		- https://clang.llvm.org/docs/ThreadSafetyAnalysis.html
		- C/C++ Thread Safety Analysis
			- DeLesley Hutchins, Aaron Ballman, Dean Sutherland
			- 2014 IEEE 14th International Working Conference on Source Code Analysis and Manipulation
			- https://research.google/pubs/pub42958/
		- Thread Safety Analysis in C and C++
			- https://insights.sei.cmu.edu/sei_blog/2014/10/thread-safety-analysis-in-c-and-c.html
		- Thread Safety Annotations in Clang
			- DeLesley Hutchins
			- 2011 LLVM Developers' Meeting; https://llvm.org/devmtg/2011-11/Hutchins_ThreadSafety.pdf
			- https://www.youtube.com/watch?v=5Xx0zktqSs4
- GCC
	- https://gcc.gnu.org/onlinedocs/gcc/Static-Analyzer-Options.html
	- https://gcc.gnu.org/wiki/DavidMalcolm/StaticAnalyzer
	- Static analysis in GCC 10
		- https://developers.redhat.com/blog/2020/03/26/static-analysis-in-gcc-10/
	- Static analysis updates in GCC 11
		- https://developers.redhat.com/blog/2021/01/28/static-analysis-updates-in-gcc-11/
	- Detecting memory management bugs with GCC 11
		- Part 1: Understanding dynamic allocation
			- https://developers.redhat.com/blog/2021/04/30/detecting-memory-management-bugs-with-gcc-11-part-1-understanding-dynamic-allocation/
- Visual C++
	- /analyze (Code analysis)
		- https://docs.microsoft.com/en-us/cpp/build/reference/analyze-code-analysis
	- Source Code Annotation Language (SAL)
		- https://docs.microsoft.com/en-us/visualstudio/code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects
		- Salieri: Source-code annotation language (SAL) compatibility header
			- https://github.com/nemequ/salieri

---

# Verification

_Verification & Model Checking_

- Formal Verification to Ensuring the Memory Safety of C++ Programs
	- 2020 M.Sc. Thesis; Felipe R. Monteiro
	- https://feliperodri.github.io/papers/msc-manuscript.pdf
	- https://feliperodri.github.io/talks/msc-presentation.pdf
	- Apply model checking techniques to ensuring memory safety of C++ programs:
		- (i) Provide a logical formalization of essential features that the C++ programming language offers, such as templates, sequential and associative containers, inheritance, polymorphism, and exception handling.
		- (ii) Provide a set of abstractions to the Standard C++ Libraries that reflects their semantics, in order to enable the verification of functional properties related to the use of these libraries.
		- (iii) Extend an existing verifier to handle the verification of C++ programs based on (i) and (ii) and evaluate its efficiency and effectiveness in comparison to similar state-of-the-art approaches.
- Model Checking a C++ Software Framework, a Case Study
	- European Software Engineering Conference / Foundations of Software Engineering (ESEC/FSE) 2019
	- John Lång, I.S.W.B. Prasetya
	- https://arxiv.org/abs/1907.00172

## Verification: Software

See also: [Program Analysis](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef) - [LLVM](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef#llvm) - [Verification](https://gist.github.com/MattPD/00573ee14bf85ccac6bed3c0678ddbef#llvm---verification)

- CMBC: C Bounded Model Checker
	- Bounded Model Checker for C and C++ programs
	- http://www.cprover.org/cbmc/
	- https://github.com/diffblue/cbmc
- DIVINE
	- DIVINE is a modern, explicit-state model checker. Based on the LLVM toolchain, it can verify programs written in multiple real-world programming languages, including C and C++.
	- https://divine.fi.muni.cz/
- ESBMC
	- ESBMC is an open source, permissively licensed, context-bounded model checker based on satisfiability modulo theories for the verification of single- and multi-threaded C/C++ programs.
	- https://github.com/esbmc/esbmc
	- https://ssvlab.github.io/esbmc/
- Symbiotic
	- Tool for verifying computer programs based on instrumentation, program slicing and symbolic executor KLEE.
	- http://staticafi.github.io/symbiotic/
