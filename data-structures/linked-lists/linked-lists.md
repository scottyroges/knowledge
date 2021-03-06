# Linked Lists (Singly Linked List)
Description: Creates a chain of nodes where each node has a reference to the next one

Strengths: Optimizes insertion and deletion since only the pointing node has to be edited. Size doesn't need to be known at creation. Can grow with the data set

Weakness: No random access. Must go through head/tail to find internal nodes. Searching requires potentially looping through all the nodes 

### Complexity:

| Operation | Time Complexity |
| --- | --- |
| Insertion | O(1) |
| Search | O(n) |
| Deletion | O(1) |

### See Also:
* [Doubly Linked Lists](doubly-linked-lists.md)
* [Circulary Linked Lists](circularly-linked-lists.md)

### Language Specifics:
* [Java Usage](/languages/java/java-linked-lists.md)
* [Java Implementation](/languages/java/java-singly-linked-list.md)

### Practice Problems
* [Find Length of a Linked List (Iterative and Recursive)](/questions/linked-lists/length-linked-list.md)
* [Linked List Contains Element (Iterative and Recursive)](/questions/linked-lists/contains-linked-list.md)
* [Get Nth Element in Linked List (Iteratvice and Recursive)](/questions/linked-lists/get-nth-linked-list.md)
* [Get Nth Element from End of Linked List](/questions/linked-lists/get-nth-from-end-linked-list.md)
* [Find middle of Linked List](/questions/linked-lists/middle-linked-list.md)
* [Detect Loop in Linked List](/questions/linked-lists/loop-linked-list.md)