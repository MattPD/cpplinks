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
* CARRV: Workshop on Computer Architecture Research with RISC-V - https://carrv.github.io/ 
* Design of the RISC-V Instruction Set Architecture - http://www.eecs.berkeley.edu/Pubs/TechRpts/2016/EECS-2016-1.html
* GRVI Phalanx: A Massively Parallel RISC-V FPGA Accelerator Accelerator - https://arxiv.org/abs/1606.01037
* How Genode came to RISC-V - https://genode.org/documentation/articles/riscv
* Instruction Sets Should Be Free: The Case For RISC-V - https://www.eecs.berkeley.edu/Pubs/TechRpts/2014/EECS-2014-146.html
* Proprietary versus Open Instruction Sets - http://research.cs.wisc.edu/multifacet/papers/ieeemicro16_card_isa.pdf
* RISC-V development plans - https://groups.google.com/a/groups.riscv.org/d/msg/isa-dev/sUQk6pFG0eA/AGNF44e4AAAJ
* RISC-V Geneology - https://www.eecs.berkeley.edu/Pubs/TechRpts/2016/EECS-2016-6.html
* RISC-V International Conference Proceedings - http://rise.cse.iitm.ac.in/ric2017/index.html#Proceedings
* RISC-V Offers Simple, Modular ISA - https://riscv.org/2016/04/risc-v-offers-simple-modular-isa/
* rv8: a high performance RISC-V to x86 binary translator
	+ https://anarch128.org/~mclark/rv8-carrv.pdf
	+ https://carrv.github.io/papers/clark-rv8-carrv2017.pdf
* The Berkeley Out-of-Order Machine (BOOM): An Industry-Competitive, Synthesizable, Parameterized RISC-V Processor
	+ https://www.eecs.berkeley.edu/Pubs/TechRpts/2015/EECS-2015-167.html
	+ BOOM v2: an open-source out-of-order RISC-V core - https://www2.eecs.berkeley.edu/Pubs/TechRpts/2017/EECS-2017-157.html
* The Case for Open Instruction Sets - http://www.linleygroup.com/mpr/article.php?id=11267
* The Renewed Case for the Reduced Instruction Set Computer: Avoiding ISA Bloat with Macro-Op Fusion for RISC-V - https://arxiv.org/abs/1607.02318 - https://www.eecs.berkeley.edu/Pubs/TechRpts/2016/EECS-2016-130.html

## Books

* "Computer Organization and Design: The Hardware Software Interface: RISC-V Edition" by David A. Patterson, John L. Hennessy (2017) - http://store.elsevier.com/product.jsp?isbn=9780128122754
* "The RISC-V Reader: An Open Architecture Atlas" by David Patterson, Andrew Waterman (2017) - http://www.riscvbook.com/ 

## Open-Source Hardware Projects

* Ariane RISC-V CPU (SystemVerilog)
	+ Ariane is a 6-stage, single issue, in-order CPU which implements the 64-bit RISC-V instruction set.
	+ https://pulp-platform.github.io/ariane/
	+ https://github.com/pulp-platform/ariane
* BOOM: The Berkeley Out-of-Order RISC-V Processor (Chisel)
	+ https://ccelio.github.io/riscv-boom-doc/
	+ https://github.com/ucb-bar/riscv-boom
	+ https://twitter.com/boom_cpu
* f32c - A 32-bit RISC-V / MIPS retargetable CPU core (VHDL)
	+ https://github.com/f32c/f32c
* lowRISC - creating a fully open-sourced, Linux-capable, RISC-V-based SoC (SystemVerilog)
	+ http://www.lowrisc.org/
	+ https://github.com/lowRISC/lowrisc-chip/
	+ https://twitter.com/lowRISC
* mriscv: A 32-bit Microcontroller featuring a RISC-V core (Verilog)
	+ http://www.onchipuis.io/risc-v
	+ https://github.com/onchipuis/mriscv
	+ https://github.com/onchipuis/mriscvcore
	+ https://twitter.com/onchipUIS
* ORCA - an implementation of RISC-V intended to target FPGAs (VHDL)
	+ https://github.com/VectorBlox/orca
* PicoRV32 - A Size-Optimized RISC-V CPU (Verilog)
	+ https://github.com/cliffordwolf/picorv32
* PULPino - 32-bit RISC-V microcontroller core (SystemVerilog)
	+ http://www.pulp-platform.org/
	+ https://github.com/pulp-platform/pulpino
	+ https://twitter.com/pulp_platform
* RIDECORE (RIsc-v Dynamic Execution CORE) - Out-of-Order RISC-V processor (Verilog)
	+ https://github.com/ridecore/ridecore
* RI5CY: RISC-V Core - PULP RI5CY core modified for Verilator modeling and as a GDB server (SystemVerilog)
	+ https://github.com/embecosm/ri5cy
* RISC V Cores and SoCs
	+ https://github.com/riscv/riscv-wiki/wiki/RISC-V-Cores-and-SoCs
* RISC-V VHDL: System-on-Chip (VHDL)
	+ VHDL implementation of the RISC-V System-on-Chip based on bare "Rocket Chip"
	+ http://sergeykhbr.github.io/riscv_vhdl/
	+ https://github.com/sergeykhbr/riscv_vhdl
* Riscy Processors - Open-Sourced RISC-V Processors (Bluespec System Verilog)
	+ https://github.com/csail-csg/riscy
* Rocket Chip Generator (Chisel)
	+ https://github.com/ucb-bar/rocket-chip/
* SCR1: an open-source RISC-V compatible MCU core (SystemVerilog)
	+ https://github.com/syntacore/scr1 
* SHAKTI Processor Project (Bluespec System Verilog; generated Verilog)
	+ http://rise.cse.iitm.ac.in/shakti.html
	+ SHAKTI Tutorial at the VLSI Design Conference - http://www.slideshare.net/GSMadhusudan/shaktivlsidtutorial
	+ https://bitbucket.org/casl/shakti_public
* SiFive's Freedom platforms RTL source files (Chisel)
	+ https://github.com/sifive/freedom
* Sodor Processor Collection - educational microarchitectures (Chisel)
	+ https://github.com/ucb-bar/riscv-sodor
* Taiga (SystemVerilog)
	+ 32-bit RISC-V processor designed for FPGAs supporting the Multiply/Divide and Atomic extensions (RV32IMA)
	+ https://gitlab.com/sfu-rcl/Taiga
	+ TAIGA: A new RISC-V soft-processor framework enabling high performance CPU architectural features
		- Field Programmable Logic and Applications (FPL) 2017
		- E. Matthews and L. Shannon
		- https://doi.org/10.23919/FPL.2017.8056766
		- https://carrv.github.io/2017/papers/matthews-taiga-carrv2017.pdf
* VexRiscv: FPGA-friendly 32-bit RISC-V CPU implementation (SpinalHDL)
	+ https://github.com/SpinalHDL/VexRiscv
* YARVI - Yet Another RISC-V Implementation (Verilog)
	+ https://github.com/tommythorn/yarvi
	+ https://www.cl.cam.ac.uk/teaching/1516/ECAD+Arch/exercise-yarvi.html

## References

https://riscv.org/specifications/

* A RISC-V ELF psABI Document - RISC-V calling convention - https://github.com/riscv/riscv-elf-psabi-doc 
* Calling Convention - http://riscv.org/wp-content/uploads/2015/01/riscv-calling.pdf
* Documentation for RISC-V Spike - https://github.com/poweihuang17/Documentation_Spike 
* Notes on RISC-V assembly - https://www.imperialviolet.org/2016/12/31/riscv.html
* Reference Card - https://www.cl.cam.ac.uk/teaching/1617/ECAD+Arch/files/docs/RISCVGreenCardv8-20151013.pdf
* RISC-V Assembly Programmer's Manual - https://github.com/riscv/riscv-asm-manual/blob/master/riscv-asm.md
* riscv-calling-conv-model: work towards a "golden model" of the RISC-V calling convention(s) - https://github.com/lowRISC/riscv-calling-conv-model
* RISC-V Instruction Set Manual - https://github.com/riscv/riscv-isa-manual
* RISC-V Instruction Set Listing - https://github.com/michaeljclark/riscv-meta/blob/master/doc/pdf/riscv-instructions.pdf
* RISC-V Instruction Types - https://github.com/michaeljclark/riscv-meta/blob/master/doc/pdf/riscv-types.pdf
* RISC-V Toolchain Conventions - https://github.com/lowRISC/riscv-toolchain-conventions
* The Embedded RISC-V Project
	+ A complementary RISC-V specification intended for bare metal embedded applications 
	+ https://emb-riscv.github.io/
	+ https://github.com/emb-riscv
	+ https://github.com/emb-riscv/specs-markdown
* The RISC-V Compressed Instruction Set Manual - https://riscv.org/specifications/compressed-isa/
* The RISC-V Instruction Set Manual, Volume I: User-Level ISA - https://riscv.org/specifications/
* The RISC-V Instruction Set Manual Volume II: Privileged Architecture - https://riscv.org/specifications/privileged-isa/
* Wikipedia: RISC-V - https://en.wikipedia.org/wiki/RISC-V

## Software

https://riscv.org/software-tools/

* Compiler Explorer with RISC-V support - https://cx.rv8.io/
* Debian port - https://wiki.debian.org/RISC-V
* hpm_counters: A simple utility for doing RISC-V Hardware Performance Monitor (HPM) perf monitoring - https://github.com/ccelio/riscv-hpmcounters 
* L3 Specification of the RISC-V ISA - https://github.com/SRI-CSL/l3riscv
* RISC-V Disassembler: Single file RISC-V Disassembler with support for RV32/RV64/RV128 IMAFDC
	+ https://github.com/michaeljclark/riscv-disassembler
* RISC-V Formal Verification Framework - https://github.com/cliffordwolf/riscv-formal
* RISC-V Meta – a suite of tools that operate on RISC-V ISA - https://github.com/michaeljclark/riscv-meta/
* RISC-V support for LLVM projects - http://www.lowrisc.org/llvm/status/ - https://github.com/lowRISC/riscv-llvm
* RISC-V Torture Test Generator - https://github.com/ucb-bar/riscv-torture 
* riscv-semantics - formal specification of the RISC-V ISA written in Haskell - https://github.com/mit-plv/riscv-semantics
* RISCVEMU
	+ RISCVEMU is a system emulator for the RISC-V architecture. Its purpose is to be small and simple while being complete. Among its features the support of 128 bit addressing and 128 bit floating point makes it ready for the future!
	+ http://bellard.org/riscvemu/
* RISCVEmu Toy RISC-V emulator - https://github.com/jdryg/RISCVEmu
* rv8: RISC-V simulator for x86-64 - https://rv8.io/
	+ https://github.com/rv8-io/rv8
* Spike, a RISC-V ISA Simulator - https://github.com/riscv/riscv-isa-sim
* venus: RISC-V instruction set simulator built for education
	+ https://kvakil.github.io/venus/ 
	+ https://github.com/kvakil/venus

## Talks

* End-to-end formal ISA verification of RISC-V processors with riscv-formal
	+ 34C3 (2017), Clifford Wolf 
	+ https://www.youtube.com/watch?v=VU97ffHF_IQ
	+ https://media.ccc.de/v/34c3-8768-end-to-end_formal_isa_verification_of_risc-v_processors_with_riscv-formal

## Tutorials

* "All Aboard" Blog Series
	+ Part 0: Introduction: Part 0: Introduction - https://www.sifive.com/blog/2017/08/07/all-aboard-part-0-introduction/
	+ Part 1: The -march, -mabi, and -mtune arguments to RISC-V Compilers - https://www.sifive.com/blog/2017/08/14/all-aboard-part-1-compiler-args/
	+ Part 2: Relocations in ELF Toolchains - https://www.sifive.com/blog/2017/08/21/all-aboard-part-2-relocations/
	+ Part 3: Linker Relaxation in the RISC-V Toolchain - https://www.sifive.com/blog/2017/08/28/all-aboard-part-3-linker-relaxation-in-riscv-toolchain/
	+ Part 4: The RISC-V Code Models - https://www.sifive.com/blog/2017/09/11/all-aboard-part-4-risc-v-code-models/
	+ Part 5: Per-march and per-mabi Library Paths on RISC-V Systems - https://www.sifive.com/blog/2017/09/18/all-aboard-part-5-risc-v-multilib/
	+ Part 6: Booting a RISC-V Linux Kernel - https://www.sifive.com/blog/2017/10/09/all-aboard-part-6-booting-a-risc-v-linux-kernel/
	+ Part 7: Entering and Exiting the Linux Kernel on RISC-V - https://www.sifive.com/blog/2017/10/23/all-aboard-part-7-entering-and-exiting-the-linux-kernel-on-risc-v/
	+ Part 8: The RISC-V Linux Port is Upstream! - https://www.sifive.com/blog/2017/12/05/all-aboard-part-8-the-risc-v-linux-port-is-upstream/
	+ Part 9: Paging and the MMU in the RISC-V Linux Kernel - https://www.sifive.com/blog/2017/12/11/all-aboard-part-9-paging-and-mmu-in-risc-v-linux-kernel/
	+ Part 10: How to Contribute to the RISC-V Software Ecosystem - https://www.sifive.com/blog/2018/02/20/all-aboard-part-10-how-to-contribute-to-the-risc-v-software-ecosystem/
* Building upstream RISC-V GCC+binutils+newlib: the quick and dirty way - http://www.lowrisc.org/blog/2017/09/building-upstream-risc-v-gccbinutilsnewlib-the-quick-and-dirty-way/
* RISC-V 101 Webinar - https://info.sifive.com/risc-v-webinar
* RISC-V Presentation at ESC Boston 2016 - https://riscv.org/2016/04/risc-v-presentation-esc-boston/
* RISC-V QEMU
	+ Part 1: Privileged ISA v1.10, HiFive1 and VirtIO - https://www.sifive.com/blog/2017/12/20/risc-v-qemu-part-1-privileged-isa-hifive1-virtio/
* RISC-V Tutorial at HPCA 2015 - https://riscv.org/2015/02/risc-v-tutorial-hpca-2015/
