# Struct

Sometimes you need a more complex data type. For this, Solidity provides ***structs***:

```solidity
struct Person {
  uint age;
  string name;
}
```

Structs allow you to create more complicated data types that have multiple properties.

In our app, we're going to want to create some students! And students will have multiple properties, so this is a perfect use case for a struct.

1. Create a struct named Student
2. Our student will have 2 properties: name (a string), and an studentId (a `uint`)

```solidity
pragma solidity >=0.5.0 <0.6.0;

contract Block2SchoolFactory {

    uint nbStudent = 16;
    uint Modulus = 10 ** nbStudent;

    // type your code here 

}
```

Exepted result