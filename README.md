# 项目命名

小写方式， 以下划线分隔 
big_data_analysis_platform 大数据分析平台

<h4>1.目录命名</h4>
小写方式 以下划线分隔 
src common dist components data_modules

<h4>2.CSS scss命名</h4>
BEM规范 块block、元素element、修饰符modifier 使用 block__element--modifier连接<br>
css <br>
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
小写方式 以下划线分隔 <br>
sider_nav.js<br>
类js文件首字母大写<br>
User.js<br>

【复数命名】 charts.js charts.css <br>

# 规范

<h4>1.HTML</h4>
页面开头使用这个简单地 doctype 来启用标准模式，使其每个浏览器中尽可能一致的展现 <!DOCTYPE html><br>
在属性上，使用双引号  '<img src="head_img.png" alt="head_img">'<br>
IE compatibility mode 最好是设置为 edge mode <meta http-equiv="X-UA-Compatible" content="IE=Edge"><br>
字符编码 <meta charset="UTF-8"><br>
引入 CSS 和 JavaScript <br>
<code>
<link rel="stylesheet" href="common.css">
<style>
    /* ... */
</style>
<script src="code-guide.js"></script>
</code>

html属性顺序<br>
class<br>
id<br>
name<br>
data-*<br>
src, for, type, href, value<br>
placeholder, title, alt<br>
 role<br>
required, readonly, disabled<br>
例如<br>
<a id="" class="" data-modal="" href="#">link</a><br>

尽量减少标签数量 例如<br>
<div class="head">
    <img src="">
</div>
==> 
<img class="head" src="">



<h4>2.css </h4>
使用组合选择器时，保持每个独立的选择器占用一行<br>
.btn,
.btn__icon{
	font-size: 1.1em;
}

每条声明应该只占用一行来保证错误报告更加准确<br>
.btn{}
.btn__icon{}

所有的十六进制值都应该使用小写字母 尽可能使用短的十六进制值如#fff替代#ffffff<br>
.btn{
	color: #fff;//#ffffff
}

不用元素选择器<br>
ul.tabellist{} 
==> 
.tablelist{}

相关的属性声明应该以下面的顺序分组处理<br>
Positioning //position top right bottom left z-index<br>
Box model 盒模型 //display float width height margin padding<br>
Typographic 排版 // font line-height text-align<br>
Visual 外观 //color background-color border border-radius box-shadow<br>

/* Misc */

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
