# Building a Matter over Thread Accessory Device based on the Silicon Labs EFR32xG24 Explorer Kit (BRD2703A Rev A02)
### Author: [Olav Tollefsen](https://www.linkedin.com/in/olavtollefsen/)

## Introduction

This article shows how to build a Matter Air Quality sensor with an Silicon Labs EFR32xG24 Explorer Kit board and a Sensirion SEN66 air quality sensor. The Sensirion SEN66 sensor connects to the Silicon Labs EFR32xG24 Explorer Kit using I2C and supports measuring Particulate Matter (PM1, PM2.5, PM4, PM10), Relative Humidity, Temperature, Volatile Organic Compound, NOx (nitrogen oxides) and CO2.

![Silicon Labs EFR32xG24 Explorer Ki](./images/exg24-ek2703a.png)
![Sensirion SEN66 Air Quality Sensor](./images/sensirion-sen66.png)

### What you will need

- A Mac computer as the development workstation
- Espressif ESP32-C6-DEVKITC-1-N8 Dev Kit board
- Sensirion SEN66 air quality sensor
