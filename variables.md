# Variables

A variable is an allocated space in memory to store value.

Example:

```c
int x;       // declaration
x = 23;      // initialization
int y = 321; // declaration + initialization
```

Different types of variables:

```c
int age = 21;            // integer
float gpa = 2.05;        // float
char grade = 'C';        // single character
char name[] = "Gaspard"; // array of characters
```

How to display variable values:

```c
printf("Hello %s!\n", name);                  // s for string
printf("You are %d years old.\n", age);       // d for decimal
printf("Your average grade is %c.\n", grade); // c for character
printf("Your GPA is %f.\n", gpa);             // f for float
```

## Constants

A constant is a fixed value that cannot be altered by the program during its execution.

Example:

```c
const float PI = 3.14159; // common convention is to right constant names in full uppercase
```

## Swapping values

Swapping the values between two variables is fairly simple:

```c
char a = 'A';
char b = 'B';
char temp;         // temporary variable that will hold a value during the swap

printf("%c\n", a); // -> A
printf("%c\n", b); // -> B

temp = a;          // assign a's value to temp
a = b;
b = temp;          // assign a's previous value stored in temp to b

printf("%c\n", a); // -> B
printf("%c\n", b); // -> A
```

Things get a little different when working with strings:

```c
char a[15] = "water"; // we specify a length to avoid unexpected behavior when swapping values 
char b[15] = "lemonade";
char temp[15];

printf("%s\n", a);    // -> water
printf("%s\n", b);    // -> lemonade

strcpy(temp, x);      // make sure to include the <string.h> library to use this function
strcpy(x, y);
strcpy(y, temp);

printf("%s\n", a);    // -> lemonade
printf("%s\n", b);    // -> water
```

## `typedef`

`typedef` is a reserved keyword that gives an existing datatype a "nickname".

Example:

```c
typedef char user[25];        	  // define a "nickname" called user that represents a char type variable with a length of
				  // 25 bytes

int main() {
	user user1 = "DarkblooM"; // same as: char user1[25] = "DarkblooM";

	return 0;
}
```

`typedef` can be used alongside structs:

```c
typedef struct {
	char name[25];
	char password[16];
	int id;
} User;				        // set the struct name at the end of the typedef

int main() {
	User user1 = {"DarkblooM", "password123", 69420};

	printf("%s\n", user1.name);     // -> DarkblooM
	printf("%s\n", user1.password); // -> password123
	printf("%d\n", user1.id);       // -> 69420

	return 0;
}
```

## Enums

An enum is a user defined type of named integer identifiers. It helps to make a program more readable.

Example:

```c
enum Day{Sun = 1, Mon = 2, Tue = 3, Wed = 4, Thu = 5, Fri = 6, Sat = 7};

int main() {
	enum Day today = Sun;

	printf("%d\n", today); // -> 1

	return 0;
}
```
