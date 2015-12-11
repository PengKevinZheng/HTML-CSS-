# HTML-CSS-
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
		
      


