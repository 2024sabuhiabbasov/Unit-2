# Quiz 029
**Statement**

![image](https://user-images.githubusercontent.com/111758436/204445946-d85315ed-325f-4eeb-9303-91de5ef69127.png)

## My solutions
### Code for program
```.py
# Program for Quiz 029

colors = ["\033[0;30m", "\033[0;31m", "\033[0;32m", "\033[0;33m", "\033[0;34m", "\033[0;35m", "\033[0;36m", "\033[0;37m"]
# Line above: Each element of the list colors[] represent a color as follows: black, red, green, yellow, blue, purple, cyan, white
bold_colors = ["\033[1;30m", "\033[1;31m", "\033[1;32m", "\033[1;33m", "\033[1;34m", "\033[1;35m", "\033[1;36m", "\033[1;37m"]
# Line above: Each element of the list colors[] represent a color but bold as follows: black, red, green, yellow, blue, purple, cyan, white
end_code = "\033[00m" # We need to use this variable to stop using formatting text (coloring in this code)

def count_letters(lexicon: dict, msg: str)->str: # Function for counting letters
    for letter in msg: # A for loop for every letter in the message given to the function
        if letter in lexicon.keys(): # If statement to check if the dictionary lexicon has a key with the name letter
            lexicon[letter] += 1 # Increasing the value of key by 1
    return lexicon # Returning the dictionary lexicon

my_dict1 = {
    'w': 0,
    'l': 0,
    'c': 0
}
message1 = "hello world"

my_dict2 = {
    'a': 0,
    'e': 0,
    'i': 0,
    'o': 0,
    'u': 0
}

message2 = "Why did I choose CS?"

output1 = count_letters(my_dict1, message1)
output2 = count_letters(my_dict2, message2)
print(output1)
print(output2)
```
**Testing the code**

**Test 1**

![image](https://user-images.githubusercontent.com/111758436/204446024-e15c63e1-b039-45c1-9d60-9cecda4c0a84.png)

### How many different colors could you represent in a 6 bit computer? 
Answer: 64

Work: 
