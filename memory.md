# Memory

- **Memory**: an array of bytes within RAM
- **Memory block**: a single unit (byte) within memory, used to hold some value
- **Memory address**: the address of where a memory block is located

Example:

```c
char a = 'X';
char b = 'Y';
char c = 'Z';

printf("%d bytes\n", sizeof(a)); // -> 1 bytes
printf("%d bytes\n", sizeof(b)); // -> 1 bytes
printf("%d bytes\n", sizeof(c)); // -> 1 bytes

// use %p and & to display a memory address
printf("%p\n", &a);              // -> (memory addresses are never the same)
printf("%p\n", &b);
printf("%p\n", &c);
```

## Pointers

> `int *pX = &x;`: *integer pointer named pX is set to the address of x*

A pointer is a "variable-like" reference that holds a memory address to another variable, array, etc.

**Advantages of using pointers**:
- Less time in program execution
- Working on the original variable
- Possibility to create data structures (linked-list, stack, queue)
- Returning more than one value from functions
- Dynamic memory allocation

Example:

```c
int age = 20;
int *pAge = &age;      // pointers are initialized using this naming convention:
		       // [var type] *p[Name] = &[name];
		       // the * signifies that we are storing a variable's address

printf("%p\n", &age);  // memory address
printf("%d\n", age);   // -> 20

printf("%d\n", age);   // -> 20
printf("%d\n", *pAge); // -> 20
```

Pointers can be passed as arguments to functions:

```c
void printAge(int *pAge) {                       // take note of the *
	printf("You are %d years old\n", *pAge); // dereference: taking the value from the address stored in pAge
}

int main() {
	int age = 20;
	int *pAge = &age;

	printAge(pAge);                          // -> You are 20 years old

	return 0;
}
```
