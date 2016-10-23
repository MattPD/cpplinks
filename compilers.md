# [C++ links](README.md): compilers

Note: see also [Assembly (x86)](assembly.x86.md)

# Background & Resources

* Jordan Rose (Swift team) recommendations - http://belkadan.com/blog/2015/11/Recommendations/
* GCC Wiki - List of compiler books - https://gcc.gnu.org/wiki/ListOfCompilerBooks
* Let’s Build A Simple Interpreter - https://ruslanspivak.com/lsbasi-part1/
* Life of an instruction in LLVM - http://eli.thegreenplace.net/2012/11/24/life-of-an-instruction-in-llvm
* Life of an instruction in Clang / LLVM - https://github.com/thegameg/llvm-life/
* LLVM - Chris Lattner, The Architecture of Open Source Applications - http://www.aosabook.org/en/llvm.html
* LLVM Tutorial: Kaleidoscope - http://llvm.org/docs/tutorial/
  - Haskell version: http://www.stephendiehl.com/llvm/
* LLVM for Grad Students - http://adriansampson.net/blog/llvm.html
* Resources for Amateur Compiler Writers - http://c9x.me/compile/bib/
* Object Files and Symbols - http://nickdesaulniers.github.io/blog/2016/08/13/object-files-and-symbols/
* Validation & testing: http://web.cs.ucdavis.edu/~su/emi-project/
* https://github.com/melling/ComputerLanguages/blob/master/compilers.org

# Courses

* Advanced Compilers - John Regehr, University of Utah
  - Weeks 1 and 2: http://blog.regehr.org/archives/1419
  - Weeks 3-5: http://blog.regehr.org/archives/1428
* Compilers -  Alex Aiken, Stanford OpenEdX
  - http://online.stanford.edu/course/compilers-0
* Compilers - Hal Perkins, CSEP 501, UW CSE
  - https://courses.cs.washington.edu/courses/csep501/
  - Winter 2016 Homepage: https://courses.cs.washington.edu/courses/csep501/16wi/
  - Winter 2016 Playlist: https://www.youtube.com/playlist?list=PLTPQEx-31JXhfAWGnGzwbfhB2zUB7Jd4C
  - Winter 2016 Topics: https://courses.cs.washington.edu/courses/csep501/16wi/calendar/lecturelist.html
* Program Analysis and Reliability - Nick Sumner, CMPT 886, Spring 2015, SFU
  - Playlist: https://www.youtube.com/playlist?list=PLNC6lmsIySCOPjY8IwKBtD2cqe-MMgIGM
  - Schedule & Slides: http://www.cs.sfu.ca/~wsumner/teaching/886/15/schedule.html

# Documentation

* Clang documentation - http://clang.llvm.org/docs/
* GCC online documentation - https://gcc.gnu.org/onlinedocs/
* LLVM documentation - http://llvm.org/docs/
* Visual C++ documentation - https://msdn.microsoft.com/en-us/library/60k1461a.aspx

# Implementations

* LLVM - http://llvm.org/
  - LLVM Developers' Meeting - http://llvm.org/devmtg/
  - http://blog.llvm.org/
  - http://llvmweekly.org/
* GCC (GNU Compiler Collection) - https://gcc.gnu.org/
  - GNU Tools Cauldron - https://gcc.gnu.org/wiki#Events
  - https://twitter.com/gnutools/
* Visual C++ - https://www.visualstudio.com/vs/cplusplus/
  - https://blogs.msdn.microsoft.com/vcblog/

# Linking

* _The missing link: explaining ELF static linking, semantically._ Stephen Kell, Dominic P. Mulligan, and Peter Sewell. OOPSLA 2016.
  - http://www.cl.cam.ac.uk/~pes20/rems/papers/oopsla-elf-linking-2016.pdf
  - https://bitbucket.org/Peter_Sewell/linksem/
* Linkers - 20 part linker essay by Ian Lance Taylor - https://lwn.net/Articles/276782/

# Optimization

* Automatic Feedback Directed Optimizer (AutoFDO)
  - https://gcc.gnu.org/wiki/AutoFDO
  - https://github.com/google/autofdo
* Compiler Optimization Options
  - GCC: https://gcc.gnu.org/onlinedocs/gcc/Optimize-Options.html
  - Clang: http://clang.llvm.org/docs/CommandGuide/clang.html#cmdoption-O0 - https://stackoverflow.com/questions/15548023/clang-optimization-levels
  - Visual C++: https://msdn.microsoft.com/en-us/library/19z1t1wy.aspx
* Devirtualization in C++ - https://hubicka.blogspot.com/search/label/devirtualization
* Link time optimization (LTO) - https://hubicka.blogspot.com/search/label/link-time%20optimization
* GoingNative 50: New Visual C++ Code Optimizer - https://channel9.msdn.com/Shows/C9-GoingNative/GoingNative-50-New-Visual-C-Code-Optimizer

## Superoptimization

* GNU Superoptimizer Version 2 - https://github.com/embecosm/gso2
* Souper - a superoptimizer for LLVM IR - https://github.com/google/souper
* Stochastic Superoptimization - http://blog.regehr.org/archives/923
* STOKE: A stochastic superoptimizer and program synthesizer - http://stoke.stanford.edu - https://github.com/StanfordPL/stoke
* Superoptimizing Compilers - http://superoptimization.org/wiki/Superoptimizing_Compilers
* Superoptimization - James Pallister - FOSDEM 2015 - https://archive.fosdem.org/2015/schedule/event/superoptimization/

# Sanitizers

https://maitesin.github.io/clang_sanitizers/

# Talks

## 2016

* Introduction to LLVM – Projects, Components, Integration, Internals - Renato Golin
  - Linaro Connect Las Vegas 2016 (LAS16) \ LAS16-501
  - http://connect.linaro.org/resource/las16/las16-501/
* Anders Hejlsberg on Modern Compiler Construction
  - Channel 9; May 12, 2016
   https://channel9.msdn.com/Blogs/Seth-Juarez/Anders-Hejlsberg-on-Modern-Compiler-Construction
* STOKE: Search-Based Compiler Optimization - Alex Aiken
  - UCI CS Distinguished Lecture; April 29, 2016
  - https://www.youtube.com/watch?v=rZFeTTFp7x4

## 2015

* Understanding Compiler Optimization - Chandler Carruth
  - Opening Keynote Meeting C++ 2015
  - https://www.youtube.com/watch?v=FnGCDLhaxKU
* Stochastic Optimization for x86 Binaries - Eric Schkufza
  - Google Tech Talks; January 12, 2015
  - https://www.youtube.com/watch?v=aD9mZDJzb58

## 2014

* Superoptimizing LLVM - John Regehr
  - UW CSE Colloquium; December 2, 2014
  - https://www.youtube.com/watch?v=Ux0YnVEaI6A
* Compiler Technologies - Jim Hogg
 - Northwest C++ Users' Group; October 15, 2014
 - http://nwcpp.org/october-2014.html

## 2013

* Compiler Confidential - Eric Brumer
  - GoingNative 2013
  - https://channel9.msdn.com/Events/GoingNative/2013/Compiler-Confidential

# Warnings

* leathers - Warning suppression library (C++) - https://github.com/ruslo/leathers
  - Warnings list: https://github.com/ruslo/leathers/wiki/List
