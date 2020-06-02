---
title: Flask
tags: Python,web,flask
grammar_cjkRuby: true
---


# 第一部分 基础篇
## 第一章 初识Flask
   		Flask：瓶子，烧瓶
		
## 第三章 模版

### 3.3 模版结构组织
 3.3.1 局部模版
 局部可重复利用的html片段，如banner，可以插入到别的独立模版
 {% include '_banner.html' %}
  通常使用下划线开头来命名。
  
  3.3.2 宏
  宏macro当于python中的函数，宏代码保存在html文件中。使用时可以引入并调用。
  3.3.3 模版继承