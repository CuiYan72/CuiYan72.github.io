---
layout: post
section-type: post
title: 安装 jekyll theme 遇到的问题
category: tech
tags: [ 'tutorial' ]
---

### 查看window端口占用
##### 将personal theme 配置到本地，运行到`./scripts/production`时，出现如下错误：

```
    Configuration file: none
    Source: C:/Projects/Prototypes/Jekyll-Test-Site/_plugins
    Destination: C:/Projects/Prototypes/Jekyll-Test-Site/_plugins/_site
    Incremental build: enabled
    Generating...
    done.
    Please add the following to your Gemfile to avoid polling for changes:
    	gem 'wdm', '>= 0.1.0' if Gem.win_platform?
    Auto-regeneration: enabled for 'C:/Projects/Prototypes/Jekyll-Test-Site/_plugins'
    Configuration file: none
    jekyll 3.0.0-beta1 | Error:  Permission denied - bind(2) for 127.0.0.1:4000
```

##### 当遇到这个问题时，需要检查端口被占用的情况
###### 1. 在cmd中，输入 命令 *netstat -ano* ，列出所有端口情况。在“本地地址”中查找需要的端口号。
![]({{site.url}}/img/blog/port1.png)
###### 2. 查看被占用端口对应的PID，输入命令  *tasklist|findstr"8424"*
![]({{site.url}}/img/blog/port2.png)
###### 3. 输入命令 *taskkill /f /t /im ruby.exe*结束进程，或者在任务管理器中结束该进程。

###### 感谢学长的大力帮助~~