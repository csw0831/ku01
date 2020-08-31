# 什么是jQuery？

 jQuery是一个快速，小型且功能丰富的JavaScript库。借助易于使用的API（可在多种浏览器中使用），使HTML文档的遍历和操作，事件处理，动画和Ajax等事情变得更加简单。兼具多功能性和可扩展性，jQuery改变了数百万人编写JavaScript的方式。 



### 库，框架：

​	指的是一堆方法的集合。每个方法都有自己独特的功能，本质上库或者框架能够对外提供很多的功能。

# 引入jquery

```
<script src="../../jquery.min.js"></script>

cdn：https://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js
```

# 窗体加载事件

```
$(function(){
	//窗体加载执行的代码
	alert(3)
})
```

# 选择器

jquery选择器有一个固定语法，$("选择器"),选择器一定要用$("")包起来。

选择器的内容：

### 基础选择器：

```
		*
​		tagname
​		.classname
​		#id
​		p,a
​		p a
​		p>a
​		p+a
​		P++a
​		p~a
```

### 数量选择器：

```
:first				第1个
:last				最后一个
:eq(1)				第2个
:eq(2)				第3个
:lt(2)				下标小于2的所有
:gt(2)				下标大于2的所有
:odd				奇数个
:even				偶数个q
```

### 属性选择器

```
[a]					包含a属性
[a=b]				a属性值为b
[a^=b]				a属性值以b开头
[a$=b]				a属性值以b结尾
[a~=b]				a属性的值包含b
[a][b]				同时包含a属性与b属性
[a!=b]				a属性的值不等于b
[a*=b]				a属性的值里面包含了字母b
```

### css3选择器

```
:first-child			$("p:first-child")			属于其父元素的第一个子元素的所有 <p> 元素
:first-of-type			$("p:first-of-type")		属于其父元素的第一个 <p> 元素的所有 <p> 元素
:last-child				$("p:last-child")			属于其父元素的最后一个子元素的所有 <p> 元素
:last-of-type			$("p:last-of-type")			属于其父元素的最后一个 <p> 元素的所有 <p> 元素
:nth-child(n)			$("p:nth-child(2)")			属于其父元素的第二个子元素的所有 <p> 元素
:nth-last-child(n)		$("p:nth-last-child(2)")	属于其父元素的第二个子元素的所有 <p> 元素，从最后一													个子元素开始计数
:nth-of-type(n)			$("p:nth-of-type(2)")		属于其父元素的第二个 <p> 元素的所有 <p> 元素
:nth-last-of-type(n)	$("p:nth-last-of-type(2)")	属于其父元素的第二个 <p> 元素的所有 <p> 元素，从最													  后一个子元素开始计数
:only-child				$("p:only-child")			属于其父元素的唯一子元素的所有 <p> 元素
:only-of-type			$("p:only-of-type")			属于其父元素的特定类型的唯一子元素的所有 <p> 元素
```

### 其他选择器：

```
:not()					反选，排除选择器
:visible				选择可见的
:hidden					选择隐藏的
:checked				选择所有勾选中的
:selected				选择所有拉选中的
:enabled				选择可操作的
:disabled				选择不可操作的
:empty					选择无内容的标签
:contains(text)			包含指定内容的标签
:has(a)					包含a子元素的标签					
:parent					选择有爹的孩子
:root					指的是html标签
:target					目标元素
```

### 表单选择器

```
:input			$(":input")		所有 input 元素
:text			$(":text")		所有带有 type="text" 的 input 元素
:password		$(":password")	所有带有 type="password" 的 input 元素
:radio			$(":radio")		所有带有 type="radio" 的 input 元素
:checkbox		$(":checkbox")	所有带有 type="checkbox" 的 input 元素
:submit			$(":submit")	所有带有 type="submit" 的 input 元素
:reset			$(":reset")		所有带有 type="reset" 的 input 元素
:button			$(":button")	所有带有 type="button" 的 input 元素
:image			$(":image")		所有带有 type="image" 的 input 元素
:file			$(":file")		所有带有 type="file" 的 input 元素
```

# 事件

jquery的事件跟js的事件其实是一毛一样的，只是绑定语法有些微的不同。

## 语法：

### 		绑定事件：

​				

```
			第一种绑定事件：		
					node
					.click(function(){
​							//点击事件的代码
​					})
					.mouseover(function(){
​						  //鼠标放上去事件的代码
​					})
			第二种绑定事件：
					node
					.bind("click",function(){
							//点击事件的代码
					})
					.bind("mouseout",function(){
							//点击事件的代码
					})
```

### 		解绑事件：

```
$("button:eq(0)").unbind("click");
```



## 常见事件：

| 鼠标事件                                                     | 键盘事件                                                     | 表单事件                                                  | 文档/窗口事件                                             |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :-------------------------------------------------------- | :-------------------------------------------------------- |
| [click](https://www.runoob.com/jquery/event-click.html)      | [keypress](https://www.runoob.com/jquery/event-keypress.html) | [submit](https://www.runoob.com/jquery/event-submit.html) | [load](https://www.runoob.com/jquery/event-load.html)     |
| [dblclick](https://www.runoob.com/jquery/event-dblclick.html) | [keydown](https://www.runoob.com/jquery/event-keydown.html)  | [change](https://www.runoob.com/jquery/event-change.html) | [resize](https://www.runoob.com/jquery/event-resize.html) |
| [mouseenter](https://www.runoob.com/jquery/event-mouseenter.html) | [keyup](https://www.runoob.com/jquery/event-keyup.html)      | [focus](https://www.runoob.com/jquery/event-focus.html)   | [scroll](https://www.runoob.com/jquery/event-scroll.html) |
| [mouseleave](https://www.runoob.com/jquery/event-mouseleave.html) |                                                              | [blur](https://www.runoob.com/jquery/event-blur.html)     | [unload](https://www.runoob.com/jquery/event-unload.html) |
| [hover](https://www.runoob.com/jquery/event-hover.html)      |                                                              |                                                           |                                                           |

# dom操作

## 内容操作

```
使用html函数操作
    获取内容--如果node是一格数组，返回的即是数组第一个元素的内容 （能够获取到标签本身，比如p,span)
    let con = node.html()
    console.log(con);

    设置内容--可以设置html标签
    node.html("新的内容")		
    
使用text函数操作
	获取内容--如果node是一格数组，返回内容(没办法获取标签本身，只能获取内容)
	let con = node.text();
	console.log(con)
	
	设置内容--真的只能设置文本，哪怕给个标签，人家也是当文本
	node.text("文本内容")
```



## 属性操作

<img src="./mdimg/属性.png" height="150"/>

```
使用val函数操作属性---只能操作元素的value属性
    获取内容
    let val = node.val()
    console.log(val)

    设置内容
    node.val("内容")

使用attr函数来操作其他属性(包括value属性)
	获取属性内容
	let attr = node.attr("属性名字");
	console.log(attr)
	
	设置属性内容
	node.attr("属性名字","属性值")
	
	移除属性
	node.removeAttr("属性名")
```



## 样式操作



## 增



## 删除



## 替换









