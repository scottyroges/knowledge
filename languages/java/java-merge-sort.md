# MergeSort
## Example Usage:
Arrays.sort uses MergeSort for objects that implement Comparable
```java
java.util.Arrays.sort(Comparable[] a);
```

## Custom Implementation
### Recursive
Things to Remember:
* left to middle and middle + 1 to right
```java
public static int[] mergeSort(int[] arr, int left, int right)
{
    if(right > left)
    {
        int middle = (left + right)/2;

        int[] a = mergeSort(arr, left, middle);
        int[] b = mergeSort(arr, middle + 1, right);

        return merge(a, b);
    }
    else
    {
        return new int[]{arr[left]};
    }
}

private static int[] merge(int[] a, int[] b)
{

    int[] r = new int[a.length + b.length];
    int i = 0;
    int j = 0;
    int x = 0;

    while(i < a.length && j < b.length)
    {
        if(a[i] > b[j])
        {
            r[x++] = b[j++];
        }
        else
        {
            r[x++] = a[i++];
        }
    }

    //remaining in a
    while(i < a.length)
    {
        r[x++] = a[i++];
    }

    //remaining in b
    while(j < b.length )
    {
        r[x++] = b[j++];
    }

    return r;
}
```
