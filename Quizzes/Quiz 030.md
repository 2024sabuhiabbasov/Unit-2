# Quiz 030
**Statement**

![image](https://user-images.githubusercontent.com/111758436/206598707-f23560eb-17b3-4be8-83a6-9dc4cbf5f240.png)

## My solutions
### Code for program
```.py
# Program for Quiz 030

import requests
import matplotlib.pyplot as plt
import numpy as np

plt.style.use("seaborn-v0_8-colorblind") # Choosing a style for graphs in the program

h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
number_samples_per_hour = 4 # Variable to smooth the data every 4 value
mean_per_hour = [] # Variable to find the mean per hour
x = [] # List for x-axis values of the graph
for t in range(0, len(h), 2):
    t_hour = h[t:t+number_samples_per_hour] # Making a list of every 4 variable from the list h
    mean_per_hour.append(sum(t_hour)/len(t_hour)) # Adding mean of 4 variables to the list mean_per_hour
    x.append(t) # Adding value t to the list x for x-axis values of the graph

ax = plt.axes()
ax.set_facecolor("lightsteelblue") # Choosing the background color
plt.grid(True, color='dimgray') # Adding grid to the graph
plt.plot(x, mean_per_hour, color='b') # Plotting graph
plt.xlabel("Samples") # Choosing title for x-axis
plt.ylabel("Relative humidity") # Choosing title for x-axis
plt.show() # Showing the graph
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/206601283-d2b780df-8e1a-4a73-8b51-6bd397087cfe.png)

### When was the internet first created?
January 1, 1983 is considered the official birthday of the Internet. Prior to this, the various computer networks did not have a standard way to communicate with each other. A new communications protocol was established called Transfer Control Protocol/Internetwork Protocol (TCP/IP). This allowed different kinds of computers on different networks to "talk" to each other. ARPANET and the Defense Data Network officially changed to the TCP/IP standard on January 1, 1983, hence the birth of the Internet. All networks could now be connected by a universal language.

<h3 align="center">
<strong>Works cited</strong>
</h3>

“A Brief History of the Internet.” A Brief History of the Internet, The Online Library Learning Center, https://usg.edu/galileo/skills/unit07/internet07_02.phtml. Accessed on 9 December 2022.
