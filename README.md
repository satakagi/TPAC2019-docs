# [Web GPIO](https://github.com/browserobo/WebGPIO) and [Web I2C](https://github.com/browserobo/WebI2C)
API specifications that allows WebApps to use devices connected to GPIO or I2C on a single board computer.
Specifications are edited by [Browsers and Robotics CG](https://www.w3.org/community/browserobo/).

# [CHIRIMEN Project](https://chirimen.org)
CHIRIMEN is an open source software and open source hardware community.　They are developing an environment where various electronic parts and devices can be operated from WebApps.The core of the implementation is an APIs for GPIO and I2C.

They are also developing [learning/tutorial materials](https://tutorial.chirimen.org) for beginners of WebApps and IoT technology.

## Activity intention
Rather than practical, for prototyping and learning.

However, such educational board computers and their use cases have a huge market for both Rasoberry PI and micro:bit, so it makes sense to make them web-friendly.

# Implementations
Except for B2G, WebI2C and WebGPIO are implemented by polyfills.

## CHIRIMEN for [Raspberry PI3](https://www.raspberrypi.org/)
Localhost Node server provides GPIO and I2C pin services. Polyfill on the browser provides WebGPIO and I2C by communicating with the Node server via WebSocket. Everything works on RPi3.

![conf rpi3](https://qiita-user-contents.imgix.net/http%3A%2F%2Fgc.dfm.lrv.jp%2F0.secerror%2Farchitecture.png?ixlib=rb-1.2.2&auto=compress%2Cformat&fit=max&s=2982bb219c6a4eed787da4d5b81e12a4)

## CHIRIMEN with [micro:bit](https://microbit.org/)
The polyfill on the browser operates the micro:bit pins via Web Bluetooth. A program that provides GPIO and I2C pin operations via BLE is implemented on micro:bit. WebApps runs on a browser on a PC or smartphone.

Instead of Web Bluetooth, Implementation via Web USB is also planned.

![conf microbit](https://github.com/chirimen-oh/chirimen-micro-bit/blob/master/imgs/chirimenMicrobitDiagram.png)

## CHIRIMEN with ty51822r3
Mbed single board computer using Nordic Semiconductor's [nRF51822](https://www.nordicsemi.com/Products/Low-power-short-range-wireless/nRF51822). The structure is almost similar to CHIRIMEN with micro: bit.

## CHIRIMEN on B2G Open Source Hardware Single Board Computer
WebGPIO and WebI2C are implemented natively on B2G.
The community designed an open source hardware board computer designed for Boot to Gecko (an open source version of Firefox OS). Board computer production has already ended.

# Already Supported Devices / Parts

As learning materials for beginners, the community has developed drivers/libraries for various devices, especially for I2C devices. They are javascript libraries using WebI2C. This makes it easy to use I2C devices.　Therefore, it is common to all board computers (RPi3, micro: bit etc).

There are over thirty drivers for well-known parts/devices available for a few dollars from amazon/ebay/aliexpress.

## I2C Devices

|Category|Device||Picture|
|-|-|-|-|
|Analog to Digital|ADS1015|![](imgs/ADS1015.jpg)|
|^^|ADS1115|![](imgs/ADS1115.jpg)|
|ADC and DAC|PCF8591|![](imgs/PCF8591.jpg)|
|Temperature|ADT7410|![](imgs/ADT7410.jpg)|
|Thermo Graphy|AMG8833|![](imgs/AMG8833.jpg)|
|Temperature, Pressure, Humidity|BME280|![](imgs/BME280.jpg)|
|Temperature, Pressure|BMP180|![](imgs/BMP180.jpg)|
|Temperature, Pressure|BMP280|![](imgs/BMP280.jpg)|
|Laser Ranging Sensor|GP2Y0E03|![](imgs/GP2Y0E03.jpg)|
|Time-of-flight distance sensor|VL53L0X|![](imgs/VL53L0X.jpg)|
|Gesture Sensor|Grove-Gesture|![](imgs/Grove-Gesture.jpg)|
|Light Sensor|Grove-Light|![](imgs/Grove-Light.jpg)|
|OledDisplay|Grove-OledDisplay|![](imgs/Grove-OledDisplay.jpg)|
|Touch Sensors|Grove-Touch|![](imgs/Grove-Touch.jpg)|
|Color Sensor|S11059|![](imgs/S11059.jpg)|
|Ultraviolet (UV) light sensor |VEML6070|![](imgs/VEML6070.jpg)|
|Accelerometer|Grove-Accelerometer|![](imgs/Grove-Accelerometer.jpg)|
|Accelerometer + Gyroscope|MPU6050|![](imgs/MPU6050.jpg)|
|Gyro + Accelerometer + Compass|MPU9250|![](imgs/MPU9250.jpg)|
|Addressable full-color LED|NEOPIXEL|![](imgs/NEOPIXEL.jpg)|
|driver board|NEOPIXEL_I2C|![](imgs/NEOPIXEL_I2C.jpg)|
|Multi-channel PWM Servo/LED driver|PCA9685|![](imgs/PCA9685.jpg)|
|^^|PCA9685_Servo2|![](imgs/PCA9685_Servo2.jpg)|

## GPIO Devices
|Category|Device||Picture|
|-|-|-|-|
|LED|LED|![](imgs/LED.jpg)|
|DC Motor|Geared Motor|![](imgs/gearedMotor.jpg)|
|Full Bridge Motor Driver|L298N|![](imgs/L298N.jpg)|
|^^|L9110S|![](imgs/L9110S.jpg)|
|^^|MX1508|![](imgs/MX1508.jpg)|
|^^|TB6612FNG|![](imgs/TB6612FNG.jpg)|
|Pyro electric Sensor||![](imgs/PIR Sensor.jpg)|

