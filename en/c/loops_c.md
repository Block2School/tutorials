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

```c
#include <stdio.h>

int main() {
    // Declare the variable and assign a value here

    // Fill in the blank here to use a for loop to calculate and print the multiples

    return 0;
}
````

Expected answer : 
```c
#include <stdio.h>

int main() {
    // Declare the variable and assign a value here
    int baseNumber = 3;

    // Fill in the blank here to use a for loop to calculate and print the multiples
    for (int i = 1; i <= 5; i++) {
        printf("%d x %d = %d\n", baseNumber, i, baseNumber * i);
    }

    return 0;
}
```

