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


Expected output: 
Before Swap: a = 5, b = 10
After Swap: a = 10, b = 5