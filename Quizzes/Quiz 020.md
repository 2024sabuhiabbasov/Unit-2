# Quiz 020
**Statement**

![image](https://user-images.githubusercontent.com/111758436/199932045-6f867600-77d1-4542-8927-c5024d249ca4.png)

## My solutions
### Code for a
```.py
# Program for Quiz 020
def get_truth():
    print(f"| A | B | C |") # Printing the heading
    x = False # Defining x as False
    y = False # Defining y as False
    z = False # Defining z as False
    for i in range(1, 9):
        if not x: 
            print(f"| 0 |", end='')
        else:
            print(f"| 1 |", end='')
        if not y:
            print(f" 0 |", end='')
        else:
            print(f" 1 |", end='')
        if not z:
            print(f" 0 |")
        else:
            print(f" 1 |")
        if i % 4 == 0:
            x = not x
        if i % 2 == 0:
            y = not y
        z = not z

get_truth() # Calling the program to print the truth table for 3 inputs
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/199932674-6a0b2685-4bdf-4c3d-81d4-b7c0c403fee5.png)

### Truth table for S1S2+(S2+S3(notS1))S1
| S1 | S2 | S3 | S1S2 | not S1 | S3(notS1) | S2+S3(notS1) | (S2+S3(notS1))S1 | S1S2+(S2+S3(notS1))S1 |
|----|----|----|------|--------|-----------|--------------|------------------|-----------------------|
| 0  | 0  | 0  | 0    | 1      | 0         | 0            | 0                | 0                     |
| 0  | 0  | 1  | 0    | 1      | 1         | 1            | 0                | 0                     |
| 0  | 1  | 0  | 0    | 1      | 0         | 1            | 0                | 0                     |
| 0  | 1  | 1  | 0    | 1      | 1         | 1            | 0                | 0                     |
| 1  | 0  | 0  | 0    | 0      | 0         | 0            | 0                | 0                     |
| 1  | 0  | 1  | 0    | 0      | 0         | 0            | 0                | 0                     |
| 1  | 1  | 0  | 1    | 0      | 0         | 1            | 1                | 1                     |
| 1  | 1  | 1  | 1    | 0      | 0         | 1            | 1                | 1                     |

### Boolen circuit for S1S2+(S2+S3(notS1))S1 
