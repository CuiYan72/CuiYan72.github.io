---
layout: post
section-type: post
title: LEETCODE-Reverse Words in a String
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
##### 使用的方法：(1) reverse() (2) toString() 
##### 4. for(String word: words)
##### 伪代码：从words数组中遍历每一个word 
