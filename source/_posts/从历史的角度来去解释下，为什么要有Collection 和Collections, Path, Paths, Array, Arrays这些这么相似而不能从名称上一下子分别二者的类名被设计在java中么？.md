---
title: 从历史的角度来去解释下，为什么要有Collection 和Collections, Path, Paths, Array, Arrays这些这么相似而不能从名称上一下子分别二者的类名被设计在java中么？
date: 2023-04-28
tags: 
- Java 
- Collection 
- Collections 
- Path 
- Paths 
- Array 
- Arrays 
---

时间：2023-04-26
标签： #Java #Collection #Collections #Path #Paths #Array #Arrays 

---

1. Collection 和 Collections
   - Collection 是 Java 集合框架的基础接口，定义了一组通用的集合操作方法。List、Set 和 Queue 都是 Collection 的子接口，它们提供了各自特定的数据存储和操作方法。
   - Collections 是一个工具类，包含了许多静态方法，用于操作集合对象，如排序、查找、同步等。这个类的设计是为了提供一些通用的、与具体实现无关的集合操作方法。
   - 为什么使用相似的名称：Collection 和 Collections 的设计目的是不同的。Collection 是一个接口，用于定义集合操作的通用规范，而 Collections 是一个工具类，用于提供一些集合操作的通用实现。它们之间的关系是互补的，这也是为什么它们的名称如此相似的原因。

2. Path 和 Paths
   - Path 是 Java NIO. 2 的一个接口，表示文件系统中的路径。它提供了许多用于操作路径的方法，如获取文件名、父路径、子路径等。
   - Paths 是一个工具类，包含了一些静态方法，用于创建 Path 对象。例如，Paths.Get () 方法可以根据一个字符串或者 URI 创建一个 Path 对象。
   - 为什么使用相似的名称：Path 和 Paths 的设计目的是不同的。Path 是一个接口，用于定义路径操作的通用规范，而 Paths 是一个工具类，用于创建和操作 Path 对象。它们之间的关系是互补的，这也是为什么它们的名称如此相似的原因。

3. Array 和 Arrays
   - Array 是 Java 反射 API 的一个类，用于动态创建和访问数组对象。它提供了一些方法，如创建数组、获取数组长度、访问数组元素等。
   - Arrays 是一个工具类，包含了许多静态方法，用于操作数组，如排序、查找、比较等。这个类的设计是为了提供一些通用的、与具体实现无关的数组操作方法。
   - 为什么使用相似的名称：Array 和 Arrays 的设计目的是不同的。Array 是一个类，用于动态地创建和访问数组，而 Arrays 是一个工具类，用于提供一些数组操作的通用实现。它们之间的关系是互补的，这也是为什么它们的名称如此相似的原因。