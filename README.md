# 🚀 ARM_Nucleof446RE_Projects

This repository contains a practical collection of embedded systems projects built using the **STM32 Nucleo-F446RE** board, focusing on low-level hardware control, I2C communication, PWM signal generation, ultrasonic sensing, and custom protocol handling. These projects were built using **STM32CubeMX**, **STM32CubeIDE**, and **HAL drivers**, and are intended for learning, experimentation, and building real-world embedded systems.

---

## 📁 Project Overview

| Folder Name                     | Description                                                            |
|--------------------------------|------------------------------------------------------------------------|
| `I2C_Master`                   | Basic I2C master setup and transmission example                        |
| `I2C_Master_Receiver`          | I2C master reading data from a slave device                            |
| `I2C_Master_Servo`             | Control servo motor using I2C master communication                     |
| `I2C_Master_ServoFT7135M`      | I2C-based servo control with FT7135M (special motor driver)            |
| `I2C_Slave`                    | Basic STM32 I2C slave configuration                                    |
| `I2C_Slave_Servo`              | STM32 slave receiving I2C commands to control servo                    |
| `I2C_Slave_ServoFT7135M`       | FT7135M servo control via STM32 I2C slave                              |
| `I2C_Slave_Transmitter`        | STM32 slave sending data to I2C master                                 |
| `Master_ExternalPullUp`        | I2C master with external pull-up resistors handling                    |
| `Master_Request`               | Master initiating request–response protocol                           |
| `PWM`                          | Generate PWM signals for LED or motor control                          |
| `RCCF103`                      | RCC setup for STM32F103 (cross-reference test)                         |
| `RCCNucleoF446`                | Clock configuration for STM32F446RE                                    |
| `Servo`                        | Basic servo motor control via PWM                                      |
| `Servo_PWM_FT7135M`            | Servo PWM using FT7135M motor controller                               |
| `Slave_ExternalPullUp`         | I2C slave handling external pull-up resistors                          |
| `Slave_Request`                | Slave responds to master-initiated data request                        |
| `Test_I2C_With_Motion`         | Motion-based control using I2C communication                          |
| `UltraSonic`                   | HC-SR04 ultrasonic sensor for distance measurement                     |

---

## 🧠 What You'll Learn

- Configure **STM32 I2C as Master/Slave**
- Communicate with peripherals using **custom protocols**
- Control **servo motors** with **PWM**
- Integrate **ultrasonic sensors**
- Explore **inline ARM assembly**
- Manage **RCC clock systems** for STM32

---

## 🛠️ Tools & Technologies

- STM32 Nucleo-F446RE (ARM Cortex-M4)
- STM32CubeMX & STM32CubeIDE
- HAL Driver Layer in C
- Keil uVision (optional)
- NRF24L01 (in some tests)
- FT7135M driver (motor control)

---

## ⚙️ How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/AhmedShawada/ARM_Nucleof446RE_Projects.git
