- Some issues may arrive with arrays and iteration
	- Base class might not have enough storage to hold derived class
	- We may call the wrong type of function

**To Solve the Storage Issue**
- Use pointers
	- Base class can point to a derived class

Example;
```c++
Vehicle x; //base class
Car y; //derived from Vehicle

Vehicle *a, *b;

a = &x; //points at Vehicle
b = &y; //points at Car
```



**To Solve the Function Issue**
- Remember the different types of stages
	- [[Multiple File Compilation]]
zdxcghjk