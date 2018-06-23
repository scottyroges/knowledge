## Maps
Interface: java.util.Map

Implementation:
* java.util.HashMap - implemented as a hash table, and there is no ordering on keys or values
* java.util.TreeMap - implemented based on red-black tree structure, and it is ordered by the key
* java.util.LinkedHashMap - preserves the insertion order
* java.util.HashTable - synchronized, in contrast to HashMap. It has an overhead for synchronization

Example:
```
Map<String, Integer> map = new HashMap<>();

hashMap.put("red", 10);
hashMap.put("black", 15);
hashMap.put("white", 5);
hashMap.put("white", 20);

//print black
System.out.println(hashMap.get("black");

//print size
System.out.println(hashMap.size());
		
//loop HashMap
for (Entry<Dog, Integer> entry : hashMap.entrySet()) 
{
	System.out.println(entry.getKey().toString() + " - " + 
	entry.getValue());
}
```

