# Functions

Functions in C are essential for organizing code. They allow you to group related code together. Here's an example:

```c
#include <stdio.h>

// Declare a function prototype
void myFunction();

int main() {
    // Call the function
    myFunction();

    return 0;
}

// Define the function
void myFunction() {
    printf("This is my function!\n");
}
```

In this example, **myFunction** is declared with a prototype before **main**, and then it is defined after main. The function is then called from main.

## It's your turn

Create a program that calculates the factorial of a given number. Declare a variable num and assign it a value (num = 5). Write a function calculateFactorial to compute the factorial and then print the result.

Expected output: 
The factorial of 5 is: 120

