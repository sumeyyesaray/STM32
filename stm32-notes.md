# 🛠 STM32

## What is STM32?
STM32 is a family of **microcontrollers** produced by STMicroelectronics, based on **ARM architecture**. It is commonly used in embedded systems.  
ARM (Advanced RISC Machine) → A low-power, high-efficiency processor architecture based on RISC (Reduced Instruction Set Computer).  
It is widely used in microcontrollers like STM32 as well as in phones, tablets, and similar devices.
-Includes cortes processor.
<img width="881" height="216" alt="image" src="https://github.com/user-attachments/assets/edd3357a-edb1-4066-9f6c-4af82789f2a4" />

---

## 🧠 What is a Microcontroller?

- A single chip that includes **CPU**, **RAM**, **Flash/ROM**, and **I/O units**.
- Can directly interact with hardware and peripheral devices.
- Typically performs fixed tasks (e.g., washing machines, robot vacuums).
- Operates with **low clock speed** and **limited RAM**.

---

## 💻 What is a Microprocessor?

- An integrated circuit that contains only the **CPU**.
- Memory and I/O units are connected externally.
- Designed for general-purpose computing (e.g., desktop computers).
- Features **high clock speed** and **large RAM capacity**.

---

## 🔁 Comparison

| Feature         | Microcontroller (MCU)         | Microprocessor (CPU)          |
|------------------|-------------------------------|-------------------------------|
| Components       | CPU + RAM + ROM + I/O         | Only CPU                      |
| Clock Speed      | Low                           | High                          |
| Memory Capacity  | Limited                       | Large                         |
| Use Case         | Embedded systems              | Computers, smartphones, etc.  |

### 🔧 STM32 Microcontroller Categories

The STM32 series is classified based on use case as follows:

- 🚀 **High Performance**: For applications requiring high processing power (e.g., STM32H7, F7)  
- ⚙️ **Mainstream**: Balanced performance for general-purpose use (e.g., STM32F1, F4)  
- 🌱 **Ultra-Low Power**: For low-power, energy-efficient systems (e.g., STM32L0, L4)  
- 📡 **Wireless**: Models with integrated wireless connectivity (e.g., STM32WB, WL)

# STM32F4 Discovery Board

The **STM32F4 Discovery** board is based on the **STM32F407VGT6** microcontroller (ARM Cortex‑M4, 168 MHz).  
It comes with an **embedded ST-LINK/V2** for programming and debugging, making it ideal for rapid prototyping.  

![STM32F4 Discovery](f8bcc433-2613-4719-97b4-7c9350182443.png)

---

## Features

| Feature                | Description                                 |
|------------------------|---------------------------------------------|
| **MCU**                | STM32F407VGT6 (Cortex-M4, 168 MHz)           |
| **Programming**        | Embedded ST-LINK/V2 via Mini USB             |
| **GPIO & Headers**     | All main pins are exposed for prototyping    |
| **User Input**         | 1x User Button (B1), 1x Reset Button (B2)    |
| **LEDs**               | 8x (Green, Red, Blue, Orange)                |
| **Sensors**            | LIS302DL accelerometer, MP45DT02 microphone  |
| **Audio**              | CS43L22 DAC with audio output (jack)         |
| **Connectivity**       | Mini USB (programming), Micro USB (power)    |

---

## Quick Start

1. Connect the board to your PC using **Mini USB**.  
2. Flash your firmware or start **debugging** using ST-LINK.  
3. Use GPIO pins, LEDs, and the user button for quick prototyping.  

> 💡 **Tip:** All LEDs, buttons, and sensors are ready for immediate use in your projects.  

---


