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

**Truth table for the program**

### Truth table for  ZW ⊕ (Z ⊕ Y(not W))

### Boolen circuit for ZW ⊕ (Z ⊕ Y(not W))
