# miffy-blinky! 🐰✨

This is my first PCB project. I made a custom Miffy-shaped blinky keychain following Hack Club's Stasis project started guide! 

![Miffy 3D Render](3d-view.png)

Coming from mostly web dev and frontend stuff, jumping into KiCad was definitely an experience. It turns out making a PCB is basically like doing UI design, except the components actually take up physical space and you can't just z index them away lol. 

### What I learned
* I learned how to physically route components on the PCB.
* I imported a custom DXF drawing for Miffy's face, but it wouldn't show up in the 3D viewer. Turns out CAD lines have a 0mm thickness by default, so I had to manually set the ink to 0.2mm so the factory actually prints it!
* Drawing the copper tracks is honestly like a puzzle game. You can't cross a front wire over another front wire without shorting the board, but you can drop a pin and draw on the back layer to go underneath. 

Super proud of how this turned out!

## Journal

I finally finished my first ever custom hardware project! I made a PCB shaped like Miffy, one of my favorite characters, that also doubles as a keychain.

## Schematic
The first step is in the schematic editor of KiCad to design the circuit. Here, I placed symbols for the 555 timer, a 4017 counter, a power bank, two capacitors, two resistors, and 10 LEDs.

In my Principles of Engineering class in school, we briefly covered circuitry, but I was under the assumption that everything needs to be connected. However, something cool I learned was using labels. This kept my schematic design cleaner and more readable.

![image](https://stasis.hackclub-assets.com/images/1776548844604-slpc8w.png)

## Footprints
I followed the guide to add the custom 4017 counter footprint to my project. Then, I switched to the PCB view, only to find that I couldn't actually move the LEDs. After a lot of troubleshooting, I realized that I hadn't added any footprints for the rest of my components like the actual LEDs.

## PCB Design
This was the most fun part!

### Positioning
Now that the footprints were installed, I uploaded a DXF file of Miffy. I learned about grouping and ungrouping and how to set each part of her face on the correct layer. I changed the border to be an Edge Cut for the outline of the PCB. Then, I placed the components and LEDs where I wanted on the board.

### Copper Wiring
Now that everything was positioned where I wanted it to be, I had to replace the ratsnets with copper tracks. This was both therapeutic and frustrating at times because you can't have two lines of the same color cross. When a red track blocked my path, I switched to the blue layer and vice versa.


![image](https://stasis.hackclub-assets.com/images/1776549165996-sya7a9.png)

The Design Rules Checker tool was extremely helpful because it helped me catch mistakes I made.

Finally, I added another hole from the Edge Cuts layer with a diameter of 1.5 mm to serve as the hole where I can insert my keychain later. I also converted Miffy's eyes and mouth into Polygons (this took a lot longer than expected) and filled them in.

## Gerbers
This was the last step, I just generated the gerber and drill files and saved them into a zip. Then, I went to JLCPCB to get a price estimate. I changed the color of my PCB to white, and so the drawings turned black, so it actually looks pretty similar to the original Miffy character!


![image](https://stasis.hackclub-assets.com/images/1776549341116-bizm2i.png)

I also pushed my files to GitHub and wrote up a quick README for my project.

## Final Thoughts
This was my first time working with PCBs and it was an awesome experience. Designing a physical object that I can hold in my hands is completely different from anything I've done before since I usually just write software. I learned a lot about designing readable schematics and positioning them on the actual PCB.

Even though there was a huge learning curve and a fair share of frustrating moments, I learned a lot and it was really fun!

I had so much fun building this Miffy blinky keychain and I'm definitely going to design more PCBs in the future!

---
<div align="center">

### This project was made for Hack Club's Stasis event.
</div>
