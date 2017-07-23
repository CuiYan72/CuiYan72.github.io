---
layout: post
section-type: post
title: 安装jekyll以及从Github上clone博客
category: tech
tags: [ 'tutorial' ]
---

## 安装Jekyll

Windows环境

1.安装Ruby  

官网：http://rubyinstaller.org/downloads/  

测试：Ruby是否安装成功，执行命令 ```ruby -v```  

*注意：勾选 “Add Ruby executables to your PATH”，安装路径不能包含空格！*  

2.安装DevKit  

官网：http://rubyinstaller.org/downloads/  

步骤：cmd中进入到安装目录  

```
ruby dk.rb init
ruby dk.rb install
```  

测试：gem是否安装成功，执行命令  ```gem -v```  

*注意：安装包在页面下方“DEVELOPMENT KIT”处*  

3.安装Jekyll  

步骤：cmd执行以下命令  ```gem install jekyll```  

4.安装Python（这里不做赘述）  

5.Jekyll启动与调试  

步骤：cmd执行以下命令  

```
//创建Jekyll博客文件夹
jekyll new Blog（文件夹名）
//进入到博客文件夹
cd Blog
//开启服务
jekyll serve
```  

*注意：如果出现端口冲突的情况，可以参考《安装 jekyll theme 遇到的问题》这篇博客*  

测试：在本地浏览器中输入127.0.0.1:4000，出现Jekyll静态页面即为部署成功。  

## GitHub博客下载  

1.git 下载  

官网：https://git-scm.com/downloads  

2.进入到本地Git_workspace,右击git bush  

3.复制你想要下载的项目的链接，如图所示：  
![]({{site.url}}/img/blog/gitclone.png)  

4.在命令窗口中输入如下命令：
```
git clone git@github.com:CuiYan72/CuiYan72.github.io.git
```  

5.进入到下载的项目中,右击git bush,在命令窗口中输入如下命令：  
```
git init  
//可以随意创建一个测试文件，注意文件里必须有内容！
git add test.md 
git commit -m "test"  
//第一次提交需要，之后一般可以省略 
git remote add origin git@github.com:CuiYan72/CuiYan72.git  
git push -u origin master  
```
