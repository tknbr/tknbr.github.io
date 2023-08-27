---
layout: post
title: Understanding the Raspberry Pi 3 boot process
categories: [funRTOS]
---


## The hardware

The Raspberry Pi 3 is a credit-card-sized single-board computer developed by the Raspberry Pi Foundation. Here's a summary its hardware specifications:

1. **Processor:** 1.2 GHz 64-bit quad-core ARM Cortex-A53 processor.

2. **GPU:** VideoCore IV GPU.

3. **Memory (RAM):** It comes with 1 GB of LPDDR2 RAM.

4. **Connectivity:**
   - **Wi-Fi:** Built-in 2.4 GHz 802.11n.
   - **Bluetooth:** It also features Bluetooth 4.1.

5. **Ethernet:** The board has a 10/100 Ethernet port for wired network connections.

6. **USB Ports:** four USB 2.0 ports.

7. **Video Output:** HDMI output with resolutions up to 1080p.

8. **Audio:**  3.5mm audio jack, as well as support for HDMI audio output.

9. **GPIO Pins:** 40-pin GPIO (General Purpose Input/Output) header.

10. **Storage:** The primary storage is provided through a microSD card slot, where you can install the operating system and store your data.

11. **Power:** micro USB port using a 5V power adapter.

For the time being, we will concentrate on these four key elements: the Processor, GPU, Memory, and Storage. To develop a clearer comprehension of the processor, let's take a closer look:

1. **Processor Cores:** The BCM2837 SoC features four ARM Cortex-A53 cores. These cores are 64-bit capable and based on the ARMv8-A architecture. Each core operates at a clock speed of 1.2 GHz.

2. **Cache:** The Cortex-A53 cores on the BCM2837 have a hierarchical cache structure, which includes both L1 and L2 caches:
   - **L1 Cache:** Each core has separate instruction and data L1 caches. The instruction L1 cache is 32 KB, and the data L1 cache is also 32 KB.
   - **L2 Cache:** The L2 cache is shared among all four cores and has a total size of 512 KB. It helps improve memory performance by storing frequently accessed data and instructions closer to the cores.

3. **Instruction Set:** The Cortex-A53 cores use the ARMv8-A instruction set architecture, which includes support for 64-bit instructions and addressing.

With this overview of the concepts, we now have enough information to comprehend all the different components involved in the boot process.

## The boot process

The boot process on the Raspberry Pi 3 consists of different bootloader stages:

1. The on-chip ROM contains the firmware bootloader. When we power on the Raspberry Pi 3b, the CPU is halted, and the code from the firmware will run on the GPU. The firmware bootloader is in charge of searching for the bootcode.bin file located at the root of the boot partition inside the microSD card and loading it into the L2 cache.

2. The GPU will then start executing the code loaded from bootcode.bin, enabling SDRAM. Afterward, it will load the loader.bin file, also located at the root of the boot partition inside the microSD card.

3. The GPU is also responsible for executing loader.bin. This binary contains all the information needed to execute .elf files. This enables the code to load start.elf, which, depending on the configuration, will look for our kernel name.

4. The kernel is then loaded and starts executing on the CPU.

So, apart from the kernel itself we will need several files to be included in the boot partition of our microSD:

* bootcode.bin
* loader.bin
* start.elf
* config.txt



