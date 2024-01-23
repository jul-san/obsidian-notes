- When multiple classes have similar behavior and code, inheritance can be used
	- Simplifies code

**Types of Classes**
- Base class - contains the main features of a program
- Derived class - utilizes similar functionalities of the base class
	- Inherits all of base class features

- Referred to a "is a " relationship
	- Think of subcategories

**Declaration**
- Derived class followed by base class
```c++
class derivedClass : public baseClass
```

Example with a Vehicle class:
```c++
class Vehicle{
	
}:

class Car : public Vehicle{

};
```


**Protection Levels**
- Public - members can be accesered by name from anywhere
- Private - members can be accesed only by class it's declared in
- Protected - members can be acessed by class its declared in and derived classes

**Constructors in Derived Class**
- Creating an object for a derived class will run the base construtor then derived constuctor

Example:
```c++
//Vehicle is the base
//Car is derived from Vehicle
//Honda is derived from Car

Vehicle x;
//Vehicle() runs
Car y;
//Vehicle() -> Car()
Honda z;
//Vehicle() -> Car() -> Honda()

```

- If we wanted to add parameters to a derived class, an initialization list is needed
```c++
function prototype : initialization list{

}
```


**Function Overriding**
- Used if you want to reuse a function from the base class

Example:
```C++
//Class Vehicle has the function Show() defined
Vehicle x;
Car y;
Honda z;

x.Show();
	//runs Show() from Vehicle class
y.Show();
	//runs Show() from Vehicle Class
z.Show();
	//runs Show() from Car class

```
