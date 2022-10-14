# Return Value on function

To return a value from a function, the declaration looks like this:

```solidity
string greeting = "Hello Gabriel";

function sayHello() public returns (string memory) {
  return greeting;
}
```

In Solidity, the function declaration contains the type of the return value (in this case `string`).

## **Function modifiers**

The above function doesn't actually change state in Solidity — e.g. it doesn't change any values or write anything.

So in this case we could declare it as a ***view*** function, meaning it's only viewing the data but not modifying it:

```solidity
function _multiply(uint a, uint b) private pure returns (uint) {
  return a * b;
}
```

This function doesn't even read from the state of the app — its return value depends only on its function parameters. So in this case we would declare the function as ***pure***.

# Exercise

---

We're going to want a helper function that generates a random Student Id number from a string.

1. Create a `private` function called `_generateRandomStudentId`. It will take one parameter named `_str` (a `string`), and return a `uint`. Don't forget to set the data location of the `_str` parameter to `memory`.
2. This function will view some of our contract's variables but not modify them, so mark it as `view`.
3. The function body should be empty at this point — we'll fill it in later.