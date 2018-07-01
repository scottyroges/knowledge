# Get Nth Element from End of Linked List

```java
private static SinglyLinkedListImpl.Node getNthFromEnd(SinglyLinkedListImpl linkedList, int n)
{
    int length = 0;
    SinglyLinkedListImpl.Node curr = linkedList.head;
    while(curr != null)
    {
        length++;
        curr = curr.next;
    }

    int fromFront = length - n;
    curr = linkedList.head;
    SinglyLinkedListImpl.Node node = null;
    for(int i = 0; i <= fromFront; i++)
    {
        if(curr == null)
        {
            break;
        }

        if(i == fromFront)
        {
            node = curr;
            break;
        }
        curr = curr.next;
    }

    return node;
}
```