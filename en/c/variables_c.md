# Variables

In C, variables must be declared before use. The type of the variable must also be specified. Here's an example:

```c
// Declare a variable of type int
int number;
// Assign a value to the variable
number = 42;
```

Here is differents type you can find in C : 

- char : Character type, typically one byte. \
```char myChar = 'A'; ```
- char* : string literal. It's often used with dynamic memory location fucntions like malloc (you will discover that on the next tutoriel) \
```char myChar = 'A'; ```
- int : Integer type. \
```int myInt = 42; ```

## It's your turn

Declare an integer variable named myNumber, assign it a value of 25, and print the value to the console.

Empty code :
```c
#include <stdio.h>

int main() {
    // Declare the variable and assign a value here

    // Fill in the blank here to print the value

    return 0;
}
```

Expected answer : 
```c
#include <stdio.h>

int main() {
    // Declare the variable and assign a value here
    int myNumber = 25;

    // Fill in the blank here to print the value
    printf("The value of myNumber is: %d\n", myNumber);

    return 0;
}
```

