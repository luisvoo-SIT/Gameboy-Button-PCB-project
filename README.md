# Gameboy-Button-PCB-project

This project aims to be a repository for various PCBs intended to allow a user to construct a high quality game controller using the Nintendo Game Boy as a basis. The primary goal is to create a gamepad that used an original or reproduction Game Boy shella and buttons and one of these PCBs in order to have the most authentic control scheme for emulation or virtual consol/Switch online gaming functionality. Eventual plans also include functionality with the original Super Famicom/Super Nintendo console in order to play with the original Super Game Boy. An additional set of shoulder buttons are included on the PCB, as well as an additional third button footprint that can be uses for a home/guide/function button. 

These PCBs support a rich set of features provided mostly in part of the wonderful GP2040-CE project [which can be found here](https://github.com/OpenStickCommunity/GP2040-CE), with Bluetooth functionality provided by @jfedor2's Slimbox-bt firmware [which can be found here.](https://github.com/jfedor2/slimbox-bt)
There are two (2) variants of the board for the original Game Boy- the "DMG-01" model. I have designed both to be a bolt-in replacement for the original button/screen PCB, with some trimming of the battery compartment being required to allow the microcontroller board and USB-C port to clear. 

### DMG2040-Pro
The DMG2040-Pro PCB uses the popular Waveshare RP2040-zero MCU, and allows the unused GPIO pins to be accessed by standard 0.1" pitch (2.54mm) pin headers. I2C and USB could be easily accessed by GPIO 28/29 (USB) and GPIO 8/9 (I2C). This board is meant to be a versatile and potentially feature rich way to make a full featured controller that will work on many different platforms- depending on your choice of firmware, of course. Additional screw mounting holes have been added for custom shell applications. (MOST CURRENT RELEASE LIVE AS OF 04/14/2026)

![DMG2040-Pro PCB design multilayer](DMG2040-pro-all-03162026.png)


### DMG2040-Lite
The DMG2040-Lite is a stripped down, more basic version of the PCB, with the primary intention being to use the popular Seeed Studio Xiao microcontrollers- specifically the Seeed Xiao nRF52840. 
The nRF52840 is meant to be used with the lovely slimbox-bt firmware by Jfedor, found here- https://github.com/jfedor2/slimbox-bt. The Seeed Xiao RP2040 will also fit and function perfectly on this board, and if used with the GP2040-CE firmware will simply require manual configuration of the GPIO to assign the buttons to their proper functions. Additional screw mounting holes have been added for custom shell applications. (RELEASE DATE TBD)

![DMG2040-Lite PCB multilayer]( DMG2040-lite-all-03162026.png)

## Installation and configuration
Refer to the instructions given by your chosen firmware for detailed software installation instructions. Once the firmware has been installed It is recommended that you confirm function before soldering the microcontroller board to the Game Boy button PCB. 

-The DMG2040-Pro will work with the standard GP2040-CE firmware file without additional configuration for the buttons, but will require configuration via the Web Configurator utility to assign any additional function to the GPIO pins, such as I2C, USB passthrough, or additional buttons. The shoulder and home buttons are by default assigned as TSW3= `B3`, TSW4= as `B4` and TSW9= `A1` using GP2040-CE nomenclature. Standard button assignment on the PCB is B1= `A`, B2= `B`, S1= `Select`, and s2= `Start`. Please keep in mind using input mode `Nintendo Switch` will swap the functions for B1/B2 and may require a custom profile to prevent this if your use case has you swapping between consoles/devices.

-The DMG2040-Lite when using the Seeed Xiao nRF52840 Microcontroller will work with the Slimbox-BT `slimbox-bt-xiao_nrf52840.uf2` firmware file without additional configuration for the buttons. The shoulder and home buttons are by default assigned as TSW3- `West`, TSW4 as `North` and TSW9 ``Home using Jfedor's slimbox-bt nomenclature. If you use the Seeed RP2040 Microcontroller with the Gp2040-CE firmware you will need to maually configure the GPIO pin assignments to line up with the chosen button configuration.

## Hardware setup
Coming soon!
