第12章 文本
目标：
	文本的大小和字型
	粗体、斜体、大写和下划线
	行间距、字母间距和单词间距
12.1、字体堆栈
你可以指定多种字体并为其创建一个优先次序，这有时称为字体堆栈。
SERIF：衬线字体，比如Georigia、Times、Times New Roman；
SNAS-SERIF：无衬线字体，比如Arial、Verdanna、Helvetica；
MONOSPACE：等宽字体，比如Courier、Courier New；
CURSIVE：草书字体，比如Comic Sans MS、Monotype Corsiva；
FANtASY：虚幻字体，比如Impact、Haettenschweiler。

浏览器应该至少支持上述每组字体中的一种，因此，通常要在你所偏爱的字体后面加上这些通用字体名：
font-family: Georgia, Times, serif;
12.2、字体其他
font-size：
	大小，有几种常用的指定方式：
		像素：12px;
		百分数：200%，文本在浏览器中默认大小是16px，因此200%相当于32px；注意如果你首先指定body下面所有文本的大小是默认大小的75%，则此时，是75% * 2 = 24px；
		EM值：1 em相当于一个字母m的宽度；
@font-face{
	font-family:"ChunkFiveRegular";
	src:url("fonts/chunkfive.eot");
}
	这种方式可以指定字体的下载地址，让客户端浏览器安装，但是需要许可。
font-weight：
	粗体，可选值normal和bold；
font-style：
	斜体，可选值normal、italic和oblique，第一种正常，第二种斜体，第三种文本倾斜。
text-transform：
	大写、小写，uppercase：大写，lowercase：小写，capitalize：使每个单词的首字母大写。
text-decoration：
	下划线、删除线，none：无，underline：底部实线，overline：顶部实线；line-through：删除线；blink：动态闪烁。
line-height：
	行间距（leading）是印刷行业的术语，对于一种字型来说，位于基准线以下的部分称为字母下缘（descender），而字母的最高点称为字母上缘（ascender）。行间距指某一行字母下缘的底端到下一行字母上缘的顶端之间的距离，最好行间距以em的方式定义。
letter-spacing：
	字距是印刷业用来描述字母之间空隙的一个术语，应该以em方式指定。
word-spacing：
	单词间距是控制单词之间的间距，应该以em方式指定。
text-align：
	对齐方式，有如下值：
		left：左对齐；
		right：右对齐；
		center：文本居中显示；
		justify：两端对齐。
vertical-align：
	垂直对齐，通常用于内联元素，有如下值：
		baseline；
		sub；
		super；
		top；
		text-top；
		middle；
		bottom；
		text-bottom。
text-indent：
	文本缩进。
text-shadow：
	投影，必须指定三个长度值和一种颜色，第一个长度值代表阴影向左或者向右延伸的距离；第二个长度代表阴影向上或者向下延伸的距离；第三个长度为可选项，用于指定投影的模糊程度；最后一项是颜色值。
	比如：text-shadow: 1px 1px 0px #000000;
:first-letter：
	为一个元素的首字母指定一个值；是伪元素。
:first-line：
	为一个元素的首行指定一个值；是伪元素。
伪类：
	伪元素就像在代码中加入了额外的元素，伪类就像一个类特性的额外的值，比如:visited代表那些被访问过的链接；
	:link：
		该伪类允许你为那些尚未访问过的链接设置样式；
	:visited：
		该伪类允许你为那些访问过的链接设置样式；
	:hover：
		该伪类允许你为那些鼠标悬停的设置样式；
	:active：
		该伪类允许你为那些鼠标点击时的设置样式；
	:focus：
		该伪类在元素拥有焦点时生效。
	当使用伪类时，应该遵循以下顺序：
		:link;:visited;:hover;:focus;:active.
12.3、特性选择器
EXISTENCE（简单选择器）：匹配一种特定的特性（与具体值无关），比如p[class]：应用于所有包含class特性的<p>元素；
EQUALITY（精确选择器）：匹配一个具有特定值得特性，比如p[class="dog"]：应用于所有class值为dog的<p>元素；
SPACE（部分选择器）：匹配一个特性值，该特性值出现在以空格隔开的单词列表中，比如p[class~="dog"]：应用于所有class值包含dog的<p>元素；
PREFIX（开头选择器）：匹配一个以某个特定字符串开头的特性，比如p[attr^"d"]：应用于所有class值以d开头的<p>元素；
SUBSTRING（包含选择器）：匹配一个特性值包含某个字符串的特性，比如p[attr*"d"]：应用于所有class值包含d的<p>元素；
SUFFIX（结尾选择器）：匹配一个以某个特定字符串结尾的特性，比如p[attr$"d"]：应用于所有class值以d结尾的<p>元素；









