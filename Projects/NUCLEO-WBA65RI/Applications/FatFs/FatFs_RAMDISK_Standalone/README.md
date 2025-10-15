
## FatFs_RAMDISK_Standalone Application Description

How to use STM32Cube firmware with FatFs middleware component as a generic FAT
file system module. This example develops an application that exploits FatFs
features to configure the ram as a fat drive.

At the beginning of the main program the HAL_Init() function is called to reset
all the peripherals, initialize the Flash interface and the systick.
Then the SystemClock_Config() function is used to configure the system clock
(SYSCLK) to run at 100 MHz.

The application is based on writing and reading back a text file from a drive,
and it's performed using FatFs APIs to access the FAT volume as described
in the following steps:

 - Link the RAM disk I/O driver;
 - Register the file system object (mount) to the FatFs module for the RAM drive;
 - Create a FAT file system (format) on the RAM drive;
 - Create and Open new text file object with write access;
 - Write data to the text file;
 - Close the open text file;
 - Open text file object with read access;
 - Read back data from the text file;
 - Close the open text file;
 - Check on read data from text file;
 - Unlink the RAM disk I/O driver.

It is worth nothing that the application manages any error occurred during the
access to FAT volume, when using FatFs APIs. Otherwise, user can check if the
written text file is available on the RAM.

It is possible to fine tune needed FatFs features by modifying defines values
in FatFs configuration file "ffconf.h" available under the project includes
directory, in a way to fit the application requirements.

#### <b>Expected success behavior</b>

- A blinking blue LED light marks the success of the file operations.

#### <b>Error behaviors</b>

- On failure, the red LED should start blinking.

#### <b>Assumptions if any</b>

None.

#### <b>Known limitations</b>

None.

#### Notes

 1. Care must be taken when using HAL_Delay(), this function provides accurate delay (in milliseconds)
    based on variable incremented in SysTick ISR. This implies that if HAL_Delay() is called from
    a peripheral ISR process, then the SysTick interrupt must have higher priority (numerically lower)
    than the peripheral interrupt. Otherwise the caller ISR process will be blocked.
    To change the SysTick interrupt priority you have to use HAL_NVIC_SetPriority() function.

 2. The application needs to ensure that the SysTick time base is always set to 1 millisecond
    to have correct HAL operation.

### Keywords

FatFs, Ramdisk, File system, FAT Volume, Format, Mount, Read, Write.

### Hardware and Software environment

  - This application runs on STM32WBA65xx devices

  - This application has been tested with NUCLEO-WBA65RI board MB2130 Rev. A01 and can be
    easily tailored to any other supported device and development board.

### How to use it ?

In order to make the program work, you must do the following:
 - Open your preferred toolchain
 - Rebuild all files and load your image into target memory
 - Run the application
