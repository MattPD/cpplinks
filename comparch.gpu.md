# [C++ links](README.md): computer architecture - GPU

See also: [computer architecture](comparch.md)

---

# Articles & Papers

- A closer look at GPUs
	- CACM 2008
	- Fatahalian, K., & Houston, M.
	- http://graphics.stanford.edu/~kayvonf/papers/fatahalianCACM.pdf
- AMD’s Cayman GPU Architecture - http://www.realworldtech.com/cayman/
- Benchmarking the cost of thread divergence in CUDA - https://arxiv.org/abs/1504.01650
- Broadcom VideoCore IV GPU
	- Life of a Triangle - https://latchup.blogspot.com/2016/02/life-of-triangle.html
	- VideoCore QPU Pipeline - https://latchup.blogspot.com/2016/03/videocore-qpu-pipeline.html
- Demystifying GPU Microarchitecture through Microbenchmarking - http://www.eecg.toronto.edu/~myrto/gpuarch-ispass2010.pdf - microbenchmark suite: http://www.stuffedcow.net/research/cudabmk
- GPU Concurrency: Weak Behaviours and Programming Assumptions
	- Architectural Support for Programming Languages and Operating Systems (ASPLOS) 2015
	- Alglave, J.; Batty, M.; Donaldson, A. F.; Gopalakrishnan, G.; Ketema, J.; Poetzl, D.; Sorensen, T.; and Wickerson, J.
	- http://johnwickerson.github.io/papers/gpuconcurrency.pdf
	- http://multicore.doc.ic.ac.uk/gpu-litmus/
- GPU Performance Modeling and Optimization - Ang Li
	- https://pure.tue.nl/ws/files/39759895/20161018_Li.pdf
- GPUs and the Future of Parallel Computing
	- IEEE Micro 31(5) 2011
	- Stephen W. Keckler, William J. Dally, Brucek Khailany, Michael Garland, David Glasco
	- http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.232.1574&rep=rep1&type=pdf
- HAXWell - Joshua Barczak
	- Code which loads custom ISA on Intel Haswell GPUs - https://github.com/jbarczak/HAXWell
	- You Compiled This, Driver. Trust Me… - http://www.joshbarczak.com/blog/?p=1028
	- SPMD Is Not Intel’s Cup Of Tea - http://www.joshbarczak.com/blog/?p=1120
	- GPU Ray Tracing The Wrong Way - http://www.joshbarczak.com/blog/?p=1197
- Inside Fermi: Nvidia’s HPC Push - http://www.realworldtech.com/fermi/
- Intel Processor Graphics: Microarchitecture and ISA, Tutorial, MICRO 2016
	- Microarchitecture: https://software.intel.com/sites/default/files/managed/89/92/Intel-Graphics-Architecture-ISA-and-microarchitecture.pdf
	- ISA: https://software.intel.com/sites/default/files/managed/89/92/micro-2016-ISA-tutorial.pdf
- Low-Level GPU Documentation - http://renderingpipeline.com/graphics-literature/low-level-gpu-documentation/
- NVIDIA Tesla: A Unified Graphics and Computing Architecture
	- IEEE Micro 2008
	- Lindholm, E., Nickolls, J., Oberman, S., & Montrym, J.
	- http://people.cs.umass.edu/~emery/classes/cmpsci691st/readings/Arch/gpu.pdf
- NVIDIA’s GT200: Inside a Parallel Processor - http://www.realworldtech.com/gt200/
- Patterson, Hennessy (2016): _Computer Organization and Design: The Hardware/Software Interface ARM Edition_ - Appendix B Graphics and Computing GPUs - http://booksite.elsevier.com/9780128017333/content/Appendix%20B.pdf
- Performance Analysis and Tuning for General Purpose Graphics Processing Units (GPGPU)
	- H. Kim, R. Vuduc, S. Baghsorkhi, J. Choi, W.-m. Hwu, 2012.
	- http://impact.crhc.illinois.edu/shared/papers/sara2012.pdf
	- http://impact.crhc.illinois.edu/paper_details.aspx?paper_id=203
- Predicting AMD and Nvidia GPU Performance - http://www.realworldtech.com/amd-nvidia-gpu-performance/
- Understanding Latency Hiding on GPUs
	- Vasily Volkov; EECS Department; University of California, Berkeley; Technical Report No. UCB/EECS-2016-143; August 12, 2016
	- https://www2.eecs.berkeley.edu/Pubs/TechRpts/2016/EECS-2016-143.html
- Understanding the GPU Microarchitecture to Achieve Bare-Metal Performance Tuning (PPoPP 2017)
	- http://dl.acm.org/citation.cfm?id=3018755
	- https://github.com/PAA-NCIC/PPoPP2017_artifact

---

# Communication

## Communication: Readings

### Communication: Readings: 2025

- Collective Communication for 100k+ GPUs
	- 2025
	- https://arxiv.org/abs/2510.20171
	- Connecting 100k+ GPUs
		- SIGCOMM'25: Meta Sponsor Talk
		- https://www.youtube.com/watch?v=pTu3AdfppyY
- Demystifying NCCL: An In-depth Analysis of GPU Communication Protocols and Algorithms
	- 32nd Annual Symposium on High-Performance Interconnects (HOTI) 2025
	- Zhiyi Hu, Siyuan Shen, Tommaso Bonato, Sylvain Jeaugey, Cedell Alexander, Eric Spada, James Dinan, Jeff Hammond, Torsten Hoefler
	- https://arxiv.org/abs/2507.04786
	- https://spcl.inf.ethz.ch/Publications/index.php?pub=554
	- https://www.youtube.com/watch?v=UDCLvBqEPcA

### Communication: Readings: 2024

- The Landscape of GPU-Centric Communication
	- 2024
	- Didem Unat, Ilyas Turimbetov, Mohammed Kefah Taha Issa, Doğan Sağbili, Flavio Vella, Daniele De Sensi, Ismayil Ismayilov
	- https://arxiv.org/abs/2409.09874

## Communication: Software

### Communication: Software: AMD

- ROCm Communication Collectives Library (RCCL)
	- a stand-alone library that provides multi-GPU and multi-node collective communication primitives optimized for AMD GPUs
	- https://github.com/ROCm/rccl
	- https://rocmdocs.amd.com/projects/rccl/

### Communication: Software: NVIDIA

- NCCL: NVIDIA Collective Communications Library
	- Optimized primitives for collective multi-GPU communication
	- https://github.com/NVIDIA/nccl
	- https://developer.nvidia.com/nccl
- NVSHMEM: NVIDIA OpenSHMEM Library
	- https://github.com/NVIDIA/nvshmem
	- https://developer.nvidia.com/nvshmem
	- https://docs.nvidia.com/nvshmem/

## Communication: Talks

- Landscape of GPU-Centric Communication
	- GPU MODE Lecture 68 (2025)
	- Didem Unat
	- https://www.youtube.com/watch?v=beuOWBbiJfQ
- Multi-GPU Programming
	- GPU MODE Lecture 64 (2025)
	- Markus Hrywniak
	- https://www.youtube.com/watch?v=BgeFR4UfajQ
- Multi-GPU Programming in NCCL and NVSHMEM
	- GPU MODE Lecture 67 (2025)
	- Jeff Hammond
	- https://www.youtube.com/watch?v=zxGVvMN6WaM
	- https://drive.google.com/file/d/1T8uHhFIeVa_g1oYb_O4d2Ltb8YQly1zK/view
	- https://github.com/ParRes/Kernels/tree/main/Cxx11

---

# CUDA

## CUDA: Books

- Wilt (2013) "The CUDA Handbook: A Comprehensive Guide to GPU Programming"
	- http://www.cudahandbook.com/
	- Chapter 8 (Streaming Multiprocessors) sample chapter: [HTML](http://www.informit.com/articles/article.aspx?p=2103809) [PDF](http://ptgmedia.pearsoncmg.com/images/9780321809469/samplepages/0321809467.pdf)

## CUDA: Courses

- Intro to Parallel Programming
	- https://classroom.udacity.com/courses/cs344
	- https://www.youtube.com/playlist?list=PLAwxTw4SYaPnFKojVQrmyOGFCqHTxfdv2

## CUDA: Documentation

- CUDA C Programming Guide - http://docs.nvidia.com/cuda/cuda-c-programming-guide/
- CUDA C Best Practices Guide - http://docs.nvidia.com/cuda/cuda-c-best-practices-guide/
- CUDA Toolkit Documentation - http://docs.nvidia.com/cuda/

## CUDA: Readings

- How to Optimize a CUDA Matmul Kernel for cuBLAS-like Performance: a Worklog
	- 2022; Simon Boehm
	- https://siboehm.com/articles/22/CUDA-MMM

## CUDA: Software

- NVBench: CUDA Kernel Benchmarking Library
	- https://github.com/NVIDIA/nvbench

## CUDA: Talks

### CUDA: Talks: 2021

- CUDA Memory Model
	- CUDA Community Meetup Group 2021-01-04
	- Georgy Evtushenko
	- https://www.youtube.com/watch?v=VJ1QLrmfQws
	- https://github.com/CUDACommunity/CUDACommunityMeetup2021/tree/master/CUDAMemoryModel
- The CUDA C++ Standard Library
	- Meeting C++ 2021
	- Bryce Adelstein Lelbach
	- https://www.youtube.com/watch?v=-ENnYEWezKo

---

# Open Source Hardware GPU Projects

- GPLGPU
	- https://github.com/asicguy/gplgpu
	- https://latchup.blogspot.com/2016/07/gplgpu-walkthrough.html
- MIAOW
	- An open source GPU based off of the AMD Southern Islands ISA.
	- http://miaowgpu.org/
	- https://github.com/VerticalResearchGroup/miaow
	- https://github.com/VerticalResearchGroup/miaow/wiki
	- MIAOW Architecture Whitepaper [https://raw.githubusercontent.com/wiki/VerticalResearchGroup/miaow/files/MIAOW_Architecture_Whitepaper.pdf]
- Nyuzi Processor
	- Nyuzi is an experimental multicore GPGPU processor. It supports vector floating point, hardware multithreading, virtual memory, and cache coherence. The SystemVerilog-based hardware implementation is synthesizable and runs on FPGA. This project also includes an LLVM-based C++ toolchain.
	- https://github.com/jbush001/NyuziProcessor
	- https://github.com/jbush001/NyuziProcessor/wiki
- ORGFXSoC: ORSoC Graphics Accelerator
	- An example implementation of Open Source Graphics Accelerator (a fixed point, fixed function pipeline GPU).
	- https://github.com/maidenone/ORGFXSoC
	- http://opencores.org/project,orsoc_graphics_accelerator
- Theia GPU Overview - http://opencores.org/project,theia_gpu
- tiny-gpu
	- A minimal GPU implementation in Verilog optimized for learning about how GPUs work from the ground up.
	- Built with <15 files of fully documented Verilog, complete documentation on architecture & ISA, working matrix addition/multiplication kernels, and full support for kernel simulation & execution traces.
	- https://github.com/adam-maj/tiny-gpu

---

# Performance

## Performance: Optimization

- Optimization Techniques for GPU Programming
	- ACM Computing Surveys 2022
	- Pieter Hijma, Stijn Heldens, Alessio Sclocco, Ben Van Werkhoven, Henri Bal
	- https://dl.acm.org/doi/10.1145/3570638

---

# Software

- GPU Vendor/Programming Model Compatibility Table
	- 2022, JSC Accelerating Devices Lab Blog
	- Andreas Herten
	- https://doi.org/10.34732/xdvblg-r1bvif
	- https://x-dev.pages.jsc.fz-juelich.de/2022/11/02/gpu-vendor-model-compat.html
	- https://github.com/AndiH/gpu-lang-compat
- PerfTest: GPU texture/buffer performance tester
	- A simple GPU shader memory operation performance test tool. Current implementation is DirectX 11.0 based.
	- https://github.com/sebbbi/perftest
- Pyramid Shader Analyzer
	- Pyramid is a free, open GUI tool for offline shader validation and analysis. The UI takes HLSL or GLSL as input, and runs them through various shader compilers and static analyzers.
	- https://github.com/jbarczak/Pyramid

## Simulators

- Barra - NVIDIA GPU Architecture Simulator
	- http://gforge.inria.fr/plugins/mediawiki/wiki/barra/
	- http://homepages.dcc.ufmg.br/~sylvain.collange/papers/CoDaDePa_MASCOTS2010.pdf
- GPGPU-Sim
	- http://www.gpgpu-sim.org/
	- https://github.com/gpgpu-sim/gpgpu-sim_distribution
	- http://gpgpu-sim.org/manual/
		- http://gpgpu-sim.org/manual/index.php/Main_Page#Microarchitecture_Model
		- http://gpgpu-sim.org/manual/index.php/Main_Page#Visualizing_High-Level_GPGPU-Sim_Microarchitecture_Behavior
		- http://gpgpu-sim.org/manual/index.php/Main_Page#Visualizing_Cycle_by_Cycle_Microarchitecture_Behavior
	- http://www.gpgpu-sim.org/micro2012-tutorial/
	- using Docker containers - https://socal-ucr.github.io/GPGPU-sim-container/
- Integrated gem5 + GPGPU-Sim Simulator
	- http://cpu-gpu-sim.ece.wisc.edu/
	- gem5-gpu: A Heterogeneous CPU-GPU Simulator
		- IEEE Computer Architecture Letters 14(1) 2015
		- J. Power, J. Hestness, M.S. Orr, M.D. Hill, D.A. Wood
		- http://ieeexplore.ieee.org/document/6709764/
		- https://www.researchgate.net/publication/274858518_Gem5-gpu_A_heterogeneous_CPU-GPU_simulator
- MacSim
	- A cycle-level, heterogeneous architecture simulator for x86 and NVIDIA PTX instructions.
	- http://comparch.gatech.edu/hparch/macsim.html
	- https://github.com/gthparch/macsim
- Multi2Sim: A Heterogeneous System Simulator
	- http://www.multi2sim.org/
	- https://github.com/Multi2Sim/multi2sim

---

# Talks

- GPU Architectures and New Programming Model Features
	- Argonne Training Program in Extreme Scale Computing (ATPESC) 2016
	- Nikolai Sakharnykh, NVIDIA
	- video: https://www.youtube.com/watch?v=CWYx0HZ0zYM
	- slides: http://press3.mcs.anl.gov/atpesc/files/2016/08/Sakharnykn_145aug1GPU_architecture.pdf
- Introduction to GPU Architecture and Programming Models
	- Argonne Training Program in Extreme Scale Computing (ATPESC) 2018
	- Tim Warburton, Virginia Tech
	- video: https://www.youtube.com/watch?v=uvVy3CqpVbM&index=4&list=PLGj2a3KTwhRa6Ux64xg5L5ga6Jg8QykoQ
	- examples: https://github.com/tcew/ATPESC18
	- slides: http://extremecomputingtraining.anl.gov/files/2018/08/ATPESC_2018_Track-2_3_8-2_830am_Warburton-Accelerators.pdf
- Portable GPU Programming: Hands-on
	- Argonne Training Program in Extreme Scale Computing (ATPESC) 2016
	- Tim Warburton, Virginia Tech
	- video: https://www.youtube.com/watch?v=I33WSjcvfpI
