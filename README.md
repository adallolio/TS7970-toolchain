# Cross-compilation toolchain for the TS-7970 development board

This repository contains pre-built compilator binaries for the GCC 4.9 Linaro toolchain, for cross-compilation to the NXP i.MX6
ARMv7 Cortex-A9 processor. You can download the original toolchain [here](http://ftp.embeddedarm.com/ftp/ts-arm-sbc/ts-7553-V2-linux/cross-toolchains/gcc-linaro-4.9-2016.02-x86_64_arm-linux-gnueabihf.tar.xz), 
as indicated in the [TS-7970 user manual](https://wiki.embeddedarm.com/wiki/TS-7970#Debian_Application_Development_2).

## Usage

* Clone the repository to a folder in your computer (e.g., the HOME folder):

```
$ git clone https://github.com/adallolio/TS7970-toolchain $HOME
```

* To target the i.MX6 for cross-compilation, point to the "arm-linux-gnueabihf-" files inside the "bin" folder in this repository.
For example, to cross-compile the [DUNE](http://github.com/lsts/dune) software:

```
$ CROSS_COMPILE=$HOME/TS7970-toolchain/bin/arm-linux-gnueabihf-
$ cd $HOME/dune/build
$ cmake -DCROSS=$CROSS_COMPILER ..
$ make
```
