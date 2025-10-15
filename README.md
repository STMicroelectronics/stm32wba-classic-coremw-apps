# STM32WBA Classic Core Middleware (CoreMW) MCU Firmware Package

![latest tag](https://img.shields.io/github/v/tag/STMicroelectronics/stm32wba-classic-coremw-apps.svg?color=brightgreen)

![fatfs](https://img.shields.io/badge/fatfs-R0.15-blue.svg)

## Description

**STM32Cube** is an STMicroelectronics original initiative to ease developers' life by reducing efforts, time and cost.

**Classic CoreMW** is a collection of middleware stacks and associated applications allowing RTOS management, File System operations and connectivity through USB. It is based on:
* ST's proprietary stacks: ST USB Device and ST USB Host
* Third parties' stacks: FatFS

This package is **exclusively** published on GitHub (and is neither available in STM32CubeMX nor STM32CubeIDE available on www.st.com).
It contains the integration of the Classic CoreMW stacks with *STM32WBA* devices, allowing users to get quick access to pre-built projects integrating them.

#### *Note*

 * The repository containing this package has been created using the `git submodule` command. Please refer to the ["How to use"](README.md#how-to-use) section explaining how to clone this repository and how to get the latest updates.

## Release note

Details about the content of this release are available in the release note [here](https://htmlpreview.github.io/?https://github.com/STMicroelectronics/stm32wba-classic-coremw-apps/blob/main/Release_Notes.html).

## List of applications

The **STM32WBA Classic CoreMW** package contains the following applications:

Middleware    | Application                            | Short Description
--------------|----------------------------------------|------------------------------------------------------------------------
FatFs	      | FatFs_RAMDISK_Standalone               | Shows a typical application where the STM32 MCU write and read back a Fat Format text file from RAMDISK
ST USB Device | HID_Standalone                         | Shows a typical application where the STM32 MCU is enumerated as a HID device
ST USB Device | CDC_Standalone                         | Shows a typical application where the STM32 MCU is enumerated as a CDC device
ST USB Host   | HID_Standalone                         | Shows how to use USB host application based on the Human Interface Class (HID) to connect a mouse or a keyboard
ST USB Host   | CDC_Standalone                         | Shows how to use USB host application based on the Communication Device Class (CDC) to communicate with a usb flash disk

#### *Note*
 * *FreeRTOS* Middleware and examples are delivered on STM32WBA in the form of X-CUBE-FREERTOS that is available from [st.com](https://www.st.com/en/embedded-software/x-cube-freertos.html), from [GitHub](https://github.com/STMicroelectronics/x-cube-freertos) and from STM32CubeMX.
 * Projects in this package have not been generated with STM32CubeMX (**i.e.**, no `.ioc` files are delivered).

## Boards available

 * STM32WBA
   * [NUCLEO-WBA55CG](https://www.st.com/en/evaluation-tools/nucleo-wba55cg.html)
   * [NUCLEO-WBA65RI](https://www.st.com/en/evaluation-tools/nucleo-wba65ri.html)

## Development Toolchains and Compilers

 * IAR Embedded Workbench for ARM (EWARM) toolchain **9.60.3** + ST-LINKV3.Patch available [here](https://github.com/STMicroelectronics/STM32CubeWBA/tree/main/Utilities/PC_Software)
 * RealView Microcontroller Development Kit (MDK-ARM) toolchain V5.39 + ST-LINKV3.Patch available [here](https://github.com/STMicroelectronics/STM32CubeWBA/tree/main/Utilities/PC_Software)
 * [STM32CubeIDE **V2.0.0**](https://www.st.com/en/development-tools/stm32cubeide.html) + ST-LINKV3


## Dependencies

This package has been developed and tested using the list of components detailed in the table below.

Name                       |   Version
---------------------------|---------------
Cortex-M CMSIS             |   V5.9.0
STM32WBAxx CMSIS           |   V1.7.0
STM32WBAxx HAL             |   V1.7.0
BSP STM32WBAxx NUCLEO      |   V1.1.0
BSP Common                 |   V7.3.0
FatFS                      |   R0.15
STM32 USB Device Library   |   V2.11.4
STM32 USB Host Library     |   V3.5.3

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
