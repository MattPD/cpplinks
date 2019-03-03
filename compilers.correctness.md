# [C++ links](README.md): compilers - correctness

Note: see also [compilers](compilers.md)

# Contents

* [General](#general)
* [Testing](#testing)
	+ [Articles](#articles)
	+ [Software](#software)
	+ [Talks](#talks)
* [Validation](#validation)
* [Verification](#verification)

---

# General

* ACM SIGPLAN Conference on Certified Programs and Proofs (CPP) - http://dblp.org/db/conf/cpp/
* Black-Box Equivalence Checking Across Compiler Transformations
	+ 2018 PhD thesis; Manjeet Dahiya
	+ https://www.cse.iitd.ac.in/~sbansal/pubs/manjeet_thesis.pdf
* Compiling with Proofs
	+ 1998 Ph.D. Thesis; George C. Necula
	+ https://people.eecs.berkeley.edu/~necula/Papers/thesis.pdf
* How to prove a compiler correct - Daniel Patterson
	+ https://dbp.io/essays/2018-01-16-how-to-prove-a-compiler-correct.html
	+ https://github.com/dbp/howtoproveacompiler
* Operational Refinement for Compiler Correctness
	+ 2012 PhD Dissertation; Robert W. Dockins
	+ ftp://ftp.cs.princeton.edu/reports/2012/936.pdf
* What even is compiler correctness? - https://www.williamjbowman.com/blog/2017/03/24/what-even-is-compiler-correctness/
* Write Your Compiler by Proving It Correct - http://liamoc.net/posts/2015-08-23-verified-compiler.html

---

# Testing

* Dagstuhl Seminar 17502 – Testing and Verification of Compilers
	+ December 2017
	+ http://dagstuhl.de/17502
	+ Materials: http://materials.dagstuhl.de/index.php?semnr=17502
* EMI-based Compiler Testing - http://web.cs.ucdavis.edu/~su/emi-project/

## Articles

* A Systematic Impact Study for Fuzzer-Found Compiler Bugs
	+ 2019 arXiv
	+ Michaël Marcozzi, Qiyi Tang, Alastair Donaldson, Cristian Cadar
	+ https://arxiv.org/abs/1902.09334
	+ https://sites.google.com/view/michaelmarcozzi/compiler-bugs
* An empirical comparison of compiler testing techniques
	+ International Conference on Software Engineering (ICSE 2016)
	+ Junjie Chen, Wenxiang Hu, Dan Hao, Yingfei Xiong, Hongyu Zhang, Lu Zhang, Bing Xie
	+ http://sei.pku.edu.cn/~xiongyf04/papers/ICSE16.pdf
	+ http://emponcc.github.io/
	+ https://github.com/emponcc/emponcc.github.io/blob/master/CompilerTestingComparison.md
	+ https://dl.acm.org/citation.cfm?id=2884878
* Automatic Test Case Reduction for OpenCL - https://dl.acm.org/citation.cfm?id=2909439
	+ paper: https://spiral.imperial.ac.uk/handle/10044/1/39576
	+ slides: http://www.iwocl.org/wp-content/uploads/iwocl-2016-automatic-test-case-reduction.pdf
* Automated Testing of Graphics Shader Compilers
	+ https://www.doc.ic.ac.uk/~afd/homepages/papers/pdfs/2017/OOPSLA.pdf
	+ Overview of the GLFuzz transformations - https://medium.com/@afd_icl/overview-of-the-glfuzz-transformations-d530540a5a18
* Automatic Testing of Symbolic Execution Engines via Program Generation and Differential Testing - https://srg.doc.ic.ac.uk/files/papers/symex-engine-tester-ase-17.pdf
* Causal Distance-Metric-Based Assistance for Debugging After Compiler Fuzzing
	+ IEEE International Symposium on Software Reliability Engineering (ISSRE) 2018
	+ Josie Holmes and Alex Groce
	+ https://agroce.github.io/issre18.pdf
* Checking Correctness of Code Generator Architecture Specifications 
	+ Code Generation and Optimization (CGO) 2015
	+ N. Hasabnis, R. Qiao, R. Sekar 
	+ http://www3.cs.stonybrook.edu/~nhasabni/papers/cgo15.pdf
	+ http://www3.cs.stonybrook.edu/~nhasabni/papers/cgo15_talk.pdf
* Compiler fuzzing, part 1
	+ http://www.vegardno.net/2018/06/compiler-fuzzing.html
* Compiler Fuzzing through Deep Learning
	+ Chris Cummins, Pavlos Petoumenos, Hugh Leather and Alastair Murray
	+ International Symposium on Software Testing and Analysis (ISSTA) 2018
	+ http://homepages.inf.ed.ac.uk/hleather/publications/2018_deepfuzzing_issta.pdf
	+ https://chriscummins.cc/deepsmith
* Compiler Testing via a Theory of Sound Optimisations in the C11/C++11 Memory Model
	+ Programming Language Design and Implementation (PLDI) 2013
	+ Robin Morisset, Pankaj Pawan, Francesco Zappa Nardelli
	+ https://www.di.ens.fr/~zappa/readings/pldi13.pdf
* Coverage Prediction for Accelerating Compiler Testing
	+ IEEE Transactions on Software Engineering (2019)
	+ Junjie Chen, Guancheng Wang, Dan Hao, Yingfei Xiong, Hongyu Zhang, Lu Zhang, Bing Xie
	+ https://ieeexplore.ieee.org/abstract/document/8588375
* DATm: Diderot's Automated Testing Model.
	+ 39th International Conference on Software Engineering ICSE (12th International Workshop on Automation of Software Test AST) 2017
	+ C. Chiw, G. Kindlmann, J. Reppy
	+ https://www.researchgate.net/publication/317836930_DATm_Diderot%27s_Automated_Testing_Model
	+ https://www.dropbox.com/s/5twsrp12vg4or7t/datm_talk.key?dl=0
* DeepFuzz: Automatic Generation of Syntax Valid C Programs for Fuzz Testing
	+ AAAI Conference on Artificial Intelligence (AAAI) 2019
	+ Xiao Liu, Xiaoting Li, Rupesh Prajapati, Dinghao Wu
	+ https://faculty.ist.psu.edu/wu/papers/DeepFuzz.pdf
	+ https://github.com/s3team/DeepFuzz
* Detecting Arithmetic Optimization Opportunities for C Compilers by Randomly Generated Equivalent Programs
	+ IPSJ Transactions on System LSI Design Methodology, vol. 9, 2016; A. Hashimoto and N. Ishiura
	+ <https://www.jstage.jst.go.jp/article/ipsjtsldm/9/0/9_21/_article>
* Detecting Missed Arithmetic Optimization in C Compilers by Differential Random Testing - http://ist.ksc.kwansei.ac.jp/~ishiura/publications/C2016-10a.pdf
* Differential Testing for Software - http://www.cs.dartmouth.edu/~mckeeman/references/DifferentialTestingForSoftware.pdf
* Effect-Driven QuickChecking of Compilers
	+ ICFP 2017
	+ Jan Midtgaard, Mathias Nygaard Justesen, Patrick Kasting, Flemming Nielson, Hanne Riis Nielson
	+ paper: http://janmidtgaard.dk/papers/Midtgaard-al%3AICFP17-full.pdf
	+ implementation: https://github.com/jmid/efftester
	+ talk
		- http://podcasts.ox.ac.uk/effect-driven-quickchecking-compilers
		- https://www.youtube.com/watch?v=_KrZzaShDew&list=PLnqUlCo055hW7kU-SBQEhC_87etA5Gqlq&index=15
* Evaluating the Effects of Compiler Optimizations on Mutation Testing at the Compiler IR Level - ISSRE’16
	+ http://mir.cs.illinois.edu/farah/presentations/issre16_presentation.pdf
	+ http://mir.cs.illinois.edu/marinov/publications/HaririETAL16CompilerIRMutation.pdf
	+ https://www.researchgate.net/publication/311529837_Evaluating_the_Effects_of_Compiler_Optimizations_on_Mutation_Testing_at_the_Compiler_IR_Level
* Finding and Analyzing Compiler Warning Defects - http://ieeexplore.ieee.org/document/7886904/
* Finding Missed Compiler Optimizations by Differential Testing
	+ Compiler Construction (CC) 2018
	+ Gergö Barany
	+ https://github.com/gergo-/missed-optimizations/raw/master/missed_optimizations_preprint.pdf
	+ Missed optimizations in C compilers: https://github.com/gergo-/missed-optimizations/
	+ https://hal.inria.fr/hal-01682683
* Finding and Understanding Bugs in C Compilers
	+ http://www.cs.utah.edu/~regehr/papers/pldi11-preprint.pdf
	+ https://www.flux.utah.edu/download?uid=114
	+ https://blog.regehr.org/archives/492
	+ http://lambda-the-ultimate.org/node/4241
* Fuzzing with Grammars - Generating Software Tests - https://www.fuzzingbook.org/html/Grammars.html
* Fuzzing the .NET JIT Compiler
	+ http://mattwarren.org/2018/08/28/Fuzzing-the-.NET-JIT-Compiler/
	+ Fuzzlyn: Fuzzer for the .NET toolchains
		- https://github.com/jakobbotsch/Fuzzlyn
* Improving the Utility of Compiler Fuzzers
	+ 2014 Ph.D. Dissertation; Yang Chen
	+ http://www.cs.utah.edu/~chenyang/papers/thesis_draft.pdf
	+ https://search.proquest.com/openview/4799de27b7f7d50c7d4f1d2335316065/1?pq-origsite=gscholar&cbl=18750&diss=y
* Learning to Accelerate Compiler Testing
	+ International Conference on Software Engineering (ICSE), Doctoral Symposium, 2018
	+ [Junjie Chen](https://sites.google.com/site/junjiechen08/)
	+ https://www.icse2018.org/event/icse-2018-doctoral-symposium-learning-to-accelerate-compiler-testing
	+ Slides (2017): http://materials.dagstuhl.de/files/17/17502/17502.JunjieChen.Slides.pdf
* Learning to Prioritize Test Programs for Compiler Testing
	+ International Conference on Software Engineering (ICSE 2017)
	+ Junjie Chen, Yanwei Bai, Dan Hao, Yingfei Xiong, Hongyu Zhang, Bing Xie
	+ http://sei.pku.edu.cn/~xiongyf04/papers/ICSE17b.pdf
* Nautilus: Fishing for Deep Bugs with Grammars
	+ Network and Distributed System Security Symposium (NDSS) 2019
	+ Cornelius Aschermann, Tommaso Frassetto, Thorsten Holz, Patrick Jauernig, Ahmad-Reza Sadeghi, Daniel Teuchert
	+ https://www.syssec.ruhr-uni-bochum.de/research/publications/nautilus/
	+ https://github.com/RUB-SysSec/nautilus
	+ testing applications: ChakraCore (the JavaScript engine of Microsoft Edge), PHP, mruby, and Lua
* RandIR: Differential Testing for Embedded Compilers - https://www.cs.purdue.edu/homes/rompf/papers/ofenbeck-scala16.pdf
* Reinforcing Random Testing of Arithmetic Optimization of C Compilers by Scaling up Size and Number of Expressions, IPSJ Transactions on System LSI Design Methodology, vol. 7, 2014. E. Nagai, A. Hashimoto, and N. Ishiura. <https://www.jstage.jst.go.jp/article/ipsjtsldm/7/0/7_91/_article>
* Scaling up Size and Number of Expressions in Random Testing of Arithmetic Optimization of C Compilers
	+ SASIMI 2013
	+ http://ist.ksc.kwansei.ac.jp/~ishiura/publications/C2013-10.pdf
* Some Goals for High-impact Verified Compiler Research - https://blog.regehr.org/archives/1565
* System Under Test: LLVM - https://systemundertest.org/llvm/
* Taming compiler fuzzers
	+ PLDI 2013
	+ Y. Chen, A. Groce, C. Zhang, W.-K. Wong, X. Fern, E. Eide, J. Regehr
	+ https://www.cs.utah.edu/~regehr/papers/pldi13.pdf
	+ Fuzzers Need Taming - https://blog.regehr.org/archives/925
* Test-Case Reduction for C Compiler Bugs - https://www.cs.utah.edu/~regehr/papers/pldi12-preprint.pdf
* Testing LLVM - http://blog.regehr.org/archives/1450
* The Correctness-Security Gap in Compiler Optimization - LangSec 2015, IEEE SPW
	+ paper: https://research.google.com/pubs/pub43856.html
	+ slides: https://nebelwelt.net/publications/files/15LangSec-presentation.pdf
	+ talk: https://www.youtube.com/watch?v=g6LCtHz_MDc&list=PL0pRF4xvoD0kuECJuowraVIIHlT3pN1Cm&index=3
* The problem with differential testing is that at least one of the compilers must get it right - http://blog.frama-c.com/index.php?post/2013/09/25/The-problem-with-differential-testing-is-that-at-least-one-of-the-compilers-must-get-it-right

## Software

* CF3: Test suite for arithmetic optimization of C compilers
	+ https://ist.ksc.kwansei.ac.jp/~ishiura/pub/CF3/
	+ https://github.com/ishiura-compiler/CF3
* Csmith, a random generator of C programs
	+ https://github.com/csmith-project/csmith
	+ https://embed.cs.utah.edu/csmith/
	+ Csmith testing - http://blog.frama-c.com/index.php?pages/Csmith-testing
* C-Reduce, a C program reducer
	+ https://embed.cs.utah.edu/creduce/
	+ https://github.com/csmith-project/creduce
* Fuzzing LLVM libraries and tools - https://llvm.org/docs/FuzzingLLVM.html
	+ Adventures in Fuzzing Instruction Selection
		- 2017 EuroLLVM Developers’ Meeting; Justin Bogner
		- http://llvm.org/devmtg/2017-03/assets/slides/adventures_in_fuzzing_instruction_selection.pdf
		- https://www.youtube.com/watch?v=UBbQ_s6hNgg
	+ Structure-aware fuzzing for Clang and LLVM with libprotobuf-mutator
		- 2017 LLVM Developers’ Meeting; Kostya Serebryany, Vitaly Buka, Matt Morehouse
		- https://www.youtube.com/watch?v=U60hC16HEDY
* gcc-for-llvm-testing: A modified GCC test suite suitable for testing non-GCC compilers
	+ https://github.com/embecosm/gcc-for-llvm-testing
	+ Using the GCC regression test suite for LLVM (and other compilers)
		- GNU Tools Cauldron 2018; Simon Cook
		- https://speakerdeck.com/simonpcook/using-the-gcc-regression-test-suite-for-llvm-and-other-compilers
	+ Repurposing GCC Regression for LLVM Based Tool Chains
		- 2018 LLVM Developers’ Meeting; Jeremy Bennett
		- https://www.youtube.com/watch?v=GV4PoWu0UZ0
* GraphicsFuzz: A testing framework for automatically finding and simplifying bugs in graphics shader compilers.
	+ https://github.com/google/graphicsfuzz
* kscope
	+ a library which recursively generates randomized code while keeping it 100% equivalent to the original one
	+ http://ithare.com/c17-compiler-bug-hunt-very-first-results-12-bugs-reported-3-already-fixed/
	+ https://github.com/ITHare/kscope
* ldrgen: Liveness-driven random C code generator - https://github.com/gergo-/ldrgen
* llvm-mutate – mutate LLVM IR - http://eschulte.github.io/llvm-mutate/
* opt-fuzz: a simple implementation of bounded exhaustive testing for LLVM programs
	+ https://github.com/regehr/opt-fuzz
* Orange3
	+ a tool to test C compilers with randomly generated programs; mainly targets arithmetic optimization such as constant folding.
	+ https://ist.ksc.kwansei.ac.jp/~ishiura/pub/orange3/
	+ https://github.com/ishiura-compiler/Orange3
* Orange4
	+ a tool to test C compilers by randomly generated programs; based on equivalent transformations on C programs and can generate wider class of C test programs than Orange3.
	+ https://ist.ksc.kwansei.ac.jp/~ishiura/pub/orange4/
	+ https://github.com/ishiura-compiler/Orange4
* OutputCheck: A tool for checking tool output inspired by LLVM's FileCheck
	+ https://github.com/stp/OutputCheck/
* prog-fuzz: Compiler/source code fuzzing tool using AFL instrumentation
	+ https://github.com/vegard/prog-fuzz
* Quest: A tool for testing C compilers - https://github.com/lindig/quest
* shader-compiler-bugs: A collection of shader compiler bugs - https://github.com/mc-imperial/shader-compiler-bugs
* yarpgen: Yet Another Random Program Generator
	+ a random C/C++ program generator, which produces correct runnable C/C++ programs
	+ specifically designed to trigger compiler optimization bugs and is intended for compiler testing
	+ https://github.com/intel/yarpgen

## Talks

* Adventures in Fuzzing Instruction Selection
	+ EuroLLVM 2017 - Justin Bogner
	+ https://www.youtube.com/watch?v=UBbQ_s6hNgg
	+ http://llvm.org/devmtg/2017-03//assets/slides/adventures_in_fuzzing_instruction_selection.pdf
* Compiler testing: GCC Vs LLVM
	+ https://docs.google.com/presentation/d/1RIfDj1r0VQ-m919zy7fCFrGS76UysSUOJbjrpYbNLgY/
	+ Linaro Connect Vancouver 2018 (YVR18) TCWG07; Thomas Preud’homme
	+ FileCheck numeric expressions: features and implementation - https://connect.linaro.org/resources/yvr18/yvr18-tcw07/
* Coverage-Directed Differential Testing of JVM Implementations - Yuting Chen, PLDI 2016
	+ https://www.youtube.com/watch?v=2Reaqfp4v-g
	+ http://cse.sjtu.edu.cn/~zhao/pub/pdf/pldi2016.pdf
* Exposing Difficult Compiler Bugs With Random Testing
	+ https://gcc.gnu.org/wiki/summit2010?action=AttachFile&do=get&target=regehr_gcc_summit_2010.pdf
* Finding Missed Optimizations in LLVM (and other compilers)
	+ EuroLLVM 2018 - Gergö Barany
	+ https://www.youtube.com/watch?v=V6ug3e3jC54
	+ http://llvm.org/devmtg/2018-04/slides/Barany-Finding%20Missed%20Optimizations%20in%20LLVM.pdf
	+ https://github.com/gergo-/missed-optimizations/
* Testing Language Implementations - Alastair Donaldson - Programming Language Implementation Summer School (PLISS) 2017
	+ https://www.youtube.com/watch?v=ZJUk8_k1HbY

---

# Validation

Validation: Including translation validation, equivalence checking.

* Black-box equivalence checking across compiler optimizations - APLAS ’17 (2017) - http://www.cse.iitd.ac.in/~sbansal/pubs/aplas17.pdf
* Modeling undefined behaviour semantics for checking equivalence across compiler optimizations - Manjeet Dahiya, Sorav Bansal. HVC 2017
	+ http://www.cse.iitd.ernet.in/~sbansal/pubs/hvc17.pdf
	+ http://www.cse.iitd.ac.in/~dahiya/hvc17.pdf
* Evaluating value-graph translation validation for LLVM
	+ Programming and Language Design Implementation (PLDI) 2011
	+ Tristan, Jean-Baptiste, Paul Govereau, Greg Morrisett
	+ https://dl.acm.org/citation.cfm?id=1993498.1993533
* Formally Verified Compilation of Low-Level C code
	+ 2016 PhD Dissertation; Pierre Wilke
	+ https://tel.archives-ouvertes.fr/tel-01483676
* Proving the correctness of heuristically optimized code
	+ Hanan Samet, CACM 1978
	+ http://www.cs.umd.edu/~hjs/pubs/compilers/proving-correctness.pdf
* Translation validation
	+ TACAS 1998
	+ Amir Pnueli, Michael Siegel, Eli Singerman
	+ https://dl.acm.org/citation.cfm?id=349314
	+ "We present the notion of _translation validation_ as a new approach to the verification of translators (compilers, code generators). Rather than proving in advance that the compiler always produces a target code which correctly implements the source code (compiler verification), each individual translation (i.e. a run of the compiler) is followed by a validation phase which verifies that the target code produced on this run correctly implements the submitted source program."
* Translation Validation: Automatically Proving the Correctness of Translations Involving Optimized Code
	+ [Hanan Samet](http://www.cs.umd.edu/~hjs/)
	+ translation validation - http://www.cs.umd.edu/~hjs/hjscat.html#sectiontranslationvalidation
	+ compiler testing - http://www.cs.umd.edu/~hjs/hjscat.html#sectioncompilertesting
	+ http://www.cs.umd.edu/~hjs/pubs/compilers/CS-TR-75-498.pdf
	+ http://www.cs.umd.edu/~hjs/slides/translation-validation-slides.pdf
* Translation Validation: From DC+ to C*
	+ FM-Trends 1998
	+ Amir Pnueli, Ofer Shtrichman, Michael Siegel
	+ https://dl.acm.org/citation.cfm?id=729871
	+ "Translation validation is an alternative to the verification of translators (compilers, code generators). Rather than proving in advance that the compiler always produces a target code which correctly implements the source code (compiler verification), each individual translation (i.e. a run of the compiler) is followed by a validation phase which verifies that the target code produced on this run correctly implements the submitted source program."
* Translation validation for an optimizing compiler
	+ PLDI 2000
	+ George C. Necula
	+ https://dl.acm.org/citation.cfm?id=349314
* Translation Validation for Verified, Efficient and Timely Operating Systems
	+ 2017 PhD Dissertation; Thomas Sewell
	+ http://handle.unsw.edu.au/1959.4/58861
	+ https://ts.data61.csiro.au/publications/papers/Sewell:phd
	+ https://ts.data61.csiro.au/projects/TS/compiler-correctness.pml
* Translation Validation of Bounded Exhaustive Test Cases - Nuno Lopes, John Regehr - https://blog.regehr.org/archives/1510
* Translation Validation with Alive - https://github.com/nunoplopes/alive/tree/newsema/tv
* Validating Optimizations of Concurrent C/C++ Programs
	+ CGO 2016
	+ Soham Chakraborty, Viktor Vafeiadis
	+ https://plv.mpi-sws.org/validc/paper.pdf

---

# Verification

* A Higher-Order Abstract Syntax Approach to the Verified Compilation of Functional Programs
	+ 2016 PhD thesis; Yuting Wang 
	+ https://arxiv.org/abs/1702.03363
	+ http://www.cs.yale.edu/homes/wang-yuting/files/phd_thesis.pdf
* A Verified Compiler for a Linear Function/Imperative Intermediate Language
	+ 2018 PhD Thesis; Sigurd Schneider
	+ https://www.ps.uni-saarland.de/Publications/documents/Schneider_2018_PhDThesis.pdf
	+ LVC - Linear Verified Compiler: https://www.ps.uni-saarland.de/~sdschn/LVC.html
* ALIVe: Automatic LLVM InstCombine Verifier
	+ https://github.com/nunoplopes/alive
	+ online: http://rise4fun.com/Alive
	+ blog post: http://blog.regehr.org/archives/1170
	+ slides: http://llvm.org/devmtg/2014-10/Slides/Menendez-Alive.pdf
	+ Alive-FP: Automated Verification of Floating Point Based Peephole Optimizations in LLVM - https://www.cs.rutgers.edu/research/technical_reports/report.php?series_id=1&report_id=723
	+ Alive-Loops: https://github.com/rutgers-apl/alive-loops
		- "Termination checking for LLVM peephole optimizations" (ICSE 2016); David Menendez, Santosh Nagarakatte
		- https://www.cs.rutgers.edu/~sn349/papers/icse2016-alive-loops.pdf
	+ Alive-NJ - https://github.com/rutgers-apl/alive-nj
	+ LifeJacket: Verifying precise floating-point optimizations in LLVM - http://export.arxiv.org/abs/1603.09290 - https://github.com/4tXJ7f/alive
	+ Practical Formal Techniques and Tools for Developing LLVM's Peephole Optimizations
		- 2018 PhD Thesis; David Menendez
		- https://www.cs.rutgers.edu/~santosh.nagarakatte/david-menendez-phd-thesis.pdf
	+ Precondition Inference for Peephole Optimizations in LLVM
		- http://export.arxiv.org/abs/1611.05980
		- https://www.cs.rutgers.edu/~santosh.nagarakatte/papers/pldi2017-alive-infer.pdf
		- PLDI 2017 talk, David Menendez - https://pldi17.sigplan.org/event/pldi-2017-papers-precondition-inference-for-peephole-optimizations-in-llvm
	+ Provably Correct Peephole Optimizations with Alive - https://www.cs.utah.edu/~regehr/papers/pldi15.pdf
* An Abstract Stack Based Approach to Verified Compositional Compilation to Machine Code
	+ POPL 2019
	+ Yuting Wang, Pierre Wilke, Zhong Shao
	+ https://popl19.sigplan.org/event/popl-2019-research-papers-an-abstract-stack-based-approach-to-verified-compositional-compilation-to-machine-code
* CakeML: A Verified Implementation of ML
	+ https://cakeml.org/
	+ https://github.com/CakeML/cakeml
	+ Verified Compilation of CakeML to Multiple Machine-Code Targets
		- Certified Programs and Proofs (CPP) 2017
		- Anthony Fox, Magnus O. Myreen, Yong Kiam Tan, Ramana Kumar.
		- http://www.cl.cam.ac.uk/~mom22/cpp17.pdf
		- http://www.cl.cam.ac.uk/~mom22/publications.html
	+ The Verified CakeML Compiler Backend
		- JFP 2019
		- Yong Kiam Tan, Magnus O. Myreen, Ramana Kumar, Anthony Fox, Scott Owens, Michael Norrish
		- https://www.cs.cmu.edu/~yongkiat/files/cakeml-jfp.pdf
* CompCert: formally-verified C compiler
	+ http://compcert.inria.fr/
	+ https://github.com/AbsInt/CompCert 
	+ The formal verification of compilers - Xavier Leroy - DeepSpec Summer School 2017
		- https://deepspec.org/event/dsss17/lecture_leroy.html
		- http://gallium.inria.fr/~xleroy/courses/DSSS-2017/
	+ Closing the Gap – The Formally Verified Optimizing Compiler CompCert
		- SSS'17: Safety-critical Systems Symposium 2017
		- https://hal.inria.fr/hal-01399482/
	+ Compositional CompCert
		- POPL 2015
		- Stewart, G., Beringer, L., Cuellar, S., Appel, A.W.
		- https://github.com/PrincetonUniversity/compcomp
	+ Lightweight Verification of Separate Compilation
		- POPL 2016
		- Jeehoon Kang, Yoonseung Kim, Chung-Kil Hur, Derek Dreyer, Viktor Vafeiadis
		- https://sf.snu.ac.kr/sepcompcert/
	+ Verified Peephole Optimizations for CompCert
		- PLDI 2016
		- Eric Mullen, Daryl Zuniga, Zachary Tatlock, Dan Grossman
		- http://peek.uwplse.org/
		- https://conf.researchr.org/event/pldi-2016/pldi-2016-papers-verified-peephole-optimizations-for-compcert-
		- Peek: a verified peephole optimizer for CompCert - https://github.com/uwplse/peek
* Compilation Using Correct-by-Construction Program Synthesis
	+ Clément Pit-Claudel; 2016 Master's Thesis at MIT; William A. Martin Memorial Thesis Award for Outstanding Thesis in CS
	+ http://pit-claudel.fr/clement/MSc/
	+ https://dspace.mit.edu/bitstream/handle/1721.1/107293/973557793-MIT.pdf?sequence=1
	+ http://pit-claudel.fr/clement/MSc/FiatToFacade_Pit-Claudel_2016.pdf
* Compositional Verification of Compiler Optimisations on Relaxed Memory
	+ ESOP 2018
	+ Mike Dodds, Mark Batty, Alexey Gotsman
	+ https://arxiv.org/abs/1802.05918
* Crellvm: Verified Credible Compilation for LLVM
	+ Programming Languages Design and Implementation (PLDI) 2018
	+ Jeehoon Kang, Yoonseung Kim, Youngju Song, Juneyoung Lee, Sanghoon Park, Mark Dongyeon Shin, Yonghyun Kim, Sungkeun Cho, Joonwon Choi,Chung-Kil Hur, Kwangkeun Yi
	+ a verified credible compilation (or equivalently, verified translation validation) framework for LLVM
	+ http://sf.snu.ac.kr/crellvm/
	+ http://sf.snu.ac.kr/gil.hur/publications/crellvm.pdf
	+ http://sf.snu.ac.kr/gil.hur/publications/crellvm.zip
	+ https://github.com/snu-sf/crellvm-tests-parallel
* Pilsner: A Compositionally Verified Compiler for a Higher-Order Imperative Language
	+ International Conference on Functional Programming (ICFP) 2015
	+ Georg Neis, Chung-Kil Hur, Jan-Oliver Kaiser, Craig McLaughlin, Derek Dreyer, Viktor Vafeiadis
	+ https://people.mpi-sws.org/~dreyer/papers/pilsner/paper.pdf
	+ http://plv.mpi-sws.org/pils/
* Pushing the Limits of Compiler Verification
	+ 2018 PhD Thesis; Eric Mullen
	+ https://homes.cs.washington.edu/~djg/theses/mullen_thesis.pdf
	+ Œuf: Verified Coq Extraction in Coq - https://github.com/uwplse/oeuf
	+ Peek: Verified Peephole Optimizations for CompCert - https://github.com/uwplse/peek
* Self-compilation and self-verification - Ramana Kumar
	+ http://www.sigplan.org/Awards/Dissertation/2017_kumar.pdf
	+ https://cakeml.org/
* Vale (Verified Assembly Language for Everest)
	+ https://github.com/project-everest/vale
	+ https://www.microsoft.com/en-us/research/publication/vale-verifying-high-performance-cryptographic-assembly-code/
	+ https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/bond
* Vellvm: Verifying the LLVM
	+ http://www.cis.upenn.edu/~stevez/vellvm/
	+ https://github.com/vellvm
	+ DeepSpec Summer School 2017; Steve Zdancewic - https://deepspec.org/event/dsss17/lecture_zdancewic.html
	+ Galois, Inc. Tech Talk 2018; Steve Zdancewic
		- https://galois.com/blog/2018/07/vellvm-verifying-the-llvm/
		- https://www.youtube.com/watch?v=qGpRKkP8gec
	+ Strange Loop 2018; Steve Zdancewic
		- https://www.youtube.com/watch?v=q6gSC3OxB_8
		- https://thestrangeloop.com/2018/vellvm---verifying-the-llvm.html
* Verified Compilers for a Multi-Language World
	+ Summit on Advances in Programming Languages (SNAPL) 2015
	+ Amal Ahmed
	+ http://www.ccs.neu.edu/home/amal/papers/verifcomp.pdf
