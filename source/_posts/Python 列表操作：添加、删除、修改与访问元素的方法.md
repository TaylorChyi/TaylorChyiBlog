---
title: Python 列表操作：添加、删除、修改与访问元素的方法
date: 2023-04-23
tags: 
- Python 
- 列表 
- 添加 
- 删除 
- 修改 
- 访问
---

时间：2023-04-22
标签： #Python #列表 #添加 #删除 #修改 #访问

---

Python 的列表（list）是一种可变、有序的数据结构，常用于存储和操作一系列相关数据。在本文中，我们将介绍如何在 Python 中对列表执行添加、删除、修改和访问元素的操作。

**1. 添加元素**

在 Python 中，可以使用以下方法将元素添加到列表：

* `append()`: 在列表末尾添加一个元素。

示例：

```python
fruits = ["apple", "banana"]
fruits.append("orange")
print(fruits)
```

输出：

```
["apple", "banana", "orange"]
```

* `insert()`: 在列表指定位置插入一个元素。接受两个参数：插入位置的索引和要插入的元素。

示例：

```python
fruits = ["apple", "banana"]
fruits.insert(1, "orange")
print(fruits)
```

输出：

```
["apple", "orange", "banana"]
```

* `extend()`: 将一个列表（或其他可迭代对象）的所有元素添加到另一个列表的末尾。

示例：

```python
fruits = ["apple", "banana"]
more_fruits = ["orange", "grape"]
fruits.extend(more_fruits)
print(fruits)
```

输出：

```
["apple", "banana", "orange", "grape"]
```

**2. 删除元素**

在 Python 中，可以使用以下方法从列表中删除元素：

* `remove()`: 删除列表中第一个匹配的元素。如果元素不存在，则抛出 ValueError。

示例：

```python
fruits = ["apple", "banana", "orange"]
fruits.remove("banana")
print(fruits)
```

输出：

```
["apple", "orange"]
```

* `pop()`: 删除并返回列表中指定索引处的元素。如果未提供索引，则删除并返回列表中的最后一个元素。

示例：

```python
fruits = ["apple", "banana", "orange"]
fruit = fruits.pop(1)
print(fruits)
print("Removed:", fruit)
```

输出：

```
["apple", "orange"]
Removed: banana
```

* `del` 语句：删除列表中的一个或多个元素。

示例：

```python
fruits = ["apple", "banana", "orange"]
del fruits[1]
print(fruits)
```

输出：

```
["apple", "orange"]
```

**3. 修改元素**

要修改列表中的元素，可以使用索引直接为其分配一个新值。

示例：

```python
fruits = ["apple", "banana", "orange"]
fruits[1] = "grape"
print(fruits)
```

输出：

```
["apple", "grape", "orange"]
```

**4. 访问元素**

要访问列表中的元素，可以使用索引。正索引从 0 开始，负索引从 -1 开始。

示例：

```python
fruits = ["apple", "banana", "orange"]
print(fruits[1])
print(fruits[-1])
