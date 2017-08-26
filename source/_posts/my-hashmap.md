---
title: 自己动手实现一个HashMap
date: 2017-08-26 17:30:39
tags:
copyright: true
---
# 1. 前言
HashMap作为java数据结构中重要的一员，同时拥有高效的查询和插入的优点。近期在做项目的时候我也是领略到了hashmap的强大之处，hashmap为前后台数据的交互提供了非常高的可扩展性和灵活性。键值对的数据结构也天然对json字符串的转换提供良好的支持。这篇文章主要分析HashMap的原理，以及如何自己实现一个HashMap。
<!--more-->

# 2. HashMap的原理
## 2.1 什么是HashMap？
基于哈希表的 Map 接口的实现。此实现提供所有可选的映射操作，并允许使用 null 值和 null 键。（除了非同步和允许使用 null 之外，HashMap 类与 Hashtable 大致相同。）此类不保证映射的顺序，特别是它不保证该顺序恒久不变 ——摘自百度百科。
## 2.2 什么是Hash
Hash是一种算法，能将一个任意长度的二进制值通过一个映射关系转换成一个固定长度的二进制值。在HashMap中，哈希算法主要是用于根据key的值算出存放数组的index值。HashMap中的存储都是根据key的哈希值有关的。
哈希算法又被称为散列的过程，那么什么是散列呢？散列即把数据均匀的存放到数组中的各个位置，从而尽量避免出现多个数据存放在一块区间内。 
		
优秀的哈希算法应该具备以下两点：
- 保证散列值非常均匀
- 保证冲突极少出现
		
哈希函数有很多种，在这里我以除留取余法（取模）为例，首先定义一个数组的长度，假设为16。那么此时的索引为key摸于m，m的取值规则是比数组长度小的最大质数。在这个情况下m为13。由于这种算法会导致这样的情况出现，即不同的key经过哈希运算之后得到了一样的index，如key为2和15的index值都为2，那么此时就需要我们处理冲突了。
		
Ps. JDK中的hash算法远比这个复杂，在这里我仅仅只是举一个例子方便读者理解。

## 2.3 处理冲突
- 线性探测法
当冲突产生时，查找下一个索引是否被占用，如果没有，则把数据存到该索引上。
- 链表形式
由于在HashMap中，单个数据是以entry的形式存储的，而entry中包含了key，value和next指针。那么当冲突产生时，我们就把原先存放到这个位置的数据取出来，然后在这个位置存放新的数据，并且把新数据的next指针设为原数据，也就是说链表头位置的数据永远是最新的数据。

# 3. 实现自己的HashMap
To be continued...

***
