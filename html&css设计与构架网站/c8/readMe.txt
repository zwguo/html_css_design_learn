第8章 其他标记 p165
目标：
	指定不同的HTML版本
	元素的标识和分组
	注释、meta信息和内联框架
8.1、HTML历史
HTML4：1997年；
XHTML1.0：2000年，1998年一种称为XML的语言公诸于世，它的目的是为了让人们编写新的标记语言，所以HTML4重新制定，有如下要求：
	每个元素都要有一个结束标签，除了<img />这种元素外；
	特性名称必须使用小写字母；
	所有的特性都必须对应一个特性值，所有的特性值都需要在双括号中；
	不能再使用过时的元素；
	如果一个元素在另一个元素中开始，那么它应该在同一个元素内结束。
为了帮助网页设计人员转换到这种新语法，其有两个主要版本：
	严格版XHTML1.0：必须严格遵守规则；
	过渡版XHTML1.0：仍可以使用表示性元素；
此外还有一个XHTML1.0框架版本，允许网页设计人员将浏览器窗口分割成几个框架，每个框架内嵌入一个不同的HTML页面，如今这个框架正在被淘汰。
HTML5：新的规则。
8.2、DOCTYPE文档类型
由于存在HTML多个版本，因此需要告诉浏览器我们用的是哪种版本：
注意是文档的开头，前面连空格都不能有！
HTML5：
	<!DOCTYPE html>
HTML4：
	<!DOCTYPE html PUBLIC 
	"-//W3C//DTD HTML 4.01 Transitional//EN" 
	"http://www.w3.org/TR/html4/loose.dtd">
Transitional XHTML 1.0：
	<!DOCTYPE html PUBLIC 
	"-//W3C//DTD XHTML 1.0 Transitional//EN" 
	"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
Strict XHTML 1.0：
	<!DOCTYPE html PUBLIC 
	"-//W3C//DTD XHTML 1.0 Strict//EN" 
	"http://www.w3.org/TR/xhtml1/DTD/xhtml1-Strict.dtd">
XML声明：
	<?xml version="1.0" ?>
8.3、全局特性
id特性：所有的HTML元素均支持，它的值应该以字母或下划线开头，必须全局唯一。
class特性：所有的HTML元素都支持，其值可以有多个，以空格隔开。
8.4、块级元素
有些元素在显示时总是另起一行，叫做：块级元素，包括：<h1-6>、<p>、<ul>、<li>等；
有些元素在显示时总是与它邻近的元素出现在同一行内，这些元素叫做内联元素，包括：<a>、<b>、<em>以及<img>等。
可以通过<div>将文本和元素集中在一个块级元素中，通过<span>将其集中在一个内联元素中。
8.5、内联框架
<iframe>是inline frame的缩写。
<iframe src="testA.html" width="300px" height="200px" seamless="seamless"></iframe>
seamless是HTML5的特性：不希望出现滚动条，其他的scrolling和frameborder都已不支持。
8.6、meta页面信息
<head>
	<title>第8章 其他标记</title>
	<meta charset="utf-8" />
	<meta name="description" content="描述信息，不要超过155个字符">
	<meta name="keywords" content="关键字1,关键字2,关键字3">
	<meta name="robots" content="nofollow">
	<meta http-equiv="author" content="gzw">
	<meta http-equiv="pragma" content="no-cache">
	<meta http-equiv="expires" content="Fri, 04 Apr 2018 23:59:59 GMT">
</head>
其中的name属性支持keywords，description，robots，其中robots是指如果不需要搜索引擎使用则是：noindex，如果希望其使用但是不希望其跟踪页面的其他链接，则使用nofollow。另外可使用http-equiv特性，注意expires必须按照指定格式来设置缓存的有效期。
8.7、转义字符
<	&lt;
	&#60;
>	$gt;
&	&amp;
	&#38;
"	&quot;
	&#34;
等。

























