# Msg.sender

Now that we have our mappings to track the ownership of a bird, let's update the `_createBird` method to use them.

To do this, we will utilize something called `msg.sender`.

## msg.sender

In Solidity, there are global variables accessible to all functions. One of them is `msg.sender`, which refers to the `address` of the person (or smart contract) who called the current function.

> *Note: In Solidity, executing a function requires an external call. A contract will simply remain on the blockchain doing nothing until someone calls one of its functions. There will always be a `msg.sender` in such cases.*

Here is an example of using `msg.sender` to update a `mapping`:

```js
mapping (address => uint) favoriteNumber;

function setMyNumber(uint _myNumber) public {
  // update our `favoriteNumber` mapping to store `_myNumber` under `msg.sender`
  favoriteNumber[msg.sender] = _myNumber;
  // ^ The syntax to store datas inside a mapping is the same for arrays
}

function whatIsMyNumber() public view returns (uint) {
  // We get the value stored inside the sender address
  // Who will be `0` if the sender doesn't already call `setMyNumber`
  return favoriteNumber[msg.sender];
}
```

In this trivial example, anyone can call `setMyNumber` and store a `uint` in our contract, which would be associated with their address. They can then call `whatIsMyNumber`, and they would receive the uint they stored back.

Using `msg.sender` provides security to the Ethereum blockchain - the only way for someone to modify another person's data would be to steal their private key associated with their Ethereum address.

## It's your turn

Let's update our `_createBird` function from our last exercise to designate the caller of this function as the owner of a bird.

1. After retrieving the `id` of the new bird, let's update our `birdToOwner` mapping to store `msg.sender` under that `id`.
2. Then, let's increment our `ownerBirdCount` for `msg.sender`.

In solidity you can increment a `uint` using `++`, like Javascript.

```js
uint number = 0;
number++;
// `number` value is now `1`
```

The final answer for this exercise must be 2 lines code length.