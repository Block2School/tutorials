## Input and Output

## It's your turn

Create a program that takes user input for their name and age and then prints a greeting with the provided information.

Empty code
```cpp
#include <iostream>
#include <string>

int main() {
    // Declare variables for name and age

    // Fill in the blank here to get user input for name and age

    // Fill in the blank here to print a greeting with the provided information

    return 0;
}
```

Expected answer: 
```cpp
#include <iostream>
#include <string>

int main() {
    // Declare variables for name and age
    std::string name;
    int age;

    // Fill in the blank here to get user input for name and age
    std::cout << "Enter your name: ";
    std::getline(std::cin, name);
    
    std::cout << "Enter your age: ";
    std::cin >> age;

    // Fill in the blank here to print a greeting with the provided information
    std::cout << "Hello, " << name << "! You are " << age << " years old." << std::endl;

    return 0;
}
```
