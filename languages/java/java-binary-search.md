# Binary Search
### Recursive
Things to Remember:
* right must always be greater than or equal to left
* difference between right and left divided by 2 is the amount to shift over from left

Implementation:
```java
private static int myBinarySearchRecursive(int[] array, int left, int right, int s)
{
    int index = -1;
    if(right >= left)
    {
        int diff = right - left;
        int shift = diff/2;
        int middle = left + shift;
        if(array[middle] == s)
        {
            index = middle;
        }
        else if(array[middle] > s) //check left
        {
            index = myBinarySearchRecursive(array, left, middle -1, s);
        }
        else //check right
        {
            index = myBinarySearchRecursive(array, middle + 1, right, s);
        }
    }

    return index;
}
```

### Iterative
Things to Remember:
* right must always be greater than or equal to left
* difference between right and left divided by 2 is the amount to shift over from left
* looks almost identical to recursive, except we just keep changing left and right instead of passing them to the function again
* dont forget to break out of the while look when the number is found

Implementation:
```java
private static int myBinarySearchIterative(int[] array, int left, int right, int s)
{
    int index = -1;
    while(right >= left)
    {
        int diff = right - left;
        int shift = diff/2;
        int middle = left + shift;
        if(array[middle] == s)
        {
            index = middle;
            break;
        }
        else if(array[middle] > s) //check left
        {
            right = middle - 1;
        }
        else //check right
        {
            left = middle + 1;
        }
    }
    return index;
}
```