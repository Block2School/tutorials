# Pointers

Pointers in C store memory addresses. They provide a way to work with memory directly. Here's a simple example:

```c
#include <stdio.h>

int main() {
    int number = 42;

    // Declare a pointer and assign the address of the variable
    int *ptr = &number;

    // Print the value and address using the pointer
    printf("Value: %d\n", *ptr);
    printf("Address: %p\n", (void *)ptr);

    return 0;
}
```


## It's yourn turn

Create a program that uses pointers to swap the values of two integers. Declare two variables, a and b, and assign them values (a = 5, b = 10). Write a function swapValues that takes pointers as parameters to swap the values, and then print the values before and after the swap.

Empty code: 
```c
#include <stdio.h>

void swapValues(int *x, int *y);

int main() {
    int a = 5;
    int b = 10;

    printf("Before Swap: a = %d, b = %d\n", a, b);

    // Call the function to swap values

    printf("After Swap: a = %d, b = %d\n", a, b);

    return 0;
}

void swapValues(int *x, int *y) {
  // Write your code here
}
```


Expected output: 
Before Swap: a = 5, b = 10
After Swap: a = 10, b = 5

Expected answer :

```c
#include <stdio.h>

// Declare the function prototype here
void swapValues(int *x, int *y);

int main() {
    // Declare the variables and assign values here
    int a = 5;
    int b = 10;

    // Print values before the swap
    printf("Before Swap: a = %d, b = %d\n", a, b);

    // Call the function to swap values
    swapValues(&a, &b);

    // Print values after the swap
    printf("After Swap: a = %d, b = %d\n", a, b);

    return 0;
}

// Define the function here
void swapValues(int *x, int *y) {
    int temp = *x;
    *x = *y;
    *y = temp;
}
```