**Two Types of Memory Allocation**
- Static
	- Memory for variables is allocated by compiler
	- Exact size and type must be known, size is constant
- Dynamic
	- Memory allocated during run time
	- Allocated space is placed in the heap
		- Memory set aside for allocation
	- Must use pointers   :(

**Two Steps For Dynamic Allocation:**
1. Create dynamic space
2. Store the address in a pointer

**Allocating Space**
- Use the 'new' operator following by type
```c++
new int;
new double;
```

- For arrays:
```c++
new int[40];
new double[size];
```

- 'new' operator returns starting address which can be stored in a pointer
```cpp
//two-line statement
int * x;
x = new int;

//one-line statement
int * x = new int[size];
```

**Accessing the Space**
- Use pointers for single object
	- Deference the pointer to reach the target
```cpp
//dynamic integer
int* x = new int;

*x = 10;
cout<<*x;
```

- For dynamic arrays
```cpp
int* list = new int[size];

for(int i = 0; i < size; i++){
	list[i] = 0;
}

//bracket notation
list[5] = 20;

//pointer-offset notation
*(list + 7) = 15; // = list[7]
```

**Dellocation**
- Use the operator 'delete'

- For single object
```cpp
//dynamic int
int* x = new int;

//delete the space that the x points to
delete x;
```

- For dynamic arrays
```cpp
//dynamic array of integers
int* list = new int[size];

delete[] list;
list = 0;
```

**Steps to Dyanamically Resizing an Array**
- Say you want to rersize and original array by 5 spots
```cpp
int* list = new int[size];
```

Here are the steps:
1. Create a new array + the new size
```cpp
int* temp = new int[size +5];
```

2. Copy data from old array to a new array
```cpp
for(int i = 0; i < size; i++){
	temp[i] = list[i];
}
```

3. Delete the old array
```cpp
delete[] list;
```

4. Change the pointer
```cpp
list = temp;
```


**Dynamic Allocation of Objects**
- When the object is created, the constructor runs

Example of dyamic objects:
```cpp
Fraction *x, *y, *list;

x = new Fraction;
y = new Fraction(3, 5);

list = new Fraction[20];
```

Deallocation:
```cpp
delete x;
delete y;
delete[] list;
```

**Dot-Operator vs. Arrow-Operator**
- Dot-operator requires an obect name and 