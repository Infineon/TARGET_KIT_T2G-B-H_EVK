# KIT_T2G-B-H_EVK BSP Release Notes
The KIT_T2G-B-H_EVK, a 272-pin evaluation board is based on the TRAVEO T2G family of devices. T2G-B-H MCU is designed for  industrial applications. The evaluation board carries a T2G-B-H microcontroller, a M.2 interface connector for interfacing  radio modules based on AIROC™ Wi-Fi and Bluetooth® combos (currently not supported), SMIF dual header compatible with Digilent  Pmod for interfacing HYPERBUS™ memories (currently not supported), and headers compatible with Arduino for  interfacing Arduino shields. In addition, the board features an on-board programmer/debugger (KitProg3),  a 512-Mbit QSPI NOR flash, CAN FD transceiver, Gigabit Ethernet PHY transceiver with RJ45 connector interface,  a micro-B connector for USB device interface, three user LEDs, one potentiometer, and two push buttons.  The board supports operating voltages from 3.3 V to 5.0 V for T2G-B-H device.

NOTE: BSPs are versioned by family. This means that version 1.2.0 of any BSP in a family (eg: XMC™ ) will have the same software maturity level. However, not all updates are necessarily applicable for each BSP in the family so not all version numbers will exist for each board. Additionally, new BSPs may not start at version 1.0.0. In the event of adding a common feature across all BSPs, the libraries are assigned the same version number. For example if BSP_A is at v1.3.0 and BSP_B is at v1.2.0, the event will trigger a version update to v1.4.0 for both BSP_A and BSP_B. This allows the common feature to be tracked in a consistent way.

### What's Included?
The KIT_T2G-B-H_EVK library includes the following:
* BSP specific makefile to configure the build process for the board
* cybsp.c/h files to initialize the board and any system peripherals
* cybsp_types.h file describing basic board setup
* Linker script & startup code for GCC and ARM toolchains
* Configurator design files (and generated code) to setup board specific peripherals
* .lib file references for all dependent libraries
* API documentation

### What Changed?
#### v1.0.0
Note: This revision is only compatible with ModusToolbox Tools 3.0 and newer.
* Initial production release

### Supported Software and Tools
This version of the KIT_T2G-B-H_EVK BSP was validated for compatibility with the following Software and Tools:

| Software and Tools                        | Version |
| :---                                      | :----:  |
| ModusToolbox™ Software Environment        | 3.0.0   |
| GCC Compiler                              | 10.3.1  |
| IAR Compiler                              | 9.30.1  |
| ARM Compiler                              | 6.16    |

Minimum required ModusToolbox™ Software Environment: v3.0.0

### More information
* [KIT_T2G-B-H_EVK BSP API Reference Manual][api]
* [KIT_T2G-B-H_EVK Documentation](https://www.infineon.com/KIT_T2G-B-H_EVK)
* [Cypress Semiconductor, an Infineon Technologies Company](http://www.cypress.com)
* [Infineon GitHub](https://github.com/infineon)
* [ModusToolbox™](https://www.cypress.com/products/modustoolbox-software-environment)

[api]: https://infineon.github.io/TARGET_KIT_T2G-B-H_EVK/html/modules.html

---
© Cypress Semiconductor Corporation (an Infineon company) or an affiliate of Cypress Semiconductor Corporation, 2019-2022.