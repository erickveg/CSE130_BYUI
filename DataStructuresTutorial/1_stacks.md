# STACKS

## Table of Contents

* [Introduction](#introduction)
* [Stacks in Python](#stacks-in-python)
* [Performance](#performance)
* [Example](#example)
* [Problem to Solve](#problem-to-solve)

## Introduction

A stack is a linear data structure which means that each element exists next to each other in memory. The main feature of a stack is that new components can be added or removed only from one end also known as Last In First Out (LIFO) estructure, while other data structures like [Queues](https://dbader.org/blog/queues-in-python) remove items from one end and added to the oposite end. Stacks are used to implement functions and are used in a variety of ways in computer science because is useful to process nested functions.

## Stacks in Python

The built-in List data structure in Python can be used to implement a stack. To add a new component in the stack we use the function `append()` and to remove any element from the end `pop()` is used, but it must be used carefully because it won't work if the list is empty.

```python
# How to use Python's list as a LIFO stack:

stack = list()

# Add elements to the stack
stack.append('bananas')
stack.append('apples')
stack.append('mangos')
```
```python
>>> stack
['bananas','apples','mangos']
```
```python
# Remove items from the stack
>>> stack.pop()
'mangos'
>>> stack.pop()
'apples'
>>> stack.pop()
'bananas'
>>> stack.pop()
ERROR  # You can't remove any item because the stack is empty
```
## Performance
As you can notice, because we add or removed a stack component only from one end of the structure the performance of those operation will always be O(1). 

## Example
Have you ever been writing an important document and suddenly you press a key and everything desapears? You get desperate but remember that "Ctrl + Z" is there to undo your mistake. How does the computer know what to put back when you use the Undo property? In this example we will implement a simple text editor with the capacity to undo any deletion. 

```python
# Create a stack to store the text inserted by the user
text = []
# Create a stack to store the words deleted
memory = []

quit = False

while quit == False:
    
    user_input = int(input(""" 
    Choose an option:
    (1) Insert text
    (2) Delete last word
    (3) Undo deletion
    (4) Quit 
    """))

    if user_input == 1:
        user_text = input("Insert text here: ")
        for word in user_text.split():
            text.append(word)
    
    if user_input == 2:
        if len(text) > 0: # Make sure your text stack is not empty
            removed_word = text.pop()
            memory.append(removed_word)
            print(f"You have removed the word {removed_word}")
        else:
            print("Sorry, you need to insert text first")
    
    if user_input == 3:
        if len(memory) > 0 # Make sure your memory stack is not empty
            
            restore_word = text.append(memory.pop())
            print(f"Word: {restore_word} added again")
        else:
            print("No words in 'memory'")
    
    # Exit the program if the user enters 4
    if user_input == 4:
        quit = True

    print(f"""\n 
    ==================
    {' '.join(text)}
    ==================
    """)
```
OUTPUT:
```
Choose an option:
    (1) Insert text
    (2) Delete last word
    (3) Undo deletion
    (4) Quit 
    
>>> 1

Insert text here: My name is Erick

==================
My name is Erick
==================

Choose an option:
    (1) Insert text
    (2) Delete last word
    (3) Undo deletion
    (4) Quit 

>>> 2 
You have removed the word 'Erick'

==================
My name is
==================

Choose an option:
    (1) Insert text
    (2) Delete last word
    (3) Undo deletion
    (4) Quit 

>>> 3

Word: 'Erick' added again

==================
My name is Erick
==================

... # Menu removed for simplicity

>>> 3    # 'is' removed
>>> 3    # 'name' removed
>>> 3    # 'My' removed
>>> 3
No words in memory

>>> 2    # 'My' added to text
==================
My 
==================
```


## Problem to Solve


[Back to Welcome Page](0_Welcome.md)

