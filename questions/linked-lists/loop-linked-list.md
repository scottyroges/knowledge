# Detect Loop in Linked List

```java
public static boolean isLoopPointer(SinglyLinkedListImpl linkedList)
{
    SinglyLinkedListImpl.Node p1 = linkedList.head;
    SinglyLinkedListImpl.Node p2 = linkedList.head;

    while(p2 != null && p2.next != null)
    {
        p1 = p1.next;
        p2 = p2.next.next;

        //put after we move pointer, otherwise it will always be true
        if(p1.equals(p2))
        {
            return true;
        }
    }
    return false;
}

public static boolean isLoopHash(SinglyLinkedListImpl linkedList)
{
    Set<SinglyLinkedListImpl.Node> set = new HashSet<>();

    SinglyLinkedListImpl.Node curr = linkedList.head;
    while(curr != null)
    {
        if(set.contains(curr))
        {
            return true;
        }
        else
        {
            set.add(curr);
        }
        curr = curr.next;
    }
    return false;
}
```

Follow up question: how long is the loop
```java
public static int loopCountPointer(SinglyLinkedListImpl linkedList)
{
    SinglyLinkedListImpl.Node p1 = linkedList.head;
    SinglyLinkedListImpl.Node p2 = linkedList.head;

    SinglyLinkedListImpl.Node loopStart = null;
    while(p2 != null && p2.next != null)
    {
        p1 = p1.next;
        p2 = p2.next.next;

        //put after we move pointer, otherwise it will always be true
        if(p1.equals(p2))
        {
            loopStart = p1;
            break;
        }
    }

    int count = 0;
    if(loopStart != null)
    {
        SinglyLinkedListImpl.Node curr = loopStart;
        while(curr != null)
        {
            count++;
            curr = curr.next;
            if(curr.equals(loopStart)){
                curr = null;
            }
        }
    }
    return count;
}
public static int loopCountHash(SinglyLinkedListImpl linkedList)
{

    SinglyLinkedListImpl.Node curr = linkedList.head;
    SinglyLinkedListImpl.Node prev = null;

    Map<SinglyLinkedListImpl.Node, Integer> map = new HashMap<>();
    int i = 0;
    while(curr != null)
    {
        if(map.containsKey(curr))
        {
            return map.get(prev) - map.get(curr) + 1;
        }
        else
        {
            map.put(curr, i++);
        }
        prev = curr;
        curr = curr.next;
    }

    int count = 0;
    return count;
}
```