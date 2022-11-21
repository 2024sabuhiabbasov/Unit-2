# Quiz 027
**Statement**

![image](https://user-images.githubusercontent.com/111758436/203176827-72259f00-2973-447f-b7cb-336eea8ee717.png)

## My solutions
### Code for program
```.py
# Program for Quiz 027

import matplotlib.pyplot as plt
import numpy as np

plt.style.use("seaborn-v0_8-colorblind")

sensorA = [16, 24, 24, 9, 23, 26, 26, 23, 25, 14]
sensorB = [2, 19, 25, 10, 11, 24, 17, 7, 24, 17]
sensorC = [15, 11, 24, 21, 6, 2, 18, 27, 1, 16]

# Step 1: Visualize data
samples = [] # empty list
for i in range(len(sensorA)): # list to make the list samples full of values from 0 to the length of sensorA 
    samples.append(i)

fig = plt.figure(figsize=(8, 4)) # choosing graph size
plt.subplot(1, 2, 1) # drawing the first graph
plt.grid(True, color='dimgray') # drawing grid
plt.plot(samples, sensorA, color='#3264a8') # adding values of sensorA to the graph
plt.plot(samples, sensorB, color='#3290a8') # adding values of sensorB to the graph
plt.plot(samples, sensorC, color='#32a89c') # adding values of sensorC to the graph
plt.legend(['sensorA', 'sensorB', 'sensorC']) # adding labels of colors to the graph
# Step 3: Analyze the data
mean = [] # empty list for means
standard_dev = [] # empty list for standard deviations
min_v = [] # empty list for minimum values from the lists 
max_v = [] # empty list for maximum values from the lists
for i in range(len(sensorA)): # list for finding mean, standard deviation, minimum, and maximum values from the lists
    data = [sensorA[i], sensorB[i], sensorC[i]] # variable for every i-th element of sensorA, sensorB, and sensorC
    min_v.append(min(data)) # adding the minimum value to the list min_v from the i-th elements of sensorA, sensorB, and sensorC
    max_v.append(max(data)) # adding the maximum value to the list max_v from the i-th elements of sensorA, sensorB, and sensorC
    mean.append(np.mean(data)) # adding the mean to the list mean from the i-th elements of sensorA, sensorB, and sensorC
    standard_dev.append(np.std(data)) # adding the standard deviation to the list standard_dev from the i-th elements of sensorA, sensorB, and sensorC

plt.subplot(1, 2, 2) # drawing the second graph
plt.fill_between(samples, max_v, min_v, alpha=0.5, linewidth=0, color="#267a91") # filling the graph with color for showing the maximum and minumum values
plt.errorbar(samples, mean, standard_dev, fmt='o') # adding error bars to the graph
plt.show() # showing the graph
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/202661195-1c311800-38ba-46cc-a541-ec756c1e1cfa.png)

### Convert the following rgb color to hex to rgb: red=250, green=100, blue=10

red=250: 250//16=15=f, remainder=10=a, **red=fa**

green=100: 100//16=6, remainder=4, **green=64**

blue=10: 10//16=0, remainder=10=a, **blue=0a**

![image](https://user-images.githubusercontent.com/111758436/202662435-b0d4e4e6-9f6a-477b-b727-0c402eb765e8.png)
