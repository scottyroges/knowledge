# Depth First Search
Description:
An algorithm that searches a tree (or graph) by searching depth of the tree first, starting at the root.
It traverses left down a tree until it cannot go further.
Once it reaches the end of a branch it traverses back up trying the right child of nodes on that branch, and if possible left from the right children.
When finished examining a branch it moves to the node right of the root then tries to go left on all it's children until it reaches the bottom.
The right most node is evaluated last (the node that is right of all it's ancestors).

Uses a stack