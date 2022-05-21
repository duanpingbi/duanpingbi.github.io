---
layout: post
title: typescript
description: typescript
---

### 为什么要使用typescript
javascript 是一门动态弱类型的语言，对变量的类型十分宽容，而且不会在这些变量和他们的调用者之间建立契约，对javascript类型进行静态检查

- typescript 更像是一门工具而不是一门语言，
  - 1. 类型检查，typescript会在编译时进行严格的静态类型检查，这意味着可以在编码的阶段发现可能存在的隐患
  - 2. 语言扩展
  - 3. 工具属性，typescript 可以编译成标准的javascript 可以在任何浏览器和操作系统

  - 4. typescript 可以帮助团队重塑“类型思维”

  ## 强类型语言和弱类型语言
  - 强类型语言： 不允许改变变量的数据类型，除非进行强制类型转换
  - 弱类型语言：变量可以被赋予不同的数据类型

https://juejin.cn/post/6999985372440559624

##  type 和 interface 的区别
- type可以为任何类型引入名称，例如基本类型，联合类型等， 不支持继承，不会创建一个真正的名字，无法实现（implements），重名编译器会抛错误
- interface：可以被派生类型实现，重名时会合并

## commonJs 跟 esmodule 区别？
- commonJs输出的是值的拷贝，运行时加载，require()同步加载
- esmodle 输出的是值的引用，编译输出接口，import 异步加载，有一个独立的模块依赖的解析过程





  