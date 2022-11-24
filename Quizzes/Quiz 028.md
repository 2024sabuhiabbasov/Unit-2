# Quiz 028
**Statement**

![image](https://user-images.githubusercontent.com/111758436/203696790-2b6da300-1abe-43b5-b3f5-1bfadd9ae455.png)

## My solutions
### Code for program
```.py
# Program for Quiz 028

import matplotlib.pyplot as plt
import numpy as np

colors = ["\033[0;30m", "\033[0;31m", "\033[0;32m", "\033[0;33m", "\033[0;34m", "\033[0;35m", "\033[0;36m", "\033[0;37m"]
# Line above: Each element of the list colors[] represent a color as follows: black, red, green, yellow, blue, purple, cyan, white
bold_colors = ["\033[1;30m", "\033[1;31m", "\033[1;32m", "\033[1;33m", "\033[1;34m", "\033[1;35m", "\033[1;36m", "\033[1;37m"]
# Line above: Each element of the list colors[] represent a color but bold as follows: black, red, green, yellow, blue, purple, cyan, white
end_code = "\033[00m" # We need to use this variable to stop using formatting text (coloring in this code)

plt.style.use("seaborn-v0_8-colorblind") # Choosing graph style

data = {
    'x': [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19],
    'y': [24, 1, 2, 25, 26, 21, 23, 34, 49, 2, 19, 32, 7, 17, 36, 7, 45, 28, 40, 46]
}
data['title'] = "quiz028" # adding the item title:quiz028 to the dictionary
output = f"{colors[3]}|   {bold_colors[4]}x{colors[3]}    |  {bold_colors[1]}y(x){colors[3]}  |" # Heading text
print(f"{data['title'].center(19, ' ')}") # printing title item from the dictionary data
print(output, end='')
for i in range(len(data['x'])):
        print(f"\n{colors[3]}|{colors[4]}{str('%.2f' % data['x'][i]).center(8, ' ')}{colors[3]}|{colors[1]}{str('%.2f' % (round(data['y'][i], 2))).center(8, ' ')}{colors[3]}|", end='') # Printing the x and y, answer of the equation
ax = plt.axes()
ax.set_facecolor("lightsteelblue") # Choosing the background color
plt.grid(True, color='dimgray') # Adding grid to the graph
plt.plot(data['x'], data['y'], color='b') # Drawing graph
plt.title(f"{data['title']}") # Choosing title for the graph from the dictionary data
plt.show() # Showing the graph
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/203698762-aa21a456-352c-4e62-af91-82f259f21a0d.png)

### Convert the following rgb color to hex: red=10, green=255, blue=255
![image](https://user-images.githubusercontent.com/111758436/203700789-4a569edc-a61f-431d-8604-54cfb3090b90.png)
![image](https://user-images.githubusercontent.com/111758436/203700941-e0f95694-a989-41c1-b7f4-1bb97d3561be.png)
