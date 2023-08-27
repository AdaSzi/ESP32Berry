# Welcome to New ESP32Berry Project

## This is a new ESP32Berry project space based on T-Deck.

![T-Deck](./misc/images/t-deck.jpg)

## *Updates*

### Unit Test with LovyanGFX in Arduino Platform
Use LovyanGFX instead of TFT_eSPI to update the screen. This makes it possible to update the screen more quickly than TFT_eSPI. In order to run this without problems, first configure the development environment using the T-Deck library officially supported by LilyGO. https://github.com/Xinyuan-LilyGO/T-Deck

![T-Deck w/ LovyanGFX](./misc/images/unit_test_lovyangfx.jpg)

### *Version 0.5

- Base Structure
- LVGL Environment 
- Home Screen 
- Second Screen for Apps 
- Control Panel (Volume/Brightness)
- Dynamic WiFi Selection 
- ChatGPT Client

[![Video: Version 0.5](./misc/images/esp32berry_0.5.jpg)](https://youtu.be/5K6rSw9j5iY)

## Installation guide
### Windows
1. Arduino IDE: Download and install the latest version of the Arduino IDE from the official website (https://www.arduino.cc/en/Main/Software).
2. Install `esp32` (by Espressif) boards using `Tools` -> `Board` -> `Boards Manager`
3. In `Arduino IDE` -> `Tools` select following options:
	- `Board` -> `ESP32S3 Dev Module`
	- `USB CDC On Boot` -> `Enable`
	- `CPU Frequency` -> `240MHz`
	- `USB DFU On Boot` -> `Disable`
	- `Flash Mode` -> `QIO 80MHz`
	- `Flash Size` -> `16MB(128Mb)`
	- `USB Firmware MSC On Boot` -> `Disable`
	- `PSRAM` -> `OPI PSRAM`
	- `Partition Scheme` -> `16M Flash (3MB APP/9.9MB FATFS)`
	- `USB Mode` -> `Hardware CDC and JIAG`
	- `Upload Mode` -> `UART0/Hardware CDC`
	- `Upload Speed` -> `921600`
4. Install libraries:
	1. Copy contents of `lib` directory from https://github.com/Xinyuan-LilyGO/T-Deck to your `libraries` folder (Most likely in your `Documents/Arduino/libraries`)
	2. In `Arduino IDE` go to `Sketch` -> `Include Library` -> `Manage Libraries` search and install following libraries:
		- `LovyanGFX` by lovyan03
		- `ChatGPT_Client` by Eric Nam (**with** prerequisites)
	3. Copy `lv_conf.h` from `LVGL_Setting` to your `libraries` folder (overwrite the old one)

ESP32Berry project should now compile successfully in your Arduino IDE

### MIT License

Copyright (c) 2023 Eric Nam

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE