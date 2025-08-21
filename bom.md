# Bill of Materials (BOM) — Self-Balancing Robot (STM32F103 + LQR)

Note: Quantities assume 1 robot build plus 10–20% spares for small passives and SMD assembly.

## 1) Controller and Compute - Bluepill

| Item | Part Number/Spec | Qty | Notes |
|---|---|---:|---|
| MCU (LQFP-48) | STM32F103C8T6 | 1 | 72MHz, 64KB/128KB Flash, Cortex-M3 |
| External crystal (MCU) | 8MHz, HC-49S or SMD 3225 | 1 | Load caps 18–22pF |
| RTC crystal (optional) | 32.768kHz, SMD | 1 | For low-power timing if needed |
| LDO regulator | AMS1117-5.0 (or AP7365-5.0) | 1 | 12V→5V, consider thermal |
| Buck converter (recommended) | MP1584/LM2596 module or TPS5430 | 1 | Higher efficiency 12V→5V |
| 3.3V regulator | AMS1117-3.3 or AP2112-3.3 | 1 | 5V→3.3V for MCU, IMU, radio, GPS |
| SWD header | 2x5 1.27mm or 2x5 2.54mm | 1 | For programming/debug |
| USB-UART (optional) | CP2102/CH340N + USB-C | 1 | Onboard or external dongle |
| Reset tactile switch | 6x6 SMD/THT | 1 | MCU reset |
| Boot mode jumpers | 2-pin headers + shunts | 2 | BOOT0/BOOT1 |

## 2) Sensors and Feedback

| Item | Part Number/Spec | Qty | Notes |
|---|---|---:|---|
| IMU 6-axis | MPU-6050 (I2C) | 1 | Angle estimation with complementary/Kalman |
| Magnetometer (optional) | HMC5883L/QMC5883 | 1 | Heading (optional) |
| Wheel encoders | Integrated in motor (e.g., 11–13 PPR x4) | 2 | Quadrature A/B |
| GPS module | u-blox NEO-6M or NEO-M8N | 1 | UART @ 3.3V, with active antenna |
| Radio/remote (option A) | nRF24L01+ with PA/LNA | 2 | Robot+Tx controller |
| Radio/remote (option B) | HC-05/06 Bluetooth | 1 | Simpler RC/telemetry |

## 3) Power and Motor Drive

| Item | Part Number/Spec | Qty | Notes |
|---|---|---:|---|
| Battery | 3S LiPo 11.1V, 1500–2200mAh, 30C | 1 | Primary power |
| Battery connector | XT60 male/female pair | 1 | With 12–14AWG leads |
| Power switch | 10–15A toggle/rocker | 1 | Main power |
| Fuse/Polyfuse | 10–15A blade or PTC 5–7A | 1 | Safety |
| Motor driver (recommended) | TB6612FNG dual H-bridge | 1–2 | 1 board drives 2 small DC motors |
| Alternative driver (higher current) | VNH5019 single H-bridge | 2 | For 10–12A peak motors |
| DC gear motors with encoder | 12V, 25mm/37mm, 200–400RPM | 2 | 2-wheel self-balancing |
| DC barrel jack (optional) | 2.1mm | 1 | Bench power |

## 4) PCB and Passive Components

