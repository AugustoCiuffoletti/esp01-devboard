# esp01-devboard
If you come from an Arduino experience, the first experiences with the ESP-10 (and other similar WiFi-able MCUs) is
frustrating for two main reasons:
-) the switch from "Upload" to "Operate" is not fully automatic
-) the operation of the board needs a voltage of 3.3V
-) the operation of the WiFi device drains a relevant power
I designed this elementary board to help the hobbist willing to try these devices.
The board is connected to the PC (hosting a Arduino IDE) with a USB-TTL/USB-STC-ISP adapter that needs to be bought separately
(less than 10$ on Internet shops), and hosts a connector for the ESP-01 board.
An LM317 IC stabilizes an external power source, like a 9V battery or a pack of 3x1.5V batteries.
A jumper helps to change from "Bootload" to "Usage" with minimal effort
A button resets the ESP device
A set of connectors allows to connect other components to the devboard.

The components are soldered on a perfboard: we have 8 connectors, one capacitor, four resistors, one button, one battery.

CAUTION: USB-TTL/USB-STC-ISP adapters may have different pinout: the one I used in the design are:

3.3V - 5V - TXD - RXD - GND

You may have to need to change the connection of the J6 connector

Operation
Preliminary setup
-) plug the ESP-10 MCU in the middle 8-pins connector (J4-J5)
-) plug the USB-TTL/USB-STC-ISP adapter into the J6 connector
-) short the two left pins of the J7 connector with a jumper
-) push the reset button
-) plug the adapter into a USB socket in you PC
Now you are ready to upload: select your sketch (I assume that you know how to do) and upload.
In order to see your program running:
-) unplug the USB-TTL/USB-STC-ISP adapter from the J6 connector
-) remove the jumper
-) press the reset button
To flash again:
-) plug the USB-TTL/USB-STC-ISP adapter into the J6 connector
-) short again the J7 pins
-) push the reset button
and you are ready to flash again!
