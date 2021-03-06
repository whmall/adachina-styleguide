##web前端规范之HTML

###HTML书写规范
为每个HTML页面的第一行添加标准模式（standard mode）的声明，确保在每个浏览器中拥有一致的展现。

###属性顺序
HTML 属性应当按照以下给出的顺序依次排列，确保代码的易读性。

	class
	id 、 name
	data-*
	src、for、 type、 href
	title、alt

###文件引用
* 页面中不允许出现css内容(包括行内样式和style)。
* 非特殊情况下样式文件必须外链至`<head></head>`之间;非特殊情况下JavaScript文件必须外链至页面底部。

###文件和目录命名约定
* 一律小写，必须是英文单词，多个单词以连字符 ( _ ) 连接。

###其他

* 所有编码均遵循xhtml标准，标签、属性、属性命名必须由小写字母及下划线数字组成, 且所有标签必须闭合，包括br，hr等；属性值必须用双引号包括.

		<div class="item"></div>

* 充分利用无兼容性问题的html自身标签，比如span、em、strong、optgroup、label等等; 需要为html元素添加自定义属性的时候，首先要考虑下有没有默认的已有的合适标签去设置，如果没有，可以使用须以”data-”为前缀来添加自定义属性，避免使用”data:”等其他命名方式。

* 语义化html，如:标题根据重要性用h*(同一页面只能有一个h1)，段落标记用p，列表用ul，内联元素中不可嵌套块级元素。

* 尽可能减少div嵌套，使得代码层级更加清晰，便于阅读。

* 能以背景形式呈现的图片，尽量写入css样式中，如：icon等图片使用背景设置。

* 重要图片必须加上alt属性。

		<img src="bg.jpg" alt="背景图片" />

* 给区块代码及重要功能(比如循环)加上注释, 方便后台集成功能。

		<ul class="list">
			//循环体
			<li class="item"><li>
		</ul>

* 一个页面只出现一次h1标签，便于SEO。
* 书写链接地址时避免重定向。

		href="http://www.kahn1990.com/" //即在URL地址后面加“/”

* 含有描述性表单元素（INPUT，TEXTAREA）添加LABEL

		<p>
    		<label for="test">测试</label>
    		<input type="text" id="test" />
		</p>

* 书写HTML少使用table布局，因为可能很小的一个小改动会造成整个 table 的重新布局。

***
###参考文档
[HTML参考手册](http://www.w3school.com.cn/tags/index.asp)

[前端开发规范手册](https://github.com/Aaaaaashu/Front-End-Style-Guide)





