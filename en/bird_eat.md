# What do birds eat ?

It's time to feed our birds ! What do birds eat ? Worms !

To be able to do that, we will need to read the DNA of the worms (wormDna) from the Worm smart contract. We can do this because the data of Worms is openly stored on the blockchain. Isn't the blockchain great?!

Don't worry - our game will not harm any Worm. We will only read the data from Worms; we are not capable of removing it.

## Interact with others contracts


To interact with a contract that we don't own on the blockchain, we need to define an `interface`.

Let's take a simple example. Imagine a contract like this on the blockchain:

```js
contract LuckyNumber {
  mapping(address => uint) numbers;

  function setNum(uint _num) public {
    numbers[msg.sender] = _num;
  }

  function getNum(address _myAddress) public view returns (uint) {
    return numbers[_myAddress];
  }
}
```

That would be a simple contract where anyone could store their lucky number, and it would be associated with their Ethereum address. Then anyone could look up their lucky number using their address.

Now, imagine we have an external contract that wants to read the data from this contract using the `getNum` function.

First, we should define an `interface` for the `LuckyNumber` contract:

```js
contract NumberInterface {
  function getNum(address _myAddress) public view returns (uint);
}
```

You will notice that it resembles the definition of a contract with a few differences. Firstly, we only declare the functions with which we want to interact - in this case, `getNum` - and we do not mention any other functions or variables.

Secondly, we do not define a function body; instead of `{` and `}`, we simply end the function declaration with a `;`.

It's like the skeleton of a contract. This is how the compiler knows that it is an interface.

By including this interface in our dapp's code, our contract knows what the functions of the other contract look like, how to call them, and what type of response to expect.

We will see how to call functions from the other contract in the next lesson. For now, let's declare our interface for the Worm contract.

## It's your turn

We have looked at the source code of `Worm` for you and found a function called `getWorm` that returns all the data of the `worms`, including their "genes" (which is what we need to create a new bird!).

The function looks like this:

```js
function getWorm(uint256 _id) external view returns (
    bool isGestating,
    bool isReady,
    uint256 cooldownIndex,
    uint256 nextActionAt,
    uint256 siringWithId,
    uint256 birthTime,
    uint256 matronId,
    uint256 sireId,
    uint256 generation,
    uint256 genes
) {
    Worm storage wor = worms[_id];

    // if this variable is equal to 0 then it's not in gestation
    isGestating = (wor.siringWithId != 0);
    isReady = (wor.cooldownEndBlock <= block.number);
    cooldownIndex = uint256(wor.cooldownIndex);
    nextActionAt = uint256(wor.cooldownEndBlock);
    siringWithId = uint256(wor.siringWithId);
    birthTime = uint256(wor.birthTime);
    matronId = uint256(wor.matronId);
    sireId = uint256(wor.sireId);
    generation = uint256(wor.generation);
    genes = wor.genes;
}
```

The function is a bit different from what we're used to. As you can see, it returns... a bunch of different values. If you come from a programming language like JavaScript, this is different - in Solidity, a function can return more than one value.

Now that we know what our function looks like, we can use it to create an interface:

1. Define an interface named `WormInterface`. It's like declare a new contract - we use the keyword `contract`.
2. Inside the interface, define a function `getWorm` (who will be a copy/paste of this function above, **but** with a `;` after the declaration `returns` instead of everything you have between `{}`).