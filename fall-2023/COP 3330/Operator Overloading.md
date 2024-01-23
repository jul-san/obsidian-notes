- Creation of new operators for user-defined types

**Important Rules**
- Operater Overloading cannot:
	- Change precedence
	- Change associativity
	- Change its number of operands
	- Create new operators
	- The function of an operator (i.e. '+'' cannot subtract)

**friends Function vs. member Functions**
- Depending on the operator, they can be written as a member function, stand-alone function (w/ friend), or both

- For binary operators ((+), (-), (<), (/), (%), etc.)
	- Stand-alone - function w/ two parameters that takes both operands
	- Member function - first operand is the calling object, other is parameter

- For unary operators ((!), (++), (--), etc.)
	- Stand-alone - operand is a parameter
	- Member function - one calling object and NO parameters

**Format**
- Functions needs a:
	- Return type
	- Name
	- Parameter list

**Scenario #1**
- You want to add two Fraction objects
	- Write one function as a stand-alone
	- Write another function as a member

```c++
//Declaration

//stand-alone
friend Fraction operator+(Fraction f1, Fraction f2);

//member
	Fraction operator+(const Fraction& f) const;
```

```c++
//Definition

//stand-alone
Fraction operator+(Fraction f1, Fraction f2){
	Fraction result;

	result.numerator = (f1.numerator*f2.denominator)
					+(f2.numerator*f1.denominator);

	result.denominator = f1.denominator*f2.denominator;

	return result;
}

//member
Fraction Fraction::operator+(const Fraction& f2) const{
	Fraction result;
	
	result.numerator = (numerator*f2.denominator)
				+(f2.denominator*denominator);

	result.denominator = (denominator*f2.denominator);

	return result;
}
```


**Overloading Insertion (<<) and Extraction (>>) Operators**
- Compiler does not know about new object types we create, meaning that it does not know how to handle data that we want to input or output

Example:
```c++
Class x;

cout<<x;
cin>>x;
```
- The compiler does not know how to treat the variable x since it does not know how to deal with a new class type