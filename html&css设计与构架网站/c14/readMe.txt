第14章 列表、表格和表单
目标：
	指定项目符号样式
	为表格添加边框和背景
	更改表单元素的外观
14.1、项目符号样式
list-style-type属性允许你控制项目符号的形状或样式。
该属性可以应用到<ol>、<ul>、<li>元素中使用。
对于一个无序列表<ol>，其值可为：
	none：无；
	disc：实心圆；
	circle：空心圆；
	square：实心方块。
对于一个有序列表<ul>，其值可为：
	decimal：1 2 3；
	decimal-leading-zero：01 02 03；
	lower-alpha：a b c；
	upper-alpha：A B C；
	lower-roman：i. ii. iii.；
	upper-roman：I II III；
也可以指定图像，用：list-style-type:url('images/star.png');
14.2、列表的定位
一般来说，列表会缩进到页面，而list-style-position可以指定标记显示的位置：
	outside：标记位于文本的左侧，也是默认的；
	inside：标记位于文本的内部，同时文本块会被缩进。
还可以快捷的设置符号样式：list-style:inside circle; 顺序无关。
14.3、表格属性
参见书籍中的table-properties.html。
交替改变行的背景色：
	tr.even {
			background-color: #efefef;
	}
14.4、空单元格样式
空单元格样式，当一个单元格中没有内容时，可能你不希望显示边框。可用如下样式控制：
table{
	empty-cells:show;
}
有三个值：
	show：显示边框；
	hide：隐藏边框；
	inherit：继承外部表格规则；
14.5、单元格之间的空隙
border-spacing：允许你控制相邻单元格之间的距离，比如隔开一点空隙；
border-collapse：允许你控制相邻单元格的边框的处理方式，有如下值：
	collapse：相邻边框合并成一个，此时empty-cells属性会被忽略；
	separate：表示将相邻的边框分离，此时border-spacing属性才会生效。
14.6、定义表单样式
如果要保持表单外观在各个浏览器中的一致性，你可以从http://formalize.me下载一个CSS文件，该作者已经完成了这项艰巨的工作。
表单控件对齐可以用float把label移到左边，然后让其右对齐。
14.7、光标的样式
cursor: move;可以有如下值：
	auto;
	crosshair;
	default;
	pointer;
	move;
	text;
	wait;
	help;
	url('cursor.gif');
14.8、示例html
示例的html很不错，是example.html。
:first-child：第一个子元素；
:last-child：最后一个子元素；
