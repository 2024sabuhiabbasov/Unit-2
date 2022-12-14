# Quiz 022
**Statement**

![image](https://user-images.githubusercontent.com/111758436/201060610-c07efa74-fb7d-4b63-a7cd-4fca45bc980b.png)

## My solutions
### Code for program
```.py
# Program for Quiz 022

import math # Importing the math library
import random # Importing the random library
random.seed(1234) # The start number of the random number generator

colors = ["\033[0;30m", "\033[0;31m", "\033[0;32m", "\033[0;33m", "\033[0;34m", "\033[0;35m", "\033[0;36m", "\033[0;37m"]
# Line above: Each element of the list colors[] represent a color as follows: black, red, green, yellow, blue, purple, cyan, white
bold_colors = ["\033[1;30m", "\033[1;31m", "\033[1;32m", "\033[1;33m", "\033[1;34m", "\033[1;35m", "\033[1;36m", "\033[1;37m"]
# Line above: Each element of the list colors[] represent a color but bold as follows: black, red, green, yellow, blue, purple, cyan, white
end_code = "\033[00m" # We need to use this variable to stop using formatting text (coloring in this code)

def produce(n: int, m: int, s: int) -> str:
    output = f"{colors[3]}|   {bold_colors[2]}x{colors[3]}    |  {bold_colors[1]}y(x){colors[3]}  |" # Heading text
    for i in range(0, n): # For loop to repeat the equation n time
        x = random.randint(0, 100) # Choosing a random number between 0 and 100
        y = pow(x, (0.5*pow(m/s, 2))) # The equation
        output += f"\n{colors[3]}|{colors[2]}{str(x).center(8, ' ')}{colors[3]}|{colors[1]}{str(round(y, 2)).center(8, ' ')}{colors[3]}|" # Printing the equation
    return output

sample = produce(5, 3, 2) # Calling the function and making it equal to a variable
print(sample) # Printing the answer
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/200589400-502edee6-238a-4475-8bfe-37b48def2eaf.png)

### Proof that: A (A + B) = A
**Truth table for A (A + B)**

| A | B | A + B | A (A + B) |
|---|---|-------|-----------|
| 0 | 0 | 0     | 0         |
| 0 | 1 | 1     | 0         |
| 1 | 0 | 1     | 1         |
| 1 | 1 | 1     | 1         |

As we can see from the table, A and A (A + B) has the same values for all rows. From here, we can say that A is equal to A (A + B).
