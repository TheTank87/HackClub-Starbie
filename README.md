# Starbie PCB
This Starbie board will be my first project and I will program it to do some cool things.

<img width="626" height="522" alt="3DRender" src="https://github.com/user-attachments/assets/d30b5715-7859-498a-82db-3c8a08a51001" />

# Description
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

# Process
## CAD Model:
To start designing the Starbie, I had to first download Kicad, which was pretty easy. The next part of learning to navigate Kicad and all its features. I learned that Kicad on mac was very different from Kicad on windows. It turns out that the files and preferences tabber were on the very tippy top that I somehow missed. 
The actual designing process was making the schematic and I learned a few keyboard shortcuts that made the workflow more smooth and efficient. It turns out that making schematics are really easy, but I had to understand what each part does and where each port goes to make things work. I had to watch a few videos on these to truly understand why the guide wired the components a specific way.

<img width="1046" height="742" alt="Screenshot 2026-10-18 at 3 59 40 PM" src="https://github.com/user-attachments/assets/10a81a9b-cbe5-4dc4-ade6-d6eb4d718c7c" />

Btw, I also created this cool button you can press, it does something!
<a href="https://kicanvas.org/?repo=https://github.com/TheTank87/HackClub-Starbie/tree/main/Starbie">
  <img src="https://github.com/TheTank87/HackClub-Starbie/blob/ccf2b87a4c0c2da5647c10054101eb9e2c20533c/button.png" alt="View PCB on KiCanvas" width="100">
</a>


## Firmware:
I used Ardunio IDE for the firmware, it turns out there are MANY types of firmware I could choose from and there’s also this thing called circuit python that people also use. I am a novice at python so I was able to read the code.py, however, there was still a lot of jargon that I still don’t understand, so I’ll just go with the flow for now and learn it later. The code the guide gave basically told my board to have these functions though, that I understood. Controls layout below:

| Control | Purpose |
| -------- | -------- |
| Button 1, first press  | Opens the menu.  |
| Tilting the board  | Moves a selector ball or cursor  |
| Button 1, 2nd press | Chooses highlighted action |
| Button 2 | Show/Hide stat screen |
| Shaking while seeing a pet | Gives the shake reaction |

 
