---
layout: post
title: RISC
permalink: /projects/risc/
---

For our EE224 course project, we were asked to implement a RISC (Reduced Instruction Set Computer) with 14 basic general purpose instructions.

We implemented it in VHDL and tested it using the popular software Quartus.
The complete design specification can be found [here]({{site.url}}/assets/pdf/risc_specs.pdf).
We approached the problem using the following strategy:
 
* Design the Finite State Machine on paper.
* Make the datapath which shows the required components such as ALU, MUXes, register files, etc. with wires connecting them.
* Write the actual code in VHDL.
* Make a set of test instructions to test the machine

The final presentation can be found [here]({{site.url}}/assets/pdf/risc_report.pdf).
You can visit my Github [repo](https://github.com/methi1999/risc) which contains the entire code.

