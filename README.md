# vga_arcade
1TE663 project

One Arduino controls the VGA output, controls the slave Arduino to play music/sfx, reads Wii-controller and handles the game logic.

The code produces 2-bit color output, and in this project we have used the following colors:
| | R | G | B|
| --- | --- | --- | --- |
|00: Black|	0|	0|	0|
|01: Cyan|	0|	1|	1|
|10: Red|	1|	0|	0|
|11: White|	1|	1|	1|

The VGA-signal is produced using two interrupts.

TIMER1_OVF_vect: VSYNC interrupt, 60Hz

TIMER2_OVF_vect: HSYNC interrupt, 15kHz


The project milestones:
- [x] Get a stable VGA image on a TFT-screen using PWM.
- [x] Use an analog potentiometer to control the game paddle.
- [x] Moving bouncing ball in a playable game.
- [ ] Use a Wii-nunchuk (I2C) to control the game paddle.
- [ ] Create advanced music and sfx using a secondary Arduino.
- [ ] Create an simple AI that can play against a human player.
- [ ] Create a 3D-printed box for the hardware.
- [ ] Create the project report (=> 10 pages).
- [ ] Create a project presentation (Google Presentation).

The actual project progress are marked below:
- [x] Code adjustment for C++ syntax.
- [x] Prototype hardware constructed and assembled.
- [x] Both ordinary buttons are now active low with internal pull-ups.
- [ ] Simple buzzer sound effects mute function.
- [ ] Blue VGA-line connected to green. TODO: Improve VGAX to use more colors.
- [ ] Wii-nunchuk routine will be created.
- [ ] SID Music and sound effects using an slave Atmel 328P. :slightly_smiling_face:


## External resources
This project uses the following public libraries as code sections in this project. The libraries are often modified to suit this project and we have made comments in the code when edits are made. In some parts of this project only smaller fractions of the public libraries are used.

VGAXUA Library for Arduino UNO and MEGA [https://github.com/smaffer/vgaxua](https://github.com/smaffer/vgaxua)

Electrical connections for VGA-cable [https://forum.arduino.cc/t/vga-library-for-arduino-uno-and-atmega328/308936](https://forum.arduino.cc/t/vga-library-for-arduino-uno-and-atmega328/308936)

VGA Breakout With Arduino Uno [https://www.instructables.com/VGA-Breakout-With-Arduino-Uno/](https://www.instructables.com/VGA-Breakout-With-Arduino-Uno/)

Wii-Nunchuk communication [https://github.com/infusion/Fritzing](https://github.com/infusion/Fritzing)

MOS6581 SID Emulator Arduino Library [https://github.com/cybernesto/sid-arduino-lib](https://github.com/cybernesto/sid-arduino-lib)

MOS6581 SID Emulator Extra examples [https://github.com/daitangio/sid-arduino-lib](https://github.com/daitangio/sid-arduino-lib)

