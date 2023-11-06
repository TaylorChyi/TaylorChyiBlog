---
title: WeakHashMap 简介
date: 2023-04-28
tags: 
- Java 
- WeakHashMap 
- 数据结构
---

时间：2023-04-27
标签： #Java #WeakHashMap #数据结构

---

WeakHashMap 是 Java 集合框架中的一种特殊类型的 Map，其键（Key）是弱引用。它与常规 HashMap 的主要区别在于，当 WeakHashMap 中的键不再被其他地方引用时，这些键及其对应的值可以被垃圾回收器自动回收。这种特性使得 WeakHashMap 在处理具有短暂生命周期的键时非常有用。

以下是 WeakHashMap 的一些特点：

1. 弱引用键：WeakHashMap 的键被封装为弱引用。当这些键不再被其他地方强引用时，它们可以被垃圾回收器回收。这有助于避免因长时间保留不再使用的对象而导致的内存泄漏。

2. 自动清理：当垃圾回收器回收了 WeakHashMap 中的键时，与这些键关联的值也会从 Map 中移除。这样，WeakHashMap 可以在不影响其他应用程序功能的情况下自动清理不再使用的数据。

3. 用途：WeakHashMap 通常用于实现缓存、注册表等，这些场景下键的生命周期可能较短，且不再使用的键应该被垃圾回收器回收。

需要注意的是，WeakHashMap 不适用于那些需要长时间保留键值对的场景，因为垃圾回收器可能会在任何时候回收键。在这种情况下，应使用其他类型的 Map，如 HashMap 或 LinkedHashMap。

示例：

```java
import java.util.WeakHashMap;

public class WeakHashMapExample {
    public static void main(String[] args) {
        WeakHashMap<String, String> weakMap = new WeakHashMap<>();
        String key = new String("WeakKey");
        weakMap.put(key, "WeakValue");

        System.out.println("WeakHashMap before GC: " + weakMap);
        key = null; // Remove the strong reference to the key
        System.gc(); // Request garbage collection

        // Wait for a short period to let GC complete
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        System.out.println("WeakHashMap after GC: " + weakMap);
    }
}
```

输出：
```
WeakHashMap before GC: {WeakKey=WeakValue}
WeakHashMap after GC: {}
```

在这个例子中，在请求垃圾回收并移除对键的强引用后，WeakHashMap 中的键值对被自动清除。