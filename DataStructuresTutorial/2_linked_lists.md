# Linked Lists

## Table of Contents

* [Introduction](#introduction)
* [Structure](#structure)
* [Linked Lists in Python](#linked-lists-in-python)
* [Performance](#performance)
* [Linked List vs Dynamic Array](#differences-between-a-linked-list-and-a-dynamic-array)
* [Example](#example)
* [Problem to Solve](#problem-to-solve)

## Introduction
A linked list is a collection of data stored in a random way in memory which means elements of the structure are not next to the other (for more information scroll down clic here: [Linked List vs Dynamic Array](#differences-between-a-linked-list-and-a-dynamic-array)). Therefore, the structure needs a way to track the position of each element to keep the structure together, here we introduce the term of a __Node__. The node will contain both the value and a link to the previous and next node, this is Bi-directional linking.

## Structure

In a link list we called the first node __the head__ and the last one __the tail__. If you know where __the head__ is, you will be able to traverse the entire list and access to all the nodes of the structure.   

![realpython.com](Group_21.webp)

## Linked Lists in Python
* Using collections.deque

## Performance
O(n)

## Linked List vs Dynamic Array

The main difference between a linked list and a dynamic array is how the memory is managed, therefore, the same operations might have different perfomance on each one.

## Example
* Example using collections.deque

## Problem to Solve
* Implement your own linked list ...
```
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
```

