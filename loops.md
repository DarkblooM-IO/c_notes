# Loops

Loops are a way to repeat code multiple times without copying it.

## FOR loop

A `for` loop repeats a section of code a limited amount of times.

Example:

```c
// we declare a variable i and set it to 1, the loop will then continue as long as the condition in the middle is true, in this case i <= 10, and the statement at the end will be executed at the end of each loop, in this case incrementing i by 1
for (int i = 1; i <= 10; i++) {
	printf("loop %d\n", i); // -> loop 1
							// -> loop 2
							// -> loop 3
							// -> loop 4
							// -> loop 5
							// -> loop 6
							// -> loop 7
							// -> loop 8
							// -> loop 9
							// -> loop 10
}
```

## WHILE loop

### Standard `while`

A `while` loop repeats a section of code as long as a condition is true.

Example:

```c
char name[25];

printf("What is your name? ");
fgets(name, 25, stdin);
name[strlen(name) - 1] = '\0';

while (strlen(name) == 0) { // the loop will continue as long as the user hasn't given
							// an answer
	printf("You did not enter your name.\n");
	printf("What is your name? ");
	fgets(name, 25, stdin);
	name[strlen(name) - 1] = '\0';
}
```

### `do while`

A `do while` loop is like a `while` loop, except it executes the code inside of it *before* checking the condition.

Example:

```c
int n = 0;
int sum;

do {
	printf("Enter a number above 0: ");
	scanf("%d", &n);
	if (n > 0) {
		sum += n;
	}
} while (n > 0); // the code above will run once, then check the condition and continue
				 // running if it is true
```

## `break` and `continue`

The `continue` statement skips the rest of the code and forces the next iteration of the loop.
The `break` statement exits the loop (or the `switch`).

Example:

```c
for (int i = 1; i <= 20; i++) {
	if (i == 13) { // skip this iteration if i == 13
		continue;
	}
	printf("%d\n", i); // -> 1
					   // -> 2
					   // -> 3
					   // -> 4
					   // -> 5
					   // -> 6
					   // -> 7
					   // -> 8
					   // -> 9
					   // -> 10
					   // -> 11
					   // -> 12
					   // -> 14
					   // -> 15
					   // -> 16
					   // -> 17
					   // -> 18
					   // -> 19
					   // -> 20
}

for (int i = 1; i <= 20; i++) {
	if (i == 13) { // exit the loop if i == 13
		break;
	}
	printf("%d\n", i); // -> 1
					   // -> 2
					   // -> 3
					   // -> 4
					   // -> 5
					   // -> 6
					   // -> 7
					   // -> 8
					   // -> 9
					   // -> 10
					   // -> 11
					   // -> 12
}
```