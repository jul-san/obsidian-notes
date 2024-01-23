- Causes a value to not change 
- Can be used to express the programmers intent with a function or value

**const Reference Parameters**
- Pass-by-Value
	- A copy of an object is made, any R-value can be sent
- Pass-by-Reference
	- No copy is made, only L-values can be sent

- Passing by const reference can save lots of overhead (resources)

Example Declaration:
```c++
//pass-by-value
friend Class Add(Class x, Class y);


//pass by const reference
friend Class Add(const Class& x, const Class& y);
```
