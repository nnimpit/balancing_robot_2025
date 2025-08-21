# Self-Balancing Robot Senior Project Teaching Plan
# 📌 Senior Project 1
# 📌 บรรยายรายวิชา
รายวิชานี้มุ่งเน้นการพัฒนาทักษะทางวิศวกรรมไฟฟ้าและระบบควบคุม ผ่านการออกแบบและพัฒนาหุุ่นยนค์ทรงตัว (Self Balancing Robot) นักศึกษาจะได้เรียนรู้ตั้งแต่ การออกแบบ PCB, การประกอบอุปกรณ์, การเขียนโปรแกรมควบคุมด้วย STM32F103C8 และ Arduino IDE, การสื่อสารระหว่างอุปกรณ์, ไปจนถึงการทดสอบหุุ่นยนค์ทรงตัว

โดยเนื้อหาของรายวิชาจะช่วยให้นักศึกษาสามารถ อธิบายความรู้เกี่ยวข้องกับการจัดการพลังงานของอุปกรณ์ (CLO1) เลือกใช้เทคโนโลยีที่เหมาะสม (CLO2), แก้ไขปัญหาที่เกิดขึ้นระหว่างพัฒนา (CLO3) และสร้างโครงการต้นแบบที่สามารถทำงานได้จริง

# 📌 เกณฑ์การให้คะแนน
- การเข้าเรียน (20%)
- การออกแบบ PCB (30%)
- ผลการประกอบและทดสอบการทรงตัว (30%)
- การนำเสนอ (20%)
- 
### Duration: 2 Semesters (30 weeks, ~1 year)
### Target: From Scratch → Fully Functional Self-Balancing Robot with LQR control

---

## Semester 1: Fundamentals, Hardware, and Basic Control

| Week | Objectives | Topics | Labs | Deliverables |
|------|------------|--------|------|--------------|
| 1-2 | Understand MCU basics and development environment | - Intro to STM32F103 architecture <br> - IDE setup (STM32CubeIDE) <br> - GPIO and basic peripherals | LED blink, button input | Lab report on STM32 basics |
| 3-4 | Learn digital communication for sensors | - I²C, SPI, USART overview <br> - Sensor interfacing (IMU: MPU6050/MPU9250) | Connect IMU sensor via I²C, display raw data via serial | Demonstration of IMU output in serial console |
| 5-6 | Design hardware/PCB suitable for robot controller | - Schematic capture (KiCad/Altium) <br> - PCB layout for STM32 + IMU + motor drivers | Group PCB design project | Gerber files + PCB schematic |
| 7-8 | Explore SMD soldering and PCB assembly | - SMD parts, reflow basics <br> - PCB soldering lab | Assemble controller board using custom PCB | Functional PCB with STM32 + IMU tested |
| 9-10 | Introduction to motor control | - DC motors with encoders <br> - Quadrature encoder basics <br> - Motor driver ICs (L298N/TB6612FNG) | Motor + encoder test with STM32 PWM + capture | Report: encoder readings with motor control |
| 11-12 | Data acquisition from IMU | - Kalman filter vs Complementary filter <br> - Fusion of accelerometer + gyroscope | Implement complementary filter for angle estimation | Plot real-time robot tilt angle |
| 13-14 | Basic closed-loop control concepts | - Review: PID control <br> - Step response analysis | Control 1D inverted pendulum simulation in MATLAB/Python | PID simulation results |
| 15 | - Semester wrap <br> - สอบโปรเจค 1  | - System integration checkpoint | Demonstrate sensor + motor loop closed testing | Milestone: PCB functioning + IMU angle + motor encoder demo |

---

## Semester 2: Advanced Control, FreeRTOS, Wireless, and LQR

| Week | Objectives | Topics | Labs | Deliverables |
|------|------------|--------|------|--------------|
| 1-2 | Real-time OS for robot | - FreeRTOS tasks, scheduling, drivers | Implement FreeRTOS tasks for IMU + motor | Lab report: Multitasking robot system |
| 3-4 | Onboard debugging | - UART debugging <br> - Real-time logging tools | Display PID variables via serial/RTT logging | Debug console working |
| 5-6 | PID implementation and tuning | - Hands-on PID tuning <br> - Response curves | Tune robot balance with PID control | Robot balancing demo (PID) |
| 7-8 | Advanced control system | - LQR overview <br> - State-space modeling <br> - MATLAB LQR design workflow | Simulate robot dynamics and LQR control in MATLAB | Report with state-space model + LQR gains |
| 9-10 | Implement LQR on hardware | - STM32 implementation <br> - Comparison vs PID | Run LQR control loop on robot | Robot balance with LQR (demo video) |
| 11-12 | Wireless communication | - Radio transmission modules (NRF24L01, Bluetooth) <br> - Remote control inputs | Implement wireless manual control | Wireless RC demo |
| 13-14 | GPS and path following | - GPS basics (NEO-6M) <br> - Waypoint navigation | Integrate GPS to STM32 + log coordinates | Robot moves toward simple waypoint |
| 15 | Final project integration | - Error checking, stability improvements <br> - Final presentation prep | Full system demo | Final demo: Self-balancing robot with LQR + wireless + GPS navigation |

---

## Final Deliverables
- **Semester 1**:  
  - Functioning STM32-based PCB  
  - Sensor data acquisition (IMU + Encoder)  
  - Angle estimation system  
- **Semester 2**:  
  - Robot balances on its own (PID → LQR)  
  - Wireless manual control capability  
  - GPS-guided navigation prototype  
  - Final technical report + Demonstration  

---
