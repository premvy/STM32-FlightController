# STM32 Rocket Flight Controller

## PCB design 


<img width="615" height="649" alt="image" src="https://github.com/user-attachments/assets/651189a1-e600-4357-a4d0-fea4e383fb3f" />


<img width="630" height="700" alt="image" src="https://github.com/user-attachments/assets/81112d13-a7ee-4a6e-ae6f-d70e0aae1eaf" />


## Schematic

<img width="2277" height="1568" alt="image" src="https://github.com/user-attachments/assets/9841681a-46cd-432e-b6f0-e6bb7e4525e1" />

**Hardware Specs:**
* **MCU:** STM32F722RETx clocked by a 25MHz external crystal.
* **Sensors:** ICM-42688 (6-axis IMU) and BMP580 (Barometer).
* **Power:** USB-C connectivity, BQ-series battery charging, a clean 3.3V logic rail, and a 5V buck-boost rail for servos and ESCs.
* **Data Logging:** Dedicated 4-bit microSD slot for high-speed flight recording.
* **I/O:** 3-pin PWM motor headers and hardware `BOOT` / `RESET` buttons.

