<!-- import js for mathjax -->
<script src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>
<div id="header"></div>
* [前言](#preface)
* [表格](#form)
	- [1.表格](#form)
	- [2.表格对齐方式](#align)
* [公式](#formula)
	- [1.行内公式](#line formula)
	- [2.陈列公式](#display formula)
	- [3.MathJax语法](#mathjax)


<div id="preface"></div>
##1. 前言
MarkDown是一种轻量级标记语言，让我们更注重于内容本身，而非format。MarkDown标签数量相对于html来说，极大地减少，但能基本满足我们撰文需求。本教程分为几个部分来介绍MarkDown。本教程将介绍：***表格和公式 !***

<div id="form"></div>
##2. 表格


###2.1 表格
Markdown使用管线图的方式实现表格，表格里面可以使用强调、链接等行内格式。   
下面代码所示为一个基本的表格：  

```
教程标题|主要内容
---|---
关于Markdown|markdown简介
markdown基础|Markdown***基本语法***，格式化文本，代码，链接，图片，分割线和转移字符
markdown表格和公式|markdown的***扩展语法***，表格和公式
```

在网页表示为：

|教程标题|主要内容|
|---|---|
|关于Markdown|markdown简介|
|markdown基础|Markdown***基本语法***，格式化文本，代码，链接，图片，分割线和转移字符|
|markdown表格和公式|markdown的***扩展语法***，表格和公式|

为了美观，你可以将代码写为：

```
|   教程标题 |   主要内容   |
|-----------|------------|
|关于Markdown|markdown简介|
|markdown基础|Markdown***基本语法***，格式化文本，代码，链接，图片，分割线和转移字符|
|markdown表格和公式|markdown的***扩展语法***，表格和公式|
```

效果一样：

|   教程标题 |   主要内容   |
|-----------|------------|
|关于Markdown|markdown简介|
|markdown基础|Markdown***基本语法***，格式化文本，代码，链接，图片，分割线和转移字符|
|markdown表格和公式|markdown的***扩展语法***，表格和公式|

<div id="align"></div>
###2.2 表格对齐方式
注意，我们同时可以指定表格单元格的对齐方式，如下面代码所示。

```
| Day     | Meal     | Price   |
|:--------|---------:|:-------:|
| Monday  | pasta    | $6      |
| Tuesday | chicken  | $8      |
```

在网页表示为：

| Day     | Meal     | Price   |
|:--------|---------:|:-------:|
| Monday  | pasta    | $6      |
| Tuesday | chicken  | $8      |

上面例子分别表示了左对齐，右对齐和两端对齐。


<div id="formula"></div>
##3. 公式
通过使用MathJax，我们可以让Markdown解析LaTeX数学表达式，通常情况下，我们需要引入MathJax插件才可能工作。
引入插件的代码：

```
\<script type="text/javascript" src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML"></script>(最前面的backslash用来转义)
```

<div id="line formula"></div>
###3.1 行内公式

我们使用`\\(公式\\)`的方式来包含行内公式，例如:  

```
一个简单的数学公式，求出圆的面积： \\(s=\\pi r^2\\)
注意：行内公式的语法为： \\(公式\\),在Tex中是\(公式\),但是在markdown中，backslash是转义字符，所以用double backslash来表示backslash。
```

在网页显示为：  
一个简单的数学公式，求出圆的面积： \\(s=\\pi r^2\\)


<div id="display formula"></div>
###3.2 陈列公式(行间公式)

我们使用`$$...$$`来表示行间公式。例如：

```
同样的是求出圆的面积： $$s= \pi r^2$$
```

在网页表示为：
$$s= \pi r^2$$


<div id="mathjax"></div>
###3.3 MathJex语法

1.利用\alpha、\beta、\gamma表示希腊字母α、β、γ， 使用\Gamma表示大写希腊字母Γ等，如下表所示。
  

|字母|实现|字母|实现|
|---|---|---|---|
|\\(A\\)|`A`|\\(\alpha\\)|`\alpha`|
|\\(B\\)|`B`|\\(\beta\\)|`\bata`|
|\\(\Gamma\\)|`\Gamma`|\\(\gamma\\)|`\gamma`|
|\\(\Delta\\)|`\Delta`|\\(\delta\\)|`\delta`|
|\\(E\\)|`E`|\\(\epsilon\\)|`\epsilon`|
|\\(Z\\)|`Z`|\\(\zeta\\)|`\zeta`|
|\\(H\\)|`H`|\\(\eta\\)|`\eta`|
|\\(\Theta\\)|`\Theta`|\\(\theta\\)|`\theta`|
|\\(I\\)|`I`|\\(\iota\\)|`\iota`|
|\\(K\\)|`K`|\\(\kappa\\)|`\kappa`|
|\\(\Lambda\\)|`\Lambda`|\\(\lambda\\)|`\lambda`|
|\\(M\\)|`M`|\\(\mu\\)|`\mu`|
|\\(N\\)|`N`|\\(\nu\\)|`\nu`|
|\\(\Xi\\)|`\Xi`|\\(\xi\\)|`\xi`|
|\\(O\\)|`O`|\\(\omicron\\)|`\omicron`|
|\\(\Pi\\)|`\Pi`|\\(\pi\\)|`\pi`|
|\\(P\\)|`P`|\\(\rho\\)|`\rho`|
|\\(\Sigma\\)|`\Sigma`|\\(\sigma\\)|`\sigma`|
|\\(T\\)|`T`|\\(\tau\\)|`\tau`|
|\\(\Upsilon\\)|`\Upsilon`|\\(\upsilon\\)|`\upsilon`|
|\\(\Phi\\)|`\Phi`|\\(\phi\\)|`\phi`|
|\\(X\\)|`X`|\\(\chi\\)|`\chi`|
|\\(\Psi\\)|`\Psi`|\\(\psi\\)|`\psi`|
|\\(\Omega\\)|`\Omega`|\\(\omega\\)|`\omega`|

2.利用{}实现优先级。
   
例如`\\(x\_i^2\\)`实现\\(x\_i^2\\)，而`\\(x\_{i^2}\\)`实现\\(x\_{i^2}\\)。   
例如`\\(lim\_{x\to\infty}\\)`实现\\(lim\_{x\to\infty}\\)。  

3.常用数学运算符表示如下。
 
 |运算符|说明|案例|案例实现|
 |:---|:---|:---:|:---:|
 |+|加|\\(x + y\\)|`\\(x + y\\)`|
 
