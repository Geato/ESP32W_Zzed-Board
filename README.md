ESP32W_Zzed-Board
=================

This Altium project is a remake of the classic ESP32W “DOIT” dev board but
including a real time clock, DS3231 (U5), a LiPo charger (U8) and a coin cell.

The RTC controls the enable pin on the regulator (U7). Upon an alarm compare
interrupt, the regulator is enabled and the module powers up. Asserting GPIO 33
high will put the board back into power down mode. The RTC is kept alive with a
CR1220 / 1225 lithium cell.

Switch SW3 will force a wakeup should the user need to wake the board before the
programmed sample interval. Jumper P5 enables the RTC function OR permanently
enables the LP5912 so the board never goes into power down mode. This is helpful
in case there are issues in the firmware that need to be resolved.

P4 is for future expansion. Possibly a camera board with a PIR motion sensor.
Motion will wake the ESP32 and take a photo …
