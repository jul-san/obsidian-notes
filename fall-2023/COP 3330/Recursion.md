- Function that calls itself
- Like iteration, allow a way for the recurive calls to stop
	- Infitnite recursion causes a crash

- If a function can be written recursively, then it can be written iteratively
```c++
//Task: Write a function that calculates n!

//Iterative Approach
unsigned long Factorial(int n){
	unsigned long f = 1;
	for (int i = n; i >= 1; i--){
		f*=i;
	}
	
	return f;
}

//Recursive Approach
unsigned long Factorial(int n){
	if(n<=1){
		return 1;
	}
	else{
		return (n*Factorial(n-1));
	}
}
```
