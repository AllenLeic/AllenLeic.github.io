---
layout: post
title: "markdown-GFM-常用语法总结"
date: 2016-04-25
description: "这是 markdown 的常用语法。如果忘记了，可以在这里找到。"
tag: 博客
---

## 基本语法

Markdown是一种可以使用普通文本编辑器编写的标记语言，通过简单的标记语法，它可以使普通文本内容具有一定的格式。    

另外值得注意的是：**MarkDown支持所有的HTML语法**，也就是说你可以在 Markdown 文档中使用 HTML 标签。

对于我们程序员来说，使用 Markdown 可以让我们写博客的时候专注于内容而不用花太多的时间在文章的格式上面，所以，学习 Markdown 的基本语法于使用是非常有必要的，目前支持 Markdown 的平台有很多，比如 GitHub ，简书， 有道云等等。 但是这些平台基本都有一些衍生版本，如 GFM 就是 GitHub上面的 Markdown 的衍生格式。本文将介绍一些基本的 Markdown 语法。

### Headers 标题：

| 标题 |  格式  |
| :--: | :----: |
|  H1  |   #    |
|  H2  |   ##   |
|  H3  |  ###   |
|  H4  |  ####  |
|  H5  | #####  |
|  H6  | ###### |



另外，H1和H2还能用以下方式显示：

	一级标题
	===
	 
	二级标题
	---
  
<br/>
### Emphasis 文本强调：

| 效果 |  格式  |
| :--: | :----: |
|   *斜体* or _斜体_  |   `*斜体* or _斜体_`    |
|  **加粗** or **加粗**  |   `**加粗** or **加粗**`   |
|  ***粗斜体*** or ___粗斜体___  |   `***粗斜体*** or ___粗斜体___`   |
|  ~~删除线~~  |  `~~删除线~~`   |
|  ***加粗斜体***  |  `***加粗斜体***`  |
|  ~~**删除**~~  | `~~**删除**~~`  |
|  *~~删除斜体~~*  | `*~~删除斜体~~*` |
|  ***~~加粗删除斜体~~***  | `***~~加粗删除斜体~~***` |


>但是，如果你的\*和\_两边都有空白的话，它们就只会被当成普通的符号：这是一段 * 文本强调 * 的说明示例。  

>如果要在文字前后直接插入普通的星号或底线，你可以用反斜线（转义符）：\*这是一段被星号包围的文字\*


<br>
## Lists 列表：

### Unordered 无序列表：

无序列表可以使用的三种符号来表示，格式为 **” 符号 + 空格“**

	* 无序列表
	* 子项
	* 子项
	 
	+ 无序列表
	+ 子项
	+ 子项
	 
	- 无序列表
	- 子项
	- 子项

### Ordered 有序列表：
  有序列表如果强行插如一个乱序列表会自动识别 如1.2.4.3.照样能识别，格式为 **”序号 + . + 空格"**
```
1. 第一行
2. 第二行
3. 第三行
 
1. 第一行
- 第二行
- 第三行
```

## 组合： 一级列表下面加 **两个空格**再写其他的列表就可以了

	* 产品介绍（子项无项目符号）
	    此时子项，要以一个制表符或者4个空格缩进
	 
	* 产品特点
	    1. 特点1
	    - 特点2
	    - 特点3
	* 产品功能
	    1. 功能1
	    - 功能2
	    - 功能3
	可有时我们会出现这样的情况，首行内容是以日期或数字开头：2017. 公司年度目标。
	为了避免也被转化成有序列表，我们可以在"."前加上反斜杠（转义符）：2017\. 公司年度目标。



## 进阶语法

### 内嵌式链接

- 外部链接：`[百度](http://www.baidu.com)`
- 内部链接1：链接仓库的其他文件：`[README](README.md)`
- 内部链接2：链接本文档的其他部分：`[内嵌式链接](#链接-demo)`   

>  **空格一般用-代替，链接本文档的其他标题直接`#标题名`**



### 引用式链接

- 外部链接：`[百度]`
- 外部链接：`[百度][baidu]`
- 内部链接1：链接仓库的其他文件：`[README]`
- 内部链接2：链接本文档的其他部分：`[内嵌式链接]`

> **引用式链接把链接放到文档的最下面，为了不影响阅读。**



### 图片链接

```
`![alt](url text)`
```

- `alt`：图片显示不出来的时候（可以省略）
- `url`: 地址
- `text`: 鼠标放上去时的文字提示（可以省略）

### 外部图片

- 如：`![baidu](https://www.baidu.com/img/bd_logo1.png "百度网站")`
- 其他用法和网页跳转链接类似



### 引用

> 这是一个引文

要结束引文要在下面空一行 **引用要符合使用场景的使用,引用不会自动换行等.最好不要用引用来突出文本** 

多重引文

> > > 这是多重引文

基本就这样



## Code and Syntax Highlighting 代码和语法高亮

### 行内代码块

`行内代码块` ，标记一小段行内代码：本文是一篇介绍`Markdown`的语法的文章。  

格式： ``` ` 这个符号中间，写上内容就是行内代码块了。 这个符号在键盘上面的 `ESC` 下面 `1` 旁边，需要再英文输入状态下才能打出这个符号。

### 快式代码块

```java
System.out.println("hellow world!")
```

~~~markdown
如果高亮的内容包含 ` 号，可以这样写：`` `包裹起来 ` ``

语法高亮：

```html
 <div>Syntax Highlighting</div>
```

```css
body{font-size:12px}
```
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
```php
<?php
  echo "hello, world!";
?>
```
```python
s = "Python syntax highlighting"
print s
```
~~~

>此外还可以在前面空四个空格或者一个table键一般不用空四个空格的方式制作代码块 不能设置语法高亮

<br>

### Escape character 转义符(反斜杠)：

Markdown 可以利用反斜杠来插入一些在语法中有其它意义的符号。  

例如：如果你想要用星号加在文字旁边的方式来做出强调效果，你可以在星号的前面加上反斜杠：
	\*literal asterisks\*

	Markdown 支持以下这些符号前面加上反斜杠来帮助插入普通的符号：
	\反斜杠  
	`反引号  
	*星号  
	_下划线  
	{}花括号  
	[]方括号  
	()括弧  
	#井字号  
	+加号  
	-减号  
	.英文句 
	!感叹号



## GFM 语法

Github Fivored MarkDown,GFM 这是 GitHub 自己扩展的 markdown 格式，支持 表情符号，表格 代办事项等。

### task list 任务列表

![](/images/posts/markdown/GFMtasklist.png)  

### emoji 表情符号  

😄  关于表情符号，GitHub 提供了 非常多的表情供我们选择，也有人整理出了 GitHub emoji 的所有表情符号。

链接 ：  <http://www.emoji-cheat-sheet.com> 

仓库地址：https://github.com/AllenLeic/emoji-cheat-sheet.com.git

# GFM 语法注意事项

- 文本换行要在后面加上两个空格
- 语法高亮用

> \`\`\`java  
> 内容   
> \`\`\`

- 如果不是列表在后面也没有两个空格的话会自动变成一行的。
- 字体加粗强调的时候要在两边留空格，否则加粗无效。 
- 如果在本文档内跳转，英文字母要全部小写



`<!-- 下面是本文档中用到的链接 -->`  
`[百度]: http://www.baidu.com`  
`[baidu]: http://www.baidu.com`  
`[README]:README.md`  
`[内嵌式链接]: #内嵌式链接`  


<br/>
转载请注明: [雷聪的博客](https://allenleic.github.io) » [点击阅读原文](https://allenleic.github.io/2016/04/markdown-GFM-常用语法)
