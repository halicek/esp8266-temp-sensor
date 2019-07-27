# ESP8266 temperature sensor for IoT
Wireless temperature sensor to be used in your next IoT project. :) Quite low consumption, months with single 18650 cell.

## Features:
- Wireless connectivity (ESP8266 12E)
- SHT30 temperature sensor
- low voltage cut-off
- I2C and other free pins accessible via pads
- approx 47 mm x 19 mm size (including 12E)
- position for smd resetable fuse (not used on my prototype)

![ESP8266 Temp Sensor v3](https://raw.githubusercontent.com/halicek/esp8266-temp-sensor/master/iot-pcb-front.png)

## Used IOs:
- ESP8266 12E uController
- Sensirion SHT30 temperature sensor
- STM1061 3.4 V voltage monitor
- MCP1603T 3.3 V synchronous buck voltage regulator

Why so high voltage cut-off? It seems that around 3.0 V input regulator will not supply enough power for ESP8266 to perform well so this regulator meant for 3.3V power level seems appropriate. Please prove how wrong I am! :) 

## Used firmware:
ESP Easy. https://www.letscontrolit.com/wiki/index.php/ESPEasy Tested and working with ESPEasy Mega package 20190511. The SHT330 support is currently only in test branch, so I recommend using "ESP_Easy_mega-20190511_test_core_260_sdk222_alpha_ESP8266_4M.bin" firmware. Caution: Your ESP8266 may not boot or work properly when started in AP mode, I recommend to supply the credentials via post-flash actions in ESP Easy Flasher or via Serial interface (more fun, don!t forget to "Save" the changes.)

## Bill of materials:
I have used Farnell for nearly all of my purchases. Only inductors were purchased on TME.eu (just because I've purchased bad ones with low Isat and the shipping from Farnell was too high.)

- 1x (5 in package) Snap-on battery contact - 3029803 (bigger were out of stock)
- 2x SKRBAGE010 SWITCH, 1.1N, 4.8X4.8MM, LOW PROFILE - 2056852

- 1x EEEFT0J221AR CAP, 220µF, 6.3V, RADIAL, SMD - 2065953
- 1x EEE0JA101WR CAP, 100µF, 6.3V, SMD - 2807989
- 1x MC0805X475K100CT CAP, 4.7µF, 10V, 10%, X5R, 0805

- 1x SHT30-DIS-P2.5KS HUMIDITY/TEMP SENSOR, DIGITAL, DFN-8 - 2886652
- 1x STM1061N34WX6F MPU SUPERVISOR/MONITOR - 3129930
- 1x MCP1603T-330I/OS V REG, SYNCH BUCK 0.5A, SMD - 1439373

- 5x RC0805FR-0710KL RES, 10K, 1%, 0.125W, 0805 - 9237755
- 2x CRGH0805F4K7 RES, 4K7, 1%, 0.33W, 0805 - 2332080

- 1x Inductor from TME.eu - 0603 SMD, 4.7 uH, 600mA Isat - NL03JTC4R7 (you generally need an inductor with parameters recommended in MCP1603T datasheet).

## Warning:
There could be some libraries missing in the project. Let me know, I will fix this as I am still learning with kicad and this is my first published project. Just let me know.

## Status

**As of today (July 2019) this is working prototype, third generation of board design with three working prototypes in my flat. Anyway, build at your own risk! And do not forget that 18650 cells can burn too!**

![prototype v3](https://raw.githubusercontent.com/halicek/esp8266-temp-sensor/master/prototype.jpg)

## What I need to finish:
- 3D printed case - i have some preliminary holder for 18650 cell. - https://github.com/halicek/esp8266-temp-sensor/blob/master/Temp-sensor-case-v1.stl

## License:
This is open hardware, use, make, modify. Just let me know any improvement. I will welcome any fix or upgrade. Thank you!
