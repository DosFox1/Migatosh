IMPORTANT NOTE:
unfortunately I made an error with the Tang Nano footprint - turns out the Tang Nano 20K is 0.7" wide, not the common 0.6". Seriously. Why.
Either way VDEV2 will be completed shortly. 

# So what is it?
This is a board that combines two projects. 
The first is the incredible NanoMig from MiSTle DEV: https://github.com/MiSTle-Dev/NanoMig (TODO: upload firmware)
The second is an onboard Teensy ADB to USB converter is present to allow for a real ADB keyboard and mouse to be used with the core.
This uses the TMK firmware on the Teensy Pro (TODO: upload firmware).
The board also includes a Pi Pico as the companion microcontroller. 

As this is a tiny two layer PCB with minimal vias, the board is incredibly low cost to manufacture.
JLCPCB suggests five boards will cost £1.50 - 50p per board!

# Note on the serial port:
The board has not been built or tested at the moment.
As such, there is a chance there are gremlins still in the system - especially with the serial port.

Also keep in mind that this is RS232 only, not RS422!

For example, this should be able to print to an imagewriter - but it cannot connect to an appletalk network! (without workarounds!)

# Renders of the Board:

<img width="354" height="213" alt="migatosh low res top render" src="https://github.com/user-attachments/assets/01badb9f-ead8-40a2-8ead-f0493a4aa9b9" />

<img width="354" height="212" alt="migatosh low res bottom render" src="https://github.com/user-attachments/assets/abfff7a7-228e-4200-b501-99c2029c3c4e" />

# Main Dev Boards needed for this build:
1) Tang Nano 20K (main FPGA board)
2) Raspberry Pi Pico (companion microcontroller)
3) Arduino Pro (for the ADB to USB adapter)

# Notes on the firmware
It's intended to run the NanoMig core, with the 68EC020 core and 4mb Fastram enabled.

The two front buttons are intended to replace the two user buttons that are present on the Tang Nano 20K.
This is specifically for when I get around to designing a case for this.

This will need to be updated in the firmware (I'll upload examples at some point). 

This setup will allow for the system to run Shapeshifter - effectively turning this into a pretty terrible Macintosh II. 
With Shapeshifter, the system has around 2.7mb of RAM free. However, the display needs to be left in black and white - colour causes it to slow to a crawl!

Audio output is only through HDMI, annoyingly. 

This system can support the other available cores (NanoMac for a 68000 Mac Core, MiSTeryNano for an Atari ST core).

I guess you could also use this as an Amiga if you really wanted to?

# TODO:
Upload example Amiga firmware with modifications to use the two onboard buttons, as well as the 68EC020 core and 4mb Fast RAM. 
Upload TMK Firmware for the Teensy
Design a Case

# License:
CERN Permissive
