# Betaflight Pixhawk Compatibility List

Overview

This repository tracks Pixhawk-style flight controllers that can run or be adapted to run Betaflight firmware.

Although Betaflight is traditionally designed for FPV flight controllers, many modern Pixhawk-compatible boards share similar STM32 MCU architectures, making experimental Betaflight builds possible.

The goal of this project is to document:

Compatible Pixhawk-style flight controllers

Hardware configurations

Sensor compatibility

Experimental Betaflight firmware builds

This information may be useful for UAV developers, FPV builders and embedded engineers exploring alternative firmware platforms.

Hardware Overview

Several modern Pixhawk-style flight controllers share similar hardware architectures:

MCU

Typical processors include:

STM32F405

STM32F722

STM32H743 (H7 series)

For example, the Holybro Kakute H7 Flight Controller uses:

STM32H743 MCU

Running up to 480MHz

Significantly higher performance than typical F4/F7 controllers

IMU Sensor

Flight performance is heavily dependent on the IMU (Inertial Measurement Unit).

Example configuration from the Kakute H7 hardware:

IMU:
CM-42688-P

Features:

High-performance 6-axis IMU

Low noise gyro and accelerometer

High sampling rate suitable for FPV control loops

Widely supported in modern Betaflight firmware

The CM-42688-P IMU provides stable gyro data even under high vibration environments typical in FPV drones.

Other Hardware Features

Typical Pixhawk-style Betaflight capable boards include:

Multiple UART interfaces (often 6+)

I2C interface for GPS / magnetometer

OSD chip (AT7456E)

Blackbox logging via MicroSD

ESC output for up to 8 motors

3S–8S battery input support

Built-in BEC regulators

These features make them highly flexible for both FPV drones and experimental UAV platforms.

IMU Component Availability

In recent years, sourcing IMU sensors has become an important issue for many flight controller manufacturers.

Commonly used IMUs include:

MPU6000

ICM42688

BMI270

However, supply chain fluctuations and EOL status of some sensors have pushed many developers to explore alternative IMU solutions.

Some projects are currently evaluating compatible IMU alternatives that can replace commonly used sensors while maintaining Betaflight performance.

These alternatives may include domestic or regionally manufactured IMU solutions suitable for flight control applications.

Current Testing Hardware

The following boards are currently under testing with Betaflight builds:

Flight Controller	MCU	IMU	Status
Kakute H7	STM32H743	CM-42688-P	Tested
Kakute F722	STM32F722	MPU6000 / ICM42688	Testing
Kakute F4 V2.4	STM32F405	MPU6000	Stable
Experimental Betaflight Firmware

Custom Betaflight builds are being tested for:

STM32H7 flight controllers

Pixhawk-style boards

alternative IMU sensor configurations

Testing focuses on:

gyro stability

PID loop performance

sensor compatibility

blackbox logging

IMU Alternative Research

Another focus of this project is evaluating compatible IMU replacements for flight controllers.

Many developers and hardware teams are currently looking for:

alternative IMU sources

drop-in replacements for common sensors

solutions compatible with existing Betaflight firmware

Several IMU replacement solutions are currently under evaluation, including options designed to be compatible with common FPV flight controller hardware.

If you are developing flight controllers, drone autopilots, or UAV hardware and are facing IMU supply issues, feel free to open a discussion.

Community Contributions

Contributions are welcome.

If you have experience running Betaflight on Pixhawk-style hardware, please feel free to:

open an Issue

submit a Pull Request

share hardware test results

Disclaimer

This repository is intended for research and hardware experimentation.

Running alternative firmware on Pixhawk-style hardware may require advanced knowledge of embedded systems and flight control tuning.
If you wish to obtain technical support, please contact me
telegram：@zaqm88
email：luhaoy2023@gmail.com
