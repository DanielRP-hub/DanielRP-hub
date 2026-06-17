# Daniel Ruiz Perez | Embedded Software Engineering Portfolio

## About Me
Final-year Mechatronics Engineering student specializing in embedded systems, microcontroller architecture, and real-time software development. This repository serves as a comprehensive portfolio of my bare-metal programming, hardware abstraction, and hardware-in-the-loop (HIL) validation projects across multiple architectures. 

My primary focus lies in developing robust firmware for automotive and industrial applications, emphasizing hardware interrupts, custom peripheral drivers, deterministic control loops, and complex sensor fusion algorithms.

## Technical Proficiencies
* **Programming Languages:** C (Register-level & Bare-Metal), Python / MicroPython, MATLAB.
* **Microcontroller Architectures:** * ARM Cortex-M4 (STM32F407VGT6)
  * ARM Cortex-M0+ (RP2040 / Raspberry Pi Pico)
  * AVR (ATmega2560)
  * PIC & ESP32
* **Hardware Protocols & Interfaces:** I2C, SPI, UART/USART, Fast/Phase-Correct PWM, ADC, GPIO bitwise manipulation.
* **Systems Engineering:** Interrupt Service Routines (EXTI/NVIC), State-Machine UI Design, Asynchronous Scheduling, Ring Buffers, Hardware Multiplexing.
* **Control & Signal Processing:** PID Control, Discrete Lead-Lag Compensators, ZUPT (Zero Velocity Update), Digital Low-Pass Filters, Numerical Integration (Simpson's 3/8).
* **Validation & Tools:** Hardware-in-the-Loop (HIL) methodologies, CustomTkinter/Python SCADA Dashboards, Asynchronous Telemetry.

---

## Repository Index & Featured Projects

### 1. ARM Cortex-M4 (STM32F407VGT6)
A collection showcasing deep bare-metal C programming, bypassing vendor HALs to implement direct register manipulation, deterministic execution, and complex real-time asynchronous architectures.

* **Digital_Control_HIL_Dashboard:** A full-stack solution combining a hard-real-time 20ms execution loop (TIM6) with an asynchronous Python SCADA GUI. Implements Hardware Quadrature Decoding (TIM3) and Discrete Digital Compensators via difference equations for closed-loop motor control.
* **Dual_UART_Telematics_Bridge:** An asynchronous serial bridge between a PC terminal and an external SIM808 GSM/GPS module. Implements non-blocking `USARTx_IRQHandler` vectors and Ring Buffers to capture incoming byte streams without CPU stalling.
* **Hardware_PWM_Generation:** Direct configuration of Advanced-Control Timers (TIM4) and Alternate Function (AF) multiplexing to generate deterministic, high-frequency PWM signals entirely via hardware.
* **Asynchronous_EXTI_HMI:** Robust decoupling pattern between high-priority hardware interrupts (EXTI) and main-thread UI logic using volatile flag signaling and multi-source ISR dispatching.
* **BareMetal_Register_Mapping:** Foundational hardware control through custom `typedef struct` memory mapping for O(1) register access, demonstrating safe software debouncing and bus clock management.

### 2. AVR Architecture (ATmega2560)
Projects demonstrating deep register-level manipulation and real-time scheduling on 8-bit architectures without relying on third-party libraries.

* **Multi_Sensor_Central_Node:** A complex systems integrator bridging I2C, SPI, and USART protocols to process environmental telemetry and actuate physical outputs via a non-blocking command parser.
* **PWM_Motor_Control_HMI:** Closed-loop DC motor control utilizing 25kHz hardware PWM (Timer4). Includes an asynchronous hardware emergency stop (INT5) and an LCD/Keypad interface.
* **Servo_Position_Control_PWM:** Precise angular actuation using 50Hz Phase and Frequency Correct PWM, demonstrating mathematical scaling of timer pre-load registers for servo control.
* **Interrupt_Driven_Clock_LCD:** Event-driven real-time clock transitioning from standard polling to an asynchronous ISR-based architecture, ensuring zero input lag.
* **Multi_Timer_Scheduling:** Advanced timebase generation utilizing four independent 16-bit hardware timers to orchestrate asynchronous tasks concurrently.

### 3. ARM Cortex-M0+ (RP2040 / Raspberry Pi Pico)
Focuses on rapid mathematical prototyping and sensor fusion algorithms using MicroPython before low-level C implementation.

* **Rapid_Prototyping_AHRS:** An advanced Attitude and Heading Reference System (AHRS) validating complex mathematics on the MPU6050. Features include Welford's algorithm for dynamic noise deadbands, ZUPT for gyro bias correction, and Simpson's 3/8 rule for high-fidelity yaw integration.
* **Digital_Inclinometer_Accelerometry:** A 2-axis tilt sensor isolating the static 1g gravity vector to calculate Pitch and Roll, featuring a non-blocking UART command-line interface for dynamic hardware calibration.

---

## Contact & Links
* **Location:** Pachuca, Hidalgo, Mexico (Open to relocate)
* **LinkedIn:** [Insert your LinkedIn URL here]
* **Email:** ruiz.pdaniel222.1821@gmail.com
