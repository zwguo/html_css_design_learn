第4章 链接 p63页
目标：
	在页面之间建立链接
	链接到其他网站
	电子邮件链接
4.1、URL
全称是Uniform Resource Locator 统一资源定位器，绝对的URL以网站的域名开头，后面指定具体的路径。
如果是指向同一网站中的页面，此时就不需要用绝对URL，而使用相对URL即可。
可以用../表示上级目录：
		<a href="../parent.html">parent.html</a><br />
		<a href="grandson/grandson.html">grandson.html</a><br />
/：代表网站根目录。
4.2、邮件连接
<a href="mailto:jon@example.com">mailtojon</a><br />
4.3、在新窗口中打开连接
使用target="_blank"
4.4、页面内跳转
<a href="#top">top</a>
top是一个元素的id。
