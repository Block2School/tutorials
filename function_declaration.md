# Function declaration

A function declaration in solidity looks like the following:

```solidity
function myFunction(string memory _name, uint _amount) public {

}
```

This is a function named myFunction that takes 2 parameters: a string and a uint. For now the body of the function is empty. Note that we're specifying the function visibility as public. We're also providing instructions about where the _name variable should be stored-in memory. This is required for all reference types such as arrays, structs, mappings, and strings.

What is a reference type you ask?

Well, there are two ways in which you can pass an argument to a Solidity function:

- By value, which means that the Solidity compiler creates a new copy of the parameter's value and passes it to your function. This allows your function to modify the value without worrying that the value of the initial parameter gets changed.
- By reference, which means that your function is called with a... reference to the original variable. Thus, if your function changes the value of the variable it receives, the value of the original variable gets changed.

You can call this function like that 

```solidity
myFunction("Yannick", 100);
```

In our app, we're going to need to be able to create some student. Let's create a function for that.

1. Create a `public` function named `createStudent`. It should take two parameters: **_name** (a `string`), and **_id** (a `uint`). Don't forget to pass the first argument by value by using the `memory` keyword

Leave the body empty for now — we'll fill it in later.

```solidity
contract Block2SchoolFactory {

    uint nbStudent = 16;
    uint Modulus = 10 ** nbStudent;

    struct {
			string name;
			uint studentId;
		}

		Student[] public students;
	
		//type your code here

}
```

Expected result :