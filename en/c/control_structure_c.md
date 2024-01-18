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


Expected output: 
7 is odd
