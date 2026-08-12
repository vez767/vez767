# Hi, I'm Wanaemi Alagoa

### Year 3 Computer Engineering Student | Embedded Systems | Low-Level Architecture 

I am a third-year Computer Engineering student fascinated by how software dictates physical action.

Rather than relying on high-level abstractions, I am dedicated to mastering low-level systems architecture. I believe it is the critical foundation that ensures any physical system, regardless of its scale or application, can safely and deterministically execute its core tasks.

I specialize in writing memory-safe and fault-tolerant firmware in C, specifically optimized for ARM architectures to extract maximum performance and reliability from resource-constrained devices.

My engineering philosophy is user-centric: To design robust state machines and hardware-level safe fallbacks that prioritize the end-user's safety, anticipate severe edge cases, and guarantee reliability even when the physical hardware is compromised. To ensure enterprise readiness, I strictly adhere to a traceable, requirement-driven SDLC (Software Development Life Cycle) Git workflow, documenting hardware constraints and architectural intent at every stage.

Currently, I am executing a self-driven curriculum to bridge academic theory with production-grade, safety-critical architecture.

---

###  Programming Languages

![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=white) 
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white) 
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

I utilize C to interface directly with hardware registers, manage memory, and implement fault-tolerant architecture on silicon. I am also proficient in C++ and have foundational experience with Python.

---

###  Core Tech Stack & Hardware Integration

![STM32](https://img.shields.io/badge/STM32-03234B?style=for-the-badge&logo=stmicroelectronics&logoColor=white) 
![ARM](https://img.shields.io/badge/ARM_Cortex--M-0091D4?style=for-the-badge&logo=arm&logoColor=white) 
![AVR](https://img.shields.io/badge/AVR_ATmega328P-00979C?style=for-the-badge&logo=arduino&logoColor=white)
![STM32CubeIDE](https://img.shields.io/badge/STM32CubeIDE-03234B?style=for-the-badge&logo=stmicroelectronics&logoColor=white)
![VSCode](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white) 
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

**Hardware Subsystems & Protocols:**
* **Core Silicon:** RCC (Reset and Clock Control), NVIC (Nested Vectored Interrupt Controller), Hardware Timers (TIM/PWM), ADC (Analog-to-Digital Converter), DMA (Direct Memory Access).
* **Operating Systems:** FreeRTOS (Task Scheduling, Semaphores, Stack Profiling, Stack Overflow Hooks / Kernel Panics).
* **Communication & I/O:** I2C, UART, GPIO, EXT-I (External Interrupts), Single-Wire Digital Protocols.

**Instrumentation & Tooling:**
* **Hardware Debugging:** 8-Channel USB Logic Analyzers (for verifying physical clock drift and microsecond timing constraints), SWD (Serial Wire Debug), and Live Expressions telemetry.
* **Software Environment:** STM32CubeIDE, VS Code, Git, and Serial Terminals (PuTTY).
* **Hardware Prototyping:** Soldering, breadboard circuit design, introductory PCB assembly, and sensor integration.

---

### Featured Architecture

#### [FreeRTOS Environmental & Spatial Telemetry Monitor](https://github.com/vez767/DHT22-Telemetry)
*A fault-tolerant, multi-threaded sensor fusion system actively monitoring 3D kinematics, temperature, and proximity.*
* **Custom Bare-Metal HAL:** Engineered a Hardware Abstraction Layer from scratch by manually mapping memory base addresses and defining raw register macros (e.g., `GPIOA_ODR`), explicitly bypassing CMSIS to master low-level silicon architecture.
* **Mutex Bus Arbitration:** Architected a thread-safe I2C routing system using FreeRTOS Mutexes, guaranteeing collision-free bus sharing across an MPU-6050 IMU and three independent HD44780 LCD modules.
* **ISO 14971 Fault Isolation & Recovery:** Designed independent task architectures where physical sensor disconnections trigger localized safe-state error codes without stalling the RTOS scheduler. Engineered a 3-strike anomaly reset matrix to flush stale acoustic data and prevent filter lockouts.

#### [HC-SR04 DSP Tracking Engine & Hardware Safety Monitor](https://github.com/vez767/Hardware-Timers)
*An event-driven RTOS pipeline decoupling the CPU from acoustic flight times while actively profiling kernel memory.*
* **Asynchronous Execution:** Replaced blocking delay loops with an event-driven architecture using FreeRTOS Binary Semaphores and EXTI interrupts, waking the CPU via PendSV context switching only when the hardware catches the returning echo.
* **Kernel Panic Fallback:** Engineered a highly resilient fallback state using `vApplicationStackOverflowHook`. Upon detecting an intentional kernel memory crash via stack watermarking, the system bypasses OS scheduling to trigger a bare-metal visual hardware alarm.
* **Digital Signal Processing (DSP) & Fault Recovery:** Developed a dynamic application gate and slew-rate variance filter to actively reject acoustic anomalies and hardware noise. The system drops invalid data, outputs a strict error code upon physical wire disconnections, and seamlessly resumes autonomous tracking the moment hardware connections are restored.

#### [Non-Blocking NEO-6M GPS DMA & CMSIS Driver](https://github.com/vez767/gps-dma-module)
*An autonomous USART telemetry pipeline utilizing Direct Memory Access (DMA) to prevent CPU starvation.*
* **Industry-Standard CMSIS:** Transitioned from raw memory-mapped macros to STMicroelectronics CMSIS architecture, configuring `USART6` and `DMA2` in Circular Mode to stream NMEA payloads directly into system memory without CPU intervention.
* **RTOS Task Synchronization:** Utilized USART IDLE line interrupts combined with deferred FreeRTOS Task Notifications (`vTaskNotifyGiveFromISR`) to synchronize the RTOS scheduler only when a complete hardware transmission burst finishes.
* **Hardware Limitation Logging:** Actively profiled and documented DMA circular buffer wrap-around corruption caused by asynchronous NMEA data bursts, establishing a clear roadmap for Half-Transfer/Transfer-Complete (HT/TC) interrupt integration.

---

![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white) https://www.linkedin.com/in/wanaemi-alagoa-0711b8327/





![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white) alagoa.wanaemi.emi@gmail.com
