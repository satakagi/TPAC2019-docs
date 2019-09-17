# [Web GPIO](https://github.com/browserobo/WebGPIO) and [Web I2C](https://github.com/browserobo/WebI2C)
API specifications that allows WebApps to use devices connected to GPIO or I2C on a single board computer.
Specifications are edited by [Browsers and Robotics CG](https://www.w3.org/community/browserobo/).

# [CHIRIMEN Project](https://chirimen.org)
CHIRIMEN is an open source software and open source hardware community.　They are developing an environment where various electronic parts and devices can be operated from WebApps.The core of the implementation is an APIs for GPIO and I2C.

They are also developing [learning/tutorial materials](https://tutorial.chirimen.org) for beginners of WebApps and IoT technology.

# Implementations
Except for B2G, WebI2C and WebGPIO are implemented by polyfills.

## CHIRIMEN for [Raspberry PI3](https://www.raspberrypi.org/)
Localhost Node server provides GPIO and I2C pin services. Polyfill on the browser provides WebGPIO and I2C by communicating with the Node server via WebSocket. Everything works on RPi3.
![conf rpi3](https://qiita-user-contents.imgix.net/http%3A%2F%2Fgc.dfm.lrv.jp%2F0.secerror%2Farchitecture.png?ixlib=rb-1.2.2&auto=compress%2Cformat&fit=max&s=2982bb219c6a4eed787da4d5b81e12a4)

## CHIRIMEN with [micro:bit](https://microbit.org/)
The polyfill on the browser operates the micro:bit pins via Web Bluetooth. A program that provides GPIO and I2C pin operations via BLE is implemented on micro:bit. WebApps runs on a browser on a PC or smartphone.
![conf microbit](https://github.com/chirimen-oh/chirimen-micro-bit/blob/master/imgs/chirimenMicrobitDiagram.png)

## CHIRIMEN with ty51822r3
Mbed single board computer using Nordic Semiconductor's [nRF51822](https://www.nordicsemi.com/Products/Low-power-short-range-wireless/nRF51822). The structure is almost similar to CHIRIMEN with micro: bit.

## CHIRIMEN on B2G Open Source Hardware Single Board Computer
WebGPIO and WebI2C are implemented natively on B2G.
The community designed an open source hardware board computer designed for Boot to Gecko (an open source version of Firefox OS). Board computer production has already ended.

# Already Supported Devices / Parts

As a textbook for beginners, the community has developed drivers for various I2C devices, especially for I2C devices. They are javascript libraries using WebI2C. This makes it easy to use I2C devices.
There are already drivers for many of the well-known I2C devices on the market.


|a  |b  |c  |
|---|---|---|
|1  |2  |3  |
|4  |5  |6  |
