# Breadth First Search
Description:
An algorithm that searches a tree (or graph) by searching levels of the tree first, starting at the root.
It finds every node on the same level, most often moving left to right.
While doing this it tracks the children nodes of the nodes on the current level.
When finished examining a level it moves to the left most node on the next level.
The bottom-right most node is evaluated last (the node that is deepest and is farthest right of it's level).

Uses a queue

