# 概述

## 2.1 编译器

typescript 编译过程:

TS
------------------

> 1.typescript源码 -> typescript AST(abstract syntax tree, AST抽象语法树)

> 2.类型检查器检查AST

> 3.typescript AST -> javascript源码

JS
------------------

> 4.javascript源码 -> javascript AST

> 5.AST -> 字节码

> 6.运行时计算字节码

## 2.2 类型系统
类型检查器：程序分配类型时使用的一系列规则

类型系统两种： 

1.显式句法告诉编译器所有值类型

2.自动推导值的类型

## 2.3代码编辑器设置


```
初始化一个新的npm项目
npm init

'