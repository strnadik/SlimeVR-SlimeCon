# SlimeVR-SlimeCon
SlimeCon - A SlimeVR tracker with the form factor of a JoyCon!

## Main Features

- Small form-factor (JoyCon sized)
- Custom QSB
- Includes battery sense and charge & play
- Straps are widely available on [Aliexpress](https://www.aliexpress.com/item/1005008147257166.html) and such (Switch JoyCon accessory) for like 2$ a piece
- [Compatible with Meia's / Deyta's IMU units (LSM6DSR, LSM6DSV)](https://moffshop.deyta.de/)


# Required items

- 3D printed shell
- Custom QSB PCB
- [TP4056](https://www.aliexpress.com/item/1005006368807036.html)
- [Meia's / Deyta's LSM6DSR/LSM6DSV](https://moffshop.deyta.de/)
- [Wemos D1 Mini](https://www.aliexpress.com/item/1005007877904928.html)
- [1N5817 Shottky diode (SMD)](https://www.aliexpress.com/item/1005001835967051.html)
- [180k 0805 resistor](https://www.aliexpress.com/item/1005006144658512.html)
- [102050 1000mAh battery](https://www.aliexpress.com/item/1005008270331326.html)
- [MSK12C02 Switch](https://www.aliexpress.com/item/1005006710234187.html)

# How to make it

Order the Quick Solder Board from a PCB maker of your choice. I use JLCPCB.

Use the included gerber .zip.

For JLCPCB, use the default setting, 1.6mm thickness is OK. Only change is to leave the vias untented.

![qsbpic](https://github.com/strnadik/SlimeVR-SlimeCon/blob/main/pictures/slimePCB.png)

Simply put the Wemos D1, IMU and TP4056 on top of the board like this, align the holes and put your soldering iron into each, use plenty of solder. Flux optional - I use a Sn60Pb40 solder rich on lead so I often don't use additional flux. Leave your tip in for a little, so the solder binds the 2 vias together. 

![boardpic](https://github.com/strnadik/SlimeVR-SlimeCon/blob/main/pictures/IMG_5233.jpg)

Solder in the 180k resistor. 

Put the switch on the board, it should click in (there's 2 docking holes for the switch). Remember to solder all legs including the corner ones, otherwise the switch can hinge out of its place.

When soldering in the two D1 diodes, pay attention to the polarity strip on the top. Negative side is towards the Wemos D1.

For the battery, we're gonna sandwich it into the 2-via connection on TP4056. Solder the negative wire to B- and positive to B+.

I recommend testing it out at this stage before putting it into the shell. Plug it into your PC through the Wemos D1 USB-C. Go to the firmware flashing site and [use these settings (embed into the link)](https://slimevr-firmware.bscotch.ca/?config=eyJyZWxlYXNlIjoiU2xpbWVWUi9tYWluIiwiYm9hcmQiOnsidHlwZSI6IkJPQVJEX1dFTU9TRDFNSU5JIiwicGlucyI6eyJpbXVTREEiOiJEMiIsImltdVNDTCI6IkQxIiwibGVkIjoiMiJ9LCJsZWRJbnZlcnRlZCI6dHJ1ZSwiZW5hYmxlTGVkIjp0cnVlfSwiaW11cyI6W3siZW5hYmxlZCI6dHJ1ZSwidHlwZSI6IklNVV9MU002RFNSIiwicm90YXRpb24iOiIzNjAiLCJpbXVJTlQiOiJENSJ9LHsiZW5hYmxlZCI6ZmFsc2UsInR5cGUiOiJJTVVfQk1JMTYwIiwicm90YXRpb24iOjI3MCwiaW11SU5UIjoiRDYifV0sImJhdHRlcnkiOnsidHlwZSI6IkJBVF9FWFRFUk5BTCIsInJlc2lzdGFuY2UiOjE4MCwicjEiOjEwMCwicjIiOjIyMCwicGluIjoiQTAifSwic3dhcEFkZHJlc3NlcyI6ZmFsc2UsImRlYnVnIjp7InVzZTZBeGlzIjp0cnVlLCJvcHRpbWl6ZVVwZGF0ZXMiOnRydWUsImNvbXBsaWFuY2VNb2RlIjp0cnVlLCJibWkxNjBVc2VUZW1wY2FsIjp0cnVlLCJibWkxNjBUZW1wY2FsRGVidWciOmZhbHNlLCJibWkxNjBVc2VTZW5zY2FsIjp0cnVlfX0)

Keep in mind that for chest/hip trackers, you should set the angle to 270.

Once flashed, it should appear on your SlimeVR Server. If the battery sense won't show up, touch up on your resistor on both sides, and the A0 on Wemos D1. 

Now take the bottom part of the shell, and insert the pcb angled like on this photo.

![shell1](https://github.com/strnadik/SlimeVR-SlimeCon/blob/main/pictures/IMG_5234.jpg)

![shell2](https://github.com/strnadik/SlimeVR-SlimeCon/blob/main/pictures/IMG_5236.jpg)

![shell3](https://github.com/strnadik/SlimeVR-SlimeCon/blob/main/pictures/IMG_5237.jpg)

![shell4](https://github.com/strnadik/SlimeVR-SlimeCon/blob/main/pictures/IMG_5238.jpg)

![shell5](https://github.com/strnadik/SlimeVR-SlimeCon/blob/main/pictures/IMG_5239.jpg)

![shell6](https://github.com/strnadik/SlimeVR-SlimeCon/blob/main/pictures/IMG_5240.jpg)
Then click it in, take the battery and put it on top of the pcb, wrap it into its own wires to make it compact. Take the top shell, insert it from once side, then click it on the other. Pay attention to the thickness of the top shell edges. One is thicker, that belongs to the TP4056 side. 

Click in. Done! Now just wedge it into the JoyCon velcro pouch and you're all set! 

![done](https://github.com/strnadik/SlimeVR-SlimeCon/blob/main/pictures/IMG_9836.jpg)

