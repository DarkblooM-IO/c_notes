# Logical operators

## AND operator

The AND logical operator (`&&`) checks if multiple conditions are true.

Example:

```c
float temp = 25;
bool sunny = false;

if (temp >= 0 && temp <= 30 && sunny) { // condition is true if temp >= 0 and temp <= 30 and sunny is true
	printf("The weather is good!\n");
}
else {
	printf("The weather is bad...\n");
}
```

## OR operator

The OR logical operator (`||`) checks if at least one condition is true.

Example:

```c
float temp = 25;

if (temp <= 0 || temp >= 30) { // condition is true if temp <= 0 or temp >= 30
	printf("The weather is bad!\n");
}
else {
	printf("The weather is bad...\n");
}
```

# NOT operator

The NOT logical operator (`!`) reverses the state of a condition.

Example:

```c
bool sunny = true;

if (sunny) {       // This statement will be true if sunny is true
	printf("It's sunny outside\n");
}
else if (!sunny) { // This statement will be true if sunny is false
	printf("It's cloudy outside");
}
```
