---
{"dg-publish":true,"permalink":"/Personal-Projects/TabDesk/","tags":["p_project","diy","desktopComputer"]}
---

# Applicable Knowledge
- Circuit Design / Electrical Engineering
- CAD design of the case 
- Linux for the operating system
	- figure out how to do WINE for Solidworks and other necessities from windows
		- for beginnings might just stick with windows until I'm good enough at FreeCAD to switch over unless I run into some windows based errors with this build
		- React OS might be an option that works with Solidworks but I'm more and more tempted to just get good at FreeCAD and if it's missing any features I want then I'll just code them in myself!
- Firmware design?(idk if that would actually be needed since it seems mostly like desoldering ports to make things lower profile)
- [[Knowledge/Electroplating\|Electroplating]] 3d printed parts for sudo machined parts
	- (JB welds + Metal Finish paint) as the cheap man's electroplating

## Resources 
- [MNT Laptops](https://source.mnt.re/reform/reform-next) 
	- could be good for lots of the hardware connections and designs
- [Framework 12](https://frame.work/laptop12) 
	- could be perfect for a small screen with digitizer 
	- and looked into using their weird connector for the tablet -> keyboard
		- its currently more complicated then its worth and I'll just use an Oculink cable and usb-c pogo pins connector

# Project Tasks

- [ ] do the project
- [ ] find out how to properly bend heat pipes into a desired shape? (3d print a bending jig)
- [ ] oculink switching options?
- [ ] reversible power connector?
- [ ] limits of usb-c power delivery and risks for data/input transfer at the same time. 

{ .block-language-dataview}

##### Old Tasks 
> [!hide]- 
> - [ ] do the project
> - [x] Compile a parts list ✅ 2025-04-04
> 	- [x] Each needed category 
> 	- [x] multiple options for each needed part
> - [x] watch and take notes on Inspiration video
> 	- [x] including parts and what modifications that he made
> 	-  there wasn't much information on the video
> - [ ] find out how to properly bend heat pipes into a desired shape? (3d print a bending jig)
> 

 
# Project Writeup 

## Introduction/[Inspiration](https://www.youtube.com/watch?v=SfUCBTpOvCE) 
I want to create a tablet computer utilizing as many of the "off-the-shelf" components of a desktop computer as possible. I don't see any reason that portable computers need to be stuck in this non-upgradable hell that is the current market. There are some companies that are trying to do similar like framework but I think I can make something interesting and uniquely suited to me.

My use case for this device would be a combination of mobile CAD workstation, programming/debuging tool and a note-taking tool (mainly with obsidian but also using the Excalidraw plugin for sketches). I know this is a lot to fit into a small package but I don't think it's impossible.

My current thoughts on the structure and components are a variation of the linked inspiration video. It would probably need to be the Mini-ITX style motherboard since that is the smallest that I can find with the standard cpu sockets. Then for other internals I just thought of maybe using some of the Framework internals if they can be made compatible. otherwise I'll mirror the video(which I still need to thourghly watch and take notes on) but instead of making it a normal laptop like his. I want to use the tablet as it's own device for the lighter weight work and then be able to dock the tablet into a keyboard that would connect the tablet to a dedicated graphics card and an extended battery bank.


# Hardware

## from video
- Motherboard : A520I AC
- Cpu: rizen 5
- RAM: Low profile
- Graphics Card: random card that he cut shit off of
- Monitor/Screen: random portable monitor
- Battery systems: No battery he lost interest
- Cooling:
	- heat pipes
		- bent around pipe and used jb-welds mixed with thermal paste 
	- aluminum heatsinks
	- custom printed fan using stock motors
	- 
- keyboard: random usb keyboard. 

## My Hardware
- Motherboard:
	- [X600TM-ITX](https://asrock.com/mb/AMD/X600TM-ITX/) [Sale Link (china-only release)](https://parcelup.com/shop/item.php?id=810173778124#5500347116648) $138
		-  Thin Mini-ITX Form factor: 6.7-in x 6.7-in, 17.0 cm x 17.0 cm x 15mm Height ?
			- BIOS: 256Mb AMI UEFI Legal BIOS with GUI support
			* (Optional) 1 x Onboard TPM 2.0 (INFINEON SLB9672 or NUVOTON NPCT750AADYX)  
			- 1 x Chassis Intrusion Header  
			- 1 x Panel Voltage Selection Header  
			- 1 x Backlight Inverter Voltage Selection Header  
			- 1 x FPD Brightness Header  
			- 1 x Panel Off Header  
			- 1 x LVDS Connector  
			- 1 x CPU Fan Connector (4-pin)  
			* The CPU Fan Connector supports the CPU fan of maximum 1A (12W) fan power.  
			- 1 x 4 pin 19V Power Connector  
			* (Optional) 1 x Chassis Fan Connector (4-pin) (Smart Fan Speed Control)  
			- 1 x Front Panel Audio Connector  
			- 1 x Internal Speaker Header (4-Pin)  
			- 1 x Digital MIC Header  
			- 2 x SATA Power Connectors  
			- 1 x USB 2.0 Header (Supports 2 USB 2.0 ports) (Supports ESD Protection)  
			- 1 x USB 3.2 Gen1 Header (Supports 2 USB 3.2 Gen1 ports) (Supports ESD Protection)
			- Supports AMD AM5 Socket CPUs (Ryzen™ 9000, 8000 and 7000 Series Processors, up to 65W)
			- Supports Intel® CPU Cooler
			- Supports Dual DDR5 6400+(OC)MHz memory, Max. 96GB
			- Multi Video Outputs: Dual HDMI, one DisplayPort, **one LVDS**
			- Quad Storage Devices: Dual Hyper M.2 Socket (PCIe Gen4x4), Dual SATA 6Gb
			- Abundant USB Ports:  
			    1 x USB 3.2 Gen2 Type-C Ports,  
			    1 x USB 3.2 Gen2 Type-A Port,  
			    2 x USB 3.2 Gen1 Type-A Ports
- CPU: Ryzen 5 7600X ? maybe the 7 idk I think the 5 is enough and would be less power hungry but for handheld performance the 7 could be nicer
- RAM: maximize ram and ram speed for future-proofing
- m.2 -> occulink i4 cable (i8 would be better but that would need a full pcie slot and thats unlikely on a TM-ITX mobo)
- Cooling: 
	- heat pipes with fans 
		- How to bend heat pipes properly?: [Source](https://celsiainc.com/heat-sink-blog/heat-pipe-design-guide/?utm_source=LinkedIn&utm_medium=Microblog+Link&utm_campaign=Bending+Heat+Pipes) for heat pipe info
			- Bending the heat pipe will also affect the maximum power handling capacity, for which the following rules of thumb should be kept in mind.
				- First, minimum bend radius is three times the diameter of the heat pipe.
				- Second, every 45 degree bend will reduce Q_max by about 2.5%.  From Table 1, an 8 mm heat pipe, when flattened to 2.5mm, has a Q_max of 52 W.  Bending it 90 degrees would result in a further 5% reduction.  The new Q_max would be 52 – 2.55 = 49.45 W.
	- might have found the perfect [cpu cooler](https://www.ebay.com/itm/334085185276?mkcid=16&mkevt=1&mkrid=711-127632-2357-0&ssspo=gRe709TGSki&sssrc=4429486&ssuid=nsrn4h6ctkw&var=&widget_ver=artemis&media=COPY) that would work without modifications for this build
- Graphics Card: 
	- whatever I have around at least for now.
	- occulink i4 converter/port/dock  
- Monitor/Screen:
	- [xp-pen 10.1"](https://www.xp-pen.com/store/buy/artist-10-2nd-gen.html) (might not have multi-touch support?)
		- has some built-in hotkeys that could be coinvent to have.
	- Lenovo ThinkVision LT1423p (13.3")
	- ASUS ZENSCREEN MB14AC (14")
	- [BT-12HDT](https://www.aliexpress.com/i/3256805875327431.html?gatewayAdapt=4itemAdapt) (11.6")  ⭐ ($169/$212) 
		- this is a drawing tablet with touch support
		- the one with built-in hotkeys is ~$45 more expensive and makes the device larger than necessary so I'm leaning towards not having it, but IDK cause hotkeys on a tablet sound nice as fuck to have.
	- surface go replacement screen using LVDS cable into mobo
		- 
- Battery System: 
	- (18650 cells connected to a controller, induvial cells but 3d-print a case to enable fast swapping) 
		- adapt the mnt reform next battery system. (need to take their extremely integrated system and distil it down into a more standalone verson.)
			- [Battery holders](https://shop.mntre.com/products/protected-battery-board) ($30 per pair) from mnt reform built-in under/over voltage protections
			- need to check voltage of their system and probably add more cells to have any reasonable battery life. 
		- to make the batteries appear as a normal backup battery [HID UPS Power Device](https://github.com/abratchik/HIDPowerDevice) 
		- [Guide for 18650 battery packs](https://hackaday.com/2019/06/12/an-exhaustive-guide-to-building-18650-packs/) 
		- [openUPS](https://www.mini-box.com/OpenUPS?sc=8&category=1264) 
	- [prebuilt ups](https://www.aliexpress.us/item/3256805086466053.html?gatewayAdapt=glo2usa4itemAdapt) ⭐ tempted to use this with a pico power supply just to get the project off the ground
		- would simplify the build extremely at least for the beginning but would also probably have less adaptability for the future
		- 
- Ports: 
	- use native ports on the mobo
		- v2:  Port boards similar to the Reform Next system.
- Case/Hinges: 
	- 3d printed case 
		- possibly using jb welds and metal spray paint to get nicer finish and help with rigidity/toughness.
	- framework or Reform Next hinges
- Keyboard: 
	- [MNT Reform Mechanical keyboard](https://shop.mntre.com/products/mnt-reform-keyboard-30) Dimensions: 28.5 cm x 13.1 cm x 1.7 cm ($140)
		- tempted to add the [MNT trackball](https://shop.mntre.com/products/mnt-reform-optical-trackball-module) ($54) instead of a touchpad but Idk if I like trackballs lol. 
	- tempted to get the bottom case for the MNT Reform so that the keyboard, trackball and batteries would all fit nicely but idk if it would fit like I wanted

# Work Log
## 2025-04-01
- Battery design work:
	- it might be easier to maximize amps for the battery configuration and then convert that into the correct voltage.
		- or I could make my life easy and for now just use a prebuilt ups as the battery

## 2025-04-04
- Working on [Cost analysis](https://docs.google.com/spreadsheets/d/1QRfptfgFWxblpQRR6fuZvzW0cqzBG6CAJUpwuBmoFps/edit?usp=sharing) 
- [x] Complete Cost analysis
	 ✅ 2025-04-04
- since I don't know the cost of the framework screen I will use the drawing tablet that I found for this cost estimate 
- Decided to go with the Ryzen 7 and I could just figure out how to underclock it when I'm not plugged in 
- might need a different keyboard since the MNT one is more expensive then my mobo (but I really like the look of that keyboard and think it would be perfect for this build.)
	- maybe just salvage one from my older laptops
- for battery simplicity and price I'm currently going with the prebuilt mini-ups and I added this y-pwr loadsharing adapter for using both batteries when it's plugged into the keyboard.
- I had the thought to make the hinge a 360 hinge so that if I connected the tablet backwards on the keyboard I could lay it flat and have the gpu and extra battery power but then I remembered that the oculink plug is not reversible 
	- I really wish it was but maybe I could put an oculink switch, (if thats a thing) then I could have 2 plugs on either side of the keyboard for the oculink and 1 reversible usbc pogo pins plug in the middle for the rest 
	- or have a separate power plug for either direction and when power connects that picks the side of the oculink port to enable? cold work

- [ ]  oculink switching options? 
- [ ] reversible power connector?
- [ ] limits of usb-c power delivery and risks for data/input transfer at the same time.

- this would be more powerful than the framework 13 options at the same price and with extra features of dedicated graphics and pen supported touch screen 
	- would be slightly less powerful than the framework 16 but have size and upgradability advantages over it.

## 2025-04-17
- this [console pc case](https://zaber.com.pl/sentry/) site might be a useful resource

- I'm worried that this build is going to be impossible to do in a way that actually satisfies my wants. But every other option that I think about or look at just completely fails to check the boxes. I wish the GPD Pocket 4 was better built with active pen support and had the expansion modules using PCIE instead of usb protocols.

- 