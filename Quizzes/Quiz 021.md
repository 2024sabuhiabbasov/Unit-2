# Quiz 021
**Statement**

![image](https://user-images.githubusercontent.com/111758436/201060449-c1d4bca0-8db2-4a49-93ce-f488ffa05ef3.png)

## My solutions
### Code for a
```.py
# Program for Quiz 021
def get_truth():
    print(f"| A | B | C | AB + not B + not BC |") # Printing the heading
    x = False # Defining x as False
    y = False # Defining y as False
    z = False # Defining z as False
    output = ''
    for i in range(1, 9):
        output = output + f"| {int(x)} | {int(y)} | {int(z)} | {str(int((((int(x) and int(y)) or (not int(y))) or (not (int(y) and int(z)))))).center(19, ' ')} |\n"
        if i % 4 == 0:
            x = not x
        if i % 2 == 0:
            y = not y
        z = not z
    return output

answer = get_truth() # Calling the program to print the truth table for 3 inputs
print(answer)
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/202156946-e121cd92-f9e9-4d02-9582-c014c813b984.png)

### Truth table for  ZW ⊕ (Z ⊕ Y(not W))
| W | X | Y | Z | not W | Y(not W) | Z ⊕ Y(not W)| ZW | ZW ⊕ (Z ⊕ Y(not W)) |
|---|---|---|---|-------|----------|--------------|----|------------------------|
| 0 | 0 | 0 | 0 | 1     | 0        | 0            | 0  | 0                      |
| 0 | 0 | 0 | 1 | 1     | 0        | 1            | 0  | 1                      |
| 0 | 0 | 1 | 0 | 1     | 1        | 1            | 0  | 1                      |
| 0 | 0 | 1 | 1 | 1     | 1        | 0            | 0  | 0                      |
| 0 | 1 | 0 | 0 | 1     | 0        | 0            | 0  | 0                      |
| 0 | 1 | 0 | 1 | 1     | 0        | 1            | 0  | 1                      |
| 0 | 1 | 1 | 0 | 1     | 1        | 1            | 0  | 1                      |
| 0 | 1 | 1 | 1 | 1     | 1        | 0            | 0  | 0                      |
| 1 | 0 | 0 | 0 | 0     | 0        | 0            | 0  | 0                      |
| 1 | 0 | 0 | 1 | 0     | 0        | 1            | 1  | 0                      |
| 1 | 0 | 1 | 0 | 0     | 0        | 0            | 0  | 0                      |
| 1 | 0 | 1 | 1 | 0     | 0        | 1            | 1  | 0                      |
| 1 | 1 | 0 | 0 | 0     | 0        | 0            | 0  | 0                      |
| 1 | 1 | 0 | 1 | 0     | 0        | 1            | 1  | 0                      |
| 1 | 1 | 1 | 0 | 0     | 0        | 0            | 0  | 1                      |
| 1 | 1 | 1 | 1 | 0     | 0        | 1            | 1  | 1                      |
### Boolen circuit for ZW ⊕ (Z ⊕ Y(not W))
![image](https://user-images.githubusercontent.com/111758436/199957668-e78ecb7c-adef-4089-b566-f70c2197d4ea.png)
