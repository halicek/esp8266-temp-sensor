# ESP8266 temperature sensor for IoT
Wireless temperature sensor to be used in your next IoT project. :) Quite low consumption, months with single 18650 cell.

## Features:
- Wireless connectivity (ESP8266 12E)
- SHT30 temperature sensor
- low voltage cut-off
- I2C and other free pins accessible via pads
- approx 47 mm x 19 mm size (including 12E)

![ESP8266 Temp Sensor v 1.3](https://raw.githubusercontent.com/halicek/esp8266-temp-sensor/master/iot-pcb-front.png)

## Used IOs:
- ESP8266 12E uController
- Sensirion SHT30 temperature sensor
- STM1061 3.4 V voltage monitor
- MCP1603T 3.3 V synchronous buck voltage regulator

## Used firmware:
ESP Easy. https://www.letscontrolit.com/wiki/index.php/ESPEasy Tested and working with ESPEasy Mega package 20190511. The SHT330 support is currently only in test branch, so I recommend using "ESP_Easy_mega-20190511_test_core_260_sdk222_alpha_ESP8266_4M.bin" firmware. Caution: Your ESP8266 may not boot or work properly when started in AP mode, I recommend to supply the credentials via post-flash actions in ESP Easy Flasher or via Serial interface (more fun, don!t forget to "Save" the changes.)

## Warning:
There could be some libraries missing in the project. Let me know, I will fix this as I am still learning with kicad and this is my first published project. Just let me know.

## Status

**As of today (July 2019) this is working prototype, third generation of board design with three working prototypes in my flat. Anyway, build at your own risk! And do not forget that 18650 cells can burn too!**

## What I need to finish:
- 3D printed case - i have some preliminary holder for 18650 cell.

## License:
This is open hardware, use, make, modify. Just let me know any improvement. I will welcome any fix or upgrade. Thank you!
