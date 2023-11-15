C supports various operators for performing operations on variables. Here's a simple example using arithmetic operators:

```c
#include <stdio.h>

int main() {
    int num1 = 10;
    int num2 = 5;

    // Perform addition, subtraction, multiplication, and division
    int sum = num1 + num2;
    int difference = num1 - num2;
    int product = num1 * num2;
    int quotient = num1 / num2;

    // Print the results
    printf("Sum: %d\n", sum);
    printf("Difference: %d\n", difference);
    printf("Product: %d\n", product);
    printf("Quotient: %d\n", quotient);

    return 0;
}
```

This example demonstrates the use of basic arithmetic operators (+, -, *, /) in C.

## It's your turn

Create a program that calculates the area of a rectangle. Declare two variables, **length** and **width**, assign them values (length = 5, width = 8), and then calculate and print the area.

Empty code : 
```c
#include <stdio.h>

int main() {
    // Declare variables and assign values here

    // Fill in the blank here to calculate the area (Reminder: AREA = LENGHT*WIDTH)

    printf("The area of the rectangle is: %d\n", area);

    return 0;
}
````

Expected answer : 
```c
#include <stdio.h>

int main() {
    // Declare variables and assign values here
    int length = 5;
    int width = 8;

    // Fill in the blank here to calculate the area
    int area = length * width;

    // Fill in the blank here to print the area
    printf("The area of the rectangle is: %d\n", area);

    return 0;
}
```