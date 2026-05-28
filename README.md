# STM32 Rocket Flight Controller

Bill of Materials (BOM)

- USB-C: Connector Port
- MicroSD: Memory Storage
- TPS63070: Buck-Boost Regulator
- LMR51430: Step-Down Regulator
- BQ25883: Battery Charger
- STM32F722RETx: Main Microcontroller
- ICM-45686: IMU Sensor (tracks motion/orientation)
- BMP580: Barometric Altimeter (tracks altitude/pressure)

## Schematic

<img width="2277" height="1568" alt="image" src="https://github.com/user-attachments/assets/9841681a-46cd-432e-b6f0-e6bb7e4525e1" />

**Hardware Specs:**
* **MCU:** STM32F722RETx clocked by a 25MHz external crystal.
* **Sensors:** ICM-42688 (6-axis IMU) and BMP580 (Barometer).
* **Power:** USB-C connectivity, BQ-series battery charging, a clean 3.3V logic rail, and a 5V buck-boost rail for servos and ESCs.
* **Data Logging:** Dedicated 4-bit microSD slot for high-speed flight recording.
* **I/O:** 3-pin PWM motor headers and hardware `BOOT` / `RESET` buttons.
