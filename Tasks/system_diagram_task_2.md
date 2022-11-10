# Task 2 - System diagram
**Statement**

![image](https://user-images.githubusercontent.com/111758436/201068915-063aae8a-ff64-433a-9b84-3b7ffbb75f5a.png)

## My solutions
### Code for program
```.py
# Program for blinking 3 leds with Arduino

from pyfirmata import Arduino
import time

def validate_int_input(prompt:str)->int:
    num = input(prompt)
    while not num.isdigit() or int(num) < 0 or int(num) > 7:
        num = input(f"{prompt}")
        if num.isdigit():
            if int(num) < 0 or int(num) > 7:
                num = input(f"{prompt}")
    return int(num)

board = Arduino("COM3") # Defining COM3 as the board
print("Communication Successfully started")
while True:
    number = validate_int_input("Please input a number from 0 to 7 you want to see in leds: ")
    # Getting input from the user with using the function validate_int_input

    x = False # Defining x as False
    y = False # Defining y as False
    z = False # Defining z as False

    if number == 0: # If number is 0, it will turn off all the LEDs
        print(str(int(x)) + str(int(y)) + str(int(z)))
        board.digital[6].write(x)
        board.digital[8].write(y)
        board.digital[13].write(z)

    if number > 0: # If the number is bigger than 0, this block of code will work
        for i in range(1, 9):
            if i % 4 == 0: # Defining x as its opposite (1, if it is 0. 0, if it is 1) every 4 step
                x = not x
            if i % 2 == 0: # Defining y as its opposite (1, if it is 0. 0, if it is 1) every 2 step
                y = not y
            z = not z # Defining x as its opposite (1, if it is 0. 0, if it is 1) every step
            if i == number: # If i equals to the number user entered, the code will work
                print(str(int(x)) + str(int(y)) + str(int(z)))
                board.digital[6].write(x) # Sending the value of x to the first LED
                board.digital[8].write(y) # Sending the value of y to the second LED
                board.digital[13].write(z) # Sending the value of z to the third LED
```

### Video of the circuit
