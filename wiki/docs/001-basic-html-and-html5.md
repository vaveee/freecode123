### 向HTML元素问好
大部分HTML元素都包含开始标签，结束标签，内容则放在两者之间:

`<tagname>`内容`</tagname>` 【tagname:标签名】 HTML元素包含从开始标签到结束标签的所有内容:

`<p>`这是一个段落.`</p>`


 |  子元素  |  	描述 |  
 |  ----  | ----  |
 | `<p>`	 | 开始标签| 
 | 这是一个段落 | 	内容 | 
 | `</p>`	 | 结束标签 | 

 > 开始标签和结束标签之间的唯一区别是，结束标签在其打开尖括号后有一个斜线。

### 副标题使用h2元素
你可以使用h1，h2，h3，h4，h5，h6创建不同级别的Heading【Heading:标题】元素，它们大小各不同。

 |  代码	 |  效果  |
 |  ----  | ----  |
 | `<h1>一号标题</h1>`	| <h1> 一号标题</h1> |
 | `<h2>二号标题</h2>`	| <h2> 二号标题</h2> |
 | `<h3>三号标题</h3>`	| <h3> 三号标题</h3> |
 | `<h4>四号标题</h4>`	| <h4> 四号标题</h4> |
 | `<h5>五号标题</h5>`	| <h5> 五号标题</h5> |
 | `<h6>六号标题</h6>`	| <h6> 六号标题</h6> |


### 段落使用p元素
p元素是网站上普通段落文本的首选元素。P是“paragraph”【paragraph:段落】的缩写。

你可以像这样创建一个p元素:`<p>`这是一个段落标签!`</p>`。

```
<h1> 你好，世界 </h1> 
<h2> 小猫相册App </h2> 
<p> 这是一个段落标签</p>
```
### 用占位符文本填写空白
传统上，Web开发人员使用lorem ipsum文本作为占位符文本，这是古罗马西塞罗著名段落的前两个词。

lorem ipsum文本自16世纪以来一直被排字工人用作占位符文本，并且这种传统在网络上继续存在。

```
<h1>你好世界</h1>

<h2> 小猫相册App </h2>

<p>lorem ipsum小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p>
```

### 去除 HTML 的注释
鉴于有两种方法可以用JavaScript编写注释:

使用 //
使用 `<!-- 内容 --->`

你只需删除注释元素即可轻松取消注释。

### 给 HTML 添加注释
注释有两种作用:

 1. 可以在代码内保留注释而又不影响代码本身。

 2. 可以使代码变为非活动状态而不必完全删除它。

 写注释是一个好习惯，它让你的代码更容易理解。

你可以使用添加`<!--` 开始注释，使用`-->`结束注释，两者缺一不可。
```
<!-- 
<h1> 你好，世界 </h1>

<h2> 小猫相册App </h2>

<p>你好段落</p> 
-->
```

### 删除HTML元素
删除元素非常简单。就是删除元素开头到结尾的所有内容，并将其删除。不需要额外的代码。


### HTML5 元素介绍
HTML5 引入了很多更具描述性的 HTML 元素，例如：header、footer、nav、video、article、section、main等等。

这些元素让 HTML 更易读，同时有助于搜索引擎优化和无障碍访问。在后面的课程中我们会接触到更多新的 HTML5 元素，明白它们的用处。

### 给网站添加图片
你可以使用img元素将图像添加到你的网站，并使用src属性指向特定图像的URL 。

例如`<img src="www.your-image-source.com/your-image.jpg">`。请注意，在大多数情况下，img元素是自动关闭的。和之前的p标签相比，img没有单独的结束标签！

```
<h2  class ="red-text"> 小猫相册App </h2> 
<img  src ="https://bit.ly/fcc-relaxing-cat"> 
<p  class ="red-text"> 小猫的那一双大耳朵，一天到晚都直竖着，哪个地方有声音，马上往那边转，活像一架有特殊性能的雷达。</p> 
```

###　用锚点实现网页间的跳转
a 元素，也称为锚元素，用于链接到当前页面之外的内容。

这是一个示例:`<a href="http://www.baidu.com">百度</a>`。

###　用锚点实现网页内部跳转
锚点同样也可以用来在网页内不同区域的跳转。

设置锚点的href属性值为#加上想跳转区域对应的id属性值，这样就可以创建一个内部跳转。id是用来描述网页元素的一个属性，它的值在整个页面中唯一。

下面是用来创建内部锚点的例子：
```
<a href="#contacts-header">联系我们</a>
<!--这里再加多行代码，这样跳转才会明显-->
<h2 id="contacts-header">联系我们</h2>
```
当用户点击了**联系我们**链接，页面就会跳转到网页的**联系我们**区域。

### 将锚点嵌套在段落中
嵌套很简单，只需在另一个元素内添加一个元素即可: 
`<p> 试试点击右边的链接： <a href="http://www.baidu.com">百度</a></p>`


### 使用散列符号建立死链接
将元素的href属性替换为#，也称为哈希符号，以将其变为无效链接。

`<a href="#">还没想好链接到哪</a>`

当你使用jQuery更改链接的行为时，这也很方便，稍后我们将进行介绍。

### 给图片添加链接
给图片添加链接是必不可少的，也是网页开发中最常用的功能之一。将你的图片嵌套在一个a元素中。这是一个示例:
`<a href="#"><img src="http://bit.ly/fcc-running-cats"/></a>`。

### 创建一个无序列表
HTML可以创建无序列表。

无序列表以`<ul>`元素开头。然后它们包含一些`<li>`元素。

例如:
```
<ul> 
  <li>牛奶</li> 
  <li>奶酪</li> 
</ul>
```
创建项目符号样式为点的无序列表。

### 创建一个有序列表
HTML可以创建有序列表。

有序列表以`<ol>`元素开头。然后它们包含一些`<li>`元素。

例如:
```
<ol> 
  <li>氢</li> 
  <li>氦</li> 
</ol>
```

创建项目符号样式为数字的有序列表。

### 创建一个文本输入
文本输入是从用户那里获取输入的便捷方法。

你可以这样创建一个:`<input type="text">`。请注意，输入元素是自动闭合的。

### 给输入框添加占位符文本
占位符文本是用户输入任何内容之前在输入框显示的内容。

你可以像这样创建占位符文本:`<input type="text" placeholder="这是一段占位符">`。

```
<input type="text" placeholder="猫照片URL">
```

### 创建一个表单
你可以构建仅使用纯HTML将数据提交到服务器的Web表单。

通过在form元素上指定action来做到这一点。例如:
`<form action="/您要提交数据的网址"></form>`。

```
<form action="/submit-cat-photo"><input type="text" placeholder="猫照片URL"></form>
```
网址涉及到网页后台代码，我们会在后边的章节中学习。

### 给表单添加提交按钮
你将需要创建一个button【button：按钮】元素,提交表单到服务器。这是一个示例提交按钮:`<button type="submit">提交</button>`。
```
<form action="/submit-cat-photo">
  <input type="text" placeholder="猫照片URL">
  <button type="submit">提交</button>
</form>
```

### 给表单添加一个必填字段
你可以要求必填字段，以便你的用户在填写表单之前不能提交你的表单。

例如，如果要使文本输入字段为必填字段，则只需在输入元素中添加required即可，你可以使用:
`<input type="text" required>`。

```
<form action="/submit-cat-photo">
  <input type="text" placeholder="猫照片URL" required>
  <button type="submit">提交</button>
</form>
```


### 创建一组单选按钮
你可以使用单选按钮提出问题，让用户只能选择一个答案。

单选按钮是一种输入。它们嵌套在自己的label元素中。此外，所有相关的单选按钮应具有相同的名称属性。

这是一个单选按钮的示例:`<label><input type="radio" name="indoor-outdoor">室内</label>`。
```
<form action="/submit-cat-photo">
  <label><input type="radio" name="indoor-outdoor">室内</label>
  <label><input type="radio" name="indoor-outdoor">室外</label>
  <input type="text" placeholder="猫照片URL" required>
  <button type="submit">提交</button>
</form>
```
 > 注意代码中，哪些部分用了英文，哪些用了中文。我们这里使用英文通常是因为，使用中文代替它们会有问题。

### 创建一组复选框
复选框是一种输入。每个复选框都应嵌套在其自己的label元素内。
所有相关的复选框输入应具有相同的名称属性。
这是一个复选框的示例:`<label><input type="checkbox" name="personality"> 有爱心的</label>`。
```
<form action="/submit-cat-photo">
  <label><input type="radio" name="indoor-outdoor"> 室内</label>
  <label><input type="radio" name="indoor-outdoor"> 室外</label>
  <label><input type="checkbox" name="personality"> 有爱心的</label>
  <label><input type="checkbox" name="personality"> 懒惰的</label>
  <label><input type="checkbox" name="personality"> 精力充沛的</label>
  <input type="text" placeholder="猫照片URL" required>
  <button type="submit">提交</button>
</form>
```


### 使用单选框和复选框的 value 属性
提交表单时，所选项的值会发送给服务端。 
radio 和 checkbox 的 value 属性值决定了发送到服务端的实际内容。

例如：
```
<label for="indoor">
  <input id="indoor" value="indoor" type="radio" name="indoor-outdoor">室内
</label>
<label for="outdoor">
  <input id="outdoor" value="outdoor" type="radio" name="indoor-outdoor">室外
</label>
```
网址涉及到网页后台代码，我们会在后边的章节中学习。

### 给单选按钮和复选框添加默认选中项
你可以使用checked属性将复选框或单选按钮设置为默认选中状态。

为此，只需在输入元素的内部添加单词"checked”。例如，`<input type="radio" name="test-name" checked>`。
```
<form action="/submit-cat-photo">
  <label><input type="radio" checked name="indoor-outdoor"> 室内</label>
  <label><input type="radio" name="indoor-outdoor"> 室外</label>
  <label><input type="checkbox" checked name="personality"> 有爱心的</label>
  <label><input type="checkbox" name="personality"> 懒惰的</label>
  <label><input type="checkbox" name="personality"> 精力充沛的</label>
  <input type="text" placeholder="猫照片URL" required>
  <button type="submit">提交</button>
</form>
```

### 将多个元素嵌套在一个Div元素中
该div元素也称为分隔元素，是其他元素的通用容器。

> div元素可能是所有元素中最常用的HTML元素。

就像其他任何非自动关闭元素一样，你可以使用打开一个div元素`<div>`并将其关闭在另一行上`</div>`。
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

### 声明 HTML 文档的文档类型
这是网页结构一个例子：
```
<!DOCTYPE html>
<html>
  <!-- 网页的内容 -->
</html>
```

`<!DOCTYPE html>`是告诉浏览器你使用的是 HTML5版本。

### 定义 HTML 文档的标题和正文
这是网页布局的一个例子：
【head：头】【title：标题】【body：身体】
```
<!DOCTYPE html>
<html>
  <head>
    <title>网页标题</title>
  </head>
  <body>
    <div>网页正文</div>
  </body>
</html>

```
你可尝试修改标题和正文。