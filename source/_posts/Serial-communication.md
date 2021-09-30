---
title: Serial-communication
date: 2021-09-29 07:22:33
tags: 
 - Serial Communication
 - Synchronous Communication
 - Asynchronous Communication
---

Serial通信一般分为同步通信（SPI、I^2C）和异步通信（UART），硬件上主要区别是同步通信总线上有单独的同步时钟线，在数据链路层，异步通信数据帧上需添加额外信息（起始位、停止位、空闲位）用于同步数据帧。逻辑信号表示分为single-ended和differential，差分信号有较好抗噪声、传输距离更长优点正逐步替代单端模式。

## Asynchronous Communication

UART：通用异步收发器，一般指串口、总线标准有EIA RS-232  、EIA RS-485、RS-422，是早期计算机最早的通信设备之一，应用十分广泛。

CAN：控制器局域网，由BOSCH公司开发，利用message identifier定义内容和消息优先顺序进行传输。当前使用较多的规范11位标识符的CAN2.0 A和29位标识符的CAN2.0B。ISO于1993年公布了can标准ISO11898。

Ethernet：以太网通信规范，现互联网使用较为普遍的通信标准，10BASE-T使用manchester编码，100BASE-T使用4B5B编码，1000BASE-T（IEEE802.3ab）使用PAM-5编码。

Firewire：”火线“是苹果公司对IEEE 1394标准的命名，该标准的提出与USB有着相似目的，早期1394标准速度优于USB。

SATA：一种用于连接主机总线和大容量存储设备的总线接口。

SAS：序列化SCSI（Serial Attached SCSI）一种点对点的串行协议，由并行SCSI发展而来。主要用作连接计算机周边设备如硬盘、CD-ROM，进行数据传输。

### 电路电平

RS232电平范围-15~15V，采用负逻辑。RS485使用差分信号表示，电平范围-7~12V

<img src="Rs232_Rs485_standard.PNG" alt="Rs232 Rs485 Standard" style="zomm:%100;"/>

CAN电平范围0~5V，使用differential模式以dominant state （逻辑0，diff v:2.0v）和 recessive state（逻辑1，diff v:0v）两种状态表示逻辑信号。

<img src="ISO11898-2.svg" alt="CAN standard logic level" style="zomm:%100;"/>

常见TTL（7000 series）、CMOS（4000 series）

<img src="Standard Logic Levels.PNG" alt="Standard Logic Levels" style="zomm:%100;"/>

### 信号波形

Rs232发送'K'字符（0x4B）波形如下图：

<img src="Rs232_oscilloscope_trace.svg" alt="Rs232 waveform" style="zomm:%100;"/>

Rs485发送0xD3波形如下图：

<img src="RS-485_waveform.svg" alt="Rs485 waveform" style="zomm:%100;"/>

CAN波形：

CAN采用NRZ编码，为维护帧同步一般会对数据帧进行位填充。

<img src="CAN-Bus-frame_in_base_format_without_stuffbits.svg" alt="CAN waveform without stuffbits" style="zomm:%100;"/>

<img src="CAN-Frame_mit_Pegeln_mit_Stuffbits.svg" alt="CAN waveform with stuffbits" style="zomm:%100;"/>

### 常见电平转换芯片

232转ttl电平：max232（MAXIM），SP3232E（SIPEX）

usb转ttl：PL2303HX（Prolific）、CH340（沁恒）、XR21V1410（MaxLinear）、FT232（FTDI）、CP2104（SILICON LABS）

## Synchronous Communication

HDMI：高清多媒体接口（High Definition Multimedia Interface）该接口实现了 EIA/CEA-861标准，用于传输音视频数据。

PCIE：高速串行计算机扩展总线标准。（PCI：Peripheral Component Interconnect，外设组件互连总线）

SPI：串行外设接口（Serial Peripheral Interface），一种短距离的同步串行通信接口规范，主要用于嵌入式系统中。使用主从架构，工作在全双工模式。

SPI　master－slave连接示意图

<img src="SPI_8-bit_circular_transfer.svg" alt="SPI　connection" style="zomm:%100;"/>

SPI　时序图

<img src="SPI_timing_diagram2.svg" alt="SPI　timing　diagram" style="zomm:%100;"/>

I^2C：集成电路总线（Inter-Integrated Circuit），是一种同步、多主多从，single-ended串行通信总线。广泛应用于外设集成电路和mcu之间的一种短距离板级通信协议。

<img src="Basics-of-I2C-Communication-Data-Transfer-Protocol.jpg" alt="I2C frame format" style="zomm:%100;"/>

<img src="I2C.svg" alt="I2C schematic" style="zomm:%100;"/>

<img src="I2C_data_transfer.svg" alt="I2C timing diagram" style="zomm:%100;"/>

## 思考

Rs232为何采用负逻辑

异步通信与同步通信（SPI、I^2C）的主要区别

PCI发展到PCI-e，并行SCSI发展到串行SCSI，即串行总线代替并行总线速度反而提高

