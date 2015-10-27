<div id="header"></div>
- [前言](#preface)
- [基本语法](#syntax)
	- [1.文本格式化](#text format)
		- [1.1 强调文字](#strong)
		- [1.2 添加删除线](#delete)
		- [1.3 标题](#head)
		- [1.4 引用](#quote)
	- [2.代码格式化](#code format)
		- [2.1 行内代码](#line code)
		- [2.2 区内代码](#block code)
	- [3.列表](#list)
		- [3.1 无序列表](#ul) 
		- [3.2 有序列表](#ol)
		- [3.3 列表嵌套](#nl)
		- [3.4 多段列表](#ml)
	- [4.链接](#link)
		- [4.1 行内式链接](#line link)
		- [4.2 参考式链接](#ref link)
		- [4.3 页内导航](#page index)
	- [5.图片](#img)
	- [6.分割线](#cutting line)
	- [7.转义](#esc)
	
	
<div id="preface"></div>
## 前言
MarkDown是一种轻量级标记语言，让我们更注重于内容本身，而非format。MarkDown标签数量相对于html来说，极大地减少，但能基本满足我们撰文需求。本教程分为几个部分来介绍MarkDown。

<div id="syntax"></div>
##基本语法
<div id="text format"></div>
###1 文本格式化
<div id="strong"></div>
#### 1.1 强调文字
我们使用*斜体文字*的方式倾斜文字，**加粗的文字**的方式加粗文字，使用***加粗的斜体字***同时加粗和倾斜文字。  
下面是MarkDown代码:  

```
 *斜体的文字*
 **加粗的文字**  
 ***加粗的斜体字***
```

<div id="delete"></div>
####1.2 添加删除线

MarkDown代码：  

```
~~此处添加删除线~~
```  

其结果显示为:  
~~此处添加删除线~~

<div id="head"></div>
#### 1.3 标题
MarkDown代码：  

```
# 一号标题 
## 一号标题  
### 三号标题  
#### 四号标题  
##### 五号标题  
###### 六号标题
```  

在网页显示为：  
# 一号标题  
## 二号标题
### 三号标题  
#### 四号标题  
##### 五号标题  
###### 六号标题

<div id="quote"></div>
####1.4 引用 
  Markdown通过在引用的文字之前添加”>”标记达到引用的效果，引用段落的时候可以偷懒只在整个段落的第一行最前面加上 >。  
引用里面可以使用强调、链接等其他语法。
  > 这里是一段引用  
  > 这里也是一段引用  
  > > 这里是一个嵌套引用  
  >  
  > 请注意引用符号后面加一个空格和结束引用时的空引用符号加一行空行。
  >  
  
  Markdown 代码如下：  
  
  ```
  > 这里是一段引用 
  > 这里也是一段引用
  > > 这里是一个嵌套引用
  >
  > 请注意引用符号后面加一个空格和结束引用时的空引用符号加一行空行。  
  >  
  ```
  
<div id="code format"></div>
### 2 代码格式化

<div id="line code"></div>
####2.1 行内代码

使用反引号\`可以实现行内代码。  
Markdown 代码如下：   

``` 
我们可以使用'<br>'来换行  
'高亮`文字
```

网页显示为：
  
我们可以使用`<br>`来换行  
`高亮`文字


<div id="block code"></div>
####2.2 区块代码

如果需要在代码内插入反引号，需要多个反引号开始和结束一段代码。 
如果需要代码块和语法高亮，可以采用三个反引号的方式，同时可以注明语言类型。  

```
 ruby  
 require 'redcarpet'  
 markdown = Redcarpet.new("Hello World!")
 puts markdown.to_html
 ```
 
<div id="list"></div>
###3 列表

<div id="ul"></div>
####3.1 无序列表
无序列表使用星号、加号或是减号作为列表标记，如果不按列表显示，前面记得加一空行。  
Markdown 代码如下:  

```
- red  
- green  
- yellow
```  

在网页表示为:  

- red  
- green  
- yellow  
   
<div id="ol"></div>
####3.2 有序列表
使用数字接着一个英文句点表示一个有序列表， 注意前面的数字对列表没有影响。  
代码如下：

```
1. 文字
2. 表格  
4. 图片 
``` 

在网页表示为：

1. 文字
2. 表格
3. 图片


<div id="nl"></div>
####3.3 列表嵌套
列表可以嵌套，添加tab缩进表示层次。例如下面的Markdown代码：

```
1. 文字
    1. 强调
        - 粗体
        - 斜体
        - 粗体和斜体
    2. 引用
2. 图片
3. 表格
``` 

在网页表示为：

1. 文字
    1. 强调
        - 粗体
        - 斜体
        - 粗体和斜体
    2. 引用
2. 图片
3. 表格

<div id="ml"></div>
####3.4 多段列表

列表项里可以包含多个段落，每个项目下的段落都必须缩进 4 个空格或是 1 个制表符：

``` 
1. 学习Markdown  
	学习Markdown的网站   
2. 使用Markdown  
	可以使用在线编辑器和客户端
```

在网页表示为：

1. 学习Markdown  
	学习Markdown的网站，我们可以参考文章结尾的学习资源，文档、案例、教程。  
	学习起来很简单。    
2. 使用Markdown  
	可以使用在线编辑器和客户端
	

<div id="link"></div>
###4 链接
Markdown 支持两种形式的链接语法： 行内式和参考式两种形式。

<div id="line link"></div>
####4.1 行内式链接
首先来看行内式，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可。

markdown代码如下：

```
欢迎大家访问我的[Github](https://github.com/smartYi?tab=repositories "Github")
```

在网页表示为：  
欢迎大家访问我的[Github](https://github.com/smartYi?tab=repositories "Github")


<div id="ref link"></div>
####4.2 参考式链接
参考式链接需要进行链接内容定义，然后引用该定义设置链接。   

链接内容定义格式为:

```
［链接名］: 链接地址 "链接title"  
［链接名］: 空格(tab) 链接地址 空格(tab) "链接title" 
```

设置链接的格式为

``` 
[链接文字][链接名]  
```

所以综合起来就是： 

``` 
欢迎大家访问我的[Github][blog],获取你想要的信息。
［blog］: https://github.com/smartYi?tab=repositories "Github" 
```

在网页显示为：

欢迎大家访问我的[Github][blog],获取你想要的信息。  
[blog]: https://github.com/smartYi?tab=repositories "Github"  

<div id="page index"></div>
####4.3 页内导航
我们同样可以使用markdown实现页内导航，步骤如下：  

1. 先定义一个锚(id)  
2. 然后设置页内链接  

```
	<div id="footer"></div>  
	[到底部](#footer)
```
	
	
[点击此到顶部](#header)

<div id="img"></div>
###5 图片
Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式： 行内式和参考式。   
行内式图片如下所示：

```
![Alt text](/path/to/img.jpg "Optional title") 
![Alt text](/path/to/img.jpg)
```  

下面为参考式：

```
![Alt text][id]
[id]: /url/to/img "Otional title" 
``` 

<div id="cutting line"></div>
###6 分割线

你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：  
 
 ```
***
* * *  
*****  
- - -
```

在网页以上都表示为：
- - -  

<div id="esc"></div>
###7 转义  

Markdown 可以利用反斜杠来实现转义， 支持以下这些符号前面加上反斜杠来帮助插入普通的符号：  

```
\   反斜线  
`   反引号  
*   星号  
_   底线  
{}  花括号  
[]  方括号  
()  括弧  
#   井字号
+   加号  
-   减号  
.   英文句点  
!   惊叹号 
``` 

##Part1 结束。

  