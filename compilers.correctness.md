# [C++ links](README.md): compilers - correctness

See also:

- [Compilers](compilers.md)
- [Debugging](https://github.com/MattPD/cpplinks/blob/master/debugging.md): [Implementation](https://github.com/MattPD/cpplinks/blob/master/debugging.md#implementation): [Correctness](https://github.com/MattPD/cpplinks/blob/master/debugging.md#correctness)

# Contents

- [General](#general)
	- [Debugging](#debugging)
	- [History](#history)
	- [Lectures](#lectures)
- [Calculation](#calculation)
- [Testing](#testing)
	- [Readings](#testing-readings):
		- [Performance Optimization](#testing-readings-performance-optimization): [Loops](#testing-readings-performance-optimization-loops), [Vectorization](#testing-readings-performance-optimization-vectorization)
		- [Reduction](#testing-readings-reduction): [LLVM](#testing-readings-reduction-llvm)
	- [Software](#testing-software):
		- [Generation](#testing-software-generation)
		- [Performance Optimization](#testing-software-performance-optimization): [Parallelization](#testing-software-performance-optimization-parallelization), [Vectorization](#testing-software-performance-optimization-vectorization)
		- [Reduction](#testing-software-reduction)
	- [Talks](#testing-talks)
- [Type Preservation](#type-preservation)
- [Validation](#validation)
- [Verification](#verification)
	- [Talks](#verification-talks)

---

# General

- ACM SIGPLAN Conference on Certified Programs and Proofs (CPP) - http://dblp.org/db/conf/cpp/
- Black-Box Equivalence Checking Across Compiler Transformations
	- 2018 PhD thesis; Manjeet Dahiya
	- https://www.cse.iitd.ac.in/~sbansal/pubs/manjeet_thesis.pdf
- Compiling with Proofs
	- 1998 Ph.D. Thesis; George C. Necula
	- https://people.eecs.berkeley.edu/~necula/Papers/thesis.pdf
- Compilers and Termination Revisited
	- https://blog.regehr.org/archives/161
- Correct by Construction Language Implementations
	- 2021 PhD Dissertation
	- Arjen Rouvoet
	- https://doi.org/10.4233/uuid:f0312839-3444-41ee-9313-b07b21b59c11
	- https://ajrouvoet.github.io/files/thesis.pdf
- Correctly Compiling Proofs About Programs Without Proving Compilers Correct
	- 15th International Conference on Interactive Theorem Proving (ITP 2024)
	- Audrey Seo, Chris Lam, Dan Grossman, Talia Ringer
	- https://doi.org/10.4230/LIPIcs.ITP.2024.28
	- https://dependenttyp.es/pdf/potpie.pdf
	- Potpie: Proof Object Transformation, Preserving Imp Embeddings: the first proof compiler to be formally proven correct
		- https://github.com/uwplse/potpie
- Defect Categorization in Compilers: A Multi-vocal Literature Review
	- ACM Computing Surveys (CSUR) 56(4):104 2024
	- Akond Rahman, Dibyendu Brinto Bose, Farhat Lamia Barsha, Rahul Pandita
	- https://dl.acm.org/doi/10.1145/3626313
	- https://akondrahman.github.io/files/papers/csur2024.pdf
- Formal Approaches to Secure Compilation: A Survey of Fully Abstract Compilation and Related Work
	- ACM Computing Surveys (CSUR) 51(6) 2019
	- Marco Patrignani, Amal Ahmed, Dave Clarke
	- https://doi.org/10.1145/3280984
	- http://theory.stanford.edu/~mp/mp/Publications_files/a125-patrignani.pdf
	- http://theory.stanford.edu/~mp/mp/Publications_files/main-full.pdf
- Generating Compiler Optimizations from Proofs
	- POPL 2010
	- Ross Tate, Michael Stepp, Sorin Lerner
	- https://doi.org/10.1145/1707801.1706345
	- https://www.cs.cornell.edu/~ross/publications/proofgen/
	- https://cseweb.ucsd.edu/~lerner/papers/popl10.html
- How to prove a compiler correct - Daniel Patterson
	- https://dbp.io/essays/2018-01-16-how-to-prove-a-compiler-correct.html
	- https://github.com/dbp/howtoproveacompiler
- How to prove a compiler fully abstract
	- https://dbp.io/essays/2018-04-19-how-to-prove-a-compiler-fully-abstract.html
- Operational Refinement for Compiler Correctness
	- 2012 PhD Dissertation; Robert W. Dockins
	- https://arks.princeton.edu/ark:/88435/dsp01rr171x259
	- ftp://ftp.cs.princeton.edu/reports/2012/936.pdf
- Some Goals for High-impact Verified Compiler Research - https://blog.regehr.org/archives/1565
- The Next 700 Compiler Correctness Theorems (Functional Pearl)
	- ICFP 2019
	- Daniel Patterson, Amal Ahmed
	- https://icfp19.sigplan.org/details/icfp-2019-papers/35/The-Next-700-Compiler-Correctness-Theorems-A-Functional-Pearl-
	- https://dbp.io/pubs/2019/ccc/
	- https://www.ccs.neu.edu/home/amal/papers/next700ccc.pdf
	- https://www.youtube.com/watch?v=qrwzpo6ISCQ
- Towards Understanding Tool-chain Bugs in the LLVM Compiler Infrastructure
	- IEEE International Conference on Software Analysis, Evolution and Reengineering (SANER) 2021
	- Xiaoyuan Xie, Haolin Yang, Qiang He, Lin Chen
	- https://doi.org/10.1109/SANER50967.2021.00010
	- https://www.youtube.com/watch?v=tWb9zwRH-1g
	- https://github.com/DataProvided/Tool-chain-Bugs-Data
- Well-Typed Programs Can Go Wrong: A Study of Typing-Related Bugs in JVM Compilers
	- OOPSLA 2021
	- Stefanos Chaliasos, Thodoris Sotiropoulos, Georrgios-Petros Drosos, Charalambos Mitropoulos, Dimitris Mitropoulos, Diomidis Spinellis
	- https://dimitro.gr/assets/papers/CSDMMS21.pdf
- What even is compiler correctness? - https://www.williamjbowman.com/blog/2017/03/24/what-even-is-compiler-correctness/
- Why Do Peephole Optimizations Work?
	- 2023; John Regehr
	- https://blog.regehr.org/archives/2485
- Write Your Compiler by Proving It Correct - http://liamoc.net/posts/2015-08-23-verified-compiler.html

## Debugging

Debugging of compilers bugs

See also: Section 6.3 (Compiler Bug Debugging) in ["A Survey of Compiler Testing"](https://software-lab.org/publications/csur2019_compiler_testing.pdf); [Compilers Correctness](https://github.com/MattPD/cpplinks/blob/master/compilers.correctness.md): [Testing](https://github.com/MattPD/cpplinks/blob/master/compilers.correctness.md#testing): [Reduction](https://github.com/MattPD/cpplinks/blob/master/compilers.correctness.md#testing-readings-reduction); [Debugging](https://github.com/MattPD/cpplinks/blob/master/debugging.md): [Readings](https://github.com/MattPD/cpplinks/blob/master/debugging.md#readings): Delta Debugging

- Automatic Isolation of Compiler Errors
	- ACM Transactions on Programming Languages and Systems (TOPLAS) 16(5) 1994
	- David Whalley
	- https://www.cs.fsu.edu/~whalley/papers/acmtoplas94.pdf
- Bugfind: A Tool for Debugging Optimizing Compilers
	- ACM SIGPLAN Notices 25, no. 1 (1990)
	- Jacqueline M. Caron, Peter A. Darnell
	- https://doi.org/10.1145/74105.74106
- Compiler Bug Isolation via Effective Witness Test Program Generation
	- ESEC/FSE 2019
	- Junjie Chen, Jiaqi Han, Peiyi Sun, Lingming Zhang, Dan Hao, Lu Zhang
	- https://dl.acm.org/citation.cfm?id=3338957
	- https://personal.utdallas.edu/~lxz144130/publications/fse2019.pdf
	- DiWi (Diversified Witnesses)
		- https://github.com/JunjieChen/DiWi
- Debugging compilers with optimization fuel
	- 2011
	- Edward Z. Yang
	- http://blog.ezyang.com/2011/06/debugging-compilers-with-optimization-fuel/
- GCC Wiki: Finding miscompilations on large testcases
	- https://gcc.gnu.org/wiki/Analysing_Large_Testcases
- Replay Compilation: Improving Debuggability of a Just-in-Time Compiler
	- OOPSLA 2006
	- Kazunori Ogata, Tamiya Onodera, Kiyokuni Kawachiya, Hideaki Komatsu, Toshio Nakatani
	- https://doi.org/10.1145/1167473.1167493
	- https://www.researchgate.net/publication/221321785_Replay_compilation_Improving_debuggability_of_a_just-in-time_compiler
- Toward Automatic Debugging of Compilers
	- International Joint Conference on Artificial Intelligence 1977
	- Hanan Samet
	- http://www.cs.umd.edu/~hjs/pubs/compilers/toward-automatic-debugging.pdf
- Type-Based Verification of Assembly Language for Compiler Debugging
	- ACM SIGPLAN Workshop on Types in Language Design and Implementation (TLDI) 2005
	- Bor-Yuh Evan Chang, Adam Chlipala, George C. Necula, Robert R. Schneck
	- http://adam.chlipala.net/papers/CoolaidTLDI05/

### Debugging: 2023

- FuzzyFlow: Leveraging Dataflow To Find and Squash Program Optimization Bugs
	- International Conference for High Performance Computing, Networking, Storage and Analysis (SC) 2023
	- Philipp Schaad, Timo Schneider, Tal Ben-Nun, Alexandru Calotoiu, Alexandros Nikolaos Ziogas, Torsten Hoefler
	- https://arxiv.org/abs/2306.16178
	- https://dl.acm.org/doi/10.1145/3581784.3613214
- MLIR Actions: Tracing and Debugging MLIR-based Compilers
	- RFC
		- https://discourse.llvm.org/t/rfc-mlir-action-tracing-and-debugging-mlir-based-compilers/68679
	- Open MLIR Meeting 2023-02-23; Mehdi Amini
		- https://www.youtube.com/watch?v=ayQSyekVa3c
- OrdinalFix: Fixing Compilation Errors via Shortest-Path CFL Reachability with Attribute Checking
	- IEEE/ACM International Conference on Automated Software Engineering (ASE) 2023
	- Wenjie Zhang, Guancheng Wang, Junjie Chen, Yingfei Xiong, Yong Liu, Lu Zhang
	- https://arxiv.org/abs/2309.06771
	- https://github.com/myxxxsquared/OrdinalFix
	- https://conf.researchr.org/details/ase-2023/ase-2023-papers/44/OrdinalFix-Fixing-Compilation-Errors-via-Shortest-Path-CFL-Reachability-with-Attribu
- Silent Compiler Bug De-duplication via Three-Dimensional Analysis
	- ACM SIGSOFT International Symposium on Software Testing and Analysis (ISSTA) 2023
	- Chen Yang, Junjie Chen, Xingyu Fan, Jiajun Jiang, Jun Sun
	- https://dl.acm.org/doi/abs/10.1145/3597926.3598087
	- https://2023.issta.org/details/issta-2023-technical-papers/47/Silent-Compiler-Bug-De-duplication-via-Three-Dimensional-Analysis
	- "In this work, we propose a novel technique (called D3) to solve the duplication problem on silent compiler bugs. Its key insight is to characterize the silent bugs from the testing process and identify three-dimensional information (i.e., test program, optimizations, and test execution) for bug de-duplication."

### Debugging: 2022

- LocSeq: Automated Localization for Compiler Optimization Sequence Bugs of LLVM
	- IEEE Transactions on Reliability 2022
	- Zhide Zhou, He Jiang, Zhilei Ren, Yuting Chen, Lei Qiao
	- https://ieeexplore.ieee.org/abstract/document/9765328
	- https://gitee.com/teazhou/loc-seq
- Modeling Code Manipulation in JIT Compilers
	- SOAP 2022: ACM SIGPLAN International Workshop on the State Of the Art in Program Analysis
	- HeuiChan Lim, Xiyu Kang, Saumya Debray
	- https://doi.org/10.1145/3520313.3534656
	- "This paper discusses a different approach to analyzing JIT compiler optimization behaviors, based on using dynamic analysis to construct abstract models of the JIT compiler’s optimizer and back end. By comparing the models obtained for buggy and non-buggy executions of the JIT compiler, we can pinpoint the components of the JIT compiler’s internal representation that have been affected by the bug; this can then be mapped back to identify the buggy code."

### Debugging: 2021

- Automated Bug Localization in JIT Compilers
	- Virtual Execution Environments (VEE) 2021
	- HeuiChan Lim, Saumya Debray
	- https://dl.acm.org/doi/10.1145/3453933.3454021

### Debugging: 2020

- Enhanced Compiler Bug Isolation via Memoized Search
	- ASE 2020
	- Junjie Chen, Haoyang Ma, Lingming Zhang
	- https://www.youtube.com/watch?v=G8Ev6hujI6g
	- https://lingming.cs.illinois.edu/publications/ase2020b.pdf
	- https://conf.researchr.org/details/ase-2020/ase-2020-papers/36/Enhanced-Compiler-Bug-Isolation-via-Memoized-Search
	- RecBi: Reinforcement compiler Bug isolation
		- https://github.com/haoyang9804/RecBi
- Locating a compiler bug with git bisection
	- 2020; William Woodruff
	- https://blog.yossarian.net/2020/05/07/Locating-a-compiler-bug-with-git-bisection
- Using Mutants to Help Developers Distinguish and Debug (Compiler) Faults
	- Journal of Software Testing, Verification, and Reliability (STVR) Volume 30, Issue 2 (2020)
	- Josie Holmes and Alex Groce
	- https://agroce.github.io/stvr20.pdf
	- https://github.com/agroce/compilermutants

## History

- Advice on Structuring Compilers and Proving Them Correct
	- Principles of Programming Languages (POPL) 1973
	- F. Lockwood Morris
	- https://dl.acm.org/citation.cfm?id=512941
- Compiler Correctness Proofs
	- Papers on Compiler Correctness and Related Topics - Mitchell Wand et al.
	- https://www.ccs.neu.edu/home/wand/compiler-correctness-papers.html
	- "Our work of the early 80's (POPL 1982, 1983; TOPLAS 1982; I&C 1983) established a flexible method for the correctness of semantics-based compilers. We spent most of the rest that decade trying to make that development more applicable. As part of a cooperative project with the Mitre Corporation, we applied this technique to prove the correctness of a compiler for PreScheme, a dialect of Scheme tailored for systems programming, as part of a verified implementation of Scheme called VLisp. This research was published as a special double issue of the journal Lisp and Symbolic Computation. At the time, this was the largest compiler-correctness project ever attempted."
	- Research Interests
		- https://www.ccs.neu.edu/home/wand/research.html
- Compiler Verification: A Bibliography
	- ACM SIGSOFT Software Engineering Notes 28(6) 2003
	- Maulik A. Dave
	- https://dl.acm.org/citation.cfm?id=966235
	- https://web.archive.org/http://www.cs.utah.edu/~skchoe/research/p2-dave.pdf
	- https://www.semanticscholar.org/paper/Compiler-verification%3A-a-bibliography-Dave/36e028f88fc56eaf919b6d96c7a087c102ad4569
	- Compiler Verification: A Brief History - http://web.archive.org/web/20090807085152/http://www.geocities.com/compiler00/dave1.html
- Correctness of a Compiler for Algol-like Programs
	- Stanford Artificial Intelligence Memo No. 48 (1967)
	- Donald M. Kaplan
	- https://exhibits.stanford.edu/ai/catalog/hk625xv7120
- Correctness of a Compiler for Arithmetic Expressions
	- Mathematical Aspects of Computer Science (1) 1967
	- John McCarthy and James A. Painter
	- http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.76.7835
	- http://www-formal.stanford.edu/jmc/mcpain.html
- Formalising Meaning: a History of Programming Language Semantics
	- 2019 PhD dissertation; Troy Kaighin Astarte
	- http://homepages.cs.ncl.ac.uk/t.astarte/res/pdf/TK_Astarte_Formalising_Meaning_2019.pdf
- More on Advice on Structuring Compilers and Proving them Correct
	- James W. Thatcher, Eric G. Wagner and Jesse B. Wright
	- Theoretical Computer Science, Volume 15, Issue 3, 1981
		- https://doi.org/10.1016/0304-3975(81)90080-3
	- SDCG 1980: Semantics-Directed Compiler Generation
		- https://doi.org/10.1007/3-540-10250-7_22
- Toward Compiler Implementation Correctness Proofs
	- ACM Transactions on Programming Languages and Systems (TOPLAS) 8(2) 1986
	- Laurian M. Chirica, David F. Martin
	- https://doi.org/10.1145/5397.30847

## Lectures

- Compiler Verification: The Next Generation
	- PurPL Fest 2019; Amal Ahmed
	- https://www.youtube.com/watch?v=KcOxdyq1vs0
- OPLSS (Oregon Programming Languages Summer School)
	- 2019 - https://www.cs.uoregon.edu/research/summerschool/summer19/topics.php
		- Secure Compilation - Amal Ahmed
			- https://www.youtube.com/playlist?list=PL0DsGHMPLUWXXWjqfRuA20FNnNXOTj_Wh
	- 2017 - https://www.cs.uoregon.edu/research/summerschool/summer17/topics.php
		- Correct and Secure Compilation for Multi-Language Software - Amal Ahmed
			- https://www.youtube.com/playlist?list=PL0DsGHMPLUWUSJ8_THYt6Jcu7Kgp2kjaP
	- 2016 - https://www.cs.uoregon.edu/research/summerschool/summer16/curriculum.php
		- Logical relations/Compiler verification - Amal Ahmed
			- https://www.youtube.com/playlist?list=PLiHLLF-foEexzqkMlTqzbbX_7V45MAXyX
	- 2015 - https://www.cs.uoregon.edu/research/summerschool/summer15/curriculum.html
		- Logical Relations - Amal Ahmed
			- https://www.youtube.com/playlist?list=PLiHLLF-foEex7BOvMbrbUFC9XgU7fZW66
	- 2014 - https://www.cs.uoregon.edu/research/summerschool/summer14/curriculum.html
		- Software Verification - Andrew Appel
	- 2013 - https://www.cs.uoregon.edu/research/summerschool/summer13/curriculum.html
		- Logical Relations - Amal Ahmed
		- Verifying LLVM Optimizations in Coq - Steve Zdancewic
	- 2012 - https://www.cs.uoregon.edu/research/summerschool/summer12/curriculum.html
		- Logical Relations - Amal Ahmed
		- Compiler verification - Xavier Leroy

---

# Calculation

## Calculation: 2020s

- Beyond Trees: Calculating Graph-Based Compilers
	- ICFP 2024
	- Patrick Bahr, Graham Hutton
	- https://doi.org/10.1145/3674638
	- https://www.cs.nott.ac.uk/~pszgmh/graphs.pdf
	- https://icfp24.sigplan.org/details/icfp-2024-papers/15/Beyond-Trees-Calculating-Graph-Based-Compilers
	- https://github.com/pa-ba/calc-graph-comp
- Calculating Compilers for Concurrency
	- International Conference on Functional Programming (ICFP) 2023
	- Patrick Bahr, Graham Hutton
	- https://dl.acm.org/doi/10.1145/3607855
	- https://www.cs.nott.ac.uk/~pszgmh/choice-trees.pdf
	- https://github.com/pa-ba/calculating-compilers-for-concurrency
- Calculating Correct Compilers II: Return of the Register Machines
	- Journal of Functional Programming 2020
	- Patrick Bahr and Graham Hutton
	- http://www.cs.nott.ac.uk/~pszgmh/bib.html#ccc2
- Calculating Dependently-Typed Compilers
	- International Conference on Functional Programming 2021
	- Mitchell Pickard, Graham Hutton
	- http://www.cs.nott.ac.uk/~pszgmh/well-typed.pdf
- Monadic Compiler Calculation
	- International Conference on Functional Programming (ICFP) 2022
	- Patrick Bahr, Graham Hutton
	- https://www.cs.nott.ac.uk/~pszgmh/ccc3.pdf
	- https://bahr.io/pubs/files/mococo-paper.pdf
	- https://github.com/pa-ba/monadic-compiler-calculation
	- https://icfp22.sigplan.org/details/icfp-2022-papers/4/Monadic-Compiler-Calculation

## Calculation: 2010s

- Abstracting Definitional Interpreters (Functional Pearl)
	- ICFP 2017
	- David Darais, Nicholas Labich, Phuc C. Nguyen, David Van Horn
	- https://arxiv.org/abs/1707.04755
	- https://plum-umd.github.io/abstracting-definitional-interpreters/
	- https://david.darais.com/assets/papers/abstracting-definitional-interpreters/adi.pdf
- Calculating Certified Compilers for Non-Deterministic Languages
	- MPC 2015: Mathematics of Program Construction
	- Patrick Bahr
	- https://bahr.io/pubs/entries/bahr15mpc.html
	- https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.709.7040&rep=rep1&type=pdf
- Calculating Correct Compilers
	- Journal of Functional Programming, Volume 25, September 2015
	- Patrick Bahr and Graham Hutton
	- http://www.cs.nott.ac.uk/~pszgmh/bib.html#ccc

## Calculation: 2000s

- From Interpreter to Compiler and Virtual Machine: A Functional Derivation
	- BRICS Report Series 10(14) 2003
	- Mads Sig Ager, Dariusz Biernacki, Olivier Danvy, Jan Midtgaard
	- https://doi.org/10.7146/brics.v10i14.21784

## Calculation: 1990s

- Calculating Compilers
	- 1992 PhD Dissertation
	- Erik Meijer
	- http://hdl.handle.net/2066/114054
	- https://web.archive.org/web/20120416010128/http://research.microsoft.com/en-us/um/people/emeijer/Papers/Thesis.pdf
- Deriving a Lazy Abstract Machine
	- Journal of Functional Programming 7(3) 1997
	- Peter Sestoft
	- https://doi.org/10.1017/S0956796897002712

## Calculation: 1980s

- Deriving Target Code as a Representation of Continuation Semantics
	- ACM Transactions on Programming Languages and Systems 4, 3 (1982)
	- Mitchell Wand
	- https://dl.acm.org/doi/10.1145/357172.357179

## Calculation: 1970s

- Definitional Interpreters for Higher-Order Programming Languages
	- Proceedings of the ACM Annual Conference 1972
	- John C. Reynolds
	- https://dl.acm.org/doi/10.1145/800194.805852
	- Definitional Interpreters Revisited
		- Higher-Order and Symbolic Computation, 11 (1998)
		- John C. Reynolds
		- https://homepages.inf.ed.ac.uk/wadler/papers/papers-we-love/reynolds-definitional-interpreters-revisited.pdf

---

# Type Preservation

- From System F to Typed Assembly Language
	- Greg Morrisett, David Walker, Karl Crary, Neal Glew
	- POPL 1998
		- https://doi.org/10.1145/268946.268954
	- ACM Transactions on Programming Languages and Systems (TOPLAS) 21(3) 1999
		- https://doi.org/10.1145/319301.319345
- Programming type-safe transformations using higher-order abstract syntax
	- Journal of Formalized Reasoning (JFR) 8, 1 (2015)
	- Olivier Savary Bélanger, Stefan Monnier, Brigitte Pientka
	- https://doi.org/10.6092/issn.1972-5787/5122
- Type-Preserving CPS Translation of Σ and Π Types is Not Not Possible
	- Principles of Programming Languages (POPL) 2018
	- William J. Bowman, Youyou Cong, Nick Rioux, Amal Ahmed
	- https://doi.org/10.1145/3158110
	- https://www.williamjbowman.com/#cps-sigma
	- https://popl18.sigplan.org/details/POPL-2018-papers/69/Type-Preserving-CPS-Translation-of-and-Types-is-Not-Not-Possible

## Type Preservation: Intrinsically Typed Compilation

- A Certified Type-Preserving Compiler from Lambda Calculus to Assembly Language
	- ACM SIGPLAN Conference on Programming Language Design and Implementation (PLDI) 2007
	- Adam Chlipala
	- https://doi.org/10.1145/1250734.1250742
	- http://adam.chlipala.net/papers/CtpcPLDI07/
	- Lambda Tamer: https://ltamer.sourceforge.net/
- A Type-Correct, Stack-Safe, Provably Correct, Expression Compiler in Epigram
	- 2006
	- James McKinna, Joel Wright
	- https://www.cs.tufts.edu/comp/150FP/archive/conor-mcbride/epigram-pearl.pdf
	- Epigram: http://www.e-pig.org/
- A Type-Preserving Compiler in Haskell
	- ACM SIGPLAN International Conference on Functional Programming (ICFP) 2008
	- Louis-Julien Guillemette, Stefan Monnier
	- https://doi.org/10.1145/1411204.1411218
	- https://www.iro.umontreal.ca/~monnier/icfp08.pdf
- An Intrinsically Typed Compiler for Algebraic Effect Handlers
	- ACM SIGPLAN International Workshop on Partial Evaluation and Program Manipulation (PEPM) 2024
	- Syouki Tsuyama, Youyou Cong, Hidehiko Masuhara
	- https://dl.acm.org/doi/abs/10.1145/3635800.3636968
	- https://prg.is.titech.ac.jp/papers/pdf/pepm2024-paper.pdf
	- https://www.youtube.com/watch?v=kPnk1BpYHuc
	- https://popl24.sigplan.org/details/pepm-2024/1/An-Intrinsically-Typed-Compiler-for-Algebraic-Effect-Handlers
	- https://github.com/prg-titech/Effect-Handler-Compiler
- Correct by Construction Language Implementations
	- 2021 PhD Dissertation
	- Arjen Rouvoet
	- https://doi.org/10.4233/uuid:f0312839-3444-41ee-9313-b07b21b59c11
	- https://pure.tudelft.nl/ws/portalfiles/portal/100792932/thesis.pdf
- Intrinsically Typed Compilation with Nameless Labels
	- POPL 2021
	- Arjen Rouvoet, Robbert Krebbers, Eelco Visser
	- https://doi.org/10.1145/3434303

## Type Preservation: Testing

- API-driven Program Synthesis for Testing Static Typing Implementations
	- POPL 2024
	- Thodoris Sotiropoulos, Stefanos Chaliasos, Zhendong Su
	- https://doi.org/10.1145/3632904
	- https://arxiv.org/abs/2311.04527
	- https://theosotr.github.io/assets/pdf/popl24.pdf
	- https://www.youtube.com/watch?v=lZws2_bhL58
	- Thalia: A framework for testing compilers' type checkers
		- https://github.com/hephaestus-compiler-project/thalia
- Experience Report: Applying Random Testing to a Base Type Environment
	- ICFP 2013
	- Vincent St-Amour, Neil Toronto
	- https://doi.org/10.1145/2500365.2500616
	- https://users.cs.northwestern.edu/~stamourv/papers/random-testing-base-type-environment.pdf
	- https://users.cs.northwestern.edu/~stamourv/slides/tr-random-testing-icfp13.pdf
- Finding Typing Compiler Bugs
	- PLDI 2022
	- Stefanos Chaliasos, Thodoris Sotiropoulos, Diomidis Spinellis, Arthur Gervais, Ben Livshits, Dimitris Mitropoulos
	- https://doi.org/10.1145/3519939.3523427
	- http://resolver.tudelft.nl/uuid:8661c485-5d4b-48c5-bba9-8bb21f72ff72
	- Hephaestus: A framework for testing compilers' type checkers
		- https://github.com/hephaestus-compiler-project/hephaestus
- Fuzzing the Rust Typechecker Using CLP
	- Automated Software Engineering (ASE) 2015
	- Kyle Dewey, Jared Roesch, Ben Hardekopf
	- https://ieeexplore.ieee.org/document/7372036
	- https://hardekbc.github.io/files/dewey15fuzzing.pdf
	- CLP: Constraint Logic Programming
	- lecture notes: Special Topics in Software Engineering
		- 2021
		- Jonathan Bell
		- https://neu-se.github.io/CS7580-Fall-2021/lecture-notes/23-rust/
- Generating Well-Typed Terms that are not "Useless"
	- POPL 2024
	- Justin Frank, Benjamin Quiring, Leonidas Lampropoulos
	- https://doi.org/10.1145/3632919
	- https://www.youtube.com/watch?v=KkE-wVqUbVQ
	- well-typed-term-generator: An OCaml generator for well-typed terms (that use their arguments)
		- https://github.com/bquiring/well-typed-term-generator
- Making Random Judgments: Automatically Generating Well-Typed Terms from the Definition of a Type-System
	- European Symposium on Programming (ESOP) 2015
	- Burke Fetscher, Koen Claessen, Michał Pałka, John Hughes, Robert Bruce Findler
	- http://users.eecs.northwestern.edu/~baf111/random-judgments/
	- https://users.cs.northwestern.edu/~robby/pubs/papers/esop2015-fcphf.pdf
	- https://link.springer.com/chapter/10.1007/978-3-662-46669-8_16

---

# Testing

See also: [Testing](https://github.com/MattPD/cpplinks/blob/master/testing.md)

- A Survey of Compiler Testing
	- ACM Computing Surveys (CSUR) 2019
	- Junjie Chen, Jibesh Patra, Michael Pradel, Yingfei Xiong, Hongyu Zhang, Dan Hao, Lu Zhang
	- https://software-lab.org/publications/csur2019_compiler_testing.pdf
- Dagstuhl Seminar 17502 – Testing and Verification of Compilers
	- December 2017
	- http://dagstuhl.de/17502
- EMI-based Compiler Testing - http://web.cs.ucdavis.edu/~su/emi-project/

## Testing: Readings

- An Empirical Comparison of Compiler Testing Techniques
	- International Conference on Software Engineering (ICSE 2016)
	- Junjie Chen, Wenxiang Hu, Dan Hao, Yingfei Xiong, Hongyu Zhang, Lu Zhang, Bing Xie
	- https://dl.acm.org/citation.cfm?id=2884878
	- https://xiongyingfei.github.io/papers/ICSE16.pdf
	- https://emponcc.github.io/
	- https://github.com/emponcc/emponcc.github.io/blob/master/CompilerTestingComparison.md
- Automatic Testing of Symbolic Execution Engines via Program Generation and Differential Testing
	- ASE 2017
	- Timotej Kapus, Cristian Cadar
	- https://srg.doc.ic.ac.uk/files/papers/symex-engine-tester-ase-17.pdf
- Checking Correctness of Code Generator Architecture Specifications
	- Code Generation and Optimization (CGO) 2015
	- N. Hasabnis, R. Qiao, R. Sekar
	- http://www3.cs.stonybrook.edu/~nhasabni/papers/cgo15.pdf
	- http://www3.cs.stonybrook.edu/~nhasabni/papers/cgo15_talk.pdf
- Coverage Prediction for Accelerating Compiler Testing
	- IEEE Transactions on Software Engineering (2019)
	- Junjie Chen, Guancheng Wang, Dan Hao, Yingfei Xiong, Hongyu Zhang, Lu Zhang, Bing Xie
	- https://ieeexplore.ieee.org/abstract/document/8588375
- DATm: Diderot's Automated Testing Model.
	- 39th International Conference on Software Engineering ICSE (12th International Workshop on Automation of Software Test AST) 2017
	- C. Chiw, G. Kindlmann, J. Reppy
	- https://www.researchgate.net/publication/317836930_DATm_Diderot%27s_Automated_Testing_Model
	- https://www.dropbox.com/s/5twsrp12vg4or7t/datm_talk.key?dl=0
- Deep Differential Testing of JVM Implementations
	- ICSE 2019
	- Yuting Chen, Ting Su, Zhendong Su
	- https://tingsu.github.io/files/icse19-classming.pdf
- Differential Testing for Software
	- Digital Technical Journal 10, 1 (1998)
	- William M. McKeeman
	- http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.83.445
- Effect-Driven QuickChecking of Compilers
	- ICFP 2017
	- Jan Midtgaard, Mathias Nygaard Justesen, Patrick Kasting, Flemming Nielson, Hanne Riis Nielson
	- paper: http://janmidtgaard.dk/papers/Midtgaard-al%3AICFP17-full.pdf
	- implementation: https://github.com/jmid/efftester
	- talk
		- http://podcasts.ox.ac.uk/effect-driven-quickchecking-compilers
		- https://www.youtube.com/watch?v=_KrZzaShDew&list=PLnqUlCo055hW7kU-SBQEhC_87etA5Gqlq&index=15
- Extending Equivalence Transformation Based Program Generator for Random Testing of C Compilers
	- A-TEST 2018
	- Shogo Takakura, Mitsuyoshi Iwatsuji, Nagisa Ishiura
	- https://dl.acm.org/citation.cfm?doid=3278186.3278188
	- https://ist.ksc.kwansei.ac.jp/~ishiura/publications/C2018-11a.pdf
- Finding and Analyzing Compiler Warning Defects
	- ICSE 2016
	- Chengnian Sun, Vu Le, Zhendong Su
	- http://ieeexplore.ieee.org/document/7886904/
	- https://web.cs.ucdavis.edu/~su/publications/icse16-warning.pdf
- Finding and Understanding Bugs in C Compilers
	- PLDI 2011
	- Xuejun Yang, Yang Chen, Eric Eide, John Regehr
	- http://www.cs.utah.edu/~regehr/papers/pldi11-preprint.pdf
	- https://www.flux.utah.edu/download?uid=114
	- https://blog.regehr.org/archives/492
	- http://lambda-the-ultimate.org/node/4241
- History-Guided Configuration Diversification for Compiler Test-Program Generation
	- Automated Software Engineering (ASE) 2019
	- Junjie Chen, Guancheng Wang, Dan Hao, Yingfei Xiong, Hongyu Zhang, Lu Zhang
	- https://xiongyingfei.github.io/publications.html#ASE19b
- K-CONFIG: Using Failing Test Cases to Generate Test Cases in GCC Compilers
	- Automated Software Engineering (ASE 2019) Late Breaking Research-Track
	- Md Rafiqul Islam Rabin, Mohammad Amin Alipour
	- https://arxiv.org/abs/1908.10481
- Learning to Accelerate Compiler Testing
	- International Conference on Software Engineering (ICSE), Doctoral Symposium, 2018
	- [Junjie Chen](https://sites.google.com/site/junjiechen08/)
	- https://www.icse2018.org/event/icse-2018-doctoral-symposium-learning-to-accelerate-compiler-testing
	- Slides (2017): http://materials.dagstuhl.de/files/17/17502/17502.JunjieChen.Slides.pdf
- Learning to Prioritize Test Programs for Compiler Testing
	- International Conference on Software Engineering (ICSE 2017)
	- Junjie Chen, Yanwei Bai, Dan Hao, Yingfei Xiong, Hongyu Zhang, Bing Xie
	- http://sei.pku.edu.cn/~xiongyf04/papers/ICSE17b.pdf
- Nautilus: Fishing for Deep Bugs with Grammars
	- Network and Distributed System Security Symposium (NDSS) 2019
	- Cornelius Aschermann, Tommaso Frassetto, Thorsten Holz, Patrick Jauernig, Ahmad-Reza Sadeghi, Daniel Teuchert
	- https://www.syssec.ruhr-uni-bochum.de/research/publications/nautilus/
	- https://github.com/RUB-SysSec/nautilus
	- testing applications: ChakraCore (the JavaScript engine of Microsoft Edge), PHP, mruby, and Lua
- Practical Testing of a C99 Compiler Using Output Comparison
	- Software: Practice and Experience 37(14) 2007
	- Flash Sheridan
	- http://doi.wiley.com/10.1002/spe.812
	- Pre-print: http://flash-sheridan.name/Practical_Testing_of_C99.pdf
	- Bibliography, updated sporadically: http://flash-sheridan.name/compiler_testing_bibliography.html
- RandIR: Differential Testing for Embedded Compilers
	- SCALA 2016
	- Georg Ofenbeck, Tiark Rompf, Markus Püschel
	- https://www.cs.purdue.edu/homes/rompf/papers/ofenbeck-scala16.pdf
- System Under Test: LLVM - https://systemundertest.org/llvm/
- Testing LLVM - http://blog.regehr.org/archives/1450
- The problem with differential testing is that at least one of the compilers must get it right
	- http://blog.frama-c.com/index.php?post/2013/09/25/The-problem-with-differential-testing-is-that-at-least-one-of-the-compilers-must-get-it-right

### Testing: Readings: 2024

- Boosting Compiler Testing by Injecting Real-World Code
	- PLDI 2024
	- Shaohua Li, Theodoros Theodoridis, Zhendong Su
	- https://dl.acm.org/doi/10.1145/3656386
	- https://shao-hua-li.github.io/assets/pdf/2024_pldi_creal_final.pdf
	- https://pldi24.sigplan.org/details/pldi-2024-papers/10/Boosting-Compiler-Testing-by-Injecting-Real-World-Code
	- Creal: an automated program generator for C. Given a valid C program as the seed, Creal can inject new functions into it and produce new valid programs. By default, Creal uses Csmith to produce seed programs.
		- https://github.com/UniCodeSphere/Creal
- Characterizing and Detecting WebAssembly Runtime Bugs
	- ACM Transactions on Software Engineering and Methodology 33(2) 2024
	- Yixuan Zhang, Shangtong Cao, Haoyu Wang, Zhenpeng Chen, Xiapu Luo, Dongliang Mu, Yun Ma, Gang Huang, Xuanzhe Liu
	- https://arxiv.org/abs/2301.12102
	- https://dl.acm.org/doi/10.1145/3624743
	- https://discovery.ucl.ac.uk/id/eprint/10176723
	- https://github.com/bnmcxlzd/TOSEM2023_Complementary_materials
- Java JIT Testing with Template Extraction
	- ACM International Conference on the Foundations of Software Engineering (FSE) 2024
	- Zhiqiang Zang, Fu-Yao Yu, Aditya Thimmaiah, August Shi, Milos Gligoric
	- https://doi.org/10.1145/3643777
	- https://2024.esec-fse.org/details/fse-2024-research-papers/110/Java-JIT-Testing-with-Template-Extraction
	- https://github.com/EngineeringSoftware/lejit
- Testing the MSVC Compiler Backend
	- 2024
	- Troy Johnson
	- https://devblogs.microsoft.com/cppblog/testing-the-msvc-compiler-backend/

### Testing: Readings: 2023

- Feature-Sensitive Coverage for Conformance Testing of Programming Language Implementations
	- PLDI 2023
	- Jihyeok Park, Dongjun Youn, Kanguk Lee, Sukyoung Ryu
	- https://github.com/jestfs/jestfs
	- https://doi.org/10.1145/3591240
	- https://pldi23.sigplan.org/details/pldi-2023-pldi/21/Feature-Sensitive-Coverage-for-Conformance-Testing-of-Programming-Language-Implementa
- Metamorphic Shader Fusion for Testing Graphics Shader Compilers
	- International Conference on Software Engineering (ICSE) 2023
	- Dongwei Xiao, Zhibo Liu, Shuai Wang
	- https://doi.org/10.1109/ICSE48619.2023.00201
	- https://conf.researchr.org/details/icse-2023/icse-2023-technical-track/123/Metamorphic-Shader-Fusion-for-Testing-Graphics-Shader-Compilers
- Program Reconditioning: Avoiding Undefined Behaviour When Finding and Reducing Compiler Bugs
	- PLDI 2023
	- Bastien Lecoeur, Hasan Mohsin, Alastair F. Donaldson
	- https://www.doc.ic.ac.uk/~afd/homepages/papers/pdfs/2023/PLDI.pdf
	- "The problem we address is: How can we apply differential testing and test-case reduction to languages that feature UB [Undefined Behaviour] (or whose current implementations feature UB) in the absence of UB-detection tools, to yield minimised UB-free programs that trigger miscompilations?"
- Revisiting the Evaluation of Deep Learning-Based Compiler Testing
	- International Joint Conference on Artificial Intelligence (IJCAI) 2023
	- Yongqiang Tian, Zhenyang Xu, Yiwen Dong, Chengnian Sun, Shing-Chi Cheung
	- https://doi.org/10.24963/ijcai.2023/542
	- https://www.ijcai.org/proceedings/2023/0542.pdf
- RustSmith: Random Differential Compiler Testing for Rust
	- ACM SIGSOFT International Symposium on Software Testing and Analysis (ISSTA) 2023
	- Mayank Sharma, Pingshi Yu, and Alastair F. Donaldson
	- https://doi.org/10.1145/3597926.3604919
	- https://www.doc.ic.ac.uk/~afd/homepages/papers/pdfs/2023/ISSTA-tool.pdf
	- https://github.com/rustsmith/rustsmith
- Rust-twins: Automatic Rust Compiler Testing through Program Mutation and Dual Macros Generation
	- IEEE/ACM International Conference on Automated Software Engineering (ASE) 2024
	- Wenzhang Yang, Cuifeng Gao, Xiaoyuan Liu, Yuekang Li, Yinxing Xue
	- https://dl.acm.org/doi/10.1145/3691620.3695059
	- https://wzyang.cn/files/Rust_twins.pdf
- Testing a Formally Verified Compiler
	- Tests and Proofs (TAP) 2023
	- David Monniaux, Léo Gourdin, Sylvain Boulmé, Olivier Lebeltel
	- https://hal.science/hal-04096390
- Testing the Compiler for a New-Born Programming Language: An Industrial Case Study (Experience Paper)
	- ACM SIGSOFT International Symposium on Software Testing and Analysis (ISSTA) 2023
	- Yingquan Zhao, Junjie Chen, Ruifeng Fu, Haojie Ye, Zan Wang
	- https://doi.org/10.1145/3597926.3598077
	- https://2023.issta.org/details/issta-2023-technical-papers/37/Testing-the-Compiler-for-a-New-Born-Programming-Language-An-Industrial-Case-Study-E
- Validating JIT Compilers via Compilation Space Exploration
	- ACM SIGOPS Symposium on Operating Systems Principles (SOSP) 2023
	- Cong Li, Yanyan Jiang, Chang Xu, Zhendong Su
	- https://doi.org/10.1145/3600006.3613140
	- https://connglli.github.io/pdfs/artemis_sosp23.pdf
	- Artemis: A JIT Compiler Fuzzer for JVMs via "Compilation Space Exploration" (CSE)/"JIT-Op Neutral Mutation" (JoNM) in "Validating JIT Compilers via Compilation Space Exploration"
		- https://github.com/test-jitcomp/Artemis
	- "This paper introduces the novel concept of compilation space, which facilitates the thorough validation of just-in-time (JIT) compilers in modern language virtual machines (LVMs). The compilation space, even for a single program, consists of an extensive array of JIT compilation choices, which can be cross-validated for the correctness of JIT compilation. To thoroughly explore the compilation space in a lightweight and LVM-agnostic manner, we strategically mutate test programs with JIT-relevant, yet semantics-preserving code structures to trigger diverse JIT compilation choices. We realize our technique in Artemis, a tool for the Java virtual machine (JVM). Our evaluation has led to 85 bug reports for three widely used production JVMs, namely HotSpot, OpenJ9, and the Android Runtime. Among them, 53 have already been confirmed or fixed with many being critical. It is also worth mentioning that all the reported bugs concern JIT compilers, demonstrating the clear effectiveness and strong practicability of our technique. We expect that the generality and practicability of our approach will make it broadly applicable for understanding and validating JIT compilers."
- Vectorizing Program Ingredients for Better JVM Testing
	- International Symposium on Software Testing and Analysis (ISSTA) 2023
	- Tianchang Gao, Junjie Chen, Yingquan Zhao, Yuqun Zhang, Lingming Zhang
	- https://doi.org/10.1145/3597926.3598075
	- https://lingming.cs.illinois.edu/publications/issta2023b.pdf
	- https://2023.issta.org/details/issta-2023-technical-papers/35/Vectorizing-Program-Ingredients-for-Better-JVM-Testing
	- VECT: Vectorized JVM Testing
		- https://github.com/gaotravor/VECT
- WRTester: Differential Testing of WebAssembly Runtimes via Semantic-aware Binary Generation
	- 2023
	- Shangtong Cao, Ningyu He, Xinyu She, Yixuan Zhang, Mu Zhang, Haoyu Wang
	- https://arxiv.org/abs/2312.10456

### Testing: Readings: 2022

- Compiler Testing using Template Java Programs
	- IEEE/ACM International Conference on Automated Software Engineering (ASE) 2022
	- Zhiqiang Zang, Nathan Wiatrek, Milos Gligoric, August Shi
	- https://arxiv.org/abs/2209.04514
	- https://doi.org/10.1145/3551349.3556958
	- https://github.com/EngineeringSoftware/jattack
- Detecting C++ Compiler Front-end Bugs via Grammar Mutation and Differential Testing
	- IEEE Transactions on Reliability 2022
	- Haoxin Tu, He Jiang, Zhide Zhou, Yixuan Tang, Zhilei Ren, Lei Qiao, Lingxiao Jiang
	- https://haoxintu.github.io/files/tr-2022-draft.pdf
	- https://github.com/haoxintu/CCOFT
- Differential Testing of Simulation-Based VM Generators: Automatic Detection of VM Generator Semantic Gaps between Simulation and Generated VMs
	- Pierre Misse-Chanabier, Guillermo Polito, Stéphane Ducasse, Noury Bouraqadi, Luc Fabresse, Pablo Tesone
	- ACM Symposium On Applied Computing (SAC) 2022
		- https://doi.org/10.1145/3477314.3507171
	- International Conference on Software and Systems Reuse (ICSR) 2022
		- https://doi.org/10.1007/978-3-031-08129-3_7
- Interpreter-guided Differential JIT Compiler Unit Testing
	- Programming Language Design and Implementation (PLDI) 2022
	- Guillermo Polito, Stéphane Ducasse, Pablo Tesone
	- https://doi.org/10.1145/3519939.3523457
	- https://www.youtube.com/watch?v=V3LUdA52rnc
- Metamorphic Testing of Deep Learning Compilers
	- SIGMETRICS 2022
	- Proceedings of the ACM on Measurement and Analysis of Computing Systems, Volume 6, Issue 1, March 2022
	- Dongwei Xiao, Zhibo Liu, Yuanyuan Yuan, Qi Pang, Shuai Wang
	- https://dl.acm.org/doi/abs/10.1145/3508035
	- https://www.youtube.com/watch?v=C4yCBihNQUA
	- https://github.com/Wilbur-Django/Testing-DNN-Compilers

### Testing: Readings: 2021

- JEST: N+1-version Differential Testing of Both JavaScript Engines and Specification
	- International Conference on Software Engineering (ICSE) 2021
	- Jihyeok Park, Seungmin An, Dongjun Youn, Gyeongwon Kim, Sukyoung Ryu
	- https://arxiv.org/abs/2102.07498
- SpecTest: Specification-Based Compiler Testing
	- Fundamental Approaches to Software Engineering (FASE) 2021
	- Richard Schumi, Jun Sun
	- https://www.springerprofessional.de/en/spectest-specification-based-compiler-testing/18985506
- Toolchain testing
	- 2021; MaskRay (Fangrui Song)
	- https://maskray.me/blog/2021-08-08-toolchain-testing

### Testing: Readings: 2020

- Closer to the Edge: Testing Compilers More Thoroughly by Being Less Conservative About Undefined Behaviour
	- Automated Software Engineering (ASE) 2020
	- Karine Even-Mendoza, Cristian Cadar, Alastair F. Donaldson
	- https://srg.doc.ic.ac.uk/projects/csmithedge/
	- https://srg.doc.ic.ac.uk/files/papers/csmithedge-ase-nier-20.pdf
	- https://www.youtube.com/watch?v=JGpAO_Gu4zU
	- https://conf.researchr.org/details/ase-2020/ase-2020-nier-track/8/Closer-to-the-Edge-Testing-Compilers-More-Thoroughly-by-Being-Less-Conservative-Abou
- Compiler Testing: A Systematic Literature Analysis
	- Frontiers of Computer Science 14 (2020)
	- Yixuan Tang, Zhilei Ren, Weiqiang Kong, He Jiang
	- https://arxiv.org/abs/1810.02718
	- https://link.springer.com/article/10.1007/s11704-019-8231-0
- Random Testing for C and C++ Compilers with YARPGen
	- OOPSLA 2020
	- Vsevolod Livinskii, Dmitry Babokin, John Regehr
	- https://doi.org/10.1145/3428264
	- http://www.cs.utah.edu/~regehr/yarpgen-oopsla20.pdf
	- https://www.youtube.com/watch?v=mb9aRoXnicE
- Testing Static Analyses for Precision and Soundness
	- Code Generation and Optimization (CGO) 2020
	- Jubi Taneja, Zhengyang Liu, John Regehr
	- http://www.cs.utah.edu/~regehr/cgo20.pdf
	- https://github.com/jubitaneja/souper-cgo20-artifact
	- Testing Dataflow Analyses for Precision and Soundness
		- https://blog.regehr.org/archives/1709
		- LLVM Dataflow Info Printer Pass
			- https://github.com/regehr/llvm-dataflow-info

### Testing: Readings: 2017

- Testing... Testing... GCC
	- 2017; David Malcolm
	- https://developers.redhat.com/blog/2017/02/13/testing-testing-gcc

### Testing: Readings: Fuzzing

See also: [Testing](https://github.com/MattPD/cpplinks/blob/master/testing.md): [Fuzzing](https://github.com/MattPD/cpplinks/blob/master/testing.fuzzing.md)

- Fuzzing with Grammars
	- In "The Fuzzing Book" - https://www.fuzzingbook.org/
	- Andreas Zeller, Rahul Gopinath, Marcel Böhme, Gordon Fraser, Christian Holler
	- https://www.fuzzingbook.org/html/Grammars.html

#### Testing: Readings: Fuzzing: 2023

- A Generative and Mutational Approach for Synthesizing Bug-exposing Test Cases to Guide Compiler Fuzzing
	- ACM Joint European Software Engineering Conference and Symposium on the Foundations of Software Engineering (ESEC/FSE) 2023
	- Guixin Ye, Tianmin Hu, Zhanyong Tang, Zhenye Fan, Shin Hwei Tan, Bo Zhang, Wenxiang Qian, Zheng Wang
	- https://dl.acm.org/doi/10.1145/3611643.3616332
	- https://eprints.whiterose.ac.uk/202769/
	- https://zwang4.github.io/publications/fse23.pdf
	- COMFUZZ: a compiler fuzzing framework that combines generative and mutation techniques
		- https://github.com/NWU-NISL-Fuzzing/COMFUZZ
- A Survey of Modern Compiler Fuzzing
	- 2023
	- Haoyang Ma
	- https://arxiv.org/abs/2306.06884
- Finding Deep-Learning Compilation Bugs with NNSmith
	- ASPLOS 2023
	- Jiawei Liu, Jinkun Lin, Fabian Ruffy, Cheng Tan, Jinyang Li, Aurojit Panda, Lingming Zhang
	- https://arxiv.org/abs/2207.13066
	- NNSmith: Automatic DNN generation for fuzzing and more
		- https://nnsmith-asplos.readthedocs.io/en/latest/
		- https://github.com/ise-uiuc/nnsmith
- FUZZILLI: Fuzzing for JavaScript JIT Compiler Vulnerabilities
	- Network and Distributed Systems Security (NDSS) Symposium 2023
	- Samuel Groß, Simon Koch, Lukas Bernhard, Thorsten Holz, Martin Johns
	- https://www.ndss-symposium.org/ndss-paper/fuzzilli-fuzzing-for-javascript-jit-compiler-vulnerabilities/
	- https://github.com/evaluating-fuzzilli-for-js-jit-fuzzing
	- https://github.com/googleprojectzero/fuzzilli
- Fuzzing Deep Learning Compilers with HirGen
	- International Symposium on Software Testing and Analysis (ISSTA) 2023
	- Haoyang Ma, Qingchao Shen, Yongqiang Tian, Junjie Chen, Shing-Chi Cheung
	- https://doi.org/10.1145/3597926.3598053
	- https://2023.issta.org/details/issta-2023-technical-papers/13/Fuzzing-Deep-Learning-Compilers-with-HirGen
	- https://github.com/haoyang9804/HirGen
- FuzzJIT: Towards Fuzzing JavaScript Engine JIT Compiler
	- USENIX Security Symposium 2023
	- Junjie Wang, Zhiyi Zhang, Shuang Liu, Xiaoning Du, Junjie Chen
	- https://www.usenix.org/conference/usenixsecurity23/presentation/wangjunjie
	- https://github.com/SpaceNaN/fuzzjit
- GrayC: Greybox Fuzzing of Compilers and Analysers for C
	- ACM SIGSOFT International Symposium on Software Testing and Analysis (ISSTA) 2023
	- Karine Even Mendoza, Arindam Sharma, Alastair F. Donaldson, Cristian Cadar
	- https://kclpure.kcl.ac.uk/portal/en/publications/grayc-greybox-fuzzing-of-compilers-and-analysers-for-c(614e1ae8-b5b8-44ae-939a-75e3009eea91).html
	- https://srg.doc.ic.ac.uk/projects/grayc/
	- https://github.com/srg-imperial/directed-compiler-fuzzing-code
- Industrial Deployment of Compiler Fuzzing Techniques for Two GPU Shading Languages
	- ICST 2023
	- Alastair F. Donaldson, Ben Clayton, Ryan Harrison, Hasan Mohsin, David Neto, Vasyl Teliman, Hana Watson
	- https://www.doc.ic.ac.uk/~afd/homepages/papers/pdfs/2023/ICST.pdf
	- https://conf.researchr.org/details/icst-2023/icst-2023-industry/47/Industrial-Deployment-of-Compiler-Fuzzing-Techniques-for-Two-GPU-Shading-
- JITfuzz: Coverage-guided Fuzzing for JVM Just-in-Time Compilers
	- International Conference on Software Engineering (ICSE) 2023
	- Mingyuan Wu, Minghai Lu, Heming Cui, Junjie Chen, Yuqun Zhang, Lingming Zhang
	- https://lingming.cs.illinois.edu/publications/icse2023e.pdf
	- https://conf.researchr.org/details/icse-2023/icse-2023-technical-track/150/JITfuzz-Coverage-guided-Fuzzing-for-JVM-Just-in-Time-Compilers
- MLIRSmith: Random Program Generation for Fuzzing MLIR Compiler Infrastructure
	- IEEE/ACM International Conference on Automated Software Engineering (ASE) 2023
	- Haoyu Wang, Junjie Chen, Chuyue Xie, Shuang Liu, Zan Wang, Qingchao Shen, Yingquan Zhao
	- https://ieeexplore.ieee.org/document/10298562
	- https://tjusail.github.io/people/papers/MLIRSmith_CameraReady.pdf
	- https://conf.researchr.org/details/ase-2023/ase-2023-papers/49/MLIRSmith-Random-Program-Generation-for-Fuzzing-MLIR-Compiler-Infrastructure
	- https://github.com/Colloportus0/MLIRSmith
- SJFuzz: Seed and Mutator Scheduling for JVM Fuzzing
	- ACM Joint European Software Engineering Conference and Symposium on the Foundations of Software Engineering (ESEC/FSE) 2023
	- Mingyuan Wu, Yicheng Ouyang, Minghai Lu, Junjie Chen, Yingquan Zhao, Heming Cui, Guowei Yang, Yuqun Zhang
	- https://doi.org/10.1145/3611643.3616277
	- https://shadowmydx.github.io/papers/fse2023b.pdf
	- SJFuzz: Scheduling for JVM Fuzzing
		- Discrepancy-driven JVM Fuzzing
		- https://github.com/fuzzy000/SJFuzz
- TorchProbe: Fuzzing Dynamic Deep Learning Compilers
	- APLAS 2023: Asian Symposium on Programming Languages and Systems
	- Qidong Su, Chuqin Geng, Gennady Pekhimenko, Xujie Si
	- https://arxiv.org/abs/2310.20078
	- https://link.springer.com/chapter/10.1007/978-981-99-8311-7_15

#### Testing: Readings: Fuzzing: 2022

- Coverage-Guided Tensor Compiler Fuzzing with Joint IR-Pass Mutation
	- OOPSLA 2022
	- Jiawei Liu, Yuxiang Wei, Sen Yang, Yinlin Deng, Lingming Zhang
	- https://arxiv.org/abs/2202.09947
	- https://dl.acm.org/doi/10.1145/3527317
	- Tzer: TVM Implementation
		- https://github.com/ise-uiuc/tzer
- High-coverage metamorphic testing of concurrency support in C compilers
	- Software Testing Verification & Reliability 2022
	- Matt Windsor, Alastair F. Donaldson, John Wickerson
	- https://onlinelibrary.wiley.com/doi/10.1002/stvr.1812
- High-Throughput, Formal-Methods-Assisted Fuzzing for LLVM
	- 2022; Yuyou Fan, John Regehr
	- https://blog.regehr.org/archives/2148
	- https://github.com/Hatsunespica/alive2
- Jit-Picking: Differential Fuzzing of JavaScript Engines
	- Computer and Communications Security (CCS) 2022
	- Lukas Bernhard, Tobias Scharnowski, Moritz Schloegel, Tim Blazytko, Thorsten Holz
	- https://doi.org/10.1145/3548606.3560624
	- https://publications.cispa.saarland/3773/1/2022-CCS-JIT-Fuzzing.pdf
	- https://github.com/RUB-SysSec/JIT-Picker
- Making No-Fuss Compiler Fuzzing Effective
	- Compiler Construction (CC) 2022
	- Alex Groce, Rijnard van Tonder, Goutamkumar Tulajappa Kalburgi, Claire Le Goues
	- https://dl.acm.org/doi/10.1145/3497776.3517765
	- https://agroce.github.io/cc22.pdf
	- Deconstructing programs for compiler fuzzing
		- https://comby.dev/blog/2022/04/11/comby-decomposer-compiler-fuzzing
- On the Naturalness of Fuzzer-Generated Code
	- Mining Software Repositories (MSR) 2022
	- Rajeswari Hita Kambhamettu, John R Billos, Tomi Oluwaseun-Apo, Benjamin Gafford, Rohan Padhye, Vincent J Hellendoorn
	- https://rohan.padhye.org/files/natfuzz-msr22.pdf

#### Testing: Readings: Fuzzing: 2021

- A Comprehensive Study of Deep Learning Compiler Bugs
	- ESEC/FSE 2021
	- Qingchao Shen, Haoyang Ma, Junjie Chen, Yongqiang Tian, Shing-Chi Cheung, Xiang Chen
	- https://doi.org/10.1145/3468264.3468591
		- Free Access (OpenTOC): https://www.sigsoft.org/resources/opentoc/ESEC-FSE-21toc.html
	- https://2021.esec-fse.org/details/fse-2021-papers/60/A-Comprehensive-Study-of-Deep-Learning-Compiler-Bugs
	- TVMfuzz: a demo project for fuzzing TVM
		- https://github.com/ShenQingchao/DLCstudy
		- https://github.com/anonymousWork000/DLCstudy
- An Empirical Study of the Reliability of High-Level Synthesis Tools
	- FCCM 2021
	- Yann Herklotz, Zewei Du, Nadesh Ramanathan, John Wickerson
	- https://johnwickerson.github.io/papers/fuzzingHLS.pdf
	- https://johnwickerson.wordpress.com/2021/05/07/fuzzing-hls/
- Automated Conformance Testing for JavaScript Engines via Deep Compiler Fuzzing
	- PLDI 2021
	- Guixin Ye, Zhanyong Tang, Shin Hwei Tan, Dingyi Fang, Xiaoyang Sun, Lizhong Bian, Songfang Huang, Haibo Wang, Zheng Wang
	- https://doi.org/10.1145/3453483.3454054
	- https://pldi21.sigplan.org/details/pldi-2021-papers/29/Automated-Conformance-Testing-for-JavaScript-Engines-via-Deep-Compiler-Fuzzing
- C4: The C Compiler Concurrency Checker
	- ACM SIGSOFT International Symposium on Software Testing and Analysis (ISSTA) 2021 (tool demonstrations track)
	- Matt Windsor, Alastair F. Donaldson, John Wickerson
	- https://johnwickerson.github.io/papers/c4_issta2021.pdf
	- C4: a project to check C compiler concurrency.
		- The goal is to be able to find bugs in the way real-world compilers implement the C11 memory model.
		- https://c4-project.github.io
		- https://github.com/c4-project
		- Introducing C4: the C Compiler Concurrency Checker: https://johnwickerson.wordpress.com/2021/06/09/c4/
		- C4 contains several free and open-source (FOSS) subprojects:
			- c4f: a fuzzer for litmus tests github; MIT with some CECILL-B code
			- c4t: an automatic runner for compiler test campaigns github; MIT
			- c4-corpora: a set of litmus tests pre-generated with memalloy, for use as c4f input github; public domain
			- c4-scripts: a set of Bash scripts for automating some c4f and c4t workflows github; MIT
			- mutated-llvm: a copy of LLVM instrumented with run-time selectable, concurrency-related, mutations github; Apache 2.0 with LLVM extensions
			- These projects are designed to be used together with a litmus test runner (such as litmus7) to run automatic tests against compilers on one or more machines.
- Cranelift, Part 3: Correctness in Register Allocation
	- Or: How I Learned to Stop Worrying and Fuzz with a Symbolic Checker
	- 2021; Chris Fallin
	- https://cfallin.org/blog/2021/03/15/cranelift-isel-3/
	- https://github.com/bytecodealliance/regalloc.rs
- One Engine to Fuzz ’em All: Generic Language Processor Testing with Semantic Validation
	- IEEE S&P 2021
	- Yongheng Chen, Rui Zhong, Hong Hu, Hangfan Zhang, Yupeng Yang, Dinghao Wu, Wenke Lee
	- https://faculty.ist.psu.edu/wu/papers/polyglot.pdf
	- PolyGlot, a fuzzing framework for language processors
		- https://github.com/s3team/Polyglot

#### Testing: Readings: Fuzzing: 2020

- CUDAsmith: A Fuzzer for CUDA Compilers
	- Computers, Software and Applications Conference (COMPSAC) 2020
	- Bo Jiang, Xiaoyan Wang, W. K. Chan, T. H. Tse, Na Li, Yongfeng Yin, Zhenyu Zhang
	- https://www.cs.hku.hk/data/techreps/document/TR-2020-05.pdf
	- https://github.com/gongbell/CUDAsmith
- Fuzzing JavaScript Engines with Aspect-preserving Mutation
	- IEEE Symposium on Security and Privacy (S&P) 2020
	- Soyeon Park, Wen Xu, Insu Yun, Daehee Jang, Taesoo Kim
	- https://gts3.org/assets/papers/2020/park:die.pdf
	- https://github.com/sslab-gatech/DIE
- Putting Randomized Compiler Testing into Production
	- ECOOP 2020
	- Alastair Donaldson, Hugues Evrard, Paul Thomson
	- https://www.doc.ic.ac.uk/~afd/homepages/papers/pdfs/2020/ECOOP_GraphicsFuzz.pdf
	- https://2020.ecoop.org/details/ecoop-2020-papers/22/Putting-Randomized-Compiler-Testing-into-Production
	- http://multicore.doc.ic.ac.uk/tools/GraphicsFuzz/ECOOP2020Artifact/
	- https://www.youtube.com/watch?v=qhqTyGccwS0

#### Testing: Readings: Fuzzing: 2019

- Compiler Fuzzing: How Much Does It Matter?
	- OOPSLA 2019
	- Michael Marcozzi, Qiyi Tang, Alastair Donaldson, Cristian Cadar
	- https://srg.doc.ic.ac.uk/projects/compiler-bugs/
	- https://sites.google.com/view/michaelmarcozzi/software/compiler-bugs-impact
	- A Systematic Impact Study for Fuzzer-Found Compiler Bugs
		- 2019 arXiv (pre-print)
		- https://arxiv.org/abs/1902.09334
		- https://sites.google.com/view/michaelmarcozzi/compiler-bugs
	- PapersWeLove London 2020
		- Michael Marcozzi
		- https://www.youtube.com/watch?v=CUBmXYahTb0
- DeepFuzz: Automatic Generation of Syntax Valid C Programs for Fuzz Testing
	- AAAI Conference on Artificial Intelligence (AAAI) 2019
	- Xiao Liu, Xiaoting Li, Rupesh Prajapati, Dinghao Wu
	- https://faculty.ist.psu.edu/wu/papers/DeepFuzz.pdf
	- https://github.com/s3team/DeepFuzz
- Neural Program Synthesis for Compiler Fuzzing
	- 2019 PhD Dissertation; Xiao Liu
	- https://faculty.ist.psu.edu/wu/papers/xiao-liu-dissertation.pdf

#### Testing: Readings: Fuzzing: 2018

- Causal Distance-Metric-Based Assistance for Debugging After Compiler Fuzzing
	- IEEE International Symposium on Software Reliability Engineering (ISSRE) 2018
	- Josie Holmes and Alex Groce
	- https://agroce.github.io/issre18.pdf
- Compiler fuzzing, part 1
	- 2018; Vegard Nossum
	- http://www.vegardno.net/2018/06/compiler-fuzzing.html
- Compiler Fuzzing through Deep Learning
	- International Symposium on Software Testing and Analysis (ISSTA) 2018
	- Chris Cummins, Pavlos Petoumenos, Hugh Leather and Alastair Murray
	- http://homepages.inf.ed.ac.uk/hleather/publications/2018_deepfuzzing_issta.pdf
	- https://chriscummins.cc/deepsmith
- Fuzzing the .NET JIT Compiler
	- 2018; Matt Warren
	- http://mattwarren.org/2018/08/28/Fuzzing-the-.NET-JIT-Compiler/
	- Fuzzlyn: Fuzzer for the .NET toolchains
		- https://github.com/jakobbotsch/Fuzzlyn

#### Testing: Readings: Fuzzing: 2017

- Automated Testing of Graphics Shader Compilers
	- SPLASH 2017 OOPSLA
	- Alastair F. Donaldson, Hugues Evrard, Andrei Lascu, Paul Thomson
	- https://dl.acm.org/citation.cfm?id=3152284.3133917
	- https://www.doc.ic.ac.uk/~afd/homepages/papers/pdfs/2017/OOPSLA.pdf
	- Overview of the GLFuzz transformations - https://medium.com/@afd_icl/overview-of-the-glfuzz-transformations-d530540a5a18

#### Testing: Readings: Fuzzing: 2014

- Improving the Utility of Compiler Fuzzers
	- 2014 Ph.D. Dissertation; Yang Chen
	- https://collections.lib.utah.edu/details?id=196364

#### Testing: Readings: Fuzzing: 2013

- Taming compiler fuzzers
	- PLDI 2013
	- Y. Chen, A. Groce, C. Zhang, W.-K. Wong, X. Fern, E. Eide, J. Regehr
	- https://www.cs.utah.edu/~regehr/papers/pldi13.pdf
	- Fuzzers Need Taming - https://blog.regehr.org/archives/925

### Testing: Readings: Generation

- Compiler Test-Program Generation via Memoized Configuration Search
	- International Conference on Software Engineering (ICSE) 2023
	- Junjie Chen, Chenyao Suo, Jiajun Jiang, Peiqi Chen, Xingjian Li
	- https://doi.org/10.1109/ICSE48619.2023.00172
	- https://xgdsmileboy.github.io/files/paper/compiler-icse23.pdf
	- MCS: Memoized Configuration Search
		- https://github.com/tju-chenyaosuo/MCS
- CsmithEdge: More Effective Compiler Testing by Handling Undefined Behaviour Less Conservatively
	- Empirical Software Engineering (EMSE) 2022
	- Karine Even-Mendoza, Cristian Cadar, Alastair F. Donaldson
	- https://multicore.doc.ic.ac.uk/publications/emse-22.html
	- https://github.com/karineek/CsmithEdge
- Generating Conforming Programs With Xsmith
	- ACM SIGPLAN International Conference on Generative Programming: Concepts and Experiences (GPCE) 2023
	- William Gallard Hatch, Pierce Darragh, Sorawee Porncharoenwase, Guy Watson, Eric Eide
	- https://doi.org/10.1145/3624007.3624056
	- https://willghatch.net/publications/xsmith-gpce-2023-preprint.pdf
	- https://2023.splashcon.org/details/gpce-2023-papers/7/Generating-Conforming-Programs-With-Xsmith
- Growing A Test Corpus with Bonsai Fuzzing
	- ICSE 2021
	- Vasudev Vikram, Rohan Padhye, Koushik Sen
	- https://rohan.padhye.org/files/bonsai-icse21.pdf
	- Bonsai Fuzzing: a fuzz-testing algorithm that generates concise test cases for software such as compilers.
		- https://github.com/vasumv/bonsai-fuzzing
- Inputs from Hell: Learning Input Distributions for Grammar-Based Test Generation
	- International Conference on Software Engineering ICSE 2021
	- IEEE Transactions on Software Engineering (TSE) Volume 48, Issue 4, 01 2022
	- Ezekiel Soremekun, Esteban Pavese, Nikolas Havrikov, Lars Grunske, Andreas Zeller
	- https://doi.org/10.1109/TSE.2020.3013716
	- https://publications.cispa.saarland/3167/
	- https://conf.researchr.org/details/icse-2021/icse-2021-Journal-First-Papers/18/Inputs-from-Hell-Learning-Input-Distributions-for-Grammar-Based-Test-Generation
- RemGen: Remanufacturing a Random Program Generator for Compiler Testing
	- IEEE International Symposium on Software Reliability Engineering (ISSRE) 2022
	- Haoxin Tu, He Jiang, Xiaochen Li, Zhilei Ren, Zhide Zhou, Lingxiao Jiang
	- https://haoxintu.github.io/files/issre2022-camera-ready.pdf
	- https://github.com/RemGen2022/RemCCG
	- https://github.com/haoxintu/RemCCG
- Stack-Driven Program Generation of WebAssembly
	- Asian Symposium on Programming Languages and Systems (APLAS) 2020
	- Árpád Perényi, Jan Midtgaard
	- https://janmidtgaard.dk/papers/Perenyi-Midtgaard%3aAPLAS20.pdf
	- Property-Based Testing of WebAssembly
		- https://github.com/jmid/wasm-prop-tester
- Testing an Optimising Compiler by Generating Random Lambda Terms
	- 2012 Licentiate thesis
		- Michał H. Pałka
		- https://research.chalmers.se/en/publication/157525
		- https://publications.lib.chalmers.se/records/fulltext/157525.pdf
	- AST 2011: 6th International Workshop on Automation of Software Test
		- Michał H. Pałka, Koen Claessen, Alejandro Russo, John Hughes
		- https://dl.acm.org/doi/10.1145/1982595.1982615
- Writing a Test Case Generator for a Programming Language
	- 2020
	- Nick Fitzgerald
	- https://fitzgeraldnick.com/2020/08/24/writing-a-test-case-generator.html

### Testing: Readings: Performance Optimization

- An empirical study of optimization bugs in GCC and LLVM
	- Journal of Systems and Software, 174:110884, 2021
	- Zhide Zhou, Zhilei Ren, Guojun Gao, and He Jiang
	- https://www.sciencedirect.com/science/article/abs/pii/S0164121220302740?via%3Dihub
	- http://oscar-lab.org/paper/An%20empirical%20study%20of%20optimization%20bugs%20in%20GCC%20and%20LLVM.pdf
- AnghaBench: A Suite with One Million Compilable C Benchmarks for Code-Size Reduction
	- Angha Project
		- http://cuda.dcc.ufmg.br/angha/
		- https://github.com/brenocfg/AnghaBench
	- AnghaBench: a Synthetic Collection of Benchmarks Mined from Open-Source Repositories
		- Synthesis of Benchmarks for the C Programming Language by Mining Software Repositories
		- SBLP 2019
		- Breno Campos Ferreira Guimarães, José Wesley de S. Magalhães, Anderson Faustino da Silva, Fernando M. Q. Pereira
		- https://dl.acm.org/doi/10.1145/3355378.3355380
	- Automatic Synthesis of Compilable C Benchmarks from Open Source Repositories
		- 2020
		- Faustino, Anderson, Bruno Kind, Fernando Magno Quint
		- http://lac.dcc.ufmg.br/pubs/TechReports/LaC_TechReport012020.pdf
	- AnghaBench: A Suite with One Million Compilable C Benchmarks for Code-Size Reduction
		- CGO 2021
		- Anderson Faustino da Silva, Bruno Conde Kind, José Wesley de Souza Magalhães, Jerônimo Nunes Rocha, Breno Campos Ferreira Guimarães, Fernando Magno Quintão Pereira
		- https://doi.org/10.1109/CGO51591.2021.9370322
		- https://homepages.dcc.ufmg.br/~fernando/publications/papers/FaustinoCGO21.pdf
- Compiler Testing via a Theory of Sound Optimisations in the C11/C++11 Memory Model
	- Programming Language Design and Implementation (PLDI) 2013
	- Robin Morisset, Pankaj Pawan, Francesco Zappa Nardelli
	- https://www.di.ens.fr/~zappa/readings/pldi13.pdf
- CTOS: Compiler Testing for Optimization Sequences of LLVM
	- IEEE Transactions on Software Engineering 2021
	- He Jiang, Zhide Zhou, Zhilei Ren, Jingxuan Zhang, Xiaochen Li
	- https://doi.org/10.1109/TSE.2021.3058671
	- https://doi.ieeecomputersociety.org/10.1109/TSE.2021.3058671
- Detecting Arithmetic Optimization Opportunities for C Compilers by Randomly Generated Equivalent Programs
	- IPSJ Transactions on System LSI Design Methodology, vol. 9, 2016; A. Hashimoto and N. Ishiura
	- <https://www.jstage.jst.go.jp/article/ipsjtsldm/9/0/9_21/_article>
- Detecting Missed Arithmetic Optimization in C Compilers by Differential Random Testing
	- The 20th Workshop on Synthesis And System Integration of Mixed Information technologies (SASIMI 2016)
	- Mitsuyoshi Iwatsuji, Atsushi Hashimoto, Nagisa Ishiura
	- http://ist.ksc.kwansei.ac.jp/~ishiura/publications/C2016-10a.pdf
- Evaluating the Effects of Compiler Optimizations on Mutation Testing at the Compiler IR Level
	- ISSRE 2016
	- Farah Hariri, August Shi, Hayes Converse, Sarfraz Khurshid, Darko Marinov
	- http://mir.cs.illinois.edu/farah/presentations/issre16_presentation.pdf
	- http://mir.cs.illinois.edu/marinov/publications/HaririETAL16CompilerIRMutation.pdf
	- https://www.researchgate.net/publication/311529837_Evaluating_the_Effects_of_Compiler_Optimizations_on_Mutation_Testing_at_the_Compiler_IR_Level
- Finding Missed Compiler Optimizations by Differential Testing
	- Compiler Construction (CC) 2018
	- Gergö Barany
	- https://github.com/gergo-/missed-optimizations/raw/master/missed_optimizations_preprint.pdf
	- Missed optimizations in C compilers: https://github.com/gergo-/missed-optimizations/
	- https://hal.inria.fr/hal-01682683
- Finding Missed Optimizations through the Lens of Dead Code Elimination
	- Architectural Support for Programming Languages and Operating Systems (ASPLOS) 2022
	- Theodoros Theodoridis, Manuel Rigger, Zhendong Su
	- https://ethz.ch/content/dam/ethz/special-interest/infk/ast-dam/documents/Theodoridis-ASPLOS22-DCE-Paper.pdf
	- https://github.com/DeadCodeProductions/dead
- Lost in translation: Exposing hidden compiler optimization opportunities
	- 2019 arXiv
	- Kyriakos Georgiou, Zbigniew Chamski, Andres Amaya Garcia, David May, Kerstin Eder
	- https://arxiv.org/abs/1903.11397
	- https://github.com/TrustworthySystemLab/LostInTranslation
- Random Testing of Compilers’ Performance Based on Mixed Static and Dynamic Code Comparison
	- A-TEST 2018
	- Kota Kitaura, Nagisa Ishiura
	- https://ist.ksc.kwansei.ac.jp/~ishiura/publications/C2018-11b.pdf
	- https://dl.acm.org/citation.cfm?id=3278192
- Reinforcing Random Testing of Arithmetic Optimization of C Compilers by Scaling up Size and Number of Expressions
	- IPSJ Transactions on System LSI Design Methodology, vol. 7, 2014
	- E. Nagai, A. Hashimoto, N. Ishiura
	- <https://www.jstage.jst.go.jp/article/ipsjtsldm/7/0/7_91/_article>
- Scaling up Size and Number of Expressions in Random Testing of Arithmetic Optimization of C Compilers
	- SASIMI 2013
	- E. Nagai, A. Hashimoto, N. Ishiura
	- http://ist.ksc.kwansei.ac.jp/~ishiura/publications/C2013-10.pdf
- Synthesizing Benchmarks for Predictive Modeling
	- CGO 2017
	- Chris Cummins, Pavlos Petoumenos, Zheng Wang, Hugh Leather
	- https://github.com/ChrisCummins/paper-synthesizing-benchmarks
	- https://chriscummins.cc/pub/2017-cgo.pdf
	- CLgen: Deep learning program generator
		- https://github.com/ChrisCummins/clgen
- The Correctness-Security Gap in Compiler Optimization
	- LangSec 2015, IEEE SPW
	- Vijay D'Silva, Mathias Payer, Dawn Song
	- paper: https://research.google.com/pubs/pub43856.html
	- slides: https://nebelwelt.net/publications/files/15LangSec-presentation.pdf
	- talk: https://www.youtube.com/watch?v=g6LCtHz_MDc&list=PL0pRF4xvoD0kuECJuowraVIIHlT3pN1Cm&index=3

#### Testing: Readings: Performance Optimization: 2024

- Beyond a Joke: Dead Code Elimination Can Delete Live Code
	- ICSE 2024
	- Haoxin Tu, Lingxiao Jiang, Debin Gao, He Jiang
	- https://conf.researchr.org/details/icse-2024/icse-2024-new-ideas-and-emerging-results/6/Beyond-a-Joke-Dead-Code-Elimination-Can-Delete-Live-Code
	- https://haoxintu.github.io/files/icse2024-nier-camera-ready.pdf
	- https://github.com/AnonyGiit/Xdead
	- https://github.com/haoxintu/Xdead
- Refined Input, Degraded Output: The Counterintuitive World of Compiler Behavior
	- PLDI 2024
	- Theodoros Theodoridis, Zhendong Su
	- https://dl.acm.org/doi/10.1145/3656404

#### Testing: Readings: Performance Optimization: 2023

- Diagnosing Compiler Performance by Comparing Optimization Decisions
	- International Conference on Managed Programming Languages & Runtimes (MPLR) 2023
	- Andrej Pečimúth, David Leopoldseder, Petr Tůma
	- https://2023.splashcon.org/details/mplr-2023-papers/12/Diagnosing-Compiler-Performance-by-Comparing-Optimization-Decisions
	- https://doi.org/10.1145/3617651.3622994
	- https://github.com/oracle/graal/blob/master/compiler/docs/Profdiff.md
- Exploring Missed Optimizations in WebAssembly Optimizers
	- ACM SIGSOFT International Symposium on Software Testing and Analysis (ISSTA) 2023
	- Zhibo Liu, Dongwei Xiao, Zongjie Li, Shuai Wang, Wei Meng
	- https://2023.issta.org/details/issta-2023-technical-papers/28/Exploring-Missed-Optimizations-in-WebAssembly-Optimizers

#### Testing: Readings: Performance Optimization: Loops

- An Empirical Study of the Effect of Source-level Loop Transformations on Compiler Stability
	- OOPSLA 2018
	- Zhangxiaowen Gong, Zhi Chen, Justin Szaday, David Wong, Zehra Sura, Neftali Watkinson, Saeed Maleki, David Padua, Alexander Veidenbaum, Alexandru Nicolau, Josep Torrellas
	- https://2018.splashcon.org/details/splash-2018-OOPSLA/42/An-Empirical-Study-of-the-Effect-of-Source-level-Loop-Transformations-on-Compiler-Sta
	- https://iacoma.cs.uiuc.edu/iacoma-papers/oopsla18.pdf
	- https://dl.acm.org/doi/10.1145/3276496
- Correctness Testing of Loop Optimizations in C and C++ Compilers
	- Seminar on Advanced Techniques & Tools for Software Evolution (SATToSE) 2018
		- Remi van Veen, Marcel Beemster, Clemens Grelck
		- https://staff.fnwi.uva.nl/c.u.grelck/publications/2018_SATToSE18_compiler_testing.pdf
	- 2018 Master's Thesis; Remi van Veen
		- https://solidsands.com/wp-content/uploads/thesis_remi_van_veen.pdf
	- https://github.com/msaroufim/C-compiler-optimizations
- Fuzzing Loop Optimizations in Compilers for C++ and Data-Parallel Languages
	- PLDI 2023
	- Vsevolod Livinskii, Dmitry Babokin, John Regehr
	- https://doi.org/10.1145/3591295
	- https://users.cs.utah.edu/~regehr/pldi23.pdf
	- https://github.com/intel/yarpgen
- LORE: A loop repository for the evaluation of compilers
	- International Symposium on Workload Characterization (IISWC) 2017
	- Zhi Chen, Zhangxiaowen Gong, Justin Josef Szaday, David C. Wong, David A. Padua, Alexandru Nicolau, Alexander V. Veidenbaum, Neftali Watkinson, Zehra Sura, Saeed Maleki, Josep Torrellas, Gerald DeJong
	- https://iacoma.cs.uiuc.edu/iacoma-papers/iiswc17.pdf
	- https://iacoma.cs.uiuc.edu/iacoma-papers/PRES/present_iiswc17.pdf

#### Testing: Readings: Performance Optimization: Vectorization

- An Evaluation of Vectorizing Compilers
	- Parallel Architectures and Compilation Techniques (PACT) 2011
	- Saeed Maleki, Yaoqing Gao, María J. Garzarán, Tommy Wong, David A. Padua
	- https://dl.acm.org/doi/10.1109/PACT.2011.68
	- https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.927.6231&rep=rep1&type=pdf
- Evaluating Auto-Vectorizing Compilers through Objective Withdrawal of Useful Information
	- ACM Transactions on Architecture and Code Optimization (TACO) 16(4), 40 2019
	- Sergi Siso, Wes Armour, Jeyan Thiyagalingam
	- https://dl.acm.org/doi/abs/10.1145/3356842
	- https://ora.ox.ac.uk/objects/uuid:eac7b135-e92b-48dc-a1f7-4de66a441390
	- autovec-benchmark: Auto-vectorization test suite with withdrawal of useful compile-time information
		- https://github.com/sergisiso/autovec-benchmark
- Performance Left on the Table: An Evaluation of Compiler Auto-Vectorization for RISC-V
	- IEEE Micro 2022
	- Neil Adit, Adrian Sampson
	- https://ieeexplore.ieee.org/document/9802745
- A RISC-V Simulator and Benchmark Suite for Designing and Evaluating Vector Architectures
	- ACM Transactions on Architecture and Code Optimization (TACO), 2020
	- Cristóbal Ramírez Lazo, César-Alejandro Hernández-Calderón, Oscar Palomar, Osman Sabri Unsal, Marco Antonio Ramírez, Adrián Cristal
	- https://dl.acm.org/doi/10.1145/3422667
	- https://arxiv.org/abs/2111.01949
- Vectorizing Compilers: A Test Suite and Results
	- Supercomputing 1988
	- David Callahan, Jack Dongarra, David Levine
	- https://doi.org/10.1109/SUPERC.1988.44642
	- https://www.semanticscholar.org/paper/Vectorizing-compilers%3A-a-test-suite-and-results-Callahan-Dongarra/4b3dc3baae8a448a6dce5c8d132971f8455b685a

### Testing: Readings: Reduction

See also: [Testing](https://github.com/MattPD/cpplinks/blob/master/testing.md): [Reduction](https://github.com/MattPD/cpplinks/blob/master/testing.md#reduction)

- Automatic Test Case Reduction for OpenCL
	- IWOCL 2016
	- Moritz Pflanzer, Alastair F. Donaldson, Andrei Lascu
	- https://dl.acm.org/citation.cfm?id=2909439
	- paper: https://spiral.imperial.ac.uk/handle/10044/1/39576
	- slides: http://www.iwocl.org/wp-content/uploads/iwocl-2016-automatic-test-case-reduction.pdf
- Binary Reduction of Dependency Graphs
	- ESEC/FSE 2019
	- Christian Gram Kalhauge and Jens Palsberg
	- http://compilers.cs.ucla.edu/papers/binary-reduction/
	- https://dl.acm.org/doi/10.1145/3338906.3338956
	- JReduce: a tool to reduce Java ByteCode
		- https://github.com/ucla-pls/jreduce
- How to reduce LLVM crashes
	- 2023; Nikita Popov
	- https://www.npopov.com/2023/10/22/How-to-reduce-LLVM-crashes.html
- Perses: Syntax-Directed Program Reduction
	- https://github.com/chengniansun/perses
	- ICSE 2018
		- Chengnian Sun, Yuanbo Li, Qirun Zhang, Tianxiao Gu, Zhendong Su
		- https://dl.acm.org/doi/10.1145/3180155.3180236
		- https://people.inf.ethz.ch/suz/publications/perses.pdf
		- https://helloqirun.github.io/papers/icse18_chengnian.pdf
- ReduKtor: How We Stopped Worrying About Bugs in Kotlin Compiler
	- Automated Software Engineering (ASE) 2019
	- Daniil Stepanov, Marat Akhin, Mikhail Belyaev
	- https://arxiv.org/abs/1909.07331
- Test-Case Reduction and Deduplication Almost for Free with Transformation-Based Compiler Testing
	- PLDI 2021
	- Alastair Donaldson, Paul Thomson, Vasyl Teliman, Stefano Milizia, André Perez Maselco, Antoni Karpiński
	- https://doi.org/10.1145/3453483.3454092
	- http://multicore.doc.ic.ac.uk/publications/pldi-21.html
	- https://www.doc.ic.ac.uk/~afd/homepages/papers/pdfs/2021/PLDI.pdf
	- https://pldi21.sigplan.org/details/pldi-2021-papers/67/Test-Case-Reduction-and-Deduplication-Almost-for-Free-with-Transformation-Based-Compi
- Test-Case Reduction for C Compiler Bugs
	- PLDI 2012
	- John Regehr, Yang Chen, Pascal Cuoq, Eric Eide, Chucky Ellison, Xuejun Yang
	- https://www.cs.utah.edu/~regehr/papers/pldi12-preprint.pdf

#### Testing: Readings: Reduction: LLVM

- LLVM bugpoint
	- LLVM bugpoint tool: design and usage
		- https://llvm.org/docs/Bugpoint.html
	- Reduce Your Testcases with Bugpoint and Custom Scripts
		- https://blog.llvm.org/posts/2015-11-12-reduce-your-testcases-with-bugpoint-and/
	- How to reduce a test case using LLVM bugpoint?
		- 2020; Djordje Todorovic
		- https://djolertrk.github.io/llvm-debug-info-blog/
- LLVM-Reduce for testcase reduction
	- 2019 LLVM Developers’ Meeting; Diego Trevino Ferrer
	- https://www.youtube.com/watch?v=n1jDj7J9N8c
- reduce_pipeline: Automatic 'opt' pipeline reducer script
	- Script for automatic 'opt' pipeline reduction for when using the new pass-manager (NPM). Based around the '-print-pipeline-passes' option.
	- https://github.com/llvm/llvm-project/blob/main/llvm/utils/reduce_pipeline.py
	- https://reviews.llvm.org/D110908

## Testing: Software

- DejaGnu - GNU Test Framework
	- https://www.gnu.org/software/dejagnu/
	- GCC Wiki: How to prepare a testcase
		- https://gcc.gnu.org/wiki/HowToPrepareATestcase
	- GCC Contributors Guide: Working with the testsuite
		- https://dmalcolm.fedorapeople.org/gcc/newbies-guide/working-with-the-testsuite.html
	- GCC Testing Efforts
		- https://gcc.gnu.org/testing/
	- Howto: Using DejaGnu for Testing - A Simple Introduction 
		- https://www.embecosm.com/appnotes/ean8/ean8-howto-dejagnu-1.0.html
	- bunsen: Toolkit for compact storage and analysis of DejaGNU test results
		- https://github.com/serhei/bunsen
- Effcee: a C++ library for stateful pattern matching of strings, inspired by LLVM's FileCheck
	- https://github.com/google/effcee
- FileCheck - Flexible pattern matching file verifier
	- https://llvm.org/docs/CommandGuide/FileCheck.html
- Fuzzing LLVM libraries and tools - https://llvm.org/docs/FuzzingLLVM.html
	- Adventures in Fuzzing Instruction Selection
		- 2017 EuroLLVM Developers’ Meeting; Justin Bogner
		- http://llvm.org/devmtg/2017-03/assets/slides/adventures_in_fuzzing_instruction_selection.pdf
		- https://www.youtube.com/watch?v=UBbQ_s6hNgg
	- Structure-aware fuzzing for Clang and LLVM with libprotobuf-mutator
		- 2017 LLVM Developers’ Meeting; Kostya Serebryany, Vitaly Buka, Matt Morehouse
		- https://www.youtube.com/watch?v=U60hC16HEDY
- gcc-for-llvm-testing: A modified GCC test suite suitable for testing non-GCC compilers
	- https://github.com/embecosm/gcc-for-llvm-testing
	- Using the GCC regression test suite for LLVM (and other compilers)
		- GNU Tools Cauldron 2018; Simon Cook
		- https://speakerdeck.com/simonpcook/using-the-gcc-regression-test-suite-for-llvm-and-other-compilers
	- Repurposing GCC Regression for LLVM Based Tool Chains
		- 2018 LLVM Developers’ Meeting; Jeremy Bennett
		- https://www.youtube.com/watch?v=GV4PoWu0UZ0
- GraphicsFuzz: A testing framework for automatically finding and simplifying bugs in graphics shader compilers.
	- https://github.com/google/graphicsfuzz
	- GraphicsFuzz: Metamorphic Testing for Graphics Shader Compilers
		- VF Conference 2019; Alastair Donaldson
		- https://www.youtube.com/watch?v=r2GHwhCbcKo
	- shader-compiler-bugs: A collection of shader compiler bugs
		- https://github.com/mc-imperial/shader-compiler-bugs
- lang_tester: Rust testing framework for compilers and VMs
	- https://crates.io/crates/lang_tester
- lit - LLVM Integrated Tester
	- https://pypi.org/project/lit/
	- Using LLVM LIT Out-Of-Tree
		- 2020; Min-Yih Hsu
		- https://medium.com/@mshockwave/using-llvm-lit-out-of-tree-5cddada85a78
	- Pushing Back Lit's Boundaries to Test Libc++
		- 2020 LLVM Developers’ Meeting; Louis Dionne
		- https://www.youtube.com/watch?v=z5-wo0TW26M
- llvm-mutate – mutate LLVM IR - http://eschulte.github.io/llvm-mutate/
- OutputCheck: A tool for checking tool output inspired by LLVM's FileCheck
	- https://github.com/stp/OutputCheck/
- prog-fuzz: Compiler/source code fuzzing tool using AFL instrumentation
	- https://github.com/vegard/prog-fuzz
- Turnt: Tiny Unified Runner N' Tester
	- simple snapshot-style integration testing for commands
	- https://github.com/cucapra/turnt

### Testing: Software: Generation

- afl-compiler-fuzzer: Variation of american fuzzy lop for testing compilers
	- https://github.com/agroce/afl-compiler-fuzzer
- Csmith, a random generator of C programs
	- https://github.com/csmith-project/csmith
	- https://embed.cs.utah.edu/csmith/
	- Csmith testing - http://blog.frama-c.com/index.php?pages/Csmith-testing
- FuzzGen
	- Generates fuzz programs using grammar.
	- Provided grammars: C++, Java, LLVM IR, Scala.
	- https://github.com/AzulSystems/FuzzGen
- kscope
	- a library which recursively generates randomized code while keeping it 100% equivalent to the original one
	- http://ithare.com/c17-compiler-bug-hunt-very-first-results-12-bugs-reported-3-already-fixed/
	- https://github.com/ITHare/kscope
- ldrgen: Liveness-driven random C code generator
	- https://github.com/gergo-/ldrgen
- Orange3
	- a tool to test C compilers with randomly generated programs; mainly targets arithmetic optimization such as constant folding.
	- https://ist.ksc.kwansei.ac.jp/~ishiura/pub/orange3/
	- https://github.com/ishiura-compiler/Orange3
- Orange4
	- a tool to test C compilers by randomly generated programs; based on equivalent transformations on C programs and can generate wider class of C test programs than Orange3.
	- https://ist.ksc.kwansei.ac.jp/~ishiura/pub/orange4/
	- https://github.com/ishiura-compiler/Orange4
- Quest: A tool for testing C compilers
	- a tool that generates C code for testing C compilers
	- https://github.com/lindig/quest
- StarSmith
	- Language-Agnostic Generation of Compilable Test Programs
	- International Conference on Software Testing, Validation and Verification (ICST) 2020
	- Patrick Kreutzer, Stefan Kraus, Michael Philippsen
	- https://icst2020.info/details/icst-2020-papers/2/Language-Agnostic-Generation-of-Compilable-Test-Programs
	- https://ieeexplore.ieee.org/abstract/document/9159098
	- https://github.com/FAU-Inf2/StarSmith
- Xsmith: a library and DSL for creating random program generators
	- https://www.flux.utah.edu/project/xsmith
	- https://gitlab.flux.utah.edu/xsmith/xsmith
- yarpgen: Yet Another Random Program Generator
	- a random C/C++ program generator, which produces correct runnable C/C++ programs
	- specifically designed to trigger compiler optimization bugs and is intended for compiler testing
	- https://github.com/intel/yarpgen
	- Finding Bugs in C and C++ Compilers using YARPGen
		- https://blog.sigplan.org/2021/01/14/finding-bugs-in-c-and-c-compilers-using-yarpgen/

### Testing: Software: Performance Optimization

- AnghaBench: A Suite with One Million Compilable C Benchmarks for Code-Size Reduction
	- Angha Project
		- http://cuda.dcc.ufmg.br/angha/
		- https://github.com/brenocfg/AnghaBench
- CF3: Test suite for arithmetic optimization of C compilers
	- https://ist.ksc.kwansei.ac.jp/~ishiura/pub/CF3/
	- https://github.com/ishiura-compiler/CF3
- Compiler-benchmark-suites
	- A list of benchmark suites used in the research related to compilers, program performance, scientific computations, etc.
	- https://github.com/quepas/Compiler-benchmark-suites
- ExeBench: An ML-Scale Dataset of Executable C Functions
	- International Symposium on Machine Programming (MAPS) 2022
	- Jordi Armengol-Estapé, Jackson Woodruff, Alexander Brauckmann, José Wesley de Souza Magalhães, Michael F. P. O'Boyle
	- https://dl.acm.org/doi/10.1145/3520312.3534867
	- https://github.com/jordiae/exebench
	- https://huggingface.co/datasets/jordiae/exebench
- Jotai Benchmarks: Collection of executable benchmarks
	- https://github.com/lac-dcc/jotai-benchmarks
	- Jotai: a Methodology for the Generation of Executable C Benchmarks
		- 2022 technical report
		- Cecília Conde Kind, Michael Canesche, Fernando M. Quintão Pereira
		- https://raw.githubusercontent.com/lac-dcc/jotai-benchmarks/main/assets/doc/LaC_TechReport022022.pdf
- llvm-test-suite: LLVM "test-suite" Repository
	- https://github.com/llvm/llvm-test-suite
	- Compile Time Mark: a collection of applications used for compiler performance testing
		- https://github.com/llvm/llvm-test-suite/tree/main/CTMark
	- MicroBenchmarks
		- https://github.com/llvm/llvm-test-suite/tree/main/MicroBenchmarks
	- MultiSource/Benchmarks
		- https://github.com/llvm/llvm-test-suite/tree/main/MultiSource/Benchmarks
	- SingleSource/Benchmarks
		- https://github.com/llvm/llvm-test-suite/tree/main/SingleSource/Benchmarks
	- tf: Easily run llvm test-suite benchmarks; a simple test framework built using bash
		- https://github.com/guilhermeleobas/tf
		- https://github.com/brenocfg/tf
	- Benchmarks: LLVM test suite benchmarks (260 benchmarks - 36 test suites) 
		- https://github.com/lac-dcc/Benchmarks
- LongFruit: Quickly Finding RISC-V Code Quality Issues with Differential Analysis
	- https://www.lowrisc.org/blog/2020/10/how-we-used-differential-testing-to-rapidly-find-and-fix-missed-optimisation-opportunities-in-llvms-risc-v-backend/
	- https://github.com/lowRISC/longfruit
- LORE: LOop Repository for the Evaluation of compilers
	- http://www.vectorization.computer/
- opt-fuzz: a simple implementation of bounded exhaustive testing for LLVM programs
	- https://github.com/regehr/opt-fuzz

#### Testing: Software: Performance Optimization: Parallelization

- AutoParBench: a benchmark framework to evaluate compilers and tools designed to automatically insert OpenMP directives
	- https://github.com/LLNL/AutoParBench
	- AutoParBench: A Unified Test Framework for OpenMP-based Parallelizers
		- International Conference on Supercomputing 2020
		- Gleison Souza Diniz Mendonça, Chunhua Liao, Fernando Magno Quintão Pereira
		- https://doi.org/10.1145/3392717.3392744
		- https://www.osti.gov/servlets/purl/1635776
- Parallel loops – A test suite for parallelizing compilers: Description and example results
	- Parallel Computing 17, 10 (1991)
	- Jack Dongarra, Mark Furtney, Steve Reinhardt, Jerry Russell
	- https://doi.org/10.1016/S0167-8191(05)80036-5
- SOLLVE V&V: OpenMP Offloading Validation & Verification Suite
	- https://github.com/SOLLVE/sollve_vv
	- https://crpl.cis.udel.edu/ompvvsollve
	- ECP SOLLVE: Validation and Verification Testsuite Status Update and Compiler Insight for OpenMP
		- 2022
		- Thomas Huber, Swaroop Pophale, Nolan Baker, Michael Carr, Nikhil Rao, Jaydon Reap, Kristina Holsapple, Joshua Hoke Davis, Tobias Burnus, Seyong Lee, David E. Bernholdt, Sunita Chandrasekaran
		- https://arxiv.org/abs/2208.13301

#### Testing: Software: Performance Optimization: Vectorization

- autovec-benchmark: Auto-vectorization test suite with withdrawal of useful compile-time information
	- https://github.com/sergisiso/autovec-benchmark
- NeuroVectorizer training data
	- https://github.com/intel/neuro-vectorizer/tree/master/training_data
	- NeuroVectorizer: End-to-End Vectorization with Deep Reinforcement Learning
	- CGO 2020
	- Ameer Haj-Ali, Nesreen K. Ahmed, Ted Willke, Sophia Shao, Krste Asanovic, Ion Stoica
	- https://arxiv.org/abs/1909.13639
	- https://github.com/intel/neuro-vectorizer
- RiVEC: RISC-V Vectorized Benchmark Suite
	- https://github.com/RALC88/riscv-vectorized-benchmark-suite
	- A RISC-V Simulator and Benchmark Suite for Designing and Evaluating Vector Architectures
		- ACM Transactions on Architecture and Code Optimization (TACO), 2020
		- Cristóbal Ramírez Lazo, César-Alejandro Hernández-Calderón, Oscar Palomar, Osman Sabri Unsal, Marco Antonio Ramírez, Adrián Cristal
		- https://dl.acm.org/doi/10.1145/3422667
		- https://arxiv.org/abs/2111.01949
- TSVC: Test Suite for Vectorizing Compilers
	- https://github.com/UoB-HPC/TSVC_2
	- https://github.com/llvm/llvm-test-suite/tree/main/MultiSource/Benchmarks/TSVC
- VectorBench: Benchmarks for vectorization
	- VectorBench is a suite of C and C++ benchmark functions that you can use to evaluate the efficacy of your compiler transformations, particularly those that auto-vectorize scalar code or revectorize SIMD code. VectorBench includes a unique suite of more than 200 hand-vectorized functions, most of which have scalar equivalents.
	- https://github.com/revec/VectorBench
	- https://www.nextgenvec.org/
	- Revec: Program Rejuvenation through Revectorization
		- Compiler Construction 2019
		- Charith Mendis, Ajay Jain, Paras Jain, Saman Amarasinghe
		- https://arxiv.org/abs/1902.02816

### Testing: Software: Reduction

- C-Reduce, a C program reducer
	- https://embed.cs.utah.edu/creduce/
	- https://github.com/csmith-project/creduce
	- https://github.com/zjturner/creduce-windows
	- Design and Evolution of C-Reduce
		- Part 1: https://blog.regehr.org/archives/1678
		- Part 2: https://blog.regehr.org/archives/1679
- C-Vise: a super-parallel Python port of the C-Reduce
	- The port is fully compatible to the C-Reduce and uses the same efficient LLVM-based C/C++ reduction tool named clang_delta.
	- https://github.com/marxin/cvise
- comby-reducer: A simple program reducer for any language
	- A program and data format reducer for arbitrary language syntax. Produces human comprehensible output. Define declarative transformations with ease.
	- https://github.com/comby-tools/comby-reducer
	- https://comby.dev/blog/2021/03/26/comby-reducer

## Testing: Talks

- A Year of Experience with Broad Based Continuous Testing with GCC
	- GNU Tools Cauldron 2019; Jeff Law
	- https://www.youtube.com/watch?v=DznwK2ht0qc&list=PL_GiHdX17Wtx2Bu1O_bREetZZv4moIaRi&index=27
	- https://gcc.gnu.org/wiki/cauldron2019#cauldron2019talks.A_year_of_experience_with_broad_based_continuous_testing_with_GCC
- Adventures in Fuzzing Instruction Selection
	- EuroLLVM 2017; Justin Bogner
	- https://www.youtube.com/watch?v=UBbQ_s6hNgg
	- http://llvm.org/devmtg/2017-03//assets/slides/adventures_in_fuzzing_instruction_selection.pdf
- Coverage-Directed Differential Testing of JVM Implementations
	- PLDI 2016; Yuting Chen
	- https://www.youtube.com/watch?v=2Reaqfp4v-g
	- http://cse.sjtu.edu.cn/~zhao/pub/pdf/pldi2016.pdf
- Exposing Difficult Compiler Bugs With Random Testing
	- GCC Developers' Summit 2010; John Regehr, Xuejun Yang, Yang Chen, Eric Eide
	- https://gcc.gnu.org/wiki/summit2010?action=AttachFile&do=get&target=regehr_gcc_summit_2010.pdf
- FileCheck
	- FileCheck Follies
		- 2016 LLVM Developers’ Meeting; Paul Robinson
		- https://www.youtube.com/watch?v=4rhW8knj0L8
		- http://www.llvm.org/devmtg/2016-11/Slides/Robinson-FilecheckFollies.pdf
	- FileCheck: learning arithmetic
		- 2019 LLVM Developers’ Meeting; Thomas Preud'homme
		- https://www.youtube.com/watch?v=mcrQ5f-mASw
		- https://llvm.org/devmtg/2019-10/slides/Preudhomme-FileCheck.pdf
- Finding Missed Optimizations in LLVM (and other compilers)
	- EuroLLVM 2018; Gergö Barany
	- https://www.youtube.com/watch?v=V6ug3e3jC54
	- http://llvm.org/devmtg/2018-04/slides/Barany-Finding%20Missed%20Optimizations%20in%20LLVM.pdf
	- https://github.com/gergo-/missed-optimizations/
- Getting Started with the LLVM Testing Infrastructure
	- 2019 LLVM Developers’ Meeting; Brian Homerding, Michael Kruse
	- https://www.youtube.com/watch?v=isVQ8kYqaSA
	- https://llvm.org/devmtg/2019-10/slides/Homerding-Kruse-LLVMTestingInfrastructureTutorial.pdf
- Guaranteeing the correctness of MC for ARM
	- 2012 EuroLLVM Developers’ Meeting; Richard Barton
	- https://www.youtube.com/watch?v=3A-QM8hWmAc
	- http://llvm.org/devmtg/2012-04-12/Slides/Richard_Barton.pdf
- Testing and Qualification of Optimizing Compilers for Functional Safety
	- 2019 EuroLLVM Developers’ Meeting; José Luis March Cabrelles
	- https://www.youtube.com/watch?v=nSfT4oND9dU
- Testing Language Implementations
	- Programming Language Implementation Summer School (PLISS) 2017; Alastair Donaldson
	- https://www.youtube.com/watch?v=ZJUk8_k1HbY

### Testing: Talks: Performance Optimization

- Protecting Compiler Optimizations with Linaro Benchmarking CI
	- Arm Tech Talk 2023
	- Maxim Kuvyrkov
	- https://www.youtube.com/watch?v=ydAOVJqeL5o&t=156s

---

# Validation

Validation: Including translation validation, equivalence checking.

## Validation: 2024

- Modeling Dynamic (De)Allocations of Local Memory for Translation Validation
	- OOPSLA 2024
	- Abhishek Rose, Sorav Bansal
	- https://dl.acm.org/doi/10.1145/3649863
	- Technical Report
		- https://arxiv.org/abs/2403.05302
- Translation Validation for JIT Compiler in the V8 JavaScript Engine
	- ICSE 2024
	- Seungwan Kwon, Jaeseong Kwon, Wooseok Kang, Juneyoung Lee, Kihong Heo
	- https://dl.acm.org/doi/10.1145/3597503.3639189
	- https://conf.researchr.org/details/icse-2024/icse-2024-research-track/189/Translation-Validation-for-JIT-Compiler-in-the-V8-JavaScript-Engine
	- https://kihongheo.kaist.ac.kr/publications/icse24.pdf
	- https://github.com/prosyslab/turbo-tv-artifact

## Validation: 2022

- End-to-End Translation Validation for the Halide Language
	- OOPSLA 2022
	- Basile Clément, Albert Cohen
	- https://dl.acm.org/doi/10.1145/3527328
	- https://cambium.inria.fr/~bclement/papers/tv-oopsla-2022.pdf
- Finding JIT Optimizer Bugs using SMT Solvers and Fuzzing
	- 2022
	- Carl Friedrich Bolz-Tereick
	- https://www.pypy.org/posts/2022/12/jit-bug-finding-smt-fuzzing.html
- GCC Translation Validation
	- 2022-2023
	- Krister Walfridsson
	- https://kristerw.github.io/2022/09/13/translation-validation/
	- pysmtgcc: Some experiments with SMT solvers and GIMPLE IR
		- https://github.com/kristerw/pysmtgcc
	- smtgcc: an experimental implementation of translation validation for GCC
		- https://github.com/kristerw/smtgcc
	- Part 1: Writing a GCC plugin in Python
		- https://kristerw.github.io/2022/10/20/gcc-python-plugin/
	- Part 2: Verifying GCC optimizations using an SMT solver
		- https://kristerw.github.io/2022/11/01/verifying-optimizations/
	- Part 3: Memory representation
		- https://kristerw.github.io/2023/07/17/memory-representation/
	- Part 4: Address calculations
		- https://kristerw.github.io/2023/07/18/address-calculations/
	- Part 5: Pointer alignment
		- https://kristerw.github.io/2023/07/20/pointer-alignment/
- SMT-Based Translation Validation for Machine Learning Compiler
	- CAV 2022: Computer Aided Verification
	- Seongwon Bang, Seunghyeon Nam, Inwhan Chun, Ho Young Jhoo, Juneyoung Lee
	- https://link.springer.com/chapter/10.1007/978-3-031-13188-2_19
	- MLIR-TV: A translation validation framework for MLIR
		- https://github.com/aqjune/mlir-tv
- Translation Validation of Tensor Compilers
	- 2022 PhD dissertation
	- Basile Clément
	- https://theses.hal.science/tel-03903895/

## Validation: 2021

- A Validated Semantics for LLVM IR
	- 2021 Ph.D. dissertation
	- Juneyoung Lee
	- https://sf.snu.ac.kr/juneyoung.lee/thesis/
- Alive2: Bounded Translation Validation for LLVM
	- PLDI 2021
	- Nuno P. Lopes, Juneyoung Lee, Chung-Kil Hur, Zhengyang Liu, John Regehr
	- https://doi.org/10.1145/3453483.3454030
	- https://www.cs.utah.edu/~regehr/alive2-pldi21.pdf
	- https://web.ist.utl.pt/nuno.lopes/pubs.php?id=alive2-pldi21
	- https://github.com/AliveToolkit/alive2
	- https://alive2.llvm.org/ce/
- An SMT Encoding of LLVM's Memory Model for Bounded Translation Validation
	- Conference on Computer-Aided Verification (CAV) 2021
	- Juneyoung Lee, Dongjoo Kim, Chung-Kil Hur, Nuno P. Lopes
	- https://web.ist.utl.pt/nuno.lopes/pubs.php?id=alive2-mem-cav21
- Language-Parametric Compiler Validation with Application to LLVM
	- Architectural Support for Programming Languages and Operating Systems (ASPLOS) 2021
	- Theodoros Kasampalis, Daejun Park, Zhengyao Lin, Vikram Adve, Grigore Rosu
	- https://dl.acm.org/doi/abs/10.1145/3445814.3446751
	- https://daejunpark.github.io/asplos21.pdf
	- https://zenodo.org/record/4322105

## Validation: 2020

- A Scalable Validation of Binary Lifters
	- PLDI 2020
	- Sandeep Dasgupta, & Vikram S. Adve
	- https://sdasgup3.github.io/files/pldi_2020.pdf
	- https://www.youtube.com/watch?v=veV6TuPsRYw
	- https://pldi20.sigplan.org/details/pldi-2020-papers/4/Scalable-Validation-of-Binary-Lifters
- Certified and Efficient Instruction Scheduling: Application to Interlocked VLIW Processors
	- OOPSLA 2020
	- Cyril Six, Sylvain Boulmé, David Monniaux
	- https://doi.org/10.1145/3428197
	- https://www.youtube.com/watch?v=a_sJr2CJ3Uk
	- https://2020.splashcon.org/details/splash-2020-oopsla/5/Certified-and-efficient-instruction-scheduling
	- https://hal.science/hal-02185883
	- https://gricad-gitlab.univ-grenoble-alpes.fr/certicompil/compcert-kvx
- Counterexample-Guided Correlation Algorithm for Translation Validation
	- OOPSLA 2020
	- Shubhani Gupta, Abhishek Rose, Sorav Bansal
	- https://doi.org/10.1145/3428289
	- https://www.youtube.com/watch?v=Bn_ekogqDcw
	- https://raw.githubusercontent.com/compilerai/compilerai-publications/master/counter.pdf

## Validation: 2019

- Semantic Program Alignment for Equivalence Checking
	- PLDI 2019
	- Berkeley Churchill, Oded Padon, Rahul Sharma, Alex Aiken
	- https://www.youtube.com/watch?v=FJGvInzaiAQ
	- https://raw.githubusercontent.com/bchurchill/pldi19-equivalence-checker/master/pldi2019.pdf
	- https://pldi19.sigplan.org/details/pldi-2019-papers/14/Semantic-Program-Alignment-for-Equivalence-Checking
	- Semantic Alignment Equivalence Checker
		- https://github.com/bchurchill/pldi19-equivalence-checker

## Validation: 2017

- Black-Box Equivalence Checking Across Compiler Optimizations
	- APLAS 2017
	- Manjeet Dahiya, Sorav Bansal
	- http://www.cse.iitd.ac.in/~sbansal/pubs/aplas17.pdf
- Modeling undefined behaviour semantics for checking equivalence across compiler optimizations
	- HVC 2017; Manjeet Dahiya, Sorav Bansal
	- http://www.cse.iitd.ernet.in/~sbansal/pubs/hvc17.pdf
	- http://www.cse.iitd.ac.in/~dahiya/hvc17.pdf
- Translation Validation for Verified, Efficient and Timely Operating Systems
	- 2017 PhD Dissertation; Thomas Sewell
	- http://handle.unsw.edu.au/1959.4/58861
	- https://ts.data61.csiro.au/publications/papers/Sewell:phd
	- https://ts.data61.csiro.au/projects/TS/compiler-correctness.pml
- Translation Validation of Bounded Exhaustive Test Cases
	- 2017; Nuno Lopes, John Regehr
	- https://blog.regehr.org/archives/1510
	- Translation Validation with Alive - https://github.com/nunoplopes/alive/tree/newsema/tv

## Validation: 2016

- Formally Verified Compilation of Low-Level C code
	- 2016 PhD Dissertation; Pierre Wilke
	- https://tel.archives-ouvertes.fr/tel-01483676
- Validating Optimizations of Concurrent C/C++ Programs
	- CGO 2016
	- Soham Chakraborty, Viktor Vafeiadis
	- https://plv.mpi-sws.org/validc/paper.pdf

## Validation: 2011-1978

- Evaluating value-graph translation validation for LLVM
	- Programming and Language Design Implementation (PLDI) 2011
	- Jean-Baptiste Tristan, Paul Govereau, Greg Morrisett
	- https://dl.acm.org/citation.cfm?id=1993498.1993533
- Proving the correctness of heuristically optimized code
	- CACM 1978; Hanan Samet
	- http://www.cs.umd.edu/~hjs/pubs/compilers/proving-correctness.pdf
- Translation validation
	- TACAS 1998
	- Amir Pnueli, Michael Siegel, Eli Singerman
	- https://dl.acm.org/citation.cfm?id=349314
	- "We present the notion of _translation validation_ as a new approach to the verification of translators (compilers, code generators). Rather than proving in advance that the compiler always produces a target code which correctly implements the source code (compiler verification), each individual translation (i.e. a run of the compiler) is followed by a validation phase which verifies that the target code produced on this run correctly implements the submitted source program."
- Translation Validation: Automatically Proving the Correctness of Translations Involving Optimized Code
	- [Hanan Samet](http://www.cs.umd.edu/~hjs/)
	- translation validation - http://www.cs.umd.edu/~hjs/hjscat.html#sectiontranslationvalidation
	- compiler testing - http://www.cs.umd.edu/~hjs/hjscat.html#sectioncompilertesting
	- http://www.cs.umd.edu/~hjs/pubs/compilers/CS-TR-75-498.pdf
	- http://www.cs.umd.edu/~hjs/slides/translation-validation-slides.pdf
- Translation Validation: From DC+ to C*
	- FM-Trends 1998
	- Amir Pnueli, Ofer Shtrichman, Michael Siegel
	- https://dl.acm.org/citation.cfm?id=729871
	- "Translation validation is an alternative to the verification of translators (compilers, code generators). Rather than proving in advance that the compiler always produces a target code which correctly implements the source code (compiler verification), each individual translation (i.e. a run of the compiler) is followed by a validation phase which verifies that the target code produced on this run correctly implements the submitted source program."
- Translation Validation for a Verified OS Kernel
	- PLDI 2013
	- Thomas Arthur Leck Sewell, Magnus O. Myreen, Gerwin Klein
	- https://doi.org/10.1145/2499370.2462183
	- https://www.cl.cam.ac.uk/~mom22/pldi13.pdf
- Translation validation for an optimizing compiler
	- PLDI 2000
	- George C. Necula
	- https://dl.acm.org/citation.cfm?id=349314

---

# Verification

- A Higher-Order Abstract Syntax Approach to the Verified Compilation of Functional Programs
	- 2016 PhD thesis; Yuting Wang
	- https://arxiv.org/abs/1702.03363
	- http://www.cs.yale.edu/homes/wang-yuting/files/phd_thesis.pdf
- A Verified Compiler for a Linear Function/Imperative Intermediate Language
	- 2018 PhD Thesis; Sigurd Schneider
	- https://www.ps.uni-saarland.de/Publications/documents/Schneider_2018_PhDThesis.pdf
	- LVC - Linear Verified Compiler: https://www.ps.uni-saarland.de/~sdschn/LVC.html
- ALIVe: Automatic LLVM InstCombine Verifier
	- https://github.com/nunoplopes/alive
	- online: http://rise4fun.com/Alive
	- blog post: http://blog.regehr.org/archives/1170
	- slides: http://llvm.org/devmtg/2014-10/Slides/Menendez-Alive.pdf
	- Alive-FP: Automated Verification of Floating Point Based Peephole Optimizations in LLVM
		- SAS 2016; David Menendez, Santosh Nagarakatte, Aarti Gupta
		- https://doi.org/doi:10.7282/T3XW4PC5
		- https://doi.org/10.1007/978-3-662-53413-7_16
	- Alive-Loops: https://github.com/rutgers-apl/alive-loops
		- Termination checking for LLVM peephole optimizations
		- ICSE 2016; David Menendez, Santosh Nagarakatte
		- https://www.cs.rutgers.edu/~sn349/papers/icse2016-alive-loops.pdf
	- Alive-NJ - https://github.com/rutgers-apl/alive-nj
	- LifeJacket: Verifying precise floating-point optimizations in LLVM
		- SOAP 2016, EuroLLVM 2017; Andres Nötzli, Fraser Brown
		- http://export.arxiv.org/abs/1603.09290
		- https://github.com/4tXJ7f/alive
		- http://llvm.org/devmtg/2017-03/2017/02/20/accepted-sessions.html#25
	- Practical Formal Techniques and Tools for Developing LLVM's Peephole Optimizations
		- 2018 PhD Thesis; David Menendez
		- https://www.cs.rutgers.edu/~santosh.nagarakatte/david-menendez-phd-thesis.pdf
	- Precondition Inference for Peephole Optimizations in LLVM
		- PLDI 2017
		- David Menendez, Santosh Nagarakatte
		- http://export.arxiv.org/abs/1611.05980
		- https://www.cs.rutgers.edu/~santosh.nagarakatte/papers/pldi2017-alive-infer.pdf
		- PLDI 2017 talk, David Menendez - https://pldi17.sigplan.org/event/pldi-2017-papers-precondition-inference-for-peephole-optimizations-in-llvm
	- Provably Correct Peephole Optimizations with Alive
		- PLDI 2015
		- Nuno P. Lopes, David Menendez, Santosh Nagarakatte, John Regehr
		- https://www.cs.utah.edu/~regehr/papers/pldi15.pdf
		- http://web.ist.utl.pt/nuno.lopes/pubs.php?id=alive-pldi15
	- AliveInLean: A Verified LLVM Peephole Optimization Verifier
		- Computer-Aided Verification (CAV) 2019
		- Juneyoung Lee, Chung-Kil Hur, Nuno P. Lopes
		- https://sf.snu.ac.kr/aliveinlean/
		- https://github.com/Microsoft/AliveInLean
- Alive2: Automatic verification of LLVM optimizations
	- https://github.com/AliveToolkit/alive2
	- https://alive2.llvm.org/
	- Alive2: Verifying Existing Optimizations
		- 2019 LLVM Developers’ Meeting; Nuno Lopes, John Regehr
		- https://www.youtube.com/watch?v=paJhdBp_iA4
		- https://llvm.org/devmtg/2019-10/slides/Lopes-Regehr-Alive2.pdf
	- Alive 2 Part 1: Introduction
		- https://blog.regehr.org/archives/1722
	- Alive2 Part 2: Tracking miscompilations in LLVM using its own unit tests
		- https://blog.regehr.org/archives/1737
	- Alive2 Part 3: Things You Can and Can’t Do with Undef in LLVM
		- https://blog.regehr.org/archives/1837
- An Abstract Stack Based Approach to Verified Compositional Compilation to Machine Code
	- POPL 2019
	- Yuting Wang, Pierre Wilke, Zhong Shao
	- https://popl19.sigplan.org/event/popl-2019-research-papers-an-abstract-stack-based-approach-to-verified-compositional-compilation-to-machine-code
- Blackbox Equivalence Checking of Program Optimizations
	- 2019 Ph.D. Dissertation; Berkeley Roshan Churchill
	- https://theory.stanford.edu/~aiken/publications/theses/churchill.pdf
- CakeML: A Verified Implementation of ML
	- https://cakeml.org/
	- https://github.com/CakeML/cakeml
	- Cakes That Bake Cakes: Dynamic Computation in CakeML
		- PLDI 2023
		- Thomas Sewell, Magnus O. Myreen, Yong Kiam Tan, Ramana Kumar, Alexander Mihajlovic, Oskar Abrahamsson, Scott Owens
		- https://doi.org/10.1145/3591266
		- https://cakeml.org/pldi23-eval.pdf
		- https://pldi23.sigplan.org/details/pldi-2023-pldi/47/Cakes-That-Bake-Cakes-Dynamic-Computation-in-CakeML
	- Verified Compilation of CakeML to Multiple Machine-Code Targets
		- Certified Programs and Proofs (CPP) 2017
		- Anthony Fox, Magnus O. Myreen, Yong Kiam Tan, Ramana Kumar.
		- http://www.cl.cam.ac.uk/~mom22/cpp17.pdf
		- http://www.cl.cam.ac.uk/~mom22/publications.html
	- Verified Compilation on a Verified Processor
		- PLDI 2019
		- Andreas Lööw, Ramana Kumar, Yong Kiam Tan, Magnus O. Myreen, Michael Norrish, Oskar Abrahamsson, Anthony Fox
		- https://cakeml.org/pldi19.pdf
	- The Verified CakeML Compiler Backend
		- JFP 2019
		- Yong Kiam Tan, Magnus O. Myreen, Ramana Kumar, Anthony Fox, Scott Owens, Michael Norrish
		- https://cakeml.org/jfp19.pdf
	- Icing: Supporting Fast-math Style Optimizations in a Verified Compiler
		- Computer-Aided Verification (CAV) 2019
		- Heiko Becker, Eva Darulova, Magnus O. Myreen, Zachary Tatlock
		- https://cakeml.org/cav19.pdf
	- Verified Compilation and Optimization of Floating-Point Programs in CakeML
		- ECOOP 2022
		- Heiko Becker, Robert Rabe, Eva Darulova, Magnus O. Myreen, Zachary Tatlock, Ramana Kumar, Yong Kiam Tan, Anthony Fox
		- https://2022.ecoop.org/details/ecoop-2022-papers/2/Verified-Compilation-and-Optimization-of-Floating-Point-Programs-in-CakeML
		- https://cakeml.org/ecoop22.pdf
- CompCert: formally-verified C compiler
	- http://compcert.inria.fr/
	- https://github.com/AbsInt/CompCert
	- CompCert Tutorial
		- November 2015; Ben Greenman
		- A fast walk through the CompCert compiler. Goes over the architecture, correctness strategy, and correctness proof.
		- http://www.ccs.neu.edu/home/types/resources/notes/compcert/cc.pdf
	- The formal verification of compilers - Xavier Leroy - DeepSpec Summer School 2017
		- https://deepspec.org/event/dsss17/lecture_leroy.html
		- http://gallium.inria.fr/~xleroy/courses/DSSS-2017/
	- A Verified CompCert Front-End for a Memory Model Supporting Pointer Arithmetic and Uninitialised Data
		- Journal of Automated Reasoning 62(4) (2019)
		- Frédéric Besson, Sandrine Blazy, Pierre Wilke
		- https://doi.org/10.1007/s10817-017-9439-z
		- https://hal.inria.fr/hal-01656895
	- An Abstract Stack Based Approach to Verified Compositional Compilation to Machine Code
		- POPL 2019
		- Yuting Wang, Pierre Wilke, Zhong Shao
		- https://www.youtube.com/watch?v=AK3wP1BK-K8
		- https://popl19.sigplan.org/event/popl-2019-research-papers-an-abstract-stack-based-approach-to-verified-compositional-compilation-to-machine-code
		- Stack-Aware CompCert and CompCert MC - https://certikos.github.io/compcertmc/
		- http://flint.cs.yale.edu/flint/publications/sacc.html
	- Closing the Gap – The Formally Verified Optimizing Compiler CompCert
		- SSS'17: Safety-critical Systems Symposium 2017
		- https://hal.inria.fr/hal-01399482/
	- CompCertELF: Verified Separate Compilation of C Programs into ELF Object Files
		- OOPSLA 2020
		- Yuting Wang, Xiangzhe Xu, Pierre Wilke, Zhong Shao
		- https://doi.org/10.1145/3428265
		- https://www.youtube.com/watch?v=po9lhcSWssg
		- https://2020.splashcon.org/details/splash-2020-oopsla/73/CompCertELF-Verified-Separate-Compilation-of-C-Programs-into-ELF-Object-Files
	- CompCertM: CompCert with Lightweight Modular Verification and Multi-Language Linking
		- POPL 2020
		- Youngju Song, Minki Cho, Dongjoo Kim, Yonghyun Kim, Jeehoon Kang, Chung-Kil Hur
		- https://sf.snu.ac.kr/compcertm/
	- CompCertS: A Memory-Aware Verified C Compiler Using a Pointer as Integer Semantics
		- Journal of Automated Reasoning 63(2) (2019)
		- Frédéric Besson, Sandrine Blazy, Pierre Wilke
		- https://doi.org/10.1007/s10817-018-9496-y
		- https://hal.inria.fr/hal-01656875
	- Compositional CompCert
		- POPL 2015
		- Stewart, G., Beringer, L., Cuellar, S., Appel, A.W.
		- https://github.com/PrincetonUniversity/compcomp
	- Formal Verification of a Constant-Time Preserving C Compiler
		- Principles of Programming Languages (POPL) 2020
		- Gilles Barthe, Sandrine Blazy, Benjamin Grégoire, Rémi Hutin, Vincent Laporte, David Pichardie, Alix Trieu
		- https://eprint.iacr.org/2019/926
		- http://cs.au.dk/%7Etrieu/POPL20/
		- Slides (Verified Software Workshop): https://vetss.org.uk/wp-content/uploads/sites/122/2019/10/Blazy-Formal-Verification-of-a-Constant-Time.pdf
		- https://vetss.org.uk/verified-software-workshop-programme/
		- https://doi.org/10.1145/3371075
		- A CompCert Compiler that Preserves Cryptographic Constant-time
			- Sandrine Blazy, Rémi Hutin, David Pichardie
			- PriSC 2020 Principles of Secure Compilation
			- https://popl20.sigplan.org/details/prisc-2020-papers/10/A-CompCert-Compiler-that-Preserves-Cryptographic-Constant-time
			- https://www.youtube.com/watch?v=eci48EC4v4o
	- Lightweight Verification of Separate Compilation
		- POPL 2016
		- Jeehoon Kang, Yoonseung Kim, Chung-Kil Hur, Derek Dreyer, Viktor Vafeiadis
		- https://sf.snu.ac.kr/sepcompcert/
	- Reconciling Low-Level Features of C with Compiler Optimizations
		- 2019 Ph.D. Dissertation; Jeehoon Kang
		- https://sf.snu.ac.kr/jeehoon.kang/thesis/
		- Chapter I, Section 2, Background: A Brief Tour of CompCert
		- Chapter III, Separate Compilation and Linking
		- Chapter IV, Cast between Integers and Pointers
	- Verified Peephole Optimizations for CompCert
		- PLDI 2016
		- Eric Mullen, Daryl Zuniga, Zachary Tatlock, Dan Grossman
		- http://peek.uwplse.org/
		- https://conf.researchr.org/event/pldi-2016/pldi-2016-papers-verified-peephole-optimizations-for-compcert-
		- Peek: a verified peephole optimizer for CompCert - https://github.com/uwplse/peek
- Compilation Using Correct-by-Construction Program Synthesis
	- 2016 Master's Thesis; Clément Pit-Claudel
	- http://pit-claudel.fr/clement/MSc/
	- https://dspace.mit.edu/handle/1721.1/107293
	- http://pit-claudel.fr/clement/MSc/FiatToFacade_Pit-Claudel_2016.pdf
- Compositional Verification of Compiler Optimisations on Relaxed Memory
	- ESOP 2018
	- Mike Dodds, Mark Batty, Alexey Gotsman
	- https://arxiv.org/abs/1802.05918
- Crellvm: Verified Credible Compilation for LLVM
	- Programming Languages Design and Implementation (PLDI) 2018
	- Jeehoon Kang, Yoonseung Kim, Youngju Song, Juneyoung Lee, Sanghoon Park, Mark Dongyeon Shin, Yonghyun Kim, Sungkeun Cho, Joonwon Choi,Chung-Kil Hur, Kwangkeun Yi
	- a verified credible compilation (or equivalently, verified translation validation) framework for LLVM
	- http://sf.snu.ac.kr/crellvm/
	- https://github.com/snu-sf/crellvm-tests-parallel
- Pilsner: A Compositionally Verified Compiler for a Higher-Order Imperative Language
	- International Conference on Functional Programming (ICFP) 2015
	- Georg Neis, Chung-Kil Hur, Jan-Oliver Kaiser, Craig McLaughlin, Derek Dreyer, Viktor Vafeiadis
	- https://people.mpi-sws.org/~dreyer/papers/pilsner/paper.pdf
	- http://plv.mpi-sws.org/pils/
- Program Logics for Certified Compilers
	- Andrew W. Appel with Robert Dockins, Aquinas Hobor, Lennart Beringer, Josiah Dodds, Gordon Stewart, Sandrine Blazy, Xavier Leroy
	- Cambridge University Press, 2014
	- https://www.cs.princeton.edu/%7Eappel/papers/plcc.pdf
- Pushing the Limits of Compiler Verification
	- 2018 PhD Thesis; Eric Mullen
	- https://homes.cs.washington.edu/~djg/theses/mullen_thesis.pdf
	- Œuf: Verified Coq Extraction in Coq - https://github.com/uwplse/oeuf
	- Peek: Verified Peephole Optimizations for CompCert - https://github.com/uwplse/peek
- Self-compilation and self-verification
	- 2017 Ph.D. Dissertation; Ramana Kumar
	- http://www.sigplan.org/Awards/Dissertation/2017_kumar.pdf
	- https://cakeml.org/
- Vale (Verified Assembly Language for Everest)
	- USENIX Security Symposium 2017
	- Barry Bond and Chris Hawblitzel, Manos Kapritsos, K. Rustan M. Leino, Jacob R. Lorch, Bryan Parno, Ashay Rane, Srinath Setty, Laure Thompson
	- https://github.com/project-everest/vale
	- https://www.microsoft.com/en-us/research/publication/vale-verifying-high-performance-cryptographic-assembly-code/
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/bond
- Vellvm: Verifying the LLVM
	- http://www.cis.upenn.edu/~stevez/vellvm/
	- https://github.com/vellvm
	- DeepSpec Summer School 2017; Steve Zdancewic - https://deepspec.org/event/dsss17/lecture_zdancewic.html
	- Galois, Inc. Tech Talk 2018; Steve Zdancewic
		- https://galois.com/blog/2018/07/vellvm-verifying-the-llvm/
		- https://www.youtube.com/watch?v=qGpRKkP8gec
	- Strange Loop 2018; Steve Zdancewic
		- https://www.youtube.com/watch?v=q6gSC3OxB_8
		- https://thestrangeloop.com/2018/vellvm---verifying-the-llvm.html
- Verified Compilers for a Multi-Language World
	- Summit on Advances in Programming Languages (SNAPL) 2015
	- Amal Ahmed
	- http://www.ccs.neu.edu/home/amal/papers/verifcomp.pdf

## Verification: 2024

- From Mechanized Semantics to Verified Compilation: the Clight Semantics of CompCert
	- 2024 Fundamental Approaches to Software Engineering (FASE)
	- Sandrine Blazy
	- https://link.springer.com/chapter/10.1007/978-3-031-57259-3_1
- Lightweight, Modular Verification for WebAssembly-to-Native Instruction Selection
	- ACM International Conference on Architectural Support for Programming Languages and Operating Systems (ASPLOS) 2024
	- Alexa VanHattum, Monica Pardeshi, Chris Fallin, Adrian Sampson, and Fraser Brown
	- https://doi.org/10.1145/3617232.3624862
	- https://www.cs.cornell.edu/~avh/veri-isle-preprint.pdf
- Memory Simulations, Security and Optimization in a Verified Compiler
	- Certified Programs and Proofs (CPP) 2024
	- David Monniaux
	- https://dl.acm.org/doi/10.1145/3636501.3636952
	- https://arxiv.org/abs/2312.08117
	- https://www.youtube.com/watch?v=xXx87Ke5S3A
- Verified inlining and specialisation for PureCake
	- European Symposium on Programming (ESOP) 2024
	- Hrutvik Kanabar, Kacper Korban, Magnus O. Myreen
	- https://cakeml.org/esop24-inlining.pdf
- Verifying Peephole Rewriting in SSA Compiler IRs
	- Interactive Theorem Proving (ITP) 2024
	- Siddharth Bhat, Alex Keizer, Chris Hughes, Andrés Goens, Tobias Grosser
	- https://arxiv.org/abs/2407.03685
	- https://doi.org/10.4230/LIPIcs.ITP.2024.23
	- Lean-MLIR: A minimal development of SSA theory
		- https://github.com/opencompl/lean-mlir

## Verification: 2023

- Cachet: A Domain-Specific Language for Trustworthy Just-In-Time Compilers
	- PriSC 2023
	- Michael Smith, Abhishek Sharma, John Renner, David Thien, Sorin Lerner, Fraser Brown, Hovav Shacham, Deian Stefan
	- https://popl23.sigplan.org/details/prisc-2023-papers/10/Cachet-A-Domain-Specific-Language-for-Trustworthy-Just-In-Time-Compilers
	- https://www.spinda.net/papers/smith-2023-cachet.pdf
	- https://www.youtube.com/watch?v=LClrvto4U3E
- CryptOpt: Verified Compilation with Randomized Program Search for Cryptographic Primitives
	- PLDI 2023
	- Joel Kuepper, Andres Erbsen, Jason Gross, Owen Conoly, Chuyue Sun, Samuel Tian, David Wu, Adam Chlipala, Chitchanok Chuengsatiansup, Daniel Genkin, Markus Wagner, Yuval Yarom
	- https://doi.org/10.1145/3591272
	- https://arxiv.org/abs/2211.10665
	- https://pldi23.sigplan.org/details/pldi-2023-pldi/53/CryptOpt-Verified-Compilation-with-Randomized-Program-Search-for-Cryptographic-Primi
- FaJITa: Verifying Optimizations on Just-In-Time Programs
	- PriSC 2023
	- David Thien, Michael Smith, Evan Johnson, Sorin Lerner, Hovav Shacham, Deian Stefan, Fraser Brown
	- https://popl23.sigplan.org/details/prisc-2023-papers/7/FaJITa-Verifying-Optimizations-on-Just-In-Time-Programs
	- https://www.youtube.com/watch?v=e1zAWj-8mNc
	- https://davidthien.com/assets/pdf/fajita-prisc23-paper.pdf
- Formally Verifying Optimizations with Block Simulations
	- 2023
	- Léo Gourdin, Benjamin Bonneau, Sylvain Boulmé, David Monniaux, Alexandre Bérard
	- https://hal.science/hal-04102940/
- Lazy Code Transformations in a Formally Verified Compiler
	- ICOOOLPS 2023: ACM International Workshop on Implementation, Compilation, Optimization of OO Languages, Programs and Systems
	- Léo Gourdin
	- https://dl.acm.org/doi/abs/10.1145/3605158.3605848
	- https://hal.science/hal-04108775
- Verified compilation of a purely functional language to a realistic machine semantics
	 - 2023 PhD Dissertation
	 - Hrutvik Kanabar
	 - https://doi.org/10.22024/UniKent/01.02.105396
	 - https://kar.kent.ac.uk/105396/
	 - https://hrutvik.co.uk/assets/pdf/Hrutvik_Kanabar_thesis.pdf
	 - https://hrutvik.co.uk/assets/pdf/viva_voce_slides.pdf
- Verified Function Inlining Optimization for the PureCake Compiler
	- 2023 Master's Thesis
	- Kacper Korban
	- http://hdl.handle.net/20.500.12380/306357
- Verifying the Verifier: eBPF Range Analysis Verification
	- International Conference on Computer Aided Verification (CAV) 2023
	- Harishankar Vishwanathan, Matan Shachnai, Srinivas Narayana, Santosh Nagarakatte
	- https://people.cs.rutgers.edu/~sn349/papers/agni-cav2023.pdf

## Verification: 2022

- Formal Verification of Just-in-Time Compilation
	- 2022 PhD Dissertation
	- Aurèle Barrière
	- https://theses.hal.science/tel-03987749
	- Defense Recording
		- https://www.youtube.com/watch?v=mbkF3BwenV4
- Formally Verified Loop-Invariant Code Motion and Assorted Optimizations
	- ACM Transactions on Embedded Computing Systems (TECS) 2022
	- David Monniaux, Cyril Six
	- https://doi.org/10.1145/3529507
- Formally Verified Native Code Generation in an Effectful JIT - or: Turning the CompCert Backend into a Formally Verified JIT Compiler
	- POPL 2023
	- Aurèle Barrière, Sandrine Blazy, David Pichardie
	- https://doi.org/10.1145/3571202
	- https://arxiv.org/abs/2212.03129
	- https://hal.inria.fr/hal-03882598
	- https://github.com/Aurele-Barriere/FM-JIT
- Formally Verified Superblock Scheduling
	- CPP 2022: ACM SIGPLAN International Conference on Certified Programs and Proofs
	- Cyril Six, Léo Gourdin, Sylvain Boulmé, David Monniaux, Justus Fasse, Nicolas Nardino
	- https://dl.acm.org/doi/pdf/10.1145/3497775.3503679
	- https://gricad-gitlab.univ-grenoble-alpes.fr/certicompil/compcert-kvx/-/tree/CPP22_main
- PureCake: A Verified Compiler for a Lazy Functional Language
	- PLDI 2023
	- Hrutvik Kanabar, Samuel Vivien, Oskar Abrahamsson, Magnus O. Myreen, Michael Norrish, Johannes Åman Pohjola, Riccardo Zanetti
	- https://dl.acm.org/doi/10.1145/3591259
	- https://pldi23.sigplan.org/details/pldi-2023-pldi/40/PureCake-A-Verified-Compiler-for-a-Lazy-Functional-Language
	- https://hrutvik.co.uk/assets/pdf/PureCake_slides_long.pdf
	- https://www.youtube.com/watch?v=pEVBUfEFW8k&t=558s
	- https://cakeml.org/purecake/
	- https://github.com/CakeML/pure
- The Trusted Computing Base of the CompCert Verified Compiler
	- European Symposium on Programming (ESOP) 2022
	- David Monniaux, Sylvain Boulmé
	- https://arxiv.org/abs/2201.10280
	- https://hal.archives-ouvertes.fr/hal-03541595
- Verified Compilation of C Programs with a Nominal Memory Model
	- POPL 2022
	- Yuting Wang, Ling Zhang, Zhong Shao, Jérémie Koenig
	- https://doi.org/10.1145/3498686
	- https://github.com/SJTU-PLV/nominal-compcert-popl22-artifact
	- https://popl22.sigplan.org/details/POPL-2022-popl-research-papers/25/Verified-Compilation-of-C-Programs-with-a-Nominal-Memory-Model
- Verified Tensor-Program Optimization Via High-level Scheduling Rewrites
	- POPL 2022
	- Amanda Liu, Gilbert Louis Bernstein, Adam Chlipala, Jonathan Ragan-Kelley
	- https://doi.org/10.1145/3498717
	- https://www.youtube.com/watch?v=f2NEU1ENt6A
	- https://popl22.sigplan.org/details/POPL-2022-popl-research-papers/55/Verified-Tensor-Program-Optimization-Via-High-level-Scheduling-Rewrites
	- Verified ATL Scheduling Framework
		- https://github.com/ChezJrk/verified-scheduling
	- SAMPL Talk 2022/04/21
		- https://www.youtube.com/watch?v=AUe9lzhBOgc

## Verification: 2021

- A Minimalistic Verified Bootstrapped Compiler (Proof Pearl)
	- Certified Programs and Proofs (CPP) 2021
	- Magnus O. Myreen
	- https://doi.org/10.1145/3437992.3439915
	- http://www.cse.chalmers.se/~myreen/cpp2021-bootstrap-myreen.pdf
	- https://www.youtube.com/watch?v=Ip6Y4O2T60Y
- Formal Verification of High-Level Synthesis
	- OOPSLA 2021
	- Yann Herklotz, James D. Pollard, Nadesh Ramanathan, John Wickerson
	- https://doi.org/10.1145/3485494
	- https://yannherklotz.com/papers/fvhls_oopsla21.pdf
	- Vericert: A formally verified high-level synthesis tool based on CompCert and written in Coq
		- https://github.com/ymherklotz/vericert
		- https://johnwickerson.wordpress.com/2021/08/27/vericert/
- Formally Verified Speculation and Deoptimization in a JIT Compiler
	- POPL 2021
	- Aurèle Barrière, Sandrine Blazy, Olivier Flückiger, David Pichardie, Jan Vitek
	- https://doi.org/10.1145/3434327
	- https://www.youtube.com/watch?v=1W1LQWBVfz4
	- https://popl21.sigplan.org/details/POPL-2021-research-papers/46/Formally-Verified-Speculation-and-Deoptimization-in-a-JIT-Compiler
- Relational compilation for end-to-end verification
	- 2021 PhD Dissertation
	- Clément Pit-Claudel
	- https://people.csail.mit.edu/cpitcla/thesis/thesis.html
	- https://people.csail.mit.edu/cpitcla/thesis/thesis.pdf

## Verification: 2020

- A Verified Packrat Parser Interpreter for Parsing Expression Grammars
	- Conference on Certified Programs and Proofs (CPP) 2020
	- Clement Blaudeau, Natarajan Shankar
	- https://arxiv.org/abs/2001.04457
	- https://www.youtube.com/watch?v=hLjRcMAMuts
- Mechanized Semantics and Verified Compilation for a Dataflow Synchronous Language with Reset
	- POPL 2020
	- Timothy Bourke, Lélio Brun, Marc Pouzet
	- https://popl20.sigplan.org/details/POPL-2020-Research-Papers/20/Mechanized-Semantics-and-Verified-Compilation-for-a-Dataflow-Synchronous-Language-wit
	- https://github.com/INRIA/velus
- Specification and verification in the field: Applying formal methods to BPF just-in-time compilers in the Linux kernel
	- Operating Systems Design and Implementation (OSDI) 2020
	- Luke Nelson, Jacob Van Geffen, Emina Torlak, Xi Wang
	- https://unsat.cs.washington.edu/papers/nelson-jitterbug.pdf
	- https://github.com/uw-unsat/jitterbug
- The Correctness of a Code Generator for a Functional Language
	- Verification, Model Checking, and Abstract Interpretation (VMCAI) 2020
	- Nathanaël Courant, Antoine Séré, Natarajan Shankar
	- https://doi.org/10.1007/978-3-030-39322-9_4
- Towards a Verified Range Analysis for JavaScript JITs
	- Programming Language Design and Implementation (PLDI) 2020
	- Fraser Brown, John Renner, Andres Nötzli, Sorin Lerner, Hovav Shacham, Deian Stefan
	- https://doi.org/10.1145/3385412.3385968
	- https://vera.programming.systems
	- https://github.com/PLSysSec/vera
	- https://pldi20.sigplan.org/details/pldi-2020-papers/8/Towards-a-Verified-Range-Analysis-for-JavaScript-JITs
	- https://www.youtube.com/watch?v=5tRK5_GPdpM
- Towards Formally Verified Just-In-Time Compilation
	- CoqPL 2020
	- Aurèle Barrière, Sandrine Blazy, David Pichardie
	- https://www.youtube.com/watch?v=Be-CwSREJOI
	- https://popl20.sigplan.org/details/CoqPL-2020-papers/4/Towards-Formally-Verified-Just-in-Time-compilation
- Verified Optimizations for Functional Languages
	- 2020 PhD Dissertation; Zoe Paraskevopoulou
	- https://www.cs.princeton.edu/research/techreps/TR-006-20
	- https://zoep.github.io/thesis_final.pdf
- Verifying and Improving Halide’s Term Rewriting System with Program Synthesis
	- OOPSLA 2020
	- Julie L. Newcomb, Andrew Adams, Steven Johnson, Rastislav Bodik, Shoaib Kamil
	- https://2020.splashcon.org/details/splash-2020-oopsla/42/Verifying-and-Improving-Halide-s-Term-Rewriting-System-with-Program-Synthesis
	- https://dl.acm.org/doi/10.1145/3428234

## Verification: Talks

- CompCert: A Journey through the Landscape of Mechanized Semantics for Verified Compilation
	- Certified Programs and Proofs (CPP) 2023 (Keynote)
	- Sandrine Blazy
	- https://www.youtube.com/watch?v=9KhagyiGQ_A
	- https://popl23.sigplan.org/details/CPP-2023-papers/26/CompCert-a-journey-through-the-landscape-of-mechanized-semantics-for-verified-compil
- How Badly Do We Want Correct Compilers?
	- NDC TechTown 2023
	- John Regehr
	- https://www.youtube.com/watch?v=tMYYrR-hazI
- Verifying optimizations using SMT solvers
	- 2013 LLVM Developers’ Meeting; Nuno Lopes
	- https://www.youtube.com/watch?v=njav5YxXaCs
	- https://llvm.org/devmtg/2013-11/slides/Lopes-SMT.pdf
