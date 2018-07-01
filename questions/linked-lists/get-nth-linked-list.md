# Get Nth Element in Linked List (Iteratvice and Recursive)

```java
private static SinglyLinkedListImpl.Node getNthRecursive(SinglyLinkedListImpl linkedList, int n)
{
    return getNth(linkedList.head, n);
}

private static SinglyLinkedListImpl.Node getNth(SinglyLinkedListImpl.Node node, int n)
{
    if(node == null)
    {
        return null;
    }

    int count = 0;
    if(count == n)
    {
        return node;
    }
    return getNth(node.next, n -1);
}

private static SinglyLinkedListImpl.Node getNthIterative(SinglyLinkedListImpl linkedList, int n)
{
    SinglyLinkedListImpl.Node curr = linkedList.head;
    SinglyLinkedListImpl.Node node = null;
    for(int i = 0; i <= n; i++)
    {
        if(curr == null) {
            break;
        }

        if(i == n)
        {
            node = curr;
            break;
        }
        curr = curr.next;

    }
    return node;
}
```