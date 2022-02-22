# MMOD

## Overview

MMOD is a 3.3V SPI memory module used in Lone Dynamics computers in order to allow for user-replaceable and user-upgradeable memory. The module is inserted into the MMOD socket with the top-side components facing the host board.

![MMOD](https://github.com/machdyne/mmod/blob/7bfb2f9bef0166ed6ebf4ede923fc044ab3f9810/mmod.png)

MMOD modules are compatible with Pmod&trade; Interface Type 2 (SPI) and can be used in 6 or 12 pin Pmod&trade; sockets (with the top-side components facing up), but Pmod modules are not necessarily compatible with MMOD sockets due to differences in size and requirements.

This repo contains specifications, pinouts, footprints and schematics.

## Pinout

| Pin | Signal |
| --- | ------ |
| 1 | SS |
| 2 | MOSI |
| 3 | MISO |
| 4 | SCK |
| 5 | GND |
| 6 | PWR3V3 |

## Dimensions

Width: 16.5mm (parallel with header)
Length: 12.5mm max (perpendicular to header)
Height: 8mm max (top of header to top of bottom-side components)

## MMOD Board Requirements

- The top-side components must not touch the host board.
- The module must not interfere with the SPI bus unless SS is asserted (low).
- The module should provide decoupling capacitors for the memory.
- The module should provide any necessary pull-up/down resistors for the memory.
- SPI SS should be pulled high with a 10K resistor.
- SPI MOSI, MISO and SCK should have no pull-up/down resistors.
- The module must not draw more than 50mA current at any time.
