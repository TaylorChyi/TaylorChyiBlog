---
title: 遍历map
date: 2023-04-19
tags: 
- Java 
- map 
---

时间：2023-04-18
标签： #Java #map 

---

在 Java 中，遍历 Map 的方式有很多，以下是常见的三种方法：

方法一：使用 keySet()
```java
Map<String, Integer> map = ...; // 假设这是你的Map
for (String key : map.keySet()) {
    Integer value = map.get(key);
    System.out.println("Key: " + key + ", Value: " + value);
}
```
方法二：使用 entrySet()
```java
Map<String, Integer> map = ...; // 假设这是你的Map
for (Map.Entry<String, Integer> entry : map.entrySet()) {
    String key = entry.getKey();
    Integer value = entry.getValue();
    System.out.println("Key: " + key + ", Value: " + value);
}
```
方法三：使用 Java 8 的 forEach() 和 Lambda 表达式
```java
Map<String, Integer> map = ...; // 假设这是你的Map
map.forEach((key, value) -> System.out.println("Key: " + key + ", Value: " + value));
 ```
以上是遍历 Map 的三种常见方法，你可以根据实际情况选择合适的方法。