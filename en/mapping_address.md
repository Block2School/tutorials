# Mapping and addresses

We made some birds and now let's assigning owners to birds in our database.  
For this, we will need two data types: mapping and address.  

## Address

The Ethereum blockchain consists of accounts, similar to bank accounts. An account holds a balance of Ether (the currency used on the Ethereum blockchain), and you can send Ethers to other accounts or receive them, just like transferring money from one bank account to another.

Each account has an `address`, which is equivalent to a bank account number. It is a unique identifier that represents an account and looks like:

`0x0000000000000000000000`

> *This address doesn't exists, it's just an example*

We will delve into the details of addresses in a future lesson, but for now, the key thing to understand is that an address belongs to a unique user (or a smart contract).

Therefore, we can use it as a unique ID to establish the ownership of our zombies. When a user creates new zombies by interacting with our application, we can define the ownership of these zombies based on the Ethereum address used to call the function.

## Mapping

In first lesson, we covered structures and arrays. Mappings are another way to organize data in Solidity.

Here's an example of a `mapping`:

```js
// For a financial application, you can store a uint representing the balance of a user account using a mapping :
mapping (address => uint) public accountBalance;
// Mappings can also be used to store and retrieve usernames based on a userId.
mapping (uint => string) userIdToName;
```

A mapping is essentially a key-value storage for storing and retrieving data. In the first example, the key is an address and the value is a uint, and in the second example, the key is a uint and the value is a string.

## It's your turn !

To track the ownership of a bird, we will use two mappings: one that stores the address associated with a bird, and another that keeps track of how many birds a user owns.

1. Create a mapping called `birdToOwner`. The key is a `uint` (we will store and retrieve the bird using its id), and the value is an `address`. This mapping will be `public`.

2. Create a mapping called `ownerBirdCount`, where the key is an `address` and the value is a `uint`