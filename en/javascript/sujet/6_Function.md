# Function

Let's now move on to functions. Up until now, you haven't created any functions.

## Creating a function

A function can be defined as follows:
```js
const myFunction = () => { // We define a variable myFunction that holds: () => {}, a function

};
myFunction(); // An action that calls the myFunction function
```

It's important to know that if you want to immediately execute an anonymous function in your code, you can do it like this:
```js
(() => {

})(); // We define an anonymous function within parentheses, and then we use () at the end to call it immediately.
```

## Parameters

You can pass variables to a function; this is called parameters. Here's how to do it:

```js
const myFunction = (param1, param2) => {
    console.log(param1); // Displays the value of param1
    console.log(param2); // Displays the value of param2
};
myFunction(10, "Test"); // We call the function by defining its parameters. param1 is set to 10, and param2 is set to "Test"
```

## Return

You can return values at the end of a function. This helps break down your code into smaller parts for better organization.

```js
const increment = (value) => {
    return value + 1 // Adds 1 to the value of the parameter
};
const nb1 = 10;
const nb2 = increment(nb1); // nb2 receives the value specified after the return.
console.log(nb2); // Displays 11
```

## It's your turn

Create the `divide` function that takes a number and a divisor as parameters. Divide the number by the divisor and return the result.