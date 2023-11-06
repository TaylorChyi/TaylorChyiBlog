---
title: 在 Java 中, Collection 类和 ArrayList 之间的关系
date: 2023-04-28
tags: 
- Java 
- Collection 
- ArrayList
---

时间：2023-04-25
标签： #Java #Collection #ArrayList

---

1. 集合框架层次结构
   - Java 集合框架 (Collections Framework) 是 Java 标准库的一部分，提供了一套用于存储和操作数据集合的接口和实现类。
   - Collection 接口是 Java 集合框架的基础接口，所有的集合类都实现了这个接口。
   - List、Set 和 Queue 都是 Collection 的子接口，它们提供了各自特定的数据存储和操作方法。
   - ArrayList 是 List 接口的一个实现类，是一个动态数组，可以自动调整大小。

2. ArrayList 的特点
   - ArrayList 是一个可变大小的数组，提供了灵活的插入、删除和查找操作。
   - ArrayList 是基于索引的数据结构，访问元素的时间复杂度是 O (1)。
   - ArrayList 的插入和删除操作可能需要移动数组中的元素，因此它们的时间复杂度可能是 O (n)。
   - ArrayList 是非线程安全的，如果需要在多线程环境下使用，可以考虑使用 Collections.SynchronizedList () 方法来包装它，或者使用线程安全的实现类，如 java. Util. Concurrent. CopyOnWriteArrayList。

3. Collection 和 ArrayList 的关系
   - ArrayList 是实现了 Collection 接口的一个具体类，它继承了 Collection 提供的通用方法，如 add ()、remove ()、contains () 等。
   - 通过实现 List 接口，ArrayList 还提供了额外的方法，如 get ()、set ()、indexOf () 等，这些方法使得 ArrayList 更适合于顺序访问和随机访问的场景。
   - 由于 ArrayList 是一个 Collection 实现类，您可以将其作为一个普通的 Collection 对象来使用，这样可以提高代码的通用性和可扩展性。

总结：Collection 是 Java 集合框架中的一个基础接口，而 ArrayList 是实现了 Collection 和 List 接口的一个具体类。ArrayList 继承了 Collection 的方法，并添加了额外的 List 方法，使其成为一个功能丰富且灵活的数据结构。