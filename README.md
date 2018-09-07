# 项目命名

小写方式， 以下划线分隔 <br>

	big_data_analysis_platform 大数据分析平台

<h4>1.目录命名</h4>

小写方式 以下划线分隔 

	src common dist components data_modules

<h4>2.CSS scss命名</h4>

BEM规范 块block、元素element、修饰符modifier 使用 block__element--modifier连接
	
	css
	
	.block{}
	.block__element{} 
	.block__element--modifier{}
	
	scss
	
	.block{
		&__element{
			&--modifier{
				/**/
			}
		}
	}

<h4>3.js文件命名</h4>

	小写方式 以下划线分隔
	sider_nav.js
	
	类js文件首字母大写
	User.js

	【复数命名】 charts.js charts.css

# HTML

页面开头使用这个简单地 doctype 来启用标准模式，使其每个浏览器中尽可能一致的展现 <!DOCTYPE html><br>
	
在属性上，使用双引号  <br>

	<img src="head_img.png" alt="head_img">
	
IE compatibility mode 最好是设置为 edge mode <meta http-equiv="X-UA-Compatible" content="IE=Edge"><br>
	
字符编码 <meta charset="UTF-8"><br>
	
引入 CSS 和 JavaScript <br>

	<link rel="stylesheet" href="common.css">
	<style>
	    /* ... */
	</style>
	<script src="code-guide.js"></script>

html属性顺序<br>

	class
	id
	name
	data-*
	src, for, type, href, value
	placeholder, title, alt
	role
	required, readonly, disabled
	例如
	<a id="" class="" data-modal="" href="#">link</a>

尽量减少标签数量 例如<br>
	
	<div class="head">
	    <img src="">
	</div>
	==> 
	<img class="head" src="">



# css 样式

使用组合选择器时，保持每个独立的选择器占用一行<br>

	.btn,
	.btn__icon{
		font-size: 1.1em;
	}

每条声明应该只占用一行来保证错误报告更加准确<br>

	.btn{}
	.btn__icon{}

		所有的十六进制值都应该使用小写字母 尽可能使用短的十六进制值如#fff替代#ffffff
	.btn{
		color: #fff;//#ffffff
	}

不用元素选择器<br>

	ul.tabellist{} 
	==> 
	.tablelist{}

相关的属性声明应该以下面的顺序分组处理<br>

	Positioning //position top right bottom left z-index
	Box model 盒模型 //display float width height margin padding
	Typographic 排版 // font line-height text-align
	Visual 外观 //color background-color border border-radius box-shadow

 
 
     Misc //opcity 
	.info-panel {
	    /* Positioning */
	    position: absolute;
	    top: 0;
	    right: 0;
	    bottom: 0;
	    left: 0;
	    z-index: 101;

	    /* Box-model */
	    display: block;
	    float: left;
	    width: 200px;
	    height: 200px;

	    /* Typography */
	    font: normal 14px "Helvetica Neue", sans-serif;
	    line-height: 1.5;
	    color: #333;
	    text-align: center;

	    /* Visual */
	    background-color: #fff;
	    border: 1px solid #ddd;
	    border-radius: 5px;

	    /* Misc */
	    opacity: 1;
	}

# js 函数

<h4>避免全局命名空间污染</h4>
	//不推荐
	var x = 1,
	    y = 1;

	// Declaring variables in the global scope is resulting in global scope pollution. All variables declared like this
	// will be stored in the window object. This is very unclean and needs to be avoided.
	// We declare a IIFE and pass parameters into the function that we will use from the global space
	
	//推荐 IIFE
	(function(log, w, undefined){
	  'use strict';

	  var x = 10,
	      y = 100;

	  // Will output 'true true'
	  log((w.x === undefined) + ' ' + (w.y === undefined));

	}(window.console.log, window));

<h4>js声明提前 设置默认参数</h4> 

	let a = null;
	let b = a || ''; //默认参数
	

<h4>等同== 和严格等===的区别</h4> 

	==， 两边值类型不同的时候，要先进行类型转换，再比较。
	===，不做类型转换，类型不同的一定不等。
	==等同操作符
	如果两个值具有相同类型，会进行===比较，返回===的比较值 
	如果两个值不具有相同类型，也有可能返回true 
	如果一个值是null另一个值是undefined，返回true 
	如果一个值是string另个是number，会把string转换成number再进行比较 
	如果一个值是true，会把它转成1再比较，false会转成0 

	console.log( false == null )      // false
	console.log( false == undefined ) // false
	console.log( false == 0 )         // true
	console.log( false == '' )        // true
	console.log( false == NaN )       // false

	console.log( null == undefined ) // true
	console.log( null == 0 )         // false
	console.log( null == '' )        // false
	console.log( null == NaN )       // false

	console.log( undefined == 0)   // false
	console.log( undefined == '')  // false
	console.log( undefined == NaN) // false

	console.log( 0 == '' )  // true
	console.log( 0 == NaN ) // false
	

<h4>真假判断</h4> 
	
	js中以下内容为假：
	false
	null
	undefined
	0
	'' (空字符串)
	NaN
	

<h4>对象调用</h4>

	map对象 判断是否为空 object && object.a
	array数组对象 判断是否为空并且长度大于0 array && array.length > 0 && array.map(function(e){})


# 注释

<h4>函数/方法注释</h4>

	/** 
	* 函数/方法说明 
	* @关键字 {类型} 说明
	*/
	/** 
	* person
	* @age {number} 年龄
	*/
	function person(age){}
	
<h4>单行注释</h4>

	//单行注释
	let num = 1//注释

<h4>多行注释</h4>

	/*
	* 代码执行到这里后会调用setTitle()函数
	* setTitle()：设置title的值
	*/
	setTitle();
