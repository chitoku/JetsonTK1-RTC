# JetsonTK1-RTC
RTC module for Jetson TK1

# What this is

This module is to give a battery backup RTC functionality to Jetson TK1, aside other minor features.

## RTC

The main feature of this board is to give a battery backup RTC functionality to Jetson TK1.
The module is designed to be placed on the J3A1 (2x25) expansion header of Jetson TK1 and is designed to be used with Santyago's Grinch Custom Kernel.
The RTC fuctionality was verifid on the initial revision of the assembled board and was cofirmed to be working in the way written  [here](http://elinux.org/Jetson/RTC). 

## Grove connectors

The board also has two Grove I2C connectors, intended to accomodate 3.3V I2C Grove modules, however they are not yet tested.
For Grove system, please refere [here](http://www.seeedstudio.com/wiki/Grove_System).

## Barometer sensor

Supplementary, the board is intended to give an accesss to MPL115A2 barometer sensor, but this sensor does not work on the initial revision of the assembled board. (See "Attention" section)

# Attribute

The design of the circuit and the basic setup is based on Santyago's [this](https://devtalk.nvidia.com/default/topic/769727/embedded-systems/-howto-battery-backup-rtc/) Hot-To.
The Grinch Custom Kernel is a work of [Santyago](https://devtalk.nvidia.com/member/1982212/).

# Attention!

The barometic sensor, MPL115A2 did not work on the initial revision of the assembled board.
It is later found that the pull-up on RST/CS pin (pin5) is mssing, so this is suspected to be the cause. 
More investigation and a fix is desired.
