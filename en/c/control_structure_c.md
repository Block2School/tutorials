## Control Structure

C provides control structures like if, else if, and else for decision-making. Here's an example:

````c
#include <stdio.h>

int main() {
    int number = 10;

    // Use if-else statements to make decisions
    if (number > 0) {
        printf("The number is positive.\n");
    } else if (number < 0) {
        printf("The number is negative.\n");
    } else {
        printf("The number is zero.\n");
    }

    return 0;
}
````

This example checks whether a given number is positive, negative, or zero using if-else statements.

## It's your turn 

Create a program that determines if a given number is even or odd. Declare a variable myNumber and assign it a value (myNumber = 7). Use an if-else statement to check if the number is even or odd and print the result.

Empty code : 
```c
#include <stdio.h>

int main() {
    int myNumber = 7;

    // Fill in the blank here to check if the number is even or odd
    // Hint: Use an if-else statement

    // Fill in the blank here to print the result

    return 0;
}
```

Expected output: 
7 is odd

Expected answer : 

```c
#include <stdio.h>

int main() {
    // Declare the variable and assign a value here
    int myNumber = 7;

    // Fill in the blank here to check if the number is even or odd
    // Hint: Use an if-else statement
    if (myNumber % 2 == 0) {
        printf("%d is even.\n", myNumber);
    } else {
        printf("%d is odd.\n", myNumber);
    }

    return 0;
}
```