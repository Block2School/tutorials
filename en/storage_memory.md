# Storage vs memory

In Solidity, there are two places to store variables - in `storage` or in `memory`.

`Storage` is used for variables that are permanently stored in the blockchain. `Memory` variables are temporary and are cleared between external function calls to your contract. It's similar to the hard disk and RAM of your computer.

Most of the time, you won't need to use these keywords because Solidity handles it automatically. State variables (declared outside functions) are by default in `storage` and written permanently to the blockchain, while variables declared inside functions are in `memory` and disappear when the function call is completed.

However, there may be cases where you need to use these keywords, especially when using `structures` and `arrays` inside functions :

```js
contract SandwichFactory {
    struct Sandwich {
        string name;
        string status;
    }

    Sandwich[] sandwiches;

    function eatSandwich(uint _index) public {
        // Sandwich mySandwich = sandwiches[_index];

        // ^ It may seem simple, but Solidity will return a warning
        // indicating that you should explicitly declare `storage` or `memory` here.

        // You should declare the keyword `storage`, like this :
        Sandwich storage mySandwich = sandwiches[_index];
        // ...in this case, `mySandwich` is a pointer to `sandwiches[_index]`
        // in the storage and...
        mySandwich.status = "Eaten!";
        // ... changes definitively `sandwiches[_index]` on the blockchain.

        // If you just want a copy, you can use `memory`:
        Sandwich memory anotherSandwich = sandwiches[_index + 1];
        // ...in this case, `anotherSandwich` will be a copy of
        // datas inside the memory and...
        anotherSandwich.status = "Eaten!";
        // ... changes the temporary variable and will not have any
        // effect on `sandwiches[_index + 1]`. But you can do that :
        sandwiches[_index + 1] = anotherSandwich;
        // ...if you want to copy the editions in the storage of the blockchain.
    }
}
```

Don't worry if you don't fully understand when to use one or the other for now. Throughout the tutorial, we will guide you on when to use `storage` and when to use `memory`, and the Solidity compiler will also provide warnings to indicate when you should use one of these keywords.

For now, just remember that there will be cases where you will need to use `storage` and `memory`!

## It's your turn

It's time to give our birds the ability to feed and multiply!

When a bird feeds on another life form, its DNA combines with the other life form to create a new bird.

1. Create a function called `feedAndMultiply` with two parameters: `_birdId` (a `uint`) and `_targetDna` (also a `uint`). This function should be `public`.
2. We don't want other people to be able to feed our bird! We will verify that we are the owner of this bird. Add a `require` statement to check that `msg.sender` is equal to the owner of the bird (similar to what we did in the `createRandomBird` function).

> *Note: Similarly, because our response validation is basic, `msg.sender` needs to be placed first for it to be validated correctly. Normally, when you code, you can choose the order as you prefer, as both are correct.*

3. We will need the DNA of this bird. The next thing our function should do is declare a local `Bird` variable called `myBird` (which will be a `storage` pointer). Set this variable equal to the element at index `_birdId` in our `birds` array.

You should have 4 lines of code so far, including the closing `}` line.

We will continue filling in this function in the next exercise!