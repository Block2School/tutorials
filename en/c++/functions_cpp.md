# Functions

Functions allow you to break down your program into smaller, manageable pieces. This tutorial explains how to declare, define, and call functions in C++. It emphasizes the importance of functions in organizing and structuring code.

## It's your turn

Create a program that calculates the factorial of a given number. Declare a variable num and assign it a value. Write a function calculateFactorial to compute the factorial and then print the result.

Empty code:

```cpp
#include <iostream>

int calculateFactorial(int n);

int main() {
     int num = 5;

    // Call the function to calculate the factorial

    std::cout << "The factorial of " << num << " is: " << result << std::endl;
    return 0;
}

int calculateFactorial(int n) {
    if (n == 0 || n == 1) {
        return 1;
    } else {
        return n * calculateFactorial(n - 1);
    }
}
```

Expected output: The factorial of 5 is: 120


Expected answer :
```cpp
#include <iostream>

// Declare the function prototype here
int calculateFactorial(int n);

int main() {
    // Declare the variable and assign a value here
    int num = 5;

    // Call the function to calculate the factorial
    int result = calculateFactorial(num);

    // Print the result
    std::cout << "The factorial of " << num << " is: " << result << std::endl;

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
```
