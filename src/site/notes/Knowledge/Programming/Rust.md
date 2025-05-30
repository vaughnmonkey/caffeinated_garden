---
{"dg-publish":true,"permalink":"/Knowledge/Programming/Rust/","tags":["programming/language","programming"]}
---


 


>[!sources]-
>- Academic Sources:
>	- [Rust (programming Language) wikipedia](https://en.wikipedia.org/wiki/Rust_(programming_language)) 
>	- [Improved Rust-Book](https://rust-book.cs.brown.edu/) 
>		- improved with quizzes by Brown university
>- [Rust-lang.ord](https://www.rust-lang.org/) 

| Syntax                                                                                                                                                                                   |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <ul><li>'&' to indicate borrowing a variable</li><li>"fn main() { 'program here' }" -> structure of main loop</li><li>"println!('printout here');" -> Rust Macro for printline</li></ul> |

{ .block-language-dataview}
| Terminal Commands                                                                                                                                                                                                                                                                                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <ul><li>"$ cargo new" -> build new cargo project</li><li>"$ cargo build" -> complies your cargo project into the executable</li><li>"$ cargo build -- release" -> which builds and optimizes your project</li><li>"$ cargo run" -> complies your cargo project into the executable and runs it</li><li>"$ cargo check " -> checks that your project would compile but doesn't make the executable</li></ul> |

{ .block-language-dataview}
# Research 
## First Googling 
- Fans known as Rustacians 
	- ![Pasted image 20250522075238.png|250](/img/user/Knowledge/Programming/Pasted%20image%2020250522075238.png) 
- What is rust?
	- a systems programming language designed for reliability, performance, and memory safety
	- created in 2012 
	- a direct response to the common memory errors experienced when using C/C++ programming
	- Started as Graydon Hoare's personal project and then was picked up by his employer Mozilla Research in 2006
	- doesn't adhere strictly to a [programming paradigm](https://en.wikipedia.org/wiki/Programming_paradigm) but is highly influenced by functional programming
		- meaning Rust is based on writing seperate functions and then using in the main loop of your programs?
- What is the best use cases for Rust?
	- everything??
	- website indicates:
		- Command Line (CLI tools)
		- WebAssembly
		- Networking 
		- Embedded
- How does Rust work?
	- has no "garbage collector" like most high level languages use for memory safety 
		- instead uses unique concept of ownership & borrowing to safe guard memory
		- by default all memory is immutable 
			- therefore can be used in Stack memory 
				- which has minimal performance overhead
	- Every value is assigned to a single variable known as its **OWNER** 
		- When this variable goes out of scope it is automatically dropped 
		- but values can be referenced from else where in the program without taking ownership via **BORROWING** 
		- Borrowing is checked at compile and this allows you full control over memory without leading to C style memory errors
			- prefixed by (syn:: '&' to indicate borrowing a variable) 

## [Rust-Book](https://rust-book.cs.brown.edu/title-page.html) 
- Install
	- using VS code as my ide 
	- had to download the [Visual Studio C++ Build tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/) and then the rustup executable but it was simple and easy to follow the instructions
- Hello World
	- (syn:: "fn main() { 'program here' }" -> structure of main loop ) 
	- (syn:: "println!('printout here');" -> Rust Macro for printline) 
		- Macros are slightly different than functions we'll find out more later
- Cargo
	- (cmd:: "$ cargo new" -> build new cargo project)  
	- (cmd:: "$ cargo build" -> complies your cargo project into the executable ) 
		- by default all builds will go into the cargo debug folder until you run (cmd:: "$ cargo build -- release" -> which builds and optimizes your project) this will make your code faster but takes much longer to compile.  
	- (cmd:: "$ cargo run" -> complies your cargo project into the executable and runs it) 
	- (cmd:: "$ cargo check " -> checks that your project would compile but doesn't make the executable ) 
	- 




# What is Rust?