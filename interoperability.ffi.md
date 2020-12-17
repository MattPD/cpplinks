# [C++ links](README.md): interoperability - foreign function interfaces (FFIs)

# Contents

- [General](#general)
- Language-specific: [Bash](#bash), [C](#c), [C#](#c-1), [Common Lisp](#common-lisp), [D](#d), [Haskell](#haskell), [Java](#java), [JavaScript](#javascript), [Julia](#julia), [Lua](#lua), [Objective-C](#objective-c), [OCaml](#ocaml), [PHP](#php), [Python](#python), [R](#r), [Rust](#rust), [Scheme](#scheme), [Stata](#stata)

---

# General

- C++ Language Interface Foundation (CLIF)
	- https://github.com/google/clif
- libffi: A portable foreign-function interface library
	- http://sourceware.org/libffi
	- https://github.com/libffi/libffi
- Scapix Language Bridge
	- Automatic, on the fly bindings from C++ to Java, Objective-C, Swift, Python, JavaScript (WebAssembly), and C#. Bridge code automatically generated directly from C++ header files, no need to manually maintain IDL definitions or bindings.
	- https://github.com/scapix-com/scapix
- SWIG: Simplified Wrapper and Interface Generator
	- http://www.swig.org/

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
- The Salami Method
	- The Salami Method finely distinguishes between the different aspects and layers required for exposing platform-independent C++ on different “specific” platforms. At its extreme it strives to create a single, thin, transparent layer for each such aspect so that each layer is more easily built, tested, debugged, managed and maintained.
	- http://videocortex.io/2017/salami-method/
	- The Salami Method: multiplatform C++ development - Adi Shavit, CoreCpp IL Meetup, April 2018
		- https://www.youtube.com/watch?v=jdEmz3iXNlA
	- The Salami Method for Cross Platform Development - CppCon 2018; Adi Shavit
		- https://www.youtube.com/watch?v=ZSpGNiUvXVI

---

# C#

- CoreRTDemo: Building a native library in C# and calling it from C++
	- https://github.com/encrypt0r/CoreRTDemo
	- Writing Native Libraries in C# and using them in other languages
		- https://dev.to/encrypt0r/writing-native-libraries-in-c-3kl
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
- Panama: A Foreign Policy for Java
	- Devoxx 2018; Maurizio Cimadamore
	- https://www.youtube.com/watch?v=cfxBrYud9KM

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
- Lua in the Stingray 3D game engine - Niklas Frykholm - https://www.youtube.com/watch?v=wTjyM7d7_YA

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
- cxx_wrapped.h
	- simple template to wrap C++ object as OCaml custom value (used for example in ocaml-hypertable)
	- https://github.com/ygrek/scraps/blob/master/cxx_wrapped.h

---

# PHP

- PHP++: C++11 Class wrap library for PHP7
	- https://github.com/phplang/p3

---

# Python

- Calling C functions from Python
	- part 1 - using ctypes - http://yizhang82.me/python-interop-ctypes
	- part 2 - writing CPython extensions using Python/C API - http://yizhang82.me/python-interop-capi
	- part 3 - deep dive into ctypes implementation in CPython
		- http://yizhang82.me/python-interop-inside-ctypes
		- https://blogs.msdn.microsoft.com/yizhang/2018/02/02/calling-c-functions-from-python-part-3-deep-dive-into-ctypes-implementation-in-cpython/
- cppyy: Python-C++ bindings interface based on Cling/LLVM
	- https://bitbucket.org/wlav/cppyy
	- https://cppyy.readthedocs.io/
	- High-performance Python-C++ bindings with PyPy and Cling
		- PyHPC 2016
		- Wim T. L. P. Lavrijsen, Aditi Dutta
		- https://dl.acm.org/doi/10.5555/3019083.3019087
		- http://wlav.web.cern.ch/wlav/Cppyy_LavrijsenDutta_PyHPC16.pdf
- Cython: Static Typing and C/C++ Interfacing in (C)Python
	- StockholmCpp; October 24, 2019; Arda Aytekin
	- https://www.youtube.com/watch?v=0R3fw7h64MY
- How and why to write Python binary extension modules using C++
	- SwedenCpp::Stockholm::0x0F, September 20, 2018; Thomas Nyberg
	- https://www.youtube.com/watch?v=LbiozBn9v6Y
	- https://github.com/ApproximateIdentity/cpp_extension_talk
- pybind11 — Seamless operability between C++11 and Python
	- https://github.com/pybind/pybind11
	- http://pybind11.readthedocs.io
	- pybind11 - seamless operability between C++11 and Python - EuroPython 2017; Ivan Smirnov
		- https://www.youtube.com/watch?v=jQedHfF1Jfw
	- Integrate Python and C++ with pybind11 - NDC 2018; Robert Smallshire
		- https://www.youtube.com/watch?v=YReJ3pSnNDo
- Python - using C and C++ libraries with ctypes
	- https://solarianprogrammer.com/2019/07/18/python-using-c-cpp-libraries-ctypes/
- Wrappy: Wrapping python made easy
	- https://github.com/lava/wrappy

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
- CXX: safe FFI between Rust and C++
	- https://github.com/dtolnay/cxx
- rustcxx: Using C++ from Rust made easy
	- https://github.com/google/rustcxx

---

# Scheme

- SCHeMe UnterstüTZung — easy Guile Scheme C++ bindings
	- https://sinusoid.es/schmutz
	- https://github.com/arximboldi/schmutz

---

# Stata

- Stata commands for inline C++ code in do-files
	- https://github.com/robertgrant/statacpp
