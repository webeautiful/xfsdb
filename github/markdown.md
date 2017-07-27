_ _ _
# markdown 语法

这是一篇讲解如何正确使用 GitHub 的 **Markdown** 的排版示例，学会这个很有必要，能让你的文章有更佳清晰的排版。

## 目录
+ [语法指导](#语法指导)
    - [代码区域](#代码区域)
    - [表格](#表格)
    - [标题](#标题)
    - [列表](#列表)
    - [分隔符](#分隔符)
    - [强调](#强调)
    - [引用(blockquote)](#blockquote)
    - [图片与链接](#图片与链接)
    - [任务清单(Task List)](#任务清单)
    - [删除线](#删除线)
    - [表情符号](#表情符号)
+ [参考文献](#参考文献)

## 语法指导

### 代码区域

1) 行内代码  
```
`行内代码`
```
效果:   `行内代码`

2) 普通代码块  
表示方法:1.每行文字前加4个空格(`空格式`)或1个文本缩进(`缩进式`);2.用3个反单引号\`\`\`包含(`围栏式`)

```
/*
* 输出数组的键值对
*/
function getKV($arr)
{
    foreach($arr as $k=>$v)
    {
        echo $k.'--'.$v.'<br/>';
    }
}
getKV($array('a','b','c'));//函数调用
```

3) 高亮代码块([语言标识符查询](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml))

```php
/*
* 输出数组的键值对
*/
function getKV($arr)
{
    foreach($arr as $k=>$v)
    {
        echo $k.'--'.$v.'<br/>';
    }
}
getKV($array('a','b','c'));//函数调用
```

## 表格

表格代码:

    |col1 |col2 | col3
    :---:|:---:|:---:
    | a   |  b  |  c
    | f   |  e  |  d
    | g   |  h  |  i
    | g   |  h  |  i

隔行换色效果:

col1 |col2 | col3
:---:|:---:|:---:
 a   |  b  |  c
 f   |  e  |  d
 g   |  h  |  i
 g   |  h  |  i

### 标题

1) AtX式

    #1号标题
    ##2号标题
    ###3号标题
    ####4号标题
    #####5号标题
    ######6号标题

标题效果:

# 1号标题
## 2号标题
### 3号标题
#### 4号标题
##### 5号标题
###### 6号标题

2)Setext式

    一号标题
    ===
    二号标题
    ---

显示效果:

一号标题
===
二号标题
---

## 列表

1) 无序列表的三种表示方法
```
* 表示普通列表
+ 表示嵌套列表外层
- 表示嵌套列表内层
+ 表示外层列表
    - 表示内层列表
    - 表示内层列表
    - 表示内层列表
```
显示效果:
* `*`+`空格`表示普通列表
+ `+`+`空格`表示嵌套列表外层
- `-`+`空格`表示嵌套列表内层
+ `+`+`空格`表示外层列表
    - `-`+`空格`表示内层列表
    - `-`+`空格`表示内层列表
    - `-`+`空格`表示内层列表

2)有序列表
* 格式:`0~9的数字`+`.`+`空格`+`列表内容`+`尾随两空格`

显示效果:

1. erlang  
    1. erlang/OTP 
    2. 并发性
    3. 集群 
2. 这是有序列表  
3. 这是有序列表  

### 分隔符

格式:

3个`*`表示:`***`  
3个`-`表示:`---`  
3个`_`表示:`___`  

效果如下:  
3个`*`表示:

***

3个`-`表示:

---

3个`_`表示:

___

### 强调

1)斜体(em)

    _这是斜体_
    *这也是斜体*

渲染效果:

_这是斜体_  
*这也是斜体*

2)加粗(strong)

    __这是加粗__
    **这也是加粗**

渲染效果:

__这是加粗__  
**这也是加粗**

### Blockquote

example 1

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    >
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

example 2

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
id sem consectetuer libero luctus adipiscing.

example 3

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

example 4

    > ## This is a header.
    >
    > 1.   This is the first list item.
    > 2.   This is the second list item.
    >
    > Here's some example code:
    >
    >     return shell_exec("echo $input | $markdown_script");

> ## This is a header.
>
> 1.   This is the first list item.
> 2.   This is the second list item.
>
> Here's some example code:
>
>     return shell_exec("echo $input | $markdown_script");

### 图片与链接

1)inline风格

    [Blog](http://xfsweb.com "myblog")

    ![](http://xfsweb.com/emlog/content/uploadfile/201306/27331370760818.jpg "乔布斯")

渲染效果:

[Blog](http://xfsweb.com "myblog")

![](http://xfsweb.com/emlog/content/uploadfile/201306/27331370760818.jpg "乔布斯")

2)reference风格

    [博客地址][url1]
    ![][url2]

    [url1]:http://xfsweb.com "blog"
    [url2]:http://xfsweb.com/emlog/content/uploadfile/201306/27331370760818.jpg "可选的title属性"

渲染效果:

[博客地址][url1]
![][url2]

[url1]:http://xfsweb.com "blog"
[url2]:http://xfsweb.com/emlog/content/uploadfile/201306/27331370760818.jpg "可选的title属性"

3)带链接的图片

    [![](http://xfsweb.com/emlog/content/uploadfile/201306/27331370760818.jpg)](http://xfsweb.com "myblog")

渲染效果:

[![](http://xfsweb.com/emlog/content/uploadfile/201306/27331370760818.jpg)](http://xfsweb.com "myblog")

[![](http://rescdn.qqmail.com/zh_CN/htmledition/images/function/qm_open/ico_mailme_01.png)](http://mail.qq.com/cgi-bin/qm_share?t=qm_mailme&email=q5qZmpuZmJmen_va2oXIxMY)

4)自动链接

    <121023254@qq.com>
    <http://xfsweb.com>

渲染效果:

<121023254@qq.com>  
<http://xfsweb.com>

### 任务清单

语法

    - [x] 支持 @提到某人、#引用、[链接]()、**格式化** 和 <del>标签</del> 等语法
    - [x] 需要使用列表语法来激活（无序或有序列表均可）
    - [x] 这是一个已完成项目
    - [ ] 这是一个未完成项目

渲染效果:

- [x] 支持 @webeautiful、#引用、[链接]()、**格式化** 和 <del>标签</del> 等语法
- [x] 需要使用列表语法来激活（无序或有序列表均可）
- [x] 这是一个已完成项目
- [ ] 这是一个未完成项目

### 删除线

    ~~删除线~~

渲染效果:

~~删除线~~

### 表情符号

:star:[emoji查询](http://www.emoji-cheat-sheet.com/)

:link:

```
:smile:
:tropical_fish:
:watermelon:
:cn:
:100:
:clock530:

/play horn
```

:smile:
:tropical_fish:
:watermelon:
:cn:
:100:
:clock530:

/play horn

## 参考文献
>
* [书写博客的神器](http://upwith.me/?p=503)
* [markdown语法说明](http://wowubuntu.com/markdown/)
* [markdown代码及效果](http://www.ituring.com.cn/article/23)
* [Markdown语法说明（详解版）][1]
* [GitHub 风格的 Markdown 语法][2]
* [Github支持的表情符号][3]
>

[1]:http://www.ituring.com.cn/article/504
[2]:https://github.com/cssmagic/blog/issues/13
[3]:http://www.emoji-cheat-sheet.com/

:boy: [@熊福松](http://weibo.com/270044128 "围脖熊")  
:calendar:2014-05-25

_ _ _

