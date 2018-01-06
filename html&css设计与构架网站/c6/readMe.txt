第6章 表格 p115
目标：
	如何创建表格
	什么样的信息适合在表格中呈现
	如何表示复杂的数据表
6.1、表格的标题
<th>元素和<td>元素的用法一样，但它的作用是表示列或者行的标题（th代表：table heading）。
<th>元素有一个scope属性：
	row：代表行标题；
	col：代表列标题。
6.2、跨行跨列
跨行：<td rowspan="2">Movie</td>
跨列：<td colspan="2">Geography</td>
6.3、长表格
可以用<thead><tbody><tfoot>来区分不同内容。
6.4、过期的属性
<th width="100px">
<table border="2" bgcolor="#efefef">
