# Using an interface

Continue our previous example with `NumberInterface`, once we have defined the interface:

```js
contract NumberInterface {
    function getNum(address _myAddress) public view returns (uint);
}
```

We could use it inside a contract like this:

```js
contract MyContract {
    address NumberInterfaceAddress = 0xab38...
    // ^ FavoriteNumber contract address on Ethereum
    NumberInterface numberContract = NumberInterface(NumberInterfaceAddress)
    // Now `numberContract` is pointing to the other contract

    function someFunction() public {
        // Now we can call `getNum` from this contract :
        uint num = numberContract.getNum(msg.sender);
        // ...and do something with this `num`
    }
}
```

In this way, your contract can interact with any other contract on the Ethereum blockchain, as long as they expose their functions as `public` or `external`.

## It's your turn

We will set up our contract to be able to read the Worm smart contract!

1. I have saved the address of the Worm contract in the code for you, under a variable called `ckAddress`. In the next line, create a `WormInterface` named `wormContract`, and initialize it with `ckAddress`, similar to what we did with `numberContract` above.