---
layout: post
section-type: post
title: collection 持续更新中
category: tech
tags: [ 'tutorial' ]
---
![]({{site.url}}/img/blog/collection.png)

### 集合框架

#### 1. List结构的集合类：ArrayList，LinkedList，Vector，Stack
#### 2. Map结构的集合类：HashMap,Hashtable
#### 3. Set结构的集合类：HashSet,TreeSet
#### 4. Queue结构的集合类：Queue接口

  *List*,它以特定的顺序保存一组元素；*Set*,元素不能重复；*Queue*，只允许在容器的“一端”插入对象，并从另一端移除对象；*Map*保存两个对象，即键和与之相关联的值。

*ArrayList*插入的元素放在后面;*Stack*插入的元素放在前面;*LinkedList*各种Queue以及栈的行为，由它提供支持。例如：```addFirst()```    ```addLast()```可以指定元素是从前面插入还是从后面插入。 *Queue*是一个典型的先进先出的容器。

### HashSet

集合可以用来删除数组中重复的元素

```
HashSet<Integer> set = new HashSet();
for (int arr:array){
	set.add(arr);
}
```
*Object为泛型，集合里面的元素可以是任意类型，如Integer,String等*

使用迭代*iterator*进行遍历
```
HashSet<String> set = new HashSet<String>
for(String s:set){
}

```