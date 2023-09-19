# Conditions

You have gained a solid understanding of variables. Now, let's explore conditions.

## How to Create a Condition

A condition is written like this:

```js
if (true) { // "if" is the keyword; within parentheses, you must place a condition that always returns a boolean.
    console.log("true");
} else if (false) {
    console.log("false");
} else {
    console.log("other");
}
```

If the condition within the first set of parentheses is not met, we move to the `else if`, which checks another condition. If no condition is met, we fall into the `else` block. You are not obligated to have both `else if` and `else`. Only the `if` is mandatory for a condition. You can also have as many `else if` as you like.

## Example

Here's a real example of a condition:
```js
const myCond = (value1, value2) => {
    if (value1 < value2) { // If value1 is less than value2
        return true;
    } else if (value1 > value2) { // If value1 is greater than value2
        return false;
    } else {
        return null;
    }
};
myCond(3, 4); // Returns true
myCond(8, 2); // Returns false
myCond(3, 3); // Returns null
```

In functions, when you trigger a return, the function immediately stops and returns the value (or no value if you don't want to return anything).

```js
const myFunction = (param) => {
    if (param == 1) {
        return true;
    }
    console.log("Pass");
    return;
};
console.log(myFunction(1)); // Displays true
console.log(myFunction(2)); // Displays Pass and then undefined because nothing is returned.
```

## Logical Operators

Here are the possible logical operators within a condition:

### Standard Operators

- `==` Strict equality between two values. `1 == 1` returns true, `1 == 2` returns false.
- `!=` Not equal to. `1 != 1` returns false, `1 != 2` returns true.
- `<` Less than. `1 < 2` returns true, `2 < 1` returns false, `1 < 1` returns false.
- `>` Greater than. `1 > 2` returns false, `2 > 1` returns true, `1 > 1` returns false.
- `<=` Less than or equal to. `1 <= 2` returns true, `2 <= 1` returns false, `1 <= 1` returns true.
- `>=` Greater than or equal to. `1 >= 2` returns false, `2 >= 1` returns true, `1 >= 1` returns true.

### Special Cases

If you have a variable with a number or a boolean (`true` or `false`), you can use these two logical operators:

```js
const num1 = 1;
const num2 = 0;
const num3 = 150;
const bTrue = true;
const bFalse = false;
const bNull = null;

if (num1) { // Check if num1 is true or different from 0 for a number. This condition is met.
    console.log("num1");
}
if (num2) { // num2 = 0, so we don't enter this condition.
    console.log("num2");
}
if (num3) { // num3 != 0, so we enter this condition.
    console.log("num3")
}
if (bTrue) { // bTrue is true, so the condition is met.
    console.log("true");
}
if (!bTrue) { // The "!" operator inverts the condition. So, we're checking if bTrue is false. It's not, so we don't enter this condition.
    console.log("bTrue not");
}
if (!bFalse) { // bFalse is false, so we enter this condition because of the "!" operator.
    console.log("false");
}
if (!bNull) { // bNull is null, but "!" can also check if a variable is null or undefined. It's the case here, so the condition is met.
    console.log("null");
}
```

## Returning with a Condition

You can use a condition to return a value like this:
```js
const i = 10;
const y = 5;
return i < y; // Returns false
```

## Multiple Conditions

You can make multiple conditions that must all be met for the `if` statement to execute. Here's an example:
```js
const i = 10;
const y = 5;
const z = 18;
if ((i > y && y == 5) || z > 40) { // If i > y AND y == 5 are both true OR if z is greater than 40, then we display "Ok."
    console.log("Ok");
}
```

- `||` **OR**
- `&&` **AND**

As you saw, it's possible to use parentheses to group conditions for multiple conditions or for a single one.

## It's your turn

You need to create several conditions:
- `toggleBoolean(boolean)` that takes a boolean as a parameter. The function should return `true` if the parameter is `false`, otherwise, it should return `true`.
- `greatestValue(number, number)` that takes 2 number parameters. The function should return the largest number among the two parameters.
- `checkEqual(number, number, boolean)` that takes 2 number parameters and one boolean parameter. The function should return true if the boolean is true **or** if the two number parameters are equal.