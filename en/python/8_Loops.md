# Loops

A loop executes the same series of instructions, but with different values.

## Example

```python
for i in range(0, 10): # Between 0 included and 10 excluded.
    print(i) # Displays the value of i at each turn of the loop. So 0, 1, 2, 3... up to 9.
```

## Loop list elements

It is possible to loop over the elements of a list.

```python
myList = ["first", "second", "third", "fourth"]

for elem in myList:
    print(elem) # Displays first, then second, then third and finally fourth.
```

## It's your turn !

Complete the function.  
This function must modify each element of the parameter list by adding the `int` value of the second parameter, and return the list