---
title: XML
date: 10 Jun 2022 00:15
tags:
- xml
---



# XML的用途

由于语言的不同，在数据的传输上需要一种统一的格式来减少在不同语言间传递的不便。

例如，天气信息是由国家气象局发布的而非是某个个人网站所能预测的，也因此，为了满足不同需求的网站对于天气信息的需要，国家气象局发布的天禧信息即是xml格式的，这种格式可以使其在不同语言中都可以被理解。

那为什么不直接用txt文件呢？我想主要是对于格式的明确，即，每个信息的含义是什么作出统一的解释，方便不同语言直接对于所需要的信息的tag进行定位索取，而不用读取整个文件然后数第几行是XXX属性再传入赋值给变量。



# XML是什么

XML is External Markup Language

XML是用于传输和储存数据所用

XML必须是自定义的，没有官方标签，一定要有含义，就像是起变量名一样。



# XML 规则

文件中有且仅有一个根标签，其余所有的数据都要包含在这个根标签中。

根标签的命名没有硬性要求，但可以选择root作为根节点标签。



# XML HTML 的区别

* XML的标签只能自定义，但是HTML不能自定义；
* HTML语法要求不大严格，XML语法非常严格（必须是成对的标签，否则报错）
* XML用来传输保存数据，HTML用来展示数据



# XML头声明

不强制 可有可无

```xml
<?xml version="1.0" encoding="utf-8" ?>
```

「version」	版本号

「encoding」	编码



# XML特点

* 标签成对
* 大小写敏感
* 特殊字符要使用实体字符，例如，<，要用，\&lt;



# XML注释

和HTML中一样 <!-- -->



# XML属性

属性是用来描述标签的一些额外的信息；

但是由于在XML中，所有的标签都是自定义的，没有必要使用属性来作为展示标签的信息，直接用父子关系来体现甚至就可以了。

同时，在解析xml时，属性的解析会带来额外的解析步骤；



# CDATA

用于注明其包含的所有数据都不需要被解析

语法如下所示

```xml 
<![CDATA[ all of the contents will not be analized ]]>
```

故，在特殊字符较少时，可以是用实体字符替换；对于段落较长时，可以用CDATA标注；

同时，CDATA一定要大写



# XML 解析原理

1. 读区xml文件到内存；
2. 形成dom树；
3. 由dom树生成对象并返回；



# XPath 用途

专门用来查找XML数据内容的一门语言

# XPath 用法

用dom树的路径来作为查找参数，简洁了代码语句；

如上述使用方法所示，其返回的结果不一定只有一个标签的值，有可能有多个同名的兄妹标签

路径参数可以是绝对路径也可以是相对路径，同时，也可以使用*，[xxx]来进行全选或有条件的检索；

@xxx 用以表示标签的属性

![Screenshot 2022-06-10 at 01.50.57](/Users/taylor/Library/Application Support/typora-user-images/Screenshot 2022-06-10 at 01.50.57.png)




