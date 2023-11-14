# Functions

Create a program that calculates the factorial of a given number. Declare a variable num and assign it a value. Write a function calculateFactorial to compute the factorial and then print the result.

Empty code:

```cpp
#include <iostream>

// Declare the function prototype here

int main() {
    // Declare the variable and assign a value here

    // Call the function to calculate the factorial

    return 0;
}

// Define the function here
```

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
