# Search an element in a Linked List (Iterative and Recursive)
```java
private static boolean searchRecursive(SinglyLinkedListImpl linkedList, int key)
{
    return search(linkedList.head, key);
}

private static boolean search(SinglyLinkedListImpl.Node node, int key)
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
        return search(node.next, key);
    }
}

private static boolean searchIterative(SinglyLinkedListImpl linkedList, int key)
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