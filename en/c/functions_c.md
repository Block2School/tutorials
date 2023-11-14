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

Empty code : 
```c
#include <stdio.h>

// Declare the function prototype here

int main() {
    // Declare the variable and assign a value here

    // Call the function to calculate the factorial

    return 0;
}

// Define the function here
```

Expected answer : 
```c
#include <stdio.h>

// Declare the function prototype here
int calculateFactorial(int n);

int main() {
    // Declare the variable and assign a value here
    int num = 5;

    // Call the function to calculate the factorial
    int result = calculateFactorial(num);

    // Print the result
    printf("The factorial of %d is: %d\n", num, result);

    return 0;
}

// Define the function here
int calculateFactorial(int n) {
    if (n == 0 || n == 1) {
        return 1;
    } else {
        return n * calculateFactorial(n - 1);
    }
}
````

