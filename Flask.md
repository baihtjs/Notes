---
title: Flask
tags: Python,web,flask
grammar_cjkRuby: true
---


# 第一部分 基础篇
## 第一章 初识Flask
   		Flask：瓶子，烧瓶
		
## 第三章 模版

3.2.3过滤器
过滤器的本质就是函数。
使用方式：

过滤器的使用方式为：变量名 | 过滤器。
{{variable | filter_name(*args)}}
如果没有任何参数传给过滤器,则可以把括号省略掉, flask中过滤器支持链式调用
{{variable | filter_name}}
例子：
from flask import Markup
@app.template_filter()
def musical(s):
return s + Markup(' &#9835;')
{{ name|musical }}-----使用


### 3.3 模版结构组织
 3.3.1 局部模版
 局部可重复利用的html片段，如banner，可以插入到别的独立模版
 {% include '_banner.html' %}
  通常使用下划线开头来命名。
  
  3.3.2 宏
  宏macro当于python中的函数，宏代码保存在html文件中。使用时可以引入并调用。
  3.3.3 模版继承
  定义一个基模版，包含网页的导航栏、页脚等通用内容。每一个继承基模版的子模版在渲染时自动包含这部分内容。
  基模版定义：
  {% block scripts %}{% endblock %}
  {% block content %}{% endblock %}
  {% block styles %}{% endblock %}
  {% block head %} {%endblock %}
  
  模版内容追加：{{super()}}
  
  ## 第四章 表单
  ### 创建表单
  from flask_wtf import FlaskForm
from wtforms import StringField, PasswordField,BooleanField,SubmitField
from wtforms.validators import DataRequired,Length
class LoginForm(FlaskForm):
    username = StringField('Username', validators=[DataRequired()])
    password = PasswordField('Password', validators=[DataRequired(), Length(min=8)])
    remember = BooleanField('Remember Me')
    submit = SubmitField('Log in')