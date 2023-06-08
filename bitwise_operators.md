# Bitwise operators

Bitwise operators are special operators used in bit level programming.

Here are the five main operators:

```
&     AND
|     OR
^     XOR
<<    left shift
>>    right shift
```

Example:

```c
int x = 6;         // 6 = 00000110
int y = 12;        // 12 = 00001100
int z = 0;         // 0 = 00000000

z = x & y;         // x 0|0|0|0|0|1|1|0
		   // y 0|0|0|0|1|1|0|0
		   // z 0|0|0|0|0|1|0|0
printf("%d\n", z); // -> 4

z = x | y;         // x 0|0|0|0|0|1|1|0
		   // y 0|0|0|0|1|1|0|0
		   // z 0|0|0|0|1|1|1|0
printf("%d\n", z); // -> 14

z = x ^ y;         // x 0|0|0|0|0|1|1|0
		   // y 0|0|0|0|1|1|0|0
		   // z 0|0|0|0|1|0|1|0
printf("%d\n", z); // -> 10

z = x << 1;        // x 0|0|0|0|0|1|1|0
		   // z 0|0|0|0|1|1|0|0
printf("%d\n", z); // -> 12

z = x >> 1;        // x 0|0|0|0|0|1|1|0
		   // z 0|0|0|0|0|0|1|1
printf("%d\n", z); // -> 3
```
