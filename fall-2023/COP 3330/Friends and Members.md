- When defining functions, there are scenarios where having private data be accessed by outside functions can make a definition more efficient

**Scenario** 
- Define a function that checks to see if two fraction objects equal each other

Objects:
```c++
Fraction f1 (1,2);
Fraction f2 (2,4);
```

- There are two approaches to check for equality

**Function Call #1:**
```c++
Equals(f1, f2);
```

Possible declaration and definition:
```c++
//function declaration (frac.h)
bool Equals(Fraction x, Fraction y);

//function definition (frac.cpp)
//cross-multiplies to check for equality
bool Equals(Fraction x, Fraction y){
	if(x.GetNumerator()*y.GetDenominator()==
		y.GetNumerator()*x.GetDenominator){
			return true;
		}
	else{
		return false;	
	}
}
```
- Definition calls upon accesor functions from Fraction class to get data
- This works, but a more intutive and faster solution is possible

**Keyword 'friend'**
- 'friend' allows outside functions and classes to have access to private data
- To use it, include the keyword before function declaration

Another declaration and definition (more efficient):
```c++
//function declaration, includes keyword 'friend' (frac.h)
friend bool Equals(Fraction x, Fraction y);

//function definition (frac.cpp)
//same process but calls private data instead of calling acessors
bool Equals(Fraction x, Fraction y){
	if(x.numerator*y.denominator==
		y.numerator*x.denominator){
			return true;
		}
	else{
		return false;	
	}
}
```
- This works, much faster and simpler than the first solution

**Function Call #2**
```c++
f1.Equals(f2);
```

- In this method, 'friend' will not be used

Possible Definition and Declaration:
```c++
//function declaration (frac.h)
bool Equals(Fraction f);

//function definition (frac.cpp)
bool Fration::Equals(Fraction f){
	if(numerator*f.denominator==f.numerator*denominator){
		return true;
	}
	else{
		return false;
	}
}
```
