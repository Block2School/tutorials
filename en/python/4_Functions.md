# Functions and typing

## Defining a function

A function allows you to perform a series of actions. It can also be useful when you need to repeat several actions several times in your code.  

```python
def myFunction(param1, param2): # myFunction is the function name, and can include one or more parameters.
    return param1 > param2 # Returns the result of the condition (True or False)
```

A function can return a value which can then be retrieved by a variable like this:

```python
result = myFunction(3, 5) # result will be False.
```

## Typing

Since the most recent versions of Python, it has been possible to type variables, parameters and function returns. Here's how:

### Function

```python
def myFunction(param1: int, param2: int) -> bool: # Here, our function takes two int parameters and returns a bool.
    return param1 > param2
```

Typing is not strict in Python, which means you can use a str variable as a function parameter and not an int variable in the above function. You can return an int type and not a bool type.  
However, it's better to type functions so that developers can find their way around your code more easily.  

### Variable

```python
myVariable: int = 10
myText: str = "My text"
```

## It's your turn

Write the `containStr` function with 3 parameters:  
- The first takes a string
- The second takes another string
- The third takes an integer

Your function should return `True` if the 1st parameter contains the same number of times the second parameter as the third.  
Example:
```python
containStr("Example text", "m", 1) # Must return True because there is 1 m in the first parameter.
containStr("Example text", "x", 5) # Must return False because there are not the same number of x's in the first parameter.
```