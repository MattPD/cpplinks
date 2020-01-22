# [C++ links](README.md): Building, Build Systems, and Build Performance Optimization

# Contents

- [Readings](#readings):
	- [Caching](#caching)
	- [Correctness](#correctness)
	- [Dependencies](#dependencies)
	- [Distributed](#distributed)
	- [Incremental Building](#incremental-building)
	- [Reproducibility](#reproducibility)
- [Build Performance](#build-performance):
	- [Build Performance Readings](#build-performance-readings)
	- [Build Performance Software](#build-performance-software)
		- [Benchmarking and Profiling](#benchmarking-and-profiling)
		- [Caching](#caching-1)
		- [Dependencies Analysis and Optimization](#dependencies-analysis-and-optimization)
	- [Build Performance Talks](#build-performance-talks)
- [Software](#software):
	- [Autotools](#autotools)
	- [Bazel](#bazel)
	- [Boost.Build](#boost-build)
	- [build2](#build2)
	- [CMake](#cmake):
		- [CMake Examples](#cmake-examples)
		- [CMake Readings](#cmake-readings)
		- [CMake Software](#cmake-software)
		- [CMake Talks](#cmake-talks)
	- [Gradle](#gradle)
	- [Make](#make):
		- [GNU Make](#gnu-make)
	- [Meson](#meson)
	- [Ninja](#ninja)
	- [Tundra](#tundra)
	- [Tup](#tup)
	- [Visual Studio](#visual-studio):
		- [MSBuild](#msbuild)
	- [Xcode](#Xcode)
	- [xmake](#xmake)
- [Talks](#talks): [2019](#2019), [2018](#2018), [2017](#2017)

---

# Readings

- Build Systems à la Carte
	- Microsoft Research 2018
	- Andrey Mokhov, Neil Mitchell, Simon Peyton Jones
	- https://www.microsoft.com/en-us/research/publication/build-systems-la-carte/
	- https://github.com/snowleopard/build
	- https://blogs.ncl.ac.uk/andreymokhov/the-task-abstraction/
	- https://blogs.ncl.ac.uk/andreymokhov/build-systems-a-la-carte/
	- https://icfp18.sigplan.org/event/icfp-2018-papers-build-systems-a-la-carte
	- https://www.youtube.com/watch?v=BQVT6wiwCxM
- Build System Rules and Algorithms
	- Mike Shal (2009)
	- http://gittup.org/tup/build_system_rules_and_algorithms.pdf
	- Build System Partial Updates - http://gittup.org/blog/2014/09/11-build-system-partial-updates/
- Clobber Builds - Mike Shal
	- Part 1 - Missing Dependencies - http://gittup.org/blog/2014/03/6-clobber-builds-part-1---missing-dependencies/
	- Part 2 - Fixing Missing Dependencies - http://gittup.org/blog/2014/05/7-clobber-builds-part-2---fixing-missing-dependencies/
	- Part 3 - Other Clobber Causes - http://gittup.org/blog/2014/06/8-clobber-builds-part-3---other-clobber-causes/
	- Part 4 - Fixing Other Clobber Causes - http://gittup.org/blog/2015/03/13-clobber-builds-part-4---fixing-other-clobber-causes/
- Correct, Efficient, and Tailored: The Future of Build Systems
	- IEEE Software, vol. 35, no. 2, 2018
	- G. Maudoux and K. Mens
	- https://doi.ieeecomputersociety.org/10.1109/MS.2018.111095025
- The C++ Build Process Explained
	- https://github.com/green7ea/cpp-compilation

## Caching

- Caching Function Calls Using Precise Dependencies
	- Programming Language Design and Implementation (PLDI) 2000
	- Allan Heydon, Roy Levin, Yuan Yu
	- http://www.vestasys.org/doc/pubs/pldi-00-04-20.pdf
	- Vesta Configuration Management System - http://www.vestasys.org/#publications
- cHash: Detection of Redundant Compilations via AST Hashing
	- USENIX Annual Technical Conference 2017
	- Christian Dietrich, Valentin Rothberg, Ludwig Füracker, Andreas Ziegler, Daniel Lohmann
	- https://www.usenix.org/conference/atc17/technical-sessions/presentation/dietrich
	- cHash Compiler Plugins and related tools - https://github.com/luhsra/chash

## Correctness

- Detecting Incorrect Build Rules
	- International Conference on Software Engineering (ICSE) 2019
	- Nandor Licker, Andrew Rice
	- https://2019.icse-conferences.org/details/icse-2019-Technical-Papers/82/Detecting-Incorrect-Build-Rules
	- https://www.repository.cam.ac.uk/handle/1810/288468
	- mkcheck: Incremental Build Verification
		- https://github.com/nandor/mkcheck
- Oops, My Tests Broke the Build: An Explorative Analysis of Travis CI with GitHub
	- Mining Software Repositories (MSR) 2017
	- M. Beller, G. Gousios, A. Zaidman
	- http://www.gousios.gr/pub/tests-broke-build-explorative-analysis-travis-ci-github.pdf
	- https://www.slideshare.net/inventitech/oops-my-tests-broke-the-build-an-explorative-analysis-of-travis-ci-with-github
- Programmers’ Build Errors: A Case Study (at Google)
	- International Conference on Software Engineering (ICSE) 2014
	- Hyunmin Seo, Caitlin Sadowski, Sebastian Elbaum, Edward Aftandilian, Robert Bowdidge
	- https://research.google.com/pubs/pub42184.html

## Dependencies

- Automatic Object Linkage, with Include Graphs (Source code sharing without static libraries)
	- 2018; Thomas Young
	- https://upcoder.com/19/automatic-object-linkage-with-include-graphs
- Build Predictor: More Accurate Missed Dependency Prediction in Build Configuration Files
	- Computer Software and Applications Conference (COMPSAC 2014)
	- Bo Zhou, Xia Xin, David Lo, Xinyu Wang
	- http://www.mysmu.edu/faculty/davidlo/papers/compsac14-dependency.pdf
	- https://www.semanticscholar.org/paper/Build-Predictor%3A-More-Accurate-Missed-Dependency-in-Zhou-Xia/a4d4b05c8594fc7358a89f0afffb7e405b65fa0d
- Program Repository
	- LLVM with Program Repository Support
			- https://github.com/SNSystems/llvm-project-prepo
	- Program Repository: What’s the Idea?
		- https://github.com/SNSystems/llvm-project-prepo/wiki
	- Early Overview
		- https://github.com/SNSystems/llvm-project-prepo/wiki/Early-Overview
	- Toy programming demo of a repository for statically compiled programs
		- 2016 US LLVM Developers' Meeting; Paul Bowen-Huggett
		- https://llvm.org/devmtg/2016-11/Slides/Bowen-Hugett-ToyProgrammingDemo.pdf
		- https://youtu.be/-pL94rqyQ6c
	- Targeting a statically compiled program repository with LLVM
		- 2019 EuroLLVM Developers’ Meeting; Phil Camp , Russell Gallop 
		- https://www.youtube.com/watch?v=mlQyEBDnDJE 
		- http://llvm.org/devmtg/2019-04/slides/Lightning-Camp-Program_Repo.pdf
	- LLVM Build Times Using a Program Repository
		- https://www.snsystems.com/technology/tech-blog/llvm-build-times-using-a-program-repository
- mtime comparison considered harmful
	- "tl;dr: Rebuilding a target because its mtime is older than the mtimes of its dependencies, like make does, is very error prone. redo does it better, and so can you."
	- https://apenwarr.ca/log/20181113
- Non-recursive Make Considered Harmful
	- Proceedings of the 9th International Symposium on Haskell, 2016
	- Andrey Mokhov, Neil Mitchell, Simon Peyton Jones, Simon Marlow
	- https://www.microsoft.com/en-us/research/publication/non-recursive-make-considered-harmful/
	- https://simonmar.github.io/bib/shake-2016_abstract.html
- Recursive Make Considered Harmful 
	- Journal of AUUG Inc, 19(1):14–25, 1998
	- Peter Miller
	- http://aegis.sourceforge.net/auug97.pdf
	- http://sites.e-advies.nl/nonrecursive-make.html

## Distributed

- CloudBuild: Microsoft’s Distributed and Caching Build Service
	- International Conference on Software Engineering (ICSE) 2016
	- Hamed Esfahani, Jonas Fietz, Qi Ke, Alexei Kolomiets, Erica Lan, Erik Mavrinac, Wolfram Schulte, Newton Sanches, Srikanth Kandula
	- https://dl.acm.org/citation.cfm?id=2889222
	- https://www.microsoft.com/en-us/research/publication/cloudbuild-microsofts-distributed-and-caching-build-service/
- From Laptop to Lambda: Outsourcing Everyday Jobs to Thousands of Transient Functional Containers
	- 2019 USENIX Annual Technical Conference
	- Sadjad Fouladi, Francisco Romero, Dan Iter, Qian Li, Shuvo Chatterjee, Christos Kozyrakis, Matei Zaharia, Keith Winstein
	- https://www.usenix.org/conference/atc19/presentation/fouladi
	- Outsourcing Everyday Jobs to Thousands of Cloud Functions with gg
		- https://www.usenix.org/system/files/login/articles/login_fall19_02_fouladi.pdf
	- gg: The Stanford Builder
		- https://github.com/stanfordsnr/gg

## Incremental Building

- A Sound and Optimal Incremental Build System with Dynamic Dependencies
	- SPLASH 2015 OOPSLA
	- Sebastian Erdweg, Moritz Lichter, Manuel Weiel
	- https://www.youtube.com/watch?v=QsgLSDMLLTo
	- https://2015.splashcon.org/event/oopsla2015-a-sound-and-optimal-incremental-build-system
- Bringing Incremental Builds to Continuous Integration
	- SaTToSE (Seminar Series on Advanced Techniques & Tools for Software Evolution) 2017
	- Guillaume Maudoux and Kim Mens
	- https://dial.uclouvain.be/pr/boreal/object/boreal:189543
	- http://sattose.wdfiles.com/local--files/2017:schedule/SATToSE_2017_paper_3.pdf
- Scalable Incremental Building with Dynamic Task Dependencies
	- Automated Software Engineering (ASE) 2018
	- Gabriël Konat, Sebastian Erdweg, Eelco Visser
	- https://doi.org/10.1145/3238147.3238196
	- https://eelcovisser.org/post/306/scalable-incremental-building-with-dynamic-task-dependencies
	- https://www.student.informatik.tu-darmstadt.de/~xx00seba/publications/pie-scalable-incremental-build.pdf

## Reproducibility

- An introduction to deterministic builds with C/C++
	- https://blog.conan.io/2019/09/02/Deterministic-builds-with-C-C++.html
- Automated Localization for Unreproducible Builds
	- ICSE 2018
	- Zhilei Ren, He Jiang, Jifeng Xuan, Zijiang Yang
	- https://arxiv.org/abs/1803.06766
	- https://blog.acolyer.org/2018/06/22/automated-localization-for-unreproducible-builds/
- Deterministic builds with Clang and LLD
	- http://blog.llvm.org/2019/11/deterministic-builds-with-clang-and-lld.html
- Reproducible Builds — a set of software development practices that create an independently-verifiable path from source to binary code
	- https://reproducible-builds.org/

---

# Build Performance

## Build Performance Readings

- 2 tips to make your C++ projects compile 3 times faster
	- Tip #1: Distributing compilation load
	- Tip #2: Using a distcc server container
	- https://developers.redhat.com/blog/2019/05/15/2-tips-to-make-your-c-projects-compile-3-times-faster/
- 30% faster Windows builds with clang-cl and the new `/Zc:dllexportInlines-` flag
	- http://blog.llvm.org/2018/11/30-faster-windows-builds-with-clang-cl_14.html
- Anders Schau Knatten
	- Another Reason to Avoid #includes in Headers
		- https://blog.knatten.org/2012/11/09/another-reason-to-avoid-includes-in-headers/
	- How to avoid includes in headers
		- https://blog.knatten.org/2012/11/30/how-to-avoid-includes-in-headers/
- Aras Pranckevičius
	- Unreasonable Effectiveness of Profilers (profiling the build system) - http://aras-p.info/blog/2017/08/08/Unreasonable-Effectiveness-of-Profilers/
	- Forced Inlining Might Be Slow - https://aras-p.info/blog/2017/10/09/Forced-Inlining-Might-Be-Slow/
	- Best unknown MSVC flag: d2cgsummary - https://aras-p.info/blog/2017/10/23/Best-unknown-MSVC-flag-d2cgsummary/
	- Slow to Compile Table Initializers - https://aras-p.info/blog/2017/10/24/Slow-to-Compile-Table-Initializers/
	- Investigating compile times, and Clang -ftime-report - http://aras-p.info/blog/2019/01/12/Investigating-compile-times-and-Clang-ftime-report/
	- Another cool MSVC flag: /d1reportTime
		- http://aras-p.info/blog/2019/01/21/Another-cool-MSVC-flag-d1reportTime/
		- Reports where the compiler frontend spends time.
		- Passing /d1reportTime to the MSVC compiler (cl.exe) will make it print:
			- Which header files are included (hierarchically), with time taken for each,
			- Which classes are being parsed, with time taken for each,
			- Which functions are being parsed, with time taken for each.
- C++ Compilation Speed
	- Walter Bright - DDJ, August 17, 2010
	- https://digitalmars.com/articles/b54.html
	- http://www.drdobbs.com/cpp/c-compilation-speed/228701711
- C++ Compilation: Fixing It
	- http://virtuallyrandom.com/c-compilation-fixing-it/
- Faster C++ builds
	- http://www.bitsnbites.eu/faster-c-builds/
- Identifying and Understanding Header File Hotspots in C/C++ Build Processes
	- Automated Software Engineering, Vol. 23, No. 4, 2016
	- Shane McIntosh, Bram Adams, Meiyappan Nagappan, Ahmed E. Hassan
	- http://rebels.ece.mcgill.ca/journalpaper/2015/07/08/identifying-and-understanding-header-file-hotspots-in-c-cpp-build-processes.html
- Improving C++ Builds with Split DWARF
	- https://www.productive-cpp.com/improving-cpp-builds-with-split-dwarf/
- Physical Design of The Machinery
	- http://ourmachinery.com/post/physical-design/
- Reducing Build Time through Precompilations for Evolving Large Software
	- International Conference on Software Maintenance (ICSM) 2005
	- Yu, Yijun; Dayani-Fard, Homayoun; Mylopoulos, John and Andritsos, Periklis 
	- http://www.cs.toronto.edu/%7Eperiklis/pubs/icsm05.pdf
	- http://oro.open.ac.uk/6944/
- To Unify or Not to Unify: A Case Study on Unified Builds (in WebKit)
	- Compiler Construction (CC) 2019
	- Takafumi Kubota, Yusuke Suzuki, and Kenji Kono
	- https://doi.org/10.1145/3302516.3307347

## Build Performance Software

- Cotire (compile time reducer)
	- a CMake module that speeds up the build process of CMake based build systems by fully automating techniques as precompiled header usage and single compilation unit builds for C and C++.
	- https://github.com/sakra/cotire

### Benchmarking and Profiling

- Clang -ftime-trace and ftime-trace-granularity=N
	- http://releases.llvm.org/9.0.0/tools/clang/docs/ReleaseNotes.html#new-compiler-flags
	- Clang Time Trace Feature
		- https://www.snsystems.com/technology/tech-blog/clang-time-trace-feature
	- Clang Build Analyzer
		- Clang build analysis tool using -ftime-trace
		- https://github.com/aras-p/ClangBuildAnalyzer
		- https://aras-p.info/blog/2019/09/28/Clang-Build-Analyzer/
		- time-trace: timeline / flame chart profiler for Clang
			- https://aras-p.info/blog/2019/01/16/time-trace-timeline-flame-chart-profiler-for-Clang/
- CTMark (Compile Time Mark)
	- https://github.com/llvm-mirror/test-suite/tree/master/CTMark
- Metabench: A simple framework for compile-time microbenchmarks
	- http://metaben.ch/
	- https://github.com/ldionne/metabench
- Templight: Template Instantiation Profiler and Debugger
	- a Clang-based tool to profile the time and memory consumption of template instantiations and to perform interactive debugging sessions to gain introspection into the template instantiation process
	- https://github.com/mikael-s-persson/templight
	- Use templight and Templar to debug C++ templates
		- https://baptiste-wicht.com/posts/2016/02/use-templight-and-templar-to-debug-cpp-templates.html
	- Templight: A Clang Extension for Debugging and Profiling C++ Template Metaprograms
		- 2015 EuroLLVM Developers’ Meeting, Zoltan Porkolab
		- https://llvm.org/devmtg/2015-04/slides/EuroLLVM2015Templight.pdf
		- https://www.youtube.com/watch?v=djAPtopWhRU
- Visual C++ - C++ Build Insights
	- Get started with C++ Build Insights
		- https://docs.microsoft.com/en-us/cpp/build-insights/get-started-with-cpp-build-insights
	- Introducing C++ Build Insights
		- https://devblogs.microsoft.com/cppblog/introducing-c-build-insights/

### Caching

- ccache: A Fast C/C++ Compiler Cache
	- https://ccache.samba.org
- distcc: A free distributed C/C++ compiler system
	- https://github.com/distcc/distcc
- icecream: Distributed compiler with a central scheduler to share build load
	- https://github.com/icecc/icecream
- sccache - Shared Compilation Cache
	- https://github.com/mozilla/sccache

### Dependencies Analysis and Optimization

- cpp-dependencies: Tool to check C++ #include dependencies (dependency graphs created in .dot format)
	- https://github.com/tomtom-international/cpp-dependencies
- Header Hero: optimizing C++ codebase header #include dependencies
	- A tool for optimizing C++ header files and reducing build times.
	- https://bitbucket.org/bitsquid/header_hero
	- https://bitsquid.blogspot.com/2011/10/caring-by-sharing-header-hero.html
	- https://aras-p.info/blog/2018/01/17/Header-Hero-Improvements/
- include-what-you-use
	- A tool for use with clang to analyze #includes in C and C++ source files
	- https://include-what-you-use.org/
	- https://github.com/include-what-you-use/include-what-you-use

## Build Performance Talks

- Common-sense acceleration of your MLOC build
	- CppCon 2014; Matt Hargett
	- https://www.youtube.com/watch?v=t4M3yG1dWho
- LLVM Compile-Time: Challenges. Improvements. Outlook.
	- 2017 LLVM Developers’ Meeting; Michael Zolotukhin
	- https://www.youtube.com/watch?v=bYHMwyyZ6Mk
- Optimizing builds on Windows
	- 2019 LLVM Developers’ Meeting; Alexandre Ganea
	- https://www.youtube.com/watch?v=usPL_DROn4k
	- https://llvm.org/devmtg/2019-10/slides/Ganea-OptimizingBuildesOnWindows.pdf
- Optimizing compilation times with Templates
	- CppCon 2017: Eddie Elizondo
	- https://www.youtube.com/watch?v=NPWQ7xKfIHQ
	- https://github.com/eduardo-elizondo/cppcon2017
- Practical Techniques for Improving C++ Build Times
	- CppCon 2017; Dmitry Panin
	- https://www.youtube.com/watch?v=h8UoYG4dvH8
- The Hitchhiker's Guide to Faster Builds
	- Viktor Kirilov
	- slides: https://slides.com/onqtam/faster_builds
	- CppOnSea 2019 - https://www.youtube.com/watch?v=anbOy47fBYI
	- C++ Russia 2019 - https://www.youtube.com/watch?v=5rRLHRRqg5A
	- code::dive 2018
		- Part 1: https://www.youtube.com/watch?v=WSFbNhCbdJM
		- Part 2: https://www.youtube.com/watch?v=9-Y5JnJlypM

---

# Software

- Build System Shootout: Comparison of build program expressive power
	- https://github.com/ndmitchell/build-shootout
- TraceCode: Trace a build to find out which source files are built in a binary
	- https://github.com/nexB/tracecode-toolkit
	- Debug your build by tracing and reversing: stracing your build from sources to binaries
		- https://fosdem.org/2018/schedule/event/debugging_tools_stracing_build/

## Autotools

- Autoconf / Automake Basics
	- Mark K. Kim; Linux Users' Group of Davis. March 2, 2004.
	- https://www.lugod.org/presentations/autotools/presentation/autotools.pdf
- Autotools Mythbuster
	- "Autotools Mythbuster is a no-nonsense guide to Autotools, written with the idea of providing a full, integrated view of the tools in the GNU build chain: autoconf, automake, libtool, pkg-config, and so on."
	- https://autotools.io/
- Autotools Tutorial
	- https://www.lrde.epita.fr/~adl/autotools.html
- Autotools Tutorial for Beginners
	- http://markuskimius.wikidot.com/programming:tut:autotools
- Autotools, 2nd Edition
	- A Practitioner's Guide to GNU Autoconf, Automake, and Libtool
	- 2019; John Calcote
	- https://nostarch.com/autotools2e
	- Chapter 2: A Brief Introduction to the GNU Autotools
		- https://nostarch.com/download/samples/Autotools2e_Sample_Ch2.pdf
- Autotools: A Demystification Tutorial
	- Embedded Linux Conference 2016; Thomas Petazzoni
	- https://www.youtube.com/watch?v=_zX8LJ9Xjyk
	- http://events.linuxfoundation.org/sites/events/files/slides/petazzoni-autotools-tutorial.pdf
- Autotools: a practitioner's guide to Autoconf, Automake and Libtool
	- http://freesoftwaremagazine.com/books/autotools_a_guide_to_autoconf_automake_libtool/
- Four Languages and Lots of Macros: Analyzing Autotools Build Systems
	- GPCE 2017
	- Jafar M. Al-Kofahi, Suresh Kothari, Christian Kästner
	- https://conf.researchr.org/event/gpce-2017/gpce-2017-gpce-2017-four-languages-and-lots-of-macros-analyzing-autotools-build-systems
	- https://www.cs.cmu.edu/~ckaestne/pdf/gpce17.pdf
- GNU Autoconf: A uniform means of creating makefiles at build time
	- Ethan McCallum - C/C++ Users Journal, January 2006
	- http://collaboration.cmc.ec.gc.ca/science/rpn/biblio/ddj/Website/articles/CUJ/2006/0601/0601mccallum/0601mccallum.html
	- https://web.archive.org/http://www.drdobbs.com/gnu-autoconf/184402060
	- https://web.archive.org/http://collaboration.cmc.ec.gc.ca/science/rpn/biblio/ddj/Website/articles/CUJ/2006/0601/0601mccallum/0601mccallum.html
- GNU Autoconf, Automake and Libtool
	- https://www.sourceware.org/autobook/
- Minimal autotools template for C++11/14 projects
	- https://github.com/mpoullet/autotools-cpp-template
- Minimal autotools template for C/C++ library projects
	- https://github.com/mpoullet/autotools-lib-template

## Bazel

- Bazel: a fast, scalable, multi-language and extensible build system
	- https://bazel.build/
	- https://github.com/bazelbuild/bazel
- Awesome Bazel: A curated list of Bazel rules, tooling and resources.
	- https://github.com/jin/awesome-bazel
- bazel-tools: Tools for dealing with very large Bazel-managed repositories
	- https://github.com/spotify/bazel-tools
- Bazel How to build at Google scale?
	- FOSDEM 2017; Klaus Aehlig
	- https://archive.fosdem.org/2017/schedule/event/bazel/
	- https://www.youtube.com/watch?v=lOUwu0myF8M
- External C++ dependency management in Bazel
	- https://medium.com/@htuch/external-c-dependency-management-in-bazel-dd37477422f5
- Faster Bazel builds with remote caching: a benchmark
	- https://nicolovaligi.com/faster-bazel-remote-caching-benchmark.html
- Your Build in a Datacenter: Remote Caching and Execution in Bazel
	- FOSDEM 2018; Jakob Buchgraber
	- https://www.youtube.com/watch?v=PrTun05W5g4
	- https://fosdem.org/2018/schedule/event/datacenter_build/

## Boost.Build

- Boost.Build - http://www.boost.org/build/
- Understanding Boost.Build
	- C++Now 2016; Steven Watanabe
	- https://www.youtube.com/watch?v=8yc7ZvU0yOw
	- https://github.com/boostcon/cppnow_presentations_2016/blob/master/03_friday/understanding_boost_build.pdf
-  Complete Overview on Boost.Jam and Boost.Build
	- BoostCon 2011; Boris Schaeling
	- https://www.youtube.com/watch?v=OgYwvzUUupM
	- https://github.com/boostcon/2011_presentations/raw/master/mon/Boost.Build.pdf

## build2

- build2: C++ Build Toolchain
	- https://build2.org/
	- https://github.com/build2/
- C++ Dependency Management: from Package Consumption to Project Development
	- CppCon 2018; Boris Kolpackov
	- https://www.youtube.com/watch?v=Nni2Qu2WitY

## CMake

- Awesome CMake
	- A curated list of awesome CMake scripts, modules, examples and others
	- https://github.com/onqtam/awesome-cmake

### CMake Examples

- C++/CMake modern boilerplate
	- https://github.com/Lectem/cpp-boilerplate
- CMake: config mode of find_package command (examples)
	- https://github.com/forexample/package-example
- CMake cookbook recipes
	- https://github.com/dev-cafe/cmake-cookbook
- CMake Examples
	- https://github.com/ttroy50/cmake-examples
- learning-cmake: a simple CMake tutorial project which contains some different scenarios
	- https://github.com/Akagi201/learning-cmake
- Modern CMake Examples
	- https://github.com/pr0g/cmake-examples
- Polly: Collection of CMake toolchain files and scripts for cross-platform build and CI testing (GCC, Visual Studio, iOS, Android, Clang analyzer, sanitizers etc.) 
	- https://github.com/ruslo/polly

### CMake Readings

- An Introduction to Modern CMake
	- https://cliutils.gitlab.io/modern-cmake/
- Basic CMake usage
	- https://codingnest.com/basic-cmake/
- CGold: The Hitchhiker’s Guide to the CMake
	- https://cgold.readthedocs.io/en/latest/
- CMake 3.16 added support for precompiled headers & unity builds - what you need to know
	- http://onqtam.com/programming/2019-12-20-pch-unity-cmake-3-16/
- CMake Coding Style
	- https://community.kde.org/Policies/CMake_Coding_Style
- Dev Santa Claus - Nick Sarten
	- Part 1: Adding Clang Sanitizers to a CMake Build
		- https://genbattle.bitbucket.io/blog/2018/01/05/Dev-Santa-Claus-Part-1/
	- Part 2: C++ code coverage metrics with gcov
		- setting up code coverage metrics for a C++ codebase built using Bamboo, CMake, and GCC
		- https://genbattle.bitbucket.io/blog/2018/01/19/Dev-Santa-Claus-Part-2/
- Effective CMake by Kai Wolf
	- http://effective-cmake.com
	- https://leanpub.com/effective-cmake
- Effective Modern CMake - Manuel Binna
	- https://gist.github.com/mbinna/c61dbb39bca0e4fb7d1f73b0d66a4fd1
- Everything You Never Wanted to Know About CMake
	- https://izzys.casa/2019/02/everything-you-never-wanted-to-know-about-cmake/
- How to Build a CMake-Based Project
	- http://preshing.com/20170511/how-to-build-a-cmake-based-project/
- It's Time To Do CMake Right
	- https://pabloariasal.github.io/2018/02/19/its-time-to-do-cmake-right/
- Learn CMake's Scripting Language in 15 Minutes
	- http://preshing.com/20170522/learn-cmakes-scripting-language-in-15-minutes/
- Professional CMake: A Practical Guide
	- https://crascit.com/professional-cmake/
- Speed up your C++ unit tests cycles with CMake/CTest (and the right testing framework)
	- https://a4z.bitbucket.io/blog/2018/05/17/Speed-up-your-test-cycles-with-CMake.html
- The Architecture of Open Source Applications: CMake
	- http://www.aosabook.org/en/cmake.html
- The Ultimate Guide to Modern CMake
	- https://rix0r.nl/blog/2015/08/13/cmake-guide/
- Tutorial: Easy dependency management for C++ with CMake and Git
	- http://foonathan.net/blog/2016/07/07/cmake-dependency-handling.html
- Using ccache with CMake
	- https://crascit.com/2016/04/09/using-ccache-with-cmake/

### CMake Software

- BLT (Build, Link and Triumph): A streamlined CMake build system foundation for developing HPC software
	- composition of CMake macros and several widely used open source tools assembled to simplify HPC software development.
	- https://github.com/llnl/blt
	- http://llnl-blt.readthedocs.io/en/latest/
- CMake Unit
	- A unit testing framework for CMake.
	- https://github.com/polysquare/cmake-unit
- CMakeBuildPackage: Automatic project build script with CMake
	- https://github.com/berenm/CMakeBuildPackage
- cmake format: Source code formatter for cmake listfiles.
	- https://github.com/cheshirekow/cmake_format
- CMake Modules
	- Additional CMake Modules
		- https://github.com/bilke/cmake-modules
	- Ryan's CMake Modules
		- https://github.com/rpavlik/cmake-modules
- cmany: CMake build tree batching tool
	- https://github.com/biojppm/cmany
- configure-cmake: autotools-style configure script wrapper around CMake
	- https://github.com/nemequ/configure-cmake
- CPM.cmake
	- CMake's missing package manager. A small CMake script for setup-free, cross-platform and reproducible dependency management.
	- https://github.com/TheLartians/CPM.cmake
- Izzy's eXtension Modules: Make CMake less painful when trying to write Modern Flexible CMake
	- https://github.com/slurps-mad-rips/ixm
- ucm - useful cmake macros
	- https://github.com/onqtam/ucm

### CMake Talks

- Building C++
	- C++ Edinburgh 2018; Morris Hafner
	- https://www.youtube.com/watch?v=n_f-2p5eDBo
- C++ Weekly - Jason Turner
	- Ep 78 - Intro to CMake
		- https://www.youtube.com/watch?v=HPMvU64RUTY
		- https://github.com/lefticus/cpp_starter_project
	- Ep 82 - Intro To CTest
		- https://www.youtube.com/watch?v=ZlMbqFcJEzA
- Deep CMake for Library Authors
	- CppCon 2019; Craig Scott
	- https://www.youtube.com/watch?v=m0DwB4OvDXk
- Effective CMake
	- Daniel Pfeifer
	- C++Now 2017
		- https://www.youtube.com/watch?v=bsXLMQ6WgIk
		- https://github.com/boostcon/cppnow_presentations_2017/raw/master/05-19-2017_friday/effective_cmake__daniel_pfeifer__cppnow_05-19-2017.pdf
	- MUCplusplus 2017
		- https://www.youtube.com/watch?v=rLopVhns4Zs
- Effective dependency management with CMake
	- MUCplusplus 2017; Kai Wolf 
	- https://www.youtube.com/watch?v=QayyhI-36os
- Embracing Modern CMake
	- Stephen Kelly
	- https://steveire.wordpress.com/2017/11/05/embracing-modern-cmake/
	- Dublin C++ User Group 2017
		- https://www.youtube.com/watch?v=JsjI5xr1jxM
	- NDC TechTown 2019
		- https://www.youtube.com/watch?v=mn1ZnO3MtVk
- How to CMake Good
	- https://vector-of-bool.github.io/2018/08/12/cmake-good.html
	- https://www.youtube.com/playlist?list=PLK6MXr8gasrGmIiSuVQXpfFuE1uPT615s
- Introduction to CMake
	- SwedenCpp 2018; Florent Castelli
	- Examples:
		- https://bit.ly/swedencpp-cmake-workshop
		- https://github.com/Orphis/cmake-workshop
	- Slides:
		- https://bit.ly/swedencpp-cmake-slides
		- https://docs.google.com/presentation/d/1vIEfCE33-1BEMT1nNQQbhe-1va-3m2pL9c6_WrIIjdU/
	- Video:
		- https://www.youtube.com/watch?v=jt3meXdP-QI
- Modern CMake for modular design
	- Meeting C++ 2017; Mathieu Ropert
	- https://www.youtube.com/watch?v=ztrnb-bVVPo
- More Modern CMake - Working with CMake 3.12 and later
	- Meeting C++ 2018; Deniz Bahadir
	- https://meetingcpp.com/2018/Talks/items/More_Modern_CMake___Working_with_CMake_3_12_and_later.html
	- https://meetingcpp.com/mcpp/slides/2018/MoreModernCMake.pdf
	- https://www.youtube.com/watch?v=y7ndUhdQuU8
- Oh No! More Modern CMake
	- Meeting C++ 2019; Deniz Bahadir
	- https://www.youtube.com/watch?v=y9kSr5enrSk
	- https://github.com/Bagira80/More-Modern-CMake
- Using Modern CMake Patterns to Enforce a Good Modular Design
	- CppCon 2017; Mathieu Ropert 
	- https://www.youtube.com/watch?v=eC9-iRN2b04

## Gradle

- https://gradle.org/
- Introduction into C++ Builds with Gradle
	- https://thoughts-on-cpp.com/2019/04/10/introduction-into-c-builds-with-gradle/

## Make

- A more helpful makefile
	- https://jakemccrary.com/blog/2018/12/27/a-more-helpful-makefile/
- A Super-Simple Makefile for Medium-Sized C/C++ Projects 
	- https://spin.atomicobject.com/2016/08/26/makefile-c-projects/
- A Tutorial on Portable Makefiles
	- http://nullprogram.com/blog/2017/08/20/
- Makefile Tutorial
	- https://gist.github.com/isaacs/62a2d1825d04437c6f08
- Notes for new Make users
	- http://gromnitsky.users.sourceforge.net/articles/notes-for-new-make-users/
- Propositions as Filenames, Builds as Proofs: The Essence of Make
	- https://bentnib.org/posts/2015-04-17-propositions-as-filenames-essence-of-make.html
- Well documented Makefiles (available via `make help`)
	- https://suva.sh/posts/well-documented-makefiles/

### GNU Make

- GNU Make - http://www.gnu.org/software/make/
	- Manual - https://www.gnu.org/software/make/manual/
- An Empirical Analysis of GNU Make in Open Source Projects
	- 2017 PhD Thesis; [Douglas Martin](http://research.cs.queensu.ca/~doug/research.html)
	- https://qspace.library.queensu.ca/handle/1974/15767
	- Makefile Corpus - http://research.cs.queensu.ca/~doug/files/MakeEgs.tar.gz
	- Makefile Framework - http://research.cs.queensu.ca/~doug/files/MakeFramework.zip
- An Empirical Study of Unspecified Dependencies in Make-Based Build Systems
	- Empirical Software Engineering (2017)
	- Cor-Paul Bezemer, Shane McIntosh, Bram Adams, Daniel M. German, Ahmed E. Hassan
	- https://doi.org/10.1007/s10664-017-9510-8
	- http://rebels.ece.mcgill.ca/journalpaper/2017/03/07/an-empirical-study-of-unspecified-dependencies-in-make-based-build-systems.html
	- http://sail.cs.queensu.ca/Downloads/EMSE2017_AnEmpiricalStudyOfUnspecifiedDependenciesInMake-BasedBuildSystems.pdf
	- Slides: https://www.slideshare.net/corpaulbezemer/an-empirical-study-of-unspecified-dependencies-in-makebased-build-systems
- GNU make - Paul D. Smith - http://make.mad-scientist.net/
	- Paul Smith's Rules of Makefiles - http://make.mad-scientist.net/papers/rules-of-makefiles/
	- Deferred Simple Variable Expansion - http://make.mad-scientist.net/deferred-simple-variable-expansion/
- GNU Make articles - John Graham-Cumming
	- http://blog.jgc.org/2013/02/updated-list-of-my-gnu-make-articles.html
	- https://www.cmcrossroads.com/keyword/type/3037?type=article
	- https://www.cmcrossroads.com/keyword/type/3169?type=article
- GNU Make meets file names with spaces in them - https://www.cmcrossroads.com/article/gnu-make-meets-file-names-spaces-them
- GNU Make Standard Library - http://gmsl.sourceforge.net/
- HOWTO: Intro to GNU make variables - https://blog.melski.net/2015/01/07/howto-intro-to-gnu-make-variables/
- Make is (probably) fine 
	- https://blog.yossarian.net/2019/04/23/Make-is-probably-fine
- Make it simple: An empirical analysis of GNU Make feature use in open source projects
	- International Conference on Program Comprehension 2015
	- Douglas H Martin, James R Cordy, Bram Adams, Giulio Antoniol
	- http://maroon.cs.queensu.ca/home/cordy/Papers/MCAA_ICPC15_Makefiles.pdf
- Managing Projects with GNU Make
	- http://www.wanderinghorse.net/computing/make/
	- http://www.oreilly.com/openbook/make3/book/index.csp
	- https://notendur.hi.is/jonasson/software/make-book/
- Properly using GNU-Make - https://slashvar.github.io/2017/02/13/using-gnu-make.html
- Remake – GNU Make with comprehensible tracing and a debugger
	- http://bashdb.sourceforge.net/remake/
	- https://github.com/rocky/remake

## Meson

- The Meson Build system
	- http://mesonbuild.com/
	- https://mesonbuild.com/Videos.html
	- https://github.com/mesonbuild/meson
- Getting started with Meson build system and C++
	- https://medium.com/@germandiagogomez/getting-started-with-meson-build-system-and-c-83270f444bee
	- https://medium.com/@germandiagogomez/getting-started-with-meson-in-c-part-2-58150354ff17
	- https://medium.com/@germandiagogomez/getting-started-with-meson-in-c-part-3-70b9bc419957
	- https://medium.com/@germandiagogomez/getting-started-with-meson-part-4-8bceec6149e1

## Ninja

- Ninja: a small build system with a focus on speed
	- https://ninja-build.org/
	- https://github.com/ninja-build/ninja
- Benchmarking the Ninja build system
	- http://david.rothlis.net/ninja-benchmark/
- Building Like (a) Ninja [Pt1]
	- https://vector-of-bool.github.io/2018/12/20/build-like-ninja-1.html
- GN: a meta-build system that generates build files for Ninja
	- https://gn.googlesource.com/gn
	- https://is.gd/gn_intro
	- Basic //build directory for GN-based projects
		- https://github.com/timniederhausen/gn-build
- ninjatracing: Convert .ninja_log files to chrome's about:tracing format.
	- https://github.com/nico/ninjatracing

## Tundra

- Tundra, a build system
	- Tundra is a high-performance code build system designed to give the best possible incremental build times even for very large software projects.
	- https://github.com/deplinenoise/tundra

## Tup

- Tup: a file-based build system.
	- http://gittup.org/tup/
	- https://github.com/gittup/tup
- Lessons and Pitfalls in Building Firefox with Tup
	- 12th Seminar on Advanced Techniques & Tools for Software Evolution (SATToSE) 2019
	- Guillaume Maudoux and Kim Mens
	- http://hdl.handle.net/2078.1/223053

## Visual Studio

- clcache.py - a compiler cache for Microsoft Visual Studio
	- https://github.com/frerich/clcache
- CompileTimer: Set of tests to benchmark the compile time of C++ constructs
	- https://github.com/janwilmans/CompileTimer
- Make VC++ Compiles Fast Through Parallel Compilation
	- https://randomascii.wordpress.com/2014/03/22/make-vc-compiles-fast-through-parallel-compilation/
- NMAKE
	- The Microsoft Program Maintenance Utility (NMAKE.EXE)
		- https://docs.microsoft.com/en-us/cpp/build/nmake-reference
- Visual Studio 2017 Throughput Improvements and Advice
	- https://blogs.msdn.microsoft.com/vcblog/2018/01/04/visual-studio-2017-throughput-improvements-and-advice/

### MSBuild

- MSBuild (Visual C++) - https://docs.microsoft.com/en-us/cpp/build/msbuild-visual-cpp 
- Make VC++ Compiles Fast Through Parallel Compilation
	- https://randomascii.wordpress.com/2014/03/22/make-vc-compiles-fast-through-parallel-compilation/
- Microsoft.Build (MSBuild)
	- The Microsoft Build Engine: the build platform for .NET and Visual Studio
	- https://github.com/Microsoft/msbuild
	- https://docs.microsoft.com/en-us/visualstudio/msbuild/
- MSBuild (Visual C++) - https://docs.microsoft.com/en-us/cpp/build/msbuild-visual-cpp
- MSBuild Binary and Structured Log Viewer - http://msbuildlog.com/
- Build Tools
	- build native and managed MSBuild-based applications without requiring the Visual Studio IDE. There are options to install the Visual C++ compilers and libraries, MFC, ATL, and C++/CLI support, and .NET and .NET Core support.
	- http://aka.ms/buildtools
	- GoingNative 63: C++ Build Tools - https://channel9.msdn.com/Shows/C9-GoingNative/GoingNative-63-CPP-Build-Tools
- Using A Custom Toolchain In Visual Studio With MSBuild
	- http://www.reedbeta.com/blog/custom-toolchain-with-msbuild/
- Visual Studio and Custom Build Rules 
	- http://miken-1gam.blogspot.com/2013/01/visual-studio-and-custom-build-rules.html

## Xcode

- xcbuild-debugging-tricks
	- Xcode new build system debugging tricks 
	- https://gist.github.com/ddunbar/2dda0e836c855ea96759d1d05f086d69

## xmake

- xmake: A cross-platform build utility based on Lua
	- https://xmake.io/
	- https://github.com/xmake-io/xmake/

---

# Talks

## 2019

- Behind the Scenes of a C++ Build System
	- CppCon 2019; Jussi Pakkanen
	- https://www.youtube.com/watch?v=34KzT2yvQuM
	- https://github.com/CppCon/CppCon2019/tree/master/Presentations/behind_the_scenes_of_a_cpp_build_system
- Building Modules
	- CppCon 2019; Michael Spencer 
	- https://www.youtube.com/watch?v=L0SHHkBenss

## 2018

- Build Systems: a Simple Solution to a Complicated Problem
	- CppCon 2018; Peter Bindels
	- https://www.youtube.com/watch?v=mWOmkwv8N_U
- Creating the Complete Build Package
	- CppCon 2018
	- Panelists: Boris Kolpackov, Titus Winter, Robert Schumacher, Paddy McDonald, Manuel Klimek
	- https://www.youtube.com/watch?v=TjdCxXdjaSA
- Don't package your libraries, write packagable libraries!
	- CppCon 2018; Robert Schumacher
	- https://www.youtube.com/watch?v=sBP17HQAQjk
- What to Expect from a Next-Generation C++ Build System
	- CppCon 2018; Boris Kolpackov
	- https://www.youtube.com/watch?v=cJP7SSLjvSI

## 2017

- Building C++ Modules
	- CppCon 2017; Boris Kolpackov
	- https://www.youtube.com/watch?v=E8EbDcLQAoc
- There Will Be Build Systems: I Configure Your Milkshake
	- CppCon 2017; Isabella Muerte
	- https://www.youtube.com/watch?v=7THzO-D0ta4
