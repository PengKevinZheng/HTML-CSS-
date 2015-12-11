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
		3.HTML<div>元素：<div>元素是内联元素，其主要是组合HTML元素的容器。
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
	
		
      


