```markdown
# Betaflight Pixhawk Compatibility List

## Overview

This repository tracks **Pixhawk-style flight controllers that can run or be adapted to run Betaflight firmware**.

Although Betaflight is traditionally designed for FPV flight controllers, many modern Pixhawk-compatible boards share similar STM32 MCU architectures, making experimental Betaflight builds possible.

The goal of this project is to document:

- Compatible Pixhawk-style flight controllers  
- Hardware configurations  
- Sensor compatibility  
- Experimental Betaflight firmware builds  

This information may be useful for UAV developers, FPV builders and embedded engineers exploring alternative firmware platforms.

---

## Hardware Overview

Several modern Pixhawk-style flight controllers share similar hardware architectures.

### MCU

Typical processors include:

- STM32F405  
- STM32F722  
- STM32H743 (H7 series)

For example, the Kakute H7 flight controller uses:

- **STM32H743 MCU**
- Running up to **480 MHz**
- Higher processing capability compared to F4/F7 controllers

---

### IMU Sensor

Flight performance heavily depends on the **IMU (Inertial Measurement Unit)**.

Example configuration from Kakute H7 hardware:

**IMU:** CM-42688-P  

Features:

- High-performance 6-axis IMU  
- Low-noise gyro and accelerometer  
- High sampling rate suitable for FPV control loops  
- Supported in modern Betaflight firmware

The CM-42688-P IMU provides stable gyro data even under high vibration environments typical in FPV drones.

---

### Other Hardware Features

Typical Pixhawk-style Betaflight capable boards include:

- Multiple UART interfaces (often 6+)  
- I2C interface for GPS / magnetometer  
- OSD chip (AT7456E)  
- Blackbox logging via MicroSD  
- ESC outputs for up to 8 motors  
- 3S–8S battery input support  
- Built-in BEC regulators  

These features make them flexible for both **FPV drones and experimental UAV platforms**.

---

## IMU Component Availability

In recent years, sourcing IMU sensors has become an important issue for many flight controller manufacturers.

Common IMUs used in flight controllers include:

- MPU6000  
- ICM42688  
- BMI270  

Due to supply chain changes and EOL issues, many developers are exploring **alternative IMU solutions** that maintain compatibility with existing flight control firmware.

Some projects are currently evaluating **alternative IMU components**, including domestic IMU solutions that can potentially replace commonly used sensors while maintaining stable flight performance.

---

## Current Testing Hardware

| Flight Controller | MCU | IMU | Status |
|------------------|-----|-----|-------|
| Kakute H7 | STM32H743 | CM-42688-P | Tested |
| Kakute F722 | STM32F722 | MPU6000 / ICM42688 | Testing |
| Kakute F4 V2.4 | STM32F405 | MPU6000 | Stable |

---

## Experimental Betaflight Firmware

Custom Betaflight builds are currently being tested for:

- STM32H7 flight controllers  
- Pixhawk-style hardware  
- Alternative IMU sensor configurations  

Testing focuses on:

- Gyro stability  
- PID loop performance  
- Sensor compatibility  
- Blackbox logging  

---

## IMU Alternative Research

Another focus of this project is evaluating **compatible IMU replacements for flight controllers**.

Many hardware teams are currently searching for:

- alternative IMU sources  
- drop-in replacements for common sensors  
- solutions compatible with Betaflight firmware  

Several IMU replacement solutions are currently under evaluation.

If you are developing **flight controllers, drone autopilots, or UAV hardware** and are facing IMU supply challenges, feel free to open a discussion.

---

## Community Contributions

Contributions are welcome.

If you have experience running Betaflight on Pixhawk-style hardware, please feel free to:

- Open an Issue  
- Submit a Pull Request  
- Share hardware test results  

---

## Disclaimer

This repository is intended for research and hardware experimentation.

Running alternative firmware on Pixhawk-style hardware may require advanced knowledge of embedded systems and flight control tuning.
If you wish to obtain technical support, please contact me
telegram：@zaqm88
email：luhaoy2023@gmail.com
```


