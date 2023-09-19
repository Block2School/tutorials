# Variables

Now that you know how to perform calculations with variables, you will learn about an important new keyword in variables: `let`.

## Let

`let` is a keyword used to define a variable. The difference from `const` is that a variable declared with `let` can be **modified after its definition**.

## Example

As mentioned in a previous tutorial, you can store a variety of things in variables, not just numbers. Here is a list of possible elements:

```js
let myText = "Hello!";
myText = "Hi!"; // The variable has been redefined, and its value is now "Hi!".
const myNumber = 0;
myNumber = 2; // !! Error because the variable is defined with "const" and not "let" !!
let myBool = true; // Boolean type, which can be either true or false.
let myNull = null; // Null represents no value. The variable is defined but contains nothing.
let myList = ["hello", 1, true, null, false]; // A list of different elements. Elements are separated by commas.
let myJson = {
    key: "value",
    number: 2,
}; // This is a JSON variable (JavaScript Object Notation), an object that contains values based on their keys. We'll cover this in more detail later.
```

Keep in mind that it is also possible to **retrieve a value that a function can return!**

## It's your turn

Create 6 different variables containing: `5, "Block2School!", false, null, -53, "This JavaScript tutorial is nice!"` and display them in the terminal in this order.