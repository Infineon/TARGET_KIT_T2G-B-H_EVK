# KIT_T2G-B-H_EVK BSP

## Overview

The KIT_T2G-B-H_EVK, a 272-pin evaluation board is based on the TRAVEO T2G family of devices. T2G-B-H MCU is designed for  industrial applications. The evaluation board carries a T2G-B-H microcontroller, a M.2 interface connector for interfacing  radio modules based on AIROC™ Wi-Fi and Bluetooth® combos (currently not supported), SMIF dual header compatible with Digilent  Pmod for interfacing HYPERBUS™ memories (currently not supported), and headers compatible with Arduino for  interfacing Arduino shields. In addition, the board features an on-board programmer/debugger (KitProg3),  a 512-Mbit QSPI NOR flash, CAN FD transceiver, Gigabit Ethernet PHY transceiver with RJ45 connector interface,  a micro-B connector for USB device interface, three user LEDs, one potentiometer, and two push buttons.  The board supports operating voltages from 3.3 V to 5.0 V for T2G-B-H device.     
**Note:**
Some additional setups will allow you to use more code examples than those shown on the next page. Click 
[here ](https://github.com/Infineon/TRAVEO_T2G_code_examples#how-to-setup)
for setup instructions.



To use code from the BSP, simply include a reference to `cybsp.h`.

## Features

### Kit Features:

* CYT4BFBCHE 8MB Flash 272-pin BGA device
* Programming interface (Arm® Standard JTAG, Cortex® Debug + ETM with Arm® ETM Mictor)
* Reset control with manual reset switch and voltage supervision
* Gigabit Ethernet interface
* CAN FD interface
* M.2 interface connector to connect radio modules based on AIROC™ Wi-Fi & Bluetooth® combos (currently not supported)
* 512-Mbit external Quad SPI NOR Flash that provides a fast, expandable memory for data and code
* KitProg3 on-board SWD programmer/debugger, USB-UART and USB-I2C bridge functionality
* A micro-B connector for USB device interface
* Selectable input supply voltages of 3.3 V and 5.0 V for the T2G-B-H device
* Three user LEDs, two user buttons, and a reset button for the T2G-B-H device
* A potentiometer which can be used to simulate analog sensor output
* A mode button and a mode LED for KitProg3

### Kit Contents:

* T2G-B-H evaluation board
* USB Type-A to Micro-B cable
* 12V/3A DC power adapter with additional blades
* Six jumper wires
* Quick start guide

### Low-level Driver References:

* See 
[Hardware abstraction layer (HAL) library](https://infineon.github.io/mtb-hal-cat1/html/modules.html)
* See 
[Peripheral driver library (PDL) library](https://infineon.github.io/mtb-pdl-cat1/pdl_api_reference_manual/html/index.html)

## BSP Configuration

The BSP has a few hooks that allow its behavior to be configured. Some of these items are enabled by default while others must be explicitly enabled. Items enabled by default are specified in the bsp.mk file. The items that are enabled can be changed by creating a custom BSP or by editing the application makefile.

Components:
* Device specific category reference (e.g.: CAT1) - This component, enabled by default, pulls in any device specific code for this board.

Defines:
* CYBSP_WIFI_CAPABLE - This define, disabled by default, causes the BSP to initialize the interface to an onboard wireless chip if it has one.
* CY_USING_HAL - This define, enabled by default in some BSPs, specifies that the HAL is intended to be used by the application. This will cause the BSP to include the applicable header file and to initialize the system level drivers.  Newer BSPs pull in the v3.x HAL, which enables itself via its own makefile, so CY_USING_HAL is not present.
* CYBSP_CUSTOM_SYSCLK_PM_CALLBACK - This define, disabled by default, causes the BSP to skip registering its default SysClk Power Management callback, if any, and instead to invoke the application-defined function `cybsp_register_custom_sysclk_pm_callback` to register an application-specific callback.

### Clock Configuration

| Clock    | Source    | Output Frequency |
|----------|-----------|------------------|
| FLL      | ECO       | 100.0 MHz        |
| PLL      | ECO       | 80.0 MHz         |
| CLK_HF0  | CLK_PATH3 | 200 MHz          |
| CLK_HF1  | CLK_PATH1 | 350 MHz          |
| CLK_HF2  | CLK_PATH4 | 80 MHz           |
| CLK_HF3  | CLK_PATH3 | 100 MHz          |
| CLK_HF4  | CLK_PATH2 | 125 MHz          |
| CLK_HF5  | CLK_PATH2 | 125 MHz          |
| CLK_HF6  | CLK_PATH3 | 200 MHz          |
| CLK_HF7  | CLK_PATH5 | 0 MHz            |

### Power Configuration

* System Idle Power Mode: Deep Sleep
* VDDA Voltage: 3300 mV
* VDDD Voltage: 3300 mV

See the [BSP Setttings][settings] for additional board specific configuration settings.

## API Reference Manual

The KIT_T2G-B-H_EVK Board Support Package provides a set of APIs to configure, initialize and use the board resources.

See the [BSP API Reference Manual][api] for the complete list of the provided interfaces.

## More information
* [KIT_T2G-B-H_EVK BSP API Reference Manual][api]
* [KIT_T2G-B-H_EVK Documentation](https://www.infineon.com/evaluation-board/KIT-T2G-B-H-EVK/)
* [Cypress Semiconductor, an Infineon Technologies Company](http://www.cypress.com)
* [Infineon GitHub](https://github.com/infineon)
* [ModusToolbox™](https://www.cypress.com/products/modustoolbox-software-environment)

[api]: https://infineon.github.io/TARGET_KIT_T2G-B-H_EVK/html/modules.html
[settings]: https://infineon.github.io/TARGET_KIT_T2G-B-H_EVK/html/md_bsp_settings.html

---
© Cypress Semiconductor Corporation (an Infineon company) or an affiliate of Cypress Semiconductor Corporation, 2019-2025.