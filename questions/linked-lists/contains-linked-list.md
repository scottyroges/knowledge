# Linked List Contains Element (Iterative and Recursive)
```java
private static boolean containsRecursive(SinglyLinkedListImpl linkedList, int key)
{
    return contains(linkedList.head, key);
}

private static boolean contains(SinglyLinkedListImpl.Node node, int key)
{
    if(node == null)
    {
        return false;
    }
    else
    {
        if(node.data == key)
        {
            return true;
        }
        return contains(node.next, key);
    }
}

private static boolean containsIterative(SinglyLinkedListImpl linkedList, int key)
{
    SinglyLinkedListImpl.Node curr = linkedList.head;
    while(curr != null)
    {
        if(curr.data == key)
        {
            return true;
        }
        curr = curr.next;
    }
    return false;
}
```