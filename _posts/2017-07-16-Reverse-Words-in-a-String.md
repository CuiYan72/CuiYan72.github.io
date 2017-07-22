---
layout: post
section-type: post
title: LEETCODE-String与StringBuilder
category: tech
tags: [ 'tutorial' ]
---
#### 提交的代码
```
public class Solution {
    public String reverseWords(String s) {
        String words[] = s.split(" ");
        StringBuilder res = new StringBuilder();
        for(String word:words){
            res.append(new StringBuilder(word).reverse()+" ");
        }
        return res.toString().trim();
    }
}
```
#### 核心知识点
##### 1. split() 
##### 定义： 用于把一个字符串分割成字符串数组。
##### 语法：*stringObject.split(separator,howmany)*
##### separator 必需。字符串或正则表达式，从该参数指定的地方分割stringObject。
##### howmany   可选。该参数可指定返回的数组的最大长度。
##### 返回值：一个字符串数组。该数组是通过在*separator*指定的边界处将字符串stringObject分割成子串创建的。返回的数组中的字符串不包括*separator*自身。
##### 2. trim()
##### 定义：去掉字符串首尾的空格。
##### 3. StringBuilder类
##### 常用方法：(1) reverse() (2) toString() (3)append() (4)console.writeLine() 
##### String对象是不可改变的。每次使用 System.String类中的方法之一时，都要在内存中创建一个新的字符串对象，这就需要为该新对象分配新的空间。在需要对字符串执行重复修改的情况下，这种做法就会耗费资源。如果要修改字符串而不创建新的对象，则可以使用System.Text.StringBuilder类。例如，当在一个循环中将许多字符串连接在一起时，使用 StringBuilder类可以提升性能，使用这个类所产生的对象默认会有16个字符的长度，也可以自行指定初始长度。如果附加的字符超出可容纳的长度，则StringBuilder对象会自动增加长度以容纳被附加的字符。
##### 4. for(String word: words)
##### 伪代码：从words数组中遍历每一个word 
