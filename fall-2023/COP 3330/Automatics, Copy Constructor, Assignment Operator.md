**Automatic Function**s
- Default version is automatically built by the compiler
	- Constructor
	- Destructor
	- Copy constructor
	- Assignment operator

**Copy Constructor**
- Function with same name as class, no return type
- Invoked implicity when an object:
	- Has the value of another object of the same type
	- Is passed by value
	- Is returned by value

Example:
```cpp
Fraction f1, f2(3, 4);
Fraction f3 = f2; //f2 is being copied into f3 by default
```

