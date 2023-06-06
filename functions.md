# Functions

**Function**: a function is a block of code that can return a value and that can be called wherever it is needed.

Example:

```c
void birthday() { // void is the data type of the return value, since we don't have a return value here, we use a void
	printf("Happy birthday to you!\n");
	printf("Happy birthday to you!\n");
	printf("Happy birthday dear you!\n");
	printf("Happy birthday to you!\n");
}

int main() {
	birthday(); // -> Happy birthday to you!
		    //    Happy birthday to you!
		    //    Happy birthday dear you!
		    //    Happy birthday to you!
	return 0;
}
```

## Function arguments

Functions can take in variables called **arguments** to be used inside of itself.

Example:

```c
void birthday(char s[], int x) { // the birthday function takes in two arguments: s (of type char) and x (of type int)
	printf("Happy birthday, dear %s!\n", s);
	printf("You are %d years old!\n", n);
}

int main() {
	char name[] = "DarkblooM";
	int age = 21;
	birthday(name, age); // -> Happy birthday, dear DarkblooM!
			     //    You are 21 years old! 
	return 0;
}
```

# Return statement

The `return` statement returns a value back to a calling function.

Example:

```c
double square(double x) { // this function expects to return a double
	double result = x * x;
	return result; // returning a double as expected by the function type indicated earlier
}

int main() {
	double n = square(3.14);
	printf("%lf", n); // -> 9.859600
	return 0;
}
```

## Ternary operators

Ternary operators behave as shortcuts to `if`/`else` statements when assigning or returning a value.

Example:

```c
int findMax(int x, int y) {
	return (x > y) ? x : y; // if x > y (?), then return x, else (:) return y
}

int main() {
	int max = findMax(3, 4);
	printf("%d", max); // -> 4
}
```

# Function prototypes

Prototyping a function is essentially declaring it without a body before `main()` to ensure that calls to said function are made with the correct arguments.

Example:

```c
void hello(char name, int age); // function prototype

int main() {
	char name[] = "DarkblooM";
	int age = 20;
	hello(name, age); // -> Hello DarkblooM
			  //    You are 20 years old
	return 0;
}

void hello(char name[], int age) { // function with body
	printf("Hello %s\n", name);
	printf("You are %d years old\n", age);
}
```

Many C compilers do not check for parameter matching, missing arguments will result in unexpected behavior.
A function prototype causes the compiler to flag an error if arguments are missing.
