# EX 6D BRUTE FORCE ALGORITHM

## AIM:
To write a python program using brute force method of searching for the given substring in the main string.




## Algorithm
Start the program.

Input the main string str1 and the substring str2.

Define a function match(string, sub) that:

Calculate the length of the main string l and the substring ls.

Loop over the main string from index 0 to l - ls:

Check if the slice string[i:i+ls] matches sub.

If it matches, print the index i as the starting position.

Call match(str1, str2) to find all occurrences.

Stop the program.   

## Program:
```
/*
To implement the program using brute force method of searching for the given substring in the main string.


Developed by: Dinesh M
Register Number: 212222040039

def match(string,sub):
    l = len(string)
    ls = len(sub)
    start = sub[0]
    for i in range(l-ls+1):
        if string[i:i+ls]==sub:
            print(f"Found at index {i}")

    ########### Add your code here #######

str1=input()
str2=input()

*/
```

## Output:
<img width="1273" height="410" alt="Screenshot 2025-09-07 191951" src="https://github.com/user-attachments/assets/d82ba51d-7212-4277-adfe-8f2011cc41b8" />



## Result:
Thus the above program was executed successfully for searching the substring at respective index.
