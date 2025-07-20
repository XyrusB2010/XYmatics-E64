---
title: "XYmatics-E64"
author: "Xyrus Babao"
description: "5-axis Klipper-powered mainboard"
created_at: "2025-07-07"
---

### <b>Total time spent: 7 hours</b>

# 7/07/2025 - Begin PCB design
For the PCB design, I am using KiCad with a few components imported from <a href="https://snapeda.com/">SnapEDA.</a> I have named <a href='https://github.com/XyrusB2010/XYmatics-Alpha/tree/main'>XYmatics-Alpha's</a> mainboard E64 (Engine64). It utilises a CM4/CM5 compute module running Klipper firmware to control the main MCU - an STM32F407. Like most Klipper systems, the compute module does not directly control the motors, sensors, etc, and instead outputs commands via USB to the STM32. I have completed desigining the Compute module side, and just need to complete the STM32 and other components. Below is an image of the CM4 schematic.

<img src="https://github.com/user-attachments/assets/16006f6d-e0e2-467e-8219-a059112f625b" alt="XYmatics-E64 CM4 schematic" width="500">

(Excuse the resolution, you can view a PDF of the schematic <a href="https://github.com/XyrusB2010/XYmatics-E64/blob/main/Schematics/xymatics-e64.pdf">here.</a>)

<b>Total time - 45 minutes</b>

# 14/07/2025 - Finish STM32 schematic and begin X42 schematic
Today I have completed the schematic for the STM32F407. It has what most other 3D Printer mainboards have, but also includes 8 CAN FD bus ports for connecting expansion boards (XYmatics-X42). It uses the high-speed TJA1051T for CAN FD communication. 5 TMC2209 Stepsticks are used to drive the main stepper motors. 5 controllable fans are included, as well as another MOSFET for the heatbed. 3 endstops/switches are included to home the printer. The entire system runs on 24V, which is the standard for most 3D printer mainboards.

<img src="https://github.com/user-attachments/assets/a8ee5966-3f1e-482e-ba25-d5396afab688" alt="XYmatics-E64 STM32F407 schematic" width="500">

<a href="https://github.com/XyrusB2010/XYmatics-E64/blob/main/Schematics/xymatics-e64.pdf">Link to schematic PDF</a>

<b>Total time - 2 hours 15 minutes</b>

# 20/07/2025 - Finish X42 schematic
I have now finished the schematic for the X42. It is quite similar to the BIGTREETECH EBB42 and Mellow Fly SHT-42, but also contains a MOSFET to drive a laser engraver or router motor. Unfortunately, I haven't broken out a USB port yet (although I may fix this in the future). This means the only other way to flash Klipper is through an ST-LINK, or other JTAG/SWD programmer. You can obtain these through Aliexpress for <$2 USD. The X42 also doesn't use a Stepstick driver like the E64 mainboard, but has a directly soldered TMC2209 instead. After looking through the schematics one more time, I should be ready to start designing the PCBs.

<img src="https://github.com/user-attachments/assets/298dfdd6-ca6b-4de3-b091-deef21a09c47" alt="XYmatics-E64 X42 schematic" width="500">

<b>Total time - 2 hours</b>
