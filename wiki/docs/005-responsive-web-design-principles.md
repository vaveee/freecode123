### 创建一个媒体查询
媒体查询是 CSS3 中引入的一项新技术，它可以根据不同的可视窗口大小显示不同的布局。

可视窗口是用户在网页上的可见区域，根据访问网站的设备不同而不同。

媒体查询由媒体类型组成，如果媒体类型与展示网页的设备类型匹配，则应用对应的样式。你可以在媒体查询中用上你想用的选择器和样式。

下面是一个媒体查询的例子，当设备宽度小于或等于 100px 时返回内容：
`@media (max-width: 100px) { /* CSS Rules */ }`


以下定义的媒体查询，是当设备高度大于或等于 350px 时返回内容：
`@media (min-height: 350px) { /* CSS Rules */ }`

只有当媒体类型与当前设备匹配时，才应用媒体查询中的 CSS。

增加一个设备的高度小于或等于 800px 时，p标签的 font-size为 12px 的媒体查询。

```
<style>
  p {
    font-size: 20px;
  }

  /* Only change code below this line */
@media(max-height: 800px){
  p {
    font-size:10px;
  }
}
  /* Only change code above this line */
</style>

<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus quis tempus massa. Aenean erat nisl, gravida vel vestibulum cursus, interdum sit amet lectus. Sed sit amet quam nibh. Suspendisse quis tincidunt nulla. In hac habitasse platea dictumst. Ut sit amet pretium nisl. Vivamus vel mi sem. Aenean sit amet consectetur sem. Suspendisse pretium, purus et gravida consequat, nunc ligula ultricies diam, at aliquet velit libero a dui.</p>
```

### 使图片自适应设备尺寸
响应式 Web 设计原则：使图片根据设备尺寸自如响应 用 CSS 来让图片自适应其实很简单。不要使用绝对单位：

`img { width: 720px; }`

你应该使用：
```
img {
  max-width: 100%;
  display: block;
  height: auto;
}

```
max-width属性能让图片以 100% 的最大宽度适应其父容器的宽度，但图片不会拉伸得比原始宽度还宽。

将 display属性设置为 block可以让 image 标签从内联元素（默认值）更改为块级元素。

设置 height属性为 auto 保持图片的原始宽高比。

给 img标签增加样式规则使它自适应容器尺寸。应声明为块级元素，应适应它容器的宽度，应保持原本的宽高比。

```
<style>
.responsive-img {
max-width:100%;
height:auto;
display:block;

}

img {
  width: 600px;
}
</style>

<img class="responsive-img" src="https://s3.amazonaws.com/freecodecamp/FCCStickerPack.jpg" alt="freeCodeCamp stickers set">

<img src="https://s3.amazonaws.com/freecodecamp/FCCStickerPack.jpg" alt="freeCodeCamp stickers set">
```

### 针对高分辨率屏幕应使用视网膜图片
响应式 Web 设计原则：针对高分辨率屏幕应使用视网膜图片 为优化图片在高分辨率设备下的显示效果，最简单的方式是定义它们的 width和 height值为源文件宽高的一半。

这是一个图片宽高设置为源文件一半的例子：
```
<style>
  img { height: 250px; width: 250px; }
</style>
<img src="coolPic500x500" alt="一张高质量的图片">
```

设置 img标签的 width和 height为它们原始宽高的一半。在这个例子中，原始 height和原始 width的值都为 200px。
```
<style>
img{
  width:100px;
  height:100px;
}
</style>

<img src="https://s3.amazonaws.com/freecodecamp/FCCStickers-CamperBot200x200.jpg" alt="freeCodeCamp sticker that says 'Because CamperBot Cares'">
```
### 使排版根据设备尺寸自如响应

除了用 em或 px去设置文本大小, 你还可以用视窗单位来做响应式排版。

视窗单位还有百分比，它们都是相对单位，但却基于不同的参照物。

视窗单位相对于设备的视窗尺寸 (宽度或高度) ，百分比是相对于父级元素的大小。

四个不同的视窗单位分别是：

vw：如 10vw的意思是视窗宽度的 10%。 
vh：如 3vh的意思是视窗高度的 3%。 

vmin：如 70vmin的意思是视窗中较小尺寸的 70% (高度 VS 宽度)。
vmax：如 100vmax的意思是视窗中较大尺寸的 100% (高度 VS 宽度)。


设置 h2标签的 width为视窗宽度的 80%，p标签的 width为视窗高度和宽度中较小值的 75%。
```
<style>
h2{
  width:80vw;
}
p{
  width:75vmin;
}
</style>

<h2>Importantus Ipsum</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus quis tempus massa. Aenean erat nisl, gravida vel vestibulum cursus, interdum sit amet lectus. Sed sit amet quam nibh. Suspendisse quis tincidunt nulla. In hac habitasse platea dictumst. Ut sit amet pretium nisl. Vivamus vel mi sem. Aenean sit amet consectetur sem. Suspendisse pretium, purus et gravida consequat, nunc ligula ultricies diam, at aliquet velit libero a dui.</p>

```