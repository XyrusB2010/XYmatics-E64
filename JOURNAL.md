---
title: "XYmatics-E64"
author: "Xyrus Babao"
description: "5-axis Klipper-powered mainboard"
created_at: "2025-07-07"
---

### <b>Total time spent: 13 hours 45 minutes</b>

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

# 23/07/2025 - Update on X42
The X42 PCB is about 75% completed, I just need to route the components for the CNC router/laser. Due to the limited amount of space on the PCB, some of the components are mounted on the back side (currently just the power supply and regulators). So far the CAN BUS, SWD, Stepper motor, Thermistor, Hotend, Fans, I2C Bus and Buttons have been placed and routed. Unfortunately, I have temporarily removed the Neopixel and BLTouch breakouts due to the lack of space, although I may re-add them later on. Below is an unfinished 3D render of the X42 PCB:

<img src="https://github.com/user-attachments/assets/ea462724-94b6-45a5-af4d-d67a52dd444e" alt="X42 PCB front view" width="300" height="300">
<img src="https://github.com/user-attachments/assets/3e4338a1-be07-48da-b687-2c748f0120a5" alt="X42 PCB back view" width="300" height="300">

<b>Total time - 1 hour 45 minutes</b>

# 25/07/2025 - Finish X42 PCB
I have now finished designing the PCB for the X42. All GPIOs/breakouts are on the front side, while the power supply and ADXL345 are mounted on the back. Endstops have also been removed due to the small amount of remaining space. This will be added in the first revision. I will begin to route the Raspberry Pi components on the E64, starting with the power supply. Below is a completed 3D render of the X42 PCB:

<img src="https://github.com/user-attachments/assets/8b807d25-d33c-4b2a-ac7d-c70b8015cccc" alt="X42 PCB front view" width="300" height="300">
<img src="https://github.com/user-attachments/assets/a9e47e3d-d03b-45a2-a376-7b630557bc3e" alt="X42 PCB back view" width="300" height="300">

<b>Total time - 2 hours</b>

# 31/07/2025 - E64 PCB complete
6 days later, the E64 PCB has been finished. Please note that the RPI-GPIO isn't fully broken out, only +5V, +3.3V and I2C Bus have been. Notice how the RPI electronics are on one side while the F407 is on the other, this is to reduce complications with the design. 3 M3 mounting holes have been placed in the corners. The rough dimensions of the board are 192x98mm. The next step is to write the firmware for Klipper, which shouldn't be too hard. Here is a 3D render of the E64 PCB:

<img src="https://github.com/user-attachments/assets/c1ebf41c-d44c-4018-8ba8-155ea10e4590" alt="E64 PCB front view" width="500">

<b>Total time - 3 hours</b>
