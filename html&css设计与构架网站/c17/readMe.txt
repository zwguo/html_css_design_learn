第17章 HTML5布局
目标：
	HTML5布局元素
	如何让旧浏览器识别新元素
	利用CSS设置HTML5布局元素的样式
17.1、传统和新式HTML5布局
传统的是使用div利用id或class来分块处理，比如有些处理header，有些处理导航，有些处理侧边，有些处理页脚。
而新式的使用独立的元素来区分：
	页眉：<header>
	页脚：<footer>
	导航：<nav>
	文章：<article>
	附属信息：<aside>，当其在<article>元素内出现时，其应该包含与当前文章相关的内容；否则就是整个页面相关的内容。
	部分：<section>，把相关的内容集中在一块，并且每个部分通常带有一个标题。其通常不能作为整个页面块使用，可以使用div。
	标题组：<hgroup>，将一个或多个<h1>到<h6>元素组合到一块，将它们当做一个标题看待。
	图形：<figure><figcaption>其表示文章中引用的任何内容，不仅是图像，所以，只有当内容引用某些内容时，才应该使用<figure>元素，而不应该对页面不可或缺的内容上使用该元素，<figcaption>元素为<figure>元素提供文本解释。
17.2、让旧浏览器识别新元素
不能识别HTML5上述元素时，仍想让这些元素作为块出现，则应该定义：
header, section, footer, aside, nav, article, figure, figcaption {
	display: block;
}
IE9是浏览器中第一个允许CSS规则与这些HTML5元素关联的IE版本，故之前的版本想引用这些样式，则应该使用一些简单地JavaScript来设置，叫做：HTML5 shiv或者HTML shim。
可以在页面中使用：
<!--[if lt IE 9]>
<script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
<![endif]-->
来引入，只有当IE版本地域IE9时这句话才会起作用，这是IE的条件注释的写法。