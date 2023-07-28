# Heaps

```ad-summary 
title: Heap
A tree-based data structure in which the value of a parent node is oredered in a certain way with respect to the value of its child node(s). A heap can be either a *min heap* (the value of a parent node is less than or equal to the value of its children) or a *max heap* (the value of a parent node is a greater than or equal to the value of its children)
```

![[Pasted image 20230725132642.png]]

link: [https://www.geeksforgeeks.org/heap-data-structure/](https://www.geeksforgeeks.org/heap-data-structure/)

## What are Heaps?

The purpose of a *min-heap* is to store objects that have a partial order on them. It has a fast (`O(log n))`) method for removing the minimum object from the heap. Min-heaps are useful for calculations where you have multiple minimum computations to perform.

A heap is either a max-heap or a min-heap, it can't be both. Given an implementation of a min-heap, a max-heap can be implemented by reversing the comparison between elements.

## How to build min-heap

A *min-heap* is a *Complete Binary Tree*. A min-heap is typically represented as an array (`Arr`). The root element will be at `Arr[0]`. For any $i$-th node: `Arr[i]` Then we have

* `Arr[(i-1)/2]` returns its parent node.
* `Arr[(2*i)+1]` returns its left child node.
* `Arr[(2*1)+2]` returns its right child node.

### Operations on min-heap

* **getMin()**: It returns the root element of the min-heap.

* **extractMin()**: Removes the minimum element from min-heap. Time complexity of this operation is `O(log n)` as this operation needs to maintain the heap property (by calling **heapify()**) after removing root

* **insert()**: Inserting a new key takes `O(log n)` time. We add a new key at the end of the tree. If new key is larger than its parent, then we don't need to do anything. Otherwise, we need to traverse up to fix the violated heap property.

## Crucial Terms

* **Key**: The values that determine the order. If you're storing numbers, the numbers can be the keys. If you're storing more complicated objects, the key is the data field that we're comparing by. Unlike in hash tables, keys in heaps do **not** have to be unique.
* **extract_min**: The method of (quickly) being able to extract the minimum element from the min-heap.

## Strengths and Weaknesses

### Strengths

* A min-heap is able to quickly extract the minimum value on the heap. Repeated extractions from a min-heap into an array will yield a sorted array.

### Weaknesses

* There's no convenient way of searching for a particular `key` value in a heap. Entries are only partially ordered; clever use of the heap property can allow for some pruning of searches.


## When to use Heaps

Heaps are designed to do one specific thing well. We use a heap when we have to do repeated minimum (maximum) **extractions**.  Some examples include:

* **Finding the minimum distance between two nodes in a graph**: The standard approach to this problem is to use [[Dijkstra's algorithm]]. One of the key steps in Dijkstra's algorithm is to select the node closest to a node that you have already completed, which is a minimum calculation. 

* **Getting the next event that is scheduled to occur**: Storing events in a heap with a timestamp as the key gives you a fast way to extract the next event (the event with the smallest timestamp will occur next)