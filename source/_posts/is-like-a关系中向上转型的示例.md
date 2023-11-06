---
title: is-like-a关系中向上转型的示例
date: 2023-04-16
tags: 
- Java 
- 多态 
- 向上转型 
- is-like-a关系 
---

时间：2023-04-14
标签： #Java #多态 #向上转型 #is-like-a关系 

---
假设我们有一个基类 Animal 和两个子类 Dog 和 Bird。其中，Dog 类扩展了 Animal 类并添加了一个新方法 `bark()`，Bird 类也扩展了 Animal 类并添加了一个新方法 `fly()`。
```java
class Animal {
    public void eat() {
        System.out.println("Animal is eating.");
    }
}

class Dog extends Animal {
    @Override
    public void eat() {
        System.out.println("Dog is eating.");
    }

    public void bark() {
        System.out.println("Dog is barking.");
    }
}

class Bird extends Animal {
    @Override
    public void eat() {
        System.out.println("Bird is eating.");
    }

    public void fly() {
        System.out.println("Bird is flying.");
    }
}
```

现在假设我们有一个方法 `makeAnimalEat`，这个方法接受一个 Animal 对象，并调用它的 `eat()` 方法。
```java
public static void makeAnimalEat(Animal animal) {
    animal.eat();
}
```
在这个方法中，我们不关心传入对象的具体类型，只要它是 Animal 或其子类即可。现在，我们可以创建 Dog 和 Bird 对象，并将它们向上转型为 Animal 类型，传递给 `makeAnimalEat` 方法。
```java
Dog dog = new Dog();
Bird bird = new Bird();

makeAnimalEat(dog); // 向上转型为Animal
makeAnimalEat(bird); // 向上转型为Animal
```
在这个例子中，向上转型允许我们将Dog和Bird对象视为Animal对象，并通过`makeAnimalEat`方法调用它们的`eat()`方法。然而，这也意味着我们不能在`makeAnimalEat`方法中直接调用Dog的`bark()`方法或Bird的`fly()`方法，因为这些方法不属于Animal类的接口。

在某些情况下，我们可能需要在 `makeAnimalEat` 方法中根据传入对象的确切类型执行一些特定操作。例如，我们希望让 Dog 在吃东西之前先叫一下。为了实现这个功能，我们需要重新确定对象的类型，然后调用相应的扩展方法。
```java
public static void makeAnimalEat(Animal animal) {
    if (animal instanceof Dog) {
        ((Dog) animal).bark();
    }
    animal.eat();
}
```
在这个例子中，我们使用`instanceof`操作符检查对象是否为Dog类型，如果是，则向下转型并调用`bark()`方法。注意，这种类型检查和向下转型的操作会降低代码的灵活性，并可能导致不易维护的代码。但在某些情况下，这种方法可能是必要的。