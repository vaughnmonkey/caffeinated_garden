---
{"dg-publish":true,"permalink":"/Personal Projects/Thor_Arm/My Thor/","tags":["robotics","3d_printing","p_project"]}
---


- Sources 
	- [Original Thor Arm](http://thor.angel-lm.com/)
	- [Danny mods & addins](https://hackaday.io/project/16665-thor-robot-with-addons-and-gui).
	- [Sepio build of Danny's mods & his improvements](https://hackaday.io/project/26341-building-and-improving-the-thor-robot-arm) 
	- [Interactive Thor Assembly](https://angellm.github.io/ThorAssembly/) 

# Hardware 

## Printed Parts


## Electronics 
### Control Board
- Original creator used custom arduino mega board running grbl
	- becasue there wasn't commercial control boards that could drive 8 stepper motors
- Danny used ultrasonics board (no longer in production)
- I am thinking to use the [Octopus Pro](https://biqu.equipment/products/bigtreetech-octopus-pro-v1-0-chip-f446?_pos=1&_psq=BTT+Octopus+Pro&_ss=e&_v=1.0&variant=39482177257570) with STM32F446ZET6 since there is a grblHAL driver for that chip
	- 48V enabled 
	- 8 limit switches 
	- 8 motor drivers 
		- 12-60v motor input voltage
		- drive input level: 5v
- Along with a Screen from the same company for my manual control of Thor

### Encoders 
- I want to eventually implement absolute encoders 
	- probably magnetic
	- Chip might be
		- [AS5048A](https://ams.com/as5048a) 
			- 14-bit
			- built in magnetic sheilding! 
			- Best source to buy:
				- [Board](https://www.tindie.com/products/smallrobots/as5048a-encoder-board-for-robots-motor-control/) 
		- ~~[AS5600](https://ams.com/en/as5600)~~ (I want to do this right and the possiblity of interveriance worries me)
			- 12-bit
			- cheap

# Code 

## Firmware 
- GrBL cnc control 
	- If I use a 32-bit board then I will need to adapt [grblHAL](https://github.com/grblHAL) 
	- Angel modified the base GrBL firmware for the thor project 
		- Github has an in-built compare function so here are all the differences between regular GrBL and Angel's [Comparison](https://github.com/grbl/grbl/compare/master...AngelLM:grbl:master) 
		- In theory I should be able to use this to make similar modifications to grblHAL!

### Angel's changes to GrBL & My understanding of why
Angel made 12 commits changing 15 files

#### Commits
1.  XYZ references changed to ABC
2. Gcode XYZ references changed to ABC
3. Modified to allow control for 7 steppers, added test code
4. ATMEGA2560 map update
5. fix pin mapping
6. update, homing works!
7. 1st try
8. Everything works mapping must be modified soon
9. Added M95 command (home)
10. Thor default settings added

#### Files Changed & their purpose
- Makefile
- grbl/config.h
- grbl/cpu_map/cpu_map_atmega2560.h
- grbl/defaults.h
- grbl/defaults/defaults_generic.h
- grbl/defaults/defaults_thor.h
- grbl/gcode.c
- grble/gcode.h
- grbl/motion_control.c
- grbl/nuts_bolts.h
- grbl/report.c
- grbl/settings.c
- grbl/spindle_control.c
- grbl/stepper.c
- test.gcode

### Comparision of GrBL to grblHAL
Research to understand how GrBL and grblHAL are different/similar
-  

## Software
- hopefully if I properly integrate my controller with the grblHAL firmware I will be able to use the already developed software

### ROS 
- Plan to develop a ROS package to integrate my thor into ROS2 after I have the initial software working 
	- **this is the major step to make a manufacturing system since it will allow me to use ROS2 (industry standard) to manage and control my system.**

#### ROS Features I Want
- Joint angle postional control
- cartiasian positional control
- feedback sensors read 
- 


# Tasks 
- [ ] Figure out firmware
	- [ ] review changes by Angel to grbl for original Thor
	- [ ] figure out what changes would need to be made to grblHAL to get the same function
- [ ] Figure out Software
	- [ ] download and understand the GUI software made by Danny
		- [ ] understand if his stepper drivers are of any use to me
	- [ ] figure out how to use his code or if i'll need to start from scratch
- [ ] Hardware
	- [ ] assemble the thor arm from components printed
	- [ ]  Buy controller
		- [ ] wire and test basic movements
		- [ ] wire feedback (angle sensors & encoders)
- [ ] ROS
	- [ ] Make list of functions that Thor ros package should be able to do
	- [ ] 
