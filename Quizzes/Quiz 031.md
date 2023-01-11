# Quiz 031
**Statement**

![image](https://user-images.githubusercontent.com/111758436/206602050-7f7a46f5-6a5d-43f9-a7fa-c70a1e3b47fa.png)

## My solutions
### Code for program
```.py
# Program for Quiz 31

import requests
import matplotlib.pyplot as plt
import numpy as np

plt.style.use("seaborn-v0_8-colorblind") # Choosing a style for the graphs in the program

req = requests.get('http://192.168.6.142/readings') # Getting data from the server and making it equal to a variable
data = req.json() # Converting json file req to a directory
readings = data['readings'][0]
print(len(readings))

temperature = [] # List for collecting temperature values of data
for sample in readings:
    if sample['sensor_id'] == 5: # Choosing sensor id 5 as it gives us the temperature
        temperature.append(sample['value']) # Adding value of temperature to the list temperature
temperature = temperature[610:801] # Making the list equal to only its values range 600:801

x = [] # List for x-axis values of the graph
for t in range(0, len(temperature)):
    x.append(t) # Adding t to x-axis values
print(x)

a, b, c = np.polyfit(x, temperature, 2)
m, B = np.polyfit(x, temperature, 1)
linear_model = []
polynomial_model = []
for t in range(0, len(temperature)):
    polynomial_model.append(a*(t**2) + b*t + c)
    linear_model.append(m*t + B)

ax = plt.axes()
ax.set_facecolor("lightsteelblue") # Choosing the background color
plt.grid(True, color='dimgray')
plt.plot(x, temperature, 'o', color='#3281a8')
plt.plot(x, polynomial_model, color='#74a7f7')
plt.plot(x, linear_model, '#2395db')
plt.show()
```
**Testing the code**

**Test 1**

Couldn't test because of a problem in the server.
