---
title: "XYmatics-E64"
author: "Xyrus Babao"
description: "5-axis Klipper powered mainboard"
created_at: "2025-07-07"
---

# 7/07/2025 - Begin PCB design
For the PCB design, I am using KiCad with a few components imported from <a href="https://snapeda.com/">SnapEDA.</a> I have named <a href='https://github.com/XyrusB2010/XYmatics-Alpha/tree/main'>XYmatics-Alpha's</a> mainboard E64 (Engine64). It utilises a CM4/CM5 compute module running Klipper firmware to control the main MCU - an STM32F407. Like most Klipper systems, the compute module does not directly control the motors, sensors, etc, and instead outputs commands via USB to the STM32. I have completed desigining the Compute module side, and just need to complete the STM32 and other components. Below is an image of the CM4 schematic.

<img src="https://github.com/user-attachments/assets/16006f6d-e0e2-467e-8219-a059112f625b" alt="XYmatics-E64 CM4 schematic" width="500">

(Excuse the resolution, you can view a PDF of the schematic <a href="https://github.com/XyrusB2010/XYmatics-E64/blob/main/Schematics/xymatics-e64.pdf">here.</a>)

Total time - 45 minutes

# 14/07/2025 - Finish STM32 schematic and begin X42 schematic
Today I have completed the schematic for the STM32F407. It has what most other 3D Printer mainboards have, but also includes 8 CAN FD bus ports for connecting expansion boards (XYmatics-X42). It uses the high-speed TJA1051T for CAN FD communication. 5 TMC2209 Stepsticks are used to drive the main stepper motors. 5 controllable fans are included, as well as another MOSFET for the heatbed. 3 Endstops/Switches are included to home the printer. The entire system runs on 24V, which is the standard for most 3D printer mainboards.

<img src="https://github.com/user-attachments/assets/a8ee5966-3f1e-482e-ba25-d5396afab688" alt="XYmatics-E64 STM32F407 schematic" width="500">

<a href="https://github.com/XyrusB2010/XYmatics-E64/blob/main/Schematics/xymatics-e64.pdf">Link to schematic PDF</a>
