# Sets
Interface: java.util.Set

Implementation:
* HashSet - quick operations, but the results are unordered
* LinkedHashSet - matches the speed of HashSet, but keeps set in insertion order
* TreeSet - Slower operations (O(logN)), but keeps values sorted

Example:
```
// We create a new, empty set
Set mySet1 = new HashSet();
// We add a few elements
mySet1.add("A");
mySet1.add("C");
mySet1.add("A");
mySet1.add("B");
// Print the elements of the Set
System.out.println("mySet1: " + mySet1);

// Now we will remove one element from mySet2 and compare again
mySet1.remove("A");
System.out.println("mySet1: " + mySet1);

// Use of Iterator in Set
Iterator iterator = mySet1.iterator();
while (iterator.hasNext()) {
    System.out.println("Iterator loop: " + iterator.next());
}

// Use of for-each in Set
for (String str : mySet1) {
    System.out.println("for-each loop: " + str);
}

// Clearing all the elements
mySet1.clear();
System.out.println("mySet1 is Empty: " + mySet1.isEmpty());

// Checking the number of elements
System.out.println("mySet1 has: " + mySet1.size() + " Elements");

// Creating an Array with the contents of the set
String[] array = mySet2.toArray(new String[mySet2.size()]);
System.out.println("The array:" + Arrays.toString(array));
```
