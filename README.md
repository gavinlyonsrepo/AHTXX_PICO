[![Website](https://img.shields.io/badge/Website-Link-blue.svg)](https://gavinlyonsrepo.github.io/)  [![Rss](https://img.shields.io/badge/Subscribe-RSS-yellow.svg)](https://gavinlyonsrepo.github.io//feed.xml)  [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/paypalme/whitelight976)

Overview
--------------------------------------------
* Name: AHTXX
* Description: 
Library for  Aosong ASAIR AHT10, AHT15 & AHT20 Digital Humidity & Temperature Sensor I2C.
Only tested on AHT10.
* Developed on
	1. Raspberry pi PICO RP2040
	2. SDK C++ compiler G++ for arm-none-eabi
	3. CMAKE , VScode

Features
----------------------

 ![o](https://github.com/gavinlyonsrepo/STM32_projects/blob/master/extra/images/aht10.jpg)
 

Library for Aosong ASAIR AHT10, AHT15 & AHT20 Digital Humidity & Temperature Sensor I2C.

1. Supply voltage:               1.8v - 3.6v for AHT10, AHT15 & 2.0v - 5.5v for AHT20
2. Temperature range:            -40°C..+85°C
3. Temperature resolution:       0.01°C
4. Temperature accuracy:         ±0.3°C
5. Relative humidity range:      0%..100%
6. Relative humidity resolution: 0.024%
7. Relative humidity accuracy:   ±2%**
8. I²C bus speed:                0Hz - 400KHz
9. Recommended polling frequency: 8sec - 30sec

Supports sensors features:

1. Read humidity
2. Read temperature
3. Soft reset with sensor initialisation
4. The library returns an errors if a communication error occurs or if the calibration coefficient is off.

**Connections**

The Sensor uses I2C for communication's. Data is outputted (eg to a PC) via a USB.
Can be set up for any I2C interface and speed. By default I2C0, GPIO16(SDATA) and GPIO17(SCLK) & 100kHz.
If you want to use the other I2C port (I2C1) in addition to changing in the main.ccp,
The user must change it in library header as well, could not find a way around this.

* i2c_inst_t *i2c = i2c0 to i2c_inst_t *i2c = i2c1


**Files**

The main.cpp contains tests showing library functions
There is also an library (ahtxx.cpp and ahtxx.h),

**Output**

Data is outputted (eg to a PC) via a USB .
 ![o1](https://github.com/gavinlyonsrepo/STM32_projects/blob/master/extra/images/aht10output.jpg)