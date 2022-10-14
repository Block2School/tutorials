# Math Operation

Math in Solidity is pretty straightforward. The following operations are the same as in most programming languages:

- Addition: `x + y`
- Subtraction: `x - y`,
- Multiplication: `x * y`
- Division: `x / y`
- Modulus / remainder: `x % y` *(for example, `13 % 5` is `3`, because if you divide 5 into 13, 3 is the remainder)*

Solidity also supports an ***exponential operator*** (i.e. "x to the power of y", x^y):

```solidity
uint x = 5 ** 2; // equal to 5^2 = 25
```

To make sure our Block2school Factory is only 16 characters, let's make another `uint` equal to 10^16. That way we can later use the modulus operator `%` to shorten an integer to 16 digits.

1. Create a `uint` named `Modulus`, and set it equal to **10 to the power of** nbStudent.

```solidity
pragma solidity >=0.5.0 <0.6.0;

contract Block2schoolFactory {

    uint nbStudent = 16;
    //type your code here

}
```

Expected Result