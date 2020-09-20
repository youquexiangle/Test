# 前端

## 前端的技术

Jquery:简化js操作

Bootstrap基于jQuery和css的框架，做响应式的网站（根据分辨率的变化而变化）非常方便，

**框架**则是提供一套解决方案，你得按我的规定来安排代码结构，它是随着前端功能的增强而产生的，对于往应用方向发展（也就是越来越像客户端）的web产品就很必要做前端架构这件事，它开始以模型为中心，DOM操作只是附加，通过关注点分离鼓励改进应用程序。



web标准的核心理念就是结构标准、样式标准和行为标准，提倡结构、表现和行为相分离，即**HTML-结构、CSS-表现、JavaScript-行为** 分离。

经常给自己的CSS等代码简化，相同的或者相似的两个并集选择器合在一起，不相同的再区分写出来

同步按你的代码顺序执行，

异步不按照代码顺序执行，异步的执行效果更高：

### 一些好用的快捷键

div*3再按tab可以生成三行div双标签

如果有父子级关系的标签，可以用>。例如ul>li就可以了

如果有兄弟关系的标签，用+就可以了。例如 div+p

如果生成带有类名或id名字的，直接写.demo或#two tab键就可以了，

.top+.banner+(.main>.left+.right+).footer按下tab会变

			<div class="top"></div>
			<div class="banner"></div>
			<div class="footer">
				<div class="main">
					<div class="left"></div>
					<div class="right"></div>
				</div>
			</div>
如果生成的div类名是有顺序的，可以用自增符号$，从1开始排序。

如果想要在生成的标签内部写内容可以用{}表示

input:submit会变<input type="submit" value="">

log 后按tab，会出现console.log。

> `例如w200，按下tab键就可以生成width: 200px;`
>
> 例如lh26，按下tab键就可以生成line-height: 26px;

### 一些好的代码

<hr><!--分界线-->
background-size:cover;<!--图片覆盖整个页面-->

setTimeout(func,1000);<!--定时器，一秒钟后执行func()函数，只执行一次-->

setInterval(function(){clock()},1000);<!--每一秒钟周期性的执行函数-->

background:url(images/1.png)  no-repeat left center;//背景图片不平铺 左 居中对齐

 border-radius:75px;//让border-radius值等于高度的一半

border-radius:50%;<!--显示边框后使盒子变圆-->

border:1px solid #000;<!--显示1px黑色边框-->

margin:0 auto;//让盒子居中对齐

text-align:center;//`文字水平居中`

overflow:hidden;<!--溢出隐藏，让图片（元素）在规定范围内变动-->

1.如何让文字垂直居中？
在一行内的盒子内，我们设定行高等于盒子的高度，就可以使文字垂直居中。（line-height:50px；）
2.如何去除a标签自带的下划线？
text-decoration: none; 取消下划线(取消文本装饰)

ul{list-style:none;}<!--去除掉li前面的小点-->

border: 4px double #000000;//定义双线边框，两条线及其间隔宽等于指定的border-width值

backface-visbility:hidden;<!--旋转时不是正面对象屏幕，就隐藏-->

```
     我们就给它的父级添上相对定位，和最小宽度，最小高度避免全部都皱成一团
     width: 100%;

​      min-width: 810px;

​      height: 100%;

​      min-height: 600px;
```

**br和hr的区别：**

<hr> 
标签在 HTML 页面中创建一条水平线。

<br> 可插入一个简单的换行符。

firworks测量工具

### 给网页标题加小图标

通过查询资料，网络上有两种写法(写在head标签内)：

```html
语句一：<link rel="shortcut icon" href="图片地址（一般是favicon.ico）" />
其中favicon.ico需放在根目录下面（不提倡用这种方法，因为图片没有授权，违反了W3C标准，）
语句二：<link rel="icon" href="图片地址" type="image/gif" />

```

静态的图标文件使用：

```html
标题栏：
<link rel="icon" href="ico地址" type="image/x-icon">
收藏夹：
<link rel="shortcut icon" href="ico地址" type="image/x-icon">

注意：图标要用 16*16 色的。。。(保证了兼容性，无论在哪个地方都可以显示)
```

动态图 gif（动画也是16*16）使用：

```html
<link rel="icon" href="1.gif" type="image/gif" >
```

### 清除原格式

*{清除默认的内外边距，几乎是必写的
margin:0;//外边距
padding:0;//内边距
}
border-top要写在border后面，不然容易被覆盖

ul{

list-style:none;//取消列表的默认样式小点

}

text-decoration:none;<!--清除文本修饰-->

input{border:0;}//所有的表单边框为0

### 鼠标经过事件

第一种：主要用了onMouseOver和onMouseOut事件
html代码：
<img alt="" src="images/1.jpg" onMouseOver="this.src='images/1.png'" onMouseOut="this.src='images/1.jpg'">

css代码：

 *img:hover{ cursor: pointer; }*

1）、alt表示图片不能正常显示时的替换内容，里面可以加上文字，一般不写这个属性的话会有警告错误，所以我一般是会加上的。

2）、src="url()"表示图片的地址，此处的意思是images文件夹下的名字为1的jpg图片。

3）、onMouseOver 属性是鼠标指针移动到元素上时触发的。

4）、onMouseOut属性是鼠标指针移出元素是触发的。

此处的意思是 在鼠标移入时显示1.png，移出时显示1.jpg。

5）、img:hover 是鼠标经过img标签时显示的内容。

6）、cursor:pointer 表示鼠标经过是指针显示为小手形状。

注：这里是两张图片完全替换，鼠标移入时图片1.jpg完全不会显示。

第二种

.div_style:hover{
background-image: url("img2.png"); //这是改变背景色
background-repeat: no-repeat;//这是让背景色不平铺
color:red; //这是让字体变为红色
}

## 文档类型

<!doctype>用来声明html的版本，浏览器只有知道html的版本后才能正确显示文档,<!DOCTYPE>本身不是一个标签，而是一个声明。

html5的文档类型是：<!DOCTYPE html>
文档类型设定
·document 
HTML：sublime输入html：4s 
XHTML：sublime输入html：xt 
HTML5：sublime输入html：5 <!DOCTYPE html>

## 字符集

由于不同的国家和地区使用不同的文字，就衍生出了很多不同的字符集和不同的字符编码方案。如：

- 用于现代英语的ASCII字符集
- 用于欧洲很多国家的iso8859系列字符集
- 用于中国的GB2312，GBk，GB18030等字符集
- 用于台湾，香港，澳门等的Big5字符集。
- 用于日本的Shift JIS字符集
- 用于越南的VISCII
- 用于印度的ISCII
- 包含全世界所有文字符号的Unicode字符集和其UTF-7，UTF-8，UTF-16等字符编码方案。

## BFC

Formatting context(格式化上下文) 是 W3C CSS2.1 规范中的一个概念。它是页面中的一块**渲染区域**，**并且有一套渲染规则**，它决定了其子元素将如何定位，以及和其他元素的关系和相互作用。

那么 BFC 是什么呢？

BFC 即 Block Formatting Contexts (块级格式化上下文)，它属于上述定位方案的普通流。

**具有 BFC 特性的元素可以看作是隔离了的独立容器，容器里面的元素不会在布局上影响到外面的元素，并且 BFC 具有普通容器所没有的一些特性。
**

通俗一点来讲，可以把 BFC 理解为一个**封闭的大箱子**，箱子内部的元素无论如何翻江倒海，都不会影响到外部。

#### 触发 BFC

只要元素满足下面任一条件即可触发 BFC 特性：

- HTML 根元素
- 浮动元素：float 除 none 以外的值
- 绝对定位元素：position (absolute、fixed)
- display 为 inline-block、table-cells、flex
- overflow 除了 visible 以外的值 (hidden、auto、scroll)

#### BFC 特性及应用

**1. 同一个 BFC 下外边距会发生折叠**

```html
<head>
div{
    width: 100px;
    height: 100px;
    background: lightblue;
    margin: 100px;
}
</head>
<body>
    <div></div>
    <div></div>
</body>
```

![img](https://pic4.zhimg.com/v2-0a9ca8952c83141250a2d9002e6d2047_b.png)

从效果上看，因为两个 div 元素都处于同一个 BFC 容器下 (这里指 body 元素) 所以第一个 div 的下边距和第二个 div 的上边距发生了重叠，所以两个盒子之间距离只有 100px，而不是 200px。

首先这不是 CSS 的 bug，我们可以理解为一种规范，**如果想要避免外边距的重叠，可以将其放在不同的 BFC 容器中。**

```html
<div class="container">
    <p></p>
</div>
<div class="container">
    <p></p>
</div>
.container {
    overflow: hidden;
}
p {
    width: 100px;
    height: 100px;
    background: lightblue;
    margin: 100px;
}
```

这时候，两个盒子边距就变成了 200px 

![img](https://pic2.zhimg.com/v2-5b8d6e8b2b507352900c1ece00018855_b.png)**2. BFC 可以包含浮动的元素（清除浮动）**

我们都知道，浮动的元素会脱离普通文档流，来看下下面一个例子

```html
<div style="border: 1px solid #000;">



    <div style="width: 100px;height: 100px;background: #eee;float: left;"></div>



</div>
```

![img](https://pic4.zhimg.com/v2-371eb702274af831df909b2c55d6a14b_b.png)由于容器内元素浮动，脱离了文档流，所以容器只剩下 2px 的边距高度。如果使触发容器的 BFC，那么容器将会包裹着浮动元素。

```html
<div style="border: 1px solid #000;overflow: hidden">

    <div style="width: 100px;height: 100px;background: #eee;float: left;"></div>

</div>
```

效果如图：

![img](https://pic4.zhimg.com/v2-cc8365db5c9cc5ca003ce9afe88592e7_b.png)

**3. BFC 可以阻止元素被浮动元素覆盖**

先来看一个文字环绕效果：

```html
<div style="height: 100px;width: 100px;float: left;background: lightblue">我是一个左浮动的元素</div>

<div style="width: 200px; height: 200px;background: #eee">我是一个没有设置浮动, 



也没有触发 BFC 元素, width: 200px; height:200px; background: #eee;</div>
```

![img](https://pic4.zhimg.com/v2-dd3e636d73682140bf4a781bcd6f576b_b.png)

这时候其实第二个元素有部分被浮动元素所覆盖，(但是文本信息不会被浮动元素所覆盖) 如果想避免元素被覆盖，可触第二个元素的 BFC 特性，在第二个元素中加入 **overflow: hidden**，就会变成：

![img](https://pic3.zhimg.com/v2-5ebd48f09fac875f0bd25823c76ba7fa_b.png)这个方法可以用来实现两列自适应布局，效果不错，这时候左边的宽度固定，右边的内容自适应宽度(去掉上面右边内容的宽度)。



## 文档流&浮动&定位

文档流指元素在文档中的位置由元素在html里的位置决定，块级元素独占一行，自上而下排列；内联元素从左到右排列
脱离文档流的方式：

- 浮动，通过设置float属性

- 绝对定位，通过设置position:absolute

- 固定定位，通过设置position:fixed

  

## meta属性

参考：https://blog.csdn.net/ssisse/article/details/51590584

meta是html语言head区的一个辅助性标签。也许你认为这些代码可有可无。其实如果你能够用好meta标签，会给你带来意想不到的效果，meta标签的作用有：搜索引擎优化（SEO），定义页面使用语言，自动刷新并指向新的页面，实现网页转换时的动态效果，控制页面缓冲，网页定级评价，控制网页显示的窗口等！

name属性主要用于描述网页，对应于content（网页内容），以便于搜索引擎机器人查找、分类（目前几乎所有搜索引擎都使用网上机器人自动查找meta值来给网页分类）。

这其中最重要的是description（站点在搜索引擎上的描述）和keywords（分类关键词）。

meta 的属性有两种：name和http- equiv。

#### 1. 指定名/值对定义元数据

name属性与content属性结合使用, name用来表示元数据的类型，表示当前<meta>标签的具体作用；content属性用来提供值。

```
<meta name="参数" content="具体描述信息">
```

例如:

```
<!DOCTYPE HTML>
<html>
    <head>
        <title>demo</title>
        <meta name="keywords" content="电商,物流">
        <meta name="author" content="张三">
        <meta name="description" content="网站描述...">
    </head>
    <body>
        <div>welcome</div>
    </body>
</html>
```

| 元数据名称(name的值) | 说明                                                         |
| -------------------- | ------------------------------------------------------------ |
| application name     | 当前页所属Web应用系统的名称                                  |
| keywords             | 描述网站内容的关键词,以逗号隔开，用于SEO搜索                 |
| description          | 当前页的说明                                                 |
| author               | 当前页的作者名                                               |
| copyright            | 版权信息                                                     |
| renderer             | renderer是为双核浏览器准备的，用于指定双核浏览器默认以何种方式渲染页面 |
| viewreport           | 它提供有关视口初始大小的提示，仅供移动设备使用               |

**viewreport**

![viewreport](https://segmentfault.com/img/remote/1460000017480059?w=1304&h=1186)

**备注:**图片截取自[MDN](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/meta)

主要介绍一个当meta标签的name属性值为viewreport时的视口的大小

**1.mate标签name属性不设置viewreport**

如果不设置name的值为viewreport，默认视口宽度为980

**2.mate标签name属性设置viewreport**

- 1.content内容为空时，默认视口宽度为980
- 2.content设置width，不设置initail-scale时，视口宽度为设置的width值
- 3.content不设置width，只设置initail-scale时，是可以根据initail-scale的值计算出视口的宽度

```
initail-scale = 屏幕宽度 / 视口宽度
```

- 4.content同时设置width和initail-scale时，视口宽度为width的值，页面显示按照initail-scale比率进行缩放
- 5.一般都是进行如下设置，来实现视口宽等于设备宽，布局完成后屏幕显示也不进行缩放

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**renderer**

```
<meta name="renderer" content="webkit"> //默认webkit内核 
<meta name="renderer" content="ie-comp"> //默认IE兼容模式 
<meta name="renderer" content="ie-stand"> //默认IE标准模式

<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

#### 2. 声明字符编码

charset属性为HTML5新增的属性，用于声明字符编码,以下两种写法效果一样

```
<meta charset="utf-8"> //HTML5
<meta http-equiv="content-Type" content="text/html;charset=utf-8"> //旧的HTML
```

GB2312，由中华人民共和国政府制定的，简体汉字编码规范，大陆所有计算机中的简体中文，都使用此种编码格式。

GBK，又称GBK大字符集，简而言之就是将所有亚洲文字的双字节字符，包括简体中文，繁体中文，日语，韩语等，都使用一种格式编码，这样就能够做到在所有的语言平台上面兼容。

#### 3. 模拟http标头字段

**http-equiv**属性与**content**属性结合使用, **http-equiv**属性为指定所要模拟的标头字段的名称，**content**属性用来提供值。

```
<meta http-equiv="参数" content="具体的描述">
```

**content-Type** 声明网页字符编码:

```
<meta http-equiv="content-Type" content="text/html charset=UTF-8">
```

**refresh** 指定一个时间间隔(以秒为单位),在此时间过去之后从服务器重新载入当前页面,也可以另外指定一个页面.

```
<meta http-equiv="refresh" content="2;URL=http://www.baidu.com">//2秒后在当前页跳转到百度
```

**X-UA-Compatible** 浏览器采取何种版本渲染当前页面

```
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1"> //指定IE和Chrome使用最新版本渲染当前页面
```

**expires** 用于设定网页的到期时间，过期后网页必须到服务器上重新传输

```
<meta http-equiv="expires" content="Sunday 22 July 2016 16:30 GMT">
```

**catch-control** 用于指定所有缓存机制在整个请求/响应链中必须服从的指令

```
<meta http-equiv="cache-control" content="no-cache">//
```

content有以下值(百度百科):

| content的值                          | 说明                                                         |
| ------------------------------------ | ------------------------------------------------------------ |
| public                               | 所有内容都将被缓存(客户端和代理服务器都可缓存)               |
| private                              | 内容只缓存到私有缓存中(仅客户端可以缓存，代理服务器不可缓存) |
| no-cache                             | 必须先与服务器确认返回的响应是否被更改，然后才能使用该响应来满足后续对同一个网址的请求。因此，如果存在合适的验证令牌 (ETag)，no-cache 会发起往返通信来验证缓存的响应，如果资源未被更改，可以避免下载。 |
| no-store                             | 所有内容都不会被缓存到缓存或 Internet 临时文件中             |
| must-revalidation/proxy-revalidation | 如果缓存的内容失效，请求必须发送到服务器/代理以进行重新验证  |
| max-age=xxx (xxx is numeric)         | 缓存的内容将在 xxx 秒后失效, 这个选项只在HTTP 1.1可用, 并如果和Last-Modified一起使用时, 优先级较高 |

### 浮动

float:left;//能让三个盒子在一行排好，且没有空隙

在众多小盒子（以一行或者一列为单位）外面加大盒子，可以有效防止覆盖的发生

浮动以最近的父亲对齐，不会超过父亲内边距的范围

一个父盒子里面的子盒子，如果一个子盒子浮动，其他子盒子都要浮动才可以一行对齐。

元素添加浮动后，元素会具有行内块的特性，元素的大小取决于定义的大小或者默认内容的多少。

浮动元素不占用位置

#### 清除浮动的几种方法

标准流：盒子会各占整行位置。子盒子若是标准流，父盒子虽然没有高度，但是会撑开父盒子高度。 

浮动：盒子浮了起来，不会占据原来的位置，若父盒子没有定义高度，则不会撑开父盒子，父盒 子高度为0。（浮动可以让多个块级元素在一行显示，且块与块之间没有空隙，但要注意给父盒子清除浮动，否则父盒子不会被撑开）。

**为什么要清除浮动呢？清除浮动的本质是什么？**

　　清除浮动主要是为了解决父级元素因为子级浮动引起的内部高度为0的问题。

**清除浮动的方法：**

**1. 额外标签法**：给谁清除浮动，就在其后额外添加一个空白标签 。
优点：通俗易懂，书写方便。（不推荐使用）
缺点：添加许多无意义的标签，结构化比较差。

给元素small清除浮动（在small后添加一个空白标签clear(类名可以随意），设置clear:both;即可）

![img](https://img2018.cnblogs.com/blog/1680537/201907/1680537-20190703112802274-1885563518.png)

![img](https://img2018.cnblogs.com/blog/1680537/201907/1680537-20190703113208658-657572243.png)

**2. 父级添加overflow方法**：可以通过触发BFC的方式，实现清楚浮动效果。
优点：代码简洁（慎重使用，若该父盒子里还有position定位会引起麻烦）
缺点：内容增多时候容易造成不会自动换行导致内容被隐藏掉，无法显示需要溢出的元素。

![img](https://img2018.cnblogs.com/blog/1680537/201907/1680537-20190703113817758-304851854.png)

注意：别加错位置，是给父亲加（并不是所有的浮动都需要清除，谁影响布局，才清除谁。）

**3. 使用after伪元素清除浮动**：：after方式为空元素的升级版，好处是不用单独加标签了。（较常用）
优点：符合闭合浮动思想，结构语义化正确。

clear:both;//清除浮动
缺点：由于IE6-7不支持：after，使用zoom：1，触发hasLayout。

![img](https://img2018.cnblogs.com/blog/1680537/201907/1680537-20190703114149745-648850256.png)

注意：这个也是给父亲添加 clearfix

**4. 使用before和after双伪元素清除浮动**：（较常用）

![img](https://img2018.cnblogs.com/blog/1680537/201907/1680537-20190703115038313-781890830.png)

注意：是给父亲添加clearfix

### **定位**

1 relative（自恋型），relative元素框偏移某个距离。元素仍保持其未定位前的形状，它原本所占的空间仍保留。它的主要效果是使元素偏离正常的位置，其他元素不会调整位置来弥补其偏离后留下来的空隙。其与 `absolute` 不同，其偏离对于父元素的定位方式没有要求，**且始终占位，不脱离文档流**

2 `absolute（拼爹型）` ，绝对定位是**脱离文档流的**，元素框从**文档流完全删除**，并相对于其包含块定位。包含块可能是文档中的另一个元素或者是初始包含块。元素原先在正常文档流中所占的空间会关闭，就好像元素原来不存在一样。元素定位后生成一个块级框，而不论原来它在正常流中生成何种类型的框

绝对定位脱离了文档流，所以会出现覆盖情况

3 static默认，一般用来清除定位的

子绝父相：父亲是相对定位，孩子是绝对定位最好

#### 实现绝对定位的水平垂直居中

平时,用的方法即第一种方法是设置left,top值均为50%,同时margin-left设置为绝对定位元素width的一半取负,margin-top设为其height的一半取负。

例如，绝对定位元素的width:100px;height:100px;

代码如下:

```
position:absolute;
left:50%;
top:50%;
margin-left:-50px;
margin-top:-50px;
```

这是比较常用的一个方法，今天介绍一个巧妙的方法，是利用了绝对定位元素的自动伸缩的特性实现的。

代码如下：

```
position:absolute;
left: 0;
right: 0;
top: 0;
bottom: 0;
margin:auto;
```

上面就是第二种方法：设置margin:auto;设置left和right的值相等,top和bottom的值相等,
注意：left和right的值不能超过其相对元素width减去它自身width的一半,否则绝对定位元素会优先取left值进行定位(前提是文档流是从左向右),但是top和bottom的值却没有这个限制。

#### absolute, relative, fixed偏移的参考点分别是什么？

- absolute参考点是离其最近设置了定位（relative、absolute)的元素，如果父级元素没有，则一层一层往上找，最终到body元素
- relative的参考点是其原来左上角的位置
- fixed的参考点是浏览器的窗口

**Z-index**

**因为绝对定位与文档流无关，所以绝对定位的元素可以覆盖页面上的其他元素，可以通过z-index属性控制叠放顺序，z-index越高，元素位置越靠上。
\**z-index只有在使用了定位属性即positon的元素上才可使用；有较高z-index值的元素比z-index值较低的元素离读者更近；z-index值是正负整数\****

####   同一个盒子同时设置相对定位和浮动或者绝对定位和浮动的问题

div｛float :left;position:relative｝这样是可以的

 div｛float :left;position:absolute｝不允许，绝对定位会使浮动失效

## 块级和行内以及行内块元素

块级元素的特点：

```
（1）**宽度默认是容器的100%**
（2）高度，行高、外边距以及内边距都可以控制。
（3）总是从新行开始
（4）可以容纳内联元素和其他块元素。
块级元素各占一行。是垂直方向的！
```

**常见的块级元素：**

　* address - 地址  ， blockquote - 块引用   ，center - 举中对齐块
　　* dir - 目录列表 ，   div - 常用块级容易，也是css layout的主要标签
　　* dl - 定义列表  ，   fieldset - form控制组   ，  form - 交互表单
　　* h1 - 大标题   ，  h2 - 副标题   ，   h3 - 3级标题
　　* h4 - 4级标题 ，  h5 - 5级标题   ，h6 - 6级标题
　　* hr - 水平分隔线
　　* isindex - input prompt
　　* menu - 菜单列表
　　* noframes - frames可选内容，（对于不支持frame的浏览器显示此区块内容
　　* noscript - 可选脚本内容（对于不支持script的浏览器显示此内容）
　　* ol - 排序表单
　　* p - 段落        pre - 格式化文本
　　* table - 表格            ul - 非排序列表

行内元素（内联元素）的特点：

```
（1）** 默认宽度就是它本身内容的宽度。 **
（2）高、宽无效，但水平方向的padding和margin可以设置，垂直方向的无效。
（3）和相邻行内元素在一行上。
（4）行内元素只能容纳文本或则其他行内元素。 a标签除外
行内元素会再一条直线上，是在同一行的。
```

**常见的内联元素：**span、img、a、lable、input、abbr（缩写）、em（强调）、big、cite（引用）、i（斜体）、q（短引用）、textarea、select、small、sub、sup，strong、u（下划线）、button（默认display：inline-block））

行内块元素（内联块元素）（inline-block）

```
在行内元素中有几个特殊的标签——<img />、<input />、<td>，
可以对它们设置宽高和对齐属性，有些资料可能会称它们为行内块元素。
行内块元素的特点：
（1）和相邻行内元素（行内块）在一行上,但是之间会有**空白缝隙**
（2）**默认宽度就是它本身内容的宽度。**
（3）高度，行高、外边距以及内边距都可以控制。
```

**常见的内联块元素：**img、input

display:inline-block;//把元素改为行内块元素

![è¡ååç´ ,åçº§åç´ ,è¡ååçº§åç´ ä¹é´çåºå«?](https://exp-picture.cdn.bcebos.com/bd72f23834bb19ef1f6891a0497bd28287893a8c.jpg?x-bce-process=image%2Fresize%2Cm_lfit%2Cw_500%2Climit_1)





## 伪元素的本质（常用于插入，免去再添加盒子）

之所以被称为伪元素，是因为他们不是真正的页面元素，html没有对应的元素，但所有的用法和表现行为和真正的页面元素是一样的，可以对其使用诸如页面元素一样的css样式，表面上看上去貌似页面的谋些元素，实际上是css展现行为，因此被称为伪元素，

伪元素添加的内容默认是inline元素，表示**伪元素的内容必须设置content属**性，否则不生效

.one——类选择器
:hover——伪类选择器，鼠标经过; :active--点击之后变换
::after——伪元素选择器

类选择器 伪类选择器 就是选取对象
伪元素选择器 本质上是插入一个元素(标签 盒子) 只不过是行内元素

### 注意事项

有时你会发现伪类元素使用了两个冒号 (::) 而不是一个冒号 (:)，这是 CSS3 规范中的一部分要求，目的是为了区分伪类和伪元素，大多数浏览器都支持这两种表示方式。单冒号(:)用于 CSS3 伪类，双冒号(::)用于 CSS3 伪元素。对于 CSS2 中已经有的伪元素，例如 :before，单冒号和双冒号的写法 ::before 作用是一样的。

所以，如果你的网站只需要兼容 webkit、firefox、opera 等浏览器，建议对于伪元素采用双冒号的写法，如果不得不兼容 IE 浏览器，还是用 CSS2 的单冒号写法比较安全。



## 什么是版心？

“版心”（可视区）是指网页中**主体内容所在的区域**。一般在浏览器窗口水平居中显示，常见的宽度值为960px、980px、1000px、1200px等。

## 布局流程

为了提高网页制作的效率，布局时通常需要遵守一定的布局流程。具体如下：

- 确定页面的版心（可视区）
- 分析页面的行模块，以及每个行模块中的列模块。
- 制作html结构
- css初始化，然后开始运用盒子模型的原理，通过DIV+CSS布局来控制网页的各个模块。

## 常用布局

##### 一列固定宽度且居中（最普通、最为常用的结构）

![一列固定宽度且居中](https://img-blog.csdnimg.cn/20200407205701697.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2d1YTIyMg==,size_16,color_FFFFFF,t_70#pic_center)

- 能共用的尽量共用，使代码看起来精简一些。
- 行间距使用margin-top或者margin-bottom时，考虑已有的margin:0 auto,避免冲突，尽量写进一个margin属性里。

##### 两列左窄右宽型结构（比如小米官网）

![两列左窄又宽](https://img-blog.csdnimg.cn/20200407215852325.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2d1YTIyMg==,size_16,color_FFFFFF,t_70#pic_center)

- 左右设置宽度之后，在调整间距边框等样式时，需要考虑到margin、border、padding等导致的盒子宽度变大，一方被挤下去的情况。确保两者之和在父元素的宽度范围内。

##### 通栏平均分布型

![通栏平均分布型](https://img-blog.csdnimg.cn/20200409211224913.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2d1YTIyMg==,size_16,color_FFFFFF,t_70#pic_center)



## 盒子模型

![CSS box-model](https://www.runoob.com/images/box-model.gif)

用padding：0 15 px;使汉字间的间距相等，尽量不要给上下的内外边距。

border-width:``2px``;/* 定义4个边都为2px*/
border-width:``2px` 4px; /* 定义上下边为2px,左右边为4px*/
border-width``:``2px` `3px` `4px``;/* 定义上边为2px,左右边为3px,下边为4px*/
border-width``:``2px` `3px` `4px` `5px;  /* 定义上边2px,右边为 3px,下边为 4px，左边为5px*/

![img](https://img-blog.csdnimg.cn/20190214184714776.PNG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3RpYW5kYW9jaG91cWluXzE=,size_16,color_FFFFFF,t_70)

#### 盒子阴影

1. 使用box-shadow属性为盒子添加阴影

2. ```
   box-shadow:h-shadow v-shadow blur spread color inset(,h-shadow v-shadow blur spread color);
   ```

   | 值       | 描述                                     |
   | -------- | ---------------------------------------- |
   | h-shadow | 必须。水平阴影的位置，允许负值           |
   | v-shadow | 必须。垂直阴影的位置。允许负值           |
   | blur     | 可选，横糊距离                           |
   | spread   | 可选阴影尺寸                             |
   | color    | 可选。阴影颜色。参考CSS颜色值            |
   | inser    | 可选。将外部阴影（outset）改为内部阴影。 |

   【注意】

   - 默认的是外阴影（outset），但是不可以写这个单词，否则导致阴影无效
   - 盒子阴影不占用空间，不会影响其他盒子排列
   - 鼠标经过时显示阴影

### 外边距合并的问题

外边距合并 **垂直**的块级盒子 以最大的外边距为准
外边距合并 **嵌套**的盒子  给子级元素加maegin:20px; 子级盒子不移动 ，父级元素移动

**为父级元素**定义1像素的边框或者内边距或者加overflow:hidden;

### 元素被撑出来怎么办

box-sizing:content-box;//以前的盒模型

box-sizing:border-box;//padding和border不会撑开盒子，被包含在width里面

## 字体图标使用流程

总体来说，字体图标按照如下流程：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190923204211903.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3pkZDUyMg==,size_16,color_FFFFFF,t_70)

### 设计字体图标

假如图标是我们公司单独设计，那就需要第一步了，这个属于UI设计人员的工作， 他们在 illustrator 或 Sketch 这类矢量图形软件里创建 icon图标， 比如下图：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190923204250321.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3pkZDUyMg==,size_16,color_FFFFFF,t_70)

之后保存为svg格式，然后给我们前端人员就好了。

其实第一步，我们不需要关心，只需要给我们这些图标就可以了，如果图标是大众的，网上本来就有的，可以直接跳过第一步，进入第三步。

### 上传生成字体包

当UI设计人员给我们svg文件的时候，我们需要转换成我们页面能使用的字体文件， 而且需要生成的是兼容性的适合各个浏览器的。

 推荐网站： http://icomoon.io

**icomoon字库**

IcoMoon成立于2011年，推出的第一个自定义图标字体生成器，它允许用户选择他们所需要的图标，使它们成一字型。 内容种类繁多，非常全面，唯一的遗憾是国外服务器，打开网速较慢。

推荐网站： http://www.iconfont.cn/

**阿里icon font字库**

http://www.iconfont.cn/

这个是阿里妈妈M2UX的一个icon font字体图标字库，包含了淘宝图标库和阿里妈妈图标库。可以使用AI制作图标上传生成。 一个字，免费，免费！！

**fontello**

http://fontello.com/

在线定制你自己的icon font字体图标字库，也可以直接从GitHub下载整个图标集，该项目也是开源的。

**Font-Awesome**

http://fortawesome.github.io/Font-Awesome/

这是我最喜欢的字库之一了，更新比较快。目前已经有369个图标了。

**Glyphicon Halflings**

http://glyphicons.com/

这个字体图标可以在Bootstrap下免费使用。自带了200多个图标。

**Icons8**

https://icons8.com/

提供PNG免费下载，像素大能到500PX

![]](https://img-blog.csdnimg.cn/20190923204319965.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3pkZDUyMg==,size_16,color_FFFFFF,t_70)

### 下载兼容字体包

刚才上传完毕， 网站会给我们把UI做的svg图片转换为我们的字体格式， 然后下载下来就好了

当然，我们不需要自己专门的图标，是想网上找几个图标使用，以上2步可以直接省略了， 直接到刚才的网站上找喜欢的下载使用吧。

![在这里插入图片描述](https://img-blog.csdnimg.cn/2019092320443640.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3pkZDUyMg==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190923204447689.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3pkZDUyMg==,size_16,color_FFFFFF,t_70)

### 字体引入到HTML

得到压缩包之后，最后一步，是最重要的一步了， 就是字体文件已经有了，我们需要引入到我们页面中。

1. 首先把 以下4个文件放入到 fonts文件夹里面。 通俗的做法

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190923204537483.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3pkZDUyMg==,size_16,color_FFFFFF,t_70)

##### 第一步：在样式里面声明字体： 告诉别人我们自己定义的字体

```css
@font-face {
  font-family: 'icomoon';
  src:  url('fonts/icomoon.eot?7kkyc2');
  src:  url('fonts/icomoon.eot?7kkyc2#iefix') format('embedded-opentype'),
    url('fonts/icomoon.ttf?7kkyc2') format('truetype'),
    url('fonts/icomoon.woff?7kkyc2') format('woff'),
    url('fonts/icomoon.svg?7kkyc2#icomoon') format('svg');
  font-weight: normal;
  font-style: normal;
}
12345678910
```

##### 第二步：给盒子使用字体

```css
span {
		font-family: "icomoon";
	}
123
```

##### 第三步：盒子里面添加结构

```css
span::before {
		 content: "\e900";
	}
或者  
<span></span>  
12345
```

### 追加新图标到原来库里面

如果工作中，原来的字体图标不够用了，我们需要添加新的字体图标，但是原来的不能删除，继续使用，此时我们需要这样做

把压缩包里面的selection.json 从新上传，然后，选中自己想要新的图标，从新下载压缩包，替换原来文件即可。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190923204633519.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3pkZDUyMg==,size_16,color_FFFFFF,t_70)

## 滑动门



###### 核心技术

核心技术就是利用CSS精灵（主要是背景位置）和盒子padding撑开宽度, 以便能适应不同字数的导航栏。

一般的经典布局都是这样的：

```html
<li>
  <a href="#">
    <span>导航栏内容</span>
  </a>
</li>
```

![img](https://img2018.cnblogs.com/i-beta/1417479/201912/1417479-20191215113904272-290919739.png)

 

 

 

可以参考：[https://blog.csdn.net/qq_36434637/article/details/98188484]

![img](https://img2018.cnblogs.com/i-beta/1417479/201912/1417479-20191215113950274-1411295674.png)

 

 

 

![img](https://img2018.cnblogs.com/i-beta/1417479/201912/1417479-20191215114043353-251735371.png)

 

 

 

![img](https://img2018.cnblogs.com/i-beta/1417479/201912/1417479-20191215114143537-1131915470.png)

 

 

 

 

 

------

实例

![img](https://img2018.cnblogs.com/i-beta/1417479/201912/1417479-20191215120034919-187977813.png)

 

 

 

![img](https://img2018.cnblogs.com/i-beta/1417479/201912/1417479-20191215115955810-595037844.png)

 

 

 

![img](https://img2018.cnblogs.com/i-beta/1417479/201912/1417479-20191215120014124-944572162.png)

 

 

 

 

![img](https://img2018.cnblogs.com/i-beta/1417479/201912/1417479-20191215120116967-884554693.png)

 

 

![img](https://img2018.cnblogs.com/i-beta/1417479/201912/1417479-20191215120150382-1168127575.png)

 

 

 

![img](https://img2018.cnblogs.com/i-beta/1417479/201912/1417479-20191215120220303-319327171.png)

## 精灵图

1、精灵图技术产生的目的：很多大型网页在首次加载的时候都需要加载很多的小图片，而考虑到在同一时间，服务器拥堵的情况下，为了解决这一问题，采用了精灵图这一技术来缓解加载时间过长从而影响用户体验的这个问题。

2、精灵图技术的本质：所谓精灵图就是把很多的小图片合并到一张较大的图片里，所以在首次加载页面的时候，就不用加载过多的小图片，只需要加载出来将小图片合并起来的那一张大图片也就是精灵图即可，这样在一定程度上减少了页面的加载速度，也一定程度上缓解了服务器的压力。

参考：https://blog.csdn.net/wangwenkai76/article/details/82556642

其实说白了就是将精灵图设为一个大背景，然后通过background-position来移动背景图，从而显示出我们想要显示出来的部分。

精灵图虽然实现了缓解服务器压力以及用户体验等问题，但还是有一个很大的不足，那就是牵一发而动全身。这些图片的背景都是我们详细测量而得出来的，如果需要改动页面，将会是很麻烦的一项工作。。。

## 过渡效果（使变换的效果看起来更自然）

通过CSS 动作触发平滑过渡功能，比如：:hover、:focus、 :active、:checked 等。

![img](https://img-blog.csdn.net/2018102320511183?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4Mzk1NDE5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

#### 1.transition-property

首先，设置过渡的第一个属性就是指定过渡的属性。

谁做动画谁加过渡，如img

同样，你需要指定你要过渡某个元素的两套样式用于用户和页面的交互。

那么就使用 transition-property 属性。

![img](https://img-blog.csdn.net/20181023205310928?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4Mzk1NDE5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

#### 2.transition-duration

必须加上过渡所需的时间，因为默 认情况下过渡时间为 0。

设置过渡时间为 1 秒钟，如果是半秒钟可以设置为.5s transition-duration: 1s;

####   3.transition-timing-function（可以不写）

当过渡效果运行时，比如产生缓动效果。默认情况下的缓动是：元素样式从初始状态过 渡到终止状态时速度由快到慢，逐渐变慢，即 ease。

![img](https://img-blog.csdn.net/20181023205649654?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4Mzk1NDE5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

#### 4.transition-delay （可以不写）

设置一个过渡延迟效果，就是效果在设置的延迟时间后再执行。

#### 5.简写

单独声明



transition: background-color 1s ease 0s, color 1s ease 0s, margin-left 1s ease 0s;
如果每个样式都是统一的，直接使用 all

transition: all 1s ease 0s;<!--背景颜色和文字颜色都变化用all-->

**transition: all 1s;**   **transition: width 1s;**

```css
/*兼容完整版*/ 
-webkit-transition: all 1s ease 0s; 
-moz-transition: all 1s ease 0s; 
-o-transition: all 1s ease 0s; 
-ms-transition: all 1s ease 0s; 
transition: all 1s ease 0s;
```

# 

## transform变形效果

#### 1.transfoem:translate移动

指定应用的**变换功能**，平移，旋转，缩放。

![img](https://img-blog.csdn.net/20181023201604309?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4Mzk1NDE5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

移动

transfoem:translate（50%）；<!--以自身宽高移动一半-->

transfoem:translate（50px,50px）；

旋转

使用rotate方法，在参数中加入角度值，角度值后面跟表示角度单位的“deg”文字即可，旋转方向为顺时针方向。

> transform：rotate（45deg）；

缩放

使用scale方法来实现文字或图像的缩放处理，在参数中指定缩放倍率。

> transform：scale（0.5）；//缩小一半

（1）可以分别指定元素的水平方向的放大倍率与垂直方向的放大倍率

> transform：scale（0.5，2）；//水平方向缩小一半，垂直方向放大一倍。

倾斜

使用skew方法实现文字或图像的倾斜处理，在参数中分别指定水平方向上的倾斜角度与垂直方向上的倾斜角度。

> transform：skew（30deg，30deg）；//水平方向上倾斜30度，垂直方向上倾斜30度。

（1）只使用一个参数，省略另一个参数

这种情况下视为只在水平方向上进行倾斜，垂直方向上不倾斜。

> transform：skew（30deg）；
>
> transform：skew（0，30deg）；延y轴倾斜

#### 2.transform-origin 

```
transform-origin:top left;围绕左上角旋转
transform-origin:20px 30px;自定义点旋转
```

指定**变换的起点**，。默认情况下，使用元素的中心作为起点。 

![img](https://img-blog.csdn.net/20181023201700974?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4Mzk1NDE5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

![img](https://img-blog.csdn.net/20181023201716853?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4Mzk1NDE5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

浏览器版本

兼容完整版

```css
-webkit-transform: rotate(45deg); 
-moz-transform: rotate(45deg);
-o-transform: rotate(45deg); 
-ms-transform: rotate(45deg);
transform: rotate(45deg);
-webkit-transform-origin: left top;
-moz-transform-origin: left top; 
-o-transform-origin: left top;
-ms-transform-origin: left top;
transform-origin: left top;
```

#### 3.3D 变形

```
**z-index:1;<!--使元素放上来一层，覆盖底下的元素，月大越往上，默认为0-->**
```

![img](https://img-blog.csdn.net/20181023202212889?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4Mzk1NDE5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

```
transform:rotatX(60deg);<!--绕X轴旋转60度-->
transform:translateZ(300px);<!--沿Z轴移动，数值越大离我们眼睛越近，物体变大最大600px-->
transform:translate3d(x,y,z);<!--xyz一起设置，x和y可以是px，也可以是%，z只能是px-->
```



```css
/*兼容版本完整形式*/ 
-webkit-transform: translateZ(200px); 

-moz-transform: translateZ(200px); 

-o-transform: translateZ(200px); 

-ms-transform: translateZ(200px); 

transform: translateZ(200px);
```

#### 4.transform-style

是指定嵌套元素如何在 3D 空间中呈现。
flat 默认值，表示所有子元素在 2D 平面呈现。

preserve-3d 表示子元素在 3D 空间中呈现。

一般设置到当前元素的父元素

transform-style: preserve-3d;

需要再配合后面的功能属性和变形配置，才能看到效果。同样，这个属性也需要加上各种厂商前缀。


#### 5.perspective （添加后有立体感）

设置查看者的位置，并将可视内容映射 到一个视锥上，继而投放到一个 2D 平面上。近大远小。
![img](https://img-blog.csdn.net/20181023204330521?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4Mzk1NDE5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

在元素中设置透视的值 perspective(长度值)，但它还是和在父元 素设置有一定不同。

因为**父元素**整个作为透视，而元素自己作为透视，导致不同。

**给父元素添加**perspectiv

具体测试看透视的距离

**综合性写法**
**transform:translate() rotate() scale()**
**注意：**
**其顺序会影响转换效果**
**当我们同时有位移和其他属性时，记得要将位移放到最前面。**

```HTML
img { 
transform: perspective(1000px) rotateY(45deg); 
如果有多组形变，都属于transform的用空格隔开
}

perspective：1000px；数值越小越明显
```



#### 6.perspective-origin

设置 3D 变形中的源点角度。该属性默认 值为 50% 50%也就是 center center。

![img](https://img-blog.csdn.net/20181023204558157?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4Mzk1NDE5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

#### 7.3D 变形属性 

运用前面 3D 功能属性 transform-style 和 perspective 来构建 3D 变形效果。

CSS3中的3D坐标系与上述的3D坐标系是有一定区别的，相当于其绕着X轴旋转了180度，如下图

![img](https://images2015.cnblogs.com/blog/1105033/201705/1105033-20170506092034507-1009808768.png)



## 动画效果

animation 属性实现了类似 Flash 关键帧控制的动画效果。

之前的 transition 属性只能通过指定属性的初始状态和结束状态来实现动画效果，有一定局限性。所有动画更灵活。

animation 实现动画效果主要由两个部分组成：

1.通过类似 Flash 动画中的关键帧声明一个动画；

2.在 animation 属性中调用关键帧声明的动画。
![img](https://img-blog.csdn.net/20181023210421615?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM4Mzk1NDE5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

关键帧属性：@keyframes

声明一个动画，然后在 animation 调用关键帧声明的动画。

基本格式，“name”可自定义 @keyframes name { /*...*/ }
步骤：

①先创建一个基本的样式。

 animation: myani 1s ease 2 alternate 0s both;

 animation: 名称 1s；

②@keyframes 声明一个动画关键帧。 

```css
/*重复可以写一起,多组动画*/

@keyframes myani { 
	0%, 100% { background-color: white; margin-left:0px; } 
	50% { background-color: black; margin-left:100px;}
    75% { background-color:yellow; margin-left:200px;}
}
/*从什么状态过渡到什么状态*/

@keyframes myani { 
	from { background-color: white; margin-left:0px; } 
	to { background-color: black; margin-left:100px; }
 }
nav:hover ul{
animation-play-state:paused; 鼠标经过，动画暂停
}
```

③animation-name 调用@keyframes 动画 

animation-name: myani;

④animation-duration  设置动画播放的时间  注意与延迟时间的区别

animation-duration: 1s;

简写形式完整版：

animation: myani 1s ease 2 alternate 0s both;

一些概念的区别：

1、animation-timing-function //设置缓动

animation-timing-function: ease-in;

animation-direction //设置缓动方向交替 ，也是播放方向的交替，不是物体运动方向，必须先设置缓动，若缓动由快到慢，则后面会由慢到快。

animation-direction: alternate;


2、animation-fill-mode //设置结束后不在返回 ，动画播放完，默认会立即回到原位置，所以有时候需此属性控制。

animation-fill-mode: forwards;

其中both属性值 根据情况产生 forwards 或 backforwards 的效果，由次数和方向自动判断最后停留位置。

## 伸缩布局也叫弹性布局（灵活）

伸缩盒基本概念

------

布局的传统解决方案，基于[盒状模型](https://developer.mozilla.org/en-US/docs/Web/CSS/box_model)，依赖 [`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display) 属性 + [`position`](https://developer.mozilla.org/en-US/docs/Web/CSS/position)属性 + [`float`](https://developer.mozilla.org/en-US/docs/Web/CSS/float)属性。它对于那些特殊布局非常不方便，比如，[垂直居中](https://css-tricks.com/centering-css-complete-guide/)就不容易实现。

2009年，W3C 提出了一种新的方案----Flex 布局，可以简便、完整、响应式地实现各种页面布局。

对于块级元素来说，布局的延伸方向是自上而下的，也就是纵向。而对于行内元素来说，布局延伸方向是自左往右的，也就是横向。而伸缩盒呢，它的方向是可变的，既能纵向延伸，也能横向舒展，这取决于你的设置了。

#### 使用

 任何一个容器都可以指定为 Flex 布局。将display属性声明为flex或inline-flex即可~

> ```css
> .box{
>   display: flex;
> }
> ```

行内元素也可以使用 Flex 布局。

> ```css
> .box{
>   display: inline-flex;
> }
> ```

Webkit 内核的浏览器，必须加上`-webkit`前缀。

> ```css
> .box{
>   display: -webkit-flex; /* Safari */
>   display: flex;
> }
> ```

**注意，设为 Flex 布局以后，子元素的`float`、`clear`和`vertical-align`属性将失效。**

伸缩盒模型基本术语

伸缩盒模型的思想和普通的块级元素和行内元素的布局思想有较大的不同，它引入了一些新的概念和术语，通过下面这张图来了解一下：

![img](https://images2015.cnblogs.com/blog/687953/201512/687953-20151203220713783-1106695950.png)

容器默认存在两根轴：水平的主轴（main axis）和垂直的交叉轴（cross axis）。主轴的开始位置（与边框的交叉点）叫做`main start`，结束位置叫做`main end`；交叉轴的开始位置叫做`cross start`，结束位置叫做`cross end`。

项目默认沿主轴排列。单个项目占据的主轴空间叫做`main size`，占据的交叉轴空间叫做`cross size`。



#### 容器属性（大盒子）：

flex子项目在主轴的缩放比例，不制动flex属性则不参与伸缩分配

- min-width 最小值 min-width：200px 最小宽度不能小于200px
- max-width 最大值 同上

##### 1.flex-direction（调整主轴方向，默认是水平方向）

取值：

- row： 主轴与行内轴方向作为默认的书写模式。即横向从左到右排列（左对齐）。
- row-reverse： 对齐方式与row相反。
- column： 主轴与块轴方向作为默认的书写模式。即纵向从上往下排列（顶对齐）。
- column-reverse： 对齐方式与column相反。

```css
flex-direction: column;   /*垂直排列*/
1
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200801105833583.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTEzNTA2OA==,size_16,color_FFFFFF,t_70)

注意：就算子盒子有固定多少px剩下的依然按份数分

> 

##### 2.flex-wrap控制是否换行

当我们子盒子内容宽度多于父盒子时的处理

- Nowrap：默认值，规定灵活的项目不拆行不拆列
- Wrap：规定灵活的项目在必要时拆行或拆列
- Wrap-reverse：规定灵活的项目在必要时拆行或拆列，但是以相反的顺序

可以取三个值：
（1） nowrap (默认)：不换行。



![img](https://upload-images.jianshu.io/upload_images/2326131-b71b6e4c79ceb64b.png?imageMogr2/auto-orient/strip|imageView2/2/w/700/format/webp)

（2）wrap：换行，第一行在上方。



![img](https://upload-images.jianshu.io/upload_images/2326131-6de957f9ef4d43fa.jpg?imageMogr2/auto-orient/strip|imageView2/2/w/700/format/webp)

（3）wrap-reverse：换行，第一行在下方。



![img](https://upload-images.jianshu.io/upload_images/2326131-b432b2461d51d73a.jpg?imageMogr2/auto-orient/strip|imageView2/2/w/700/format/webp)

##### 3.flex-flow是flex-direction、flex-wrap的简写形式

> Flex-flow：flex-direction flex-wrap；
> Flex-flow：排列方向 换不换行；

例：

```css
flex-flow: row wrap;
默认值为row nowrap
```

##### 4.justify-content 调整主轴对齐（水平）

设置或检索弹性盒子元素在主轴(横轴)方向上的对齐方式。

当弹性盒里一行上的所有子元素都不能伸缩或已经达到其最大值时，这一属性可协助对**多余的空间进行分配**。当元素溢出某行时，这一属性同样会在对齐上进行控制。

对应的脚本特性为justifyContent。

- 让子元素从父元素的开头开始排序父元素的

> justify-content: flex-start;

- 让子元素从父元素的结尾开始排序，但是顺序不变

> justify-content: end;

- 让子元素在中间排序，但是顺序不变

> justify-content: center;

- 左右的盒子贴近父盒子，中间的平均分布空白间隙

> justify-content: space-between;

- 相当于给每个盒子添加左右margin外边距

> justify-content: space-around;

![img](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071010.png)

> 

##### 5.align-content堆栈（由flex-wrap产生独立行）对齐

Align-content是针对flex容器里面多轴（多行）的情况，align-items是针对（单行)的情况下排列。**属性定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用**。

前提：

必须对父元素设置自由盒子属性 display：flex；并且设置排列方式为横向排列flex-direction：row；这样才能起作用

值：

- Stretch：默认值，项目被拉伸以适应容器
- Center：项目位于容器的中心
- Flex-start：项目位于容器的开头
- Flex-end：项目位于容器的结尾
- Space-between：项目位于各行之间留有空白的容器内
- Space-around：项目位于各行之前、之间、之后都留有空白的容器内

![img](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071012.png)

##### 6. align-items属性（调整纵轴的对齐方式）

align-items 属性定义flex子项在flex容器的当前行的侧轴（纵轴）方向上的对齐方式。

 align-items 调整侧轴对齐（垂直）单行比较多

- 垂直对齐开始位置 上对齐

> align-items: flex-start;

- 垂直对齐开始位置 底对齐

> align-items: flex-end;

- 垂直居中

> align-items: center;

- 让子元素的高度拉伸适用于父容器（子元素不加高度的前提下）

> align-items: stretch;

| 值         | 描述                           |
| ---------- | ------------------------------ |
| stretch    | 默认值。项目被拉伸以适应容器。 |
| center     | 项目位于容器的中心。           |
| flex-start | 项目位于容器的开头。           |
| flex-end   | 项目位于容器的结尾。           |
| baseline   | 项目位于容器的基线上。         |

![img](https:////upload-images.jianshu.io/upload_images/2326131-b3099f9b3e8bea50.png?imageMogr2/auto-orient/strip|imageView2/2/w/617/format/webp)

#### 弹性子元素属性（小盒子）

| 属性        | 描述                                                         |
| ----------- | ------------------------------------------------------------ |
| order       | 设置弹性盒子的子元素排列顺序。                               |
| flex-grow   | 设置或检索弹性盒子元素的扩展比率。                           |
| flex-shrink | 指定了 flex 元素的收缩规则。flex 元素仅在默认宽度之和大于容器的时候才会发生收缩，其收缩的大小是依据 flex-shrink 的值。 |
| flex-basis  | 用于设置或检索弹性盒伸缩基准值。                             |
| flex        | 设置弹性盒子的子元素如何分配空间。                           |
| align-self  | 在弹性子元素上使用。覆盖容器的 align-items 属性。            |

##### 1. order属性（定义盒子的排列顺序）



```css
.flex-container .flex-item { order: <integer>; }
```

<integer>：用整数值来定义排列顺序，数值小的排在前面。可以为负值，默认为0。



![img](https:////upload-images.jianshu.io/upload_images/2326131-5466d2ec3968ca3b.png?imageMogr2/auto-orient/strip|imageView2/2/w/751/format/webp)

##### 2. flex-grow属性



```css
.flex-container .flex-item { flex-grow: <integer>; }
```

<integer>：一个数字，规定项目将相对于其他灵活的项目进行扩展的量。默认值是 0。



![img](https:////upload-images.jianshu.io/upload_images/2326131-189a57eada2a12a8.png?imageMogr2/auto-orient/strip|imageView2/2/w/802/format/webp)

##### 3. flex-shrink属性



```css
.flex-container .flex-item { flex-shrink: <integer>; }
```

<integer>：一个数字，规定项目将相对于其他灵活的项目进行收缩的量。默认值是 1。



![img](https:////upload-images.jianshu.io/upload_images/2326131-b55c4a8caa6d3a90.jpg?imageMogr2/auto-orient/strip|imageView2/2/w/700/format/webp)

##### 4. flex-basis属性



```css
.flex-container .flex-item { flex-basis: <integer> | auto; }
```

<integer>：一个长度单位或者一个百分比，规定元素的初始长度。
 auto：默认值。长度等于元素的长度。如果该项目未指定长度，则长度将根据内容决定。

##### 5. flex属性

flex 属性用于设置或检索弹性盒模型对象的子元素如何分配空间。

flex 属性是 flex-grow、flex-shrink 和 flex-basis 属性的简写属性。



```css
.flex-container .flex-item { flex: flex-grow flex-shrink flex-basis | auto | initial | inherit; }
```

| 值          | 描述                                                         |
| ----------- | ------------------------------------------------------------ |
| flex-grow   | 一个数字，规定项目将相对于其他元素进行扩展的量。             |
| flex-shrink | 一个数字，规定项目将相对于其他元素进行收缩的量。             |
| flex-basis  | 项目的长度。合法值："auto"、"inherit" 或一个后跟 "%"、"px"、"em" 或任何其他长度单位的数字。 |
| auto        | 与 1 1 auto 相同。                                           |
| none        | 与 0 0 auto 相同。                                           |
| initial     | 设置该属性为它的默认值，即为 0 1 auto。                      |
| inherit     | 从父元素继承该属性。                                         |

为了形象说明，我们用代码来解释。

```
<div class="container">
  <div class="item item-1">item 1</div>
  <div class="item item-2">item 2</div>
  <div class="item item-3">item 3</div>
</div>
```

CSS设置为：

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```
.container {
  display: flex;
  width: 300px;
  height: 100px;
  ...
}
```

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

在这里`display: inline-flex;`好像也可以。
对于其中的伸缩项元素，我们需要给他们事先安排好住房面积比例，我们就用最简单最健康的1:1:1吧~我们将比例声明在`flex`属性里

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```
.item-1 {
  flex: 1;
  ...
}
.item-2 {
  flex: 1;
  ...
}
.item-3 {
  flex: 1;
  ...
}
```

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

![img](https://images2015.cnblogs.com/blog/687953/201512/687953-20151203221002768-1547354806.jpg)

我们的大房子被完美地平分成三个隔间了，三家平分房租！

如果有人想住大点的房子，我们直接改变`flex`的比例即可：

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```
.item-1 {
  flex: 1;
  ...
}
.item-2 {
  flex: 1;
  ...
}
.item-3 {
  flex: 2;
  ...
}
```

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

![img](https://images2015.cnblogs.com/blog/687953/201512/687953-20151203221039361-265094036.jpg)

是不是很方便？

##### 6. align-self属性



```css
.flex-container .flex-item {
    align-self: auto | stretch | center | flex-start | flex-end | baseline | initial | inherit;
}
```

| 值         | 描述                                                         |
| ---------- | ------------------------------------------------------------ |
| auto       | 默认值。元素继承了它的父容器的 align-items 属性。如果没有父容器则为 "stretch"。 |
| stretch    | 元素被拉伸以适应容器。                                       |
| center     | 元素位于容器的中心。                                         |
| flex-start | 元素位于容器的开头。                                         |
| flex-end   | 元素位于容器的结尾。                                         |
| baseline   | 元素位于容器的基线上。                                       |
| initial    | 设置该属性为它的默认值。                                     |
| inherit    | 从父元素继承该属性。                                         |

![img](https:////upload-images.jianshu.io/upload_images/2326131-8dc02c66cf79f0e8.png?imageMogr2/auto-orient/strip|imageView2/2/w/743/format/webp)

取值同 align-items。

**Reference**
 [阮一峰老师·Flex布局教程](https://link.jianshu.com?t=http%3A%2F%2Fwww.ruanyifeng.com%2Fblog%2F2015%2F07%2Fflex-grammar.html)
 [runoob·Flex布局](https://link.jianshu.com?t=http%3A%2F%2Fwww.runoob.com%2Fcss3%2Fcss3-flexbox.html)

## 浏览器内核

浏览器工作过程

**1、DNS 解析**

**2、TCP 连接**

**3、HTTP 请求**

**4、构建 DOM 树**

**5、构建 CSSOM 树**

**6、生成渲染树**

**7、合成、绘制**

四大内核分别是：Trident、webkit、Blink、Gecko
1、Trident内核（IE浏览器内核）：俗称的IE内核

2、Gecko内核（Firefox浏览器内核）：俗称Firefox内核

3、Blink内核（Chrome浏览器内核）：也称Chromium内核；Chrome浏览器以前是Webkit内核，现在是Blink内核，其实Blink就是Webkit的分支，Opera也用

4、Webkit内核（Safari浏览器内核）：苹果浏览器的内核，最早是苹果公司开发的内核，后来谷歌借来使用，谷歌这么牛的公司怎么会一直使用别人的内核呢，所以Google自己开发了Blink内核

##  关于script标签的位置

我们大都会将script标签放在**body结束标签之前**，**在</body>之后插入其他元素，从HTML 2.0起就是不合标准的。（串行）**

因为Javascript的加载和执行的特点： 
（1）载入后马上执行； 
（2）执行时会阻塞页面后续的内容（包括页面的渲染、其它资源的下载）。原因：因为浏览器需要一个稳定的DOM树结构，而JS中很有可能有 代码直接改变了DOM树结构，比如使用 document.write 或 appendChild,甚至是直接使用的location.href进行跳转，浏览器为了防止出现JS修 改DOM树，需要重新构建DOM树的情况，所以 就会阻塞其他的下载和呈现。

减少 JavaScript 对性能的影响的方法：
将所有的script标签放到页面底部，也就是body闭合标签之前，这能**确保**在脚本执行前页面已经**完成了DOM树渲染**。
尽可能地合并脚本。**页面中的script标签越少，加载也就越快，响应也越迅速。**无论是外链脚本还是内嵌脚本都是如此。

采用无阻塞下载 JavaScript 脚本的方法： 
（1）使用script标签的 defer 属性（仅适用于 IE 和 Firefox 3.5 以上版本）； 
（2）使用动态创建的script元素来下载并执行代码；

###  现在推荐的解决方案：

现在浏览器script标签支持 `async` 和 `defer` 属性. 应用这些属性当script被下载时，浏览器更安全而且可以并行下载（下载script并不阻断HTML解析）。

 async（异步并行）

```text
<script type="text/javascript" src="path/to/script1.js" async></script>
<script type="text/javascript" src="path/to/script2.js" async></script>
```

async标记的Script异步执行下载，并执行。这意味着script下载时并不阻塞HTML的解析，并且下载结束script马上执行。
异步意味着，上述代码script2可能比script1先下载完并执行完。

根据 [http://caniuse.com/#feat=script-async](https://link.zhihu.com/?target=http%3A//caniuse.com/%23feat%3Dscript-async), 90% 的浏览器支持async属性.

 defer

```text
<script type="text/javascript" src="path/to/script1.js" defer></script>
<script type="text/javascript" src="path/to/script2.js" defer></script>
```

defer标签的script顺序执行。这种方式也不会阻断浏览器解析HTML。

跟 async不同, defer scripts在整个文档里的script都被下载完才**顺序执行**。

根据 [http://caniuse.com/#feat=script-defer](https://link.zhihu.com/?target=http%3A//caniuse.com/%23feat%3Dscript-defer), 90% 的浏览器支持这个属性. 92% 至少部分支持此属性。

注意：在 IE <= 9 浏览器应用defer属性可能会导致script不会顺序执行。如果你想让低版本IE支持此属性，请看 [this](https://link.zhihu.com/?target=https%3A//github.com/h5bp/lazyweb-requests/issues/42) 

结论

应用 `async` or `defer`这两个属性，拥抱未来。

原答案来自万能的： [stackoverflow](https://link.zhihu.com/?target=https%3A//stackoverflow.com/questions/436411/where-should-i-put-script-tags-in-html-markup)

# PS

ctrl+k打开首选项

.psd原文件，自己保留，可以修改
.jpg给客户的，不可修改
ctrl+o打开 ctrl+w关闭 ctrl+t旋转
shift 等比例缩放   alt可以再复制一个或者ctrl+j
shift选中多个图层可以一起移动
ctrl+g图层分组 ctrl+shift+g取消图层分组
图层排在上面，图片中也排在上面
ctrl+] 向上移动图层   ctrl+[向下移动图层
ctrl+shift+]  图层置顶 ctrl+shift+[图层置底
ctrl+z撤销一步 ctrl+alt+z撤销多步
ctrl+e合并图层 ctrl++放大
shift+alt选中 
先建图层再画，不然不能单独动。要移动先点击移动工具

ctrl+shift+i反选

## 选区布尔运算

选区面积大小的变化。

新选区：保持选中状态

添加到选区：相加运算（按住shift再绘制选区）

从选区减去：相减（按住alt再绘制选区）

与选区交叉：重合部分保留。（按住alt+shift再绘制选区）

