# ecumasters_arduino
ECUMasters EMU multigauge project based on adafruit featherwing

## Parts list
1. Adafruit M0 basic proto
2. Adafruit TFT 2.5"
4. Sparkfun MAX3232 breakout
5. 3d printed case

## Wiring

The wiring is pretty basic based on the documents provided. 
We pull 3.3v off of the RS-232 port on the ECU. We wire power
from the ECU to the 3.3v port on the MAX3232 and the USB pin on
the featherwing. It's a common ground so ground will be wired 
to the GND on the MAX3232 and the featherwing.

TX from the ECU should be wired to R1IN on the MAX3232
R1OUT from the MAX3232 should be wired to the RX port 
on the featherwing

##Uploading code

Uploading the code will be a little harder. You'll need to setup 
the Arduino IDE and follow the instructions for setting up the 
adafruit feather family of products 
[here](https://learn.adafruit.com/adafruit-feather-m0-basic-proto/using-with-arduino-ide).

You'll need to edit variant.cpp in the feather_m0 and comment out the SERCOM0_Handler function
(lines 217-220).

Compile and upload!
