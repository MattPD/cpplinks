# [C++ links](README.md): interoperability - foreign function interfaces (FFIs)

# Contents

* [General](#general)
* Language-specific: [C](#c), [C#](#c-1), [Common Lisp](#common-lisp), [D](#d), [Haskell](#haskell), [Java](#java), [JavaScript](#javascript), [Julia](#julia), [Lua](#lua), [PHP](#php), [Python](#python), [R](#r), [Rust](#rust), [Scheme](#scheme), [Stata](#stata)

---

# General

* C++ Language Interface Foundation (CLIF)
	+ https://github.com/google/clif
* libffi: A portable foreign-function interface library
	+ http://sourceware.org/libffi
	+ https://github.com/libffi/libffi
* SWIG: Simplified Wrapper and Interface Generator
	+ http://www.swig.org/

# C

* C handler wrapping in C++ - https://arekmd.github.io/wrapping-c-handlers/
* CppCon 2014: Lisa Lippincott "How to call C libraries from C++"
	+ https://www.youtube.com/watch?v=3ZO0V4Prefc
	+ https://github.com/CppCon/CppCon2014/tree/master/Presentations/How%20to%20call%20C%20libraries%20from%20C%2B%2B
	+ Code and slides from Lisa Lippincott's “How to Call C libraries from C++” presentation from Cppcon 2014
	+ https://github.com/jfirebaugh/PlusPlus
* Cross-language interfaces between C and C++ - https://gustedt.wordpress.com/2017/08/08/cross-language-interfaces-between-c-and-c/
* DragonFFI: C Foreign Function Interface and JIT using Clang/LLVM
	+ DragonFFI is a C Foreign Function Interface (FFI) library written in C++ and based on Clang/LLVM. It allows any language to call C functions thought the provided APIs and bindings.
	+ https://github.com/aguinet/dragonffi/
	+ FOSDEM 2018 - https://fosdem.org/2018/schedule/event/dragonffi/
	+ DragonFFI: FFI/JIT for the C language using Clang/LLVM - http://blog.llvm.org/2018/03/dragonffi-ffijit-for-c-language-using.html
* Hourglass Interfaces for C++ APIs - CppCon 2014
	+ https://www.slideshare.net/StefanusDuToit/cpp-con-2014-hourglass-interfaces-for-c-apis
	+ https://www.youtube.com/watch?v=PVYdHDm0q6Y
	+ https://github.com/CppCon/CppCon2014/tree/master/Presentations/Hourglass%20Interfaces%20for%20C%2B%2B%20APIs
* The Salami Method
	+ The Salami Method finely distinguishes between the different aspects and layers required for exposing platform-independent C++ on different “specific” platforms. At its extreme it strives to create a single, thin, transparent layer for each such aspect so that each layer is more easily built, tested, debugged, managed and maintained.
	+ http://videocortex.io/2017/salami-method/
	+ The Salami Method: multiplatform C++ development - Adi Shavit, CoreCpp IL Meetup, April 2018
		- https://www.youtube.com/watch?v=jdEmz3iXNlA

# C#

* CppSharp
	+ Tools and libraries to glue C/C++ APIs to high-level languages
	+ https://github.com/mono/CppSharp
* The .NET Inter-Operability Operation
	+ Derbycon 2017; James Forshaw
	+ http://www.irongeek.com/i.php?page=videos/derbycon7/s13-the-net-inter-operability-operation-james-forshaw

# Common Lisp

* Clasp — Bringing Common Lisp and C++ Together
	+ https://github.com/drmeister/clasp

# D

* Zero Overhead Interface Between DLang & C++ Standard Lib
	+ Alexandru Razvan Caciulescu | DConf2017
	+ https://www.youtube.com/watch?v=c5zGnOWKaGo

# Haskell

* Calling C++ from Haskell - "The Hard Way"
	+ https://wiki.haskell.org/CPlusPlus_from_Haskell
* Cxx foreign function interface
	+ https://wiki.haskell.org/Cxx_foreign_function_interface
* fficxx - FFI to C++ in Haskell
	+ Haskell-C++ Foreign Function Interface Generator
	+ http://ianwookim.org/fficxx/
	+ https://github.com/wavewave/fficxx
* inline-c-cpp: Lets you embed C++ code into Haskell
	+ http://hackage.haskell.org/package/inline-c-cpp
	+ https://github.com/fpco/inline-c

# Java

* GraalVM: JIT Compiler and Polyglot Runtime for the JVM
	+ http://www.graalvm.org/
	+ https://github.com/oracle/graal
	+ Running C++ - http://www.graalvm.org/docs/reference-manual/languages/llvm/#running-c
	+ Sulong, the LLVM bitcode implementation of Graal VM
		- With Sulong you can execute C/C++, Fortran, and other programming languages that can be transformed to LLVM bitcode on Graal VM.
		- https://github.com/graalvm/sulong
* JavaCPP: The missing bridge between Java and native C++
	+ https://github.com/bytedeco/javacpp
* jnr-ffi: Java Abstracted Foreign Function Layer
	+ Java library for loading native libraries without writing JNI code by hand or using tools such as SWIG
	+ https://github.com/jnr/jnr-ffi
* Native Interfaces: The Phantom Menace
	+ NYJavaSIG, February 7, 2018
	+ Tony Printezis - JVM Engineer - Twitter
	+ JNI, Project Panama
	+ https://www.eventbrite.com/e/nyjavasig-native-interfaces-the-phantom-menace-and-java-9-compatibility-tickets-42519931259#
	+ https://www.youtube.com/watch?v=YxHb6kAGZ10

# JavaScript

* Embind: Emscripten's tool to generate JavaScript bindings for C++ code
	+ https://developers.google.com/web/updates/2018/08/embind
	+ https://kripken.github.io/emscripten-site/docs/porting/connecting_cpp_and_javascript/embind.html
* Emmagic
	+ Easily transport your data structures between C++ and Javascript
	+ https://github.com/manaflair/emmagic
* nbind: a set of headers that make your C++11 library accessible from JavaScript.
	+ https://github.com/charto/nbind
	+ https://github.com/charto/nbind#readme

# Julia

* Cxx.jl: The Julia C++ Interface
	+ https://github.com/Keno/Cxx.jl

# Lua

* Sol v2.0 - a C++ <-> Lua API
	+ Sol is a C++ library binding to Lua. It currently supports all Lua versions 5.1+ (LuaJIT 2.x included). Sol aims to be easy to use and easy to add to a project. The library is header-only for easy integration with projects.
	+ http://sol2.rtfd.org/
	+ https://github.com/ThePhD/sol2
* Lua in the Stingray 3D game engine - Niklas Frykholm - https://www.youtube.com/watch?v=wTjyM7d7_YA

# PHP

* PHP++: C++11 Class wrap library for PHP7
	+ https://github.com/phplang/p3

# Python

* Calling C functions from Python
	+ part 1 - using ctypes - http://yizhang82.me/python-interop-ctypes
	+ part 2 - writing CPython extensions using Python/C API - http://yizhang82.me/python-interop-capi
	+ part 3 - deep dive into ctypes implementation in CPython
		- http://yizhang82.me/python-interop-inside-ctypes
		- https://blogs.msdn.microsoft.com/yizhang/2018/02/02/calling-c-functions-from-python-part-3-deep-dive-into-ctypes-implementation-in-cpython/
* cppyy: Automatic Python-C++ bindings
	+ https://cppyy.readthedocs.io/
* pybind11 — Seamless operability between C++11 and Python
	+ https://github.com/pybind/pybind11
	+ http://pybind11.readthedocs.io
* Wrappy: Wrapping python made easy
	+ https://github.com/lava/wrappy

# R

* Rcpp: Seamless R and C++ Integration
	+ http://rcpp.org/
	+ http://gallery.rcpp.org/
	+ http://dirk.eddelbuettel.com/code/rcpp.html
	+ http://dirk.eddelbuettel.com/presentations.html
	+ http://adv-r.had.co.nz/Rcpp.html
	+ Rcpp: Seamless R and C++ Integration - CppCon 2015: Matt P. Dziubinski
		- https://speakerdeck.com/mattpd/rcpp-seamless-r-and-c-plus-plus-integration-cppcon-2015
		- https://www.youtube.com/watch?v=xiqYaHa2x4s

# Rust

* bindgen: Automatically generates Rust FFI bindings to C and C++ libraries
	+ https://github.com/rust-lang-nursery/rust-bindgen
* rustcxx: Using C++ from Rust made easy
	+ https://github.com/google/rustcxx

# Scheme

* SCHeMe UnterstüTZung — easy Guile Scheme C++ bindings
	+ https://sinusoid.es/schmutz
	+ https://github.com/arximboldi/schmutz

# Stata

* Stata commands for inline C++ code in do-files
	+ https://github.com/robertgrant/statacpp
