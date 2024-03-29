# Structures

Structures in C allow you to group different types of data under a single name. Here's an example:

```c
#include <stdio.h>

// Define a structure
struct Student {
    char name[50];
    int age;
    float gpa;
};

int main() {
    // Declare a variable of type struct Student
    struct Student student1;

    // Assign values to the structure members
    strcpy(student1.name, "John Doe");
    student1.age = 20;
    student1.gpa = 3.5;

    // Print the information
    printf("Name: %s\n", student1.name);
    printf("Age: %d\n", student1.age);
    printf("GPA: %.2f\n", student1.gpa);

    return 0;
}
```

In this example, a structure Student is defined with members name, age, and gpa. An instance of the structure is then declared and initialized.


## It's your turn

Create a program that uses a structure to represent a person. Declare a structure Person with members name and age. Write a function printPersonInfo to print the information of a person, and then use this structure to represent and print information for two different people.

Expected output : 
Name: Alice, Age: 25
Name: Bob, Age: 30