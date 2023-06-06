# Format specifiers

**Format specifier** (%): defines and formats a type of data to be displayed.

Examples:
```c
float item = 5.75;

printf("Item 1: $%f\n", item);    // -> Item 1: $5.750000
printf("Item 1: $%.2f\n", item);  // -> Item 1: $5.75
printf("Item 1: $%8.2f\n", item); // -> Item 1:        $5.75
                                  // this is alligned right, to allign left, replace 8 with -8

```
