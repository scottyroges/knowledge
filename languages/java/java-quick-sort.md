# QuickSort
## Example Usage:
Arrays.sort uses QuickSort for primitives
```java
java.util.Arrays.sort(int[] a);
```

## Custom Implementation
### Recursive
Things to Remember:
* partition can pick any pivot, but that pivot should be move to the end to start
* partion can us two pointers at opposite ends of each other or two pointers on the same side but opposite the pivot

Implementation
```java
private static void quickSort(int[] arr, int left, int right)
{
    if(left < right)
    {
        int p = partitionTwoPointers(arr, left, right);
        quickSort(arr, left, p - 1);
        quickSort(arr, p + 1, right);
    }
}

private static int partitionTwoPointers(int[] arr, int left, int right)
{
    int pivot = arr[right];
    int leftPointer = left;
    int rightPointer = right - 1;

    while(leftPointer <= rightPointer)
    {
        if(arr[leftPointer] > pivot && arr[rightPointer] < pivot)
        {
            swap(arr, leftPointer, rightPointer);
        }
        else
        {

            if (arr[leftPointer] <= pivot) {
                leftPointer++;
            }

            if (arr[rightPointer] >= pivot) {
                rightPointer--;
            }
        }
    }

    swap(arr, leftPointer, right);
    return leftPointer;
}

private static int partitionRight(int[] arr, int left, int right)
{
    int partitionIndex = right;
    int pivot = arr[partitionIndex];
    System.out.println(pivot);
    int i = left - 1;

    for(int j = left; j < right; j++)
    {
        if(arr[j] <= pivot)
        {
            i++;
            swap(arr, i, j);
        }
        printArray(arr);
    }

    i++;
    swap(arr, i, partitionIndex);
    return i;
}

private static int partitionLeft(int[] arr, int left, int right)
{
    int partitionIndex = left;
    int pivot = arr[partitionIndex];
    System.out.println(pivot);
    int i = right + 1;

    for(int j = right; j > left; j--)
    {
        if(arr[j] >= pivot)
        {
            i--;
            swap(arr, i, j);
        }
        printArray(arr);
    }

    i--;
    swap(arr, i, partitionIndex);
    return i;
}

private static int partitionMiddle(int[] arr, int left, int right)
{
    int partitionIndex = (right + left) /2;
    int pivot = arr[partitionIndex];

    swap(arr, partitionIndex, right);

    int i = left - 1;


    for(int j = left; j < right; j++)
    {
        if(arr[j] <= pivot)
        {
            i++;
            swap(arr, i, j);
        }
        printArray(arr);
    }

    i++;
    swap(arr, i, right);

    return i;
}

private static void swap(int[] arr, int a, int b)
{
    if(a != b)
    {
        int temp = arr[a];
        arr[a] = arr[b];
        arr[b] = temp;
    }
}
```