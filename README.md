# STM32WBA Classic Core Middleware (CoreMW) MCU Firmware Package

![latest tag](https://img.shields.io/github/v/tag/STMicroelectronics/stm32wba-classic-coremw-apps.svg?color=brightgreen)

![freertos](https://img.shields.io/badge/freertos-v10.6.2-blue.svg) ![fatfs](https://img.shields.io/badge/fatfs-R0.15-blue.svg)

## Description

**STM32Cube** is an STMicroelectronics original initiative to ease developers' life by reducing efforts, time and cost.

**Classic CoreMW** is a collection of middleware stacks and associated applications allowing RTOS management, File System operations and connectivity through USB and Ethernet. It is based on:
* ST's proprietary stacks: ST USB Device and ST USB Host
* Third parties' stacks: FreeRTOS, FatFS, and LwIP

This package is **exclusively** published on GitHub (and is neither available in STM32CubeMX nor STM32CubeIDE available on www.st.com).
It contains the integration of the Classic CoreMW stacks with *STM32WBA* devices, allowing users to get quick access to pre-built projects integrating them.

#### *Note*

 * The repository containing this package has been created using the `git submodule` command. Please refer to the ["How to use"](README.md#how-to-use) section explaining how to clone this repository and how to get the latest updates.

## List of applications

The **STM32WBA Classic CoreMW** package contains the following applications:

Middleware    | Application                        | Short Description
--------------|------------------------------------|------------------------------------------------------------------------
FatFs	        | FatFs_RAMDISK_Standalone	         | Shows how to use STM32Cube firmware with FatFs middleware component as a generic FAT file system module


#### *Note*
 * *FreeRTOS* Middleware and examples are delivered on STM32WBA in the form of X-CUBE-FREERTOS that is available from [st.com](https://www.st.com/en/embedded-software/x-cube-freertos.html), from [GitHub](https://github.com/STMicroelectronics/x-cube-freertos) and from STM32CubeMX.
 * Projects in this package have not been generated with STM32CubeMX (**i.e.**, no `.ioc` files are delivered).

## Boards available

 * STM32WBA
   * [NUCLEO-WBA52CG](https://www.st.com/en/evaluation-tools/nucleo-wba52cg.html)

## Development Toolchains and Compilers

 * IAR Embedded Workbench for ARM (EWARM) toolchain **9.20.1** + ST-LINKV3.Patch available [here](https://github.com/STMicroelectronics/STM32CubeWBA/tree/main/Utilities/PC_Software)
 * RealView Microcontroller Development Kit (MDK-ARM) toolchain V5.39 + ST-LINKV3.Patch available [here](https://github.com/STMicroelectronics/STM32CubeWBA/tree/main/Utilities/PC_Software)
 * [STM32CubeIDE **V1.17.0**](https://www.st.com/en/development-tools/stm32cubeide.html) + ST-LINKV3


## Dependencies

This package has been developed and tested using the list of components detailed in the table below.

Name                       |   Version
---------------------------|---------------
Cortex-M CMSIS             |   V5.9.0
STM32WBAxx CMSIS           |   V1.5.0
STM32WBAxx HAL             |   V1.5.0
BSP STM32WBAxx NUCLEO      |   V1.0.3
BSP Common                 |   V7.3.0
FatFS                      |   R0.15
FreeRTOS                   |   V10.6.2

## How to use

This repository intrinsically contains the applications (projects and source files) located under folder `./Projects`.
It also contains the CMSIS Core files under folder `./Drivers/CMSIS/Include` for size optimization reason.
Other dependencies such as the HAL and BSP drivers, or the middleware libraries themselves are linked using the `git submodule` command.
Please check the instructions below for a proper use.

---

#### *Note*

* To clone this repository along with the linked submodules, option `--recursive` has to be specified as shown below.

```
git clone --recursive https://github.com/STMicroelectronics/stm32wba-classic-coremw-apps
```

* To get the latest updates, issue the following **two** commands (with the repository `stm32u5-classic-coremw-apps` as the **current working directory**).

```
git pull
git submodule update --init --recursive
```

#### *Note*

 * If GitHub "Download ZIP" option is used instead of the `git clone` command, then the required components have to be collected manually by the user.

## Known Limitations

 * None

## Troubleshooting

Please refer to the [CONTRIBUTING.md](CONTRIBUTING.md) guide.
