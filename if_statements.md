# If statements

An `if` statement runs the code it's given only if a condition is true.

Example:

```c
int main() {
    int age;

    printf("Enter your age: ");
    scanf("%d", &age);

    if (age >= 18) {
        printf("You are now signed up.");
    }
    else if (age < 0) {
        printf("You haven't been born yet.");
    }
    else {
        printf("You are too young to sign up.");
    }

    return 0;
}
```

## Switch statements

A `switch` statement is a more efficient alternative to `if` statements.

Example:
```c
char grade;

printf("Enter a letter grade: ");
scanf("%c", &grade);

// standard if statement
if (grade == 'A') {
	printf("Perfect!\n");
}
else if (grade == 'B') {
	printf("You did good!\n");
}
else {
	printf("That's not a valid grade.\n");
}

// switch statement
switch (grade) {
	case 'A':
		printf("Perfect!\n");
		break;
	case 'B':
		printf("You did good!\n");
		break;
	default:
		printf("That's not a valid grade.\n");
		break;
}
```
