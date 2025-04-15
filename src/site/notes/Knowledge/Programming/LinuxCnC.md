---
{"dg-publish":true,"permalink":"/Knowledge/Programming/LinuxCnC/","tags":["programming/linux","control-systems/CnC","opensource","programming"]}
---


My current main focus is to use this to control servo/stepper motors via Ethercat 
### Resources 
- Hardware
	- [BeagleBone Parallel ](https://machinekoder.com/)
		- [CnC Cape](https://www.necitec.de/index.php/en/cnc-cape) 
	- Parallel Port options
		- [PCI Parallel Port Card](https://www.pmdx.com/1PARPCI) 
		-  [Parallel Port card for CnC](https://cnc4pc.com/a25-pci-parallel-port.html) 
	- [CnC Pendants USB](http://www.vistacnc.com/) 
	- [CnC Hardware](https://cnc4pc.com/)
- Software
	- [Machinekit Branch](https://www.machinekit.io/) : useful branch of LinuxCnC that focuses on a more specific Linux setup and has a image for Beaglebone (mostly focuses on a specific real time kernel)
	- [PyVCP, Python Virtual Control Panel](https://linuxcnc.org/docs/html/gui/pyvcp.html)  

# What is LinuxCnC
LinuxCnC is a free and open source CnC control software originally called EMC. It can drive milling machines, lathes, 3D printers, laser cutters, plasma cutters, robot arms, hexapods, and more.

- Runs under Linux (optionally with real-time extensions).
- Simple installation on Debian and Ubuntu, or via our Live/Install DVD/USB images.
- Accepts G-code input, drives CNC machines in response.
- Active user community.
- Several different GUIs available.
- Compatible with many popular machine control hardware interfaces.
- Supports rigid tapping, cutter compensation, and many other advanced control features.

# Why to use 

- The main advantage that I've been able to see is that LinuxCnC is much more robust and adaptable than GRBL which is also no longer being worked on.

- Another main advantage is the open source nature so that I don't need to pay for licensing 
- More robust and advanced control options than GRBL 

# Hardware 

## Host 
Any computer capable of running linux (some other requirements but fill that in latter)

## Connections 
- motor driver [Geckodrive G540 4-axis](https://www.geckodrive.com/product/g540-4-axis-digital-step-drive/) 
- 

