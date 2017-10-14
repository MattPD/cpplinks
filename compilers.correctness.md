# [C++ links](README.md): compilers - correctness

Note: see also [compilers](compilers.md)

* ACM SIGPLAN Conference on Certified Programs and Proofs (CPP) - http://dblp.org/db/conf/cpp/
* What even is compiler correctness? - https://www.williamjbowman.com/blog/2017/03/24/what-even-is-compiler-correctness/

# Testing

* EMI-based Compiler Testing - http://web.cs.ucdavis.edu/~su/emi-project/

## Articles

* An empirical comparison of compiler testing techniques - https://dl.acm.org/citation.cfm?id=2884878
* Automatic Test Case Reduction for OpenCL - https://dl.acm.org/citation.cfm?id=2909439
	+ paper: https://spiral.imperial.ac.uk/handle/10044/1/39576
	+ slides: http://www.iwocl.org/wp-content/uploads/iwocl-2016-automatic-test-case-reduction.pdf
* Automated Testing of Graphics Shader Compilers
	+ https://www.doc.ic.ac.uk/~afd/homepages/papers/pdfs/2017/OOPSLA.pdf
	+ Overview of the GLFuzz transformations - https://medium.com/@afd_icl/overview-of-the-glfuzz-transformations-d530540a5a18
* Automatic Testing of Symbolic Execution Engines via Program Generation and Differential Testing - https://srg.doc.ic.ac.uk/files/papers/symex-engine-tester-ase-17.pdf
* Detecting Missed Arithmetic Optimization in C Compilers by Differential Random Testing - http://ist.ksc.kwansei.ac.jp/~ishiura/publications/C2016-10a.pdf
* Differential Testing for Software - http://www.cs.dartmouth.edu/~mckeeman/references/DifferentialTestingForSoftware.pdf
* Evaluating the Effects of Compiler Optimizations on Mutation Testing at the Compiler IR Level - ISSRE’16 – Ottawa, Canada
	+ http://mir.cs.illinois.edu/farah/presentations/issre16_presentation.pdf
	+ http://mir.cs.illinois.edu/marinov/publications/HaririETAL16CompilerIRMutation.pdf
	+ https://www.researchgate.net/publication/311529837_Evaluating_the_Effects_of_Compiler_Optimizations_on_Mutation_Testing_at_the_Compiler_IR_Level
* Finding and Analyzing Compiler Warning Defects - http://ieeexplore.ieee.org/document/7886904/
* Finding Missed Compiler Optimizations by Differential Testing
	+ https://github.com/gergo-/missed-optimizations/raw/master/missed_optimizations_preprint.pdf
	+ Missed optimizations in C compilers: https://github.com/gergo-/missed-optimizations/
* Finding and Understanding Bugs in C Compilers
	+ http://www.cs.utah.edu/~regehr/papers/pldi11-preprint.pdf
	+ https://www.flux.utah.edu/download?uid=114
	+ https://blog.regehr.org/archives/492
	+ http://lambda-the-ultimate.org/node/4241
* RandIR: Differential Testing for Embedded Compilers - https://www.cs.purdue.edu/homes/rompf/papers/ofenbeck-scala16.pdf
* Test-Case Reduction for C Compiler Bugs - https://www.cs.utah.edu/~regehr/papers/pldi12-preprint.pdf
* The problem with differential testing is that at least one of the compilers must get it right - http://blog.frama-c.com/index.php?post/2013/09/25/The-problem-with-differential-testing-is-that-at-least-one-of-the-compilers-must-get-it-right

## Software

* Csmith, a random generator of C programs
	+ https://github.com/csmith-project/csmith
	+ https://embed.cs.utah.edu/csmith/
* C-Reduce, a C program reducer
	+ https://embed.cs.utah.edu/creduce/
	+ https://github.com/csmith-project/creduce
* llvm-mutate – mutate LLVM IR - http://eschulte.github.io/llvm-mutate/
* shader-compiler-bugs: A collection of shader compiler bugs - https://github.com/mc-imperial/shader-compiler-bugs

## Talks

* Coverage-Directed Differential Testing of JVM Implementations - Yuting Chen, PLDI 2016
	+ https://www.youtube.com/watch?v=2Reaqfp4v-g
	+ http://cse.sjtu.edu.cn/~zhao/pub/pdf/pldi2016.pdf
* Exposing Difficult Compiler Bugs With Random Testing
	+ https://gcc.gnu.org/wiki/summit2010?action=AttachFile&do=get&target=regehr_gcc_summit_2010.pdf
* Testing Language Implementations - Alastair Donaldson - Programming Language Implementation Summer School (PLISS) 2017
	+ https://www.youtube.com/watch?v=ZJUk8_k1HbY

# Validation

Validation: Including translation validation, equivalence checking.

* Black-box equivalence checking across compiler optimizations - APLAS ’17 (2017) - http://www.cse.iitd.ac.in/~sbansal/pubs/aplas17.pdf
* Modeling undefined behaviour semantics for checking equivalence across compiler optimizations - Manjeet Dahiya, Sorav Bansal. HVC 2017
	+ http://www.cse.iitd.ernet.in/~sbansal/pubs/hvc17.pdf
	+ http://www.cse.iitd.ac.in/~dahiya/hvc17.pdf

# Verification

* ALIVe: Automatic LLVM InstCombine Verifier
	+ https://github.com/nunoplopes/alive
	+ online: http://rise4fun.com/Alive
	+ blog post: http://blog.regehr.org/archives/1170
	+ slides: http://llvm.org/devmtg/2014-10/Slides/Menendez-Alive.pdf
	+ Alive-FP: Automated Verification of Floating Point Based Peephole Optimizations in LLVM - https://www.cs.rutgers.edu/research/technical_reports/report.php?series_id=1&report_id=723
	+ Alive-NJ - https://github.com/rutgers-apl/alive-nj
	+ LifeJacket: Verifying precise floating-point optimizations in LLVM - http://export.arxiv.org/abs/1603.09290 - https://github.com/4tXJ7f/alive
	+ Precondition Inference for Peephole Optimizations in LLVM
		- http://export.arxiv.org/abs/1611.05980
		- https://www.cs.rutgers.edu/~santosh.nagarakatte/papers/pldi2017-alive-infer.pdf
		- PLDI 2017 talk, David Menendez - https://pldi17.sigplan.org/event/pldi-2017-papers-precondition-inference-for-peephole-optimizations-in-llvm
	+ Provably Correct Peephole Optimizations with Alive - https://www.cs.utah.edu/~regehr/papers/pldi15.pdf
* CakeML: A Verified Implementation of ML
	+ https://cakeml.org/
	+ https://github.com/CakeML/cakeml
	+ Verified Compilation of CakeML to Multiple Machine-Code Targets. In Certified Programs and Proofs (CPP), 2017.
		- Anthony Fox, Magnus O. Myreen, Yong Kiam Tan, Ramana Kumar.
		- http://www.cl.cam.ac.uk/~mom22/cpp17.pdf
		- http://www.cl.cam.ac.uk/~mom22/publications.html
* CompCert: formally-verified C compiler
	+ http://compcert.inria.fr/
	+ https://github.com/AbsInt/CompCert 
	+ The formal verification of compilers - Xavier Leroy - DeepSpec Summer School 2017
		- https://deepspec.org/event/dsss17/lecture_leroy.html
		- http://gallium.inria.fr/~xleroy/courses/DSSS-2017/
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
	+ Steve Zdancewic - DeepSpec Summer School 2017 - https://deepspec.org/event/dsss17/lecture_zdancewic.html
