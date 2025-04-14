---
{"dg-publish":true,"permalink":"/Personal Projects/MyCnC/","tags":["p_project"]}
---

### Resources 
- [CnC Cookbook](https://www.cnccookbook.com/) 
- 
### Ideas to Expand/Research
-  setting aluminum extrusions into my 3d printed molds before filling with contrete/epoxy granite to have solid non-plastic mounting points
	- or if they excist a bar of steel/iron with regular tapped holes
- 

# Applicable Knowledge
 - [[Knowledge/LinuxCnC\|LinuxCnC]]
	 - [Tutorial on using EitherCat in LinuxCnC ](https://forum.linuxcnc.org/ethercat/42048-notes-from-installation-of-ethercat-on-raspberry-pi-4#203806) 
		 - [video](https://www.youtube.com/watch?v=NQ-HnrusGJo) 
 - [[Personal Projects/BLDC/BLDC_Servo\|BLDC_Servo]]
 - [[Knowledge/Industrial/Ethercat\|Ethercat]]
	 - [EtherSweep](https://github.com/neumi/ethersweep) ethernet control of stepper motors currently wouldn't work for EtherCAT due to not having 2 ethernet sockets but the controller has the capability to support another socket so I am tempted to try redesigning the controller PCB to have 2 ethernet sockets. (this could be a massive project to attempt but I'm hoping that I would only need to make minor changes to the software for this to work)
	 - [light ethercat slave](https://sourceforge.net/p/ecslave/wiki/Howto/) 
	 - possible [ethercat slave hardware ](https://youtu.be/l3UzEkGvNVM?si=NLPmLq7a6gMfDBxc) 
	 - Make my own [[Personal Projects/EtherSweep+Power\|EtherSweep+Power]] 
 - [[Knowledge/Programming/ROS\|ROS]] 

# Project Tasks
- [ ] research and flesh out the [[Knowledge/LinuxCnC\|LinuxCnC]] knowledge file
- [ ] see if using diy bldc servos would be better for ethercat controlled cnc or if steppers are fine
- [ ] Look into Ros for Working with:
    - [ ] LinuxCnC
    - [ ] Ethercat connected motors and/or sensors
- [ ] Research Epoxy concrete as more dimensionally stable than water based for filling parts
    - [Tutorial](https://www.acncf.site/cnc_lathe_epoxy_granite_base/)

{ .block-language-dataview}

> [!hide]- old tasks
> - [ ] research and flesh out the [[Knowledge/LinuxCnC\|LinuxCnC]] knowledge file
> - [ ] see if using diy bldc servos would be better for ethercat controlled cnc or if steppers are fine
> - [x] research the delta style cnc design and see if a diy version is possible. if not then wait for the files of the concrete filled one from [Chris Borge Printables](https://www.printables.com/@ChrisBorge) 
> 	-  as of  2025/02/12 I couldn't find any reference to the horizontal delta style mill I saw and I worry that rigidity in that design would be extremely difficult so I'm gonna go with the Chris Borge design as my inspiration
> - [ ] Look into Ros for Working with:
> 	- [ ] LinuxCnC
> 	- [ ] Ethercat connected motors and/or sensors
> - [ ] Research Epoxy concrete as more dimensionally stable than water based for filling parts
> 	- [Tutorial](https://www.acncf.site/cnc_lathe_epoxy_granite_base/) 

# Materials 

- [EasyCAT Pro](https://www.bausano.net/en/easycat-pro-2) 
	- possible easy way to add ethercat functions to normal microcontrollers 
	- Cost = 179 euro
- [EpoCAT Controller](https://www.bausano.net/en/epocat-fr1000-fr4000-2) 
	- up to 5-axis cnc control with RTCP
	- Cost = 400 euros 
- 

# Project Writeup 

## Introduction 
I've always been interested in CnC machines, milling machines especially especially 3d printed ones. Chuck renewed my active interest in CnCs by asking me about what would be a good and cheap. The short answer is that there wasn't any particularly good CnC mills for any reasonable amount. *insert some examples of hobby mills* 

Also even the CnC machines that were decently priced where just the router types and none of the true mills. 
## Research 

The main source I'm wanting to use for my version of the CnC Mill is the one designed by Chris Borge. (sadly he hasn't yet released the Files. but his construction video was pretty extensive so I could just be loosely inspired by him and redesign my version from scratch. but I don't really want to have to do that I'd rather use large portions of his and make my own modifications)

### Chris Borge Notes
#### [Better CnC Mill](https://youtu.be/L8t82OQXefM?si=cvvtlAbtDrEuHpIJ)

- he switched the standard names of the Y and Z axis (I won't be coping that)

- Materials used
	- X & Y axis motors appear to be Nema17s 
	- 800w ER16 Spindle
	- Control Board: CAMTool CNC V3.3
	- ![Pasted image 20250212075508.png|500](/img/user/Personal%20Projects/Pasted%20image%2020250212075508.png)
	- 
- He says he won't release the files until he makes some improvements that he wants to do and doesn't feel like answering questions before then.
	- I really hope he releases them soon cause I'm really feeling the passion to make this a reality and would love to take advantage of it before I lose it. 
	- He Released the [Files!](https://www.printables.com/model/1237272-rock-solid-milling-machine-v09) 

#### [Modular CnC Controller](https://youtu.be/phtN679qpEM?si=Bce_1QwLNYwS_c5N) 

- mostly a 3d printed modular rack system but still could be useful
	- here is the current [3d Print files](https://www.printables.com/model/1188493-rackfinity-v1-open-source/files) 
- if I wanted to go with a more solid alternative this [mini-rack](https://mini-rack.jeffgeerling.com/) could be good for both CnC controller and home lab server
	- but it might be too shallow for a full sized computer so not be useful for LinuxCnC unless I can use the ethercat controlled motors then a single board computer would work fine.
- 

### Control

# Work Log

## 2025-04-14
- Changed to the new project format and published 