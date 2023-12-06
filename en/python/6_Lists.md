# Lists

Lists are special variables. These variables are not instantiated, as is the case with dictionaries, which we'll see later.  
This means that if a list is created outside a function, and within that function, an element is removed from the list, even without returning the list, it will be modified.

## Definition

A list is defined as follows:  

```python
myList = [] # List definition

myList.append("Value") # Append a value to the list
del myList[0] # Delete the list element at index 0
len(myList) # Gets the length of the list
```

## It's your turn

Complete the functions.