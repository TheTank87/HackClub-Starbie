# Starbie PCB
This Starbie board will be my first project and I will program it to do some cool things.

<img width="1155" height="725" alt="Screenshot 2026-10-08 at 9 03 29 PM" src="https://github.com/user-attachments/assets/34ea3f6c-f528-41fe-aa01-0265f2d72615" />

Finished project design. More notes in the JOURNAL.

This is the Starbie, a two-button macropad that has an OLED display to show whatever you want and it even comes with  MPU6050 and DHT11 Environment Sensor. There are two main components to
this project which is the hardware and firmware. This project is built to be your desktop companion and it will react to how you handle it. (If you code it that way.)
It is USB powered and requires some hole-soldering.
I used the official guide as reference to get started.

# Features
* OLED Display
* MX Switches
* DHT11 and MPU6050 sensors.
* Some keycaps
* XIAO ESP32 C3
<img width="665" height="290" alt="Screenshot 2026-10-18 at 3 57 36 PM" src="https://github.com/user-attachments/assets/5fcc458f-64f8-40b8-a34e-b36806adcf28" />

# BOM
| Parts | Qty | Supplier | Cost/Item | Total Cost | Link |
|-------|-------|-------|-------|-------|-------|
| XIAO ESP32 c3 | 1 | LCSC | $5.00 | $5.00 | https://seeedstudio.com/Seeed-XIAO-ESP32C3-p-5431.html |
| 0.96 OLED | 1 | Amazon | $2.50 | $2.50 | https://www.amazon.com/dp/B0GBVWBWCR | 
|MPU6050|1|Amazon|$2.29|$2.29|https://www.amazon.com/dp/B0943SGP34|
|DHT11|1|Amazon|$3.33|$3.33|https://www.amazon.com/dp/B0BLG7R99R|
|MX Switches|4|Amazon|$0.18|$0.72|https://www.amazon.com/dp/B0FQP8VYX4|
|Keycaps|4|Amazon|$0.60|$2.40|https://www.amazon.com/dp/B0CQ2VLMVY|
|10k Resistor|1|Amazon|$0.05|$0.05|https://www.amazon.com/dp/B0B4JFPHTW|
|PCB|1|JLC|$10.00|$10.00|https://jlcpcb.com/|
|Estimated Total Shipping|1|||$0.00||
|Grand Total||||$26.29||


# CAD Model:
First designing the board components using Kicad, I had to add the actual brain, the components needed to recieve the signals from the sensors, buttons, and an OLED display component so the display actually works.
<img width="1046" height="742" alt="Screenshot 2026-10-18 at 3 59 40 PM" src="https://github.com/user-attachments/assets/10a81a9b-cbe5-4dc4-ade6-d6eb4d718c7c" />

<a href="https://kicanvas.org/?repo=https://github.com/TheTank87/HackClub-Starbie/tree/main/Starbie">
  <img src="https://github.com/TheTank87/HackClub-Starbie/blob/ccf2b87a4c0c2da5647c10054101eb9e2c20533c/button.png" alt="View PCB on KiCanvas" width="100">
</a>

# 3D Render
<img width="1081" height="628" alt="Starbie" src="https://github.com/user-attachments/assets/f9d785ec-600c-4c7c-9a5f-a347e0c2fa6d" />


# Firmware:
I used Ardunio IDE for firmware and I'm going to have to add the logic to make all my components work. All of these are hard coded, below is the table of what I'm going to add to the Starbie, however, in a future week where I actually put the firmware in, I might change some things after I learn the language used for the firmware.

| Control | Purpose |
| -------- | -------- |
| Button 1, first press  | Opens the menu.  |
| Tilting the board  | Moves a selector ball or cursor  |
| Button 1, 2nd press | Chooses highlighted action |
| Button 2 | Show/Hide stat screen |
| Shaking while seeing a pet | Gives the shake reaction |

 
