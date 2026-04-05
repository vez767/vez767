# Hi, I'm Wanaemi Alagoa

### Year 2 Computer Engineering Student | Embedded Systems | Low-Level Architecture 

I am a second-year Computer Engineering student fascinated by how software dictates physical action.

Rather than relying on high-level abstractions, I am dedicated to mastering low-level systems architecture. I believe it is the critical foundation that ensures any physical system, regardless of its scale or application, can safely and deterministically execute its core tasks.

I specialize in writing memory-safe and fault-tolerant firmware in C, specifically optimized for ARM architectures to extract maximum performance and reliability from resource-constrained devices.

My engineering philosophy is user-centric: To design robust state machines that prioritize the end-user's safety, anticipate severe edge cases, and guarantee reliability even when the physical hardware is compromised. 

Currently, I am executing a self-driven curriculum to bridge academic theory with production-grade, safety-critical architecture.

---

###  Programming Languages

![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=white) 
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white) 
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

I utilize C to interface directly with hardware registers, manage memory, and implement fault-tolerant architecture on silicon. I am also adept with C++ and use Python for rapid scripting and data analysis

---

###  Core Tech Stack & Hardware Integration

![STM32](https://img.shields.io/badge/STM32-03234B?style=for-the-badge&logo=stmicroelectronics&logoColor=white) 
![ARM](https://img.shields.io/badge/ARM_Cortex--M-0091D4?style=for-the-badge&logo=arm&logoColor=white) 
![AVR](https://img.shields.io/badge/AVR_ATmega328P-00979C?style=for-the-badge&logo=arduino&logoColor=white)
![STM32CubeIDE](https://img.shields.io/badge/STM32CubeIDE-03234B?style=for-the-badge&logo=stmicroelectronics&logoColor=white)
![VSCode](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white) 
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

**Silicon & Microcontrollers:**
* **STM32F Series (ARM Cortex-M):** Primary target for bare-metal C development, direct-register manipulation, and advanced memory/clock management.
* **ATmega328P (Arduino Uno R3):** Used for baseline 8-bit prototyping and comparative architecture analysis.

**Hardware Subsystems & Protocols:**
* **Core Silicon:** RCC (Reset and Clock Control), NVIC (Nested Vectored Interrupt Controller), Hardware Timers (TIM/PWM).
* **Communication & I/O:** I2C, UART, 1-Wire Bus, GPIO, EXT-I (External Interrupts).

**Instrumentation & Tooling:**
* **Hardware Debugging:** 8-Channel USB Logic Analyzers (for verifying physical clock drift and microsecond timing constraints), SWD (Serial Wire Debug), and Live Expressions telemetry.
* **Software Environment:** STM32CubeIDE, VS Code, Git (utilizing traceable, requirement-driven commit structures).

---

### Curriculum & Development Roadmap

To ensure I am building a versatile and enterprise-ready engineering foundation, I am executing a strict, multi-tiered roadmap. This curriculum bridges localized bare-metal firmware with distributed, multi-threaded architectures.

- [x] **Tier 0: Software Foundations** - Core C mechanics, memory constraints, and pointer arithmetic.
- [ ] **Tier 1: Bare-Metal Firmware (Current)** - Direct-register peripheral drivers, Independent Watchdogs (IWDG), Flash CRC (Cyclic Redundancy Check), and hardware clock calibration.
- [ ] **Tier 2: RTOS & Automated Verification** - Migrating synchronous blocking loops to **FreeRTOS** (Hardware Interrupts, Mutexes, Stack Watermarking) and implementing Unity/Ceedling for automated test-driven development.
- [ ] **Tier 3: The Linux IoT Gateway** - Networking localized STM32 sensor arrays to heavier Linux environments for distributed system streaming.

---

### Featured Architecture

#### [Bare-Metal Sensor Driver Suite (HC-SR04)](https://github.com/vez767/Hardware-Timers)

Engineered a system-safe, highly deterministic state machine suite capable of dynamic acoustic tracking and active fail-safe hardware recovery.

* *Architecture Highlight:* Explicitly bypassed standard abstraction libraries (HAL) by manually mapping core memory base addresses and peripheral offsets (e.g., RCC, GPIO, TIM). 
* *Event-Driven Execution:* Transitioned from synchronous blocking loops to asynchronous, hardware-level interrupts utilizing the ARM Cortex-M NVIC, ensuring the CPU remains available for multi-sensor data fusion.
* *Process:* Strictly adhered to a traceable, requirement-driven SDLC Git workflow (e.g., `feat(hcsr04): implement slew-rate filter [REQ-002]`).


#### [8-Bit ADC Engine & Interrupt Controller](https://github.com/vez767/Hardware_Interupts)

Engineered an event-driven Analog-to-Digital Converter (ADC) engine, bypassing synchronous polling methods to guarantee deterministic CPU availability during continuous analog measurements.

* **Architecture Highlight:** Configured the silicon specifically for 8-bit resolution to strictly minimize total conversion time. Manually mapped memory offsets for the ADC, RCC, and GPIO subsystems.
* **Asynchronous Execution:** Orchestrated the EXTI (External Interrupt/Event Controller) and NVIC to trigger and handle analog-to-digital conversions entirely via hardware-level interrupts, eliminating CPU wait states.
* **Hardware Fault Detection (Analog Watchdog):** Configured the ADC's High and Low Threshold Registers (HTR/LTR) to establish strict operational voltage boundaries. Leveraged dedicated ADC interrupts to autonomously trigger a physical LED warning state the moment out-of-bounds telemetry was detected, creating a hardware-enforced safety mechanism without software overhead.

---


![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white) https://www.linkedin.com/in/wanaemi-alagoa-0711b8327/







![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white) 
  wa3960f@gre.ac.uk
