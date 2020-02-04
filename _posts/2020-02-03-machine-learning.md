---
layout: post
title: machine learning
description: 机器学习
---

- NumPy
  - [Numpy](https://www.numpy.org.cn/) 系统是 Python 的一种开源的数组计算扩展，是一个用 python 实现的科学计算包。包括：
  - 1）一个具有矢量算术运算和复杂广播能力的快速且节省空间的多维数组，称为 ndaaray(N-dimensional array object)
  - 2. 用于对于数组数据进行快速运算的标准数学函数， ufunc(universal function object)
  - 3. 用于整合 c/c++和 Fortran 代码的工具包
  - 4）实用的线性代数、傅立叶变换和随机数生成函数，numpy 和稀疏矩阵运算包 scipy 配合使用更加方便。
- 建立 Ndarray 多维数组

```
    np.array(
        [
            [
            [1,2,3,4],
            [2,3,4,5],
        ],
        [
            [1,2,3,4],
            [2,3,4,5],
        ]
        ]
    )
```
- ndarray的常见创建方式
    - array函数：接受一个普通的python序列，转成ndarray
    - zeros函数：创建指定长度或形状的全零数组
    - ones函数：创建指定长度或形状的全1的数组
    - empty函数：创建一个没有任何具体值的数组（准确地说是一些未初始化的垃圾值）
    - arrange函数：类似于python的range函数，通过指定开始值、终值和元素个数来创建一维数组，可以通过endpoint关键字指定是否包括终值、缺省设置是包括终值
    - logspace函数：和linespace类似，不过它创建等比数列
    - 使用随机数填充数组，即使用numpy.random模块的random()函数，数组所包含的元素数量由参数决定
    - random函数：生成随机数，numpy.random.random((2,3,4),dtype=numpy.int),生成每一位随机数的方法：numpy.random.random_sample();
- numpy中的数据类型
    - 创建NumPy数组时可以通过dtype属性显式指定数据类型，如果不指定，NumPy会自己推断出合适的数据类型，所以一般无需显式指定
    - astype方法，可以转换数组的元素数据类型，得到一个新数组
    - reshape:改变array形状，形状可变，总数不变，得到的是原数组的一个视图
- NumPy基本操作
    - 数组与标量、数组之间的运算
        - 数组不用循环即可对每个元素执行批量运算，这通常就叫矢量化，即用数组表达式代替循环的做法
        - 矢量化数组运算性能要比纯python方式快上一两个数量级
        - 大小相等的数组之间的任何算术运算都会将运算应用到元素级
    - 元素级运算
        - 加、减、乘、除、幂运算等都可以用于数组与标量、大小行等数组之间
        - 在NumPy中，大小相等的数组之间运算，为元素级运算，即只用于位置相同的元素之间，所得到的运算结果组成一个新的数组，运算结果的位置跟操作数位置相同
    - transpace函数用于数组转置
    - 通用函数：快速的元素级数组函数
        - ufunc: 一种对ndarray中的数据执行元素级运算的函数，也可以看作是简单函数（接受一个或多个标量值，并产生一个或多个标量值）的矢量化包装器
    - numpy.where(表达式数组，为true的数组，为false的数组)实现数据的过滤操作，是三元表达式x if condition else y的矢量化版本
    - numpy.unique 取出数组的非重复值
    - 数组数据文件的读写：
        - 将数组以二进制格式保存到磁盘
            - numpy.save(文件名，数组) 写 #将多维数组存储到文件，自动添加后缀.npy(二进制文件))   
            - numpy.load(文件名)读 #需要设置文件后缀
        - 存取文本文件
            - 1.读取数据 numpy.loadtxt(文件名，数据类型，注释行的符号定义，delimiter='' 分隔符)
            numpy.genfromtxt('',delimiter='')类似于loadtxt
            - 2.写入文件
                numpy.savetxt()#如果数组是二维以上的必须要转换为二维数组才能转换
- [pandas](https://pandas.pydata.org/)
    - pandas数据结构
        - Series:一种类似于一维数组的对象，它是由一组数据（各种numpy数据类型）以及一组与之相关的数据标签（即索引）组成，仅由一组数据即可产生简单的series
            - 通过一维数组创建Series
            - 通过字典的方式创建Series
            - Series应用numpy数组运算
            - Series缺失值检测
            - Series自动对齐
            - Series及其索引的name属性
        - DataFrame:一个表格的数据结构，含有一组有序的列，每列可以是不同的值类型（数值、字符串、布尔值等），DataFrame即有行索引也有列索引，可以被看作是由series组成的字典
            - 通过二维数组创建DataFrame
            - 通过字典的方式创建DataFrame
            - 索引对象
            
    
    

