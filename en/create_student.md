# Create a student

Remember our `Person`struct in the previous example?

```solidity
struct Person {
  uint age;
  string name;
}

Person[] public people;
```

Now we're going to learn how to create new `Persons` and add them to our `people`array.

```solidity
// create a New Person:
Person satoshi = Person(172, "Satoshi");

// Add that person to the Array:
people.push(satoshi);
```

We can also combine these together and do them in one line of code to keep things clean:

```solidity
people.push(Person(16, "Vitalik"));
```

Note that `array.push()`adds something to the **end** of the array, so the elements are in the order we added them. See the following example:

```solidity
uint[] numbers;
numbers.push(5);
numbers.push(10);
numbers.push(15);
// numbers is now equal to [5, 10, 15]
```

Let's make our createStudent function do something!

1. Fill in the function body so it creates a new `Student`, and adds it to the `students` array. The `name` and `studentId` for the new Student should come from the function arguments.
2. Let's do it in one line of code to keep things clean.

```solidity
contract Block2SchoolFactory {

    uint nbStudent = 16;
    uint Modulus = 10 ** nbStudent;

    struct {
			string name;
			uint studentId;
		}

		Student[] public students;
	
		function createStudent(string memory _name, uint _studentId) public {
			//type your code here
		}

}
```

Exepected result