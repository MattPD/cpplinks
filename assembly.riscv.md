# [C++ links](README.md): RISC-V Assembly

Note: see [Computer Architecture](comparch.md) -- recommended background (which makes the following significantly more approachable) includes at least an undegraduate-level course.

# RISC-V Foundation

- https://riscv.org/
- https://github.com/riscv
- https://riscv.org/mailing-lists/
- https://riscv.org/category/workshops/proceedings/

---

## Articles

https://riscv.org/publications/

* An Agile Approach to Building RISC-V Microprocessors - https://people.eecs.berkeley.edu/~bora/Journals/2016/IEEEMicro16.pdf
* Design of the RISC-V Instruction Set Architecture - http://www.eecs.berkeley.edu/Pubs/TechRpts/2016/EECS-2016-1.html
* GRVI Phalanx: A Massively Parallel RISC-V FPGA Accelerator Accelerator - https://arxiv.org/abs/1606.01037
* How Genode came to RISC-V - https://genode.org/documentation/articles/riscv
* Instruction Sets Should Be Free: The Case For RISC-V - https://www.eecs.berkeley.edu/Pubs/TechRpts/2014/EECS-2014-146.html
* Proprietary versus Open Instruction Sets - http://research.cs.wisc.edu/multifacet/papers/ieeemicro16_card_isa.pdf
* RISC-V development plans - https://groups.google.com/a/groups.riscv.org/d/msg/isa-dev/sUQk6pFG0eA/AGNF44e4AAAJ
* RISC-V Geneology - https://www.eecs.berkeley.edu/Pubs/TechRpts/2016/EECS-2016-6.html
* RISC-V Offers Simple, Modular ISA - https://riscv.org/2016/04/risc-v-offers-simple-modular-isa/
* The Berkeley Out-of-Order Machine (BOOM): An Industry-Competitive, Synthesizable, Parameterized RISC-V Processor - https://www.eecs.berkeley.edu/Pubs/TechRpts/2015/EECS-2015-167.html
* The Case for Open Instruction Sets - http://www.linleygroup.com/mpr/article.php?id=11267
* The Renewed Case for the Reduced Instruction Set Computer: Avoiding ISA Bloat with Macro-Op Fusion for RISC-V - https://arxiv.org/abs/1607.02318 - https://www.eecs.berkeley.edu/Pubs/TechRpts/2016/EECS-2016-130.html

## Books

* "Computer Organization and Design: The Hardware Software Interface: RISC-V Edition" by David A. Patterson, John L. Hennessy (2017) - http://store.elsevier.com/product.jsp?isbn=9780128122754

## Open-Source Hardware Projects

* BOOM: The Berkeley Out-of-Order RISC-V Processor
  - https://ccelio.github.io/riscv-boom-doc/
  - https://github.com/ucb-bar/riscv-boom
  - https://twitter.com/boom_cpu
* f32c - A 32-bit RISC-V / MIPS retargetable CPU core
  - https://github.com/f32c/f32c
* lowRISC - creating a fully open-sourced, Linux-capable, RISC-V-based SoC
  - http://www.lowrisc.org/
  - https://github.com/lowRISC/lowrisc-chip/
  - https://twitter.com/lowRISC
* mriscv: A 32-bit Microcontroller featuring a RISC-V core
  - http://www.onchipuis.io/risc-v
  - https://github.com/onchipuis/mriscv
  - https://github.com/onchipuis/mriscvcore
  - https://twitter.com/onchipUIS
* ORCA - an implementation of RISC-V intended to target FPGAs
  - https://github.com/VectorBlox/orca
* PicoRV32 - A Size-Optimized RISC-V CPU
  - https://github.com/cliffordwolf/picorv32
* PULPino - 32-bit RISC-V microcontroller core
  - http://www.pulp-platform.org/
  - https://github.com/pulp-platform/pulpino
  - https://twitter.com/pulp_platform
* RIDECORE (RIsc-v Dynamic Execution CORE) - Out-of-Order RISC-V processor (Verilog)
  - https://github.com/ridecore/ridecore
* Rocket Chip Generator
  - https://github.com/ucb-bar/rocket-chip/
* SHAKTI Processor Project
  - http://rise.cse.iitm.ac.in/shakti.html
  - SHAKTI Tutorial at the VLSI Design Conference - http://www.slideshare.net/GSMadhusudan/shaktivlsidtutorial
  - https://bitbucket.org/casl/shakti_public
* SiFive's Freedom platforms RTL source files
  - https://github.com/sifive/freedom
* Sodor Processor Collection - educational microarchitectures
  - https://github.com/ucb-bar/riscv-sodor
* YARVI - Yet Another RISC-V Implementation
  - https://github.com/tommythorn/yarvi
  - https://www.cl.cam.ac.uk/teaching/1516/ECAD+Arch/exercise-yarvi.html

## References

https://riscv.org/specifications/

* Calling Convention - http://riscv.org/wp-content/uploads/2015/01/riscv-calling.pdf
* Notes on RISC-V assembly - https://www.imperialviolet.org/2016/12/31/riscv.html
* Reference Card - https://www.cl.cam.ac.uk/teaching/1617/ECAD+Arch/files/docs/RISCVGreenCardv8-20151013.pdf
* RISC-V Instruction Set Listing - https://github.com/michaeljclark/riscv-meta/blob/master/doc/pdf/riscv-instructions.pdf
* RISC-V Instruction Types - https://github.com/michaeljclark/riscv-meta/blob/master/doc/pdf/riscv-types.pdf
* The RISC-V Compressed Instruction Set Manual, Version 1.9 - https://www.eecs.berkeley.edu/Pubs/TechRpts/2015/EECS-2015-209.html
* The RISC-V Instruction Set Manual, Volume I: User-Level ISA, Version 2.1 - https://www.eecs.berkeley.edu/Pubs/TechRpts/2016/EECS-2016-118.html
* The RISC-V Instruction Set Manual Volume II: Privileged Architecture Version 1.9.1 - https://www.eecs.berkeley.edu/Pubs/TechRpts/2016/EECS-2016-161.html
* Wikipedia: RISC-V - https://en.wikipedia.org/wiki/RISC-V

## Software

https://riscv.org/software-tools/

* Debian port - https://wiki.debian.org/RISC-V
* L3 Specification of the RISC-V ISA - https://github.com/SRI-CSL/l3riscv
* RISC-V Formal Verification Framework - https://github.com/cliffordwolf/riscv-formal
* RISC-V Meta – a suite of tools that operate on RISC-V ISA - https://github.com/michaeljclark/riscv-meta/
* RISCVEMU - http://bellard.org/riscvemu/  
  RISCVEMU is a system emulator for the RISC-V architecture. Its purpose is to be small and simple while being complete. Among its features the support of 128 bit addressing and 128 bit floating point makes it ready for the future!
* Spike, a RISC-V ISA Simulator - https://github.com/riscv/riscv-isa-sim

## Tutorials

* RISC-V Presentation at ESC Boston 2016 - https://riscv.org/2016/04/risc-v-presentation-esc-boston/
* RISC-V Tutorial at HPCA 2015 - https://riscv.org/2015/02/risc-v-tutorial-hpca-2015/
