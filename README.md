# JetsonTK1-RTC
RTC module for Jetson TK1

# What this is

This module is to give a battery backup RTC functionality to Jetson TK1.
The module is designed to be placed on the J3A1 (2x25) expansion header of Jetson TK1 and is designed to be used with Santyago's Grinch Custom Kernel.

Aside from the RTC, the board is intended to give an accesss to MPL115A2 barometic sensor, but this sensor is NOT verified to work on the initial revision of the assembled board. (See "Attention" section)

# Attribute

The design of the circuit and the basic setup is based on Santyago's this [https://devtalk.nvidia.com/default/topic/769727/embedded-systems/-howto-battery-backup-rtc/] Hot-To.

# Attention!

The barometic sensor, MPL115A2 did not work on the assembled board.
It is later found that the pull up on RST/CS (pin5) is mssing, and this might be the cause. 
Fix is desired.
