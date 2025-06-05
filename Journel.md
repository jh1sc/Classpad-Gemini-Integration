---
title: "Classpad-Gemini-Intergration"
author: "jh1sc"
description: "Trying to hook up the fx-CP400 (Classpad II) to the internet and more over connect it to Googles Gemini Ai through it's API"
date created: "30/05/2025" 
---
# Journel

## 30/5/2025
> Research stuff

#### Specs of fx-CP400 (Classpad II) 
Useful resource: [Calc specs and more](https://classpaddev.github.io/)

| General          | CPU                            | Memory                      | Connector                                         | Battery                                                                 |
| :--------------- | :----------------------------- | :-------------------------- | :------------------------------------------------ | :---------------------------------------------------------------------- |
| Weight: 315 grams | SuperH 4 (SH7305) processor | Total Memory: 64 MB<br>User Memory: 512 KB | USB Mini-B / 3pin cable<br>(up to 115.2 kilobits/s) | Power: 4 AAA alkaline or<br>nickel-metal hydride batteries<br>Power Consumption: 1.0 W - 100 hours in use |

#### Serial Communication 
  * TX (Transmit): this pin sends data out of calc 
  * RX (Receive): this pin receives data in to the calc
  * GND: Common electrical reference point (0 Volts) 
    - When connected to the ESP32, TX pin connects to the calcs RX pin and vice versa, and obv grounds need to connect
    - Total Voltage must sum to 0, as if not data would be garbled

