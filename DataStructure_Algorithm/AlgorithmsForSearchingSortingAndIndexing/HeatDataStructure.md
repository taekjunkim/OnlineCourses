# Heap Data Structure

## What is Heap?
A heap is a complete binary tree, and the binary tree is a tree in which the node can have utmost two children. 

## What is a complete binary tree?
A complete binary tree is a binary tree in which all the levels except the last level. i.e., leaf node should be completely filled, and all the nodes should be left-justified. 

## Two types of the heap
* **Min Heap**: the value of the parent node should be less than or equal to either of its children
* **Max Heap**: the value of the parent node is greather than or equal to its children

## Max Heap Construction Algorithm
1. Create a new node at the end of heap
2. Assign new value to the node
3. Compare the value of this child node with its parent
4. If value of parent is less than child, then swap them
5. Repeat step 3 & 4 until Heap propertiey holds

## Max Heap Deletion Algorithm
> Deletion in Max (or Min) Heap always happens at the root to remove the Maximum (or minimum) value
1. Remove root node
2. Move the last element of last level to root
3. Compare the value of this root node with its children
4. If value of parent is less than child, then swap them (with the smaller one)
5. Repeat step 3 & 4 until Heap property holds
