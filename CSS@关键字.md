# 一.带有@的CSS关键字 ----at 规则

## `@charset`字符集设置

在CSS文件内使用,指定这个CSS文件的编码方式,如果它被使用,则应该放在最前面;

```css
@charset "utf-8";
```



## `@import` 文件引入

@import 可以引入一个文件的所有内容,但不包括@charset

```css
@import "mycss.css";
@import url("mycss.css");
```

`

语法规则:

```css
@import [ <url> | <string> ]
        [ supports( [ <supports-condition> | <declaration> ] ) ]?
        <media-query-list>? ;
```



## `@media`媒体查询

[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/@media)

能够判断设备类型,根据不同的设备类型做出不同的css动作

```css
@media：<media_query_list>

<media_query_list>：[<media_query>[',' <media_query>]*]?

<media_query>：[only | not]? <media_type> [and <expression>]* | <expression> [and <expression>]*

<expression>：'('<media_feature>[:<value>]?')'
```



### 属性值:

media_type: 指定设备类型。媒体类型包括：参阅[媒体类型](http://caibaojian.com/css3/appendix/media-types.htm)。(CSS2)

expression: 指定媒体查询使用的媒体特性。这类似于CSS属性，如：max-width:960px。(CSS3)



### media_query_list参数列表

| Media Types 媒体类型 | CSS Version 版本 | Compatibility 兼容性 | Description 简介                                 |
| :------------------- | :--------------- | :------------------- | :----------------------------------------------- |
| all                  | CSS2             | 所有浏览器           | 用于所有媒体设备类型                             |
| aural                | CSS2             | Opera                | 用于语音和音乐合成器                             |
| braille              | CSS2             | Opera                | 用于触觉反馈设备                                 |
| handheld             | CSS2             | Chrome,Safari,Opera  | 用于小型或手持设备                               |
| print                | CSS2             | 所有浏览器           | 用于打印机                                       |
| projection           | CSS2             | Opera                | 用于投影图像，如幻灯片                           |
| screen               | CSS2             | 所有浏览器           | 用于计算机显示器                                 |
| tty                  | CSS2             | Opera                | 用于使用固定间距字符格的设备。如电传打字机和终端 |
| tv                   | CSS2             | Opera                | 用于电视类设备                                   |
| embossed             | CSS2             | Opera                | 用于凸点字符（盲文）印刷设备                     |



```html
<!DOCTYPE html>
<html lang="zh-cn">
<head>
<meta charset="utf-8" />
<title>CSS @media详解-CSS教程</title>
<meta name="author" content="Joy Du(飘零雾雨), dooyoe@gmail.com, www.doyoe.com" />
<style>
.test,.test2{display:none;}
/* 本条为CSS2部分，IE8及以下只支持本条 */
@media screen{
	body{color:#f00;}
}
/* 下列为CSS3部分 */
@media screen and (min-width:960px){
	body{background:#999;}
}
@media screen and (device-width:1024px){
	.test{display:block;}
}
@media screen and (width:1024px){
	.test2{display:block;}
}
</style>
</head>
<body>
<div>Media Queries媒体查询</div>
<div class="test">如果你的显示器水平分辨率为1024px的话将能看到本条规则的效果（取决于输出设备屏幕分辨率的大小，不随包括浏览器在内的窗体大小而改变）</div>
<div class="test2">如果视口宽度为1024px的话将能看到本条规则的效果（随包括浏览器在内的窗体大小而改变）</div>
</body>
</html>
```



## `@page` 配置打印相关

可以配置打印室,纸张方向,打印内容样式等

```html
@page{
 size:a4;//定义为a4纸
 margin:0 0 0 50px;//页面的编剧
}
@page rotated { size: landscape;} //定义纸张旋转
.ccc{ 
	page: rotated; //引用旋转
	page-break-before:avoid;//前面不加空页
	page-break-after:avoid;//后面不加空页
}

```





##`@ counter-style`

counter-style产生一种数据，用于定义列表项(ul ol)的显示;

[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/@counter-style)







##`@ key-frames`

keyframes产生一种数据，用于定义动画关键帧。







## `@ fontface`

fontface用于定义一种字体，icon font技术就是利用这个特性来实现的。

```css
@font-face {
  font-family: Gentium;
  src: url(http://example.com/fonts/Gentium.woff);
}

p { font-family: Gentium, serif; }
```





## `@ support`

support检查环境的特性，它与media比较类似。



## `@ namespace`

用于跟XML命名空间配合的一个规则，表示内部的CSS选择器全都带上特定命名空间。

## `@ viewport`

用于设置视口的一些特性，不过兼容性目前不是很好，多数时候被html的meta代替。





# 二. CSS所支持的函数

 ## 1. 图片类

\* filter
\* blur()
\* brightness()
\* contrast()
\* drop-shadow()
\* grayscale()
\* hue_rotate()
\* invert()
\* opacity()
\* saturate()
\* sepia()
\* cross-fade()
\* element()
\* image-set()
\* imagefunction()

## 2. 图形绘制
\* conic-gradient()
\* linear-gradient()
\* radial-gradient()
\* repeating-linear-gradient()
\* repeating-radial-gradient()
\* shape()

## 3. 布局
\* calc()
\* clamp()
\* fit-content()
\* max()
\* min()
\* minmax()
\* repeat()

## 4. 变形/动画
\* transform
\* matrix()
\* matrix3d()
\* perspective()
\* rotate()
\* rotate3d()
\* rotateX()
\* rotateY()
\* rotateZ()
\* scale()
\* scale3d()
\* scaleX()
\* scaleY()
\* scaleZ()
\* skew()
\* skewX()
\* skewY()
\* translate()
\* translate3d()
\* translateX()
\* translateY()
\* translateZ()

## 5. 环境与元素
\* var()
\* env()
\* attr()  

