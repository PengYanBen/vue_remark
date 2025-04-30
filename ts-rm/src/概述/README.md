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
# 初始化一个新的npm项目
npm init
# 安装TSC TSLint和NodeJsDE 声明类型
npm install --save-dev typescript tslint @types/node
```

## 2.3.1 tsconfig.json

可以使用内置TSC初始化命令生成改文件
```
./node_modules/.bin/tsc --init
```
## 2.3.2 tslint.json
代码制定风格上的约定，可以用以下命令生成
```
./node_modules/.bin/tsc --init
```

## 2.4 index.ts

1.设置好tsconfig.json 和 tslint.json以后新建src文件夹
```
mkdir src
touch src/概述/index.ts
```

2.代码编辑器中打开 src/概述/index.ts，输入typescrpit代码
```
console.log('hello typescript!')
```
3.编译并运行typescript代码
```
# 使用 TSC编译 Typescript

./node_modules/.bin/tsc

# 使用nodejs 运行代码

node ./dist/index.js

```