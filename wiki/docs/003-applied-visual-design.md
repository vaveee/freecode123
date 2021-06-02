### 使用 text-align 属性创建视觉平衡
web 内容大部分都是文本。CSS 里面的text-align属性可以控制文本的对齐方式。

|   text-align  | 对齐  |
|  ----  | ----  |
| text-align: justify;  | 两端对齐 |
| text-align: center;  | 居中对齐 |
| text-align: right;  | 右对齐 |
| text-align: left;  | 默认值，左对齐 |


### 使用 width 属性调整元素的宽度
width属性来指定元素的宽度。属性值可以是相对单位（比如 em），绝对单位（比如 px），或者包含块（父元素）宽度的百分比。下面这个例子把图片的宽度设置为 220px：
```
img {
  width: 220px;
}
```
### 使用 height 属性调整元素的宽度
和width属性类似，你可以使用 CSS 里面的height属性来指定元素的高度。下面这个例子把图片的高度设置为 20px：
```
img {
  height: 20px;
}
```
### 使用 strong 标签加粗文本
Strong ⇒ s ⇒ 加粗。

你可以使用strong标签来加粗文字。添加了strong标签后，浏览器会自动给元素应用font-weight:bold;。

### 使用 u 标签给文本添加下划线
Underline ⇒ u ⇒ 下划线。

你可以使用u标签来给文字添加下划线。添加了u标签后，浏览器会自动给元素应用text-decoration: underline;。

### 使用 em 标签强调文本
emphasis ⇒ em ⇒ 强调。

你可以使用em标签来强调文本。由于浏览器会自动给元素应用font-style: italic;，所以文本会显示为斜体。

### 使用 s 标签给文本添加删除线
Strikethrough ⇒ s ⇒ 删除线。

你可以用s标签来给文字添加删除线，我是明晃晃的删除线，它代表着这段文字不再有效。添加了s标签后，浏览器会自动给元素应用text-decoration: line-through;。

### 使用 hr 标签创建水平线
Horizontal Rule ⇒ hr ⇒ 水平线。

你可以用hr标签来创建一条宽度撑满父元素的水平线。它一般用来表示文档主题的改变，在视觉上将文档分隔成几个部分。

### 调整文本的背景色
设置文字的背景色，在文字的父元素上添加background-color属性。
之前学到的hex编码或者rgb()颜色，我们也可以使用rgba()选择颜色。

rgba 代表：
```
r = red 红色
g = green 绿色
b = blue 蓝色
a = alpha 透明度
```
RGB 值可以在 0 到 255 之间。alpha 值可以在 0 到 1 之间，其中 0 代表完全透明，1 代表完全不透明。rgba()非常棒，因为你可以设置颜色的透明度，这意味着你可以做出一些很漂亮的半透明效果。

### 调整标题与段落的大小
使用font-size属性来设置元素内文字的大小。

### 给卡片元素添加 box-shadow
box-shadow属性用来给元素添加阴影，由逗号分隔的一个或多个阴影列表。

box-shadow属性的每个阴影依次由下面这些值描述：
```
*offset-x  x偏移量；
*offset-y  y偏移量;
*blur-radius  阴影扩散半径；
*spread-radius 阴影扩散半径；
*颜色
```
颜色。 其中blur-raduis和spread-raduis是可选的。

下面是创建了多个阴影的 CSS 例子，阴影加了模糊效果，颜色是透明度很高的黑色:

`box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);`
```
/* x偏移量 | y偏移量 | 阴影颜色 */
box-shadow: 60px -16px teal;

/* x偏移量 | y偏移量 | 阴影模糊半径 | 阴影颜色 */
box-shadow: 10px 5px 5px black;

/* x偏移量 | y偏移量 | 阴影模糊半径 | 阴影扩散半径 | 阴影颜色 */
box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);

/* 插页(阴影向内) | x偏移量 | y偏移量 | 阴影颜色 */
box-shadow: inset 5em 1em gold;

/* 任意数量的阴影，以逗号分隔 */
box-shadow: 3px 3px red, -1em 0 0.4em olive;
```
### 降低元素的透明度
opacity属性用来设置元素的透明度。

值 1 代表完全不透明。
值 0.5 代表半透明。
值 0 代表完全透明。

透明度会应用到元素内的所有内容，不论是图片，还是文本，或是背景色。

### 使用 text-transform 属性给文本添加大写效果
CSS 里面的text-transform属性来改变英文中字母的大小写。它通常用来统一页面里英文的显示，且无需直接改变 HTML 元素中的文本。

下面的表格展示了text-transform的不同值对文字 “Transform me” 的影响。

|值|	效果|
|  ----  | ----  |
|lowercase|	“transform me”|
|uppercase|	“TRANSFORM ME”|
|capitalize|	“Transform Me”|
|initial|	使用默认值|
|inherit|	使用父元素的text-transform值。|
|none	|Default:不改变文字。|

### 设置多个标题元素的 font-size
font-size属性用来指定元素内标题文字的大小。规则可以应用到多个元素上，合理的使用，能让页面的文字显示的错落有致。

### 设置多个标题元素的 font-weight
font-weight属性用于设置文本中所用的字体的粗细。

### 设置段落文本的 font-size
CSS 里面的font-size属性不只限于标题，它可以应用于任何包含文字的元素内。


### 设置段落的 line-height
CSS 提供line-height属性来设置行间的距离。行高，顾名思义，用来设置每行文字所占据的垂直空间。

### 调整锚点的悬停状态
本挑战将要涉及到伪类。伪类是可以添加到选择器上的关键字，用来选择元素的指定状态。

比如，超链接可以使用:hover伪类选择器定义它的悬停状态样式。下面是悬停超链接时改变超链接颜色的 CSS：
```
a:hover {
  color: red;
}
```
### 更改元素的相对位置
在 CSS 里一切 HTML 元素皆为盒子，也就是通常所说的盒模型。块级元素自动从新的一行开始（比如标题、段落以及 div），行内元素排列在上一个元素后（比如图片以及 span）。元素默认按照这种方式布局称为文档的普通流，同时 CSS 提供了 position 属性来覆盖它。

当元素的 position 设置为relative时，它允许你通过 CSS 指定该元素在当前普通流页面下的相对偏移量。 CSS 里控制各个方向偏移量的对应的属性是left、right、top和bottom。它们代表着从原来的位置向对应的方向偏移指定的像素、百分比或者 ems。下面的例子展示了段落向上偏移 10 像素：
```
p {
  position: relative;
  bottom: 10px;
}
```
把元素的 position 设置成 relative 并不会改变该元素在普通流布局所占的位置，也不会对其它元素的位置产生影响。

### 使用 CSS 偏移移动相对定位的元素
CSS 里面的top、bottom、left和right定义了元素在相应方位的偏移距离。元素将从当前位置，向属性相反的方向偏移。就像你在上一个挑战看到的，top属性使h2向下移动。left属性使元素向右移动。

![alt 属性文本](./image/eWWi3gZ.gif)

### 绝对定位的参照物是元素的父元素
position属性的取值选项absolute，absolute相对于其包含块(父元素)定位。

和relative定位不一样，absolute定位会将元素从当前的文档流里面移除，周围的元素会忽略它。可以用 CSS 的 top、bottom、left 和 right 属性来调整元素的位置。

absolute定位比较特殊的一点是元素的定位参照于最近的已定位祖先元素。

如果它的父元素没有添加定位规则（通常是position:relative;）,浏览器会继续寻找直到默认的 body 标签。

### 固定定位的参照物是浏览器的窗口

是fixed定位是一种特殊的绝对（absolute）定位，区别是其包含块是浏览器窗口。和绝对定位类似，fixed定位使用 top、bottom、left 和 right 属性来调整元素的位置，并且会将元素从当前的文档流里面移除，其它元素会忽略它的存在。

fixed定位和absolute定位的最明显的区别是fixed定位元素不会随着屏幕滚动而移动。

### 使用 float 属性将元素左浮动或右浮动
接下来要介绍的定位机制并不是position属性的选项，它通过元素的float属性来设置。
浮动元素不在文档流中，它向左或向右浮动，直到它的外边缘碰到包含框或另一个浮动框的边框为止。通常需要用width属性来指定浮动元素占据的水平空间。

### 使用 z-index 属性更改重叠元素的位置
当一些元素重叠时，后出现的元素默认显示在更早出现的元素的上面。你可以使用z-index属性指定元素的堆叠次序。z-index的取值是整数，数值大的元素优先于数值小的元素显示。

给 class 为first的元素（红色的方块）添加z-index属性并赋值为 2，使它显示在蓝色方块的上方。

 ```
<style>
  div {
    width: 60%;
    height: 200px;
    margin-top: 20px;
  }
 
  .first {
    background-color: red;
    position: absolute;
 
  }
  .second {
    background-color: blue;
    position: absolute;
    left: 40px;
    top: 50px;
    z-index: 1;
  }
</style>
 
<div class="first"></div>
<div class="second"></div>
```

### 使用 margin 属性将元素水平居中
在应用设计中经常需要把一个块级元素水平居中显示。一种常见的实现方式是把块级元素的margin值设置为auto。

同样的，这个方法也对图片奏效。图片默认是内联元素，但是可以通过设置其display属性为block来把它变成块级元素。

### 了解互补色
色彩理论以及设计色彩学很复杂，这里将只涉及很基础的部分。在网站设计里，颜色能让内容更醒目，能调动情绪，从而创造舒适的视觉体验。不同的颜色组合对网站的视觉效果影响很大，精妙的设计都需要适宜的颜色来美化页面内容。

一半是科学，一半是艺术，色环是我们认识颜色关系的好工具 - 它是一个近色相邻异色相离的圆环。当两个颜色恰好在色环的两端时，这两个颜色叫做补色。绘画中两只补色在混合后会变成灰色。补色搭配能形成强列的对比效果，传达出活力、能量、兴奋等意义。

下面是一些十六进制码（hex code）补色的例子：

红色（#FF0000）和蓝绿色 (#00FFFF)
绿色（#00FF00）和品红色（#FF00FF）
蓝色（#0000FF）和黄色（#FFFF00）
现在很多的在线选色工具都有寻找补色的功能。

### 了解三次色
电脑显示器和手机屏幕是一种加色模型，将红（R）、绿（G）、蓝（B）三原色的色光以不同的比例相加，以产生多种多样的色光。两种原色相加产生二次色：蓝绿（G+B）、品红（R+B）和黄色（R+G）。你在上一个挑战里已经见过这些颜色了。这些二次色恰好是在合成它们时未使用的原色的补色，即在色环中位于两端。例如，品红色是红色和蓝色相加产生，它是绿色的补色。

三次色是由原色和二次色相加产生的颜色，例如红色（原色）和黄色（二次色）相加产生橙色。将这六种颜色中相邻的颜色相加，便产生了十二色色环。

设计里面有很多种颜色搭配方法。涉及到三次色的一种配色方法是分裂补色搭配法。选定主色之后，在色环上选择与它的补色相邻的两种颜色与之搭配。此种搭配既有对比，又不失和谐。

下面是使用分裂补色搭配法创建的三个颜色：

|颜色	|HEX 颜色码|
|  ----  | ----  |
|橙色	|#FF7D00|
|蓝绿色|	#00FFFF|
|树莓红	|#FF007D|

### 将各种元素的颜色调整为互补色
通过前面关卡的学习，我们知道了补色搭配能形成强列的对比效果，让内容更富生机。但是如果使用不当效果会适得其反，比如如果文字背景色和文字颜色互为补色，文字会很难看清。通常的做法是，一种颜色做为主要颜色，其补色用来装点页面。
### 调整颜色的色相
HSL 色彩空间模型是一种将 RGB 色彩模型中的点放在圆柱坐标系中的表示法，描述了色相（hue）、饱和度（saturation）、亮度（lightness）。CSS3 引入了对应的hsl()属性做为对应的颜色描述方式。

色相是色彩的基本属性，就是平常所说的颜色名称，如红色、黄色等。以颜色光谱为例，光谱左边从红色开始，移动到中间的绿色，一直到右边的蓝色，色相值就是沿着这条线的取值。在hsl()里面，色相用色环来代替光谱，色相值就是色环里面的颜色对应的从 0 到 360 度的角度值。

饱和度是指色彩的纯度，也就是颜色里灰色的占比，越高色彩越纯，低则逐渐变灰，取0-100%的数值。

亮度决定颜色的明暗程度，也就是颜色里白色或者黑色的占比，100% 亮度是白色， 0% 亮度是黑色，而 50% 亮度是“一般的”。

下面是一些使用hsl()描述颜色的例子，颜色都为满饱和度，中等亮度:

|颜色|	HSL|
|  ----  | ----  |
|橙色	|#FF7D00|
|红|	hsl(0, 100%, 50%)|
|黄|	hsl(60, 100%, 50%)|
|绿|	hsl(120, 100%, 50%)|
|蓝绿	|hsl(180, 100%, 50%)|
|蓝	|hsl(240, 100%, 50%)|
|品红	|hsl(300, 100%, 50%)|
### 调整颜色的色调
hsl()使 CSS 更改色调更方便。给纯色添加白色可以创造更浅的色调，添加黑色可以创造更深的色调。另外，还可以通过给纯色添加灰色来同时改变颜色的深浅和明暗。回忆下hsl()里面的‘s’和‘l’分辨代表饱和度和亮度。饱和度代表灰色的占比，亮度代表白色和黑色的占比。这在当你有了一个基色调却需要微调时非常有用。
### 创建一个 CSS 线性渐变
HTML 元素的背景色并不局限于单色。CSS 还提供了颜色过渡，也就是渐变。可以通过background里面的linear-gradient()来实现线性渐变，下面是它的语法：

`background: linear-gradient(gradient_direction, 颜色 1, 颜色 2, 颜色 3, ...);`
第一个参数指定了颜色过渡的方向 - 它的值是角度，90deg 代表垂直渐变，45deg 的渐变角度和反斜杠方向差不多。剩下的参数指定了渐变颜色的顺序：

例子：

`background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255));`
使用linear-gradient()给div添加background渐变色，渐变角度 35deg，从#CCFFFF过渡到#FFCCCC。
### 使### 用 CSS 线性渐变创建条纹元素
repeating-linear-gradient()函数和linear-gradient()很像，主要区别是repeating-linear-gradient()重复指定的渐变。 repeating-linear-gradient()有很多参数，为了便于理解，本关只用到角度值和起止渐变颜色值。

角度就是渐变的方向。起止渐变颜色值代表渐变颜色及其宽度值，由颜色值和起止位置组成，起止位置用百分比或者像素值表示。

在代码编辑器的例子里，渐变开始于 0 像素位置的yellow，然后过渡到距离开始位置 40 像素的blue。由于下一个起止渐变颜色值的起止位置也是 40 像素，所以颜色直接渐变成第三个颜色值green，然后过渡到距离开始位置 80 像素的red。

下面的代码可以帮助理解成对的起止渐变颜色值是如何过渡的。

0px [黄色 -- 过渡 -- 蓝色] 40px [绿色 -- 过渡 -- 红色] 80px
如果每对起止渐变颜色值的颜色都是相同的，由于是在两个相同的颜色间过渡，那么中间的过渡色也为同色，接着就是同色的过渡色和下一个起止颜色，最终产生的效果就是条纹。


### 添加细微图案作为背景图像来创建纹理
添加一个精致的背景图，可以增加页面的质感，让页面更美观。需要找到一个平衡点，不能抢了内容的风头，喧宾夺主可就不妙了。使用background属性，使用url()函数包含链接的方式引入一个指定纹理或样式的图片。图片链接地址在括号内，一般会用引号包起来。

### 使用 CSS Transform scale 属性可以更改元素的大小
CSS 属性transform里面的scale()函数，可以用来改变元素的显示比例。下面的例子把页面的段落元素放大了 2 倍：
```
p {
 transform:scale(2);
}
```
### 使用CSS Transform scale 属性在悬停时缩放元素
transform属性有很多函数，可以对元素进行
调整大小scale(x,y)或scaleX(x)或scaleY(y)、
移动translate(x,y) 或者translateX(x)或者translateY(y)、
倾斜skew(x-angle,y-angle)或者skewX(angle)或者skewY(angle)、
旋转rotate(angle)或rotateX(angle)或rotateY(angle)
等操作。当使用伪类描述元素的指定状态如:hover时，transform属性可以方便的给元素添加交互。

下面是当用户悬停段落元素时，段落大小缩放到原始大小 2.1 倍的例子：
```
p:hover {
  transform: scale(2.1);
}
```
参考：https://www.cnblogs.com/EricZLin/p/8872280.html
### 使用 CSS Transform skex 属性沿X轴倾斜元素
接下来要介绍的transform属性是skewX，skewX使选择的元素沿着 X 轴（横向）翻转指定的角度。

下面的代码沿着 X 轴翻转段落元素 -32 度。
```
p {
  transform: skewX(-32deg);
}
```
### 使用 CSS Transform skex 属性沿Y轴倾斜元素
skewX函数使指定元素沿 X 轴偏斜指定的角度，想必你已经猜到了，skewY属性使指定元素沿 Y 轴（垂直方向）偏斜指定角度。

### 使用 CSS 创建一个图形（新月）
术语表：
blur-radius ⇒ 模糊半径，
spread-radius ⇒ 辐射半径，
transparent ⇒ 透明的，
border-radius ⇒ 圆角边框。

通过使用选择器选择不同的元素并改变其属性，你可以创造一些有趣的形状。
比如新月。你可以使用box-shadow属性来设置元素的阴影，border-radius属性控制元素的圆角边框。

首先你将会创建一个圆的、透明的对象，它具有模糊阴影并略微向两边递减。如你所见，这个阴影其实就是新月形狀。

为了创建一个圆形的对象，border-radius应该被设置成 50%。

你应该还记得之前关卡的box-shadow属性以及它的依次取值offset-x、offset-y、blur-radius、spread-radius和颜色值。其中blur-radius和spread-radius是可选的。

把编辑器里的正方形元素变成新月形状。

首先，把background-color改为 transparent，
接着把border-radius属性设置成 50%，以创建一个圆形。
最后，更改box-shadow属性，使其offset-x为 25px，offset-y为 10px，blur-radius为 0，spread-radius为 0，color为 blue。
```
<style>
  .center {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    width: 100px;
    height: 100px;
    background-color: transparent;
    border-radius: 50%;
    box-shadow: 25px 10px 0 0 blue;
  }

</style>
<div class="center"></div>
```
### 使用 CSS 和 HTML 创建更复杂的形状（心形）
世界上最流行的形状非心形莫属了，在本关里你将用纯 CSS 创建一个心形。
但是首先你需要了解:before和:after伪类。这些伪类用来在选择元素之前和之后添加一些内容。
在下面的例子里，:before伪类元素用来给 class 为heart的元素添加一个正方形。
```
.heart:before {
  content: "";
  background-color: yellow;
  border-radius: 25%;
  position: absolute;
  height: 50px;
  width: 70px;
  top: -50px;
  left: 5px;
}
 ```
:before和:after必须配合content来使用。这个属性通常用来给元素添加内容诸如图片或者文字。
当:before和:after伪类用来添加某些形状而不是图片或文字时，content属性仍然是必需的，但是它的值可以是空字符串。

在上面的例子里，class 为heart元素的:before伪类添加了一个黄色的长方形，长方形的height和width分别为 50px 和 70px。由于设置了其边框半径为 25%，所以长方形为圆角长方形，同时其相对位置为距离left5px，以及向top偏移 50px。

```
<style>
  .heart {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: pink;
    height: 50px;
    width: 50px;
    transform: rotate(-45deg);
  }
  .heart::after {
    background-color: pink;
    content: "";
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: 0px;
    left: 25px;
  }
  .heart::before {
    content:  "";
    background-color: pink;
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: -25px;
    left: 0px;
  }
</style>
<div class="heart"></div>
```

### 了解 CSS 的关键帧和动画是如何工作的

### 使用CSS动画更改按钮的悬停状态
### 修改动画的填充模式
### 使用 CSS 动画创建动画
### 从左到右淡化元素来创建视觉方向
### 使用无限的动画计数制作永不停止的动画
### 使用无限的动画计数制作 CSS 心跳
### 以可变速率来给元素添加动画
### 以可变速率来给多个元素添加动画
### 使用关键字更改动画定时器
### 学习贝塞尔曲线的原理
### 使用贝塞尔曲线移动图形
### 使用贝塞尔曲线让运动更加自然