# [C++ links](README.md): computer architecture - GPU

Note: see also [computer architecture](comparch.md)

# Articles & Papers

* A closer look at GPUs. Fatahalian, K., & Houston, M. (2008) CACM - http://graphics.stanford.edu/~kayvonf/papers/fatahalianCACM.pdf
* AMD’s Cayman GPU Architecture - http://www.realworldtech.com/cayman/
* Benchmarking the cost of thread divergence in CUDA - https://arxiv.org/abs/1504.01650
* Broadcom VideoCore IV GPU
  - Life of a Triangle - https://latchup.blogspot.com/2016/02/life-of-triangle.html
  - VideoCore QPU Pipeline - https://latchup.blogspot.com/2016/03/videocore-qpu-pipeline.html
* Demystifying GPU Microarchitecture through Microbenchmarking - http://www.eecg.toronto.edu/~myrto/gpuarch-ispass2010.pdf - microbenchmark suite: http://www.stuffedcow.net/research/cudabmk
* GPU Concurrency: Weak Behaviours and Programming Assumptions  
  Alglave, J.; Batty, M.; Donaldson, A. F.; Gopalakrishnan, G.; Ketema, J.; Poetzl, D.; Sorensen, T.; and Wickerson, J. In 20th ACM Int. Conf. on Architectural Support for Programming Languages and Operating Systems (ASPLOS '15), 2015. Invited for fast-track submission to ACM Transactions on Computer Systems (TOCS).
  - http://johnwickerson.github.io/papers/gpuconcurrency.pdf
  - http://multicore.doc.ic.ac.uk/gpu-litmus/
* GPU Performance Modeling and Optimization - Ang Li
  - https://pure.tue.nl/ws/files/39759895/20161018_Li.pdf
* GPUs and the Future of Parallel Computing  
  Keckler et al., IEEE Micro 2011.
  - http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.232.1574&rep=rep1&type=pdf
  - https://www.computer.org/cms/Computer.org/ComputingNow/homepage/2011/1111/W_MI_GPUsandtheFutureofParallelComputing.pdf
* HAXWell - Joshua Barczak
  - Code which loads custom ISA on Intel Haswell GPUs - https://github.com/jbarczak/HAXWell
  - You Compiled This, Driver. Trust Me… - http://www.joshbarczak.com/blog/?p=1028
  - SPMD Is Not Intel’s Cup Of Tea - http://www.joshbarczak.com/blog/?p=1120
  - GPU Ray Tracing The Wrong Way - http://www.joshbarczak.com/blog/?p=1197
* Inside Fermi: Nvidia’s HPC Push - http://www.realworldtech.com/fermi/
* Intel Processor Graphics: Microarchitecture and ISA, Tutorial, MICRO 2016
  - Microarchitecture: https://software.intel.com/sites/default/files/managed/89/92/Intel-Graphics-Architecture-ISA-and-microarchitecture.pdf
  - ISA: https://software.intel.com/sites/default/files/managed/89/92/micro-2016-ISA-tutorial.pdf
* Low-Level GPU Documentation - http://renderingpipeline.com/graphics-literature/low-level-gpu-documentation/
* NVIDIA Tesla: A Unified Graphics and Computing Architecture  
  Lindholm, E., Nickolls, J., Oberman, S., & Montrym, J. (2008). Micro, IEEE.
  - http://people.cs.umass.edu/~emery/classes/cmpsci691st/readings/Arch/gpu.pdf
* NVIDIA’s GT200: Inside a Parallel Processor - http://www.realworldtech.com/gt200/
* Patterson, Hennessy (2016): _Computer Organization and Design: The Hardware/Software Interface ARM Edition_ - Appendix B Graphics and Computing GPUs - http://booksite.elsevier.com/9780128017333/content/Appendix%20B.pdf
* Performance Analysis and Tuning for General Purpose Graphics Processing Units (GPGPU)  
  H. Kim, R. Vuduc, S. Baghsorkhi, J. Choi, W.-m. Hwu, 2012.
  - http://impact.crhc.illinois.edu/shared/papers/sara2012.pdf
  - http://impact.crhc.illinois.edu/paper_details.aspx?paper_id=203
* Predicting AMD and Nvidia GPU Performance - http://www.realworldtech.com/amd-nvidia-gpu-performance/
* Understanding Latency Hiding on GPUs
  - Vasily Volkov; EECS Department; University of California, Berkeley; Technical Report No. UCB/EECS-2016-143; August 12, 2016
  - https://www2.eecs.berkeley.edu/Pubs/TechRpts/2016/EECS-2016-143.html
* Understanding the GPU Microarchitecture to Achieve Bare-Metal Performance Tuning (PPoPP 2017)
  - http://dl.acm.org/citation.cfm?id=3018755
  - https://github.com/PAA-NCIC/PPoPP2017_artifact

# CUDA

## CUDA Books

* Wilt (2013) "The CUDA Handbook: A Comprehensive Guide to GPU Programming"
  - http://www.cudahandbook.com/
  - Chapter 8 (Streaming Multiprocessors) sample chapter: [HTML](http://www.informit.com/articles/article.aspx?p=2103809) [PDF](http://ptgmedia.pearsoncmg.com/images/9780321809469/samplepages/0321809467.pdf)

## CUDA Courses

* Intro to Parallel Programming - https://www.udacity.com/course/intro-to-parallel-programming--cs344

## CUDA Documentation

* CUDA C Programming Guide - http://docs.nvidia.com/cuda/cuda-c-programming-guide/
* CUDA C Best Practices Guide - http://docs.nvidia.com/cuda/cuda-c-best-practices-guide/
* CUDA Toolkit Documentation - http://docs.nvidia.com/cuda/

# Open Source Hardware GPU Projects

* GPLGPU
  - https://github.com/asicguy/gplgpu
  - https://latchup.blogspot.com/2016/07/gplgpu-walkthrough.html
* MIAOW  
  An open source GPU based off of the AMD Southern Islands ISA. 
  - http://miaowgpu.org/
  - https://github.com/VerticalResearchGroup/miaow
  - https://github.com/VerticalResearchGroup/miaow/wiki
  - MIAOW Architecture Whitepaper [https://raw.githubusercontent.com/wiki/VerticalResearchGroup/miaow/files/MIAOW_Architecture_Whitepaper.pdf]
* Nyuzi Processor  
  Nyuzi is an experimental multicore GPGPU processor. It supports vector floating point, hardware multithreading, virtual memory, and cache coherence. The SystemVerilog-based hardware implementation is synthesizable and runs on FPGA. This project also includes an LLVM-based C++ toolchain.
  - https://github.com/jbush001/NyuziProcessor
  - https://github.com/jbush001/NyuziProcessor/wiki
* ORGFXSoC: ORSoC Graphics Accelerator  
  An example implementation of Open Source Graphics Accelerator (a fixed point, fixed function pipeline GPU).
  - https://github.com/maidenone/ORGFXSoC
  - http://opencores.org/project,orsoc_graphics_accelerator
* Theia GPU Overview - http://opencores.org/project,theia_gpu

# Talks

* An Introduction to Graphics Processing Unit Architecture and Programming Models  
  Tim Warburton, Virginia Tech - ATPESC16 (Argonne Training Program on Extreme-Scale Computing, Summer 2016)
  - https://www.youtube.com/watch?v=Uk4DtWkEFh4
* GPU Architectures and New Programming Model Features  
  Nikolai Sakharnykh, NVIDIA - ATPESC16 (Argonne Training Program on Extreme-Scale Computing, Summer 2016)
  - https://www.youtube.com/watch?v=CWYx0HZ0zYM
  - http://press3.mcs.anl.gov/atpesc/files/2016/08/Sakharnykn_145aug1GPU_architecture.pdf
* Portable GPU Programming: Hands-on  
  Tim Warburton, Virginia Tech - ATPESC16 (Argonne Training Program on Extreme-Scale Computing, Summer 2016)
  - https://www.youtube.com/watch?v=I33WSjcvfpI

# Software

* PerfTest: GPU texture/buffer performance tester  
  A simple GPU shader memory operation performance test tool. Current implementation is DirectX 11.0 based.
  - https://github.com/sebbbi/perftest
* Pyramid Shader Analyzer  
  Pyramid is a free, open GUI tool for offline shader validation and analysis. The UI takes HLSL or GLSL as input, and runs them through various shader compilers and static analyzers.
  - https://github.com/jbarczak/Pyramid

## Simulators

* Barra - NVIDIA GPU Architecture Simulator
  - http://gforge.inria.fr/plugins/mediawiki/wiki/barra/
  - http://homepages.dcc.ufmg.br/~sylvain.collange/papers/CoDaDePa_MASCOTS2010.pdf
* GPGPU-Sim
  - http://www.gpgpu-sim.org/
  - https://github.com/gpgpu-sim/gpgpu-sim_distribution
  - http://gpgpu-sim.org/manual/
    - http://gpgpu-sim.org/manual/index.php/Main_Page#Microarchitecture_Model
    - http://gpgpu-sim.org/manual/index.php/Main_Page#Visualizing_High-Level_GPGPU-Sim_Microarchitecture_Behavior
    - http://gpgpu-sim.org/manual/index.php/Main_Page#Visualizing_Cycle_by_Cycle_Microarchitecture_Behavior
  - http://www.gpgpu-sim.org/micro2012-tutorial/
  - using Docker containers - https://socal-ucr.github.io/GPGPU-sim-container/
* Integrated gem5 + GPGPU-Sim Simulator 
  + http://cpu-gpu-sim.ece.wisc.edu/
  + gem5-gpu: A Heterogeneous CPU-GPU Simulator
    - IEEE Computer Architecture Letters, 14(1), 2015
    - J. Power, J. Hestness, M.S. Orr, M.D. Hill, D.A. Wood
    - http://ieeexplore.ieee.org/document/6709764/
    - https://www.researchgate.net/publication/274858518_Gem5-gpu_A_heterogeneous_CPU-GPU_simulator
* MacSim  
  A cycle-level, heterogeneous architecture simulator for x86 and NVIDIA PTX instructions.
  - http://comparch.gatech.edu/hparch/macsim.html
  - https://github.com/gthparch/macsim
* Multi2Sim: A Heterogeneous System Simulator
  - http://www.multi2sim.org/
  - https://github.com/Multi2Sim/multi2sim
