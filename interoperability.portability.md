# [C++ links](README.md): interoperability - portability: libraries, ABI, name mangling

# Contents

- [General](#general): [Readings](#readings), [Software](#software), [Talks](#talks)
- [ABI](#abi): [Readings](#readings-1), [Software](#software-1), [Talks](#talks-1)
- [Name Mangling](#name-mangling): [Readings](#readings-2), [Software](#software-2), [Talks](#talks-2)

---

# General

## Readings

- Beautiful Native Libraries
	- http://lucumr.pocoo.org/2013/8/18/beautiful-native-libraries/
- C++ compiler support - http://en.cppreference.com/w/cpp/compiler_support
- Compiler Dependencies - https://isocpp.org/wiki/faq/compiler-dependencies
- Creating and using shared libraries with different compilers on different operating systems
	- http://gernotklingler.com/blog/creating-using-shared-libraries-different-compilers-different-operating-systems/
- GotW #100: Compilation Firewalls - https://herbsutter.com/gotw/_100/
- GotW #101: Compilation Firewalls, Part 2 - https://herbsutter.com/gotw/_101/
- How to Write Shared Libraries - Ulrich Drepper - http://www.akkadia.org/drepper/dsohowto.pdf
- Interoperability of Libraries Created by Different Compiler Brands
	- http://www.mingw.org/wiki/Interoperability_of_Libraries_Created_by_Different_Compiler_Brands
- libabc
	- http://0pointer.de/blog/projects/libabc
	- https://git.kernel.org/pub/scm/linux/kernel/git/kay/libabc.git/about/
- PImpl - http://en.cppreference.com/w/cpp/language/pimpl
- Program Library HOWTO
	- This HOWTO for programmers discusses how to create and use program libraries on Linux. This includes static libraries, shared libraries, and dynamically loaded libraries.
	- http://tldp.org/HOWTO/Program-Library-HOWTO/
- [SEI CERT C Coding Standard](https://wiki.sei.cmu.edu/confluence/pages/viewpage.action?pageId=87151973)
	- [MSC14-C. Do not introduce unnecessary platform dependencies](https://wiki.sei.cmu.edu/confluence/display/c/MSC14-C.+Do+not+introduce+unnecessary+platform+dependencies)
	- [MSC15-C. Do not depend on undefined behavior](https://wiki.sei.cmu.edu/confluence/display/c/MSC15-C.+Do+not+depend+on+undefined+behavior)
	- [MSC23-C. Beware of vendor-specific library and language differences](https://wiki.sei.cmu.edu/confluence/display/c/MSC23-C.+Beware+of+vendor-specific+library+and+language+differences)
- Understanding GCC Builtins to Develop Better Tools
	- ESEC/FSE 2019
	- Manuel Rigger, Stefan Marr, Bram Adams, Hanspeter Mössenböck
	- https://arxiv.org/abs/1907.00863
	- https://github.com/jku-ssw/gcc-builtin-study

## Software

- Hedley
	- a single C/C++ header you can include in your project to enable compiler-specific features while retaining compatibility with all compilers. It contains dozens of macros to help make your code easier to use, harder to misuse, safer, faster, and more portable.
	- https://nemequ.github.io/hedley/
	- https://github.com/nemequ/hedley
- Portable Snippets
	- a collection of public domain (CC0) code snippets written in C for performing various common tasks which are typically OS, architecture, and/or compiler-dependent. 
	- https://github.com/nemequ/portable-snippets

## Talks

- Making a Language Cross Platform: Libraries and Tooling
	- 2019 LLVM Developers’ Meeting; Gwen Mittertreiner
	- https://www.youtube.com/watch?v=bdiQM0IPMio
	- http://llvm.org/devmtg/2019-10/slides/Mittertreiner-MakingALanguageCrossPlatform.pdf
- Naivety of Creating Cross-Platform, Modern C++ Libraries: A Tour Of Our Challenges and Successes
	- CppCon 2017; Jonathan Henson
	- https://www.youtube.com/watch?v=JPdohAomZD8
- Intro to the C++ Object Model
	- CppCon 2015; Richard Powell
	- https://www.youtube.com/watch?v=iLiDezv_Frk&list=PLgpRclL8uN4xjpYqslYJlX2H1hRukN_Qr

---

# ABI

## Readings

- `[[trivial_abi]]` 101
	- https://quuxplusone.github.io/blog/2018/05/02/trivial-abi-101/
- ABI Policy and Guidelines - The GNU C++ Library Manual
	- https://gcc.gnu.org/onlinedocs/libstdc++/manual/abi.html
- ABIs, linkers and other animals - Stephen Kell (2014)
	- https://www.cl.cam.ac.uk/~srk31/research/talks/kell14abis-slides.pdf
- Binary Compatibility Examples
	- https://community.kde.org/Policies/Binary_Compatibility_Examples
- Binary Compatibility Issues With C++
	- https://community.kde.org/Policies/Binary_Compatibility_Issues_With_C%2B%2B
- Binary Compatibility of Shared Libraries Implemented in C++ on GNU/Linux Systems
	- SYRCoSE 2009; Pavel Shved, Denis Silakov
	- http://syrcose.ispras.ru/2009/files/02_paper.pdf
	- http://static.coldattic.info/restricted/science/syrcose09/cppbincomp.pdf
- Binary-compatible C++ Interfaces - https://chadaustin.me/cppinterface.html
- C++ Standards Committee Papers
	- ABI breakage - summary of initial comments
		- 2019; Roger Orr
		- http://wg21.link/P1654
	- What is ABI, and What Should WG21 Do About It?
		- 2020; Titus Winters
		- http://wg21.link/P2028
- C++: Under the Hood (March 1994) by Jan Gray
	- http://files.rsdn.org/4539/cud94.htm
	- https://blogs.msdn.microsoft.com/xiangfan/2012/02/06/c-under-the-hood/
	- https://www.openrce.org/articles/files/jangrayhood.pdf
- Calling conventions for different C++ compilers and operating systems
	- http://www.agner.org/optimize/calling_conventions.pdf
- Describing the MSVC ABI for Structure Return Types
	- http://blog.aaronballman.com/2012/02/describing-the-msvc-abi-for-structure-return-types/
- How C array sizes become part of the binary interface of a library
	- https://developers.redhat.com/blog/2019/05/06/how-c-array-sizes-become-part-of-the-binary-interface-of-a-library/
- Itanium C++ ABI
	- https://itanium-cxx-abi.github.io/cxx-abi/
	- https://github.com/itanium-cxx-abi/cxx-abi
- Some thoughts on binary compatibility - http://blog.qt.io/blog/2009/08/12/some-thoughts-on-binary-compatibility/
- Some thoughts on calling convention - http://blog.qt.io/blog/2009/08/15/some-thoughts-on-calling-convention/
- The Importance of Calling Conventions - http://blog.aaronballman.com/2011/04/the-importance-of-calling-conventions/
- The value of passing by value - https://www.macieira.org/blog/2012/02/the-value-of-passing-by-value/
- X86-64 System V Application Binary Interface
	- https://github.com/hjl-tools/x86-psABI/wiki/X86-psABI

## Software

- ABI Compliance Checker (ABICC)
	- A tool for checking backward API/ABI compatibility of a C/C++ library
	- https://lvc.github.io/abi-compliance-checker/
	- https://github.com/lvc/abi-compliance-checker
	- http://ispras.linuxbase.org/index.php/ABI_compliance_checker
	- How to check for ABI changes with abi compliance checker - https://fedoraproject.org/wiki/How_to_check_for_ABI_changes_with_abi_compliance_checker
- ABI Dumper
	- A tool to dump ABI of an ELF object containing DWARF debug info
	- https://github.com/lvc/abi-dumper
- ABIGAIL: Application Binary Interface Generic Analysis and Instrumentation Library
	- abidiff - compares the Application Binary Interfaces (ABI) of two shared libraries in ELF format
		- https://sourceware.org/libabigail/manual/abidiff.html
	- abidw - reads a shared library in ELF format and emits an XML representation of its ABI to standard output
		- https://sourceware.org/libabigail/manual/abidw.html
	- abicompat - checks that an application that links against a given shared library is still ABI compatible with a subsequent version of that library
		- https://sourceware.org/libabigail/manual/abicompat.html
	- Comparing ABIs for Compatibility with libabigail – Part 1 - https://developers.redhat.com/blog/2014/10/23/comparing-abis-for-compatibility-with-libabigail-part-1/
	- Comparing ABIs for Compatibility with libabigail – Part 2 - https://developers.redhat.com/blog/2014/10/28/comparing-abis-for-compatibility-libabigail-part-2/
	- Pruning Dynamic Rebuilds With libabigail
		- https://engineering.mongodb.com/post/pruning-dynamic-rebuilds-with-libabigail
		- https://github.com/acmorrow/abilink-demo
	- Talk: Libabigail: How semantic analysis of C and C++ ELF binaries can be used to analyze ABI changes (openSUSE Conference 2017)
		- https://media.ccc.de/v/1234-libabigail-how-semantic-analysis-of-c-and-c-elf-binaries-can-be-used-to-analyze-abi-changes
		- https://www.youtube.com/watch?v=wxVBuZK8Dl0
- pexcheck: Pexcheck is a command-line tool for checking the binary compatibility of public interfaces.
	- https://github.com/AVGTechnologies/pexcheck

## Talks

- Analyzing changes to the binary interface exposed by the Kernel to its modules
	- Kernel Recipes 2019; Dodji Seketeli, Matthias Männich, Jessica Yu
	- https://kernel-recipes.org/en/2019/talks/analyzing-changes-to-the-binary-interface-exposed-by-the-kernel-to-its-modules/
- API & ABI versioning
	- Meeting C++ 2017; Mathieu Ropert
	- https://www.youtube.com/watch?v=k9PLRAnnEmE
- Binary compatibility for library developers
	- C++Now 2013; Thiago Macieira
	- https://www.youtube.com/watch?v=PHrXGHDd9no
	- https://github.com/boostcon/cppnow_presentations_2013/blob/master/tue/binary_compat_for_cpp_devs.pdf?raw=true
- Easy Binary Compatible C++ Interfaces Across Compilers
	- C++Now 2013; John Bandela
	- https://www.youtube.com/watch?v=BbbqBJ94-_E
	- PDF: https://github.com/boostcon/cppnow_presentations_2013/blob/master/tue/easy_binary_compat.pdf?raw=true
	- PPT: https://github.com/boostcon/cppnow_presentations_2013/blob/master/tue/easy_binary_compat.ppt?raw=true
	- https://jrb-programming.blogspot.com/2012/12/easy-binary-compatible-interfaces.html
	- https://github.com/jbandela/cppcomponents
	- https://github.com/jbandela/cross_compiler_call
- How to break an ABI and keep your users happy
	- CppCon 2017; Gennadiy Rozental
	- https://www.youtube.com/watch?v=NzaYUlAw93k
	- https://abseil.io/blog/20171023-cppcon-breaking-abi
- Linux User/Kernel ABI: the realities of how C and C++ programs really talk to the OS
	- ACCU 2018; Greg Law
	- https://www.youtube.com/watch?v=4CdmGxc5BpU
- Reversing C++
	- Black Hat USA 2007; Paul Vincent Sabanal, Mark Vincent Yason
	- https://www.blackhat.com/presentations/bh-dc-07/Sabanal_Yason/Presentation/bh-dc-07-Sabanal_Yason.pdf
	- https://www.blackhat.com/presentations/bh-dc-07/Sabanal_Yason/Paper/bh-dc-07-Sabanal_Yason-WP.pdf
	- Videos:
		- https://archive.org/details/2007_BlackHat_Vegas-V72-Yason-Sabanal-Reversing_C
		- https://www.youtube.com/watch?v=oJ3mOzD7rC8
		- 00: https://www.youtube.com/watch?v=Vy0z1baCh8s
		- 01: https://www.youtube.com/watch?v=1wZ615YlMFs
		- 02: https://www.youtube.com/watch?v=dcoNjUn_ACI
		- 03: https://www.youtube.com/watch?v=JZ8_QM-XM1k
- The ABI challenge
	- C++Now 2019; Arvid Norberg
	- https://www.youtube.com/watch?v=ncyQAjTyPwU
- The C++ ABI From the Ground Up
	- CppCon 2019; Louis Dionne
	- https://www.youtube.com/watch?v=DZ93lP1I7wU
- What's an ABI and why is it so complicated?
	- ACCU 2015; Jonathan Wakely
	- https://accu.org/content/conf2015/JonathanWakely-What%20Is%20An%20ABI%20And%20Why%20Is%20It%20So%20Complicated.pdf

---

# Name Mangling

## Readings

- Measuring Mangled Name Ambiguity in Large C / C++ Projects
	- SQAMIA 2017
	- Richárd Szalay, Zoltán Porkoláb, Dániel Krupp
	- https://www.researchgate.net/publication/320923382_Measuring_Mangled_Name_Ambiguity_in_Large_C_C_Projects
	- http://ceur-ws.org/Vol-1938/paper-sza.pdf
- Towards Better Symbol Resolution for C/C++ Programs: A Cluster-Based Solution
	- Source Code Analysis and Manipulation (SCAM) 2017
	- Richárd Szalay, Zoltán Porkoláb, Dániel Krupp
	- http://ieeexplore.ieee.org/document/8090143/
	- https://www.researchgate.net/publication/320832497_Towards_Better_Symbol_Resolution_for_CC_Programs_A_Cluster-Based_Solution

## Software

- c++filtjs: c++filt in JavaScript with Emscripten
	- https://d.fuqu.jp/c++filtjs/
	- https://github.com/nattofriends/c-filtjs
- C++ Itanium ABI demangler: C++ demangler in Python that converts the mangled name into an AST
	- https://github.com/whitequark/binja_itanium_cxx_abi/blob/master/demangler.py
- cppmangle: A library for demangling and mangling Visual Studio C++ names
	- https://github.com/AVGTechnologies/cppmangle
- cpp_demangle: A crate for demangling C++ symbols
	- https://github.com/gimli-rs/cpp_demangle
- Demangler: A C++ library and tools for demangling mangled C++ names
	- https://github.com/avast-tl/demangler
	- https://github.com/avast-tl/retdec/tree/master/src/demangler
	- https://github.com/avast-tl/retdec/tree/master/tests/demangler
- demumble: A better c++filt and a better undname.exe, in one binary.
	- demumble demangles both POSIX and Visual Studio symbols. It runs on both POSIX and Windows.
	- https://github.com/nico/demumble
- GCC and MSVC C++ Demangler - http://demangler.com/

## Talks

- C++ Weekly - Ep 8 C++ Name Demangling - https://www.youtube.com/watch?v=uX99t7GmuDc
