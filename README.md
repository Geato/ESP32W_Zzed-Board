ESP32W_Zzed-Board
=================

This is the classic ESP32W “DOIT” dev board but with a real time clock, DS3231
(U5) configured to enable the regulator (U7) upon an alarm compare interrupt.
Asserting GPIO 33 high will put the board into power down mode. The RTC is kept
alive with a CR1220 / 1225 lithium cell.

Switch SW3 will force a wakeup should the user need to wake the board before the
programmed sample interval. Jumper P5 enables the RTC function or permanently
enables the LP5912 so the board never goes into power down mode. This is helpful
in case there are issues in the firmware that need to be resolved.

There is also a LiPo charger (U8) to a battery with a capacity of \~ 2000mA-H.

P4 is for future expansion. Possibly a camera board with a PIR motion sensor.
Motion will wake the ESP32 and take a photo …
