# Conditions

## Explanation

A condition allows you to check the accuracy of certain information, as well as the value of your variables.

## Writing

```python
if condition:
    return True # The condition has been met, so we move on to this section
elif other_condition:
    return False # The first condition is not met, so we check whether the second condition is met. If it is, we move on to this section.
else:
    return None # None of the conditions are met, so we go to "the default branch".
```

## Condition types

Take as variables `bigValue`, `smallValue` and `trueVal` such as:  
```python
bigValue = 560
smallValue = 15
trueVal = True
```

- Strictly greater than -> `if bigValue > smallValue` will return `True`.
- `<` Strictly less than -> `if bigValue < smallValue` will return `False`.
- `>=` Greater than or equal to -> `if bigValue >= 560` will return `True`.
- `<=` Less than or equal to -> `if bigValue <= 559` will return `False`.
- `==` Equal to -> `if bigValue == 560` will return `True`. `if bigValue == "560"` will also return `True`.
- `not` Is not -> `if not trueVal` will return `False`. `if trueVal` will return `True`.
- `and` And, multiple conditions -> `if bigValue < smallValue and trueVal` will return `False`.
- Or, multiple conditions -> `if bigValue < smallValue or trueVal` will return `True`.

_You can link several `and` and `or` in the same branch. You can also use parentheses._

## It's your turn

Complete the functions.