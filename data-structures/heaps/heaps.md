# Heap
Description: A binary tree where each child is less than its parent. There is no order like in a BST, but the binary tree must be complete.

The shape property: the tree is a complete binary tree; that is, all levels of the tree, except possibly the last one (deepest) are fully filled and if the last level of the tree is not complete, the nodes of that level are filled from left to right.
The heap property: each node is greater than or equal to each of its children according to a comparison predicate defined for the data structure.

Uses: Priority Queue

Complexity:
| Operation | Time Complexity |
| --- | --- |
| Insert | O(logn) |
| Delete | O(logn) |
