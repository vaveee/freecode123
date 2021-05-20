### 使用 text-align 属性创建视觉平衡
web 内容大部分都是文本。CSS 里面的text-align属性可以控制文本的对齐方式。

text-align: justify;两端对齐。

text-align: center;居中对齐。

text-align: right;右对齐。

text-align: left;默认值，左对齐。

### 使用 width 属性调整元素的宽度
width属性来指定元素的宽度。属性值可以是相对单位（比如 em），绝对单位（比如 px），或者包含块（父元素）宽度的百分比。下面这个例子把图片的宽度设置为 220px：
```
img {
  width: 220px;
}
```
### 使用 height 属性调整元素的高度
和width属性类似，你可以使用 CSS 里面的height属性来指定元素的高度。下面这个例子把图片的高度设置为 20px：
```
img {
  height: 20px;
}
```
### 使用 strong 标签加粗文本
术语：Strong ⇒ s ⇒ 加粗。

你可以使用strong标签来加粗文字。添加了strong标签后，浏览器会自动给元素应用font-weight:bold;。


### 使用 u 标签给文本添加下划线
术语：Underline ⇒ u ⇒ 下划线。

你可以使用u标签来给文字添加下划线。添加了u标签后，浏览器会自动给元素应用text-decoration: underline;。

### 使用 em 标签强调文本
术语：emphasis ⇒ em ⇒ 强调。

你可以使用em标签来强调文本。由于浏览器会自动给元素应用font-style: italic;，所以文本会显示为斜体。
### 使用 s 标签给文本添加删除线
术语：Strike through ⇒ s ⇒ 删除线。

你可以用s标签来给文字添加删除线，我是明晃晃的删除线，它代表着这段文字不再有效。添加了s标签后，浏览器会自动给元素应用text-decoration: line-through;。
### 使用 hr 标签创建水平线
术语：Horizontal Rule ⇒ hr ⇒ 水平线。

你可以用hr标签来创建一条宽度撑满父元素的水平线。它一般用来表示文档主题的改变，在视觉上将文档分隔成几个部分。
### 调整文本的背景色
为了让页面更美观，除了设置整个页面的背景色以及文字颜色外，你还可以单独设置文字的背景色，即在文字的父元素上添加background-color属性。
```
r = red 红色
g = green 绿色
b = blue 蓝色
a = alpha 透明度
```
`background-color: rgba(45, 45, 45, 0.1)。`它表示背景是黑灰色，因为设置了透明度为 0.1

### 调整标题与段落的大小
使用font-size属性来设置元素内文字的大小。
### 给卡片元素添加 box-shadow
box-shadow属性用来给元素添加阴影，该属性值是由逗号分隔的一个或多个阴影列表。
```
box-shadow属性的每个阴影依次由下面这些值描述：
*offset-x阴影的水平偏移量；
*offset-y阴影的垂直偏移量;
*blur-radius模糊距离；
*spread-radius阴影尺寸；
```
下面是创建了多个阴影的 CSS 例子，阴影加了模糊效果，颜色是透明度很高的黑色:

`box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);`


### 降低元素的透明度
CSS 里的opacity属性用来设置元素的透明度。
```
值 1 代表完全不透明。
值 0.5 代表半透明。
值 0 代表完全透明。
```
### 使用 text-transform 属性给文本添加大写效果
CSS 里面的text-transform属性来改变英文中字母的大小写。

|Value	|Result  |
|  ----  | ----  |
| lowercase	| "transform me"|
| uppercase	| "TRANSFORM ME"|
| capitalize	| "Transform Me"|
| initial	| 使用默认值|
| inherit	| 使用父元素的text-transform值。|
| none	| Default:不改变文字。|

### 设置多个标题元素的 font-size
font-size属性用来指定元素内文字的大小。
### 设置多个标题元素的 font-weight
font-weight属性用于设置文本中所用的字体的粗细。
### 设置段落文本的 font-size
CSS 里面的font-size属性不只限于标题，它可以应用于任何包含文字的元素
### 设置段落的 line-height
line-height属性来设置行间的距离。行高，顾名思义，用来设置每行文字所占据的垂直空间。
### 调整锚点的悬停状态
超链接可以使用:hover伪类选择器定义它的悬停状态样式。下面是悬停超链接时改变超链接颜色的 CSS：
```
a:hover {
  color: red;
}
```
### 更改元素的相对位置
当元素的 position 设置为relative时，它允许你通过 CSS 指定该元素在当前普通流页面下的相对偏移量.
下面的例子展示了段落向上偏移 10 像素：
```
p {
  position: relative;
  bottom: 10px;
}
```

### 使用 CSS 偏移移动相对定位的元素
各个方向偏移量的对应的属性是left、right、top和bottom。它们代表着从原来的位置向对应的方向偏移量。
把元素的 position 设置成 relative 并不会改变该元素在普通流布局所占的位置，也不会对其它元素的位置产生影响。
```
h2 {
  position: relative;
  bottom: 10px;
  left:15px;
}
```

### 绝对定位的参照物是元素的父元素
absolute定位参照于最近的已定位祖先元素。如果它的父元素没有添加定位规则（通常是position:relative;）,浏览器会继续寻找直到默认的 body 标签。
和relative定位不一样，absolute定位会将元素从当前的文档流里面移除，周围的元素会忽略它。可以用 CSS 的 top、bottom、left 和 right 属性来调整元素的位置。
```
#searchbar {
position:absolute;
top:0px;
right:0px;

}
section {
border-style:solid;
height:100px;
position: relative;
}
```
### 固定定位的参照物是浏览器的窗口
fixed定位是一种特殊的绝对（absolute）定位，定位的参照物是浏览器的窗口。
和absolute定位的最明显的区别是fixed定位元素不会随着屏幕滚动而移动。
```
#navbar {
position: fixed;
top:0;
left:0;
width: 100%;
background-color: #767676;
}
```
### 使用 float 属性将元素左浮动或右浮动
float属性设置元素浮动。浮动元素不在文档流中，它向左或向右浮动，直到它的外边缘碰到父元素边框或另一个浮动框的边框为止。通常需要用width属性来指定浮动元素占据的水平空间。
```
#left {
      float: left;
      width: 50%;
}
#right {
    float: right;
    width: 40%;
}
```
### 使用 z-index 属性更改重叠元素的位置

### 使用 margin 属性将元素水平居中
### 了解互补色
### 了解三次色
### 将各种元素的颜色调整为互补色
### 调整颜色的色相
### 调整颜色的色调
### 创建一个 CSS 线性渐变
### 使### 用 CSS 线性渐变创建条纹元素
### 添加细微图案作为背景图像来创建纹理
### 使用 CSS Transform scale 属性可以更改元素的大小
### 使用CSS Transform scale 属性在悬停时缩放元素
### 使用 CSS Transform skex 属性沿X轴倾斜元素
### 使用 CSS Transform skex 属性沿Y轴倾斜元素
### 使用 CSS 创建一个图形
### 使用 CSS 和 HTML 创建更复杂的形状
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