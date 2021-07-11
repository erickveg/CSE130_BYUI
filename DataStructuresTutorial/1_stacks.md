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

```
# How to use Python's list as a LIFO stack:

stack = list()

stack.append('bananas')
stack.append('apples')
stack.append('mangos')
```
```
>>> stack
['bananas','apples','mangos']
```
```
>>> stack.pop()
'mangos'
>>> stack.pop()
'apples'
>>> stack.pop()
'bananas'
>>> stack.pop()
ERROR
```
## Performance
As you can notice, because we add or removed a stack component only from one end of the structure the performance of those operation will always be O(1).

## Example
Text Editor Undo Property

## Problem to Solve
Analyzing a Hamburger
* *
