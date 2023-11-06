---
title: Stream. Generate 的作用
date: 2023-04-28
tags: 
- Java 
- Stream 
- Streamgenerate
---

时间：2023-04-28
标签： #Java #Stream #Streamgenerate

---

Stream. Generate 是 Java 8 引入的 Stream API 中的一个方法，作用是生成一个无限长的流（Stream）对象。这个方法接收一个供给型函数（Supplier），该函数不接收任何参数，每次调用返回一个新的值。Stream. Generate 方法会不断调用该供给型函数以生成元素，直到显式限制流的长度。

具体来说，`Stream.generate(Supplier<T> s)` 方法的作用是生成一个包含无限个元素的流。每个元素的值由传入的 Supplier 函数提供。由于 Stream 为惰性求值，只有在调用终止操作时才会实际求值。

使用 Stream. Generate 的一个例子：```
java
import java.util.stream.Stream;

public class StreamGenerateExample {
    public static void main(String[] args) {
        // 使用Stream.generate生成一个无限流，每个元素都是1
        Stream<Integer> stream = Stream.generate(() -> 1);

        // 使用limit方法限制流长度，然后使用forEach打印前10个元素
        stream.limit(10).forEach(System.out::println);
    }
}
```

在这个例子中，我们使用Stream.generate生成一个每个元素都是1的无限流。然后我们使用limit方法限制流的长度为10，最后使用forEach打印前10个元素。