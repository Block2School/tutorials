# Arrays

Arrays are used to store collections of data of the same type. This tutorial introduces the concept of arrays in C++ and demonstrates how to declare, initialize, and use arrays. It's a fundamental concept for working with collections of data.

## It's your turn

Create a program that finds the sum of elements in an array. Declare an integer array numbers with values ({2, 4, 6, 8, 10}). Write a function calculateSum to compute the sum of the elements and then print the result.


Empty code : 
```cpp
#include <iostream>

// Declare the function prototype here

int main() {
    // Declare the integer array and assign values here

    // Call the function to calculate the sum

    return 0;
}

// Define the function here
```

Expected answer : 
```cpp
#include <iostream>

// Declare the function prototype here
int calculateSum(int arr[], int size);

int main() {
    // Declare the integer array and assign values here
    int numbers[] = {2, 4, 6, 8, 10};
    int size = sizeof(numbers) / sizeof(numbers[0]);

    // Call the function to calculate the sum
    int sum = calculateSum(numbers, size);

    // Print the result
    std::cout << "The sum of the elements is: " << sum << std::endl;

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