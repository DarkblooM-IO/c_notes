# String functions

Note: make sure to include the `<string.h>` library.

```c
char str1[] = "Hello";
char str2[] = "World";

strlwr(str1);           // converts a string to lowercase
			// -> hello
strupr(str1);           // converts a string to uppercase
			// -> HELLO
strcat(str1, str2);     // appends str2 to the end of str1
			// -> HelloWorld
strncat(str1, str2, 1); // appends n characters from str2 to the end of str1
			// -> HelloW
strcpy(str1, str2);     // copies str2 to str1
			// -> World
strncpy(str1, str2, 4); // copies n characters of str2 to str1
			// -> Worlo

strset(str1, '?');      // sets all characters of a string to a given character
			// -> ?????
strnset(str1, 'x', 1);  // sets first n characters of a string to a given character
			// -> xello
strrev(str1);           // reverses a string
			// -> olleH

strlen(str1);           // returns the length of a string as an int
			// -> 5
strcmp(str1, str2);     // returns 0 if two strings are equal, else returns a positive or negative
			// value depending on the first non-matching characters in both strings
			// -> -15
strncmp(str1, str2, 1); // same as strcmp but with a substring of length n
			// -> -15
```
