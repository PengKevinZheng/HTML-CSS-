# HTML-CSS-

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
		
      


