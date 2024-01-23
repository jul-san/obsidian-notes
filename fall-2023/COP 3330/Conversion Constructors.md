- Conversion Constructor - constructor with one parameter
	- Compiler will use this to convert parameter type to class type

Example:
```c++
//converts type int to type Class
Class(int x);
```
*You do NOT have to type this declaration! This is built into C++*

**Implicit vs. Explicit Conversions**
- Say you create two function definitions:
	- One takes an int parameter
	- Another one takes a string parameter

Example:
```c++
Class::Class(int n){
	m_Number = n;
}

Class::Class(string t){
	m_Text = m;
}
```

