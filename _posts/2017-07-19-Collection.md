---
layout: post
section-type: post
title: 集合类
category: tech
tags: [ 'tutorial' ]
---
![]({{site.url}}/img/blog/collection.png)

### HashSet

集合可以用来删除数组中重复的元素

```
HashSet<Integer> set = new HashSet();
for (int arr:array){
	set.add(arr);
}
```
*Object为泛型，集合里面的元素可以是任意类型，如Integer,String等*

使用迭代iterator进行遍历
```
HashSet<String> set = new HashSet<String>
for(String s:set){
}

```