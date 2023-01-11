# Quiz 032
**Statement**

![image](https://user-images.githubusercontent.com/111758436/211807364-17cbeb78-f8f0-4a55-8a8b-800bdedf5350.png)

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

temperature_10 = [] # List for collecting temperature values of data of sensor 10
temperature_9 = [] # List for collecting temperature values of data of sensor 9
for sample in readings:
    if sample['sensor_id'] == 9: # Choosing sensor id 9 as it gives us the temperature
        temperature_9.append(sample['value']) # Adding value of temperature to the list temperature
    elif sample['sensor_id'] == 10:
        temperature_10.append(sample['value'])
    

number_samples_per_hour = 12
mean_per_hour_9 = []
mean_per_hour_10 = []
x_9 = []
x_9_smooth = []
x_10 = []
x_10_smooth = []
difference_graph_data = []
for t in range(0, len(temperature_9), 12):
    t_hour_9 = temperature_9[t:t+number_samples_per_hour] # Finding mean of every 12 values and adding them to the list
    mean_per_hour_9.append(sum(t_hour_9)/len(t_hour_9)) # Finding mean of every 12 values
    x_9.append(t)
    x_9_smooth.append(t + 1)
    t_hour_10 = temperature_10[t:t+number_samples_per_hour]
    mean_per_hour_10.append(sum(t_hour_10)/len(t_hour_10))
    x_10.append(t)
    x_10_smooth.append(t + 1)

t_test = [] 
for t in range(0, (len(temperature_9)//12)):
    difference_graph_data.append(mean_per_hour_10[t] - mean_per_hour_9[t])
    t_test.append(t)


plt.subplot(3, 1, 1)
plt.grid(True, color='dimgray')
plt.plot(x_9_smooth, mean_per_hour_9, color='#3281a8')
plt.title("Sensor #9")
plt.subplot(3, 1, 2)
plt.grid(True, color='dimgray')
plt.plot(x_10_smooth, mean_per_hour_10, color='#3281a8')
plt.title("Sensor #10")
plt.subplot(3, 1, 3)
plt.grid(True, color='dimgray')
plt.plot(t_test, difference_graph_data, color='#3281a8')
plt.title("Comparison graph")
plt.show()
```
**Testing the code**

**Test 1**

Couldn't test because of a problem in the server.

### a) What are the three main operators used in boolean logic?
Answer: and, or, not
