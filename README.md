# HTML-CSS-
##HTML基础  
	1.<!DOCTYPE>: HTML也有很多版本，只有完全明白页面中所有使用的HTML版本，才能完全正确地显示出HTML页面。
	2.   
		1.<a href='http://www.jikexueyuan.com'>study</a> 添加一个超级链接。
	
	 	2.  <a href="http://www.jikexueyuan.com">  
			 <img src="html.png">  
        		</a> 以一张图片作为连接。  

		3.  <a name="tips">hello<a/>
	   <a href="#tips">跳转到hello</a>在本页面内部跳转
	3. <br/>：换行
	4. 三种样式表插入方法：  
		1.外部样式表：<link rel="stylesheet" type="text/css" href="mystyle.css">  
		2.内部样式表：  
			<style type="text/css">  
			body {background-color:red}
			p {margin-left:20px}   
			</style>
		3.内联样式表：  
			<p style="color:red">  
	5. HTML块  
		1.HTML块元素：块元素在显示时，通常会以新行开始。  如：<h1>,<p>,<ul>  
		2.HTML内联元素：内联元素通常不会以新行开始。如<b>,<a>,<img>  
		3.HTML<div>元素：<div>元素是块元素，其主要是组合HTML元素的容器。
		4.HTML<span>元素：<span>元素是内联元素，可作为文本容器。<div><p><span>hehehe</span>hahahaha<p></div> 					可单独定义<span>中的内容  
	6. HTML布局  
		1.div布局  
		2.table布局：<table> <tr> <td>等。  
		3.关于div和table布局的区别：参考：http://blog.csdn.net/wangboxian/article/details/7599665  
	7. 表单		
		<form>  
			用户名：
			<input type="text">  
			密码：  
			<input type="password">  
			你喜欢的水果有？  
			苹果<input type="checkbox">
			梨子<input type="checkbox">
			香蕉<input type="checkbox">   <!-- 复选框 -->
			性别：
			男<input type="radio" name="sex"> 
			女<input type="radio" name="sex">   <!-- name相同，代表同一组，同一组中只能选择其中一个，所以为单选框 -->  
			请选择您常用的网站：
			<select>  
				<option>极客</option>  
				<option>google</option>  
			</select>  
			<textarea clos ="30" rows="30">请再次填写个人信息</textarea>  
			<input type="button" value="确认">		
			<input type="submit" value="提交">
		</form>  
	8. 实体：  在<body>中如果要写<html>这时候浏览器是不识别的，要写&lt;html&gt; 才会在页面上出现<html>,&lt就是<的实体，&gt就是>的实体。
##HTML5新特性  
	1.用于绘画的canvas标签  
	2.用语媒体回放的video和auto标签。
	3.对本地离线存储更好的支持。  
	4.新的特殊内容元素：artical，footer, header, nav, section.新的表单空间：calendar，date，time，email，url，search
##HTML/CSS 基本布局，基础中的基础

	1. 单个div元素居中显示：
		css文件：
			#id {margin:0px auto;background: #6cf;width:900px;height: 500px;}
		margin是设置外间距的属性，0px代表上下外间距为0，auto代表让浏览器自动选择合适的
			
	2. 一列固定宽度居中+头部
		HTML文件：
      
    		<head>
        	<link href="practice_layout.css" rel="stylesheet" type="text/css" />
    		</head>
    		<body>
			<div id="container">
			<div id="header">This is the Header</div>
			<div id="content">This is the content</div>
			</div>
			</body>

		header和content这两个div放到了一个大的container中。
		
		CSS文件：
		
		body { font-family:Verdana; font-size:14px; margin:0;}

		#container {margin:0 auto; width:900px;}
		#header { height:200px; background:#6cf; margin-bottom:5px; line-height:200px;}
		#content { height:600px; background:#cff;}
		
		在父元素container中定义margin：0px auto和宽度。在两个子元素header和content中定义高度就行了。
		
	3. 两列固定宽度左窄右宽型
		HTML文件：
		<html>
			<head>
				<link href="practice_layout.css" rel="stylesheet" type="text/css" />
			</head>
	
		<body>
			<div id="container">
				<div id="left">This is left</div>
				<div id="right">This is right</div>
			</div>
		</body>
		</html>
		
		CSS文件：
		body { font-family:Verdana; font-size:14px;margin:0px; }

		#container {
		margin: 0px auto;
		width:900px;
		}

		#left {
		width:200px;
		height:600px;
		background-color:blue;
		float:left;
		}

		#right {
		width:700px; 
		height:600px;
		background-color:red;
		float:right;
		}
		
		在父元素container中规定了宽度，两个子元素分别规定了各自的宽度和高度，一个子元素float:left，一个子元素float：right.注意  
		：两个子元素的宽度之和（加上margin）等于父元素的宽度时，页面也能成功显示。子元素宽度之和大于父元素，子元素会另起一行。  
		子元素宽度之和小于父元素，两个子元素之间会有空隙。
		
	4.两列固定宽度左窄右宽型+头部
	
		HTML文件中：
			<body>
			        <div id="container">
				<div id="header">This is header</div>
					<div id="maincontent">
					<div id="left">This is left</div>
					<div id="right">This is right</div>
					</div>
				</div>
			</body>
		左右两个div在一个父元素maincontent中,maincontent和header又在一个总的divcontainer中。  
	
		
##CSS基础  
	1.派生选择器  
		HTML中：
		<ul>  
			<li><strong>Hello CSS</strong></li>  
		</ul>  
		CSS中：  
		li strong {
		color:yellow;
		}  
	2. id选择器  
	3. 类选择器  
	4. 属性选择器  
		HTML中：
		<body>  
			<p title="t">属性选择器</p>  
			<p title="te">属性和值选择器</p>
		</body>  
		CSS中：  
		[title] {
			color:red;  
			}   
		那么所有有title属性的标签都会改变。
		[title="t1"] {
			color:yellow;  
			}  
		那么title属性为t1的所有标签都会改变。  
	5. 背景：  
		background-position:  
			1.x% y%:第一个值是水平位置，第二个值是垂直位置。左上角是 0% 0%。右下角是 100% 100%。  

			如果您仅规定了一个值，另一个值将是 50%。  
			2.值：top left
			top center
			top right
			center left
			center center
			center right
			bottom left
			bottom center
			bottom right  
			如果您仅规定了一个关键词，那么第二个值将是"center"。  
			3.xpos ypos  
			第一个值是水平位置，第二个值是垂直位置。
			左上角是 0 0。单位是像素 (0px 0px) 或任何其他的 CSS 单位。
			如果您仅规定了一个值，另一个值将是50%。
			您可以混合使用 % 和 position 值。  
		background-attachment: scroll | fixed | inherit 
			scroll: 随着页面的滚动轴背景图片将移动（相对于用户）
			fixed: 随着页面的滚动轴背景图片不会移动 （相对于用户）
			inherit: 继承    
	6.文本：  
	7.CSS链接的四种状态：
		a:link 普通的，未被访问的链接  a:link {color:  }
		a:visited 用户已经访问的链接   a:visited {color:  }
		a:hover 鼠标指针位于连接上方   a:hover {color:  }
		a:active 链接被点击的时刻      a:active {color:  }   
		
	8. 对table的属性进行设置，比如边框，高宽，字居中，内边距，表格颜色。  
	9. 对标签加轮廓。  
	10.CSS盒子模型：margin，border，padding，content。  
		参考此文，很详细：http://www.cnblogs.com/linjiqin/p/3556497.html
		1.padding：内边距  
		2.border：边框样式，可以四个边一起设置，也可以单边设置。
			CSS3边框：  
			border-radius：圆角边框  
			box-shadow：边框阴影  
			border-image：边框图片    
		3.外边距：通常是透明的，代表块和块之间的距离。
		
	11.CSS定位：  
		普通流：
		position：
		static：默认值。没有定位，元素出现在正常的流中（忽略 top, bottom, left, right 或者 z-index 声明）。  
		relative：生成相对定位的元素，相对于其正常位置进行定位。 因此，"left:20" 会向元素的 LEFT 位置添加 20 像素。  
		fixed：	生成绝对定位的元素，相对于浏览器窗口进行定位。元素的位置通过 "left", "top", "right" 以及 "bottom属性进行规定。  
		absolute：生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。元素的位置通过 "left", "top", "right" 以及 		"bottom" 属性进行规定。    
		浮动：  
		http://www.cnblogs.com/icescut/archive/2009/12/29/cssfloat.html  
	12.CSS导航栏：  
		HTML文本:  
		<ul>  
			<li>Hello</li>  
			<li>Hello</li>  
			<li>Hello</li>  
		</ul>   	
		CSS文本：  
		li {
			display:inline;  
		}  
	13.CSS的2D,3D转换 (转换有很多，只列出来了几个)
		1.translate()：元素从其当前位置移动，根据给定的 left（x 坐标） 和 top（y 坐标） 位置参数：transform:
		translate(50px,100px);
		2.rotate()：元素顺时针旋转给定的角度。允许负值，元素将逆时针旋转。transform: rotate(30deg);
		scale()：元素的尺寸会增加或减少，根据给定的宽度（X 轴）和高度（Y 轴）参数：transform: scale(2,4);值 scale(2,4)  
		把宽度转换为原始尺寸的 2 倍，把高度转换为原始高度的 4 倍。
		3.skew()：元素翻转给定的角度，根据给定的水平线（X 轴）和垂直线（Y 轴）参数。transform: skew(30deg,20deg);值  
		skew(30deg,20deg) 围绕 X 轴把元素翻转 30 度，围绕 Y 轴翻转 20 度。
		matrix()：  
	14. CSS的动画过渡  
		用transition来定义过渡：  
			transition-property	规定设置过渡效果的 CSS 属性的名称。
			transition-duration	规定完成过渡效果需要多少秒或毫秒。
			transition-timing-function	规定速度效果的速度曲线。
			transition-delay	定义过渡效果何时开始。    
		transition的优点在于简单易用，但是它有几个很大的局限。
		（1）transition需要事件触发，所以没法在网页加载时自动发生。
		（2）transition是一次性的，不能重复发生，除非一再触发。
		（3）transition只能定义开始状态和结束状态，不能定义中间状态，也就是说只有两个状态。
		（4）一条transition规则，只能定义一个属性的变化，不能涉及多个属性。
		CSS Animation就是为了解决这些问题而提出的。  
	15.CSS瀑布流效果:  
		1.通过浮动完成  
		2.通过多列完成
		
		
	
	
		
			
		
		
      


