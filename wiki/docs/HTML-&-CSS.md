### 向HTML元素问好
HTML元素大多包含开始标签，结束标签，内容放在两者之间:

`<tagname>`内容`</tagname>` 【tagname:标签名】 HTML元素包含从开始标记到结束标记的所有内容:

`<p>`这是一个段落.`</p>`

开始标签如下所示:`<h1>`。结束标签看起来像这样:`</h1>` 

请注意，开始标签和结束标签之间的唯一区别是，结束标签在其打开尖括号后有一个斜线。

### 带有h2元素的标题
您可以使用h1，h2，h3，h4，h5，h6创建不同级别的Heading【Heading:标题】元素，它们大小各不同。

```
<h1> 你好，世界 </h1> 
<h2> 小猫相册App </h2>
```

### 使用段落元素
p元素是网站上普通大小的段落文本的首选元素。P是“paragraph”【paragraph:段落】的缩写。

您可以像这样创建一个p元素:`<p>`这是一个段落标签!`</p>`。

```
<h1> 你好，世界 </h1> 
<h2> 小猫相册App </h2> 
<p> 你好段落</p>
```

### 取消注释HTML
鉴于有两种方法可以用JavaScript编写注释:

使用 //
使用 `<!-- text --->`
您只需删除注释元素即可轻松取消注释。

### 注释掉HTML
注释是一种可以在代码内保留注释而又不影响代码本身的方法。

这也是使代码变为非活动状态而不必完全删除它的便捷方法。

您可以使用添加评论`<!-- and end a comment with --->`。
```
<!-- 
<h1> 你好，世界 </h1>

<h2> 小猫相册App </h2>

<p>你好段落</p> 
-->
```

### 用占位符文本填写空白
传统上，Web开发人员使用lorem ipsum文本作为占位符文本。之所以称为lorem ipsum文本，是因为这是古罗马西塞罗著名段落的前两个词。

lorem ipsum文本自16世纪以来一直被排字工人用作占位符文本，并且这种传统在网络上继续存在。

```
<h1>你好世界</h1>

<h2> 小猫相册App </h2>

<p>小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p>
```

### 删除HTML元素
删除元素非常简单。您要做的就是删除元素开头到结尾的所有内容，并将其删除。不需要额外的代码。


### 更改文字颜色
CSS允许我们更改许多样式。要更改元素的颜色，请使用color。

这里是你如何将你的h2元素的文本颜色设置为蓝色:`<h2 style="color: blue">小猫相册App</h2>`。

```
<h2  style ="color:red"> 小猫相册App </h2>

<p>小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p>
```

### 使用CSS选择器设置元素样式
不用给每个元素都添加单独的样式，可以使用一个样式同时设置多个元素。

您可以创建如下样式元素:`<style></style>`。

在该样式元素内，您可以为任何HTML元素创建CSS选择器。例如，如果您希望所有h2元素均为红色，则样式元素应如下所示:`<style>h2 {color: red;}</style>`。

**请注意，**
  1. 在每个元素的样式周围同时具有大括号({和大括号是很重要})的。
  2. 您还需要确保元素的样式在开始和结束样式标签之间。
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
class【class：类】是可重用的样式，可以添加到HTML元素中。您可以将类应用于HTML元素，例如:`<h2 class="blue-text">小猫相册App</h2>`。

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
您可以通过class="class-name" 【name：名称】在相关元素的开始标记内使用，将类附加到HTML元素。

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
您可以使用font-family属性设置元素的字体。

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

例如，如果您想要一个元素使用Helvetica字体，但又Sans-Serif在Helvetica不可用时降级为该字体，则可以使用以下CSS样式:`p { font-family: Helvetica, Sans-Serif; }`。

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

### 将图像添加到您的网站
您可以使用img元素将图像添加到您的网站，并使用src属性指向特定图像的URL 。

例如`<img src="www.your-image-source.com/your-image.jpg">`。请注意，在大多数情况下，img元素是自动关闭的。

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
</style>

<h2  class ="red-text"> 小猫相册App </h2> 
<img  src ="https://bit.ly/fcc-relaxing-cat"> 
<p  class ="red-text"> 小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p> 
<p  class ="red-text">小猫有一对透亮灵活的大眼睛，黑黑的瞳仁还会变：早晨，像枣核；中午，就成了细线；夜里，却变成两只绿灯泡，圆溜溜的，闪闪发光。</p>
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

您可以指定带有像素的边框半径。这将影响圆角。
```
.thick-green-border {
  border-color: green;
  border-width: 10px;
  border-style: solid;
  border-radius: 10px;
}
```

###　使用边界半径制作圆形图像
您还可以使用百分比border-radius使事情变得更圆滑。
```
.thick-green-border {
  border-color: green;
  border-width: 10px;
  border-style: solid;
  border-radius: 50%;
}
```

###　链接到带有锚元素的外部页面
a 元素，也称为锚元素，用于链接到当前页面之外的内容。

这是一个示例:`<p>Here's a <a href="http://freecodecamp.com"> link to Free Code Camp</a> for you to follow.</p>`。

### 在段落中嵌套锚元素
嵌套很简单，只需在另一个元素内添加一个元素即可: 
`<p> click here for <a href="http://www.小猫相册App.com">cat photos</a></p>`

### 使用散列符号建立死链接
将元素的href属性替换为#，也称为哈希符号，以将其变为无效链接。有时，您想在您的网站链接之前将其添加到您的网站中。

当您使用jQuery更改链接的行为时，这也很方便，稍后我们将进行介绍。

### 将图像变成链接
创建链接到事物的图像是必不可少的，也是Web Dev中最常用的事物之一。将您的图片嵌套在一个a元素中。这是一个示例:
`<a href="#"><img src="http://bit.ly/fcc-running-cats"/></a>`。

### 将替代文本添加到图像以实现辅助功能
alt属性（也称为替代文本）是浏览器如果无法加载图像将显示的内容。alt属性对于盲人或视障用户了解图像所描绘的内容也很重要。搜索引擎还会查看alt属性。

简而言之，每个图像都应具有alt属性！

您可以在这样img元素添加alt属性的权利:`<img src="www.your-image-source.com/your-image.jpg" alt="your alt text"/>`。

### 创建项目符号无序列表
HTML具有用于创建无序列表或项目符号点样式列表的特殊元素。

无序列表以`<ul>`元素开头。然后它们包含一些`<li>`元素。

例如:
```
<ul> 
  <li>牛奶</li> 
  <li>奶酪</li> 
</ul>
```
将创建“牛奶”和“奶酪”的项目符号点样式列表。

### 创建一个有序列表
HTML具有用于创建有序列表或编号样式列表的特殊元素。

有序列表以`<ol>`元素开头。然后它们包含一些`<li>`元素。

例如:
```
<ol> 
  <li>氢</li> 
  <li>氦</li> 
</ol>
```

将创建“氢”和“氦”的编号列表。

### 创建一个文本字段
文本输入是从用户那里获取输入的便捷方法。

您可以这样创建一个:`<input type="text">`。请注意，输入元素是自动闭合的。

### 将占位符文本添加到文本字段
占位符文本是用户输入任何内容之前在文本输入中显示的内容。

您可以像这样创建占位符文本:`<input type="text" placeholder="this is placeholder text">`。

```
<input type="text" placeholder="cat photo URL">
```

### 创建一个表单元素
您可以构建仅使用纯HTML实际将数据提交到服务器的Web表单。您可以通过在form元素上指定一个操作来做到这一点。例如:
`<form action="/url-where-you-want-to-submit-form-data"></form>`。

```
<form action="/submit-cat-photo"><input type="text" placeholder="cat photo URL"></form>
```

### 将提交按钮添加到表单
您将需要创建一个button元素。这是一个示例提交按钮:`<button type="submit">this button submits the form</button>`。
```
<form action="/submit-cat-photo">
  <input type="text" placeholder="cat photo URL">
  <button type="submit">Submit</button>
</form>
```

### 使用HTML5要求字段
您可以要求特定的表单字段，以便您的用户在填写表单之前不能提交您的表单。

例如，如果要使文本输入字段为必填字段，则只需在输入元素中添加必需的单词即可，您可以使用:
`<input type="text" required>`。

```
<form action="/submit-cat-photo">
  <input type="text" placeholder="cat photo URL" required>
  <button type="submit">Submit</button>
</form>
```

### 创建一组单选按钮
您可以使用单选按钮提出问题，让用户只给您一个答案。

单选按钮是一种输入。它们都应嵌套在自己的label元素中。此外，所有相关的单选按钮应具有相同的名称属性。

这是一个单选按钮的示例:`<label><input type="radio" name="indoor-outdoor"> Indoor</label>`。
```
<form action="/submit-cat-photo">
  <label><input type="radio" name="indoor-outdoor"> Indoor</label>
  <label><input type="radio" name="indoor-outdoor"> Outdoor</label>
  <input type="text" placeholder="cat photo URL" required>
  <button type="submit">Submit</button>
</form>
```

### 创建一组复选框
复选框是一种输入。

您的每个复选框都应嵌套在其自己的label元素内。
所有相关的复选框输入应具有相同的名称属性。
这是一个复选框的示例:`<label><input type="checkbox" name="personality"> Loving</label>`。
```
<form action="/submit-cat-photo">
  <label><input type="radio" name="indoor-outdoor"> Indoor</label>
  <label><input type="radio" name="indoor-outdoor"> Outdoor</label>
  <label><input type="checkbox" name="personality"> Loving</label>
  <label><input type="checkbox" name="personality"> Lazy</label>
  <label><input type="checkbox" name="personality"> Energetic</label>
  <input type="text" placeholder="cat photo URL" required>
  <button type="submit">Submit</button>
</form>
```

### 默认情况下选中单选按钮和复选框
您可以使用checked属性将复选框或单选按钮设置为默认选中状态。

为此，只需在输入元素的内部添加单词"checked”。例如，`<input type="radio" name="test-name" checked>`。
```
<form action="/submit-cat-photo">
  <label><input type="radio"checked name="indoor-outdoor"> Indoor</label>
  <label><input type="radio" name="indoor-outdoor"> Outdoor</label>
  <label><input type="checkbox"checked name="personality"> Loving</label>
  <label><input type="checkbox" name="personality"> Lazy</label>
  <label><input type="checkbox" name="personality"> Energetic</label>
  <input type="text" placeholder="cat photo URL" required>
  <button type="submit">Submit</button>
</form>
```

### 将多个元素嵌套在一个Div元素中
该div元素也称为分隔元素，是其他元素的通用容器。

div元素可能是所有元素中最常用的HTML元素。这对于将其自己的类声明的CSS传递到它包含的所有元素很有用。

就像其他任何非自动关闭元素一样，您可以使用打开一个div元素`<div>`并将其关闭在另一行上`</div>`。
```
<div> 
 <p>猫爱的事物:</p> 
 <ul> 
   <li>猫咬</li> 
   <li>激光笔</li> 
   <li>烤宽面条</li> 
 </ul> 
 <p>猫最讨厌的三件事:</p> 
 <ol> 
   <li>兽医</p> >
   <li>打雷</p>  
   <li>其它猫</p> 
 </ol> 
</div> 
```

### 为Div元素赋予背景色
您可以使用background-color属性设置元素的背景色。

例如，如果您希望元素的背景色为绿色，则可以`.green-background { background-color: green; }`在style元素内使用。

### 设置元素的ID
除了类之外，每个HTML元素还可以具有一个id属性。

使用id属性有很多好处，一旦开始使用jQuery，您将了解有关它们的更多信息。

id属性应该是唯一的。浏览器不会强制执行此操作，但这是广泛认可的最佳做法。因此，请不要给同一个id属性提供多个元素。

这是如何为h2元素赋予cat-photo-app id的示例: `<h2 id="cat-photo-app">`

### 使用ID属性为元素设置样式
关于id属性的一件很酷的事情是，就像类一样，您可以使用CSS设置样式。

这是一个示例，说明如何将元素与idcat-photo-element属性一起使用，并为其赋予绿色背景色。

在您的样式元素中: `#cat-photo-element { background-color: green; }`

请注意，在样式元素内部，您总是通过在类.名之前引用类来引用它们。您总是通过在ID#前面加上ID来引用ID 。

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
CSS允许您控制元素的填充四面有padding-top，padding-right，padding-bottom，和padding-left属性。
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
CSS允许您控制元素的保证金四面有margin-top，margin-right，margin-bottom，和margin-left属性。

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
您的类将覆盖主体的CSS，如果我们添加一个更改相同属性的新类，则最后一个将被应用。

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
在许多情况下，您将使用CSS库。这些可能会意外覆盖您自己的CSS。因此，当您绝对需要确保某个元素具有特定的CSS时，可以使用`!important`。

如何做到这一点的一个例子是:`color: red !important`;这将确保我们使用想要的属性，而不考虑其他替代。

### 对特定颜色使用十六进制代码
对于CSS，我们使用6个十六进制数字表示颜色。例如，`#000000`是可能的最低值，它代表黑色。

这与#RRGGBB也可以简化为的相同#RGB。

### 使用十六进制代码将元素着色为白色
0是十六进制代码中最低的数字，表示完全没有颜色。F是十六进制代码中的最高数字，它表示最大可能的亮度。

### 使用十六进制代码将元素着色为红色
十六进制代码遵循红绿蓝或rgb格式。十六进制代码的前两位数字代表颜色中红色的数量。第三和第四位数字代表绿色。第五和第六代表蓝色的数量。

因此，要获得绝对最亮的红色，您将只使用F第一和第二位数字（可能的最大值）以及0第三，第四，第五和第六位数字（可能的最小值）。

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

与其像使用十六进制代码那样使用六个十六进制数字，不如使用rbg，您可以使用0到255之间的数字指定每种颜色的亮度。 background-color: rgb(0,0,0);

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