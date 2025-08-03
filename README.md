# XYmatics E64
XYmatics E64 (Engine, 64-bit) is a 5-axis Klipper mainboard, powered by a Raspberry Pi CM4 and STM32F407. It was originally built for <a href='https://github.com/XyrusB2010/XYmatics-Alpha/tree/main'>XYmatics Alpha</a>, but you can also use it for most 3D Printers.

## E64 Features
- Powered by STM32F407VET6 (MCU) and Raspberry Pi CM4 (Host)
- 1 USB-micro OTG port + 2 USB-A ports + 1 USB JST breakout, 100 Mbit RJ45 Socket for LAN, Micro SD card for extra storage
- 5 TMC2209 Stepsticks to drive stepper motors
- 3 Endstops/Switches
- 5 Controllable fans on base board + 1 for Raspberry Pi
- 8 CAN FD bus ports to reduce amount of cables
- CSI for camera input
- HDMI or DSI for display output
- I2C bus broken out

## E64 PCB
<img src="https://github.com/user-attachments/assets/3666f2f9-8a2c-4181-a9a2-72328bd6c555" alt="E64 PCB">

# XYmatics X42
XYmatics X42 (Xpansion, for 42mm motors) is a Klipper expansion board, designed to mount onto 42mm stepper motors. Powered by a STM32G0B1, it communicates to the E64 mainboard through CAN FD. This board simplifies the mainboard, and reduces the amount of cables going out. The X42 can also be used with most other 3D Printers.

## X42 Features
- Powered by STM32G0B1CBT6
- Supports Laser engravers, CNC routers and FDM extruders
- TJA1051T CAN FD module to communicate with E64
- ~~BLTouch compatible~~
- Two PWM controllable fans
- ADXL345 accelerometer included
- ~~3~~ 1 Endstop/Switch
- I2C bus ~~and neopixel~~ broken out
>  [!NOTE]
>  May re-add these removed features in future if possible.

## X42 PCB
<img src="https://github.com/user-attachments/assets/d4ca1c45-a94d-4c25-9ed2-39776c4dd5d3" alt="X42 PCB front view" width="400" height="400">
<img src="https://github.com/user-attachments/assets/9a6bdf57-31d1-4693-97cc-d2188163e315" alt="X42 PCB back view" width="400" height="400">
