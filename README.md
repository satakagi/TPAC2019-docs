# CHIRIMEN Project

CHIRIMEN is an open source software and open source hardware community.　They are developing an environment where various electronic parts and devices can be operated from WebApps, and preparing tutorial materials.

The core of the implementation is an APIs for GPIO and I2C, based on the WebGPIO and WebI2C specifications edited by Browsers and Robotics CG.

# Implementations
Except for B2G, WebI2C and WebGPIO are implemented as polyfills.

## CHIRIMEN for Raspberry PI3
![conf rpi3](https://qiita-user-contents.imgix.net/http%3A%2F%2Fgc.dfm.lrv.jp%2F0.secerror%2Farchitecture.png?ixlib=rb-1.2.2&auto=compress%2Cformat&fit=max&s=2982bb219c6a4eed787da4d5b81e12a4)

## CHIRIMEN with micro:bit
![conf microbit](https://github.com/chirimen-oh/chirimen-micro-bit/blob/master/imgs/chirimenMicrobitDiagram.png)

## CHIRIMEN for TY

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
