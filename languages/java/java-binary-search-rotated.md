# Binary Search Rotated Array

## Custom Implementation
### Recursive
Things to Remember:
* Only works with a distinct array
```java
private static int binarySearchRotatedArrayRecursive(int[] array, int left, int right, int key)
{
    int index = -1;
    if(left <= right)
    {
        int mid = (left + right)/2;

        if(array[mid] == key)
        {
            index = mid;
        }
        else if(array[left] <= array[mid]) //left side is sorted
        {
            if(array[left] <= key && array[mid] >= key) //we can do binary search on the left
            {
                index = binarySearchRotatedArrayRecursive(array, left, mid -1, key);
            }
            else
            {
                index = binarySearchRotatedArrayRecursive(array, mid + 1, right, key);
            }
        }
        else //right side sorted
        {
            if(array[mid] <= key && array[right] >= key) //we can do binary search on the right
            {
                index = binarySearchRotatedArrayRecursive(array, mid +1, right, key);
            }
            else
            {
                index = binarySearchRotatedArrayRecursive(array, left, mid -1, key);
            }
        }
    }
    return index;
}
 ```
### Iterative
 ```java
private static int binarySearchRotatedIterative(int[] array, int left, int right, int key)
{
    int index = -1;
    while(left <= right)
    {
        int mid = (left + right)/2;

        if(array[mid] == key)
        {
            index = mid;
            break;
        }
        else if(array[left] <= array[mid]) //left side is sorted
        {
            if(array[left] <= key && array[mid] >= key) //we can do binary search on the left
            {
                right = mid -1;
            }
            else
            {
                left = mid + 1;
            }
        }
        else //right side sorted
        {
            if(array[mid] <= key && array[right] >= key) //we can do binary search on the right
            {
                left = mid +1;
            }
            else
            {
                right = mid -1;
            }
        }
    }
    return index;
}
 ```