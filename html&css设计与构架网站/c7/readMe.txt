第7章 表单
目标：
	如何收集来自访问者的信息
	各种表单控件
	HTML5中新引入的表单控件
7.1、表单结构
	<form action="" method="" id="">
		action是表单提交的url，method是get（default）或post中一种，id是一般要有的。
	<input type="text" name="" maxlength="">
		type是属性（还可以是password），name是提交到服务器的控件标识，maxlength是输入字符最大长度，size是老的属性用于限制显示长度。
	<textarea name="comments" cols="20" rows="4">Enter your comments...</textarea>
		cols表示宽度；rows是行数，也应该使用css来控制宽度和高度。
7.2、单选多选
可以设定multiple为多选，size是显示的列表个数。
<select name="instruments" size="3" multiple="multiple">
	<option value="ipod">ipod</option>
	<option value="radio" selected="selected">radio</option>
</select>
7.3、图像
可以使用<input type="image" src="" alt="" width="" height="" />用法和<img>标签一样。
7.4、label
label可以包裹整个元素，或者用for="id"来标记其他元素。
7.5、组合表单元素
可以分组：
	<fieldset>
		<legend>Contact details</legend>
		<label>Email:</label>
		<input type="text" value="" />
		<label>Address:</label>
		<input type="text" value="" />
		<label>Tel:</label>
		<input type="text" value="" />
	</fieldset>
7.6、HTML5新元素
<input type="email" />支持type为email、url，并非所有浏览器支持，当url时有些输入法还会优化为显示常用的按键。
还支持type="search"搜索框，支持placeholder属性。
