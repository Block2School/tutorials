# JSON

Let's now dive into JSON variables.

## Definition

A JSON looks like a list, but it **uses keys instead of indexes**, as we saw with lists in the previous tutorial.  
An element looks like this: `key: value`, and they are also separated by commas.

Here's an example of a JSON variable:

```js
const myJson = {
    test: "Hi",
    b2s: { // You can define another JSON within a JSON key.
        block: "Block",
        to: 2,
        school: "School",
    },
    list: [ // You can also define lists within a JSON key.
        1,
        "elem",
        5,
        -1,
        "true",
        true,
    ],
    boolean: true
};
console.log(myJson.test); // Will display the value of the key "test," which is "Hi" here.
console.log(myJson.b2s.block); // Will display "Block".
myJson.b2s.to = 3; // Changes the value of the key "to" in the JSON contained by the key "b2s" to 3.
```

Note that lists can also contain JSON values and other list values like this:

```js
const list = [
    {
        hello: "World"
    },
    [
        1,
        2,
        3,
    ],
] // This list is valid
```

But we won't go into that in this tutorial.

## Additional notes on console.log

You can directly perform actions like these within console.log:

```js
const num1 = 5;
const num2 = 10;
console.log(num1 + num2); // Will display "15"
console.log("B2S", num1); // Will display "B2S 5"
console.log("B2S" + num1); // Will display "B2S5"
console.log("test", num2, "OK"); // Will display "test 10 OK"
```

## It's your turn

You have a JSON variable defined; it's your turn to display the following operations:
- Display the result of `3 + 9`
- Display `Block TWO TestingOk`
- Display `falseBlock2School 919 200` (919 is obtained by doing `894 + 25`, and 200 is obtained by doing `25 * 8`)
- Display `SCHoolTWOBlock Block2School120 12` (12 is obtained by doing `3 + 9`)