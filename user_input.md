# User input

Prompt the user for imput:
```c
#include <stdio.h>
#include <string.h>

int main() {
    char name[25];
    int age; // create an empty variable

    printf("What is your name? ");
    fgets(name, 25, stdin); // variable to assign, max input size, input stream
    name[strlen(name)-1] = '\0'; // get rid of the trailing newline character
    printf("How old are you? ");
    scanf("%d", &age); // use the scanf function to ask the user for an input, using format
                       // specifiers to specify the type of data we want

    printf("Your name is %s.\n", name);
    printf("You are %d years old.\n", age); // print out the input embeded in a string
    
    return 0;
}
```

Note: the `scanf` function will read string inputs up until any whitespace character. To avoid this, use the `fgets` function instead.
