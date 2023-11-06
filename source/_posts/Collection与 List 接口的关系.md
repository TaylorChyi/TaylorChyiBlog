---
title: Collection与 List 接口的关系
date: 2023-04-28
tags: 
- Java 
- Collection 
- List 
---

时间：2023-04-25
标签： #Java #Collection #List 

---

1. 集合框架层次结构
   - Java 集合框架 (Collections Framework) 是 Java 标准库的一部分，提供了一套用于存储和操作数据集合的接口和实现类。
   - Collection 接口是 Java 集合框架的基础接口，所有的集合类都实现了这个接口。
   - List、Set 和 Queue 都是 Collection 的子接口，它们提供了各自特定的数据存储和操作方法。

2. Collection 接口
   - Collection 接口是集合框架的根接口，定义了一组通用的集合操作方法，如 add ()、remove ()、contains ()、isEmpty ()、size ()、iterator () 等。
   - Collection 接口不提供具体的数据结构，而是通过它的子接口和实现类来实现各种数据结构，如 List、Set、Queue 等。

3. List 接口
   - List 接口是一个有序集合，允许存储重复的元素。
   - List 接口继承了 Collection 接口，所以它具有 Collection 接口的所有通用方法。
   - List 接口还提供了一些额外的方法，用于操作有序集合，如 get ()、set ()、indexOf ()、lastIndexOf ()、subList () 等。
   - List 接口的实现类有 ArrayList、LinkedList、Vector 和 Stack 等。

4. Collection 与 List 的关系
   - List 接口是 Collection 接口的一个子接口，它继承了 Collection 提供的通用方法。
   - List 接口添加了额外的方法，用于操作有序集合，这些方法使得 List 更适合于有序集合的场景。
   - 通过实现 List 接口，具体的实现类如 ArrayList、LinkedList 等能够同时具备通用集合操作和有序集合操作的特性。

总结：Collection 接口是 Java 集合框架的基础接口，定义了一组通用的集合操作方法。List 接口是 Collection 的子接口，它继承了 Collection 的方法，并添加了额外的方法以支持有序集合的操作。具体的实现类如 ArrayList、LinkedList 等实现了 List 接口，从而具备了通用集合操作和有序集合操作的特性。