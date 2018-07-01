# Singly Linked List Implementation

```java
public class SinglyLinkedListImpl {
    Node head;

    private static class Node
    {
        int data;
        Node next;

        public Node(int data) {
            this.data = data;
        }
    }

    public void push(int data)
    {
        Node node = new Node(data);
        node.next = head;
        head = node;
    }

    public void append(int data)
    {
        Node node = new Node(data);
        Node curr = head;
        while(curr.next != null)
        {
            curr = curr.next;
        }
        curr.next = node;
    }

    public void insertAfter(int data, int index)
    {
        Node node = new Node(data);

        Node curr = head;

        for(int j = 0; j <= index; j++)
        {
            if(j == index)
            {
                node.next = curr.next;
                curr.next = node;
                break;
            }

            curr = curr.next;
            if(curr == null)
            {
                break;
            }
        }
    }

    public void deleteNode(int data)
    {
        if(head.data == data)
        {
            //detach head
            head = head.next;
        }
        else
        {
            Node curr = head.next;
            Node prev = head;
            while(curr != null)
            {
                if(curr.data == data)
                {
                    prev.next = curr.next;
                }
                prev = curr;
                curr = curr.next;
            }
        }
    }

    public void deleteIndex(int index)
    {
        if(index == 0)
        {
            head = head.next;
        }
        else
        {
            Node curr = head.next;
            Node prev = head;
            for(int j = 1; j <= index; j++)
            {
                if(j == index)
                {
                    prev.next = curr.next;
                    break;
                }

                prev = curr;
                curr = curr.next;

                if(curr == null)
                {
                    break;
                }
            }
        }
    }

    public void delete()
    {
        head = null;
    }

    public void print()
    {
        Node curr = this.head;
        while(curr != null)
        {
            System.out.print(curr.data + ",");
            curr = curr.next;
        }
        System.out.println();
    }

    public static void main(String[] args) {
        SinglyLinkedListImpl linkedList = new SinglyLinkedListImpl();
        Node n1 = new Node(1);
        Node n2 = new Node(2);
        Node n3 = new Node(3);

        linkedList.head = n1; //attach the head
        linkedList.head.next = n2; //attach 2nd node to head node
        n2.next = n3; //attach 3rd node directly to 2nd node

        linkedList.print(); //1,2,3

        linkedList.push(0);
        linkedList.print(); //0,1,2,3

        linkedList.append(5);
        linkedList.print(); //0,1,2,3,5

        linkedList.insertAfter(4, 3);
        linkedList.print(); //0,1,2,3,4,5

        linkedList.deleteNode(4);
        linkedList.print(); //0,1,2,3,5

        linkedList.deleteNode(0);
        linkedList.print(); //1,2,3,5

        linkedList.deleteIndex(0);
        linkedList.print(); //2,3,5

        linkedList.deleteIndex(1);
        linkedList.print(); //2,5

        linkedList.delete();
        linkedList.print();

    }
}
```