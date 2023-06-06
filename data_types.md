# Data types

Different data types can be attributed to variables:

```c
char a = 'C';                                    // single character / %c
char b[x] = "DarkblooM";                         // string of characters / %s
                                                 // x is the max size of the array in bytes


float c = 3.141592;                              // 4 bytes (32 bits of precision) 6 - 7 digits / %f
double d = 3.141592653589793;                    // 8 bytes (64 bits of precision) 15 - 16 digits / %lf


bool e = true;                                   // 1 byte (true or false) / %d (treated as integers, 1 being true and 0 being
						 // false)
                                                 // booleans require the <stdbool.h> library to be included


char f = 100;                                    // 1 byte (-128 to +127) / %d or %c
unsigned char g = 255;                           // 1 byte (0 to +255) / %d or %c


short h = 32767;                                 // 2 bytes (-32,768 to +32,767) / %d
unsigned short i = 65535;                        // 2 bytes (0 to +65,535) / %d


int j = 2147483647;                              // 4 bytes (-2,147,483,648 to +2,147,483,647) / %d
unsigned int k = 4294967295;                     // 4 bytes (0 to +4,294,967,295) / %u


long long int l = 9223372036854775807;           // 8 bytes (-9 quintillion to +9 quintillions) / %lld
unsigned long long int m = 18446744073709551615; // 8 bytes (0 to +18 quintillions) / %llu
```

Data types formatting:
```c
// floats
printf("%f\n", c);      // -> 3.141592
printf("%lf\n", c);     // -> 3.141592

printf("%0.15f\n", d);  // -> 3.141592741012573
printf("%0.15lf\n", d); // -> 3.141592653589793


// booleans
printf("%d\n", e);      // -> 1


// numeric chars
printf("%d\n", f)       // -> 100
printf("%c\n", f)       // -> d

printf("%d\n", g);      // -> 255


// shorts
printf("%d\n", h);      // -> 32767
printf("%d\n", i);      // -> 65535


// integers
printf("%d\n", j);      // -> 2147483647
printf("%u\n", k);      // -> 4294967295


// long long integers
printf("%lld\n", l);    // -> 9223372036854775807
printf("%llu\n", m);    // -> 18446744073709551615
                        // [WARNING] integer constant size
                        //    -> add U to end of value at var initialization
```

## Format specifiers

**Format specifier** (%): defines and formats a type of data to be displayed.

Examples:
```c
float item = 5.75;

printf("Item 1: $%f\n", item);    // -> Item 1: $5.750000
printf("Item 1: $%.2f\n", item);  // -> Item 1: $5.75
printf("Item 1: $%8.2f\n", item); // -> Item 1:        $5.75
                                  // this is alligned right, to allign left, replace 8 with -8

```

## Arrays

An array is a data structure that can store many values of  the same data type.

Example:

```c
double prices[5] = {5.0, 10.0, 15.0, 20.0, 25.0}; // we use [x] to turn the variable into an array (x being the optional maximum
						  // size of the array) and we put all of our values inside {}

printf("$%.2lf", prices[0]);                      // -> $5.00
```

Note: a string is essentially an array of characters.
```c
char name[] = "DarkblooM";
```

### 2D arrays

A two-dimensional array is an array in which each value is itself an array.

Example:

```c
int n[2][3] = {{1, 2, 3}, {4, 5, 6}}; // we specify an array of arrays with [x][y] (y being mandatory this time and defining the
				      // size of each sub-arrays)

// an easier way to visualize a 2D array is declaring it like this:
int n[2][3] = {
		{1, 2, 3},
		{4, 5, 6}
	      };

// you can also declare the array first and then assign values to it individually
int n[2][3];
n[0][0] = 1; // we specify the x and y coordinates using [x][y]
n[0][1] = 2;
n[0][2] = 3;
n[1][0] = 4;
n[1][1] = 5;
n[1][2] = 6;
```

Like previously seen, since strings are array of characters, making an array of strings implies that we make a 2D array.

Example:

```c
char cars[][] = {"Mustang", "Corvette", "Camaro"};

// here's how to change one of the strings from an array:
strcpy(cars[0], "Tesla");
// note that this requires the <string.h> library
```

## Structs

A struct is a collection of related members ("variables") listed under one name in a block of memory.
They are similar to classes in other programming languages but behave a bit differently.

Example:

```c
struct Players {
	char name[];
	int score;
}

int main() {
	struct Player player1;
	struct Player player2;

	strcpy(player1.name, "DarkblooM"); // access a member's value by using the struct name followed by a dot then its own name
	player1.score = 4;

	strcpy(player2.name, "BrightblooM");
	player2.score = 5;

	printf("%s\n", player1.name);      // -> DarkblooM
	printf("%d\n", player1.score);     // -> 4

	printf("%s\n", player2.name);      // -> BrightblooM
	printf("%d\n", player2.score);     // -> 5

	return 0;
}
```
