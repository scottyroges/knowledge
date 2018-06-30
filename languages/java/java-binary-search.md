# Binary Search
## Example Usage
```java
java.util.Arrays.binarySearch(int[] a, int key);
```

## Custom Implementation
### Recursive
Things to Remember:
* right must always be greater than or equal to left
* left plus right divided by 2 to find the middle
* when left and right are equal, thats the end of the recursion since the next calls will fail the if statement
* works for all array sizes (eg. 0, 1, 2)

```java
private static int myBinarySearchRecursive(int[] array, int left, int right, int s)
{
    int index = -1;
    if(right >= left)
    {
        int middle = (left + right)/2;
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
* looks almost identical to recursive, except we just keep changing left and right instead of passing them to the function again
* dont forget to break out of the while look when the number is found

```java
private static int myBinarySearchIterative(int[] array, int left, int right, int s)
{
    int index = -1;
    while(right >= left)
    {
        int middle = (left + right)/2;
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