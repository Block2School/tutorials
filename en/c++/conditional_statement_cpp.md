# Conditional Statement

Conditional statements, such as if, else if, and else, allow you to make decisions in your program based on certain conditions. This tutorial explores how to use conditional statements to control the flow of your program, making it more flexible and responsive.

## It's your turn

Create a program that checks whether a given number is positive, negative, or zero. Declare a variable num and assign it a value. Use an if-else statement to check the number and print the result.

Empty code: 
```cpp
#include <iostream>

int main() {
    int num = -5;

    // Fill in the blank here to check if the number is positive, negative, or zero
    // Hint: Use an if-else statement

    // Fill in the blank here to print the result

    return 0;
}
```

Expectec output : 
-5 is negative.


Expected answer : 

```cpp
#include <iostream>

int main() {
    // Declare the variable and assign a value here
    int num = -5;

    // Fill in the blank here to check if the number is positive, negative, or zero
    // Hint: Use an if-else statement
    if (num > 0) {
        std::cout << num << " is positive." << std::endl;
    } else if (num < 0) {
        std::cout << num << " is negative." << std::endl;
    } else {
        std::cout << num << " is zero." << std::endl;
    }

    return 0;
}
```
