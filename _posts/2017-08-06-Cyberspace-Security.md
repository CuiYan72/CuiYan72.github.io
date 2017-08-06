---
layout: post
section-type: post
title: 网络空间安全
category: tech
tags: [ 'tutorial' ]
---

### ROT13加密
A换成N、B换成O、依此类推到M换成Z，然后序列反转：N换成A、O换成B、最后Z换成M。只有这些出现在英文字母里头的字元受影响；数字、符号、空白字元以及所有其他字元都不变。

因为只有在英文字母表里头只有26个，并且26=2×13，ROT13函数是它自己的逆反。对任何字元x：ROT13(ROT13(x))=ROT26(x)=x。

转换可以利用查找表完成，如下例所示：
![]({{site.url}}/img/blog/rot13.png) 


### BASE64加密
```
import base64
code='Vm0w……1pXVmtSQk5RPT0='
count=0
try:
    while True:
        code = base64.decodestring(code)
        count+=1
except Exception:
    print count,code 
```

### MD5在线破解密码
*http://www.cmd5.com/*