# Quiz 021
**Statement**

screenshot

## My solutions
### Code for a
```.py
# Program for Quiz 021
def get_truth():
    print(f"| A | B | C | AB + not B + not BC |") # Printing the heading
    x = False # Defining x as False
    y = False # Defining y as False
    z = False # Defining z as False
    X = 0
    Y = 0
    Z = 0
    output = ''
    for i in range(1, 9):
        if not x:
            X = 0
        else:
            X = 1
        if not y:
            Y = 0
        else:
            Y = 1
        if not z:
            Z = 0
        else:
            Z = 1
        if i % 4 == 0:
            x = not x
        if i % 2 == 0:
            y = not y
        z = not z
        output = output + f"| {X} | {Y} | {Z} | {str(int((((X and Y) or (not Y)) or (not (Y and Z))))).center(19, ' ')} |\n"
    return output

answer = get_truth() # Calling the program to print the truth table for 3 inputs
print(answer)
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/199947308-2a2a89f4-7dd4-4299-89f6-1d7b023d6367.png)

**Truth table for the program**

| A | B | C | AB | notB | BC | not BC | AB or notB | (AB or not B) or (not BC) |
|---|---|---|----|------|----|--------|------------|---------------------------|
| 0 | 0 | 0 | 0  | 1    | 0  | 1      | 1          | 1                         |
| 0 | 0 | 1 | 0  | 1    | 0  | 1      | 1          | 1                         |
| 0 | 1 | 0 | 0  | 0    | 0  | 1      | 0          | 1                         |
| 0 | 1 | 1 | 0  | 0    | 1  | 0      | 0          | 0                         |
| 1 | 0 | 0 | 0  | 1    | 0  | 1      | 1          | 1                         |
| 1 | 0 | 1 | 0  | 1    | 0  | 1      | 1          | 1                         |
| 1 | 1 | 0 | 1  | 0    | 0  | 1      | 1          | 1                         |
| 1 | 1 | 1 | 1  | 0    | 1  | 0      | 1          | 1                         |

### Truth table for 

### Boolen circuit for
