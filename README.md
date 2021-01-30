# SealPK
This is a pre-alpha release of Sealable Memory Protection Keys (SealPK) for RISC-V. The official release will be available soon.

## Overview
In this document, we provide a guideline for running and testing SealPK. We run our experiments on the Xilinx Zynq Zedboard FPGA and use a modified Linux
kernel 4.15 to provide the support for our hardware.

**Note: Currently, you need to have access to a Xilinx Zynq Zedboard FPGA to be able to run PHMon experiments.**

To test SealPK, you need to scp the bitstream (rocketchip_sealpk.bit.bin), fesvr-zynq, and bbl to your FPGA.
Then, you can reconfigure the FPGA with the bitstream and bootup the Linux kernel.
```
$ cat rocketchip_sealpk.bit.bin > /dev/xdevcfg 
$ ./fesvr-zynq bbl_sealpk
```
