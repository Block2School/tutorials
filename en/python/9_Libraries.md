# Libraries

You can import libraries (also called packages) to access new methods in Python.  
Import is usually done at the very top of the file.  

## Example

```python
import random

print(random.randint(1, 10)) # Displays a random value between 1 and 10.
```

It's also possible to import just one function from the package, like this:  
```python
from random import randint # Import only the randint function from the random package

print(randint(1, 10))
```

## It's your turn !

Import the `math` module and create a function that multiplies the parameter value by pi.