# Loops

Loops in C, such as for and while, are used to repeat a block of code. Here's an example using a for loop:

```c
#include <stdio.h>

int main() {
    // Use a for loop to print numbers from 1 to 5
    for (int i = 1; i <= 5; i++) {
        printf("%d ", i);
    }

    printf("\n");

    return 0;
}
```

## It's your turn 

Create a program that prints the first 5 multiples of a given number. Declare a variable baseNumber and assign it a value (baseNumber = 3). Use a for loop to calculate and print the multiples.

Expected output: 
3 x 1 = 3
3 x 2 = 6
3 x 3 = 9
3 x 4 = 12
3 x 5 = 15
