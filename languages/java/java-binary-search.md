# Binary Search
Implementation:
```java
public static Integer BinarySearchIterative(int[] array, int value){
		int start = 0;
		int end = array.length - 1;
		int middle = (end - start)/2 + start;
		
		while(start <= end){
			if(array[middle] == value){
				return middle;
			} else if(array[middle] > value){
				end = middle - 1;
			} else {
				start = middle + 1;
			}
			middle = (end - start)/2 + start;
		}
		return null;
	}
```