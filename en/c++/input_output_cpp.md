# Input and Output

Input and output operations are crucial for creating interactive programs. This tutorial demonstrates how to take user input using cin and how to display information to the user using cout. It sets the foundation for building programs that interact with the user.

## Getline

The getline function is used in C++ to read a line of text from the input stream (usually the standard input, cin) and stores it in a string. It allows you to read an entire line, including spaces, until a newline character ('\n') is encountered. This function is particularly useful when you want to read input that may contain spaces.

Example : 
```cpp
#include <iostream>
#include <string>

int main() {
    std::string myString;
    std::getline(std::cin, myString);
    std::cout << "You entered: " << myString << std::endl;
    return 0;
}
```
## Cin

cin is an instance of the input stream class in C++, and it is used for standard input. It is commonly used with the extraction operator (>>) to read various types of data from the user or another input source.
```cpp
#include <iostream>

int main() {
    int myNumber;
    std::cout << "Enter a number: ";
    std::cin >> myNumber;
    std::cout << "You entered: " << myNumber << std::endl;
    return 0;
}
```



## It's your turn

Create a program that takes user input for their name and age and then prints a greeting with the provided information.