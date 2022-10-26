# Quiz 017
**Statement**

Create a function that produces the average world length of the input list. [HL] Do not count the spaces.

## Test cases
![](https://github.com/2024sabuhiabbasov/Unit-2/blob/main/Quizzes/Images/Quiz%20017%20-%20test%20cases.png)

## My solutions
### Code
```.py
# Program to find the average word length in a string

def avarageLength(words: list)->float:
    lengthSum = 0 # Variable for the length of all words
    number_of_words = 0 # Variable for the number of words in the given list
    for word in words: # For loop to check each element of the given list
        word_list = word.split(' ') # We split word if it has space (HL requirement)
        for split_word in word_list: # For loop for every split word in one element of the given list
            lengthSum += len(split_word) # Calculating the length of all words in the given list
            number_of_words += 1 # Calculating the number of words in the given list
    return lengthSum/(number_of_words)
    # Returning the average by diving the length of the words in the given list by
    # the number of the words in the given list

colors = ["\033[0;30m", "\033[0;31m", "\033[0;32m", "\033[0;33m", "\033[0;34m", "\033[0;35m", "\033[0;36m", "\033[0;37m"]
# Line above: Each element of the list colors[] represent a color as follows: black, red, green, yellow, blue, purple, cyan, white
end_code = "\033[00m" # We need to use this variable to stop using formatting text (coloring in this code)

words1 = ["Computer Science", "Art"]
words2 = ["hello", "main"]
words3 = ["Peru", "France", "Nepal"]
words4 = ["one", "two"]

case1 = avarageLength(words1) # Variable for case 1, calling the function
case2 = avarageLength(words2) # Variable for case 2, calling the function
case3 = avarageLength(words3) # Variable for case 3, calling the function
case4 = avarageLength(words4) # Variable for case 4, calling the function

print(f"{colors[2]}The average word length of the list {colors[3]}{words1}{colors[2]} is {colors[1]}{case1}")
print(f"{colors[2]}The average word length of the list {colors[3]}{words2}{colors[2]} is {colors[1]}{case2}")
print(f"{colors[2]}The average word length of the list {colors[3]}{words3}{colors[2]} is {colors[1]}{case3}")
print(f"{colors[2]}The average word length of the list {colors[3]}{words4}{colors[2]} is {colors[1]}{case4}")

print(f"\n{colors[1]}Note:{colors[4]} This code is for HL tests. It doesn't count spaces.")
```
**Testing the code**

**Test 1**

![](https://github.com/2024sabuhiabbasov/Unit-2/blob/main/Quizzes/Images/Quiz%20017%20-%20testing%20the%20code.png)
