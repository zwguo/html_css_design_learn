第16章 图像
目标：
	在CSS中控制图像的大小
	在CSS中对齐图像
	添加背景图像
16.1、可以定义统一的图片大小
img.large{
	width: 500px;
	height: 500px;
}
这样所有的class为large的img元素的大小都是500X500px。
16.2、可以使用float让图像对齐
16.3、背景图像
body{
	background-image:url('bingbkg.png');
	background-repeat: repeat-x;
}
background-repeat有如下取值：
	repeat：默认值，在水平和垂直方向都重复；
	repeat-x：在水平方向重复；
	repeat-y：在垂直方向重复；
	no-repeat：图像只显示一次；
background-attachment：指定背景图像在用户滚动页面时的移动方式，是位置固定不变，还是随页面滚动，可选值有两个：
	fixed：固定在页面中的一个位置；
	scroll：背景图像随用户上下滚动页面而滚动。
background-position：指定背景图像定位，可以有如下值：
	left top：水平居左，垂直居中，以下类似，水平可选：left center right，垂直可选：top center bottom。
	此外，还可以指定像素值或者百分比。
可是使用简写background来指定，比如：background:#ffffff url('images/tulip.gif') no-repeat top right;
其指定的属性为：background-color,background-image,background-repeat,background-attachment,background-position，顺序不可乱，但某个属性可以不指定。
16.4、图像翻转与子画面
可以设置a为按钮并设置其背景图像，然后在按钮的不同状态：正常，:hover，:active分别设置不同的background-position来显示不同的样式。