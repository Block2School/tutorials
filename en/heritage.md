# Inheritance

The code for our game is starting to become quite long. Instead of having a single, lengthy contract, it is often better to separate the logic of your code into multiple contracts to better organize it.

One of the features of Solidity that makes contracts easier to manage is `inherit`:

```js
contract Doge {
  function catchphrase() public returns (string) {
    return "So Wow CryptoDoge";
  }
}

contract BabyDoge is Doge {
  function anotherCatchphrase() public returns (string) {
    return "Such Moon BabyDoge";
  }
}
```

`BabyDoge` <font size="4">`inherits`</font> from `Doge`. This means that if you compile and deploy `BabyDoge`, it will have access to `catchphrase()` and `anotherCatchphrase()` (and any other public function we define in `Doge`).

This can be used for logical inheritances (like with subclasses, where a `Cat` is an `Animal`). But it can also be used simply to organize your code by grouping similar logic into different classes.

## It's your turn

In the next exercises, we will implement the features to feed and multiply our birds. Let's put this logic in its own class that inherits all the methods from `BirdFactory`.

1. Create a contract named BirdFeeding below BirdFactory. This contract should inherit from our BirdFactory contract.