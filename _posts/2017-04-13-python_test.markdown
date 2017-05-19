---
layout:   post 
title:   "python初体验"
subtitle:  ""
date:       2017-04-13 22:11:00
author:    "Luoyayu"
header-img: "img/post-bg-miui6.jpg"
catalog: true
tags:
    - python
---

### 最近偷学了python，深感python之简洁，优雅。
首先祭上python之禅
>The Zen of Python, by Tim Peters

>Beautiful is better than ugly.  
Explicit is better than implicit.  
Simple is better than complex.  
Complex is better than complicated.  
Flat is better than nested.  
Sparse is better than dense.  
Readability counts.  
Special cases aren't special enough to break the rules.   
Although practicality beats purity.  
Errors should never pass silently.  
Unless explicitly silenced.   
In the face of ambiguity, refuse the temptation to guess.  
There should be one-- and preferably only one --obvious way to d  
Although that way may not be obvious at first unless you're Dutc  
Now is better than never.  
Although never is often better than *right* now.  
If the implementation is hard to explain, it's a bad idea.  
If the implementation is easy to explain, it may be a good idea.  
Namespaces are one honking great idea -- let's do more of those! 

献上用python 写的可以删除烦人的.o/.exe文件

``` python
import os
n = 0
start = input("开始吧(按回车开始)")
for root, dirs, files in os.walk('C:/Users/gavin/Desktop/CodeBack'):
    for name in files:
        if(name.endswith(".o") or name.endswith(".exe") ):
            n += 1
            print("Python帮你删除了", n, "个文件")
            os.remove(os.path.join(root, name))

if(n == 0):
    print("没有该类型文件!")
else:
    print("删除完成!")
os.system("pause")

```



