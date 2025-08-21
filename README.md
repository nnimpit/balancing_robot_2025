# Senior Project Teaching Plan: Self-Balancing Robot (2 Semesters)

## Goal
Students will design and implement a self-balancing two-wheeled robot using **STM32F103** microcontroller. The project involves embedded systems, control theory (PID & LQR), real-time operating systems, electronics design, and communication modules.

---

## Semester 1: Fundamentals, Hardware Design, and Prototyping

| Week | Objectives | Topics | Labs/Activities | Deliverables |
|------|------------|--------|-----------------|--------------|
| 1 | Project overview | Introduction to self-balancing robot concept, requirements, timeline | Brainstorming, literature review | Project proposal |
| 2 | MCU fundamentals | STM32F103 architecture & development tools | Set up STM32 development environment (Keil/STM32CubeIDE) | Blink LED demo |
| 3 | Serial interfaces | UART/I2C/SPI basics for sensor interfacing | Connect IMU (MPU6050 via I2C) to STM32 | Sensor data read test |
| 4 | Sensors & filtering | IMU data, accelerometer, gyroscope, Kalman/Complementary filter concept | Acquire raw IMU data, implement simple filtering | IMU data plot |
| 5 | Motor interfacing | DC motor fundamentals, encoder basics, PWM generation | Drive DC motors with STM32 PWM, read encoder counts | Motor position control demo |
| 6 | PCB design basics | Introduction to PCB CAD (Altium/KiCAD), reference design for STM32F103 | Schematic capture practice | Draft schematic |
| 7 | Power electronics | Motor driver circuits (L298N, BTS7960, etc.), power regulation for MCU and motors | Breadboard DC motor driver with STM32 control | Motor control test with load |
| 8 | Embedded OS intro | FreeRTOS task scheduling, multitasking | Implement simple FreeRTOS LED blink & UART task | Basic FreeRTOS demo |
| 9 | Control basics | System modeling of inverted pendulum, introduction to PID | MATLAB/Simulink simulation of robot dynamics | Simulation plots |
| 10 | PCB design II | Design customized robot controller board with STM32F103, IMU, driver, comms | PCB layout exercise | Preliminary PCB layout |
| 11 | Wireless communication | Introduction to RF modules (NRF24L01/HC-12/Bluetooth/LoRa) | Basic PC-to-MCU communication demo | Robot wireless link test |
| 12 | SMD assembly | PCB fabrication and SMD soldering techniques | Assembling prototype board (reflow/hot air) | Partially assembled controller board |
| 13 | Debugging hardware | Debugging interfaces (SWD/JTAG), logic analyzer/oscilloscope use | Test signals, check power rails, verify MCU boot | Working board test log |
| 14 | Integration | Connect motors, sensors, and controller | Mount hardware on robot chassis | Hardware mock-up |
| 15 | Mid-project review | Present hardware progress | Peer review and testing | Hardware integration report |
| 16 | Semester wrap-up | Prepare documentation and reflect | Presentation | Semester 1 report |

---

## Semester 2: Control, Optimization, and Advanced Features

| Week | Objectives | Topics | Labs/Activities | Deliverables |
|------|------------|--------|-----------------|--------------|
| 1 | Recap & targets | Overview of completed hardware | System initialization testing | Working hardware check |
| 2 | Embedded drivers | Refine STM32 drivers for IMU, encoder, motor driver | Integrated sensor fusion (complementary filter/Kalman filter) | Sensor fusion output |
| 3 | Real-time scheduling | Task separation in FreeRTOS for sensing, control, communication | Multi-task demo with IMU + motor control | FreeRTOS task mapping |
| 4 | PID control implementation | Motor speed & angle control with PID | Tune PID on prototype | PID test data |
| 5 | Stability testing | Robot standing test with PID | Robot balancing with support | Robot balancing demo (PID) |
| 6 | LQR control theory | State-space modeling, linear quadratic regulator design | MATLAB pole-placement & LQR simulation | Simulation plots |
| 7 | LQR implementation | Implement LQR in STM32 | Translate MATLAB gains to embedded C | LQR code |
| 8 | LQR tuning | Compare PID vs LQR performance | Experimental testing | Stability performance graphs |
| 9 | Wireless control | Integrate radio transmission for remote control | Control robot with PC or joystick | Remote control demo |
| 10 | GPS integration | GPS fundamentals, parsing NMEA | GPS test logging | GPS data acquisition demo |
| 11 | Pathway planning | Path-following algorithms for mobile robot | Basic waypoint navigation test | GPS navigation demo |
| 12 | Safety & robustness | Fail-safe, emergency stop mechanisms | Power fault & error handling test | Safety checklist |
| 13 | System optimization | Code optimization, memory management | Profiling MCU resources | Code optimization report |
| 14 | Final integration | Combine all modules: balance, wireless, navigation | Final full system testing | System demo video |
| 15 | Final project review | Formal presentation preparation | Mock defense session | Draft report |
| 16 | Defense & submission | Final presentation & project submission | Project demonstration | Final report & robot demo |

---

## End Results
- Fully functional self-balancing robot controlled by STM32F103  
- Custom PCB with IMU, motor driver, wireless comms, and power supply  
- Implementation of **LQR control** for robust stabilizing  
- Optional features: wireless control, GPS waypoint navigation  
- Oral defense, report, and live demo
