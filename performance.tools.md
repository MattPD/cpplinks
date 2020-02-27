# [C++ links](README.md): performance tools

# Contents

- [Benchmarking](#benchmarking)
- [Memory](#memory):
	- [Memory - Benchmarking](#memory---benchmarking)
	- [Memory - Profiling](#memory---profiling)
- [Microarchitecture](#microarchitecture)
- [Optimization](#optimization)
- [Profiling](#profiling)
- [Timing](#timing)
- [Visualization](#visualization)

---

# Benchmarking

## Software

- benchmark (Google)
	- https://github.com/google/benchmark
	- https://opensource.googleblog.com/2014/01/introducing-benchmark.html
- Celero
	- https://github.com/DigitalInBlue/Celero
- hayai: the C++ benchmarking framework
	- https://github.com/nickbruun/hayai
- moodycamel::microbench
	- https://github.com/cameron314/microbench
- geiger: A micro benchmark library in C++ that supports hardware performance counters
	- https://github.com/david-grs/geiger
- Nonius: A C++ micro-benchmarking framework
	- https://github.com/libnonius/nonius

## Readings

- Examples:
	- http://www.bfilipek.com/2016/01/micro-benchmarking-libraries-for-c.html
	- http://www.bfilipek.com/2016/02/revisiting-old-benchmark-vector-of.html
	- http://www.bfilipek.com/2016/05/google-benchmark-library.html
- Systems Benchmarking Crimes - Gernot Heiser - https://www.cse.unsw.edu.au/~gernot/benchmarking-crimes.html

# Memory

## Memory - Benchmarking

- Intel Memory Latency Checker (MLC)
	- a tool used to measure memory latencies and bandwidth, and how they change with increasing load on the system
	- https://www.intel.com/software/mlc
- Memory Bandwidth Benchmark
	- MBW determines the "copy" memory bandwidth available to userspace programs. Its simplistic approach models that of real applications. It is not tuned to extremes and it is not aware of hardware architecture, just like your average software package.
	- https://github.com/raas/mbw
- pmbw: Parallel Memory Bandwidth Benchmark / Measurement
	- a set of assembler routines to measure the parallel memory (cache and RAM) bandwidth of modern multi-core machines
	- http://panthema.net/2013/pmbw/
	- https://github.com/bingmann/pmbw
- Spatter: Benchmark for measuring the performance of sparse and irregular memory access
	- https://github.com/hpcgarage/spatter
	- Spatter: A Tool for Evaluating Gather / Scatter Performance
		- https://arxiv.org/abs/1811.03743
- STREAM: Sustainable Memory Bandwidth in High Performance Computers
	- http://www.cs.virginia.edu/stream/
	- STREAM benchmark - https://github.com/jeffhammond/STREAM
	- NUMA-STREAM - https://github.com/larsbergstrom/NUMA-STREAM
	- BabelStream: STREAM, for lots of devices written in many programming models
		- https://github.com/UoB-HPC/BabelStream
		- http://uob-hpc.github.io/BabelStream/
- tinymembench: simple benchmark for memory throughput and latency
	- https://github.com/ssvb/tinymembench

## Memory - Profiling

- Heaptrack - A Heap Memory Profiler for Linux
	- https://github.com/KDE/heaptrack
	- http://milianw.de/blog/heaptrack-a-heap-memory-profiler-for-linux
	- https://www.kdab.com/heaptrack-v1-0-0-release/
- How to Write a Heap Memory Profiler
	- CppCon 2019; Milian Wolff
	- https://www.youtube.com/watch?v=YB0QoWI-g8E
	- Slides & code: https://github.com/milianw/how-to-write-a-memory-profiler
- MALT & NUMAPROF: Memory Profiling for HPC Applications
	- NUMAPROF: a NUMA memory profiler based on Pintool to track remote memory accesses
		- https://memtt.github.io/numaprof
		- https://github.com/memtt/numaprof
	- MALT: a MALloc Tracker to find where and how your made your memory allocations in C/C++/Fortran applications
		- https://memtt.github.io/malt/
		- https://github.com/memtt/malt
	- MALT: A Malloc Tracker
		- International Workshop on Software Engineering for Parallel Systems (SEPS) 2017
		- Sébastien Valat, Andres S. Charif-Rubial, William Jalby
		- paper: https://memtt.github.io/malt/downloads/2017-seps-malt.pdf
		- slides: https://svalat.github.io/docs/2017-10-MALT-SEPS17.pdf
	- FOSDEM 2019; Sébastien Valat
		- https://www.youtube.com/watch?v=TnMOjdIy_Ow
		- https://fosdem.org/2019/schedule/event/numaprof/
- Memoro: A Detailed Heap Profiler
	- https://epfl-vlsc.github.io/memoro/
	- https://github.com/epfl-vlsc/memoro
	- Detailed Heap Profiling
		- International Symposium on Memory Management (ISMM) 2018
		- Stuart Byma, Jim Larus
		- https://dl.acm.org/citation.cfm?id=3210564
	- Memoro: Scaling an LLVM-based Heap profiler
		- 2019 LLVM Developers’ Meeting; Thierry Treyer
		- https://www.youtube.com/watch?v=fm47XsATelI
		- https://llvm.org/devmtg/2019-10/slides/Treyer-Memoro.pdf
- memory-profiler: A memory profiler for Linux
	- https://github.com/nokia/memory-profiler
- memtrail: A LD_PRELOAD based memory profiler and leak detector for Linux
	- ​https://github.com/jrfonseca/memtrail
- memusage - profile memory usage of a program
	- http://man7.org/linux/man-pages/man1/memusage.1.html
- MTuner - a C/C++ memory profiler and memory leak finder for Windows, PlayStation 4, PlayStation 3, etc.
	- https://milostosic.github.io/MTuner/
	- https://github.com/milostosic/MTuner
- PerfMemPlus: A Tool for Automatic Discovery of Memory Performance Problems
	- Tool for memory performance analysis based on Linux perf.
	- https://github.com/helchr/perfMemPlus
	- PerfMemPlus: A Tool for Automatic Discovery of Memory Performance Problems
		- ISC 2019
		- Christian Helm, Kenjiro Taura
		- https://doi.org/10.1007/978-3-030-20656-7_11
	- On the Correct Measurement of Application Memory Bandwidth and Memory Access Latency
		- HPC Asia 2020
		- Christian Helm, Kenjiro Taura
		- https://doi.org/10.1145/3368474.3368476
- Typegrind
	- a type preserving heap profiler for C++ - collects memory allocation information with type information
	- https://typegrind.github.io/
	- https://github.com/typegrind/typegrind
- Valgrind
	- http://valgrind.org/
	- DHAT: a dynamic heap analysis tool - http://valgrind.org/docs/manual/dh-manual.html
	- Massif: a heap profiler - ​http://valgrind.org/docs/manual/ms-manual.html

# Microarchitecture

- Tools for microarchitectural benchmarking
	- https://dendibakh.github.io/blog/2018/04/03/Tools-for-microarchitectural-benchmarking
- asmbench: A Benchmark Toolkit for Assembly Instructions Using the LLVM JIT
	- https://github.com/RRZE-HPC/asmbench
	- OoO Instruction Benchmarking Framework on the Back of Dragons
		- 2018 SC18 ACM SRC Poster
		- J. Hammer, G. Hager, G. Wellein
		- https://sc18.supercomputing.org/proceedings/src_poster/src_poster_pages/spost115.html
- BHive: A Benchmark Suite and Measurement Framework for Validating x86-64 Basic Block Performance Models
	- IISWC 2019
	- Yishen Chen, Ajay Brahmakshatriya, Charith Mendis, Alex Renda, Eric Atkinson, Ondrej Sykora, Saman Amarasinghe, Michael Carbin 
	- http://groups.csail.mit.edu/commit/papers/19/ithemal-measurement.pdf
	- https://github.com/ithemal/bhive
- Intel Architecture Code Analyzer (IACA)
	- https://software.intel.com/en-us/articles/intel-architecture-code-analyzer
- ibench: Measure instruction latency and throughput
	- https://github.com/hofm/ibench
- Ithemal: Instruction THroughput Estimator using MAchine Learning
	- https://github.com/psg-mit/Ithemal
	- Ithemal: Accurate, Portable and Fast Basic Block Throughput Estimation using Deep Neural Networks
		- ICML 2019
		- Charith Mendis, Alex Renda, Saman Amarasinghe, Michael Carbin 
		- https://arxiv.org/abs/1808.07412
		- http://proceedings.mlr.press/v97/mendis19a.html
- llvm-exegesis – LLVM Machine Instruction Benchmark
	- https://llvm.org/docs/CommandGuide/llvm-exegesis.html
	- https://github.com/llvm-mirror/llvm/tree/master/tools/llvm-exegesis
	- Static Performance Analysis with LLVM
		- 2018 European LLVM Developers Meeting
		- C. Courbet, O. Sykora, G. Chatelet, B. De Backer
		- https://youtu.be/XinMk-t8N-w
		- http://llvm.org/devmtg/2018-04/slides/Courbet-Static%20Performance%20Analysis%20with%20LLVM.pdf
	- Measuring x86 instruction latencies with LLVM
		- 2018 European LLVM Developers Meeting
		- G. Chatelet, C. Courbet, B. De Backer, O. Sykora
		- https://youtu.be/ex_C27OoApI
		- http://llvm.org/devmtg/2018-04/slides/Chatelet-Measuring%20x86%20instruction%20latencies%20with%20LLVM.pdf
- llvm-mca - LLVM Machine Code Analyzer
	- https://llvm.org/docs/CommandGuide/llvm-mca.html
	- https://github.com/llvm-mirror/llvm/tree/master/tools/llvm-mca
	- Understanding the performance of code using LLVM's Machine Code Analyzer (llvm-mca)
		- 2018 LLVM Developers’ Meeting; Andrea Di Biagio & Matt Davis
		- https://www.youtube.com/watch?v=Ku2D8bjEGXk
	- MC Ruler: Seamless llvm-mca CMake integration
		- https://github.com/jeremyong/mc_ruler
- nanoBench: A tool for running small microbenchmarks on recent Intel and AMD x86 CPUs
	- used for running the microbenchmarks for obtaining the latency, throughput, and port usage data available on http://uops.info
	- https://github.com/andreas-abel/nanoBench
	- https://uops.info/
	- nanoBench Cache Analyzer
		- https://github.com/andreas-abel/nanoBench/tree/master/tools/CacheAnalyzer
		- https://uops.info/cache.html
	- uops.info: Characterizing Latency, Throughput, and Port Usage of Instructions on Intel Microarchitectures
		- ASPLOS 2019
		- Andreas Abel, Jan Reineke
		- https://arxiv.org/abs/1810.04610
	- nanoBench: A Low-Overhead Tool for Running Microbenchmarks on x86 Systems
		- 2019; Andreas Abel, Jan Reineke
		- https://arxiv.org/abs/1911.03282
- Open Power/Performance Analysis Tool (OPPAT)
	- a cross-OS, cross-architecture Power and Performance Analysis Tool
	- cross-OS: supports Windows ETW trace files and Linux/Android perf/trace-cmd trace files
	- cross-architecture: supports Intel and ARM chips hardware events (using perf and/or PCM)
	- https://patinnc.github.io/
	- https://github.com/patinnc/oppat
- OSACA: Open Source Architecture Code Analyzer
	- https://github.com/RRZE-HPC/osaca
	- https://hpc.fau.de/research/tools/
	- Automated Instruction Stream Throughput Prediction for Intel and AMD Microarchitectures
		- Performance Modeling, Benchmarking and Simulation of High Performance Computer Systems (PMBS) 2018
		- Jan Laukemann, Julian Hammer, Johannes Hofmann, Georg Hager, Gerhard Wellein
		- https://arxiv.org/abs/1809.00912
	- Automatic Throughput and Critical Path Analysis of x86 and ARM Assembly Kernels
		- arXiv 2019
		- Jan Laukemann, Julian Hammer, Georg Hager, Gerhard Wellein
		- https://arxiv.org/abs/1910.00214
		- https://github.com/RRZE-HPC/OSACA-CP-2019
	- Cross-Architecture Automatic Critical Path Detection For In-Core Performance Analysis
		- 2020 Master Thesis; Jan Laukemann
		- https://hpc.fau.de/files/2020/02/Masterarbeit_JL-_final.pdf
		- Measurements and reproducibility instructions
			- https://github.com/RRZE-HPC/OSACA-Artifact-Appendix
- timing-harness: Harness for profiling arbitrary basic blocks.
	- https://github.com/ithemal/timing-harness
- uarch-bench: A benchmark for low-level CPU micro-architectural features
	- https://github.com/travisdowns/uarch-bench

# Optimization

- BOLT: Binary Optimization and Layout Tool
	- A linux command-line utility used for optimizing performance of binaries
	- https://github.com/facebookincubator/BOLT
	- Accelerate large-scale applications with BOLT
		- https://code.fb.com/data-infrastructure/accelerate-large-scale-applications-with-bolt/
	- Building Binary Optimizer with LLVM
		- 2016 EuroLLVM Developers' Meeting; Maksim Panchenko
		- https://llvm.org/devmtg/2016-03/Presentations/BOLT_EuroLLVM_2016.pdf
		- https://www.youtube.com/watch?v=gw3iDO3By5Y
	- BOLT: A Practical Binary Optimizer for Data Centers and Beyond
		- Maksim Panchenko, Rafael Auler, Bill Nell, Guilherme Ottoni
		- https://arxiv.org/abs/1807.06735
- MAQAO (Modular Assembly Quality Analyzer and Optimizer)
	- http://www.maqao.org/
	- http://maqao.bordeaux.inria.fr/

# Profiling

- Agner Fog's test programs for measuring clock cycles and performance monitoring
	- http://www.agner.org/optimize/#testp
- BCC - Tools for BPF-based Linux IO analysis, networking, monitoring, and more 
	- https://iovisor.github.io/bcc/
	- https://github.com/iovisor/bcc
	- https://github.com/iovisor/bpf-docs
	- http://www.brendangregg.com/blog/2016-03-05/linux-bpf-superpowers.html
	- http://www.brendangregg.com/blog/2016-03-28/linux-bpf-bcc-road-ahead-2016.html
	- http://www.brendangregg.com/blog/2016-06-14/ubuntu-xenial-bcc-bpf.html
	- https://qmonnet.github.io/whirl-offload/2016/09/01/dive-into-bpf/
- Coz: Finding Code that Counts with Causal Profiling
	- https://github.com/plasma-umass/coz/
	- Charlie Curtsinger, Emery Berger
	- SOSP 2015
		- https://www.sigops.org/sosp/sosp15/current/2015-Monterey/printable/090-curtsinger.pdf
	- ;login: 41(2) (2016)
		- https://www.usenix.org/publications/login/summer2016/curtsinger
	- Performance Matters - Strange Loop 2019; Emery Berger
		- https://www.youtube.com/watch?v=r-TLSBdHe1A
	- Coz vs. Sampling Profilers
		- https://easyperf.net/blog/2020/02/26/coz-vs-sampling-profilers
- easy_profiler: Lightweight cross-platform profiler library for C++
	- https://github.com/yse/easy_profiler
- Event Tracing for Windows (ETW) / Windows Performance Toolkit – Xperf
	- https://blogs.msdn.microsoft.com/ntdebugging/2008/04/03/windows-performance-toolkit-xperf/
	- ETW Central: https://randomascii.wordpress.com/2015/09/24/etw-central/
- gperftools (originally Google Performance Tools)
	- "The fastest malloc we’ve seen; works particularly well with threads and STL. Also: thread-friendly heap-checker, heap-profiler, and cpu-profiler."
	- https://github.com/gperftools/gperftools
- gprof2dot
	- "Python script to convert the output from many profilers into a dot graph."
	- https://github.com/jrfonseca/gprof2dot
- HawkTracer
	- a highly portable, low-overhead, configurable profiling tool for getting performance metrics from low-end devices
	- Linux, Windows, macOS; C & C++ library; Python & Rust wrappers
	- https://www.hawktracer.org/
	- https://github.com/amzn/hawktracer
	- Low-end platform profiling with HawkTracer profiler
		- FOSDEM 2020; Marcin Kolny
		- https://fosdem.org/2020/schedule/event/debugging_hawktrace/
- Hotspot - the Linux perf GUI for performance analysis
	- https://www.kdab.com/hotspot-gui-linux-perf-profiler/
	- https://github.com/KDAB/hotspot
	- https://www.kdab.com/hotspot-video/
- Likwid: Performance monitoring and benchmarking suite
	- https://github.com/RRZE-HPC/likwid
	- https://github.com/RRZE-HPC/likwid/wiki
	- https://github.com/RRZE-HPC/likwid/wiki/TutorialStart
	- https://github.com/RRZE-HPC/likwid/wiki/likwid-perfctr
	- https://github.com/RRZE-HPC/likwid/wiki/TutorialMarkerC
	- https://github.com/RRZE-HPC/likwid/wiki/PatternsHaswellEP
- microprofile: an embeddable profiler
	- https://github.com/jonasmr/microprofile
- Optick: C++ Profiler For Games
	- https://github.com/bombomby/optick
	- https://optick.dev/
- perf
	- https://perf.wiki.kernel.org/
	- http://www.brendangregg.com/perf.html
	- https://github.com/torvalds/linux/tree/master/tools/perf/Documentation
	- https://suchakra.wordpress.com/2016/06/17/deconstructing-perfs-data-file/
	- http://www.brendangregg.com/linuxperf.html
- perf-tools - https://github.com/brendangregg/perf-tools
- perf_events: The Unofficial Linux Perf Events Web-Page
	- http://web.eece.maine.edu/~vweaver/projects/perf_events/
- perfmon2 - http://perfmon2.sourceforge.net/
	- "Perfmon2 aims to be a portable interface across all modern processors. It is designed to give full access to a given PMU and all the corresponding hardware performance counters. Typically the PMU hardware implementations use a different number of registers, counters with different length and possibly other unique features, a complexity that the software has to cope with. Although processors have different PMU implementations, they usually use configurations registers and data registers. Perfmon2 provides a uniform abstract model of these registers and exports read/write operations accordingly."
- Performance Application Programming Interface (PAPI)
	- http://icl.cs.utk.edu/papi/
	- http://icl.cs.utk.edu/projects/papi/wiki/Main_Page
	- http://www.drdobbs.com/tools/performance-monitoring-with-papi/184406109
	- papi-wrapper (C++ library) - https://github.com/sean-chester/papi-wrapper
	- libpapipp: A C++ wrapper around libpapi - https://github.com/david-grs/papipp
- pmu tools: Intel PMU profiling tools
	- https://github.com/andikleen/pmu-tools
	- https://github.com/andikleen/pmu-tools/wiki/toplev-manual
	- pmu-tools part I - introduction, ocperf - http://halobates.de/blog/p/245
	- pmu-tools part II - toplev - http://halobates.de/blog/p/262
- Processor Counter Monitor (PCM)
	- https://github.com/opcm/pcm
	- Intel Performance Counter Monitor (PCM) - http://www.intel.com/software/pcm
- Remotery: Single C file, Realtime CPU/GPU Profiler with Remote Web Viewer
	- https://github.com/Celtoys/Remotery
- sysdig
	- https://github.com/draios/sysdig
	- https://sysdig.com/blog/50-shades-of-system-calls/
- Tracy Profiler
	- Tracy is a real time, nanosecond resolution frame profiler that can be used for remote or embedded telemetry of your application. It can profile CPU (C++, Lua), GPU (OpenGL, Vulkan) and memory. It also can display locks held by threads and their interactions with each other.
	- https://bitbucket.org/wolfpld/tracy
	- Introduction to the Tracy profiler - https://www.youtube.com/watch?v=fB5B46lbapc

# Timing

- low-overhead-timers: Very low-overhead timer/counter interfaces for C on Intel 64 processors
	- https://github.com/jdmccalpin/low-overhead-timers
	- Comments on timing short code sections on Intel processors
		- http://sites.utexas.edu/jdm4372/2018/07/23/comments-on-timing-short-code-sections-on-intel-processors/

# Visualization

- Flame Graphs
	- http://www.brendangregg.com/flamegraphs.html
	- http://queue.acm.org/detail.cfm?id=2927301
- FlameScope: a visualization tool for exploring different time ranges as Flame Graphs
	- https://github.com/Netflix/flamescope
	- Netflix FlameScope - https://medium.com/@NetflixTechBlog/netflix-flamescope-a57ca19d47bb
- pprof - a tool for visualization and analysis of profiling data
	- https://github.com/google/pprof
