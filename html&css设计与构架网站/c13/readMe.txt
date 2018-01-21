第13章 盒子 
目标：
	盒子大小的控制
	盒子模型的边框、外边距和内边距
	盒子的显示与隐藏
13.1、盒子模型
CSS对待每个元素就像位于各自的盒子中一样。
13.2、盒子的大小
width、height：控制盒子的大小，最常用的方式就是指定像素、百分数或者em值。像素可以精确确定，百分数和浏览器窗口大小相关，em和盒子中文本的大小相关。
min-width,max-width指定盒子的最小、最大宽度。
min-height,max-height指定盒子的最小、最大高度，max-height可能会导致和下面的内容重叠。
另外可以设置盒子内容的溢出方式：
.widthsize{
	min-width: 300px;
	max-width: 800px;
}
.heightsize{
	min-height: 30px;
	max-height: 85px;
}
.phidden{
	overflow: hidden;
}
.pscroll{
	overflow: scroll;
}
但是注意，宽度默认是不会溢出的，所以只有高度上才会有滚动条产生。
13.3、边框、外边距和内边距
边框：border；
外边距：margin；
内边距：padding；
注意，如果为一个盒子指定了宽度，则盒子的边框、外边距和内边距也会算到宽度上。
在定义两个class时，一定中间要有空格：
	.border .one{
		border-width: 2px;
	}
13.4、边框
宽度可以指定：border-width: 1px 4px 12px 4px，分别代表上 右 下 左，↑→↓←，但是要有style才会显示。
边框样式：border-style: solid，可以指定为：
	solid：实线；
	dotted：一串点，如果宽度为2px，则点也是2px，间隔也是2px；
	dashed：一条虚线；
	double：两条实线；
	groove：显示为雕入页面的效果；
	ridge：显示为页面上凸起的效果；
	inset：显示为嵌入页面的效果；
	outset：显示为要凸出屏幕的效果；
	hidden/none：不显示；
也可以单独为每个方向设定样式：
	border-top-style、border-left-style、border-right-style、border-bottom-style。
同样的宽度也可以分成方向设置。当然还有颜色，border-color:darkcyan deeppink darkcyan deeplink;
也有设置的快捷方式：border:3px dotted red;
13.5、内、外边距
padding用于指定元素的内容和元素的边框之间的空隙。注意如果一个盒子指定了宽度，则内边距就会增加到盒子的宽度上。
js：document.getElementsByClassName('description')[0].offsetHeight 得到的是上下边框+上下内边距+内容高度。
margin用于指定元素边框到其他元素的空隙。
注意padding、margin并不会被子元素继承。
设置快捷方式是：margin:10px 20px，则代表左右是10px，上下是20px。
13.6、内容居中
盒子的外层元素的text-align必须是center，另外，盒子的本身必须设置margin-left和margin-right为auto，且必须有宽度。
body{
	text-align: center;
}
p{
	width: 300px;
	border:2px solid red;
}
.center{
	margin:10px auto 10px auto;
	text-align: left;
}
<body>
	<p>请观察内容没有居中</p>
	<p class="center">请观察内容居中了</p>
</body>
13.7、内联元素和块级元素的转换
display允许你将内联元素转成块级元素，或者反过来。该属性具有以下值：
	inline：内联；
	block：块；
	inline-block：该值可以使一个块级元素像内联元素那样浮动并保持其他的块级元素特征；
	none：该元素从页面隐藏；
13.8、盒子的隐藏
visibility允许从用户的视线中隐藏盒子，但它保留了元素原来占用的空间。该属性具有以下值：
	hidden：该值用于隐藏元素；
	visible：该值用于显示元素；
如果一个元素隐藏，则它的位置会显示空白。
13.9、CSS3-边框图像
可以用border-image:url('images/dots.gif') 11 11 11 11 round; 来指定边框的图片，11代表切割的位置，它会把一张图片切割成9块。round代表伸展模式，此位置可以有如下值：
	stretch：拉伸图片；
	repeat：重复图片；
	round：类似repeat，但是会调整图片大小使得图片不会被分裂。
13.10、CSS3-盒子的投影
box-shadow:inset 0 0 10px 10 red;
inset表示内部阴影，可以省略，之后依次是水平偏移、垂直偏移、模糊距离、阴影扩展（正数会使阴影向四周扩散，负数会使阴影向中间收缩），然后是颜色值。
13.11、CSS3-圆角
border-radius:10px;
该值表示元的半径（像素）。
13.12、CSS3-椭圆形
border-radius:80px 50px;
表示圆角的横向值和纵向值。




























