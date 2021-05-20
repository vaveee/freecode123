










### 更改文字颜色
CSS允许我们更改许多样式。要更改元素的颜色，请使用color。

这里是你如何将你的h2元素的文本颜色设置为蓝色:`<h2 style="color: blue">小猫相册App</h2>`。

```
<h2  style ="color:red"> 小猫相册App </h2>

<p>小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p>
```

### 使用CSS选择器设置元素样式
不用给每个元素都添加单独的样式，可以使用一个样式同时设置多个元素。

你可以创建如下样式元素:`<style></style>`。

在该样式元素内，你可以为任何HTML元素创建CSS选择器。例如，如果你希望所有h2元素均为红色，则样式元素应如下所示:`<style>h2 {color: red;}</style>`。

**请注意，**
  1. 在每个元素的样式周围同时具有大括号({和大括号是很重要})的。
  2. 你还需要确保元素的样式在开始和结束样式标签之间。
  3. 最后，请确保在每个元素样式的末尾添加分号。

```
<style> 
h2 {
   color : blue;
}
</style>

<h2> 小猫相册App </h2>

<p>小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p>
```

### 使用CSS class为元素设置样式
class【class：类】是可重用的样式，可以添加到HTML元素中。你可以将类应用于HTML元素，例如:`<h2 class="blue-text">小猫相册App</h2>`。

请注意，在CSS样式元素中，class应以句点开头。在HTML元素的类声明中，class不应以句点开头。
```
<style>
  .red-text {
    color: red;
  }
</style>

<h2  class ="red-text"> 小猫相册App </h2>

<p>小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p>
```

### 使用CSS class设置多个元素的样式
你可以通过class="class-name" 【name：名称】在相关元素的开始标签内使用，将类附加到HTML元素。

CSS选择器在开始时需要这样一个点:`.blue-text { color: blue; }`，但是类声明不使用这样的点，例如:`<h2 class="blue-text">小猫相册App<h2>`。

```
<style>
  .red-text {
    color: red;
  }
</style>


<h2  class ="red-text"> 小猫相册App </h2>

<p class="red-text">小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p>
```

###  更改元素的字体大小
字体大小由font-sizeCSS属性控制，例如:`h1 { font-size: 30px; }`。
```
<style>
  .red-text {
    color: red;
  }
</style>

  p {
     font-size : 16 px ;
  }
</style>

<h2  class ="red-text"> 小猫相册App </h2>

<p class="red-text">小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p> 
<p >小猫有一对透亮灵活的大眼睛，黑黑的瞳仁还会变：早晨，像枣核；中午，就成了细线；夜里，却变成两只绿灯泡，圆溜溜的，闪闪发光。</p>
```

### 设置元素的字体系列
你可以使用font-family属性设置元素的字体。

例如，如果要将h2元素的字体设置为Sans-serif，则可以使用以下CSS :`h2 { font-family: Sans-serif; }`。
```
<style>
  .red-text {
    color: red;
  }

  p {
    font-size: 16px;
    font-family: Monospace;
  }
</style>

<h2  class ="red-text"> 小猫相册App </h2>

<p class="red-text">小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p> 
<p>小猫有一对透亮灵活的大眼睛，黑黑的瞳仁还会变：早晨，像枣核；中午，就成了细线；夜里，却变成两只绿灯泡，圆溜溜的，闪闪发光。</p>
```

### 导入Google字体
要从Google或任何其他网站导入字体，请遵循以下格式: `<link href="http://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">`
```
<link href="http://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
  .red-text {
    color: red;

  }
  h2{
    font-family: Lobster;
  }

  p {
    font-size: 16px;
    font-family: Monospace;
  }
</style>

<h2  class ="red-text"> 小猫相册App </h2>

<p class="red-text">小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p> 
<p  class ="red-text"> 小猫有一对透亮灵活的大眼睛，黑黑的瞳仁还会变：早晨，像枣核；中午，就成了细线；夜里，却变成两只绿灯泡，圆溜溜的，闪闪发光。</p>
```

### 指定字体应如何降级
在所有浏览器中都可以使用几种默认字体。这些措施包括Monospace，Serif和Sans-Serif。

例如，如果你想要一个元素使用Helvetica字体，但又Sans-Serif在Helvetica不可用时降级为该字体，则可以使用以下CSS样式:`p { font-family: Helvetica, Sans-Serif; }`。

```
<!--<link href ="http://fonts.googleapis.com/css?family=Lobster” rel ="stylesheet” type ="text / css”>--> 
<style>
  .red-text {
    color: red;
  }

  h2 {
    font-family: Lobster, Monospace;
  }

  p {
    font-size: 16px;
    font-family: Monospace;
  }
</style>

<h2  class ="red-text"> 小猫相册App </h2>

<p class="red-text">小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p> 
<p  class ="red-text"> 小猫有一对透亮灵活的大眼睛，黑黑的瞳仁还会变：早晨，像枣核；中午，就成了细线；夜里，却变成两只绿灯泡，圆溜溜的，闪闪发光。</p>
```



### 调整图片大小
CSS有一个称为的属性width，用于控制元素的宽度。就像字体一样，我们将使用px（像素）来指定图像的宽度。

例如，如果我们想创建一个称为large-image的CSS类，使HTML元素的宽度为500像素，则可以使用:`<style> .larger-image { width: 500px; } </style>`。

```
<link href="http://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
  .red-text {
    color: red;
  }

  .smaller-image{
    width: 100px;
  }

  h2 {
    font-family: Lobster, Monospace;
  }

  p {
    font-size: 16px;
    font-family: Monospace;
  }
</style>

<h2  class ="red-text"> 小猫相册App </h2>

<img  class =“较小图像” src ="https://bit.ly/fcc-relaxing-cat">

<p class="red-text">小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p> 
<p  class ="red-text"> 小猫有一对透亮灵活的大眼睛，黑黑的瞳仁还会变：早晨，像枣核；中午，就成了细线；夜里，却变成两只绿灯泡，圆溜溜的，闪闪发光。</p>
```

### 在元素周围添加边框
CSS边框有这样的属性style，color和width。

例如，如果我们想在HTML元素周围创建一个5像素的红色边框，则可以使用此类:`<style> .thin-red-border { border-color: red; border-width: 5px; border-style: solid; } </style>`。

```
<link href="http://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
  .red-text {
    color: red;
  }

  h2 {
    font-family: Lobster, Monospace;
  }

  p {
    font-size: 16px;
    font-family: Monospace;
  }

  .smaller-image {
    width: 100px;
  }

  .thick-green-border{
    border-color: green;
    border-width: 10px;
    border-style: solid;
  }
</style>

<h2  class ="red-text"> 小猫相册App </h2>

<img  class =“较小图像厚绿色边框” src ="https://bit.ly/fcc-relaxing-cat">

<p class="red-text">小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p> 
<p  class ="red-text"> 小猫有一对透亮灵活的大眼睛，黑黑的瞳仁还会变：早晨，像枣核；中午，就成了细线；夜里，却变成两只绿灯泡，圆溜溜的，闪闪发光。</p>
```

### 添加带有边界半径的圆角
要制作圆角，所有border-radius像素和像素。

你可以指定带有像素的边框半径。这将影响圆角。
```
.thick-green-border {
  border-color: green;
  border-width: 10px;
  border-style: solid;
  border-radius: 10px;
}
```

###　使用边界半径制作圆形图像
你还可以使用百分比border-radius使事情变得更圆滑。
```
.thick-green-border {
  border-color: green;
  border-width: 10px;
  border-style: solid;
  border-radius: 50%;
}
```

### 将替代文本添加到图像以实现辅助功能
alt属性（也称为替代文本）是浏览器如果无法加载图像将显示的内容。alt属性对于盲人或视障用户了解图像所描绘的内容也很重要。搜索引擎还会查看alt属性。

简而言之，每个图像都应具有alt属性！

你可以在这样img元素添加alt属性的权利:`<img src="www.your-image-source.com/your-image.jpg" alt="your alt text"/>`。




### 为Div元素赋予背景色
你可以使用background-color属性设置元素的背景色。

例如，如果你希望元素的背景色为绿色，则可以`.green-background { background-color: green; }`在style元素内使用。

### 设置元素的ID
除了类之外，每个HTML元素还可以具有一个id属性。

使用id属性有很多好处，一旦开始使用jQuery，你将了解有关它们的更多信息。

id属性应该是唯一的。浏览器不会强制执行此操作，但这是广泛认可的最佳做法。因此，请不要给同一个id属性提供多个元素。

这是如何为h2元素赋予cat-photo-app id的示例: `<h2 id="cat-photo-app">`

### 使用ID属性为元素设置样式
关于id属性的一件很酷的事情是，就像类一样，你可以使用CSS设置样式。

这是一个示例，说明如何将元素与idcat-photo-element属性一起使用，并为其赋予绿色背景色。

在你的样式元素中: `#cat-photo-element { background-color: green; }`

请注意，在样式元素内部，你总是通过在类.名之前引用类来引用它们。你总是通过在ID#前面加上ID来引用ID 。

### 调整元素的填充
HTML元素本质上是小矩形。三个重要的属性控制围绕每个HTML元素的空间:padding，margin，和border。元素的填充控制元素与其边框之间的空间量。
```
.green-box {
  background-color: green;
  padding: 20px;
}
```
### 调整元素的边距
元素margin控制元素border与周围元素之间的空间量。
```
.green-box {
  background-color: green;
  padding: 20px;
  margin: 20px;
}
```

### 向元素添加负边距
元素margin控制元素边界和周围元素之间的空间量。如果将元素的边距设置为负值，则元素将变大。

### 向元素的每一侧添加不同的填充
CSS允许你控制元素的填充四面有padding-top，padding-right，padding-bottom，和padding-left属性。
```
.green-box {
  background-color: green;
  padding-top: 40px;
  padding-right: 20px;
  padding-bottom: 20px;
  padding-left: 40px;
}
```

### 向元素的每一边添加不同的边距
CSS允许你控制元素的保证金四面有margin-top，margin-right，margin-bottom，和margin-left属性。

### 使用顺时针表示法指定元素的填充
除了指定一个元素的padding-top，padding-right，padding-bottom，和padding-lef牛逼的属性，你可以在一行中指定他们，就像这样:padding: 10px 20px 10px 20px;。

这四个值像一个时钟一样工作:top, right, bottom, left【top：上，right：右，bottom：下，左：left】并且将产生与使用侧面特定的填充指令完全相同的结果。
```
.green-box {
  background-color: green;
  padding: 40px 20px 20px 40px
}
```

### 使用顺时针表示法指定元素的边距
除了指定一个元素的margin-top，margin-right，margin-bottom，和margin-left属性，你可以在一行中指定他们，就像这样:margin: 10px 20px 10px 20px;。

这四个值像一个时钟一样工作:top, right, bottom, left【top：上，right：右，bottom：下，左：left】并且将产生与使用特定于边距的边距指令完全相同的结果。

.green-box {
  background-color: green;
  margin: 40px 20px 20px 40px;
}

### 设置HTML正文元素的样式
每个HTML页面都有该body元素。就像主页一样。

### 从Body元素继承样式
该body元素可以是风格，就像任何其他。

<style>
  body {
    background-color: black;
    color: green;
    font-family: Monospace
  }

</style>
<h1>你好，世界</h1>

###　将一种样式优先于另一种样式
单个元素的类优先于一般样式。

```
<style>
  body {
    background-color: black;
    font-family: Monospace;
    color: green;
  }
  .pink-text{color: pink;}
</style>
<h1 class="pink-text">你好，世界!</h1>
```

这使得粉红色的h1代替了绿色的h1。

###　在后续CSS中覆盖样式
你的类将覆盖主体的CSS，如果我们添加一个更改相同属性的新类，则最后一个将被应用。

###　通过设置ID属性的样式来覆盖类声明
我们也可以使用id覆盖样式。
```
<style>
  body {
    background-color: black;
    font-family: Monospace;
    color: green;
  }
  .pink-text {
    color: pink;
  }
  .blue-text {
    color: blue;
  }
  #orange-text{color:orange;}
</style>
<h1 class="pink-text blue-text" id="orange-text">你好，世界!</h1>
```

### 用内联样式覆盖类声明
请记住，线条样式如下所示:`<h1 style="color: green">`它们将覆盖更改h1文本颜色的其他所有内容。

### 使用“!important”替代所有其他样式
在许多情况下，你将使用CSS库。这些可能会意外覆盖你自己的CSS。因此，当你绝对需要确保某个元素具有特定的CSS时，可以使用`!important`。

如何做到这一点的一个例子是:`color: red !important`;这将确保我们使用想要的属性，而不考虑其他替代。

### 对特定颜色使用十六进制代码
对于CSS，我们使用6个十六进制数字表示颜色。例如，`#000000`是可能的最低值，它代表黑色。

这与#RRGGBB也可以简化为的相同#RGB。

### 使用十六进制代码将元素着色为白色
0是十六进制代码中最低的数字，表示完全没有颜色。F是十六进制代码中的最高数字，它表示最大可能的亮度。

### 使用十六进制代码将元素着色为红色
十六进制代码遵循红绿蓝或rgb格式。十六进制代码的前两位数字代表颜色中红色的数量。第三和第四位数字代表绿色。第五和第六代表蓝色的数量。

因此，要获得绝对最亮的红色，你将只使用F第一和第二位数字（可能的最大值）以及0第三，第四，第五和第六位数字（可能的最小值）。

### 使用十六进制代码为元素添加绿色
就像红色和其他的一样。
```
<style>
  body {
    background-color: #00FF00;
  }
</style>
```
### 使用十六进制代码为蓝色元素着色
就像红色和其他的一样。
```
<style>
  body {
    background-color: #0000FF;
  }
</style>
```
### 使用十六进制代码混合颜色
橙色是纯红色，混合有一些绿色，没有蓝色。
```
<style>
  body {
    background-color: #FFA500;
  }
</style>
```
### 使用十六进制代码将元素着色为灰色
我们还可以通过将所有三种颜色均匀混合来创建不同的灰色阴影。 `background-color: #808080`;

### 对特定的灰色阴影使用十六进制代码
我们还可以通过将所有三种颜色均匀混合来创建其他灰色阴影。我们可以非常接近真正的黑色。`background-color: #111111`;

### 使用缩写的十六进制代码

`#FF0000`十六进制代码中的红色可以缩短为#F00。也就是说，红色代表一位，绿色代表一位，蓝色代表一位。

这样可以将可能的颜色总数减少到4,000种左右。但是浏览器会解释`#FF0000`并`#F00`显示完全相同的颜色。
```
<style>
  body {
    background-color: #F00;
  }
</style>
```
### 使用RGB值作为色彩元素
在CSS中表示颜色的另一种方法是使用rgb值。

RGB值如下所示:rgb(0, 0, 0)黑色和rgb(255, 255, 255)白色。

与其像使用十六进制代码那样使用六个十六进制数字，不如使用rbg，你可以使用0到255之间的数字指定每种颜色的亮度。 background-color: rgb(0,0,0);

### 使用RGB将元素着色为白色
background-color: rgb(255,255,255)

### 使用RGB将红色元素着色
background-color: rgb(255, 0, 0)

### 使用RGB为绿色着色元素
rgb值绿色: rgb(0, 255, 0)

### 使用RGB为蓝色元素着色
RGB值蓝色: rgb(0, 0, 255)

### 使用RGB混合颜色
RGB值橙色: rgb(255, 165, 0)

### 使用RGB将元素着色为灰色
灰色的RGB值: rgb(128, 128, 128)