---
{"dg-publish":true,"permalink":"/Knowledge/Programming/Python/","tags":["comp-sci"]}
---


 

>[!sources]-
>- Academic Sources:
>	- 
>-  [PySide6]() QT gui framework
>- 

# Research 
- Starting a Project
	- Creating an Environment 
		- using VS Code and assuming you already have python installed type the command below into your terminal to create an environment to contain your current packages to just be in this project.
			- `python -m venv .venv` 
			- To activate on windows using VScode
				- `./env/Scripts/activate`

- Debugging:
	- interactive console can run sections of code using `#%%` as the modifier to create the top of cell 
	- `pass` statement can make the framework for different objects
- Dunder methods -> (Double Underscore Methods)
	- special methods that run automatically when you do a common thing in your code
		- often not used directly and are more "" under the hood "" 
	- Examples are 
		- `__init__` 
			- initializes a new instance of the class
- ARGS & KWARGS
```python
def func(*args,**kwargs):
	pass
```
- allows an arbitrary numbers of arguments to be put into the function
	- ARGS -> Arbitrary Positional Arguments 
		- allows an arbitrary number of inputs
	- KWARGS -> Arbitrary Keyword Arguments
		- allows as many inputs as the user wants and lets them be tied to keywords
- Walrus operator  `:=`
	- assignment expression
	- allows you to create and assign value to the variable in line instead of needing a separate line 
		- ![Pasted image 20250828120600.png|300](/img/user/Knowledge/Programming/Pasted%20image%2020250828120600.png) 
	- Great for 
		- Loops 
		- list comprehension 
		- input validation
- Decorators
	- enhanceing function without perminatnly altering code 
	- create super functions by combining other functions
- with statement & context managers
	- has methods `__enter__` and `__exit__` 
- Slots Optimization `__slots__` 
	- Unique to Python
	- uses more compact internal structure  than the normal dict(key-value) structure 
	- best used for memory intensive applications
		- but can break functions that rely on `__dict__` or `vars()` 
- Else statement in Error handling 
	- only executes when no errors in the try block
- Mutible default arguments
	- data structure as an input 
## Libraries 
> [!abstract] Note:    
> Here are a lot of the Commonly used Python Libraries and I'll expand the subsections for the libraries that I have used personally with notes and/or tips that I found useful for them
### General

> [!hide]- Libraries I haven't used extensively yet
> - SQLAlchemy
> 	- powerful and userfriendly library for creating relational databases
> 	- work with dbs and tables without having to write in sql
> 		- works across many popular databases 
> - FastAPI
> 	- create APIs using python 
> - Pyglet
> 	- game library 
> - Visual Python
> 	- Vpython 
> 	- library for creating 3d objects 
> - Turtle
> 	- basic 2d drawing package
> - Pickle (not sure if this should go into data processing category or not)
> 	- serialization module 
> 	- convert data into serial bitstream to send data to different sources
> - Pillow
> 	- image processing and editing 
> - SQLite
> 	- serverless sql database building inside your python 
> - OpenCV
> 	- Image/camera processing 
> - Pygame
>	- basic game engine
#### PyWin32  	
- access to win32 apl on windows 	
- file access  	
- registry access 	
- ui elements control 	
- automate tasks on windows 
#### Py2exe
- make scripts into executables 

### Web Based Libraries
#### Site Builders / Frameworks

> [!hide]- Libraries I haven't used extensively yet
> - Django
> 	- framework for creating websites 
> 		- webpages = views
> 		- DBs = models
> 		- Logic = the controller
> 	- EMBEDD python into html
> - Flask
> 	- framework for websites (best for small scale projects)

#### Web-Scrapers / Bots

> [!hide]- Libraries I haven't used extensively yet
> - Beautiful Soup
> 	- basic html webscrapper
> - Mechanical Soup
> 	- basic database webscrapper
> - Selenium
> 	- more advanced webscrapper for dynamic and interactive websites
> - Scrapy
> 	-  framework for building webscrappers and bots
> 

### Math

> [!hide]- Libraries I haven't used extensively yet
> - Plotly
> 	- interactive charts
> - Theano
> 	- numerical computation (no longer in dev)
> - Matpoltlib
> 	- data visualization package
> - SymPy
> 	- symbolic math package
> - SciPy
> 	- science computing (numpy on steroids)
>

#### Numpy
- basic math library


#### Data Processing

> [!hide]- Libraries I haven't used extensively yet
> - Bokeh
> 	- take any data structure and create a data visualization from it  
> - RPy
> 	- lets you use the "R" programming language 
> 		- mainly for statistical computing and data anyliss

###### Pandas
- data processing library 
- Loads a large variety of file types into it's Data-Structure class

- Questions I had to lookup
	- How to trim values off the Data-Structure class?
		- 
#### Machine Learning/AI

> [!hide]- Libraries I haven't used extensively yet
> - SpaCy
> 	- advanced natural language processing 
> - Natural Language Toolkit
> 	- natural language processing library
> 		- can use N-gram algorythm
> - Sci-kit Learn
> 	- machine learning (supervised and unsupervised) general machine learning
> - PyBrain
> 	- machine learning (no longer maintained)

##### Tensorflow
-  AI deep-learning
##### Pytorch
- AI deep-learning more detail

### GUI 

> [!hide]- Libraries I haven't used extensively
>  - PyQT
> 	- gui interface for using Qt 
> 	- official one is Pyside6
> - Kivy
> 	- framework for mobile apps/ touchscreen AKA natural user interfaces 
> - Tkinter
> 	- basic GUI

#### PySide6
- Library for making GUI using the API for QT 
- `pip install PySide6`
- 

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

