```java
Iterator<Integer> keyIterator = treeMap.keySet().iterator();

while(keyIterator.hasNext()){
	Integer key = keyIterator.next();
	System.out.prinln("Schlüssel" + key);
}
```
## Traversierung mit Streams
```java
treeMap.forEach((key, value) -> System.out.println("Schlüssel:" + key + ", Wert: " + value))
```
