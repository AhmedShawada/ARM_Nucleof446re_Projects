# 🔧 Embedded Systems Projects with STM32 Nucleo-F446RE (ARM Cortex-M4)

A curated collection of real-world embedded systems projects built using the **STM32 Nucleo-F446RE** development board. Each project demonstrates fundamental concepts such as I2C communication, PWM signal generation, servo and motor control, analog signal acquisition, and ultrasonic distance sensing — all implemented using **STM32CubeMX** and **STM32CubeIDE**.

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

- **STM32CubeMX** – Peripheral configuration, clock tree, pin assignment (.ioc file)  
- **STM32CubeIDE** – Code editing, HAL library integration, compiling & debugging  
- **Language**: Embedded C (HAL-based)  
- **Protocols**: I2C, UART, ADC, PWM  
- **Timers & Peripherals**: TIMx, ADCx, GPIOx, NVIC  

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

## ⚙️ Development Workflow (STM32CubeMX + CubeIDE)

1. **Project Creation**  
   - Start with `STM32CubeMX`
   - Select `Nucleo-F446RE` board  
   - Enable peripherals (e.g., I2C1, TIM2, ADC1)  
   - Set clock configuration  
   - Assign GPIO pins to each feature

2. **Code Generation**  
   - Click `Generate Code` → opens in `STM32CubeIDE`  
   - HAL drivers and initialization code are auto-generated  
   - All configurations are stored in `.ioc` file (included in each project)

3. **Firmware Development**  
   - Add application logic in `main.c` and `user code` sections  
   - Use HAL functions for sensor reading, PWM control, I2C comm, etc.  
   - Optional: add `printf()` via UART for debugging

4. **Build and Flash**  
   - Connect STM32 via USB  
   - Click "Build" and "Debug" in STM32CubeIDE  
   - Monitor output or motor/sensor response

---

## 🧪 Example Use Cases

| Project                  | Real Application |
|--------------------------|------------------|
| `I2C_Master_Servo`       | Send commands to a remote-controlled robotic arm |
| `POT` + `PWM`            | Map analog control to motor/LED intensity |
| `L298N_Motor_Driver_Module` | Control direction and speed of a smart car |
| `UltraSonic`             | Integrate object detection in autonomous systems |
| `Gateway`                | Central hub to connect multiple I2C, PWM, and analog devices |

---

## 🧠 Code Concepts Covered

- Configuring timers for PWM  
- Reading analog voltage via ADC  
- Using STM32CubeMX `.ioc` for pin and peripheral mapping  
- Sending and receiving data over I2C (HAL-level)  
- Real-time signal processing for servos and sensors  
- Interrupt-based distance sensing (ultrasonic)

---

## 📄 License

This project is licensed under the terms of the [MIT License](LICENSE).

You are free to:

- ✅ Use the code in personal or commercial projects
- 🔧 Modify and adapt it to your needs
- 🚀 Distribute or share it publicly

**Requirement:** You must include attribution to the original author (Ahmed Shawada) in any distribution or derivative work.

> 📌 This means you can build on top of this code freely — just don’t remove my name as the original creator.

For full details, please refer to the [LICENSE](LICENSE) file.


---

## 👤 Author

**Ahmed Shawada**  
🔗 [LinkedIn](https://www.linkedin.com/in/ahmed-shawada)  
💼 Engineer | Embedded Systems Enthusiast  
📍 Based in Egypt

---

## ⭐ Star This Repo

If this helped you understand embedded systems better, please consider starring the repo!

---

## 📥 Clone This Repository

```bash
git clone https://github.com/AhmedShawada/ARM_Nucleof446RE_Projects.git

