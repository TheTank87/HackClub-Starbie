# Starbie PCB
This Starbie board will be my first project and I will program it to do some cool things.

<img width="700" height="400" alt="3DRenderfrontweek1" src="https://github.com/user-attachments/assets/63713f97-f529-48f8-af6f-947bdfdfa8d5" />

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
The actual designing process was making the schematic and I learned a few keyboard shortcuts that made the workflow more smooth and efficient. It turns out that making schematics are really easy, but I had to understand what each part does and where each port goes to make things work. I had to watch a few videos on these to truly understand why the guide wired the components a specific way. The PCB wiring was pretty straight forward since there isn't a lot of components. If I rotated stuff the correct way, the copper stays straight and I avoid the need to require ratsnests. 

<img width="300" height="300" alt="Screenshot 2026-10-18 at 3 59 40 PM" src="https://github.com/user-attachments/assets/10a81a9b-cbe5-4dc4-ade6-d6eb4d718c7c" />
<img width="300" height="300" alt="PCBSketch" src="https://github.com/user-attachments/assets/db975aee-c103-466f-8a8d-63fab54b335e" />


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

# 3D Renders
<img width="300" height="300" alt="3DRenderfrontweek1" src="https://github.com/user-attachments/assets/413832f6-58c2-4b37-9f73-c55bdedeb6a7" />
<img width="300" height="300" alt="3DRenderbackweek1" src="https://github.com/user-attachments/assets/87068d33-0ae1-496b-8a27-4b2b56b9f6ac" />

### Thoughts on assembly

After this project gets approved, I might have to use some coins to get myself a solder, however, I could just always buy it myself later. To assembly things, I'll have to get the components as well as the board and we'll see if the components fit. Then I need to watch some videos on how to solder properly and do a couple of test runs on disposable junk before I can be confident that I don't mess up my components. Based on my knowledge, I should first assess where everything goes first and then solder. That'll be it for assembly, I would then need to figure out how to upload the firmware to the pcb which might take very little time because it's so well documented. Anyways, I'll figure it out during build week.
 
