#项目命名
小写方式， 以下划线分隔 
big_data_analysis_platform 大数据分析平台

1.目录命名
小写方式 以下划线分隔 
src common dist components data_modules

2.CSS scss命名
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

3.js文件命名
小写方式 以下划线分隔 
sider_nav.js
类js文件首字母大写
User.js

【复数命名】 charts.js charts.css 

#规范
1.HTML
页面开头使用这个简单地 doctype 来启用标准模式，使其每个浏览器中尽可能一致的展现 <!DOCTYPE html>

在属性上，使用双引号  '<img src="head_img.png" alt="head_img">'

IE compatibility mode 最好是设置为 edge mode <meta http-equiv="X-UA-Compatible" content="IE=Edge">

字符编码 <meta charset="UTF-8">

引入 CSS 和 JavaScript 
<link rel="stylesheet" href="common.css">
<style>
    /* ... */
</style>
<script src="code-guide.js"></script>

html属性顺序
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

尽量减少标签数量 例如
<div class="head">
    <img src="">
</div>
==> 
<img class="head" src="">



2.css 
使用组合选择器时，保持每个独立的选择器占用一行
.btn,
.btn__icon{
	font-size: 1.1em;
}

每条声明应该只占用一行来保证错误报告更加准确
.btn{}
.btn__icon{}

所有的十六进制值都应该使用小写字母 尽可能使用短的十六进制值如#fff替代#ffffff
.btn{
	color: #fff;//#ffffff
}

不用元素选择器
ul.tabellist{} 
==> 
.tablelist{}

相关的属性声明应该以下面的顺序分组处理
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
