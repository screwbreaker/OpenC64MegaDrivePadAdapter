# OpenC64MegaDrivePadAdapter
OpenC64MegaDrivePadAdapter is an Open Hardware adapter that allows the safe connection of a Sega Mega Drive (known as *Genesis* in the US) controller to a Commodore 64 or Amiga computer.

![Board](https://raw.githubusercontent.com/screwbreaker/OpenC64MegaDrivePadAdapter/master/doc/render-top.png)

### Synopsis
This board is a fork of a project of SukkoPera: [github.com/SukkoPera](https://github.com/SukkoPera/), also this document is based on the original version.

The original version of this board can be found here: [github.com/SukkoPera/OpenC64MegaDrivePadAdapter](https://github.com/SukkoPera/OpenC64MegaDrivePadAdapter)

In this version the PCB has a particular shape in order to manage with the Amiga 600 case.
A manual cut of the DB9 connector still required in order to allow this adapter to fit into the A600 port 2. If you are not confident with cut tools, don't do it! A simple extension cable is a perfect and easy solution for this problem. 

This version use switches instead jumpers, this make the configuration much easier, plus now is impossible to set an improper configuration.
Is still recommended to turn off the computer before change the configuration.
The UP direction on the D-PAD is always active, it cannot be disabled. It can be used together with another button configured as UP. An extra diode (D6) is used to separate the two UP lines.

The transistor was biased in a different way to fix an issue with the [OpenAmigaJoyMouseSwitcher](https://github.com/SukkoPera/OpenAmigaJoyMouseSwitcher).

### Summary
Despite being compatible at the physical level (i.e.: they use the same DB-9 connectors), Sega Mega Drive controllers are slightly different from the *Atari-style joysticks* (which the C64 uses) at the electrical level. These differences usually manifest themselves in the fact that certain keyboard keys are not responsive when a Sega Mega Drive pad is connected to a C64 computer, but the CIA chip may also get harmed as a result.

Since I think that the Sega Mega Drive controller is one of the best joypads which ever saw the light, I developed this simple adapter board, which is supposed to sit inbetween the computer and the controller. You should be able to keep it plugged into the computer and then connect the controller to it, but you can also use a joystick extension cord (widely available), if that makes it easier.

Button B will work as the normal fire button, but this adapter also allows using Button C as the second fire button, for those games that support two buttons.

While this all works out of the box on Amiga computers, this adapter also allows to customize the button mapping to a certain degree: for instance, replacing UP with C might make some games more comfortable to play. This might be useful on the Amiga as well, so the adapter also supports an Amiga mode.

In this version the D-PAD UP is always active, it ca be used in games as usual, this is andy for games witch use UP for multiple things: menu, jump, go upstairs, etc.

### Configuration
The board is based on the circuit that was originally published in [issue #5 of Commodore world](https://www.scribd.com/document/8945979/Commodore-World-Issue-05) back in 1994, with a few improvements that will allow an easier gameplay with certain titles.

First of all, be sure to move the C64/Amiga switch to the proper position, before connecting the adapter.

Since most joysticks back in the day only had a single fire button, it was usually used for *firing*, whatever that meant. *Jumping* was usually done with the UP direction of the joystick, which is quite annoying on a joypad.
This is why OpenC64MegaDrivePadAdapter allows you to repurpose the B or C key to jumping, leaving the other button for firing, all at your choice.
It also allows to use C as the second fire button, which is only supported by a few titles. You can even swap B and C, if you prefer.

The switches configurations are showed on a little table printed on the board. F1 and F2 on the table refers to FIRE1 and FIRE2 switches.

The FIRE1 switch select which button to use as FIRE 1, B or C.

The FIRE2 switch select which action the FIRE 2 button must perform, UP (the same of the D-PAD UP) or FIRE.

**ALWAYS TURN YOUR COMPUTER OFF BEFORE MOVING THE CONFIGURATION SWITCHES.**
If you don't follow this rule, **you will probably cause permanent damage to your computer and/or controller**, so **please be careful**, you have been warned.

### Compatibility
This adapter is compatible with every MD gamepad, even the 6 buttons one. And also with the Master System gamepad.

The Mega Drive gamepad is designed to be back compatible with the Master System. B and C on the Mega Drive are BUTTON 1 and BUTTON 2 on the Master System.

To add more buttons on the Mega Drive, SEGA added an extra line (SELECT) wich is toggled HIGH or LOW. The state of this line determinate wich set of buttons the pad must return (B and C or A and START).
Since in this adapter the SELECT line is always HIGH, only the B and C buttons are used.

### License
OpenC64MegaDrivePadAdapter is Open Hardware. If you make any modifications to the board, please contribute them back.

### Support the Project
Since the project is open you are free to get the PCBs made by your preferred manufacturer, however in case you want to support the development, you can order them from PCBWay:

[![PCB from PCBWay](https://www.pcbway.com/project/img/images/frompcbway.png)](https://www.pcbway.com)

You get cheap, professionally-made and good quality PCBs, the autor of the board get some credit that will help with this and [other projects](https://www.pcbway.com/project/member/shareproject/?bmbid=41100). You won't even have to worry about the various PCB options, it's all pre-configured for you!

Also, if you still have to register to that site, [you can use this link](https://www.pcbway.com/setinvite.aspx?inviteid=41100) to get some bonus initial credit (and some more to the author).

Again, if you want to use another manufacturer, feel free to, don't feel obligated :).

### Get Support
If you need help or have questions, you can join [the official Telegram group](https://t.me/joinchat/HUHdWBC9J9JnYIrvTYfZmg).
