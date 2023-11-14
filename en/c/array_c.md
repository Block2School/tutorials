# Arrays

Arrays in C allow you to store multiple elements of the same type. Here's an example:

```c
#include <stdio.h>

int main() {
    // Declare and initialize an array
    int myArray[5] = {1, 2, 3, 4, 5};

    // Access and print array elements
    for (int i = 0; i < 5; i++) {
        printf("%d ", myArray[i]);
    }

    printf("\n");

    return 0;
}
```

This example declares an array of integers, initializes it with values, and then uses a loop to print the elements.

## It's yourn turn

Create a program that finds the sum of elements in an array. Declare an integer array numbers with values ({2, 4, 6, 8, 10}). Write a function calculateSum to compute the sum of the elements and then print the result.

Empty code : 
```c
#include <stdio.h>

// Declare the function prototype here

int main() {
    // Declare the integer array and assign values here

    // Call the function to calculate the sum

    return 0;
}

// Define the function here
```

Exepected answer: 
```c
#include <stdio.h>

// Declare the function prototype here
int calculateSum(int arr[], int size);

int main() {
    // Declare the integer array and assign values here
    int numbers[] = {2, 4, 6, 8, 10};
    int size = sizeof(numbers) / sizeof(numbers[0]);

    // Call the function to calculate the sum
    int sum = calculateSum(numbers, size);

    // Print the result
    printf("The sum of the elements is: %d\n", sum);

    return 0;
}

// Define the function here
int calculateSum(int arr[], int size) {
    int sum = 0;
    for (int i = 0; i < size; i++) {
        sum += arr[i];
    }
    return sum;
}
```