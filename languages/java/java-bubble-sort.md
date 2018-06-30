# Bubble Sort

### Implementation
```java
private static void bubbleSort(int arr[])
{
    boolean swapped;
    for (int i = 0; i < arr.length - 1; i++)
    {
        swapped = false;
        //highest number will bubble up to the end of the array
        for (int j = 0; j < arr.length - i - 1; j++)
        {
            System.out.println(j);
            if (arr[j] > arr[j + 1])
            {
                // swap arr[j] and arr[j+1]
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
                swapped = true;
            }
        }

        // IF no two elements were
        // swapped by inner loop, then break
        if (swapped == false)
            break;
    }
}
```