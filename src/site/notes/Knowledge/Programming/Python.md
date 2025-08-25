---
{"dg-publish":true,"permalink":"/Knowledge/Programming/Python/","tags":["comp-sci"]}
---


 


>[!sources]-
>- Academic Sources:
>	- 
>-  [PySide6]() QT gui framework
>- 

# Function/Syntax Reference



# Research 
- Starting a Project
	- Creating an Environment 
		- using VS Code and assuming you already have python installed type the command below into your terminal to create an environment to contain your current packages to just be in this project.
			- `python -m venv .venv` 
			- To activate on windows using VScode
				- `./env/Scripts/activate`
- Important Packages
	- Pandas
		- data processing library
	- Pyside6
		- Library for making GUI using the API for QT 
		- `pip install`
	- Numpy 
		- math library

## Methods 
### \_Init\_
```python
class MyClass:
	def _init_(self,arg1,arg2,...):
		# Initialization of code here
```
- automictically called when you create and instance of a class
- constructor for the class
- useful for setup default values and check inputs 
- 

## Functions 
### Super()
- built in function 
	- helps to call methods and access attributes from a parent  class withing your subclass
	- allows inheritance and extension of behavior from the parent class
```python
class Animal:
	def _init_(self,name):
		self.name = name
class Dog(Animal):
	def _init_(self,name,breed):
		super()._init_(name) # call the parent class's constructor
		self.breed = breed # add on the breed attribute for dogs
```


# What is Python?

