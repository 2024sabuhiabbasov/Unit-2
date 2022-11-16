# Quiz 025
**Statement**

![image](https://user-images.githubusercontent.com/111758436/202158501-6a23984a-6a40-4ff8-8539-3fc9be99023e.png)

## My solutions
### Code for program
```.py
# Program for Quiz 025

from matplotlib import pyplot as plt
import numpy as np

colors = ["\033[0;30m", "\033[0;31m", "\033[0;32m", "\033[0;33m", "\033[0;34m", "\033[0;35m", "\033[0;36m", "\033[0;37m"]
# Line above: Each element of the list colors[] represent a color as follows: black, red, green, yellow, blue, purple, cyan, white
bold_colors = ["\033[1;30m", "\033[1;31m", "\033[1;32m", "\033[1;33m", "\033[1;34m", "\033[1;35m", "\033[1;36m", "\033[1;37m"]
end_code = "\033[00m" # We need to use this variable to stop using formatting text (coloring in this code)
# Line above: Each element of the list colors[] represent a color but bold as follows: black, red, green, yellow, blue, purple, cyan, white

output = f"{colors[3]}|   {bold_colors[2]}x{colors[3]}    |  {bold_colors[1]}y(x){colors[3]}  |" # Heading text
x_out = [] # List for values of x to store and return
y_out = [] # List for values of y to store and return
print(output, end='')
x = -10
for i in range(0, 101):
    x_out.append(x) # Adding the value of x to the list x_out
    Y = abs(x) # The equation
    y_out.append(Y) # # Adding the value of Y to the list y_out
    print(f"\n{colors[3]}|{colors[2]}{str('%.2f' % x).center(8, ' ')}{colors[3]}|{colors[1]}{str('%.2f' % Y).center(8, ' ')}{colors[3]}|", end='') # Printing the x and y, answer of the equation
    x = x + 0.2

plt.plot(x_out, y_out, color='b') # Drawing a graph with color red ("r") and market points (".")
plt.xlabel("x") # Labeling the x-axis as "x"
plt.ylabel("$y=|x| $") # Labeling the y-axis "y"

plt.show() # Showing the graph
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/202163135-c0b15127-8f25-472c-90bb-01f2606fa719.png)

### Convert FFA5 to decimal
