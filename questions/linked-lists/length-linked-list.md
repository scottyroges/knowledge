# Find Length of a Linked List (Iterative and Recursive)
```java
private static int lengthRecursive(SinglyLinkedListImpl linkedList)
{
    return getLength(linkedList.head);
}

private static int getLength(SinglyLinkedListImpl.Node node)
{
    if(node == null)
    {
        return 0;
    }
    else
    {
        return 1 + getLength(node.next);
    }
}

private static int lengthIterative(SinglyLinkedListImpl linkedList)
{
    SinglyLinkedListImpl.Node curr = linkedList.head;
    int i = 0;
    while(curr != null)
    {
        curr = curr.next;
        i++;
    }
    return i;
}
```