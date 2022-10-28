# Quiz 019
screenshot

## My solutions
### Code
```.py
def get_l3tt3r(msg: str):
    output = ""
    for letter in msg:
        if letter == 'a':
            output += '4'
        elif letter == 'e':
            output += '3'
        elif letter == 'i':
            output += '1'
        elif letter == 'o':
            output += '0'
        elif letter == ' ':
            output += '_'
        else:
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
