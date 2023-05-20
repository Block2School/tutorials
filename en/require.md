# Require

In the first exercise, we allowed users to create new birds by calling `createRandomBird` and entering their name. However, if users could continue calling this function indefinitely to create an infinite army of birds, the game wouldn't be very fun.

We want to ensure that each player can only call this function once. This way, new players will call it when they start the game to create the first bird for their army.

How can we ensure that this function is called only once per player?

To achieve this, we will use `require`. `require` will cause the function to stop and throw an error if certain conditions are not met:

```js
function sayHiToVitalik(string _name) public returns (string) {
  // Check if `_name` is equal to "Vitalik". Throw an error and exit if it's not the case.
  // (Note : Solidity doesn't have a native `string` comparator,
  // so we compare their keccak256 hashes to check if the `string` are equals)
  require(keccak256(_name) == keccak256("Vitalik"));
  // If it's true, we continue with the function:
  return "Hi!";
}
```


If you call the function with `sayHiToVitalik("Vitalik")`, it will return "Hi!". If you call it with any other argument, it will throw an error and not execute.

Therefore, `require` is useful for verifying that certain conditions are true before executing a function.

## It's your turn


In our bird game, we don't want a user to be able to create an infinite number of birds for their army by continuously calling `createRandomBird` - it wouldn't be very fun.

We will use `require` to ensure that the function is executed only once per user when they create their first bird.

1. Add a `require` statement at the beginning of `createRandomBird`. The function should check that `ownerBirdCount[msg.sender]` is equal to `0` and throw an error otherwise.

> *Note: In Solidity, the order of terms in a require statement doesn't matter - it's the same either way. However, our basic response checker only accepts one correct response, so `ownerBirdCount[msg.sender]` needs to be mentioned first.*