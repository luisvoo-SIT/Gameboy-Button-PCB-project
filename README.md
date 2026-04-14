# Gameboy-Button-PCB-project

This project aims to be a repository for various PCBs intended to allow a user to construct a high quality game controller using the Nintendo Game Boy as a basis. The primary goal is to create a gamepad that used an original or reproduction Game Boy shella and buttons and one of these PCBs in order to have the most authentic control scheme for emulation or virtual consol/Switch online gaming functionality. Eventual plans also include functionality with the original Super Famicom/Super Nintendo console in order to play with the original Super Game Boy. An additional set of shoulder buttons are included on the PCB, as well as an additional third button footprint that can be uses for a home/guide/function button. 

These PCBs support a rich set of features provided mostly in part of the wonderful GP2040-CE project [which can be found here](https://github.com/OpenStickCommunity/GP2040-CE), with Bluetooth functionality provided by @jfedor2's Slimbox-bt firmware [which can be found here.](https://github.com/jfedor2/slimbox-bt)
There are two (2) variants of the board for the original Game Boy- the "DMG-01" model. I have designed both to be a bolt-in replacement for the original button/screen PCB, with some trimming of the battery compartment being required to allow the microcontroller board and USB-C port to clear. 

### DMG2040-Pro
The DMG2040-Pro PCB uses the popular Waveshare RP2040-zero MCU, and allows the unused GPIO pins to be accessed by standard 0.1" pitch (2.54mm) pin headers. I2C and USB could be easily accessed by GPIO 28/29 (USB) and GPIO 8/9 (I2C). This board is meant to be a versatile and potentially feature rich way to make a full featured controller that will work on many different platforms- depending on your choice of firmware, of course. Additional screw mounting holes have been added for custom shell applications. (MOST CURRENT RELEASE LIVE AS OF 04/14/2026)

![DMG2040-Pro PCB design multilayer](DMG2040PROMULTI.png)


### DMG2040-Lite
The DMG2040-Lite is a stripped down, more basic version of the PCB, with the primary intention being to use the popular Seeed Studio Xiao microcontrollers- specifically the Seeed Xiao nRF52840. 
The nRF52840 is meant to be used with the lovely slimbox-bt firmware by Jfedor, found here- https://github.com/jfedor2/slimbox-bt. The Seeed Xiao RP2040 will also fit and function perfectly on this board, and if used with the GP2040-CE firmware will simply require manual configuration of the GPIO to assign the buttons to their proper functions. Additional screw mounting holes have been added for custom shell applications. (RELEASE DATE TBD)

![DMG2040-Lite PCB multilayer]( DMG2040-lite-all-03162026.png)

## Hardware setup
Coming soon!
