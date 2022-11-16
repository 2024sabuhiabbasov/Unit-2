# Quiz 024
**Statement**

![image](https://user-images.githubusercontent.com/111758436/202153192-6b16a1fa-9bda-4e59-9851-6e66f93df9ae.png)

## My solutions
### Code for program
```.py
# Program for Quiz 024

import math # Importing the math library
import random # Importing the random library
from matplotlib import pyplot as plt # Importing the pyplot library as plt (we will use plt from now on to call the function)

colors = ["\033[0;30m", "\033[0;31m", "\033[0;32m", "\033[0;33m", "\033[0;34m", "\033[0;35m", "\033[0;36m", "\033[0;37m"]
# Line above: Each element of the list colors[] represent a color as follows: black, red, green, yellow, blue, purple, cyan, white
bold_colors = ["\033[1;30m", "\033[1;31m", "\033[1;32m", "\033[1;33m", "\033[1;34m", "\033[1;35m", "\033[1;36m", "\033[1;37m"]
end_code = "\033[00m" # We need to use this variable to stop using formatting text (coloring in this code)
# Line above: Each element of the list colors[] represent a color but bold as follows: black, red, green, yellow, blue, purple, cyan, white

output = f"{colors[3]}|     {bold_colors[2]}x{colors[3]}      |    {bold_colors[1]}y(x){colors[3]}    |" # Heading text
x_out = [] # List for values of x to store and return
y_out = [] # List for values of y to store and return
print(output, end='')
x = -10
for i in range(0, 101): # For loop to repeat the equation n time
    x_out.append(x) # Adding the value of x to the list x_out
    y = 2*(pow(x + 5, 2)) # The equation
    y_out.append(y) # Adding the value of y to the list y_out
    print(f"\n{colors[3]}|{colors[2]}{str('%.2f' % x).center(12, ' ')}{colors[3]}|{colors[1]}{str('%.2f' % (round(y, 2))).center(12, ' ')}{colors[3]}|", end='') # Printing the x and y, answer of the equation
    x = x + 0.2

plt.plot(x_out, y_out, color="b") # Drawing the graph with color blue ("b") and adding points with marker point (".")
plt.xlabel("x") # Labeling the x-axis as "x"
plt.ylabel("$y={2(x + 5)^2} $") # Labeling the y-axis as the equation. Writing in dollar signs helps it to seem as an equation
plt.show() # Showing the graph
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/202163552-2b772ebb-59ec-40cb-9d66-ba051a3224fd.png)

### Circuit for not(bit0 bit1 + not (bit0 + bit1))
![image](https://user-images.githubusercontent.com/111758436/201292633-d618a288-e838-467f-b418-fb89106f1f48.png)
