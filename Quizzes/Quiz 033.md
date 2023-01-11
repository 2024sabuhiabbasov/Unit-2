# Quiz 033

## My solutions
### Code for program
```.py
# Program for quiz 033

import matplotlib.pyplot as plt
from matplotlib.gridspec import GridSpec
from unit2_lib import get_sensor, smoothing

plt.style.use('ggplot')

sensors = [6, 8, 9, 10]
values = []
for s in sensors:
    # get the sensors from the server
    value = get_sensor(id=s)
    # smooth the data with a size of 12 samples
    x, smoothed_value = smoothing(data=value[0:501])
    values.append(smoothed_value)

# calculate the mean of the four sensors
mean_per_hour = []
for i in range(len(values[0])):
    # list comprehension
    data = [values[n][i] for n in range(len(sensors))]
    mean_per_hour.append(sum(data) / len(sensors))
print(f"Ready for plotting")

fig=plt.figure(figsize=(10,8))
#from matplotlib.gridspec import GridSpec
gs = GridSpec(4, 4, figure=fig)
# plot the mean of the sensors
ax = fig.add_subplot(gs[:, 0:3]) # all the rows, col 0 to 2
plt.title("Average of sensors")
plt.plot(x,mean_per_hour)
plt.ylim([20, 28])
plt.xlabel("Samples per hour")
plt.ylabel("Celsius")

for row, my_color in [(0,"#e63946"), (1, "#457b9d"), (2, "#6a994e"), (3, 'purple')]:
    ax = fig.add_subplot(gs[row,3])  #gs[row, col]
    plt.title(f"Sensor #{sensors[row]}")
    plt.plot(x, values[row], color=my_color)
    plt.tick_params('x', labelbottom=False)

plt.tick_params('x', labelbottom=True)
plt.show()
```
**Testing the code**

**Test 1**

Couldn't test because of a problem in the server.
