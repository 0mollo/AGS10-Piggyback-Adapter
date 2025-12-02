![image alt]() | ![image alt](https://github.com/0mollo/AGS10-Piggyback-Adapter/blob/main/AGS10%20Sensor%20piggyback%20bottom%20view.png) |
# AGS10-Piggyback-Adapter
This repository contains the design files, example code, and documentation for a piggyback adapter board that enables using the ASAIR AGS10 TVOC gas sensor directly with boards such as C3-mini or D1 mini. 


## Overview

- **Sensor**: ASAIR AGS10 — a MEMS-based TVOC sensor with I²C digital output. 
- **Purpose**: Provide a compact, easy-to-assemble adapter board that plugs onto the C3-mini / D1 mini (or equivalent) for quick integration of VOC / air quality monitoring.  
- **Output**: VOC concentration (ppb) over I²C (default address: `0x1A`, with option to reassign address if multiple sensors are used)   

## Features

- Compact form factor piggyback-style adapter — no external wiring required (just plug onto host board).  
- I²C interface with SDA, SCL, GND, VCC (3.3 V recommended).  
- Example code provided for both C3-mini and D1 mini (ESP8266 / ESP-C3) to read TVOC values.  
- Ready-to-use Gerber and fabrication files.  
    

## Usage

1. Connect the adapter to your host board (e.g. C3-mini / D1 mini) ensuring proper alignment of VCC, GND, SDA, SCL.  
2. Power the board (3.0 – 3.3 V). Note: AGS10 typical operating current ~28 mA, power ~75 mW. 
3. Allow a preheat / warm-up period (~120 s) before reading stable data.  
4. Use I²C address `0x1A` to read TVOC values; example code included.  
   

## Example Code

See `examples/C3-mini_AGS10_I2C/ags10_example.ino` or `examples/D1-mini_AGS10_I2C/ags10_example.ino`.
