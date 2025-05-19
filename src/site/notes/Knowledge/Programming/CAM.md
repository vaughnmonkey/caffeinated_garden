---
{"dg-publish":true,"permalink":"/Knowledge/Programming/CAM/","tags":["manufacturing/subtractive","control-systems/CnC"]}
---


 

>[!sources]-
>- Academic Sources:
>	- [Novel toolpath planning journal article](https://www.sciencedirect.com/science/article/abs/pii/S1526612523003316) 
>	- [Basic terms](https://fab.cba.mit.edu/classes/865.21/topics/path_planning/subtractive.html) 
>	- [MAS 865](https://fab.cba.mit.edu/classes/MAS.865/) 
>- Existing Open Source CAM: 
>	- [PyCAM](https://pycam.sourceforge.net/) 
>- 
# Research 

- What is CAM?
	- application of computational geometry for [subtractive tool path planning](https://fab.cba.mit.edu/classes/865.24/people/Fangzheng/path%20planning/Path_Planning.html) 
	- its a subset of the more general path planning used for all other robot applications
	- Hard to find resources on it but I figured it out eventually
- What are the standard algorithms used for basic CAM Tool path planning?
	- 
- Methods for Subtractive tool paths
	- Essential concepts (dependent on the subtractive tool in use)
		- Step-over:
			- thickness of material the tool cuts along a radial direction
		- Step-down:
			- thickness of material the tools cuts along it's axial direction.
	- Zig-zag:
		- for large areas with no potential collisions 
		- Back and forth across the whole surface, with seperation determined by the tool's step-over
	- Spiral:
		- alternative to Zig-zag 
		- spacing determined by step-over
	- Offset:
		- facing the bottom of a pocket (area that we can't crash into)
		- also used to finish vertical walls with a side or swarf milling cut
	- Adaptive Clearing / Trochoidal: 
		- specialized paths for roughing as quickly as possible 
	- Swarf: 
		- offset path for a (developable) surface, as opposed to a curve. 
			- offsets of planar, conical, and cylindrical faces can be determined analytically
			- NURBS surfaces must be approximated with specialized algorithms
- What is used in the open-sourced CAM toolboxs?
	- [FreeCAD CAM]()
	- [Bark Beetle](https://github.com/fellesverkstedet/Bark-beetle-parametric-toolpaths)
	- [PyCAM](https://pycam.sourceforge.net/) 
- 

# What is CAM? 

The simple answer is that CAM stands for Computer Aided Manufacturing, but that doesn't really tell you anything useful. So I'm hoping to compile a technical source for understanding what is going on under the hood of your CAM software. 
So far from what I can understand CAM is the application of [[Knowledge/Math/Computational-Geometry\|computational geometry]] for tool path planning. This is a fancy way of saying calculating how to move the machining tool to get the final shape from your 3d-Model. 