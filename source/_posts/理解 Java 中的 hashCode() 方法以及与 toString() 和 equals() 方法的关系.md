---
title: 理解 Java 中的 hashCode() 方法以及与 toString() 和 equals() 方法的关系
date: 2023-04-19
tags: 
- Java 
- hashCode 
- equals 
- toString 
- 对象比较  
- 散列数据结构
---

时间：2023-04-18
标签： #Java #hashCode #equals #toString #对象比较  #散列数据结构

---

>hashCode() 为什么会和 toString equals 方法放在一起，它也很常被重写么，为什么，它的作用是什么

`hashCode()` 方法与 `toString()` 和 `equals()` 方法经常放在一起，因为它们都是 Java 中 `Object` 类的公共方法，通常需要根据实际需求在子类中重写。当您创建自定义类时，重写这些方法可以帮助您更好地处理对象之间的比较、散列存储和调试。

`hashCode()` 的主要作用是为对象提供一个散列值。这个散列值通常用于散列数据结构（例如 `HashMap`、`HashSet`）中，以提高数据存储和检索的性能。当您将对象作为散列数据结构的键时，`hashCode()` 方法就显得非常重要。

`hashCode()` 应该遵循以下约定：

1.  在同一个 Java 应用程序执行期间，对同一个对象多次调用 `hashCode()` 应该返回相同的值。
2.  如果两个对象根据 `equals()` 方法相等，那么它们的 `hashCode()` 应该相等。
3.  如果两个对象根据 `equals()` 方法不相等，它们的 `hashCode()` 不一定要不同。但是，具有不同散列值的对象可能会提高散列数据结构的性能。

因此，当您重写 `equals()` 方法时，通常也需要重写 `hashCode()` 方法，以确保它们的行为一致。这有助于确保您的自定义类在散列数据结构中表现良好。这也是为什么 `hashCode()` 与 `toString()` 和 `equals()` 方法经常放在一起讨论的原因。

以下是一个简单的示例，说明如何重写 `hashCode()` 和 `equals()` 方法：
```java
public class Person {
    private String name;
    private int age;

    // 构造方法、getter 和 setter 省略

    @Override
    public boolean equals(Object obj) {
        if (this == obj) {
            return true;
        }
        if (obj == null || getClass() != obj.getClass()) {
            return false;
        }
        Person person = (Person) obj;
        return age == person.age && name.equals(person.name);
    }

    @Override
    public int hashCode() {
        int result = 17;
        result = 31 * result + name.hashCode();
        result = 31 * result + age;
        return result;
    }
}
```
在这个示例中，我们根据 `Person` 类的 `name` 和 `age` 属性重写了 `equals()` 和 `hashCode()` 方法。这样，当我们将 `Person` 对象作为 `HashMap` 或 `HashSet` 的键时，它们将根据 `name` 和 `age` 属性正确地进行比较和散列。