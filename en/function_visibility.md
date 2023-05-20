# More visibility on functions

**The code in our previous exercise had an error!**

If you try to compile it, the compiler will throw an error.

The problem is that we are trying to call the function `_createBird` inside `BirdFeeding`, but `_createBird` is a `private` function in `BirdFactory`. This means that no contract inheriting from `BirdFactory` can access it.

## Internal and external

In addition to `public` and `private`, Solidity has two other visibility modifiers for functions: `internal` and `external`.

`internal` is similar to `private`, except that it is also accessible to contracts that inherit from the current contract. (This seems to be what we want!)

`external` is similar to `public`, except that these functions can ONLY be called from outside the contract - they cannot be called by other functions within the contract. We will explain later why to use `external` instead of `public`.

To declare functions as `internal` or `external`, the syntax is the same as for `private` and `public`:

```js
contract Sandwich {
  uint private sandwichesEaten = 0;

  function eat() internal {
    sandwichesEaten++;
  }
}

contract BLT is Sandwich {
  uint private baconSandwichesEaten = 0;

  function eatWithBacon() public returns (string) {
    baconSandwichesEaten++;
    // We can call this function because it is `internal`
    eat();
  }
}
```

## It's your turn

1. Change `_createBird()` from `private` to `internal` so that other contracts can access it.