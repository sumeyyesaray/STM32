ingi# 🛠 STM32

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

<img width="1587" height="761" alt="image" src="https://github.com/user-attachments/assets/a36d95a3-f98c-469e-b1ec-cd3e928246e3" />



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

### 🕒 System Clock & Oscillator

- **System Clock**: The system clock drives the timing and synchronization of all operations in an STM32 microcontroller, including CPU speed, peripherals, and timers.
- **Oscillator**: A circuit that generates the base clock signal. STM32 devices can use internal RC oscillators or external crystal oscillators. Crystals offer higher precision, especially in time-critical applications.

### ⏱️ STM32 Clock Sources

STM32 microcontrollers support various internal and external clock sources:

#### 🔸 Internal Oscillators
- **HSI (High-Speed Internal):** 16 MHz internal RC oscillator. No external components needed, moderate accuracy.
- **LSI (Low-Speed Internal):** ~32 kHz internal RC oscillator. Used in low-power modes and for watchdog timers.

#### 🔹 External Oscillators
- **HSE (High-Speed External):** 4–25 MHz crystal oscillator. Provides high-precision clock for system operation.
- **LSE (Low-Speed External):** 32.768 kHz crystal oscillator. Commonly used with RTC for accurate timekeeping.
-  **PLL(Phase-Locked Loop):** is a clock multiplier circuit used to generate higher frequencies from a lower-frequency source (e.g., HSI or HSE).
- It allows the system clock (SYSCLK) to run at higher speeds than the original oscillator.
- Example: 8 MHz HSE → PLL ×9 → 72 MHz System Clock.
- PLL is commonly used in STM32 projects requiring high CPU or peripheral performance.

  ## STM32F4 Clock Tree

The **Clock Tree** in STM32F4 defines how the microcontroller generates and distributes clock signals to the CPU and peripherals.

<img width="383" height="575" alt="image" src="https://github.com/user-attachments/assets/40c918bb-f87a-4559-999d-6e8da8ff2acf" />


---

### **Key Points**
- **Clock Sources:**  
  - **HSI (16 MHz)** – Internal high-speed oscillator  
  - **HSE (8/16 MHz)** – External crystal oscillator  
  - **LSI/LSE** – Low-speed clocks (for RTC, Watchdog)  

- **PLL (Phase-Locked Loop):**  
  - Multiplies the input clock to achieve higher SYSCLK frequencies (up to 168 MHz).  

- **SYSCLK (System Clock):**  
  - Main CPU clock, generated from PLL, HSE, or HSI.  

- **Clock Distribution:**  
  1. SYSCLK → **AHB Bus** (core & memory)  
  2. AHB → **APB1 / APB2** buses with prescalers  
  3. APB buses → **Peripheral Clocks** (UART, TIM, ADC, SPI, etc.)  

> 💡 **Flow:** Clock Source → PLL → SYSCLK → AHB/APB → Peripherals

---

### **Usage Tip**
When configuring the clock in STM32CubeIDE:  
1. Choose the **main clock source** (HSE or HSI).  
2. Set **PLL multipliers** to reach the desired system frequency.  
3. Adjust **AHB/APB prescalers** for peripherals.


✅ Quick Tip:

Using your own hardware → Use MCU Selector
Using an official dev board → Use Board Selector
Want to learn via examples → Use Example Selector

