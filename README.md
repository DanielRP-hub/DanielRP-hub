# Daniel Ruiz Perez | Embedded Software Engineering Portfolio

## About Me
Final-year Mechatronics Engineering student specializing in embedded systems, microcontroller architecture, and real-time software development. This repository serves as a comprehensive portfolio of my bare-metal programming, hardware abstraction, and hardware-in-the-loop validation projects across multiple architectures. 

My primary focus lies in developing robust firmware for automotive and industrial applications, emphasizing hardware interrupts, custom peripheral drivers, and complex sensor fusion algorithms.

## Technical Proficiencies
* **Programming Languages:** C (Register-level & Bare-Metal), C++, Python / MicroPython, MATLAB.
* **Microcontroller Architectures:** * AVR (ATmega2560)
  * ARM Cortex-M4 (STM32F407VGT6)
  * ARM Cortex-M0+ (RP2040 / Raspberry Pi Pico)
  * PIC & ESP32
* **Hardware Protocols:** I2C, SPI, UART, Fast/Phase-Correct PWM, ADC, GPIO bitwise manipulation.
* **Systems Engineering:** Interrupt Service Routines (ISR), State-Machine UI Design, Asynchronous Scheduling, Hardware Multiplexing.
* **Control & Signal Processing:** PID Control, ZUPT (Zero Velocity Update) algorithms, Digital Low-Pass Filters, Numerical Integration (Simpson's 3/8).

---

## Repository Index & Featured Projects

### 1. AVR Architecture (ATmega2560)
A collection of projects demonstrating deep register-level manipulation and real-time scheduling without relying on third-party HAL libraries.

* **Multi_Sensor_Central_Node:** A complex systems integrator bridging I2C, SPI, and USART protocols to process environmental telemetry (MPU6050, MAX6675, HC-SR04) and actuate physical outputs (DC Motor, Servo, DAC) via a non-blocking USART command parser.
* **PWM_Motor_Control_HMI:** Closed-loop DC motor control utilizing 25kHz hardware PWM (Timer4). Includes an asynchronous hardware emergency stop (INT5) and an LCD/Keypad interface.
* **Servo_Position_Control_PWM:** Precise angular actuation using 50Hz Phase and Frequency Correct PWM, demonstrating mathematical scaling of timer pre-load registers for servo control.
* **Interrupt_Driven_Clock_LCD:** Event-driven real-time clock transitioning from standard polling to an asynchronous ISR-based architecture, ensuring zero input lag.
* **Multi_Timer_Scheduling:** Advanced timebase generation utilizing four independent 16-bit hardware timers to orchestrate asynchronous tasks concurrently.

### 2. ARM Cortex-M0+ (RP2040 / Raspberry Pi Pico)
Focuses on rapid mathematical prototyping and sensor fusion algorithms using Python before low-level C implementation.

* **Rapid_Prototyping_AHRS:** An advanced Attitude and Heading Reference System (AHRS) validating complex mathematics on the MPU6050. Features include Welford's algorithm for dynamic noise deadbands, ZUPT for gyro bias correction, and Simpson's 3/8 rule for high-fidelity yaw integration.
* **Digital_Inclinometer_Accelerometry:** A 2-axis tilt sensor isolating the static 1g gravity vector to calculate Pitch and Roll, featuring a non-blocking UART command-line interface for dynamic hardware calibration.

### 3. ARM Cortex-M4 (STM32F407VGT6)
**(Repository currently being updated with CMSIS and bare-metal ARM configurations).*

### 4. PIC Architecture
* **PIC_BareMetal_Drivers:** Foundational repository showcasing bare-metal C configurations for basic GPIO, ADC, and Timer manipulations on PIC microcontrollers.

---

## Contact & Links
* **Location:** Pachuca, Hidalgo, Mexico (Open to relocate)
* **LinkedIn:** [Insert your LinkedIn URL here]
* **Email:** [Insert your professional email here]
