# [C++ links](README.md): performance tools

# Benchmarking

* benchmark (Google)
  - https://github.com/google/benchmark
  - https://opensource.googleblog.com/2014/01/introducing-benchmark.html
* Celero
  - https://github.com/DigitalInBlue/Celero
* hayai - the C++ benchmarking framework
  - https://github.com/nickbruun/hayai
* moodycamel::microbench: https://github.com/cameron314/microbench
* geiger: A micro benchmark library in C++ that supports hardware performance counters: https://github.com/david-grs/geiger
* Nonius
  - https://nonius.io/

Examples:  
- http://www.bfilipek.com/2016/01/micro-benchmarking-libraries-for-c.html
- http://www.bfilipek.com/2016/02/revisiting-old-benchmark-vector-of.html
- http://www.bfilipek.com/2016/05/google-benchmark-library.html

Systems Benchmarking Crimes - Gernot Heiser - https://www.cse.unsw.edu.au/~gernot/benchmarking-crimes.html

# Optimization

* MAQAO (Modular Assembly Quality Analyzer and Optimizer)
  - http://www.maqao.org/
  - http://maqao.bordeaux.inria.fr/

# Profiling

* Agner Fog's test programs for measuring clock cycles and performance monitoring
http://www.agner.org/optimize/#testp

* BCC - Tools for BPF-based Linux IO analysis, networking, monitoring, and more 
  - https://iovisor.github.io/bcc/
  - https://github.com/iovisor/bcc
  - https://github.com/iovisor/bpf-docs
  - http://www.brendangregg.com/blog/2016-03-05/linux-bpf-superpowers.html
  - http://www.brendangregg.com/blog/2016-03-28/linux-bpf-bcc-road-ahead-2016.html
  - http://www.brendangregg.com/blog/2016-06-14/ubuntu-xenial-bcc-bpf.html
  - https://qmonnet.github.io/whirl-offload/2016/09/01/dive-into-bpf/

* Event Tracing for Windows (ETW) / Windows Performance Toolkit – Xperf
  - https://blogs.msdn.microsoft.com/ntdebugging/2008/04/03/windows-performance-toolkit-xperf/
  - ETW Central: https://randomascii.wordpress.com/2015/09/24/etw-central/

* gperftools (originally Google Performance Tools)  
  "The fastest malloc we’ve seen; works particularly well with threads and STL. Also: thread-friendly heap-checker, heap-profiler, and cpu-profiler."
  - https://github.com/gperftools/gperftools

* Intel Architecture Code Analyzer (IACA)
https://software.intel.com/en-us/articles/intel-architecture-code-analyzer

* Intel Performance Counter Monitor (PCM)
http://www.intel.com/software/pcm
https://intel-pcm-api-documentation.github.io/

* Likwid: Performance monitoring and benchmarking suite
  - https://github.com/RRZE-HPC/likwid
  - https://github.com/RRZE-HPC/likwid/wiki
  - https://github.com/RRZE-HPC/likwid/wiki/TutorialStart
  - https://github.com/RRZE-HPC/likwid/wiki/likwid-perfctr
  - https://github.com/RRZE-HPC/likwid/wiki/TutorialMarkerC
  - https://github.com/RRZE-HPC/likwid/wiki/PatternsHaswellEP

* perf
  - https://perf.wiki.kernel.org/
  - http://www.brendangregg.com/perf.html
  - https://github.com/torvalds/linux/tree/master/tools/perf/Documentation
  - https://suchakra.wordpress.com/2016/06/17/deconstructing-perfs-data-file/
  - http://www.brendangregg.com/linuxperf.html

* perf-tools
  - https://github.com/brendangregg/perf-tools

* perf_events: The Unofficial Linux Perf Events Web-Page
http://web.eece.maine.edu/~vweaver/projects/perf_events/

* perfmon2 - http://perfmon2.sourceforge.net/
  - "Perfmon2 aims to be a portable interface across all modern processors. It is designed to give full access to a given PMU and all the corresponding hardware performance counters. Typically the PMU hardware implementations use a different number of registers, counters with different length and possibly other unique features, a complexity that the software has to cope with. Although processors have different PMU implementations, they usually use configurations registers and data registers. Perfmon2 provides a uniform abstract model of these registers and exports read/write operations accordingly."

* Performance Application Programming Interface (PAPI)
  - http://icl.cs.utk.edu/papi/
  - http://icl.cs.utk.edu/projects/papi/wiki/Main_Page
  - http://www.drdobbs.com/tools/performance-monitoring-with-papi/184406109
  - papi-wrapper (C++ library) - https://github.com/sean-chester/papi-wrapper

* pmu tools: Intel PMU profiling tools 
- https://github.com/andikleen/pmu-tools
- https://github.com/andikleen/pmu-tools/wiki/toplev-manual
- pmu-tools part I - introduction, ocperf - http://halobates.de/blog/p/245
- pmu-tools part II - toplev - http://halobates.de/blog/p/262

* sysdig
  - https://github.com/draios/sysdig
  - https://sysdig.com/blog/50-shades-of-system-calls/

## Profiling - Memory

* Heaptrack - A Heap Memory Profiler for Linux Syndicate content
  - https://github.com/KDE/heaptrack
  - http://milianw.de/blog/heaptrack-a-heap-memory-profiler-for-linux

* memusage - profile memory usage of a program
  - http://man7.org/linux/man-pages/man1/memusage.1.html

* Typegrind  
  a type preserving heap profiler for C++ - collects memory allocation information with type information
  - https://typegrind.github.io/
  - https://github.com/typegrind/typegrind

# Visualization

* pprof - a tool for visualization and analysis of profiling data  
https://github.com/google/pprof

* Flame Graphs
  - http://www.brendangregg.com/flamegraphs.html
  - http://queue.acm.org/detail.cfm?id=2927301
