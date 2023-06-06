# Arithmetic operators

**+** (addition):
```c
int x = 5;
int y = 2;
int z = x + y;
printf("%d", z); // -> 7
```

**-** (substraction):
```c
int x = 5;
int y = 2;
int z = x - y;
printf("%d", z); // -> 3
```

**\*** (multiplication):
```c
int x = 5;
int y = 2;
int z = x * y;
printf("%d", z); // -> 10
```

**/** (division):
```c
int x = 5;
int y = 2;
float z = x / (float) y;
printf("%f", z); // -> 2.500000
```

**%** (modulus):
```c
int x = 5;
int y = 2;
float z = x % y;
printf("%d", z); // -> 1
```

**++** (increment):
```c
int x = 5;
x++;
printf("%d", x); // -> 6
```

**--** (decrement):
```c
int x = 5;
x--;
printf("%d", x); // -> 4
```

# Assignment using arithmetic operators

Used to replace a statement where an operator takes a variable as one of its arguments and then assigns the result back to the same variable.

Examples:
```c
int x = 10;
x += 2; // -> x = x + 2 -> 12
x -= 2; // -> x = x - 2 -> 8
x *= 2; // -> x = x * 2 -> 20
x /= 2; // -> x = x / 2 -> 5
x %= 2; // -> x = x % 2 -> 0
```
