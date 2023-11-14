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

Create a JSON variable with this informations:
```js
myJson.number // Should be 3
myJson.otherNumb // Should be 9
myJson.a // Should be 25
myJson.b[0] // Should be 5
myJson.b[1] // Should be 8
myJson.b[2] // Should be 10
myJson.b2s.block // Should be Block
myJson.b2s.to // Should be TWO
myJson.b2s.School // Should be SCHool
myJson.b2s.values.n // Should be 120
myJson.b2s.values.a // Should be 894
myJson.b2s.values.z // Should be Ok
myJson.b2s.boolean // Should be false
myJson.texting // Should be Testing
myJson.entIre // Should be Block2School
```
And return this JSON variable.