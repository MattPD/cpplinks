# [C++ links](README.md): computer architecture - FPGA

See also: [computer architecture](comparch.md)

You may also be interested in the resources listed in my talk, "FPGAs and Open-Source Hardware - An Intro" (Meeting C++ 2016):
https://speakerdeck.com/mattpd/fpgas-and-open-source-hardware-an-intro-meeting-c-plus-plus-2016

# Articles

* A 16-nm Multiprocessing System-on-Chip Field-Programmable Gate Array Platform (2016) - http://doi.org/10.1109/MM.2016.18
* Fundamental Underpinnings of Reconfigurable Computing Architectures (2015) - http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=7086421
* It’s an FPGA! (2011)
  - P. Alfke, I. Bolsens, B. Carter, M. Santarini, and S. Trimberger, IEEE Solid-State Circuits Mag., vol. 3, no. 4, 2011, pp. 15-20
  - http://phdtree.org/pdf/39505483-its-an-fpga/ / http://ieeexplore.ieee.org/document/6069771/
* Measuring the Gap Between FPGAs and ASICs (2007) - http://ieeexplore.ieee.org/document/4068926/
* Reconfigurable Computing Architectures (2015) - http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=7086414
* Reading List - ACM SIGDA Technical Committee on FPGAs (TCFPGA) Hall of Fame - http://hof.tcfpga.org/reading-list/
* Three Ages of FPGAs: A Retrospective on the First Thirty Years of FPGA Technology (2015) - http://ieeexplore.ieee.org/abstract/document/7086413/
* Trends in Reconfigurable Computing: Applications and Architectures (2015)
  - Lesley Shannon, Veronica Cojocaru, Cong Nguyen Dao, and Philip H.W. Leong. In Proc. IEEE Symposium on Field-Programmable Custom Computing Machines (FCCM), 2015
  - http://www.ee.usyd.edu.au/people/philip.leong/UserFiles/File/papers/trends_fccm15.pdf
* Xilinx and the Birth of the Fabless Semiconductor Industry (2013)
  - Steve Leibson, Chapter of "Fabless: the Transformation of the Semiconductor Industry"
  - https://forums.xilinx.com/xlnx/attachments/xlnx/Xcell/200/1/Fabless%20Book%20Chapter%20FINAL.pdf

# Courses

* 18-643 Reconfigurable Logic: Technology, Architecture and Applications - http://users.ece.cmu.edu/~jhoe/doku/doku.php?id=18-643_reconfigurable_logic

# Communities

* comp.arch.fpga - https://groups.google.com/d/forum/comp.arch.fpga
* comp.lang.verilog - https://groups.google.com/d/forum/comp.lang.verilog
* comp.lang.vhdl - https://groups.google.com/d/forum/comp.lang.vhdl
* /r/FPGA - everything about programmable hardware - https://www.reddit.com/r/FPGA
* IRC ​Channel #​#fpga - freenode - http://irc.netsplit.de/channels/details.php?room=%23%23fpga&net=freenode

# HDL

## HDL: Verilog

* EDA Playground - Verilog Tutorials
  - http://eda-playground.readthedocs.io/en/latest/code-examples/verilog.html
  - https://www.youtube.com/playlist?list=PLScWdLzHpkAfbPhzz1NKHDv2clv1SgsMo
* FPGA Resources - http://fpgacpu.ca/fpga/
  - HDL References - http://fpgacpu.ca/fpga/hdl/
* HDLBits — Verilog Practice - http://verilog.stuffedcow.net/
* Learning Verilog for FPGAs: The Tools and Building an Adder - http://hackaday.com/2015/08/19/learning-verilog-on-a-25-fpga-part-i/
* Open FPGA Verilog Tutorial - https://github.com/Obijuan/open-fpga-verilog-tutorial/wiki/Home_EN
* Quick Reference for Verilog HDL - https://github.com/parallella/oh/blob/master/docs/verilog_reference.md
* Verilog Page - http://www.asic-world.com/verilog/

## HDL: SystemVerilog

* Appendix A "Hardware Description Languages" from Neil Weste, David Harris (2010) "CMOS VLSI Design: A Circuits and Systems Perspective" (4th Edition) - http://pages.hmc.edu/harris/cmosvlsi/4e/cmosvlsidesign_4e_App.pdf
* IEEE Standard 1800-2012 - http://standards.ieee.org/getieee/1800/download/1800-2012.pdf 
* Papers
  - Cliff Cummings - http://www.sunburst-design.com/papers/#papers_top
  - Don Mills - http://www.lcdm-eng.com/html/papers.html
  - Stuart Sutherland - http://www.sutherland-hdl.com/papers.html
    - Standard Gotchas: Subtleties in Verilog and SystemVerilog That Every Engineer Should Know - http://www.sutherland-hdl.com/papers/2006-SNUG-Boston_standard_gotchas_paper.pdf
    - More Standard Gotchas: Subtleties in Verilog and SystemVerilog That Every Engineer Should Know - http://www.sutherland-hdl.com/papers/2007-SNUG-SanJose_gotcha_again_paper.pdf
* SystemVerilog Central - http://www.asic-world.com/systemverilog/
* SystemVerilog Training and Examples from Doulos - The Guide to SystemVerilog - https://www.doulos.com/knowhow/sysverilog/

# HLS

- Productive Parallel Programming for FPGA with High Level Synthesis (Tutorial)
	- Torsten Hoefler, Johannes de Fine Licht
	- https://spcl.inf.ethz.ch/Teaching/hls-tutorial/
	- https://github.com/spcl/hls_tutorial_examples
- Transformations of High-Level Synthesis Codes for High-Performance Computing
	- IEEE Transactions on Parallel and Distributed Systems (TPDS) 2021
	- Johannes de Fine Licht, Maciej Besta, Simon Meierhans, Torsten Hoefler
	- https://arxiv.org/abs/1805.08288
	- https://spcl.inf.ethz.ch/Publications/.pdf/hls-transformations.pdf

# Open Source Hardware FPGA Projects

* FOSSi: The Free and Open Source Silicon Foundation - http://fossi-foundation.org/
* FuseSoC (package manager and a set of build tools for HDL code for FPGA/ASIC development) - https://github.com/olofk/fusesoc
* LibreCores: Free and Open Source Digital Hardware - https://www.librecores.org/
* OpenCores: Open Source Hardware Community - http://opencores.org/

---

* PicoRV32 - A Size-Optimized RISC-V CPU
  - https://github.com/cliffordwolf/picorv32  
  - https://github.com/cliffordwolf/picorv32/tree/master/scripts/icestorm
* FPGA Webserver - https://github.com/hamsternz/FPGA_Webserver
* J2 core: a cleanroom reimplementation of the SH-2 ISA with extensions
  - http://j-core.org/
  - "Building a CPU from Scratch: jcore Design Walkthrough": http://j-core.org/talks/ 
* NetFPGA: http://netfpga.org/
  - https://github.com/NetFPGA/netfpga
  - https://github.com/NetFPGA/NetFPGA-public/wiki
* Nyuzi Processor: GPGPU processor, SystemVerilog FPGA implementation
  - https://github.com/jbush001/NyuziProcessor
* OH! Open Hardware for Chip Designers
  - Silicon proven Verilog library for IC and FPGA designers
  - https://github.com/parallella/oh
  - https://github.com/parallella/oh#design-guide
  - https://github.com/parallella/oh#coding-guide
* TPU: Designing a CPU in VHDL
  - http://labs.domipheus.com/blog/tpu-series-quick-links/
  - Github repository with VHDL sources, ISE project, assembler and ISA: https://github.com/Domipheus/TPU

# Software

* gEDA suite - http://geda-project.org/ - http://wiki.gedaproject.org/geda:faq
  - The gEDA project has produced and continues working on a full GPL'd suite and toolkit of Electronic Design Automation tools. These tools are used for electrical circuit design, schematic capture, simulation, prototyping, and production. Currently, the gEDA project offers a mature suite of free software applications for electronics design, including schematic capture, attribute management, bill of materials (BOM) generation, netlisting into over 20 netlist formats, analog and digital simulation, and printed circuit board (PCB) layout.
* Project IceStorm - http://www.clifford.at/icestorm/  
  - Project IceStorm aims at reverse engineering and documenting the bitstream format of Lattice iCE40 FPGAs and providing simple tools for analyzing and creating bitstream files. The IceStorm flow (Yosys, Arachne-pnr, and IceStorm) is a fully open source Verilog-to-Bitstream flow for iCE40 FPGAs. 
* SymbiFlow - https://symbiflow.github.io/
  - FOSS Verilog-to-Bitstream FGPA synthesis flow for Xilinx 7-Series FPGAs and iCE40
  - Project X-Ray: Documenting the Xilinx 7-series bit-stream format - https://github.com/SymbiFlow/prjxray

# Talks & Videos

* University of Toronto FPGA Seminar Series - http://www.eecg.utoronto.ca/~jayar/FPGAseminar/
* 2016: Formal Verification with Yosys-SMTBMC (Clifford Wolf, ORCONF 2016) - http://www.clifford.at/papers/2016/yosys-smtbmc/
* 2016: Verilog Synthesis and Formal Verification with Yosys (Clifford Wolf, Easterhegg 2016) - http://www.clifford.at/papers/2016/yosys-synth-formal/
* 2016: A Free and Open Source Verilog-to-Bitstream Flow for iCE40 FPGAs (Clifford Wolf, 32C3 & FOSDEM 2016) - http://www.clifford.at/papers/2015/icestorm-flow/
* 2015: Open Source HDL Synthesis and Verification with Yosys (Clifford Wolf, ORCONF 2015) - http://www.clifford.at/papers/2015/yosys-icestorm-etc/
* 2015: _Computer History Museum: Oral History of Bill Carter, designer of the first FPGA._ Interviewed by Steve Trimberger on 2015-07-13 - https://www.youtube.com/watch?v=1oG-3XWLgog
* 2014: The Three Ages of the FPGA - Steve Trimberger, Xilinx - https://forums.xilinx.com/t5/Xcell-Daily-Blog/Video-The-Three-Ages-of-the-FPGA-and-the-Age-of-the-Design/ba-p/644396
