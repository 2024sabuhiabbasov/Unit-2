# Quiz 023
**Statement**

![image](https://user-images.githubusercontent.com/111758436/201064317-19a6b026-5a51-4f70-bfbe-bba1a7e34fd2.png)

## My solutions
### Code for program
```.py
# Program for Quiz 023

import math # Importing the math library
import random # Importing the random library
from matplotlib import pyplot as plt # Importing the pyplot library as plt (we will use plt from now on to call the function)
random.seed(1234) # The start number of the random number generator

colors = ["\033[0;30m", "\033[0;31m", "\033[0;32m", "\033[0;33m", "\033[0;34m", "\033[0;35m", "\033[0;36m", "\033[0;37m"]
# Line above: Each element of the list colors[] represent a color as follows: black, red, green, yellow, blue, purple, cyan, white
bold_colors = ["\033[1;30m", "\033[1;31m", "\033[1;32m", "\033[1;33m", "\033[1;34m", "\033[1;35m", "\033[1;36m", "\033[1;37m"]
# Line above: Each element of the list colors[] represent a color but bold as follows: black, red, green, yellow, blue, purple, cyan, white
end_code = "\033[00m" # We need to use this variable to stop using formatting text (coloring in this code)

def produce(n: int, m: int, s: int) -> str:
    output = f"{colors[3]}|     {bold_colors[2]}x{colors[3]}      |    {bold_colors[1]}y(x){colors[3]}    |" # Heading text
    x_out = [] # List for values of x to store and return
    y_out = [] # List for values of y to store and return
    print(output, end='')
    for i in range(0, n): # For loop to repeat the equation n time
        x = random.randint(0, 100) # Choosing a random number between 0 and 100
        x_out.append(x) # Adding the value of x to the list x_out
        y = pow(x, (0.5*pow(m/s, 2))) # The equation
        y_out.append(y) # Adding the value of y to the list y_out
        print(f"\n{colors[3]}|{colors[2]}{str(x).center(12, ' ')}{colors[3]}|{colors[1]}{str(round(y, 2)).center(12, ' ')}{colors[3]}|", end='') # Printing the x and y, answer of the equation

    return y_out, x_out # Returning two values: list y_out and x_out

data_y, data_x = produce(10, 5, 2) # Calling the function produce and stroing returned values in values data_y and data_x

plt.plot(data_x, data_y, color="b", marker=".") # Drawing the graph with color blue ("b") and adding points with marker point (".")
plt.xlabel("x") # Labeling the x-axis as "x"
plt.ylabel("$y=x^{1/2(m/s)^2} $") # Labeling the y-axis as the equation. Writing in dollar signs helps it to seem as an equation
plt.show() # Showing the graph
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/201066968-327f1fc1-b8de-4b51-b2b7-ce9d7319b261.png)

### Truth table for: A(A ⊕ B)
