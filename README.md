# 我的第一篇markdown笔记
## 标签
### 认识标签一
    <p>标签，段落标签
    <hx>标签，标题标签（x为1~6）
    <strong>和<em>标签，强调语气标签
    <span>标签，为文字设置单独央视
    <q>标签，短文本引用
    <blockquote>标签，长文本引用
    <br>标签，分行显示文本
    <hr>标签，为网页添加水平线
    &nbsp 为网页添加空行
    <address>标签，为网页添加地址信息
    <code>标签，添加一行代码
    <pre>标签，为网页添加大段代码


### 认识标签二
    <ul>标签，添加新闻信息列表,图片列表
    <ol>标签，添加排行榜列表
    <div>标签，使逻辑清晰
    <table>标签，为表格添加边框 border:1px solid #000

### 认识标签三
    <a>标签，
    <a href="http://www.imooc.com" title="点击进入慕课网">click here!</a>
    //设置target="_blank"在当前浏览器打开
    //<a>链接Email地址<a href="mailto:yy@imooc.com?subject=观了不起的盖茨比有感&body=你好，对此评论有些想法">对此影评有何感想，发送邮件给我</a>
    <img>标签， <img src = "myimage.gif" alt = "My Image" title = "My Image" />
    1、src：标识图像的位置；
    2、alt：指定图像的描述性文本，当图像不可见时（下载不成功时），可看到该属性指定的文本；
    3、title：提供在图像可见时对图像的描述(鼠标滑过图片时显示的文本)；
    4、图像可以是GIF，PNG，JPEG格式的图像文件。
### 表单
1. 文本框、密码框
1. 文本域textarea
1. 单选框、复选框
1. 下拉列表框select
1. 提交按钮、重置按钮
1. label标签

## CSS样式

>CSS全称为“层叠样式表 (Cascading Style Sheets)”，它主要是用于定义HTML内容在浏览器内的显示样式，如文字大小、颜色、字体加粗等

### CSS三种形式
>内联：`<span style="color:red;font-size:10px;" >text</span>`  
嵌入：`<style type="text/css">span{color:red;font-size:10px;}</style>`  
外部：`<link href="style.css" rel="stylesheet" type="text/css">`

### CSS选择器
>标签选择器：标签名{},作用于所有标签。  
类选择器：.类名{}，在标签内定义class="",属图形结构。  
ID选择器：#ID{}，在标签内定义id="",有严格的一一对应关系。  
子选择器：.span>li{}，作用于父元素span下一层的li标签。  
包含选择器：.span li{}，作用于父元素span下所有li标签。  
通用选择器: *{}，匹配所有html元素。  
伪类选择符：它允许给html不存在的标签(标签的某种状态)设置样式，比如说我们给html中的一个标签元素的鼠标滑过的状态来设置字体颜色。

#### 选择器权值
>1. 内联样式表的权值最高 1000 
>1. ID 选择器的权值为 100
>3. Class 类选择器的权值为 10 
>4. HTML 标签选择器的权值为 1

#### CSS 优先级法则：
>A 选择器都有一个权值，权值越大越优先  
B 当权值相等时，后出现的样式表设置要优于先出现的样式表设置  
C 创作者的规则高于浏览者：即网页编写者设置的CSS 样式的优先权高于浏览器所设置的样式  
D 继承的CSS 样式不如后来指定的CSS 样式  
E 在同一组属性设置中标有“!important”规则的优先级最大  
这是规定好的,自然不能打破

    em与px之间怎么换算? 
     *任意浏览器的默认字体高度16px（16像素）。 
     *所有未经调整的浏览器都符合:1em=16px。  
     *那么12px=0.75em,10px=0.625em。 
    为了简化font-size的换算，需要在css中的body选择器中声明font-size=62.5%，这就使em值变为16px`*`62.5%=10px,这样12px=1.2em,10px=1em,也就是说只需要将你的原来的px数值除以10，然后换上em作为单位就行了。  
    注：建议不要使用em作为中文站点的文字单位，会导致文字变形十分严重的。

### CSS盒子模型
#### 元素分类
1. 常用的块状元素有：

    	<div>、<p>、<h1>...<h6>、<ol>、<ul>、<dl>、<table>、<address>、<blockquote> 、<form>

2. 常用的内联元素有：

    	<a>、<span>、<br>、<i>、<em>、<strong>、<label>、<q>、<var>、<cite>、<code>

3. 常用的内联块状元素有：

    	<img>、<input>

>inline:内联元素{  
>1. 不能设置width和height
>1. 多个行内元素排成一行，直到一行排不下，才会换新一行；  
>3. 只可以设置水平方向的边距，如：margin-left,margin-right,padding-left,padding-right.  
}
 
>block:块级元素{
>1. 块级元素独占一行；
>2. 可以设置width和height，默认宽度为一整行，除非单独设置宽度；  
>3. 可以设置margin和padding属性。    
}  

>inline-block{  
简而言之就是让元素既可以在一行内显示，又可以设置宽高边距等。
}

### CSS布局模型

1. 流动模型(Flow):默认网页布局，块状元素自上而下宽度100%，内联元素自左向右水平分布
2. 浮动模型(Float):让元素浮动起来，可使块状元素并排显示
3. 层模型(Layer)

----------
#### 层模型
1. 绝对定位(position: absolute)  
	>如果想为元素设置层模型中的绝对定位，需要设置position:absolute(表示绝对定位)，这条语句的作用将元素从文档流中拖出来，然后使用left、right、top、bottom属性相对于其最接近的一个具有定位属性的父包含块进行绝对定位。如果不存在这样的包含块，则相对于body元素，即相对于浏览器窗口。   	
2. 相对定位(position: relative) 
	>如果想为元素设置层模型中的相对定位，需要设置position:relative（表示相对定位），它通过left、right、top、bottom属性确定元素在正常文档流中的偏移位置。相对定位完成的过程是首先按static(float)方式生成一个元素(并且元素像层一样浮动了起来)，然后相对于以前的位置移动，移动的方向和幅度由left、right、top、bottom属性确定，偏移前的位置保留不动。   
3. 固定定位(position: fixed)   
	>fixed：表示固定定位，与absolute定位类型类似，但它的相对移动的坐标是视图（屏幕内的网页窗口）本身。由于视图本身是固定的，它不会随浏览器窗口的滚动条滚动而变化，除非你在屏幕中移动浏览器窗口的屏幕位置，或改变浏览器窗口的显示大小，因此固定定位的元素会始终位于浏览器窗口内视图的某个位置，不会受文档流动影响，这与background-attachment:fixed;属性功能相同。

   
 


