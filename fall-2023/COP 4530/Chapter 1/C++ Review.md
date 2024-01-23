## **Recursion**
- A function that calls itself
- Two key points:
	- Must have a base case
	- If the functions calls itself, it must make progress

**Factorial Example**
``` c++
unsigned long Factorial(int n){
	if(n<=1) //base case
		return 1;
	else // making progress
		return n*Factorial(n-1);
}
```

- Many tasks can be done with loops instead
	- Make sure to not do infinite loops

**Factorial Example w/ Loop**
```c++
unsigned long Factorial(int n){
	unsigned long f = 1;
	
	for(int i = n; i >=1; i--) 
		f*=1;
	return f;
}
```

**Incorrect Factorial Implementation**
```c++
unsigned long Factorial(int n){
	if(n<=1)
		return 1;
	else
		return n*Factorial(n+1); // no way out
}
```

## Classes
- Defines abstract characteristics of things
	- Characteristics are attributes/properties
	- Can define behavior through methods
	- Properties and methods are called members

**Example of a Class**
```C++
class IntCell{
	public:
		//constructor
		IntCell(){
			storedValue = 0;
		}

		//constructor with parameters
		IntCell(int initialValue){
			storedValue = initialValue;
		}

		//accessor
		int read(){
			return storedValue;
		}

		//mutator
		void write(int x){
			storedValue = x;
		}
		
	private:
		//member data
		int storedValue;
};
```

## **Interface Vs. Implementation** 
- Interface typically defined in .h files
	- '#include' in cpp file
	- Known as a declaration
- Preprocessor commands
	- guards against multiple inclusion of .h files

**Example of an Interface**
```C++
#ifndef TEST_H
#define TEST_H

/*
 * Your class goes here
 */
 
#endif
```

**Example of an Implementation**
```C++
#include "IntCell.h"
IntCell::IntCell(int initialValue):storedValue{initialValue}{}

```

## **main() Function**
- Objects are declared just like primitive data types

**Example of Legal Declarations**
```C++
IntCell obj1;
IntCell obj2(12);
```

**Example of Illegal Declarations**
```C++
IntCell obj3 = 37;
IntCell obj4();
```

