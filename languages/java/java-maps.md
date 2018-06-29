# Maps
Interface: java.util.Map

Implementation:
* java.util.HashMap - implemented as a hash table, and there is no ordering on keys or values
* java.util.TreeMap - implemented based on red-black tree structure, and it is ordered by the key
* java.util.LinkedHashMap - preserves the insertion order
* java.util.HashTable - synchronized, in contrast to HashMap. It has an overhead for synchronization

Example:
```java
Map<String, Integer> map = new HashMap<>();

map.put("red", 10);
map.get("red"); // 10

map.put("black", 15);
map.get("black"); // 15

map.size(); // 2 (based on keys)

map.put("white", 5);
map.get("white"); // now 5

map.put("white", 20);
map.get("white"); // now 20

map.size(); // still 2

//loop key value entry
for(Entry<Dog, Integer> entry : map.entrySet()) 
{
	entry.getKey();
	entry.getValue();
}

//loop through keys
for(String key : map.keySet())
{
	map.get(key);
}
```

