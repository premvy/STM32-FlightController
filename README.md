# Custom STM32  Flight Controller

## Description 
This project is a custom designed, two layer flight controller built to serve as the central brain for a drone prototype. The board is driven by an STM32F722RET6 microcontroller, providing the high-speed processing headroom required for low latency PID loops. The hardware stack features an ICM-42688 6-axis IMU, a BMP580 barometer for precision altitude hold, and a dedicated microSD slot for high rate Blackbox data logging. Power delivery is managed through a modern USB-C interface, paired with a BQ series battery management IC and a clean 5V buck-boost circuit to safely drive servos and ESCs. Beyond just getting a vehicle in the air, this board was designed to push a concept from a raw schematic into a fully manufactured physical product.

## PCB design 

<img width="615" height="649" alt="image" src="https://github.com/user-attachments/assets/651189a1-e600-4357-a4d0-fea4e383fb3f" />

<img width="630" height="700" alt="image" src="https://github.com/user-attachments/assets/81112d13-a7ee-4a6e-ae6f-d70e0aae1eaf" />

_Custom PCB routed in Kicad_

## Schematic

<img width="2277" height="1568" alt="image" src="https://github.com/user-attachments/assets/9841681a-46cd-432e-b6f0-e6bb7e4525e1" />

**Hardware Specs:**
* **MCU:** STM32F722RETx clocked by a 25MHz external crystal.
* **Sensors:** ICM-42688 (6-axis IMU) and BMP580 (Barometer).
* **Power:** USB-C connectivity, BQ-series battery charging, a clean 3.3V logic rail, and a 5V buck-boost rail for servos and ESCs.
* **Data Logging:** Dedicated 4-bit microSD slot for high-speed flight recording.
* **I/O:** 3-pin PWM motor headers and hardware `BOOT` / `RESET` buttons.

Designator,Footprint,Quantity,Value,LCSC Part #
"C1, C29, C30, C31",0402,4,1uF,C52923
"C10, C16, C19, C20, C21, C22, C24, C25, C26, C27, C37",0201,11,100nF,C76934
"C11, C2, C6, C9",0603,4,10uF,C19702
"C12, C13, C14",0805,3,22uF,C45783
C15,0603,1,2.2uF,C23630
"C17, C18",0402,2,22uF,C415703
C23,0201,1,2.2uF,C318539
C28,0402,1,100nF,C1525
C3,0402,1,44uF,C19702
"C32, C4",0201,2,10uF,
"C33, C34",0201,2,20pF,C325444
"C35, C36",0201,2,6.8pF,C85916
C5,0402,1,47nF,C82219
"C7, C8",0805,2,10uF,C440198
CARD1,TF-SMD_TF-01A,1,TF-01A,C91145
D1,0402,1,LED,C965793
J1,TerminalBlock_Xinya_XY308-2.54-2P_1x02_P2.54mm_Horizontal,1,Screw_Terminal_01x02,
"J2, J3",PinHeader_1x03_P2.54mm_Vertical,2,Conn_01x03,
L1,L2520,1,1uH,C435392
L2,IND-SMD_L4.0-W4.0-A,1,1.5uH,C3033018
L3,IND-SMD_L3.0-W3.0,1,5.6uH,C18236327
L4,L0603,1,FCM1608KF-601T03,C141723
"R1, R2",0201,2,5.1k,C270344
R10,0201,1,383,
"R11, R12, R13, R16, R17, R18, R19, R20, R21, R22, R3, R4, R5, R6, R7",0201,15,10K,C7467266
R14,0402,1,100K,C25741
R15,0201,1,22.1K,C384418
R8,0201,1,5.23K,C332546
R9,0201,1,30.1K,
"SW1, SW2",SW-SMD_L3.9-W3.0-P4.45,2,TS-1088-AR02016,C720477
U1,LGA-10_L2.0-W2.0-P0.50-TL_BMP580,1,BMP580,C22391138
U2,LQFP-64_10x10mm_P0.5mm,1,STM32F722RETx,C118207
U3,LGA-14_L3.0-W2.5-P0.50-TL,1,ICM-45686,C22459454
U4,VQFN-15_L3.0-W2.5-P0.50-BL,1,TPS63070RNMR,C109322
U5,VFQFPN-24_L4.0-W4.0-P0.50-BL-EP2.8,1,BQ25883RGER,C544362
U6,SOT-23-6,1,LMR51430,C5219261
USB1,USB-C-SMD_TYPE-C-16PIN-2MD-073,1,TYPE-C 16PIN 2MD,C2765186
X1,CRYSTAL-SMD_4P-L3.2-W2.5-BL,1,X322525MOB4SI,C9006
X2,FC-135R_L3.2-W1.5,1,Q13FC1350000400,C32346

[View the Bill of Materials (BOM)](./production/bom.csv)
