---
title: Set<Integer> 转换为一个 int 数组
date: 2023-04-19
tags: 
- Java 
- Set 
- 数组 
---

时间：2023-04-18
标签： #Java #Set #数组 

---

如果你想将一个 `Set<Integer>` 转换为一个 `int[]` 数组，你可以使用以下方法：
```java
import java.util.Set;
import java.util.HashSet;
import java.util.stream.IntStream;

public class Main {
    public static void main(String[] args) {
        // 创建一个 Set<Integer>
        Set<Integer> set = new HashSet<>();
        set.add(1);
        set.add(2);
        set.add(3);

        // 将 Set<Integer> 转换为 int[]
        int[] intArray = set.stream().mapToInt(Integer::intValue).toArray();

        // 打印结果
        for (int num : intArray) {
            System.out.println(num);
        }
    }
}
```
这里我们使用 Java 8 引入的 Stream API。首先，我们通过调用 `set.stream()` 获取一个 `Stream<Integer>`，然后使用 `mapToInt()` 方法将每个 `Integer` 对象转换为对应的基本类型 `int`。最后，我们调用 `toArray()` 方法将流转换为 `int[]` 数组。