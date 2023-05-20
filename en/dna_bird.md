# DNA Bird

We will finish writing the `feedAndMultiply` function.

The formula for calculating the DNA of a new bird is simple: it is just the average between the DNA of the feeding bird and the DNA of its prey.

For example:

```js
function testDnaSplicing() public {
  uint birdDna = 2222222222222222;
  uint targetDna = 4444444444444444;
  uint newBirdDna = (birdDna + targetDna) / 2;
  // ^ will be equal to 3333333333333333
}
```

Later on, we can implement a more complex formula, such as adding some randomness to the DNA of the new bird. But for now, let's keep it simple - we can always revisit it later.

## It's your turn

1. To start, we need to ensure that `_targetDna` is not longer than 16 digits. We can achieve this by setting `_targetDna` equal to `_targetDna % dnaModulus` to keep only the last 16 digits.
2. Next, our function needs to declare a `uint` called `newDna` and set it equal to the average of `myBird`'s DNA and `_targetDna` (as shown in the example above).

> *Note: You can access to properties of `myBird` using `myBird.name` and `myBird.dna`*

3. Once we have the new DNA, let's call `_createBird`. You can refer to the `birdfactory.sol` tab if you forgot the required arguments for calling this function. This function needs a name, so let's name our new bird `NoName` for now - we can write a function to change the names of birds later.

> *Note: For Solidity experts, you may have noticed an issue with our code! Don't worry, we will fix it in the next exercise.*