# Bogdan Kuljanin | Control Systems & Embedded

Control systems engineer with a focus on embedded systems. My background is in controls engineering, system modelling, and simulation. On this GitHub you'll mostly find STM32 firmware projects focused on low-level development.

I'm interested in the intersection of control theory and embedded software, from sensor interfacing and signal processing on microcontrollers to the modelling and simulation work that supports it.

---

## Quick Links

| Category | Projects |
|:---------|:---------|
| [SPI Drivers](#spi-drivers) | IMU (DMA, HAL, Sensor Fusion + SD) |
| [I2C Drivers](#i2c-drivers) | IMU (Polling, Interrupt, HAL) |
| [UART Drivers](#uart-drivers) | GPS (Polling, DMA) |
| [CAN Bus](#can-bus) | Two board CAN communication |
| [Sensor Drivers](#sensor-drivers) | Ultrasonic, Load Cell, Current Sensor |
| [PWM & ADC](#pwm--adc) | Edge/Center aligned PWM, ADC with DMA |
| [Build System](#build-system) | Custom Makefile + Linker Script + Startup |

---

## SPI Drivers

**[STM32-SPI-DMA-IMU-Driver](https://github.com/BKuljanin/STM32-SPI-DMA-IMU-Driver)**
Bare metal SPI1 driver using DMA for reading MPU6500 IMU. Full duplex burst reads with DMA TX+RX, data ready interrupt driven sampling.

**[STM32-SPI-IMU-HAL-Driver](https://github.com/BKuljanin/STM32-SPI-IMU-HAL-Driver)**
Polling based SPI driver using HAL for MPU6500.

**[STM32-IMU-FUSION-SD](https://github.com/BKuljanin/STM32-IMU-FUSION-SD)**
Real time IMU sensor fusion combining SPI1+DMA IMU reading, complementary filter attitude estimation (roll + pitch), and SD card CSV logging via FATFS over SPI2.

---

## I2C Drivers

**[STM32-I2C-IMU-Driver](https://github.com/BKuljanin/STM32-I2C-IMU-Driver)**
Bare metal I2C implementation using polling. Reads accelerometer, gyroscope, and temperature from MPU6500.

**[STM32-I2C-IRQ-IMU](https://github.com/BKuljanin/STM32-I2C-IRQ-IMU)**
I2C driver for MPU6500 using interrupt based transfers.

**[STM32-I2C-IMU-HAL-Driver](https://github.com/BKuljanin/STM32-I2C-IMU-HAL-Driver)**
HAL based I2C driver for MPU6500.

---

## UART Drivers

**[STM32-UART-DMA-GPS-Driver](https://github.com/BKuljanin/STM32-UART-DMA-GPS-Driver)**
UART DMA driver for GY-NEO6MV2 GPS module. Includes NMEA sentence parsing and PC communication.

**[STM32-UART-GPS-Driver](https://github.com/BKuljanin/STM32-UART-GPS-Driver)**
UART polling based GPS driver with sentence parsing.

---

## CAN Bus

**[STM32-CAN-LINK](https://github.com/BKuljanin/STM32-CAN-LINK)**
CAN communication between two boards: Nucleo F446RE and STM32 F103C6T6 (bluepill).

---

## Sensor Drivers

**[STM32-HCSR04-Ultrasonic-Driver](https://github.com/BKuljanin/STM32-HCSR04-Ultrasonic-Driver)**
HC-SR04 ultrasonic sensor driver for distance measurement.

**[STM32-HX711-LoadCell-Driver](https://github.com/BKuljanin/STM32-HX711-LoadCell-Driver)**
HX711 load cell amplifier driver. Bit banged serial protocol with tare and weight reading.

**[STM32-ADC-DMA-Current-Sensor](https://github.com/BKuljanin/STM32-ADC-DMA-Current-Sensor)**
Current sensor reading via ADC with DMA data transfer.

---

## PWM & ADC

**[STM32-Center-Aligned-PWM-With-ADC-Sync](https://github.com/BKuljanin/STM32-Center-Aligned-PWM-With-ADC-Sync)**
Center aligned PWM generation with ADC triggering in the middle of the pulse. ADC configured in DMA mode.

**[STM32-Edge-Aligned-PWM](https://github.com/BKuljanin/STM32-Edge-Aligned-PWM)**
Bare metal edge aligned PWM generation with configurable output.

---

## Build System

**[STM32-MAKE-BUILD-SYSTEM](https://github.com/BKuljanin/STM32-MAKE-BUILD-SYSTEM)**
Bare metal STM32 firmware built with a custom GNU Make build system. Includes startup code, linker script, and OpenOCD flashing. No IDE required.
