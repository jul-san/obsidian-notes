**Objects**
- Single instance of a class
- Three aspects
	- Name - variable name given 
	- Attritbute (member data) - data that describes the object
	- Behavior (member functions) - behavior of the object


**Class**
- Blueprint for objects
- User-defined type that describes what an object will look like
- Consists of a declaration and definition

**Protection Levels**
- Public - accessible from inside or outside of the object
- Private - only usable by the object

**Class Declaration Format**
```C++
class Name{
	public:
		//public member data and functions
	priavte:
		//private member data and functions
};
```

**Member Function Categories**
- Two Categories:
	- Mutators - changes the state of an object
	- Accessors - does NOT change the state of an object, declare with '**const**'

**Constructors**
- initializes the member data of an object
- same name as the class
- no return type

Example Class Declaration:
```c++
//Circle Class Example 
//circle.h

class Circle{
	public:
		//default contructor (no parameters)
		Circle();

		//constructor with a parameter
		Circle(double r);
		
		//setter functions
		void SetCenter(double x, double y);
		void SetRadius(double r);

		//does not change object
		void Draw() const;
		
		//getter function
		double GetArea() const;
		
	private:
		double radius;
		double center_x;
		double center_y;
};
```

Sample Calls:
```c++
//Using Circle Class Above

//object that runs default constructor
Circle c1;

//object runs constructor with one parameter
Circle c2(51.4);

c1.SetRadius(10);
c2.SetRadisu(20);

c1.SetCenter(100,200);
c1.Draw();

cout<<c1.GetArea()<<endl;
```


**Files and Syntax**
- '.h' files contain class declaration (**DECLARE**)
- '.cpp' files contain class definition (**DEFINE**)
- 'main.cpp' contains simple driver program and test classes (**USE**)

Defining
```c++
//Found in '.cpp' files
void ClassName::MemberName(){
	cout<<memberDataName<<endl;
}
```

Declaring
```c++
//Found in '.h' files
void FunctionName();
```

Using
```c++
//Found in main.cpp files
ClassName objectName;
```

Calling
```c++
//Calling member function of an object
objectName.MemberName();
```


**Fraction Class Example**

frac.h
```c++
class Fraction{
	public:
		//Default constructor
	   Fraction();

		//Constructor w/ parameters
	   Fraction(int n, int d=1);

	   void Input();
	   void Show() const;

	   //accessors (getters)
	   int GetNumerator() const;
	   int GetDenominator() const;

	   //mutator (setter)
	   bool SetValue(int n, int d);
   
	   double Evaluate() const;	
	private:
		//member data
	   int numerator;
	   int denominator;
};
```

frac.cpp
```c++
#inlcude <iostream>
#include "frac.h"
using namespace std;

//default constructor
Fraction::Fraction(){
	cout<<"Howdy";
	numerator = 0;
	denominator = 0;
}

//constructor that takes in parameters
Fraction::Fraction(int n, int d){
	//checks if fraction is legal (denom ≠ 0)
	if(SetValue(n, d) == false)
		SetValue(0, 1);
}

void Fraction::Input(){
	char divSign;
	do{
		cin>>numerator>>divSign>>denominator;

		if(denominator == 0)
			cout<<"Illegal Fraction."<<endl;
			
	}while(denominator == 0);
}

void Fraction::Show() const{
	cout<<numerator<<'/'<<denominator;
}

int Fraction::GetNumerator() const{
	return numerator;
}

int Fraction::GetDenominator() const{
	return denominator;
}

bool Fraction::SetValue(int n, int d){
	if(d == 0){
		return false;
	}
	else{
		numerator = n;
		denominator = d;
		return true;
	}
}

double Fraction::Evaluate() const{
	double n = numerator;
	double d = denominator;
	return (n/d);
}
```

main.cpp
```c++
#include<iostream>
#include "frac.h"
using namespace std;

int main(){
	//runs default constructor
	Fraction f1, f2;

	//rund constructor w/ parameters
	Fraction f3(3,4), f4(6);

	cout<<"The fraction f1 is "<<endl;
	f1.Show();

	cout<<"The fraction f2 is "<<endl;
	f2.Show();

	cout<<"The fraction f3 is "<<endl;
	f3.Show();

	cout<<"The fraction f4 is "<<endl;
	f4.Show();

	cout<<"Now enter the first fraction: "<<endl;
	f1.Input();
	cout<<"You entered "<<f1.Show()<<endl;

	cout<<"Now enter the second fraction: "<<endl;
	f2.Input();
	cout<<"You entered "<<f2.Show()<<endl;


	cout<<"\n The value of fraction 1 is "<<f1.Evaluate()<<'\n';
	cout<<"\n The value of fraction 2 is "<<f2.Evaluate()<<'\n';

	cout << "Goodbye!\n";
}
```