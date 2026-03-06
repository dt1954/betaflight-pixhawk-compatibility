# Betaflight Pixhawk Compatibility List

This repository tracks **Pixhawk-style flight controllers that can potentially run Betaflight firmware**.

While Betaflight is traditionally used on FPV flight controllers, many modern **Pixhawk-compatible boards share similar STM32 microcontrollers and hardware architectures**, which makes experimental Betaflight firmware builds possible.

The goal of this project is to maintain a **community-driven compatibility list for Pixhawk hardware running Betaflight**.

## Why Run Betaflight on Pixhawk Hardware?

Pixhawk flight controllers are widely used in UAV research and autonomous systems, while **Betaflight provides extremely fast control loops and powerful tuning tools for FPV drones**.

Combining these two ecosystems can be useful for:

- High-performance FPV drones
- Custom UAV platforms
- Experimental flight control research
- Drone developers exploring alternative firmware

## Known Pixhawk-Compatible Flight Controllers

### H7 Based Boards

| Flight Controller | MCU | Status | Notes |
|---|---|---|---|
| Kakute H7 | STM32H743 | Tested | Stable Betaflight builds available |
| Matek H743 | STM32H743 | Experimental | Hardware compatible |
| CUAV X7 | STM32H743 | Unknown | Requires firmware port |

### F7 Based Boards

| Flight Controller | MCU | Status | Notes |
|---|---|---|---|
| Kakute F722 | STM32F722 | Tested | Compatible with custom builds |
| Matek F722 | STM32F722 | Experimental | Peripheral configuration needed |

### F4 Based Boards

| Flight Controller | MCU | Status | Notes |
|---|---|---|---|
| Kakute F4 V2.4 | STM32F405 | Tested | Works with Betaflight builds |
| Matek F405 | STM32F405 | Experimental | UART mapping required |

## Hardware Features Relevant to Betaflight

- STM32 F4 / F7 / H7 microcontrollers
- Multiple UART ports
- Onboard OSD
- Blackbox logging (Dataflash or MicroSD)
- SPI gyroscopes (MPU6000 / ICM42688)
- 3S–8S battery input support
- ESC PWM / DShot outputs

## Current Development Focus

Currently experimenting with Betaflight builds on:

- Kakute H7 (STM32H743)
- Kakute F722
- Kakute F4 V2.4

Testing includes:

- flight stability
- peripheral compatibility
- UART device support
- Blackbox logging
- FPV OSD telemetry

## Community Contributions

If you have tested Betaflight on any **Pixhawk-style flight controller**, feel free to contribute:

- open a Pull Request
- open an Issue
- share test results

## Firmware Builds

Some **experimental Betaflight firmware builds for Pixhawk hardware** are currently being tested.

If you are working with similar flight controllers and want to try running Betaflight on them, feel free to:

- open an **Issue**
- start a **Discussion**
- or contact the repository maintainer.

I may already have a working firmware build for your hardware.

## Disclaimer

This project is for **research and experimental development purposes only**.

Running alternative firmware on Pixhawk hardware may require advanced knowledge of flight controllers and embedded systems.
If you wish to obtain technical support, please contact me
telegram：@zaqm88
email：luhaoy2023@gmail.com
