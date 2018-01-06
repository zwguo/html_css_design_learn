第9章 Flash、视频和音频
目标：
	如何向网站中添加Flash影片
	如何向网站中添加视频和音频
	HTML5中的<video>元素和<audio>元素
9.1、Flash简介
自从20世纪90年代末，Flash就成为一个非常流行的动画创建工具，后来它又成为网站中一种非常重要的音频和视频播放器。
在Flash开发环境中创建一个Flash文件并保存时，其扩展名是.fla，但是如果想在网页中使用，必须转成.swf格式。
可以使用HTML的<object>和<embed>标签嵌入。
9.2、Flash的使用
自从2005年以来，Flash的使用越来越少了，因为如下的原因：
	在05-06年，一系列的JavaScript库发布，使得创建动画更加轻松；
	07年的iphone和10年的ipad不支持Flash；
	Flash不适用于有视觉或身体障碍的人使用；
	08年支持HTML5的<video>和<audio>的浏览器开始增多；
9.3、向页面添加Flash影片
<head>
	<title>第9章 flash</title>
	<!-- 利用google的js脚本 -->
	<script type="text/javascript" src="http://ajax.gooleapis.com/ajax/libs/swfobject/2.2/swfobject.js"></script>
	<!-- .swf文件位置，替换的元素id，宽度，高度，可播放此影片的Flash播放器的最低版本Flash Player 8 -->
	<script type="text/javascript">
		swfobject.embedSWF("flash/bird.swf", "bird", "400", "300", "8.0.0");
	</script>
</head>
<body>
	<div id="bird"><p>An animation of a bird taking a shower</p></div>
</body>
9.4、使用视频托管服务
在支持HTML5的浏览器中使用<video>元素，而在不支持的浏览器中使用Flash视频，这种方式目前认为是最好的。
但是你要准备2种格式的视频，一种是WebM，一种是MP4，更好的方式是使用类似于YouTube这样的托管视频网站，它们内部会转码，而不用我们转码，但是有劣势：它们会自动播放广告或者加上logo之类的。
9.5、使用另外的播放器
<!-- 利用google的js脚本 -->
<script type="text/javascript" src="http://ajax.gooleapis.com/ajax/libs/swfobject/2.2/swfobject.js"></script>
<!-- .swf文件位置，替换的元素id，宽度，高度，可播放此影片的Flash播放器的最低版本Flash Player 8，flash的参数，具体的影片位置 -->
<script type="text/javascript">
	var flashvars = {};
	var params = {
		movie:"../video/puppy.flv"
	};
	swfobject.embedSWF("flash/splayer.swf", "bird", "400", "300", "8.0.0", flashvars, params);
</script>
9.6、HTML5添加视频
<video src="video/puppy.mp4" poster="images/puppy.jpg" width="400" height="300" preload controls loop>
<p>A video of a puppy playing in the snow</p>
</video>
在HTML5中你不必为所有特性都指定值，比如<video>的controls、autoplay、loop特性，如果其出现则代表打开。
preload：告诉浏览器在页面加载时需要做什么，可选：
	none：告诉浏览器什么都不需要做；
	auto：告诉浏览器应该在页面加载时载入视频；
	metadata：告诉浏览器只需收集少量视频信息，比如大小、首帧图像、播放列表和持续时间。
src：视频的路径。
poster：在视频加载时或者在视频播放之前，该特性用于指定在播放器中显示一个图像。
width,height：这两个特性用像素指定播放器大小。
controls：浏览器需要提供默认的播放控件。
autoplay：自动播放。
loop：循环播放。
9.7、HTML5多个视频源
上面的例子中，去掉src，使用<source>标签：
<video poster="images/puppy.jpg" width="400" height="300" preload controls loop>
<source src="video/puppy.mp4" type='video/mp4;codecs="avc1.42E01E, mp4a.40.2"' />
<source src="video/puppy.webm" type='video/webm;codecs="vp8, vorbis"' />
<p>A video of a puppy playing in the snow</p>
</video>
解释：<source>的src表示视频源，type指定视频格式（不然浏览器会先加载一点视频，看下是否可以播放），codecs指定编解码器。
9.8、添加音频
<!-- 利用google的js脚本 -->
<script type="text/javascript" src="http://ajax.gooleapis.com/ajax/libs/swfobject/2.2/swfobject.js"></script>
<!-- .swf文件位置，替换的元素id，宽度，高度，可播放此影片的Flash播放器的最低版本Flash Player 8，flash的参数，具体的影片位置 -->
<script type="text/javascript">
	var flashvars = {};
	var params = {
		mp3:"../audio/test-audio.mp3"
	};
	swfobject.embedSWF("flash/player_mp3_1.0.0.swf", "music-player", "200", "20", "8.0.0", flashvars, params);
</script>
9.9、HTML5音频
<audio src="audio/test-audio.ogg" controls autoplay>
	<p>This browser does not support our audio format.</p>
</audio>
src：音频文件的路径；
controls：是否显示播放控件；
autoplay：是否自动播放；
preload：同上；
loop：循环播放；
9.10、HTML5多个音频源
也是使用<source>：
<audio controls autoplay>
	<source src="audio/test-audio.ogg" />
	<source src="audio/test-audio.mp3" />
	<p>This browser does not support our audio format.</p>
</audio>
因为浏览器支持的格式不同，故放置多个source是很必要的。