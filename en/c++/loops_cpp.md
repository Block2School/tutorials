# Loops

Loops are used to execute a block of code repeatedly. This tutorial covers the for loop, a common type of loop in C++. It demonstrates how to use a loop to perform iterative tasks, such as printing multiples of a number.

## It's your turn

Create a program that prints the first 5 multiples of a given number. Declare a variable baseNumber and assign it a value. Use a for loop to calculate and print the multiples.

Empty code :
```cpp
#include <iostream>

int main() {
    // Declare the variable and assign a value here

    // Fill in the blank here to use a for loop to calculate and print the multiples

    return 0;
}
```

Expected answer : 
```cpp
#include <iostream>

int main() {
    // Declare the variable and assign a value here
    int baseNumber = 3;

    // Fill in the blank here to use a for loop to calculate and print the multiples
    for (int i = 1; i <= 5; i++) {
        std::cout << baseNumber << " x " << i << " = " << baseNumber * i << std::endl;
    }

    return 0;
}
```