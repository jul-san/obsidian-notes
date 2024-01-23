**Types of Files**
- Header file - contains declarations, no implementation
	- fileName.h
- Implementation file - contains implementations of members
	- fileName.cpp


**Two Stages of Compilation**
- Compile stage
	- Syntax is checked for correctness
	- Variable and function declarations and calls checked for matching
	- Translation to object code
- Linking stage
	- Links object code to an executable program
	- Function calls are matched w/ definitions
	- Executable program is created

**Compiling C++ with  g++**

To compile a .cpp file and link to an executable
```c++
g++ <filename>

//example
g++ main.cpp
```
- Creates and executable called 'a.out' that will compile main.cpp

To run the compile stage but NOT the linking stage
```c++
g++ -c <filename>

//example
g++ -c main.cpp
```
- Translates file into object code (main.cpp turns into main.o)
- No executable is created

To create an executable with a name other than 'a.out':
```c++
g++ -o <executable name> <filename>

//example
g++ -o runThis main.cpp
```
- Creates and executable called 'runThis' that will compile main.cpp