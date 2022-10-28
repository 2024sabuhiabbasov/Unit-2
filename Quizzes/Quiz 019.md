# Quiz 019
screenshot

## My solutions
### Code
```.py
# Program for Quiz 019

def get_l3tt3r(msg: str):
    output = ""
    for letter in msg:
        if letter == 'a': # Checking if the letter is a, it will add 4 as a character to the output
            output += '4'
        elif letter == 'e': # Checking if the letter is e, it will add 3 as a character to the output
            output += '3'
        elif letter == 'i': # Checking if the letter is i, it will add 1 as a character to the output
            output += '1'
        elif letter == 'o': # Checking if the letter is o, it will add 0 as a character to the output
            output += '0'
        elif letter == ' ': # Checking if the letter is a space, it will add _ as a character to the output
            output += '_'
        else: # In all other cases, it will add the letter itself to output
            output += letter
    return output

green = "\033[0;32m"
end_code = "\033[00m"

case1 = get_l3tt3r("Hello World")
print(f"Hello World after the change: {green}{case1}{end_code}")
case2 = get_l3tt3r("Why did I choose CS?")
print(f"Why did I choose CS? after the change: {green}{case2}{end_code}")
case3 = get_l3tt3r("Remember the Figure Caption")
print(f"Remember the Figure Caption after the change: {green}{case3}")
```
**Testing the code**

**Test 1**

![](![image](https://user-images.githubusercontent.com/111758436/198482439-9c4e94ac-a0bf-4241-a5c8-f454c0790e48.png)
