# Quiz 018
**Statement**

![image](https://user-images.githubusercontent.com/111758436/198935285-494856c5-c185-4140-b0f1-017955e45452.png)

## My solutions
### Code for the program
```.py
import math
# Program for Quiz 018

import math
def numberMatches(l: int, s: int):
    out = math.ceil(l//(s/100)/5) # ceil rounds a number up to the nearest integer
    return out

colors = ["\033[0;30m", "\033[0;31m", "\033[0;32m", "\033[0;33m", "\033[0;34m", "\033[0;35m", "\033[0;36m", "\033[0;37m"]
# Line above: Each element of the list colors[] represent a color as follows: black, red, green, yellow, blue, purple, cyan, white
bold_colors = ["\033[1;30m", "\033[1;31m", "\033[1;32m", "\033[1;33m", "\033[1;34m", "\033[1;35m", "\033[1;36m", "\033[1;37m"]
# Line above: Each element of the list colors[] represent a color but bold as follows: black, red, green, yellow, blue, purple, cyan, white
end_code = "\033[00m" # We need to use this variable to stop using formatting text (coloring in this code)

print(colors[4] ,end='')
lentgh = int(input("Please enter the length of the forest that Lily needs to cross: "))
speed = int(input("Please enter Lily's speed: "))
print(end_code, end='')
numberOfMatchsticks = numberMatches(l=lentgh, s=speed)

print(f"{colors[2]}If Lily's is {colors[1]}{speed} {colors[2]}and the length of the forest that she needs to cross is {colors[1]}{lentgh}{colors[2]}, she needs to burn {colors[1]}{numberOfMatchsticks}{colors[2]} matchsticks to cross the road safely.")
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/198936469-436c1844-2192-4d20-9923-b956ae2d0bda.png)

### Truth table for the equation out=ABC+(A+B+C)+not(notA notB notC)
