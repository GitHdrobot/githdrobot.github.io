---
title: Portability-compatibility
date: 2021-10-01 20:24:02
tags:
- Portability
- Compatibility
---

兼容性和可移植性是软件开发中重要目标，Windows、Linux取得成功的一关键原因就在两者尽可能保证了应用的可移植性和兼容性。

兼容、可移植性主要涉及源码、编译器、操作系统、硬件等方面。

### 硬件

当前主要有ARM、x86、PowerPC、MIPS、RISC-V等架构的CPU。

ARM：高级精简指令集机器（Advanced RISC Machine），指令集采用定长架构（thumb为变长指令集），大致有50条指令，广泛应用于低功耗移动设备。V6前不支持内存非对齐访问，之后有条件支持非对齐内存访问。指令中包含4bit条件执行的编码。

<img src="ARMSoCBlockDiagram.svg" alt="ARM Architecture" style="zomm:%100;"/>

X86：指令集使用变长的CISC架构，硬件采用普林斯顿架构（冯诺依曼架构）

<img src="Athlon_arch.png" alt="Athlon arch" style="zomm:%100;"/>

MIPS：采用RISC指令集架构，最新架构版本于2014年推出 ，现该架构已不再更新，但其衍生架构（龙芯、RISC-V）仍在发展中。

<img src="MIPS_Architecture_(Pipelined).svg" alt="MIPS_Architecture_Pipelined" style="zomm:%100;"/>

### 源码

开发过程中尽可能使用标准明确的、确定的语句，避免使用依赖编译器、操作系统特性的代码。对于一些强依赖于操作系统、硬件的代码一般做法是增加适配层（VOS）。因此实现可移植性则需要抽象、分层、隔离差异，如Linux不同硬件平台差异代码放在arch目录，对文件系统，设备的抽象分层处理。

### 思考

x86、ARM架构占有大部分市场，RISC-V开源架构有哪些优势，还有机会发展为硬件开源中的“Linux”吗

