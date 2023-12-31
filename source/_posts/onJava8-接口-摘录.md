---
title: onJava8-接口-摘录
date: 2023-04-19
tags: 
- java 
- 接口 
- 摘录 
---

时间：2023-04-18
标签： #java #接口 #摘录 

---

一个接口表示 ：所有实现了该接口的类看起来都像这样。因此，任何使用某特定接口的代码都知道可以调用该接口的哪些方法，而且仅需知道这些。所以，接口被用来建立类之间的协议。

接口同样可以包含属性，这些属性被隐式指明为 **static** 和 **final**。

方法签名包括方法名和参数类型 -- 返回类型不算在方法签名里。

Java 8 允许在接口中添加静态方法。这么做能恰当地把工具功能置于接口中，从而操作接口，或者成为通用的工具

有一条实际经验：尽可能地抽象。因此，更倾向使用接口而不是抽象类。只有当必要时才使用抽象类。除非必须使用，否则不要用接口和抽象类。大多数时候，普通类已经做得很好，如果不行的话，再移动到接口或抽象类中。

使用接口的核心原因之一：为了能够向上转型为多个基类型（以及由此带来的灵活性）。然而，使用接口的第二个原因与使用抽象基类相同：防止客户端程序员创建这个类的对象，确保这仅仅只是一个接口。这带来了一个问题：应该使用接口还是抽象类呢？如果创建不带任何方法定义或成员变量的基类，就选择接口而不是抽象类。事实上，如果知道某事物是一个基类，可以考虑用接口实现它

认为接口是好的选择，从而使用接口不用具体类，这具有诱惑性。几乎任何时候，创建类都可以替代为创建一个接口和工厂。

很多人都掉进了这个陷阱，只要有可能就创建接口和工厂。这种逻辑看起来像是可能会使用不同的实现，所以总是添加这种抽象性。==这变成了一种过早的设计优化==。

任何抽象性都应该是由真正的需求驱动的。当有必要时才应该使用接口进行重构，而不是到处添加额外的间接层，从而带来额外的复杂性。这种复杂性非常显著，如果你让某人去处理这种复杂性，只是因为你意识到“以防万一”而添加新接口，而没有其他具有说服力的原因——好吧，如果我碰上了这种设计，就会质疑此人所作的所有其他设计了。

恰当的原则是优先使用类而不是接口。从类开始，如果使用接口的必要性变得很明确，那么就重构。接口是一个伟大的工具，但它们容易被滥用。