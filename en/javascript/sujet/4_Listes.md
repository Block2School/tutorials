# Lists

In this tutorial, we will delve deeper into list variables.

## Playing with list variables

List variables have functions defined for them to manipulate them. Here's an example:

```js
const listVar = []; // You can define the list variable as const, and it won't affect the execution of functions
listVar.push("Test"); // Adds an element to the list
listVar.push("Ok");
listVar.push("B2S");
listVar.pop(); // Removes the last element from the list, which is "B2S" here. You can retrieve the value in a variable
console.log(listVar.length); // Displays the length of the list, which is 2 here
listVar.shift(); // Removes the first element from the list, which is "Test" here. You can retrieve the value in a variable
listVar.push("New");
console.log(listVar[0]); // Displays the element at index 0 (indexes always start at 0), which is the first element of the list, "Ok" here
const str = listVar.join(" "); // All elements of the list are put into a text variable, and the elements are separated by a space " ".
```

There are many other methods that we will explore in more advanced tutorials later!

## It's your turn!

Complete every functions.