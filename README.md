# Building a Matter over Thread Accessory Device based on the Silicon Labs EFR32xG24 Explorer Kit (BRD2703A Rev A02)
### Author: [Olav Tollefsen](https://www.linkedin.com/in/olavtollefsen/)

## Introduction

This article shows how to build a Matter Air Quality sensor with an Silicon Labs EFR32xG24 Explorer Kit board and a Sensirion SEN66 air quality sensor. The Sensirion SEN66 sensor connects to the Silicon Labs EFR32xG24 Explorer Kit using I2C and supports measuring Particulate Matter (PM1, PM2.5, PM4, PM10), Relative Humidity, Temperature, Volatile Organic Compound, NOx (nitrogen oxides) and CO2.

![Silicon Labs EFR32xG24 Explorer Kit](./images/xg24-ek2703a.png)
![Sensirion SEN66 Air Quality Sensor](./images/sensirion-sen66.png)

### What you will need

- A Mac computer as the development workstation
- A Silicon Labs EFR32xG24 Explorer Kit board
- A Sensirion SEN66 air quality sensor

## Connect the hardware

![SEN66 pin assignment](./images/sen66-pin-assignment.png)

The recommended voltage is 3.3V.

![EFR32xG24 Explorer Kit Connectors](./images/xg24-ek2703a-connectors.png)

## Create a new project based on the "Matter - SoC Sensor over Thread with external Bootloader" Solution Example

Start by creating a new project in Simplicity Studio V5 by selecting the "Matter - SoC Air Quality Sensor with internal Bootloader Solution" example solution project and click "Create":

![Matter - SoC Air Quality Sensor with internal Bootloader Solution](./images/matter-air-quiality-example-solution.png)

This is a good starting point as it already implements a fully functional Matter over Thread device.

Build the solution to make sure it builds with no errors.

## Add the I2C drivers to your project

Open the .slcp file in your project and select "SOFTWARE COMPONENTS".

Search for the I2CSPM component as shown below and install it:

![Install I2CSPM](./images/install-i2cspm.png)

Select "qwiic" as the instance name.

![Select instance name](./images/select-i2cspm-instance-name.png)

## Add support for USTIMER to your project

Open the .slcp file in your project and select "SOFTWARE COMPONENTS".

Search for the USTIMER component as shown below and install it:

![Install USTIMER](./images/install-ustimer.png)

## Copy SEN66 I2C driver source files into your project

You will find I2C driver source files in this Github repo:

https://github.com/Sensirion/embedded-i2c-sen66

Copy the .h files to your include directory and the .c files to your src directory.




