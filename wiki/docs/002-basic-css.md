
### 修改文本的颜色
CSS允许修改许多样式。使用color修改元素的颜色。

将h2元素的文本颜色设置为蓝色:`<h2 style="color: blue">小猫相册App</h2>`。

```
<h2  style ="color:red"> 小猫相册App </h2>

<p>小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p>
```
### 使用元素选择器来设置元素的样式
不用给每个元素都添加单独的样式，一个样式可以同时设置多个元素。

创建如下样式元素:`<style></style>`。

在该样式元素内，你可以为任何HTML元素创建CSS选择器。例如，如果你希望所有h2元素均为红色，则样式元素应如下所示:`<style>h2 {color: red;}</style>`。

请注意:

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

### 使用 class 选择器设置单个元素的样式
class【class：类】是可重用的样式，可以添加到HTML元素中。
你可以将class应用于HTML元素，例如:`<h2 class="blue-text">小猫相册App</h2>`。

请注意，在CSS样式元素中，class应以点开头。在HTML元素的类声明中，class不应以点开头。
```
<style>
  .red-text {
    color: red;
  }
</style>

<h2 class ="red-text"> 小猫相册App </h2>

<p>小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p>
```
### 使用 class 选择器设置多个元素的样式
你可以通过class="class-name" 【name：名称】在相关元素的开始标签内使用，将类添加到HTML元素中。

CSS选择器在开始时需要这样一个点:`.blue-text { color: blue; }`，但是类的声明不用这样的点，例如:`<h2 class="blue-text">小猫相册App<h2>`。

```
<style>
  .red-text {
    color: red;
  }
</style>


<h2  class ="red-text"> 小猫相册App </h2>

<p class="red-text">小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p>
```
### 修改元素的字体大小
字体大小由font-size属性控制，例如:`h1{ font-size: 30px; }`。

```
<style>
  .red-text {
    color: red;
  }
  p {
     font-size : 16px;
  }
</style>

<h2  class="red-text"> 小猫相册App </h2>

<p class="red-text">小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p> 
<p >小猫有一对透亮灵活的大眼睛，黑黑的瞳仁还会变：早晨，像枣核；中午，就成了细线；夜里，却变成两只绿灯泡，圆溜溜的，闪闪发光。</p>
```
### 设置元素的字体
你可以使用font-family属性设置元素的字体。

例如，如果要将h2元素的字体设置为Sans-serif，则可以使用以下CSS :
`h2 { font-family: Sans-serif; }`。

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
### 引入谷歌字体
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

<p class="red-text">The cat's big ears, all day long are straight and upright, where there is a sound, immediately turned over there, live like a radar with special performance。</p> 
<p  class ="red-text"> Cat has a pair of bright flexible eyes, black pupils will change: morning, like jujube core, at noon, became a fine line; at night, but into two green bulbs, round, shining。</p>
```
### 字体如何优雅降级
在所有浏览器中都可以使用几种默认字体。这些措施包括Monospace，Serif和Sans-Serif。

例如，如果你想要一个元素使用Helvetica字体，在Helvetica不可用时降级为Sans-Serif字体，则可以使用以下CSS样式:`p { font-family: Helvetica, Sans-Serif; }`。

```
<!--<link href ="http://fonts.googleapis.com/css?family=Lobster" rel ="stylesheet" type ="text / css">--> 
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

<h2  class ="red-text"> Cat Photo App </h2>

<p class="red-text">The cat's big ears, all day long are straight and upright, where there is a sound, immediately turned over there, live like a radar with special performance。</p> 
<p  class ="red-text"> Cat has a pair of bright flexible eyes, black pupils will change: morning, like jujube core, at noon, became a fine line; at night, but into two green bulbs, round, shining。</p>
```
### 调整图片的大小
CSS有一个width属性，用于控制元素的宽度。就像字体一样，我们将使用px（像素）来指定图像的宽度。

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

<img  class ="smaller-image" src ="https://bit.ly/fcc-relaxing-cat">

<p class="red-text">小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p> 
<p  class ="red-text"> 小猫有一对透亮灵活的大眼睛，黑黑的瞳仁还会变：早晨，像枣核；中午，就成了细线；夜里，却变成两只绿灯泡，圆溜溜的，闪闪发光。</p>
```
### 在元素周围添加边框
CSS的边框【border：边框】有style，color和width这样的属性

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

<img  class ="较小图像厚绿色边框" src ="https://bit.ly/fcc-relaxing-cat">

<p class="red-text">小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p> 
<p  class ="red-text"> 小猫有一对透亮灵活的大眼睛，黑黑的瞳仁还会变：早晨，像枣核；中午，就成了细线；夜里，却变成两只绿灯泡，圆溜溜的，闪闪发光。</p>
```
### 用 border-radius 添加圆角边框
要制作圆角边框，使用border-radius属性，使用像素设置。

你可以指定带有像素的边框半径。设置边框为圆角。
```
.thick-green-border {
  border-color: green;
  border-width: 10px;
  border-style: solid;
  border-radius: 10px;
}
```
### 用 border-radius 制作圆形图片
你还可以使用百分比border-radius制作圆形图片（边框）。
```
.thick-green-border {
  border-color: green;
  border-width: 10px;
  border-style: solid;
  border-radius: 50%;
}
```

### 给 div 元素添加背景色
你可以使用background-color属性设置元素的背景色。

例如，如果你希望元素的背景色为绿色，则可以`.green-background { background-color: green; }`在style元素内使用。

### 设置元素的 id
除了类之外，每个HTML元素还可以具有一个id属性。

使用id属性有很多好处，一旦开始使用jQuery，你将了解有关它们的更多信息。

id属性在页面内应该是唯一的。浏览器不会强制执行此操作，但这是广泛认可的最佳做法。因此，请不要给同一个id属性提供多个元素。

这是如何为h2元素赋予cat-photo-app id的示例: `<h2 id="cat-photo-element">`
### 使用 id 属性来设定元素的样式
关于id属性的一件很酷的事情是，就像类一样，你可以使用CSS设置样式。

选择id为cat-photo-element的元素，并设置它的背景样式为green，可以在你的style标签里这样写：
```
#cat-photo-element {
  background-color: green;
}
```

### 调整元素的内边距
HTML元素本质上是小矩形。三个重要的属性控制围绕每个HTML元素的空间:padding，margin，和border。元素的内边距padding控制元素内容与其边框之间的距离。
```
.green-box {
  background-color: green;
  padding: 20px;
}
```
### 调整元素的外边距
元素外边距margin控制元素border与周围元素之间的距离。
```
.green-box {
  background-color: green;
  padding: 20px;
  margin: 20px;
}
```
### 给元素添加负外边距
元素margin控制元素边界和周围元素之间的距离。如果将元素的边距设置为负值，则会边框会朝相反的方向移动。

### 给元素的每一侧添加不同的内边距
CSS允许你控制元素的上、右、下、左内边距，分别使用padding-top，padding-right，padding-bottom，和padding-left属性。
```
.green-box {
  background-color: green;
  padding-top: 40px;
  padding-right: 20px;
  padding-bottom: 20px;
  padding-left: 40px;
}
```

### 给元素的每一侧添加不同的外边距
CSS允许你控制元素的上、右、下、左外边距，分别使用margin-top，margin-right，margin-bottom，和margin-left属性。


### 使用顺时针标记指定元素的内边距
除了指定一个元素的padding-top，padding-right，padding-bottom，和padding-lef内边距的属性，你可以在同一行代码中指定它们，就像这样:padding: 10px 20px 10px 20px;。

这四个值像一个时钟一样工作:top, right, bottom, left【top：上，right：右，bottom：下，左：left】一行指定和分别制定效果完全相同。
```
.green-box {
  background-color: green;
  padding: 40px 20px 20px 40px
}
```
### 使用顺时针标记指定元素的外边距
参照内边距，外边距使用margin
.green-box {
  background-color: green;
  margin: 40px 20px 20px 40px;
}

### 使用属性选择器来设置元素的样式
下面的代码会改变所有type为radio的元素的外边距，使用属性选择器来设置元素的样式,属性名为type，属性值为'radio'。
[type='radio'] {
  margin: 20px 0px 20px 0px;
}

### 理解绝对单位与相对单位
CSS 有不同的长度单位供我们使用。

相对单位，如em的大小基于元素的字体的font-size值。

绝对单位，如in和mm分别代表着英寸和毫米。

### 给 HTML 的 body 元素添加样式
我们可以通过设置背景颜色background-color为black，来证明body元素的存在。

添加以下的代码到style标签里面：
```
body {
  background-color: black;
}
```
### 从 body 元素继承样式
下面的h1标签默认会继承body的样式。
```
<style>
  body {
    background-color: black;
    color: green;
    font-family: Monospace
  }

</style>
<h1>你好，世界</h1>
```
### 样式中的优先级
元素的class样式优先级高于继承的样式。
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

这使得粉红色pink的h1代替了绿色green的h1。
### Class 选择器的优先级高于继承样式

我们刚刚证明了 class 会覆盖 body 的 CSS 样式。

HTML 同时应用多个 class 属性需以空格来间隔，例子如下:

`class="class1 class2"`

 >注意：HTML 元素里应用的 class 的先后顺序无关紧要。

但是，在 <style> 标签里面声明的 class 顺序十分重要，之后的声明会覆盖之前的声明。 

### ID 选择器优先级高于 Class 选择器
我们也可以使用id覆盖class样式
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
### 内联样式的优先级高于 ID 选择器
请记住，内联样式如下所示:`<h1 style="color: green">`它们将覆盖修改h1文本颜色的其他所有样式，包括id选择器样式和class选择器样式。
### Important 的优先级最高
在许多情况下，你将使用CSS的第三方库（别人写的）。这些可能会意外覆盖你自己的CSS。因此，当你绝对需要确保某个元素具有特定的CSS时，可以使用`!important`。

如下所示::`color: red !important`;这将确保我们使用想要的属性，而不考虑其他。

### 使用十六进制编码获得指定颜色
对于CSS，我们使用6个十六进制数字表示颜色。例如，`#000000`是可能的最低值，它代表黑色。

`#RRGGBB也可以简化为#RGB`。

### 使用十六进制编码混合颜色
白色`#FFFFFF`
0是十六进制代码中最低的数字，表示完全没有颜色。F是十六进制代码中的最高数字，它表示最大可能的亮度。

红色`#FF0000`
十六进制代码遵循红绿蓝或rgb格式。十六进制代码的前两位数字代表颜色中红色的数量。第三和第四位数字代表绿色。第五和第六代表蓝色的数量。

因此，要获得绝对最亮的红色，你将只使用F第一和第二位数字（可能的最大值）以及0第三，第四，第五和第六位数字（可能的最小值）。

绿色`#00FF00`
蓝色`#0000FF`

我们还可以通过将所有三种颜色均匀混合来创建不同的灰色阴影。 `background-color: #808080`;

我们还可以通过将所有三种颜色均匀混合来创建其他灰色阴影。我们可以非常接近真正的黑色。`background-color: #111111`;

橙色是纯红色，混合有一些绿色，没有蓝色。
```
<style>
  body {
    background-color: #FFA500;
  }
</style>
```
### 使用缩写的十六进制编码

`#FF0000`十六进制代码中的红色可以缩短为#F00。也就是说，红色代表一位，绿色代表一位，蓝色代表一位。

这样可以将可能的颜色总数减少到4,000种左右。但是浏览器会解释`#FF0000`并`#F00`显示完全相同的颜色。
```
<style>
  body {
    background-color: #F00;
  }
</style>
```
### 使用 RGB 值为元素上色
在CSS中表示颜色的另一种方法是使用rgb值。

RGB值如下所示:rgb(0, 0, 0)黑色和rgb(255, 255, 255)白色。

你可以使用0到255之间的数字指定每种颜色的亮度。 background-color: rgb(0,0,0);

rgb值白色: rgb(255,255,255)

rgb值红色: rgb(255, 0, 0)

rgb值绿色: rgb(0, 255, 0)

rgb值蓝色: rgb(0, 0, 255)

### 使用 RGB 混合颜色
就像使用十六进制编码一样，你可以通过不同值的组合，来混合得到不同的 RGB 颜色。

rgb值橙色: rgb(255, 165, 0)

rgb值灰色: rgb(128, 128, 128)

rgb值兰花: rgb(218, 112, 214)

rgb值赭色: 	rgb(160, 82, 45)

### 使用 CSS 变量一次修改多个元素
使用CSS 变量，可以通过改变修改一个值，一次性修改多个 CSS 样式属性。
定义变量：

```
--penguin-skin: black;
--penguin-belly: gray;
--penguin-beak: yellow;
```

### 创建一个自定义的 CSS 变量
创建一个 CSS 变量，你只需要在变量名前添加两个破折号，并为其赋值，例子如下：

`--penguin-skin: gray;`

变量名：penguin-skin

变量值：gray

### 使用一个自定义的 CSS 变量
创建变量后，CSS 属性可以通过引用变量名来使用它的值。

`background: var(--penguin-skin);`

### 给 CSS 变量设置备用值
正在使用着不支持 CSS 变量的旧浏览器，或者设备不支持你设置的变量值。为了防止这种情况出现，那么你可以这样写：

background: var(--penguin-skin, black);

这样，当你的变量有问题的时候，它会设置你的背景颜色为黑色。

### 浏览器降级提高兼容性

使用 CSS 时可能会遇到浏览器兼容性问题。 提供浏览器降级方案来避免潜在的问题会显得很重要。

### 继承 CSS 变量

你创建的变量，不但可以在你声明变量的元素里面使用，同时也可以在该元素的子元素里面使用。这种效应称为cascading（层叠）。

因为层叠的效果，CSS 变量通常会定义在:root元素里。

就像html是body的容器一样，你也可以认为:root元素是你整个 HTML 文档的容器。

在:root创建的变量，在整个网页里面都能生效。
```
 :root {
    --penguin-skin: black;
  }
```

### 修改特定区域的变量
当你在:root里创建变量时，这些变量的作用域是整个页面。

如果在元素里创建相同的变量，会重写:root变量设置的值，如下的penguin-belly。
```
 :root {
    --penguin-skin: gray;
    --penguin-belly: pink;
    --penguin-beak: orange;
  }
 
  body {
    background: var(--penguin-belly, #c6faf1);
  }
```

### 使用媒体查询修改变量-不同的屏幕大小适用不同的样式
CSS 变量可以简化媒体查询的方式。
例如，当屏幕小于或大于媒体查询所设置的值，通过改变变量的值，那么应用了变量的元素样式都会得到响应修改。

在media query（媒体查询）声明的:root选择器里，重定义–penguin-size的值为 200px，且重定义–penguin-skin的值为black，然后通过缩放页面来查看是否生效。
```
  :root {
    --penguin-size: 300px;
    --penguin-skin: gray;
    --penguin-belly: white;
    --penguin-beak: orange;
  }
 
  @media (max-width: 350px) {
    :root {
      --penguin-size: 200px;
      --penguin-skin: black;
    }
  }
```