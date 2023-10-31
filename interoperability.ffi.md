# [C++ links](README.md): interoperability - foreign function interfaces (FFIs)

# Contents

- [General](#general)
- Language-specific: [Bash](#bash), [C](#c), [C#](#c-1), [Common Lisp](#common-lisp), [D](#d), [Fortran](#fortran), [Haskell](#haskell), [Java](#java), [JavaScript](#javascript), [Julia](#julia), [Lua](#lua), [Nim](#nim), [Objective-C](#objective-c), [OCaml](#ocaml), [PHP](#php), [Python](#python), [R](#r), [Rust](#rust), [Scheme](#scheme), [Stata](#stata), [Swift](#swift), [WebAssembly](#webassembly), [Zig](#zig)

---

# General

## General: Readings

- Operational Semantics for Multi-Language Programs
	- Principles of Programming Languages (POPL) 2007
	- Jacob Matthews, Robert Bruce Findler
	- https://dl.acm.org/doi/10.1145/1190215.1190220
	- Formal Semantics for Multi-Language Programs
		- Strange Loop 2023
		- Amal Ahmed
		- https://www.youtube.com/watch?v=xOInz_gt2Fg
- Semantic Soundness for Language Interoperability
	- PLDI 2022
	- Daniel Patterson, Noble Mushtak, Andrew Wagner, Amal Ahmed
	- https://doi.org/10.1145/3519939.3523703
	- https://aps.arxiv.org/abs/2202.13158
	- https://dbp.io/pubs/2022/semint.pdf
	- https://www.youtube.com/watch?v=uasYCcvYIkQ

### General: Readings: Optimization

- Low-level Cross-Language Post-Link Optimisation
	- 2021 PhD Dissertation
	- Nandor Licker
	- https://doi.org/10.17863/CAM.87641

### General: Readings: Security

- BinWrap: Hybrid Protection Against Native Node.js Add-ons
	- ACM Asia Conference on Computer and Communications Security (ASIA CCS) 2023
	- George Christou, Grigoris Ntousakis, Eric Lahtinen, Sotiris Ioannidis, Vasileios P. Kemerlis, Nikos Vasilakis
	- https://cs.brown.edu/~vpk/papers/binwrap.asiaccs23.pdf
	- https://github.com/atlas-brown/binwrap
- COOPER: Testing the Binding Code of Scripting Languages with Cooperative Mutation
	- Network and Distributed System Security Symposium (NDSS) 2022
	- Peng Xu, Yanhao Wang, Hong Hu, Purui Su
	- https://www.ndss-symposium.org/ndss-paper/auto-draft-260/
	- https://github.com/TCA-ISCAS/Cooper
- Cross-Language Attacks
	- Network and Distributed System Security Symposium (NDSS) 2022
	- Samuel Mergendahl, Nathan Burow, Hamed Okhravi
	- https://www.ndss-symposium.org/ndss-paper/auto-draft-259/

## General: Software

- C++ Language Interface Foundation (CLIF)
	- https://github.com/google/clif
- CppInterOp: A Clang-based C++ Interoperability Library
	- https://github.com/compiler-research/CppInterOp
- libffi: A portable foreign-function interface library
	- http://sourceware.org/libffi
	- https://github.com/libffi/libffi
- Scapix Language Bridge
	- Automatic, on the fly bindings from C++ to Java, Objective-C, Swift, Python, JavaScript (WebAssembly), and C#. Bridge code automatically generated directly from C++ header files, no need to manually maintain IDL definitions or bindings.
	- https://github.com/scapix-com/scapix
- SWIG: Simplified Wrapper and Interface Generator
	- http://www.swig.org/

## General: Talks

- Making Libraries Consumable for Non-C++ Developers
	- CppCon 2021
	- Aaron R Robinson
	- https://www.youtube.com/watch?v=4r09pv9v1w0

---

# Bash

- ctypes.sh: a foreign function interface for bash
	- https://github.com/taviso/ctypes.sh

---

# C

- Cross-language interfaces between C and C++ - https://gustedt.wordpress.com/2017/08/08/cross-language-interfaces-between-c-and-c/
- DragonFFI: C Foreign Function Interface and JIT using Clang/LLVM
	- DragonFFI is a C Foreign Function Interface (FFI) library written in C++ and based on Clang/LLVM. It allows any language to call C functions thought the provided APIs and bindings.
	- https://github.com/aguinet/dragonffi/
	- FOSDEM 2018 - https://fosdem.org/2018/schedule/event/dragonffi/
	- DragonFFI: FFI/JIT for the C language using Clang/LLVM - http://blog.llvm.org/2018/03/dragonffi-ffijit-for-c-language-using.html
- Efficient and Reliable Wrapping of C APIs Using Modern C++
	- Vladimir Vishnevskii
	- C++ on Sea 2023
	- https://www.youtube.com/watch?v=SJlyMV_oTpY
- ffi-overhead: comparing the C FFI (foreign function interface) overhead for various programming languages
	- https://github.com/dyu/ffi-overhead
- Hourglass Interfaces for C++ APIs - CppCon 2014
	- https://www.slideshare.net/StefanusDuToit/cpp-con-2014-hourglass-interfaces-for-c-apis
	- https://www.youtube.com/watch?v=PVYdHDm0q6Y
	- https://github.com/CppCon/CppCon2014/tree/master/Presentations/Hourglass%20Interfaces%20for%20C%2B%2B%20APIs
- How to call C libraries from C++
	- CppCon 2014; Lisa Lippincott
	- https://www.youtube.com/watch?v=3ZO0V4Prefc
	- https://github.com/CppCon/CppCon2014/tree/master/Presentations/How%20to%20call%20C%20libraries%20from%20C%2B%2B
	- Code and slides from Lisa Lippincott's “How to Call C libraries from C++” presentation from Cppcon 2014
	- https://github.com/jfirebaugh/PlusPlus
- Skip the FFI: Embedding Clang for C Interoperability
	- 2014 LLVM Developers' Meeting
	- Jordan Rose, John McCall
	- https://llvm.org/devmtg/2014-10/#talk18
- The Challenges of Implementing the C Standard Library in C++
	- CppNow 2023
	- Siva Chandra Reddy
	- https://www.youtube.com/watch?v=cuVrWUGSIgM
	- https://github.com/boostcon/cppnow_presentations_2023/blob/main/cppnow_slides/The_Challenges_of_Implementing_the_C_Standard_Library_in_Cpp.pdf
- The Salami Method
	- The Salami Method finely distinguishes between the different aspects and layers required for exposing platform-independent C++ on different “specific” platforms. At its extreme it strives to create a single, thin, transparent layer for each such aspect so that each layer is more easily built, tested, debugged, managed and maintained.
	- http://videocortex.io/2017/salami-method/
	- The Salami Method: multiplatform C++ development - Adi Shavit, CoreCpp IL Meetup, April 2018
		- https://www.youtube.com/watch?v=jdEmz3iXNlA
	- The Salami Method for Cross Platform Development - CppCon 2018; Adi Shavit
		- https://www.youtube.com/watch?v=ZSpGNiUvXVI
- Using C Libraries in your Modern C++ Embedded Project
	- CppCon 2021; Michael Caisse
	- https://www.youtube.com/watch?v=Ototzy-nP4M

---

# C#

- ClangSharpPInvokeGenerator: take a given set of C or C++ header files and generate C# bindings from them
	- https://github.com/dotnet/ClangSharp#generating-bindings
	- ClangSharp: Clang bindings for .NET written in C#
		- ClangSharp provides Clang bindings written in C#. It is self-hosted and auto-generates itself by parsing the Clang C header files using ClangSharpPInvokeGenerator.
		- https://github.com/dotnet/ClangSharp
	- LLVMSharp: a multi-platform .NET Standard library for accessing the LLVM infrastructure. The bindings are auto-generated using ClangSharp parsing LLVM-C header files.
		- https://github.com/dotnet/llvmsharp
- CoreRTDemo: Building a native library in C# and calling it from C++
	- https://github.com/encrypt0r/CoreRTDemo
	- Writing Native Libraries in C# and using them in other languages
		- https://dev.to/encrypt0r/writing-native-libraries-in-c-3kl
- CppAst.NET: a .NET library providing a C/C++ parser for header files
	- powered by Clang/libclang with access to the full AST, comments, and macros
	- the target primary usage of this library is to serve as a simple foundation for domain oriented PInvoke/Interop codegen
	- https://github.com/xoofx/CppAst.NET/
- CppSharp
	- Tools and libraries to glue C/C++ APIs to high-level languages
	- https://github.com/mono/CppSharp
- Dynamic Invocation (Avoiding PInvoke & API Hooks)
	- https://thewover.github.io/Dynamic-Invoke/
	- https://github.com/FuzzySecurity/BlueHatIL-2020
- P/Invoke: A library containing all P/Invoke code so you don't have to import it every time. Maintained and updated to support the latest Windows OS.
	- https://github.com/AArnott/pinvoke
- The .NET Inter-Operability Operation
	- Derbycon 2017; James Forshaw
	- http://www.irongeek.com/i.php?page=videos/derbycon7/s13-the-net-inter-operability-operation-james-forshaw
- Using Span for high performance interop with unmanaged libraries
	- https://ericsink.com/entries/utf8z.html

---

# Common Lisp

- Clasp — Bringing Common Lisp and C++ Together
	- https://github.com/drmeister/clasp

---

# D

- d++ - #include C and C++ headers in D files
	- https://github.com/atilaneves/dpp
	- https://dlang.org/blog/2019/04/08/project-highlight-dpp/
- Zero Overhead Interface Between DLang & C++ Standard Lib
	- DConf2017; Alexandru Razvan Caciulescu
	- https://www.youtube.com/watch?v=j-Ws4VjyUWg

---

# Fortran

- http://fortranwiki.org/fortran/show/Interoperability
- https://stackoverflow.com/tags/fortran-iso-c-binding/info
- C/Fortran interoperability - https://pages.tacc.utexas.edu/~eijkhout/istc/html/language.html
- Designing a Modern C++/Fortran Interface by Example
	- FortranCon 2020; Maximilien Ambroise
	- https://www.youtube.com/watch?v=5h0qHCVnfHI
	- https://tcevents.chem.uzh.ch/event/12/contributions/47/
- Shroud: generate Fortran and Python wrappers for C and C++ libraries
	- https://github.com/LLNL/shroud
	- FortranCon 2020; Lee Taylor
		- https://tcevents.chem.uzh.ch/event/12/contributions/30/
		- https://www.youtube.com/watch?v=1mdI-M94vDc
- SWIG-Fortran
	- https://github.com/swig-fortran
	- Flibcpp: Fortran bindings to the C++ Standard Library
		- https://github.com/swig-fortran/flibcpp
	- Automated Fortran–C++ Bindings for Large-Scale Scientific Applications
		- IDEAS-ECP Webinar 2021; Seth Johnson
		- https://www.exascaleproject.org/event/fortran-cpp-bindings/
		- https://www.youtube.com/watch?v=mC67NVuz6WI

---

# Haskell

- Calling C++ from Haskell - "The Hard Way"
	- https://wiki.haskell.org/CPlusPlus_from_Haskell
- Cxx foreign function interface
	- https://wiki.haskell.org/Cxx_foreign_function_interface
- fficxx - FFI to C++ in Haskell
	- Haskell-C++ Foreign Function Interface Generator
	- https://web.archive.org/http://ianwookim.org/fficxx/
	- https://github.com/wavewave/fficxx
- inline-c-cpp: Lets you embed C++ code into Haskell
	- http://hackage.haskell.org/package/inline-c-cpp
	- https://github.com/fpco/inline-c
- Stranger in a Strange Land: An introductory tour of the Haskell FFI
	- Haskell DC 2020; P.C. Shyamshankar
	- https://www.youtube.com/watch?v=zlOrYQH_-Xs

---

# Java

- GraalVM: JIT Compiler and Polyglot Runtime for the JVM
	- http://www.graalvm.org/
	- https://github.com/oracle/graal
	- Running C++ - http://www.graalvm.org/docs/reference-manual/languages/llvm/#running-c
	- Sulong, the LLVM bitcode implementation of Graal VM
		- With Sulong you can execute C/C++, Fortran, and other programming languages that can be transformed to LLVM bitcode on Graal VM.
		- https://github.com/graalvm/sulong
- JavaCPP: The missing bridge between Java and native C++
	- https://github.com/bytedeco/javacpp
- java-native-benchmark: Benchmarking Java's native call APIs: JNI, JNA, JNR, BridJ and Project Panama
	- https://github.com/zakgof/java-native-benchmark
- jni.hpp: a modern, type-safe, header-only, C++14 wrapper for JNI (Java Native Interface)
	- https://github.com/mapbox/jni.hpp
- jnr-ffi: Java Abstracted Foreign Function Layer
	- Java library for loading native libraries without writing JNI code by hand or using tools such as SWIG
	- https://github.com/jnr/jnr-ffi
- Native Interfaces: The Phantom Menace
	- NYJavaSIG, February 7, 2018
	- Tony Printezis - JVM Engineer - Twitter
	- JNI, Project Panama
	- https://www.eventbrite.com/e/nyjavasig-native-interfaces-the-phantom-menace-and-java-9-compatibility-tickets-42519931259#
	- https://www.youtube.com/watch?v=YxHb6kAGZ10
- Project Panama: Interconnecting JVM and native code
	- https://openjdk.java.net/projects/panama/
	- https://github.com/openjdk/panama-foreign
	- jextract: a tool which generates a Java API from one or more native C headers
		- Using Panama "foreign-jextract" JDK
			- https://github.com/openjdk/panama-foreign/blob/foreign-jextract/doc/panama_jextract.md
		- Panama jextract samples
			- https://github.com/sundararajana/panama-jextract-samples
	- Panama: A Foreign Policy for Java
		- Devoxx 2018; Maurizio Cimadamore
		- https://www.youtube.com/watch?v=cfxBrYud9KM
	- JEP 412: Foreign Function & Memory API (Incubator)
		- https://openjdk.java.net/jeps/412
		- A practical look at JEP-412 in JDK17 with libsodium
			- https://blog.arkey.fr/2021/09/04/a-practical-look-at-jep-412-in-jdk17-with-libsodium/
		- Finalizing the Foreign APIs
			- https://inside.java/2021/09/16/finalizing-the-foreign-apis/
	- Lifetimes in the Foreign Function & Memory API
		- 2023; Maurizio Cimadamore
		- https://cr.openjdk.java.net/~mcimadamore/panama/why_lifetimes.html
	- Project Panama: Foreign Function & Memory API
		- JVM Language Summit 2023
		- Maurizio Cimadamore
		- https://www.youtube.com/watch?v=kUFysMkMS00

---

# JavaScript

- Embind: Emscripten's tool to generate JavaScript bindings for C++ code
	- https://developers.google.com/web/updates/2018/08/embind
	- https://kripken.github.io/emscripten-site/docs/porting/connecting_cpp_and_javascript/embind.html
- Emmagic
	- Easily transport your data structures between C++ and Javascript
	- https://github.com/manaflair/emmagic
- nbind: a set of headers that make your C++11 library accessible from JavaScript.
	- https://github.com/charto/nbind
	- https://github.com/charto/nbind#readme
- v8pp: Bind C++ functions and classes into V8 JavaScript engine
	- https://github.com/pmed/v8pp

---

# Julia

- Cxx.jl: The Julia C++ Interface
	- https://github.com/Keno/Cxx.jl

---

# Lua

- Sol v2.0 - a C++ <-> Lua API
	- Sol is a C++ library binding to Lua. It currently supports all Lua versions 5.1+ (LuaJIT 2.x included). Sol aims to be easy to use and easy to add to a project. The library is header-only for easy integration with projects.
	- http://sol2.rtfd.org/
	- https://github.com/ThePhD/sol2
	- Scripting at the Speed of Thought: Lua and C++ with sol3 - CppCon 2018; JeanHeyd Meneide
		- https://www.youtube.com/watch?v=xQAmGBfKnas
- Using Lua with C++ (and C)
	- Elias Daler
	- 2023-02-14
	- https://edw.is/using-lua-with-cpp/

## Lua: Talks

- C++20 + Lua = Flexibility
	- ACCU 2021; James Pascoe
	- https://www.youtube.com/watch?v=ojph4RZvqqQ
	- https://accu.org/conf-docs/PDFs_2021/james_pascoe_cpp20_lua_flexibility.pdf
- Lua in the Stingray 3D game engine
	- Lua Workshop 2015; Niklas Frykholm
	- https://www.youtube.com/watch?v=wTjyM7d7_YA

---

# Nim

- Nim's FFI (foreign function interface)
	- https://nim-lang.org/docs/manual.html#foreign-function-interface
- ImportCpp pragma
	- https://nim-lang.org/docs/manual.html#implementation-specific-pragmas-importcpp-pragma
- Nim Backend Integration: Interfacing
	- https://nim-lang.org/docs/backends.html#interfacing
- c2nim
	- c2nim is a tool to translate Ansi C code to Nim. The output is human-readable Nim code that is meant to be tweaked by hand before and after the translation process.
	- https://github.com/nim-lang/c2nim

---

# Objective-C

- OC - Easily Declare/Invoke Objective-C APIs from C11 or C++11
	- Macro magic for declaring/calling Objective-C APIs from C11 or C++. Preloads selectors, chooses the correct objc_msgSend to call per method/platform.
	- https://github.com/garettbass/oc

---

# OCaml

- Foreign Function Interface - Real World OCaml
	- http://dev.realworldocaml.org/foreign-function-interface.html
- Interfacing C with OCaml
	- https://caml.inria.fr/pub/docs/manual-ocaml/intfc.html
- Duplo: A Framework for OCaml Post-Link Optimisation
	- [ICFP 2020](https://icfp20.sigplan.org/details/icfp-2020-papers/5/Duplo-A-Framework-for-OCaml-Post-Link-Optimisation)
	- Nandor Licker, Timothy M. Jones
	- https://www.cl.cam.ac.uk/~nl364/docs/duplo.pdf
	- LLIR (Low-Level Intermediate Representation) cross-language post-link optimiser for OCaml and C
		- https://github.com/nandor/llir-opt
- Melocoton: A Program Logic for Verified Interoperability Between OCaml and C
	- OOPSLA 2023
	- Armaël Guéneau, Johannes Hostert, Simon Spies, Michael Sammler, Lars Birkedal, Derek Dreyer
	- https://doi.org/10.1145/3622823
	- https://gallium.inria.fr/~agueneau/publis/melocoton.pdf
	- https://2023.splashcon.org/details/splash-2023-oopsla/57/Melocoton-A-Program-Logic-for-Verified-Interoperability-Between-OCaml-and-C
	- https://melocoton-project.github.io/
- cxx_wrapped.h
	- simple template to wrap C++ object as OCaml custom value (used for example in ocaml-hypertable)
	- https://github.com/ygrek/scraps/blob/master/cxx_wrapped.h

---

# PHP

- PHP++: C++11 Class wrap library for PHP7
	- https://github.com/phplang/p3

---

# Python

## Python: Readings

- Calling C functions from Python
	- part 1 - using ctypes - http://yizhang82.me/python-interop-ctypes
	- part 2 - writing CPython extensions using Python/C API - http://yizhang82.me/python-interop-capi
	- part 3 - deep dive into ctypes implementation in CPython
		- http://yizhang82.me/python-interop-inside-ctypes
		- https://blogs.msdn.microsoft.com/yizhang/2018/02/02/calling-c-functions-from-python-part-3-deep-dive-into-ctypes-implementation-in-cpython/
- Python - using C and C++ libraries with ctypes
	- https://solarianprogrammer.com/2019/07/18/python-using-c-cpp-libraries-ctypes/
- Toward Efficient Interactions between Python and Native Libraries
	- ESEC/FSE 2021
	- Jialiang Tan, Yu Chen, Zhenming Liu, Bin Ren, Shuaiwen Leon Song, Xipeng Shen, Xu Liu
	- https://arxiv.org/abs/2107.00064
- Towards Reliable Memory Management for Python Native Extensions
	- ICOOOLPS 2023 
	- Joannah Nanjekye, David Bremner, Aleksandar Micic
	- https://conf.researchr.org/details/ecoop-issta-2023/ICOOOLPS-2023/4/Towards-Reliable-Memory-Management-for-Python-Native-Extensions

## Python: Software

- cppyy: Python-C++ bindings interface based on Cling/LLVM
	- cppyy provides fully automatic, dynamic Python-C++ bindings by leveraging the Cling C++ interpreter and LLVM. It supports both PyPy (natively), CPython, and C++ language standards through C++17 (and parts of C++20).
	- https://github.com/wlav/cppyy
	- https://cppyy.readthedocs.io/
	- High-performance Python-C++ bindings with PyPy and Cling
		- PyHPC 2016
		- Wim T. L. P. Lavrijsen, Aditi Dutta
		- https://dl.acm.org/doi/10.5555/3019083.3019087
		- http://wlav.web.cern.ch/wlav/Cppyy_LavrijsenDutta_PyHPC16.pdf
- HPy: a better API for Python
	- https://hpyproject.org/
	- https://github.com/hpyproject/hpy
	- HPy: How To Design a C API For Optimizing Runtimes
		- Truffle 2022: Truffle/GraalVM Languages Workshop
		- Tim Felgentreff
		- https://www.youtube.com/watch?v=SSS9q3md3mA
		- https://2022.ecoop.org/details/truffle-2022/6/HPy-How-To-Design-a-C-API-For-Optimizing-Runtimes
- libpy: Utilities for writing C++ extension modules
	- https://github.com/quantopian/libpy
- nanobind: tiny and efficient C++/Python bindings
	- https://github.com/wjakob/nanobind
	- https://nanobind.readthedocs.io/en/latest/
- pybind11 — Seamless operability between C++11 and Python
	- https://github.com/pybind/pybind11
	- http://pybind11.readthedocs.io
	- pybind11 - seamless operability between C++11 and Python - EuroPython 2017; Ivan Smirnov
		- https://www.youtube.com/watch?v=jQedHfF1Jfw
	- Integrate Python and C++ with pybind11 - NDC 2018; Robert Smallshire
		- https://www.youtube.com/watch?v=YReJ3pSnNDo
- Wrappy: Wrapping python made easy
	- https://github.com/lava/wrappy

## Python: Talks

- Cython: Static Typing and C/C++ Interfacing in (C)Python
	- StockholmCpp; October 24, 2019; Arda Aytekin
	- https://www.youtube.com/watch?v=0R3fw7h64MY
- How and why to write Python binary extension modules using C++
	- SwedenCpp::Stockholm::0x0F, September 20, 2018; Thomas Nyberg
	- https://www.youtube.com/watch?v=LbiozBn9v6Y
	- https://github.com/ApproximateIdentity/cpp_extension_talk
- Writing Python Bindings for C++ Libraries for Performance and Ease of Use
	- CppNow 2023
	- Saksham Sharma
	- https://www.youtube.com/watch?v=2rJJfTt72Dk

---

# R

- Rcpp: Seamless R and C++ Integration
	- http://rcpp.org/
	- http://gallery.rcpp.org/
	- http://dirk.eddelbuettel.com/code/rcpp.html
	- http://dirk.eddelbuettel.com/presentations.html
	- http://adv-r.had.co.nz/Rcpp.html
	- Rcpp: Seamless R and C++ Integration - CppCon 2015: Matt P. Dziubinski
		- https://speakerdeck.com/mattpd/rcpp-seamless-r-and-c-plus-plus-integration-cppcon-2015
		- https://www.youtube.com/watch?v=xiqYaHa2x4s

---

# Rust

- Autocxx: a tool for calling C++ from Rust in a heavily automated but safe fashion
	- https://github.com/google/autocxx
- bindgen: Automatically generates Rust FFI bindings to C and C++ libraries
	- https://github.com/rust-lang/rust-bindgen
- cbindgen: creates C/C++11 headers for Rust libraries which expose a public C API
	- https://github.com/eqrion/cbindgen
	- cbindgen User Guide
		- https://github.com/eqrion/cbindgen/blob/master/docs.md
- Corrosion: lets you instantly start using Rust in any existing C and C++ project using CMake
	- a tool for integrating Rust into an existing CMake project; capable of importing executables, static libraries, and dynamic libraries from a crate.
	- https://github.com/AndrewGaspar/corrosion
- CXX: safe FFI between Rust and C++
	- https://github.com/dtolnay/cxx
- rustcxx: Using C++ from Rust made easy
	- https://github.com/google/rustcxx

## Rust: Readings

- Aliasing Limits on Translating C to Safe Rust
	- OOPSLA 2023
	- Mehmet Emre, Peter Boyland, Aesha Parekh, Ryan Schroeder, Kyle Dewey, Ben Hardekopf
	- https://2023.splashcon.org/details/splash-2023-oopsla/20/Aliasing-Limits-on-Translating-C-to-Safe-Rust

---

# Scheme

- SCHeMe UnterstüTZung — easy Guile Scheme C++ bindings
	- https://sinusoid.es/schmutz
	- https://github.com/arximboldi/schmutz

---

# Stata

- Stata commands for inline C++ code in do-files
	- https://github.com/robertgrant/statacpp

---

# Swift

- C++ Interoperability Workgroup
	- https://www.swift.org/cxx-interop-workgroup/
- Mixing Swift and C++
	- https://www.swift.org/documentation/cxx-interop/
- Vision Documents
	- Using C++ from Swift
		- https://github.com/apple/swift-evolution/blob/main/visions/using-c%2B%2B-from-swift.md
	- Using Swift from C++
		- https://github.com/apple/swift-evolution/blob/main/visions/using-swift-from-c%2B%2B.md

---

# WebAssembly

- Emscripten
	- Emscripten compiles C and C++ to WebAssembly using LLVM and Binaryen. Emscripten output can run on the Web, in Node.js, and in wasm runtimes.
	- https://emscripten.org/
	- https://github.com/emscripten-core/emscripten
- Sandbox Games: Using WebAssembly and C++ to make a simple game
	- CPPP 2021; Ólafur Waage
	- https://www.youtube.com/watch?v=Su9SfiGySFQ
	- https://github.com/CpppFr/CPPP-21/tree/main/webassembly-olafur_waage
- Typescripten: a compiler that creates C++ header files from TypeScript interface definitions
	- https://github.com/think-cell/typescripten
	- Typescripten: Generating type-safe JavaScript bindings for emscripten
		- CppNow 2022; Sebastian Theophil
		- https://www.youtube.com/watch?v=fOagTqBYHug

---

# Zig

- Zig In-depth Overview - Integration with C libraries without FFI/bindings
	- https://ziglang.org/learn/overview/#integration-with-c-libraries-without-ffibindings
- Zig Language Reference - C
	- https://ziglang.org/documentation/master/#C
- Zig Learn - Chapter 4 - Working with C
	- https://ziglearn.org/chapter-4/
