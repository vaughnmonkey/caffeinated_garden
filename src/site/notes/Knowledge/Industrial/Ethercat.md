---
{"dg-publish":true,"permalink":"/Knowledge/Industrial/Ethercat/","tags":["programming","electrical","industrial","diy/software"]}
---

#### My Understanding
```meta-bind
INPUT[progressBar:Understanding]
```

### Found Resources 
##### Software 
- [Open EtherCAT Society](https://openethercatsociety.github.io/) 
- [light ethercat slave](https://sourceforge.net/p/ecslave/wiki/Howto/)
- Join [EtherCat Technology Group](https://www.ethercat.org/en/membership_application.html) 
- [ROS Ethercat](https://github.com/shadow-robot/ros_ethercat) 
- 
##### Hardware 
- [EtherSweep](https://github.com/Neumi/ethersweep/tree/master) 
- [EtherCAT Servodrive](https://hackaday.io/project/181058-ethercat-servodrive) 
	- [EtherCAT Shield V1](https://kubabuda.github.io/ecat_servo/html/ax58100rev1_ibom.html) 
- [Beckoff dev board](https://www.beckhoff.com/en-us/products/i-o/ethercat-development-products/elxxxx-etxxxx-fbxxxx-hardware/fb1311.html) 
- [Adifruit POE power and data splitter 12v](https://www.adafruit.com/product/3238) 
- 

## Hardware Options
### Personal DIY Ethercat+Power Adapter
- make an ethercat+POE (connector) for any/as many as possible microntrollers/stepper motor drivers [[Personal-Projects/EtherCAT+POE\|EtherCAT+POE]]
	- apparently there is a Beckhoff dev board that does exactly that! so maybe I can clone it's circuit design if I can find a schematic or something like it.
	- found reference design by Texas Instruments [TIDA-01461](https://www.ti.com/tool/TIDA-01461#description) 
		- This reference design only adds power into and breaks power out of  an Ethercat system still useful but needs to be combined with something like the etherCAT shield to be what I wanted
		- has 24v,12v, and 5v outputs
		- compare this with the existing hobbyist EtherCAT shield
		- strip it down to bare bones with dip switch for different power voltages
#### Existing DIY Options
- [EtherSweep](https://github.com/Neumi/ethersweep/tree/master) 
- [EtherCAT Servodrive](https://hackaday.io/project/181058-ethercat-servodrive) 
	- [EtherCAT Shield V1](https://kubabuda.github.io/ecat_servo/html/ax58100rev1_ibom.html) 
### Professional Hardware
#### Hobbyist
- 

#### Industrial
- [Beckoff dev board](https://www.beckhoff.com/en-us/products/i-o/ethercat-development-products/elxxxx-etxxxx-fbxxxx-hardware/fb1311.html) 

---
# What is Ethercat
Ethercat is a specialized protocol for real-time industrial controls running on standard ethernet hardware. Ethercat can be chained together to make complex systems controlled by one chain of ethernet cables. 

## Different Versions of Ethercat 

### Ethercat


### Ethercat+Power (EthercatP)


### Functional Safety over EtherCAT (FSoE)
FSoE is a safety profile for transmitting safety-critical data over EtherCAT. It meets the highest safety requirements of SIL3, thereby enabling safe data communication.