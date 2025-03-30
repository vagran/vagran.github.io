---
title: GateForge Python RTL hardware design framework and RISC-V CPU
subtitle:
tags: ["Python", "RTL", "Verilog", "RISC-V"]
date: 2025-03-30
---

{{< github-repo name="vagran/GateForge" >}}

So, I tried using an open-source toolchain for my next FPGA project. The first feature I checked in
Yosys was SystemVerilog interfaces, but unfortunately, they were not supported. This presents a
significant limitation in structuring a complex project effectively. Obviously, we need a framework
to address this. MyHDL, Magma, and Chisel all sound promising, but who says I can't create my own?

<!--more-->

I want to use Python for all metaprogramming — to structure and parameterize my design — while
sticking to familiar Verilog constructs for actual synthesizable logic. Seamless integration with
Verilator, allowing my Python unit tests to work with the emulated design, would be the cherry on
top.

To prove that it is actually usable, I created a reference implementation of a RISC-V CPU:

{{< github-repo name="vagran/gateforge-riscv" >}}
