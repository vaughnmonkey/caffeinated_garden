---
{"dg-publish":true,"permalink":"/Personal-Projects/Home Server/","tags":["p_project"]}
---

> [!sources]
> - Sound Proofing
> 	- [Method for small and loud machines](https://acousticalsolutions.com/soundproofing-small-loud-machines/) 
> 	- [Possible Materials source](https://www.secondskinaudio.com/soundproofing/server-rack-soundproofing/) 
> 	- [3d printable structure best to absorb sound](https://pmc.ncbi.nlm.nih.gov/articles/PMC7284723/) 
> - 


# Project Tasks
- [ ] Do this Project
- [ ] Select and print a 3d printable rackmount case to use.
- [ ] select apps and figure out how many servers are going to be built from the different pcs I have laying around. 

{ .block-language-dataview}


# Project Writeup 

## Mission



## Software 
- Requirements 
	- needs to be free and preferably open source 
	- needs to be able to cluster the different "server devices" I have around.
	- needs manage the different programs running (PLex, file hosting, Home Assitant, Minecraft, and whatever else I want to run)

- I don't know anything about how to cluster old pcs into a functional server cluster
- But I will find out.
	- [ProxMox](https://www.proxmox.com/en/products/proxmox-virtual-environment/overview) : seems like the more popular server manager and it can cluster and run containerized webapps
		- is an open-source server manager platform
	- KuberNetes cluster was used in this [tutorial video](https://www.youtube.com/watch?v=S_pp_nc5QuI) 
		- apparently has different flavors and the video used [this](https://k3s.io/) and it could be more lightweight than Proxmox
	- Docker 
		- seems like this is most people's start at home labs 
		- things for Docker 
			- Heimdall
			- Portainer 
	- [Incus](https://linuxcontainers.org/incus) 
		- a next-generation system container, application container, and virtual machine manager
		- it runs on pretty much any Linux distribution and supports arm processors so it's now ahead of proxmox for being the backbone of my server 

### Self-Hosted Apps
- PLEX 
- Home Assistant 
	- this one is one I'm most interested in playing with to try and get local "" Alexa "" type functionality
- [PortNote](https://github.com/crocofied/PortNote) 
	- Managing what services are runnin on what port. 
- 


# Work Log 

## 2025-08-27
Project Started 
- [ ] Do this Project

Breaking this into 2 sections 1 for hardware and 1 for software


## 2025-10-06 

- I've finally gotten a little server rack and am going to start my homelab journey
- [x] Build the physical rack ✅ 2025-10-08
- [ ] Select and print a 3d printable rackmount case to use.
- [x] Decide/research the best software base to use (Proxmox, docker or something else.)
	- I'm going with Proxmox since it seems like the most robust and open solution to future scaling that I will want to do.
- [ ] select apps and figure out how many servers are going to be built from the different pcs I have laying around. 

- for the how many servers to make I'm thinking of saving my old lenovo laptop to be a Linux cnc controll panel but other than that I think I could use all the other hardware for different purposes 
- Since I have lots of older computers around to use as servers, I might want to go with Proxmox from the beginning since it has the ability to manage nodes across multiple devices more easily. but it might be easier to get a docker build off the ground quickly 
- 

