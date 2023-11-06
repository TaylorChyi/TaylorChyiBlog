---
title: 「dictionary」和「python package」的区别
date: 2023-04-28
tags: 
- python 
- dictionary 
- package
---

时间：2023-04-26
标签： #python #dictionary #package

---


# 简论

在 pycharm 中新建 python package 文件 下会有一个空的 \_\_init\_\_.py 文件，而 dictionary 文件没有。

<!--more--> 

# dictionary

dictionary 在pycharm 中就是一个普通的文件夹，用于划分项目内部各文件间关系。

# python package

对于 python package 文件夹而言，其会额外自动创建 \_\_init\_\_.py 文件。简单来说，python package 就是一个目录，其中包含一组模块和个 \_\_init\_\_.py 文件
## \_\_init\_\_.py

该文件是 python package的唯一标识， 如果删除 \_\_init\_\_.py 文件，则python package会变成 dictionary。

## 包的导入

python 中包和模块有两种导入包方式：精确导入 和 模糊导入。

例如：在function 文件夹下，func.py 中有 func1()，func2()，func3() 三个方法。

**精准导入**:

``` python 
from function.func import func1,func2
```

**模糊导入**:

 ``` python
 from function.func import *
 ```



# 引用

>   https://blog.csdn.net/weixin_44250149/article/details/102909411