# Quiz 026
**Statement**

![image](https://user-images.githubusercontent.com/111758436/202620578-9d3ab0fa-9a7f-4d99-bce3-0cf8a3e37e78.png)

## My solutions
### Code for program
```.py
# Program for Quiz 026

from matplotlib import pyplot as plt
import numpy as np

colors = ["\033[0;30m", "\033[0;31m", "\033[0;32m", "\033[0;33m", "\033[0;34m", "\033[0;35m", "\033[0;36m", "\033[0;37m"]
# Line above: Each element of the list colors[] represent a color as follows: black, red, green, yellow, blue, purple, cyan, white
bold_colors = ["\033[1;30m", "\033[1;31m", "\033[1;32m", "\033[1;33m", "\033[1;34m", "\033[1;35m", "\033[1;36m", "\033[1;37m"]
# Line above: Each element of the list colors[] represent a color but bold as follows: black, red, green, yellow, blue, purple, cyan, white
end_code = "\033[00m" # We need to use this variable to stop using formatting text (coloring in this code)

h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
samples = [] # empty list

for i in range(len(h)):
    samples.append(i) # Adding the value of x to the list x_out
   # Y = abs(x) # The equation

   # print(f"\n{colors[3]}|{colors[2]}{str('%.2f' % x).center(8, ' ')}{colors[3]}|{colors[1]}{str('%.2f' % Y).center(8, ' ')}{colors[3]}|", end='') # Printing the x and y, answer of the equation

m, b = np.polyfit(samples, h, 1)
output = f"{colors[3]}|   {bold_colors[2]}x{colors[3]}    |  {bold_colors[1]}y(x){colors[3]}  |" # Heading text
x_out = [] # List for values of x to store and return
y_out = [] # List for values of y to store and return
print(output, end='')
for i in range(0, 32):
    x_out.append(i) # Adding the value of x to the list x_out
    Y = m*i+b # The equation
    y_out.append(Y) # # Adding the value of Y to the list y_out
    print(f"\n{colors[3]}|{colors[2]}{str('%.2f' % i).center(8, ' ')}{colors[3]}|{colors[1]}{str('%.2f' % (round(Y, 2))).center(8, ' ')}{colors[3]}|", end='') # Printing the x and y, answer of the equation

ax = plt.axes()
ax.set_facecolor("lightsteelblue") # Choosing the background color
plt.grid(True, color='dimgray') # Adding grid to the graph
plt.plot(samples, h, linestyle='none', marker='v') # Adding dots to the graph
plt.plot(x_out, y_out, color='b') # Drawing a line
plt.title("Relative humidity") # Choosing the title for the graph
plt.xlabel("Samples") # Labeling the x-axis as "Samples"
plt.ylabel("Relative humidity") # Labeling the y-axis "Relative humidity"

plt.show() # Showing the graph
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/202622492-b12ee2ef-df20-4555-8a7e-d880f01eef93.png)

### Convert the following color in hex to rgb: #e6e627
e6e627 = 14 x 16⁵ + 6 x 16⁴ + 14 x 16³ + 6 x 16² + 2 x 16¹ + 7 x 16⁰ = 14680064 + 393216 + 57344 + 1536 + 32 + 7 = 15132199₁₀
