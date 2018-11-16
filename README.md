# Print.js 网页打印插件
![print.jpg][1]

 - 原生js，不依赖其它库 
 - 可指定打印（或不打印）区域
 - 支持css样式（内联、外联、嵌入）
 - 支持input（radio/checkbox/text）、select、textarea值获取

#### 使用方法
 1. 引入Print.js
 
		<script src="Print.js"></script>

 2. 调用方法
 

		Print('#Dom',{
			noPrint:'.no-print'
		});
		
 3. 所有参数
 
		noPrint : String 不打印区域,默认'.no-print'
		onStart : Function 打印前回调
		onEnd  : Function 打印后回调（不区分确定/取消）

 4. 指定不打印区域

> 方法一. 添加no-print样式类

		<div class="no-print">不要打印我</div>

> 方法二. 自定义类名

		Print('#Dom',{noPrint:'.do-not-print-me-xxx'});
		
		<div class="do-not-print-me-xxx">不要打印我</div>
		


#### 演示地址
 - [[demo]][2]

#### 思路
 将目标区域的dom/css添加到空iframe中，打印该iframe。


#### 注意
 1. 不支持background-color背景色打印，试试用background-image代替
 2. 低级浏览器兼容性待验证

  [1]: files/print.jpg
  [2]: http://denghao.me/demo/2017/Print.js/index.html
