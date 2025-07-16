# 🔧 Embedded Systems Projects with STM32 Nucleo-F446RE (ARM Cortex-M4)

A curated collection of real-world embedded systems projects built using the STM32 Nucleo-F446RE development board. Each project demonstrates fundamental concepts such as I2C communication, PWM signal generation, servo and motor control, analog signal acquisition, and ultrasonic distance sensing — all implemented using STM32CubeIDE and HAL drivers.

---

## 📁 Repository Structure

| Project Folder                | Description |
|------------------------------|-------------|
| `GatewayV1.1`, `GatewayV1.2` | Modular gateway between STM32 peripherals (I2C, PWM, ADC) – improved versioning |
| `I2C_Master_Receiver`        | Receives data from an I2C slave (e.g., angle/sensor reading) |
| `I2C_Master_Servo`           | Sends angle over I2C to a slave that rotates a servo |
| `I2C_Slave_Servo`            | Receives angle via I2C and drives SG90 servo motor |
| `I2C_Slave_Transmitter`      | Sends data from slave to master over I2C |
| `Master_ExternalPullUp`      | Stable I2C master setup with external pull-up resistors |
| `Slave_ExternalPullUp`       | Slave implementation with optimized signal integrity |
| `Master_Request` / `Slave_Request` | Implements request-response communication pattern over I2C |
| `PWM`                        | PWM signal generation for motors, LEDs, and servos |
| `Servo`                      | Drives SG90 servo via PWM using timer configuration |
| `Servo_PWM_FT7135M`          | Custom PWM for FT7135M servo (different pulse specs) |
| `L298N_Motor_Driver_Module`  | Controls direction and speed of a DC motor via L298N H-Bridge |
| `POT`                        | Reads analog voltage using ADC and displays/stores the value |
| `UltraSonic`                 | Measures distance using HC-SR04 ultrasonic sensor |

---

## 🧰 Tools & Technologies

- **MCU**: STM32 Nucleo-F446RE (ARM Cortex-M4)
- **IDE**: STM32CubeIDE
- **Language**: Embedded C with STM32 HAL Drivers
- **Communication**: I2C (Master-Slave), UART (optional debug), PWM
- **Other**: External interrupts, timers, analog input (ADC)

---

## 🧱 Hardware Requirements

| Component             | Purpose |
|-----------------------|---------|
| STM32 Nucleo-F446RE   | Main MCU board |
| L298N Motor Driver    | H-bridge for bidirectional motor control |
| SG90 / FT7135M Servo  | PWM-controlled actuators |
| HC-SR04 Sensor        | Distance measurement (ultrasonic) |
| Potentiometer         | Analog voltage source |
| Jumper Wires & Breadboard | Circuit prototyping |
| 4.7kΩ Resistors       | I2C pull-ups (if not internal) |
| Power Supply          | 5V and 12V as needed for motors/servos |

---

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/AhmedShawada/ARM_Nucleof446RE_Projects.git
