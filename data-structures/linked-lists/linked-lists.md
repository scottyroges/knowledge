# Linked Lists
Description: Creates a chain of nodes where each node has a reference to the next one

Strengths: Optimizes insertion and deletion since only the pointing node has to be edited

Weakness: Searching requires looking at potentially looping through all the nodes 

Complexity:

| Operation | Time Complexity |
| --- | --- |
| Insertion | O(n) |
| Search | O(n) |
| Deletion | O(n) |

Doubly linked list has nodes that reference the previous node and the next node. It also has a reference to the head and the tail so that operations
 can take place from either end.
Circularly linked list is simple linked list whose tail, the last node, references the head, the first node.
