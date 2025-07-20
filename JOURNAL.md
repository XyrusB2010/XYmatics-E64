---
title: "XYmatics-E64"
author: "Xyrus Babao"
description: "5-axis Klipper powered mainboard"
created_at: "2025-07-07"
---

# 7/07/2025 - Begin PCB design
For the PCB design, I am using KiCad with a few components imported from <a href="https://snapeda.com/">SnapEDA.</a> I have named XYmatics-Alpha's mainboard E64 (Engine64). It utilises a CM4/CM5 compute module running Klipper firmware to control the main MCU - an STM32F407. Like most Klipper systems, the compute module does not directly control the motors, sensors, etc, and instead outputs commands via USB to the STM32. I have completed desigining the Compute module side, and just need to complete the STM32 and other components. Below is an image of the CM4 schematic.

<img src="https://github.com/user-attachments/assets/16006f6d-e0e2-467e-8219-a059112f625b" alt="XYmatics-E64 CM4 schematic" width="500">

(Excuse the resolution, you can view a PDF of the schematic <a href="https://github.com/XyrusB2010/XYmatics-Alpha/blob/main/PCB/xymatics-e64.pdf">here.</a>)

Total time - 45 minutes
