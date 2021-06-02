### 为视觉障碍用户添加替代图像的文本
在其他挑战里你应该已经见到过img标签的alt属性了。alt属性中的文本作为备用文字描述了图片的内容，这可以帮助用户在图片加载失败或者不可见的情况下理解图片内容，也有助于搜索引擎理解图片内容，并将其加入到搜索结果中。例如：

`<img src="importantLogo.jpeg" alt="Company logo">`
那些无法通过视觉获取信息的用户，只能通过屏幕阅读器将网页内容转换为音频的方式获取信息，而屏幕阅读器通过识别alt属性，并朗读其中的内容，来告知用户图片包含的关键信息。

良好的alt文本可以简明扼要地描述图片信息，所以你应该为图片添加alt属性。另外，HTML5 标准也在考虑强制要求对图片添加alt属性。
### 了解 Alt 文本留空的情景
在上节中，我们了解到img标签必须有一个alt属性。在图片已经有了文字说明，或者仅仅为了美化页面的情况下，alt属性似乎有些多余。

即便如此，我们仍然需要为img标签添加alt属性，这时可以把它设为空，例如：

`<img src="visualDecoration.jpeg" alt="">`
对于背景图片，它们通常起装饰作用，而且含有 CSS 类，所以背景图片不会被屏幕阅读器处理。

注意： 对于有标题的图片，我们依然需要添加alt属性，因为这样有助于搜索引擎记录图片内容。

### 使用标题显示内容的层次关系
标题标签（包括h1到h6）有很高的使用率，它们用于描述内容的主题。在屏幕阅读器中，用户为更快地了解页面内容，可以设置让阅读器只朗读页面标题。这意味着标题标签之间以及标签本身都应语义化，不应仅仅为了获得不同字号而使用不同级别的标题标签。

语义化：标签名能准确地表达它所含内容的信息类型。

对于一篇含有引言、正文、结论的论文，把结论作为引言的一部分没有任何意义，因为结论应该是独立的章节。类似地，页面中的标题标签也应该是有序的，并且能表明内容的层次关系。

在使用中，相同级别（或者更高级别）的标题标签用于开启新的章节，低一级别的标题标签用于开启上一级标题标签的子小节。

举个例子：一个h2标签后紧跟若干h4标签的页面，会让使用屏幕阅读器的用户感到困惑。尽管在页面中，使用这 6 个标题标签可以控制内容的的视觉样式，但我们应该使用 CSS 来调整。

最后一点，每个页面应该只有一个h1标签，用来说明页面主要内容。h1标签和其他的标题标签可以让搜索引擎获取页面的大纲。
```
<h1>How to Become a Ninja</h1>
<main>
  <h2>Learn the Art of Moving Stealthily</h2>
  <h3>How to Hide in Plain Sight</h3>
  <h3>How to Climb a Wall</h3>

  <h2>Learn the Art of Battle</h2>
  <h3>How to Strengthen your Body</h3>
  <h3>How to Fight like a Ninja</h3>

  <h2>Learn the Art of Living with Honor</h2>
  <h3>How to Breathe Properly</h3>
  <h3>How to Simplify your Life</h3>
</main>
```
### 使用 main 元素包裹主题内容
HTML5 添加了诸如main、header、footer、nav、article、section等大量新标签，这些新标签为开发人员提供更多的选择和辅助特性。

默认情况下，浏览器呈现这些新标签的方式与div相似。然而，合理地使用它们，可以使你的标签更加的语义化。辅助技术（如：屏幕阅读器）可以通过这些标签为用户提供更加准确的、易于理解的页面信息。

main标签用于呈现网页的主体内容，且每个页面只能有一个。这意味着它只应包含与页面中心主题相关的信息，而不应包含如导航连接、网页横幅等可以在多个页面中重复出现的内容。

main标签的语义化特性可以使辅助技术快速定位到页面的主体。有些页面中有 “跳转到主要内容” 的链接，使用main标签可以使辅助设备自动获得这个功能。
```
<header>
  <h1>Weapons of the Ninja</h1>
</header>

<main>

</main>

<footer></footer>
```
### 使用 article 元素包裹文章内容
article是另一个具有语义化特性的 HTML5 新标签。article是一个分段标签，用于呈现独立及完整的内容。这个标签适用于博客入口、论坛帖子或者新闻文章。

有些技巧可以用来判断内容是否独立，像是如果内容脱离了上下文，是否仍然有意义？类似地，对于 RSS 提要中的文本，它是否有意义？

请牢记，使用辅助设备的用户依赖组织良好的、语义化的标签来获取页面中的信息。

请注意section和div的区别： section也是一个 HTML5 新标签，与article标签的语义含义略有不同。article用于独立的、完整的内容，而section用于对与主题相关的内容进行分组。它们可以根据需要嵌套着使用。举个例子：如果一本书是一个article的话，那么每个章节就是section。当内容组之间没有联系时，可以使用div。

`<div> `- 内容组
`<section>` - 有联系的内容组
`<article>`- 独立完整的内容
```
<h1>Deep Thoughts with Master Camper Cat</h1>
<main>
  <article>
    <h2>The Garfield Files: Lasagna as Training Fuel?</h2>
    <p>The internet is littered with varying opinions on nutritional paradigms, from catnip paleo to hairball cleanses. But let's turn our attention to an often overlooked fitness fuel, and examine the protein-carb-NOM trifecta that is lasagna...</p>
  </article>

  <img src="samuraiSwords.jpeg" alt="">

  <article>
    <h2>Defeating your Foe: the Red Dot is Ours!</h2>
    <p>Felines the world over have been waging war on the most persistent of foes. This red nemesis combines both cunning stealth and lightning speed. But chin up, fellow fighters, our time for victory may soon be near...</p>
  </article>

  <img src="samuraiSwords.jpeg" alt="">

  <article>
    <h2>Is Chuck Norris a Cat Person?</h2>
    <p>Chuck Norris is widely regarded as the premier martial artist on the planet, and it's a complete coincidence anyone who disagrees with this fact mysteriously disappears soon after. But the real question is, is he a cat person?...</p>
  </article>
</main>
```
### 使用 header 元素来让屏幕阅读器更容易进行导航
header也是一个具有语义化的、提升页面可访问性的 HTML5 标签。它可以为父级标签呈现简介信息或者导航链接，适用于那些在多个页面顶部重复出现的内容。

与main类似，header的语义化特性也可以使辅助技术快速定位到它的内容。

注意： header用在 HTML 文档的body标签中。这点与包含页面标题、元信息的head标签不同。

```
<body>

  <header>
    <h1>Training with Camper Cat</h1>
  </header>


  <main>
    <section id="stealth">
      <h2>Stealth &amp; Agility Training</h2>
      <article><h3>Climb foliage quickly using a minimum spanning tree approach</h3></article>
      <article><h3>No training is NP-complete without parkour</h3></article>
    </section>
    <section id="combat">
      <h2>Combat Training</h2>
      <article><h3>Dispatch multiple enemies with multithreaded tactics</h3></article>
      <article><h3>Goodbye world: 5 proven ways to knock out an opponent</h3></article>
    </section>
    <section id="weapons">
      <h2>Weapons Training</h2>
      <article><h3>Swords: the best tool to literally divide and conquer</h3></article>
      <article><h3>Breadth-first or depth-first in multi-weapon training?</h3></article>
    </section>
  </main>
</body>
```

### 使用 nav 元素使屏幕阅读器更容易导航
nav也是一个具有语义化特性的 HTML5 标签，用于呈现页面中的主导航链接。它可以使屏幕阅读器快速识别页面中的导航信息。

对于页面底部辅助性质的站点链接，不需要使用nav，用footer（在下个挑战中介绍）会更好。
```
<body>
  <header>
    <h1>Training with Camper Cat</h1>

    <nav>
      <ul>
        <li><a href="#stealth">Stealth &amp; Agility</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Weapons</a></li>
      </ul>
    </nav>

  </header>
  <main>
    <section id="stealth">
      <h2>Stealth &amp; Agility Training</h2>
      <article><h3>Climb foliage quickly using a minimum spanning tree approach</h3></article>
      <article><h3>No training is NP-complete without parkour</h3></article>
    </section>
    <section id="combat">
      <h2>Combat Training</h2>
      <article><h3>Dispatch multiple enemies with multithreaded tactics</h3></article>
      <article><h3>Goodbye world: 5 proven ways to knock out an opponent</h3></article>
    </section>
    <section id="weapons">
      <h2>Weapons Training</h2>
      <article><h3>Swords: the best tool to literally divide and conquer</h3></article>
      <article><h3>Breadth-first or depth-first in multi-weapon training?</h3></article>
    </section>
  </main>
</body>
```


### 使用 footer 元素来让屏幕阅读器更容易进行导航
与header和nav类似，footer也具有语义化特性，可以使辅助设备快速定位到它。它位于页面底部，用于呈现版权信息或者相关文档链接。
```
<body>
  <header>
    <h1>Training</h1>
    <nav>
      <ul>
        <li><a href="#stealth">Stealth &amp; Agility</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Weapons</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section id="stealth">
      <h2>Stealth &amp; Agility Training</h2>
      <article><h3>Climb foliage quickly using a minimum spanning tree approach</h3></article>
      <article><h3>No training is NP-complete without parkour</h3></article>
    </section>
    <section id="combat">
      <h2>Combat Training</h2>
      <article><h3>Dispatch multiple enemies with multithreaded tactics</h3></article>
      <article><h3>Goodbye world: 5 proven ways to knock out an opponent</h3></article>
    </section>
    <section id="weapons">
      <h2>Weapons Training</h2>
      <article><h3>Swords: the best tool to literally divide and conquer</h3></article>
      <article><h3>Breadth-first or depth-first in multi-weapon training?</h3></article>
    </section>
  </main>


  <footer>&copy; 2018 Camper Cat</footer>


</body>
```
### 使用 audio 元素提高音频内容的可访问性
HTML5 的audio标签用于呈现音频内容，它也具有语义化特性。可以在audio上下文中为音频内容添加文字说明或者字幕链接，使听觉障碍用户也能获取音频中的信息。

audio支持controls属性，可以使浏览器为音频提供具有开始、暂停等功能的播放控件。controls属性是一个布尔属性，只要这个属性出现在audio标签中，浏览器就会开启播放控件。

举个例子：
```
<audio id="meowClip" controls>
  <source src="audio/meow.mp3" type="audio/mpeg" />
  <source src="audio/meow.ogg" type="audio/ogg" />
</audio>
```
注意： 多媒体内容通常同时包含音频与视频部分，它需要同步音频与字幕，以使视觉或听觉障碍用户可以获取它的内容。一般情况下，网页开发者不需要创建音频与字幕，但是需要将它们添加到多媒体中。
```
<body>
  <header>
    <h1>Real Coding Ninjas</h1>
  </header>
  <main>
    <p>A sound clip of Zersiax's screen reader in action.</p>


<audio id="meowClip" controls>
  <source src="https://s3.amazonaws.com/freecodecamp/screen-reader.mp3" type="audio/mpeg">
</audio>

  </main>
</body>
```

### 使用 figure 元素提高图表的可访问性
HTML5 引入了figure标签以及与之相关的figcaption标签。它们一起用于展示可视化信息（如：图片、图表）及其标题。这样通过语义化对内容进行分组并配以用于解释figure的文字，可以极大的提升内容的可访问性。

对于图表之类的可视化数据，标题可以为屏幕阅读器用户提供简要的说明。但是这里有一个难点，如何处理那些超出屏幕可视范围（使用 CSS ）的表格版本的图表数据，以使屏幕阅读器用户也可以获取信息。

举个例子——注意figcaption包含在figure标签中，并且可以与其他标签组合使用：
```
<figure>
  <img src="roundhouseDestruction.jpeg" alt="Photo of Camper Cat executing a roundhouse kick">
  <br>
  <figcaption>
    Master Camper Cat demonstrates proper form of a roundhouse kick.
  </figcaption>
</figure>

```
```
<body>
  <header>
    <h1>Training</h1>
    <nav>
      <ul>
        <li><a href="#stealth">Stealth &amp; Agility</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Weapons</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section>

      <!-- Only change code below this line -->
      <figure>
        <!-- Stacked bar chart will go here -->
        <br>
        <figcaption>Breakdown per week of time to spend training in stealth, combat, and weapons.</figcaption>
      </figure>
      <!-- Only change code above this line -->

    </section>
    <section id="stealth">
      <h2>Stealth &amp; Agility Training</h2>
      <article><h3>Climb foliage quickly using a minimum spanning tree approach</h3></article>
      <article><h3>No training is NP-complete without parkour</h3></article>
    </section>
    <section id="combat">
      <h2>Combat Training</h2>
      <article><h3>Dispatch multiple enemies with multithreaded tactics</h3></article>
      <article><h3>Goodbye world: 5 proven ways to knock out an opponent</h3></article>
    </section>
    <section id="weapons">
      <h2>Weapons Training</h2>
      <article><h3>Swords: the best tool to literally divide and conquer</h3></article>
      <article><h3>Breadth-first or depth-first in multi-weapon training?</h3></article>
    </section>
  </main>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```


### 使用 label 元素提高表单的可访问性
合理地使用语义化的 HTML 标签和属性可以提升页面可访问性。在接下来的挑战中，你将会看到使用表单属性的重要场景。

label标签用于呈现特定表单控件的文本，通常是选项的名称。这些文本代表了选项的含义，使表单具有更好的可读性。label标签的for属性指定了与label绑定的表单控件，并且屏幕阅读器也会读取for属性。

在 HTML 基础章节的课程中，我们已经了解了单选按钮标签。在那节课程中，我们为了可以点击单选按钮的名称，将input标签放在label标签中。在本节课程中，我们介绍了另外一种实现这个功能的方法，那就是使用for属性。

for属性的值必须与表达控件的id属性的值相同。举个例子：
```
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name">
</form>
```
### 将单选按钮包裹在 fieldset 元素中以获得更好的可访问性
下一个小节与单选按钮的可访问性有关。在上一小节中，单选按钮含有一个拥有for属性的label标签，for属性指向相关选项的id。然而单选按钮通常成组出现，用户必须其中选择一项。本小节介绍一种可以语义化呈现单选按钮组的方法。

使用fieldset标签将单选按钮组包含在里面就可以实现这个目的，通常还会使用legend标签来为单选按钮组提供文字说明。屏幕阅读器也可以朗读这些文字。

当选项的含义很明确时，如：性别选择，fieldset标签与legend标签就可以省略。这时，使用含有for属性的label标签就足够了。

举个例子：
```
<form>
  <fieldset>
    <legend>Choose one of these three items:</legend>
    <input id="one" type="radio" name="items" value="one">
    <label for="one">Choice One</label><br>
    <input id="two" type="radio" name="items" value="two">
    <label for="two">Choice Two</label><br>
    <input id="three" type="radio" name="items" value="three">
    <label for="three">Choice Three</label>
  </fieldset>
</form>
 ```

```
<body>
  <header>
    <h1>Deep Thoughts with Master Camper Cat</h1>
  </header>
  <section>
    <form>
      <p>Sign up to receive Camper Cat's blog posts by email here!</p>
      <label for="email">Email:</label>
      <input type="text" id="email" name="email">


      <!-- Only change code below this line -->
      <fieldset>
        <legend>What level ninja are you?</legend>
        <input id="newbie" type="radio" name="levels" value="newbie">
        <label for="newbie">Newbie Kitten</label><br>
        <input id="intermediate" type="radio" name="levels" value="intermediate">
        <label for="intermediate">Developing Student</label><br>
        <input id="master" type="radio" name="levels" value="master">
        <label for="master">Master</label>
      </fieldset>
      <!-- Only change code above this line -->


      <input type="submit" name="submit" value="Submit">
    </form>
  </section>
  <article>
    <h2>The Garfield Files: Lasagna as Training Fuel?</h2>
    <p>The internet is littered with varying opinions on nutritional paradigms, from catnip paleo to hairball cleanses. But let's turn our attention to an often overlooked fitness fuel, and examine the protein-carb-NOM trifecta that is lasagna...</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Defeating your Foe: the Red Dot is Ours!</h2>
    <p>Felines the world over have been waging war on the most persistent of foes. This red nemesis combines both cunning stealth and lightning speed. But chin up, fellow fighters, our time for victory may soon be near...</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Is Chuck Norris a Cat Person?</h2>
    <p>Chuck Norris is widely regarded as the premier martial artist on the planet, and it's a complete coincidence anyone who disagrees with this fact mysteriously disappears soon after. But the real question is, is he a cat person?...</p>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

### 添加可访问的日期选择器
表单中经常出现input标签，它可以用来创建多种表单控件。它的type属性指定了所要创建的input标签类型。

在以前的挑战中，你可能已经见过text与submit类型的input标签，HTML5 引入了date类型来创建时间选择器。依赖于浏览器的支持，当点击input标签时，时间选择器会显示出来，这可以让用户填写表单更加容易。

对于旧版本的浏览器，type属性的默认值是text。这种情况下，可以利用label标签或者占位文本来提示用户input标签的输入类型为日期。

举个例子：
```
<label for="input1">Enter a date:</label>
<input type="date" id="input1" name="input1">
```
### 使用 HTML5 的 datatime 属性标准化时间
继续日期主题。HTML5 还引入了time标签与datetime属性来标准化时间。time是一个行内标签，用于在页面中呈现日期或时间，而datetime属性保存了日期的有效格式，辅助设备可以访问这个值。通过标准化时间格式，即使时间在文本中是以非正式的或口语化的形式编写，辅助设备依然可以获取准确的时间和日期。

举个例子：
```
<p>
  Master Camper Cat officiated the cage match between Goro and Scorpion 
  <time datetime="2013-02-13">last Wednesday</time>, which ended in a draw.
</p>
```
```
<body>
  <header>
    <h1>Tournaments</h1>
  </header>
  <article>
    <h2>Mortal Kombat Tournament Survey Results</h2>

    <!-- Only change code below this line -->

    <p>Thank you to everyone for responding to Master Camper Cat's survey. The best day to host the vaunted Mortal Kombat tournament is <time datetime="2016-09-15">Thursday, September 15<sup>th</sup></time>. May the best ninja win!</p>

    <!-- Only change code above this line -->

    <section>
      <h3>Comments:</h3>
      <article>
        <p>Posted by: Sub-Zero on <time datetime="2016-08-13T20:01Z">August 13<sup>th</sup></time></p>
        <p>Johnny Cage better be there, I'll finish him!</p>
      </article>
      <article>
        <p>Posted by: Doge on <time datetime="2016-08-15T08:12Z">August 15<sup>th</sup></time></p>
        <p>Wow, much combat, so mortal.</p>
      </article>
      <article>
        <p>Posted by: The Grim Reaper on <time datetime="2016-08-16T00:00Z">August 16<sup>th</sup></time></p>
        <p>Looks like I'll be busy that day.</p>
      </article>
    </section>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```
### 使用自定义 CSS 让元素仅对屏幕阅读器可见
到目前为止，所有关于可访问性的挑战都没有使用 CSS。这是为了让你在关注外观样式之前，先把页面的逻辑结构写清，以及明确语义化标签的重要性。

然而，如果我们需要在页面中添加一些只对屏幕阅读器可见的内容时，CSS 可以提升页面的可访问性。当信息以可视化形式（如：图表）展示，而屏幕阅读器用户需要一种替代方式（如：表格）来获取信息时，就会出现这种情况。CSS 被用来将这些仅供屏幕阅读器使用的信息定位到浏览器可见区域之外。

举个例子：
```
.sr-only {
  position: absolute;
  left: -10000px;
  width: 1px;
  height: 1px;
  top: auto;
  overflow: hidden;
}
```
注意： 下面的 CSS 代码与上面的结果不同：

`display: none;或visibility: hidden;`会把内容彻底隐藏起来，对于屏幕阅读器也不例外。

如果把值设置为 0px，如`width: 0px; height: 0px;`，意味着让元素脱离文档流，这样做也会让元素被屏幕阅读器忽略。
```
<head>
  <style>
  .sr-only {
    position: absolute ;
    left: -10000px;
    width: 1px;
    height: 1px;
    top: auto;
    overflow: hidden;
  }
  </style>
</head>
<body>
  <header>
    <h1>Training</h1>
    <nav>
      <ul>
        <li><a href="#stealth">Stealth &amp; Agility</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Weapons</a></li>
      </ul>
    </nav>
  </header>
  <section>
    <h2>Master Camper Cat's Beginner Three Week Training Program</h2>
    <figure>
      <!-- Stacked bar chart of weekly training -->
      <p>[Stacked bar chart]</p>
      <br />
      <figcaption>Breakdown per week of time to spend training in stealth, combat, and weapons.</figcaption>
    </figure>
    <table class="sr-only">
      <caption>Hours of Weekly Training in Stealth, Combat, and Weapons</caption>
      <thead>
        <tr>
          <th></th>
          <th scope="col">Stealth &amp; Agility</th>
          <th scope="col">Combat</th>
          <th scope="col">Weapons</th>
          <th scope="col">Total</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">Week One</th>
          <td>3</td>
          <td>5</td>
          <td>2</td>
          <td>10</td>
        </tr>
        <tr>
          <th scope="row">Week Two</th>
          <td>4</td>
          <td>5</td>
          <td>3</td>
          <td>12</td>
        </tr>
        <tr>
          <th scope="row">Week Three</th>
          <td>4</td>
          <td>6</td>
          <td>3</td>
          <td>13</td>
        </tr>
      </tbody>
    </table>
  </section>
  <section id="stealth">
    <h2>Stealth &amp; Agility Training</h2>
    <article><h3>Climb foliage quickly using a minimum spanning tree approach</h3></article>
    <article><h3>No training is NP-complete without parkour</h3></article>
  </section>
  <section id="combat">
    <h2>Combat Training</h2>
    <article><h3>Dispatch multiple enemies with multithreaded tactics</h3></article>
    <article><h3>Goodbye, world: 5 proven ways to knock out an opponent</h3></article>
  </section>
  <section id="weapons">
    <h2>Weapons Training</h2>
    <article><h3>Swords: the best tool to literally divide and conquer</h3></article>
    <article><h3>Breadth-first or depth-first in multi-weapon training?</h3></article>
  </section>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```
### 使用高对比度文本提高可读性
低对比度的前景色与背景色会使文本难以阅读。足够的对比度可以提高内容的可读性，但是怎样的对比度才算是 “足够” 的？

Web 内容无障碍指南（WCAG）建议正常文本的对比度至少为 4.5 : 1。对比度是通过比较两种颜色的相对亮度值来计算的，其范围是从相同颜色的 1 : 1（无对比度）到白色与黑色的最高对比度 21 : 1。网上有很多可以帮助你计算对比度的工具。

### 考虑色盲用户的需求设置合适的对比度
颜色是可视化设计的重要组成部分，但是使用颜色也引入了两个可访问性问题。首先，不能仅仅使用颜色作为传达重要信息的唯一方式，因为屏幕阅读器无法获取这些信息。其次，前景色与背景色需要有足够的对比度，这样色盲用户才可以识别它们。

在之前的挑战中，我们用文本备用方案解决了第一个问题。在上一个挑战中，我们使用对比度检测工具解决了第二问题。WCAG 建议为颜色及灰度组合使用 4.5 : 1 的对比度。

色盲用户无法将一些颜色与另一些颜色区分出来——通常是因为色调，也有时候是因为亮度。你可能想起对比度是用前景色与背景色的相对亮度计算的。

实践中，在对比度检测工具的帮助下，我们可以将较暗的颜色变暗、将较淡的颜色变淡的方法来使对比度达到 4.5 : 1。在色轮中，较暗的颜色通常是蓝色、紫色、洋红和红色，而较淡的颜色通常是橙色、黄色、绿色和蓝绿色。


### 考虑色盲用户的需求仔细选择传达信息的颜色
色盲的形式有很多种，它的表现可以从对特定波长光波的感知度较低，到几乎无法看到颜色。最常见的形式是对绿色的低感知度。

例如：如果内容的前景色与背景色是两种相近的绿色，那么色盲用户可能会无法识别它们。可以将色轮上相邻的颜色认为是相近的，我们不应用这些颜色来表示重要的信息。

注意： 一些在线颜色拾取器有色盲模拟功能，可以模拟颜色在不同形式色盲的视觉中的呈现结果，它们和在线对比度检查器一样，都是很好的工具。

### 为链接添加描述性的文本
屏幕阅读器用户可以选择其设备读取的内容的类型，这包括跳转到（或跳过）标志标签，以便跳转到主要内容，或者从标题中获取页面摘要，还可以选择只听取页面中的有效链接。

屏幕阅读器通过阅读链接文本或者锚点标签（a）之间的内容来完成这个操作。拥有 “click here” 或者 “read more” 列表并没有什么用处。相反地，应该在a标签中使用简洁的描述性语言来为用户提供更多的信息。

### 通过给元素添加 accesskey 属性来让用户可以在链接之间快速导航
HTML 提供accesskey属性，用于指定激活标签或者使标签获得焦点的快捷键，这可以使键盘用户的导航更加有效。

HTML5 允许在任何标签上使用这个属性。该属性对于交互类标签（如链接、按钮、表单控件等）十分有用。

带有指定快捷键的超链接：

<a href="#" accesskey="h">HTML</a><br />
<a href="#" accesskey="c">CSS</a>

注释：请使用Alt + accessKey (或者 Shift + Alt + accessKey) 来访问带有指定快捷键的元素。

### 使用 tabindex 将键盘焦点添加到元素中

HTML 的tabindex属性有三个不同与标签焦点的功能。当它在标签上时，表示标签可以获得焦点。它的值可以是零、负整数及正整数，并决定了标签的行为。

当用户在页面中使用 tab 键时，有些标签，如：链接、表单控件，可以自动获得焦点。它们获得焦点的顺序与它们出现在文档流中的顺序一致。我们可以通过将tabindex属性值设为 0，来给其他标签赋予相同的功能，如：div、span、p等。举个例子：

`<div tabindex="0">I need keyboard focus!</div>`

注意： tabindex属性值为负整数（通常为 -1）的标签也是有焦点的，只是不可以通过 tab 键来获得焦点。这种方法通常用于以编程的方式使内容获得焦点（如：激活用于弹出框的div标签），但是它超出了当前挑战的范围。

### 使用 tabindex 指定多个元素的键盘焦点顺序

tabindex属性还可以指定标签的 tab 键顺序，将它的值设置为大于或等于 1 就可以实现这个功能。

tabindex属性值为 1 的标签将首先获得键盘焦点，然后焦点将按照指定的tabindex的值（如：2，3 等）的顺序进行移动，直到回到默认的或tabindex值为 0 的标签上，如此循环。

需要注意的是，当按照这种方式设置 tab 键顺序时，将会覆盖默认的顺序（标签在文档流中出现的顺序）。这可能会令那些希望从页面顶部开始导航的用户感到困惑。这个技术在某些情况下可能是必要的，但是对可访问性而言，在应用时要十分小心。

举个例子：
```
<div tabindex="1">I get keyboard focus, and I get it first!</div>
<div tabindex="2">I get keyboard focus, and I get it second!</div>
```

带有指定 tab 键顺序的链接：
```
<a href="http://www.baidu.com/" tabindex="2">baidu</a>
<a href="http://www.google.com/" tabindex="1">Google</a>
<a href="http://www.microsoft.com/" tabindex="3">Microsoft</a>
```
