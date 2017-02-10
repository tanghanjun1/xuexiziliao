#链接  
  ####语法：[链接名](url)
##内部链接  
####内嵌式链接
* 外部链接 :[百度](http://www.baidu.com)
* 内部链接1，链接仓库的其他文件 [demo1](demo1.md)
* 内部链接2，链接文本中的其他内容部分（相当于锚点） [代码块](Markdown.md#代码块)
####引用式链接
- 外部链接: [百度]
* 内部链接1，链接仓库的其他文件 [demo1]
* 内部链接2，链接文本中的其他内容部分（相当于锚点） [代码块](Markdown.md#代码块)

#图片
* 图片的MarkDown语法
    ![图片替换文字](url 鼠标移动到图片上浮动的文字)
* 外部图片demo 
 ![baidu] (https://www.baidu.com/img/bd_logo1.png "百度网站")
* 仓库的内部图片  
 ![] (images/shuzu.png)
 
 
#图片的引用式链接
* 外部图片demo  
 ![baidu] [baidu_logo]
* 仓库的内部图片  
 ![] (images/shuzu.png)
 ![] (images/markdown.png)
#引用
>这是一段引文。    

——出自《出处》

多次引用。
>>>这是多重引用



#代码块
* 块式代码
```javascript
var a=10;
console.log(a);
```



<!--下面是文档中要用到的链接-->
[百度]: http://www.baidu.com 
[demo1]:(demo1.md)
[代码块]:(Markdown.md#代码块)
[baidu_logo]: https://www.baidu.com/img/bd_logo1.png "百度网站"