# JetsonTK1-RTC
RTC module for Jetson TK1

# What this is

This module is to give a battery backup RTC functionality to Jetson TK1.
The module is designed to be placed on the J3A1 (2x25) expansion header of Jetson TK1 and is designed to be used with Santyago's Grinch Custom Kernel.
The RTC fuctionality was verifid on the initial revision of the assembled board and was cofirmed to be working in the way written  [here](http://elinux.org/Jetson/RTC). 

The board also has two Grove I2C connectors, however they are not yet tested.

Aside from the RTC, the board is intended to give an accesss to MPL115A2 barometic sensor, but this sensor does not work on the initial revision of the assembled board. (See "Attention" section)

# Attribute

The design of the circuit and the basic setup is based on Santyago's [this](https://devtalk.nvidia.com/default/topic/769727/embedded-systems/-howto-battery-backup-rtc/) Hot-To.

# Attention!

The barometic sensor, MPL115A2 did not work on the initial revision of the assembled board.
It is later found that the pull-up on RST/CS pin (pin5) is mssing, so this is suspected to be the cause. 
More investigation and a fix is desired.
