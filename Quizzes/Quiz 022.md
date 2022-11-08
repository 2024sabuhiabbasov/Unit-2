# Quiz 022
**Statement**

screenshot

## My solutions
### Code for a
```.py
# Program for Quiz 022

import math # Importing the math library
import random # Importing the random library
random.seed(1234) # The start number of the random number generator
def produce(n: int, m: int, s: int) -> str:
    output = "|   x    |  y(x)  |" # Heading text
    for i in range(0, n): # For loop to repeat the equation n time
        x = random.randint(0, 100) # Choosing a random number between 0 and 100
        y = pow(x, (0.5*pow(m/s, 2))) # The equation
        output += f"\n|{str(x).center(8, ' ')}|{str(round(y, 2)).center(8, ' ')}|" # Printing the equation
    return output
sample = produce(5, 3, 2) # Calling the function and making it equal to a variable
print(sample) # Printing the answer
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/200446429-69eedbbd-093e-4275-9174-f40085b5a566.png)

**Truth table for the program**

### Truth table for  ZW ⊕ (Z ⊕ Y(not W))

### Boolen circuit for ZW ⊕ (Z ⊕ Y(not W))
