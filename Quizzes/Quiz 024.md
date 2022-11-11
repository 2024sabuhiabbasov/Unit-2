# Quiz 024
**Statement**

Screeenshot

## My solutions
### Code for program
```.py
# Program for Quiz 024

from matplotlib import pyplot as plt
import numpy as np

colors = ["\033[0;30m", "\033[0;31m", "\033[0;32m", "\033[0;33m", "\033[0;34m", "\033[0;35m", "\033[0;36m", "\033[0;37m"]
# Line above: Each element of the list colors[] represent a color as follows: black, red, green, yellow, blue, purple, cyan, white
bold_colors = ["\033[1;30m", "\033[1;31m", "\033[1;32m", "\033[1;33m", "\033[1;34m", "\033[1;35m", "\033[1;36m", "\033[1;37m"]
end_code = "\033[00m" # We need to use this variable to stop using formatting text (coloring in this code)
# Line above: Each element of the list colors[] represent a color but bold as follows: black, red, green, yellow, blue, purple, cyan, white

x = [1, 2, 3, 1.5, 4, 2.5, 6, 4, 3, 5.5, 5, 2]
y = [3, 4, 8, 4.5, 10, 5, 15, 9, 5, 16, 13, 3]

plt.scatter(x, y, color="b") # Drawing a scatter plot graph with color blue ("b")
plt.title("Scatter plot")
plt.xlabel("x") # Labeling the x-axis as "x"
plt.ylabel("$y=2.78x-1.20 $") # Labeling the y-axis "y"

m, b = np.polyfit(x, y, 1)
output = f"{colors[3]}|   {bold_colors[2]}x{colors[3]}    |  {bold_colors[1]}y(x){colors[3]}  |" # Heading text
x_out = [] # List for values of x to store and return
y_out = [] # List for values of y to store and return
print(output, end='')
for i in range(1, 8):
    x_out.append(i) # Adding the value of x to the list x_out
    Y = m*i+b # The equation
    y_out.append(Y) # # Adding the value of Y to the list y_out
    print(f"\n{colors[3]}|{colors[2]}{str('%.2f' % i).center(8, ' ')}{colors[3]}|{colors[1]}{str('%.2f' % (round(Y, 2))).center(8, ' ')}{colors[3]}|", end='') # Printing the x and y, answer of the equation

plt.plot(x_out, y_out, color='r', marker='.') # Drawomg a graph with color red ("r") and market points (".")

plt.show() # Showing the graph
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/201291462-5597f1ad-c5cd-4dd6-b7dd-0d00654ebde7.png)

### Circuit for not(bit0 bit1 + not (bit0 + bit1))
