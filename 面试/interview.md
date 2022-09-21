# 自我介绍

各位面试官上午好！我是王晓娜，目前在广东工业大学攻读电子信息硕士学位，很荣幸能得到这个面试机会。因为前端入门相对简单，也能及时带来成就感，所以对前端开发比较感兴趣，通过自学html，css，js等，培养了对前端技术的浓厚兴趣，在掌握了一些基础知识后接触了前沿的vue框架，利用vue2全家桶，es6，axios等开发了一个电商平台，经历此项目后，我对前端开发有了更多的理解，同时也对前期所学的知识进行了巩固。希望能加入贵公司与大家一起工作学习，从而在前端开发领域深入发展。以上是我的个人情况，请面试官指点。谢谢！

**为什么自学前端**：因为前端入门相对简单，也能及时带来成就感，总是和用户交互界面打交道，对这方面比较感兴趣。前端的工作所见即所得，写下代码就能呈现效果，直接看到UI动态效果，获得来自产品最直接的反馈。

**前端开发工程师做什么**：在移动端、PC端、VR设备等各类不同的设备与系统上，开发与用户交互的界面，完成从用户可视的交互界面到存储后台之间的开发建设。UI界面、活动页面、用户交互响应......均由前端开发工程师完成。前端这个职业的历史比较短，新技术层出不穷，很多问题还没有最优解，有很大的探索空间。

**项目收获**：经历此项目后，我对前端开发有了更多的理解，同时也对所学的知识进行了巩固。

# HTML5

## 什么是HTML5

 HTML5是HTML最新的修订版本，2014年10月由万维网联盟（W3C）完成标准制定。设计目的是为了在移动设备上支持多媒体。   

**总结：**

- HTML5是最新的HTML标准。

- 是专门为承载丰富的web内容而设计的，并且无需额外插件。
- HTML5拥有新的语义、图形以及多媒体元素。通常简称 “H5”。
- HTML5提供的新元素和新的API简化了web应用程序的搭建
- HTML5是跨平台的，被设计为在不同类型的硬件之上运行。

## HTML5中的新内容

### 文档声明类型

```html
<!DOCTYPE html>
```

< !DOCTYPE html >是html5文档类型声明，必须声明在HTML文档的第一行。用来告诉浏览器使用哪种模式来渲染页面，以及使用什么规则来验证页面。

目前浏览器的排版引擎有三种文档模式：

- 怪异/混杂模式：该模式是为了兼容很早之前针对旧版本浏览器的设计，并未严格遵循W3C标准而产生的一种页面渲染模式，浏览器用自己的方式解析代码。
- 接近标准模式：相较怪异模式，只有少数的怪异行为。
- 标准/严格模式：该模式严格按照W3C规定的HTML 与 CSS 标准来渲染页面。

声明< !DOCTYPE html >，浏览器会默认开启标准模式；否则，部分浏览器会使用混杂模式渲染页面。

**Q：HTML5如果不写<! DOCTYPE html > ，页面还会正常工作么**

**A**：页面可以正常工作，页面会根据浏览器自身的解析标准来解析，可能会导致页面在不同的浏览器呈现不同的效果，但是浏览器认为这是正常的。

### 新特性

#### 新增语义化标签

![1660144695808](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1660144695808.png)

![1660144723770](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1660144723770.png)

#### 新增表单元素

- < datalist > 定义输入控件的预定义选项
- < keygen > 定义键对生成器字段
- < output > 定义计算结果
- HTML5版本之前的表单元素有input、select、button、textarea

#### 新增表单控件（新的输入类型）和输入属性

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1660145278958.png" alt="1660145278958" style="zoom:67%;" />

#### 强大的图像支持

**HTML5画布Canvas**

canvas元素使用JavaScript在网页上绘制图形。拥有多种绘制路径、矩形、圆形、字符以及添加图像的方法。

**HTML5内联SVG**

什么是SVG？

- SVG指可伸缩矢量图形
- SVG用于定义用于网络的基于矢量的图形
- SVG使用XML格式定义图形
- SVG图像在放大或改变尺寸的情况下其图形质量不会有损失
- SVG是万维网联盟的标准

与其他图像格式(比如jpeg，gif)相比，SVG的优势：

- SVG图像可通过文本编辑器来创建和修改
- SVG图像可被搜索、索引、脚本化或压缩
- SVG是可伸缩的
- SVG图像可在任何的分辨率下被高质量地打印
- SVG可在图像质量不下降的情况下被放大

**Canvas  vs  SVG**

- Canvas通过JS来绘制2D图形，支持分辨率，不支持事件处理器，是逐像素进行渲染的，最适合图像密集型的游戏
- SVG使用XML描述2D图形，不依赖分辨率，支持事件处理器，最适合带有大型渲染区域的应用程序(比如谷歌地图)，复杂度高会减慢渲染速度，不适合游戏应用

#### 强大的多媒体支持

video、audio -- 用于播放视频和音频的媒体。

### 新增API

#### 本地存储

用本地存储取代cookie

在网页刷新的时候，所有数据都会被清空，这时候就要用到本地存储的技术，通过本地存储，web应用程序能够在用户浏览器中对数据进行本地的存储。前端本地存储的方式有三种，分别是cookie，localStorage和sessionStorage。

**不同点**

**生命周期：**

cookie：可以设置失效时间，没有设置的话，默认是关闭浏览器后失效。

localStorage：除非手动清除，否则将会永久保存。

sessionStorage：仅在当前网页会话下有效，关闭页面或浏览器后就会被清除。

**存放数据大小：**

cookie：4KB左右

localStorage和sessionStorage：可以保存5MB的信息

**http请求：**

cookie：每次都会携带在HTTP头中，如果使用cookie保存过多数据会带来性能问题

localStorage和sessionStorage：仅在客户端（即浏览器）中保存，不参与和服务器的通信

**易用性：**

cookie：需要程序员自己封装，原生的Cookie接口不友好

localStorage和sessionStorage：原生接口可以接受，也可以再次封装来对Object和Array有更好的支持。

**Q：localStorage和sessionStorage的用法与区别**

localStorage和sessionStorage所使用的方法是一样的，

设置缓存数据sessionS.setItem(key,value)  

获取缓存数据sessionS.getItem(key) 

获取全部缓存数据sessionStorage.valueOf()  

获取指定下标的key键值：sessionStorage.key(N)

删除缓存数据sessionStorage.removeItem(key)

清空缓存数据sessionStorage.clear()

**localStorage和sessionStorage区别**

（1）

localStorage是存储没有截止日期的数据，永久保存在浏览器里面，可以用来跨页面传递参数

sessionStorage是针对一个会话来存储数据，在关闭网页时会清除缓存数据，用来保存一些临时的数据，防止用户刷新页面之后丢失了一些参数。

（2）

两者都受同源策略的影响，但是，在同源的前提下，

对于以下三种情况：

a) 新打开的页面，

b) 在当前页面通过window.open( ) 跳转到新的页面

c) 在当前页面点击a链接跳转到新的页面(包含属性rel=“openner)

localStorage都可以共享数据，但是sessionStorage只能在b、c两种情况下共享数据。

#### 地理定位

 HTML5 Geolocation（地理定位）用于定位用户的位置。 

#### 拖放

拖放（Drag 和 Drop）是很常见的特性。它指的是您抓取某物并拖入不同的位置。

拖放是 HTML5 标准的组成部分：任何元素都是可拖放的。

#### 应用缓存

HTML5 引入了应用程序缓存（Application Cache），这意味着可对 web 应用进行缓存，并可在没有因特网连接时进行访问。

应用程序缓存为应用带来三个优势：

1. 离线浏览 - 用户可在应用离线时使用它们
2. 速度 - 已缓存资源加载得更快
3. 减少服务器负载 - 浏览器将只从服务器下载更新过或更改过的资源

#### Web Worker

众所周知，JavaScript是单线程的语言。当我们面临需要大量计算的场景时（比如视频解码等），UI线程就会被阻塞，甚至浏览器直接卡死。现在前端遇到大量计算的场景越来越多，为了有更好的体验，HTML5中提出了Web Worker的概念。Web Worker允许一段JavaScript程序运行在主线程之外的另外一个线程中。可以使脚本运行在新的线程中，它们独立于主线程，可以进行大量的计算活动，而不会影响主线程的UI渲染。当计算结束之后，它们可以把结果发送给主线程，从而形成了高效、良好的用户体验。

当在 HTML 页面中执行脚本时，页面是不可响应的，直到脚本已完成。

Web worker 是运行在后台的 JavaScript，独立于其他脚本，不会影响页面的性能。您可以继续做任何愿意做的事情：点击、选取内容等等，而此时 web worker 运行在后台。

**使用场景**：（1）做在线编辑器，需要对全文的某些词进行替换，然后将字符串替换的工作放到worker中。（2）在高并发场景下，服务端计算压力较大时，可以考虑将部分运算迁移到浏览器中，可以利用webworker提高浏览器的并发能力，从而降低服务端的高并发压力。

由于 web worker 位于外部文件中，它们无法访问下列 JavaScript 对象：

- window 对象
- document 对象
- parent 对象

#### SSE

Server-Sent 事件指的是网页自动从服务器获得更新。

以前也可能做到这一点，前提是网页不得不询问是否有可用的更新。通过 Server-Sent 事件，更新能够自动到达。

例如：Facebook/Twitter 更新、股价更新、新的博文、赛事结果，等等。

## 被删元素

< acronym > < applet > < basefont > < big > < center > < dir > < font > < frame > < frameset > 

< noframes > < strikes > < tt >

## HTML5与HTML的区别

（1） html5 不区分是否是严格模式还是传统模式，而html 声明时有严格、传统、框架模式。 

（2） html没有语义化标签，而html5 添加了许多语义标签，使代码结构清晰，提高代码可读性，使浏览器能够识别正确的网页内容。  语义标签如：header、nav、footer、main、artical、section。

（3） html无法在网页上动态的绘制图片，而 html5 新增了canvas画布，canvas绘制的图片放大后会失真，而SVG可绘制矢量图形。 

## HTML5浏览器支持

所有现代浏览器都支持HTML5。包括Firefox（火狐浏览器），IE9及其更高版本，Chrome（谷歌浏览器），Safari，Opera等；国内的 遨游浏览器（Maxthon），以及基于IE或Chromium（Chrome的工程版或称实验版）所推出的360浏览器、搜狗浏览器、QQ浏览器、猎豹浏览器等国产浏览器同样具备支持HTML5的能力。

## HTML5的优点

提高可用性和可维护性，改进了用户体验。

新增语义化标签，有助于开发人员定义清晰的结构。

可以播放视频音频，增加多媒体元素。

利用h5动画，友好地替代了flash和silverlight。

爬虫抓取网站的时候，对于SEO很友好。

H5被大量应用于移动应用和游戏开发。

可移植性好。

## 语义化标签具有如下特点

根据标签的语义，在合适的地方给一个最为合理的标签，可以让页面结构更清晰。

- 比所有布局全部采用 div 标签阅读起来更清晰
- **利于 SEO，方便搜索引擎识别页面结构** - 这也是非常重要的
- 方便设备解析，比如盲人阅读，语义化标签比 div 标签要好很多

## HTML5的缺点

 现在大多数高版本浏览器都支持html5，但是少部分的低版本浏览器目前不支持html5，因新标签的引入，各浏览器之间将缺少一种统一的数据描述格式，造成用户体验不佳。 

## HTML其他面试题

### 重排和重绘

在页面加载时，浏览器会把HTML代码解析成一个DOM树，包含了所有的HTML标签，以及display：none的元素，还有js动态添加的元素，render tree类似于DOM tree，但区别很大，因为render tree能够识别样式，render tree的每个节点都有自己的样式，不会呈现出来的元素不包含在render tree中（如display：none的元素）。简单点理解DOM tree和CSS结合在一起就形成了render tree。

**重排**

重排(Reflow)：**元素的位置和尺寸大小发生变动时发生重排**，也叫回流。此时在Layout阶段，**重新计算每个元素在设备视口内的确切位置和大小**。当一个元素位置发生变化时，其父元素及其后边的元素位置都可能发生变化，代价极高。

**下面情况会发生重排：**

- 页面初始渲染，这是开销最大的一次重排
- 添加/删除可见的DOM元素
- 改变元素的位置
- 改变元素的尺寸，比如边距、填充、边框、宽度和高度等
- 改变元素内容，比如文字数量，图片大小等
- 改变元素字体大小
- 改变浏览器窗口尺寸，比如resize事件发生时
- 激活CSS伪类
- 设置style属性的值，因为通过设置style属性改变节点样式的话，每一次设置都会触发一次reflow
- 查询某些属性或调用某些计算方法：offsetWidth、offsetHeight等，当调用getComputedStyle方法，或者IE里的currentStyle时，也会触发重排。

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1662883885010.png" alt="1662883885010" style="zoom:50%;" />

**重绘**

重绘(Reoaint)：元素的样式发生变动，但是位置没有改变。此时在关键渲染路径中的Paint阶段，**将渲染树中的每个节点转换成屏幕上的实际像素**，这一步通常称为绘制或栅格化。

常见的引起重绘的属性：

![1662883651433](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1662883651433.png)

**性能优化**

（1）减少DOM树渲染时间（如降低HTML层级、标签尽量语义化）

（2）减少CSSOM树渲染时间（如降低选择器层级）

（3）减少HTTP请求次数及请求大小

（4）将CSS放在页面开始位置

（5）将js放在页面底部位置，并尽可能用defer或者async避免阻塞的js加载，确保DOM树生成完才会去加载JS

（6）用link代替@important

（7）如果页面css较少，尽量使用内嵌式

（8）为了减少白屏时间，页面加载时先快速生成一个DOM树

**减少回流和重绘的方法**

（1）不使用能够触发回流的属性（2）尽量不要使用table布局，因为一个小小的改动可能会使整个table进行重新布局（3）使用transform代替top，left，margin-left等属性（4）不要频繁操作元素的样式，对于静态页面，可以修改类名，而不是样式。

**关键渲染路径（Critical Rendering Path）**

关键渲染路径是指浏览器将HTML，CSS，JavaScript转换为屏幕上所呈现的实际像素这期间所经历的一系列步骤。优化关键渲染路径可提高渲染性能。

关键渲染路径共分为五个步骤：构建DOM->构建CSSOM->构建渲染树->布局->绘制

- 构建DOM树

  HTML文档描述一个页面的结构，但是浏览器无法理解和使用HTML，所以需要通过HTML解析器将HTML转换成浏览器能够理解的结构--DOM树。HTML文档中所有内容皆为节点，各节点之间有层级关系，彼此相连，构成DOM树。

  **构建过程**：读取HTML文档的字节(Bytes)，将字节转换成字符(Chars)，依据字符确定标签(Tokens)，将标签转换成节点(Nodes)，以节点为基准构建DOM树。

  在控制台打印出来的DOM结构和HTML内容几乎一样，但和HTML不同的是，DOM是保存在内存中的树状结构，可以通过JavaScript来查询或修改其内容。

- 样式计算

  **解析CSS**

  和HTML一样，浏览器无法直接理解纯文本的CSS样式，需要通过CSS解析器将CSS解析成styleSheets结构，也就是常说的CSSOM树。

  **属性值标准化**

  浏览器通常不容易理解我们设置的css样式属性值，需要将所有的值转换成渲染引擎容易理解的、标准化的计算值，这个过程就是属性值标准化。

  **计算DOM树中每个节点的样式**

  完成样式的属性值标准化后，就需要计算每个节点的样式属性，这个阶段CSS有两个规则：

  （1）继承规则：每个DOM节点都包含有父节点的样式

  （2）层叠规则：层叠是CSS的一个基本特征，是一个定义了如何合并来自多个源的属性值的算法

  该阶段最终输出的内容是每个DOM节点的样式，并被保存在ComputedStyle的结构中。

- 布局阶段

  经过构建DOM和样式计算，已经拿到了DOM树和DOM树中元素的样式，接下来需要计算DOM树中可见元素的几何位置，这个计算过程就是布局。

  **创建布局树**

  从DOM树的根节点开始遍历，将所有可见的节点加到布局树中，忽略不可见的节点。

  **布局计算**

  计算布局树节点的坐标位置。从根节点开始遍历，结合上面得到的样式，确定每个节点对象在页面上的具体大小和位置，将这些信息保存在布局树中。布局阶段输出的是一个盒子模型，它会精确地捕获每个元素在屏幕内的确切位置与大小。

- 分层

  因为页面中会有像3D变换、页面滚动、或者用z-index进行z轴排序等复杂效果，为了更方便实现这些效果，渲染引擎还需要为特定的节点生成专用的图层，并生成一棵对应的图层树。

- 图层绘制

  构建好图层树之后，渲染引擎就会对图层树中每个图层进行绘制。渲染引擎实现图层绘制，会把一个图层的绘制拆分成很多小的绘制指令，然后这些指令按照顺序组成一个待绘制列表。

- 栅格化操作

  实际上绘制操作是由渲染引擎中的合成线程来完成的。首先合成线程会将图层划分为图块，图块大小通常是256X256或者512X512。然后合成线程会按照视口附近的图块来优先生成位图，实际生成位图的操作是由栅格化来执行的。

  所谓栅格化，是指将图块转换为位图。

- 合成与显示

  一旦所有的图块都被栅格化，合成线程就会生成一个绘制图块的命令，然后将该命令提交给浏览器进程。

  浏览器进程里面有一个叫viz的组件，用来接收合成线程发过来的绘制图块命令，然后根据绘制图块命令，将其页面内容绘制到内存中，最后再将内存显示在屏幕上。

**一个完整的渲染流程可以总结如下**：

（1）渲染进程将HTML内容转换为浏览器能够读懂的DOM树结构。

（2）渲染引擎将CSS样式表转化为浏览器可以理解的styleSheets，计算出DOM节点的样式。

（3）创建布局树，并计算元素的布局信息。

（4）对布局树进行分层，并生成分层树。

（5）为每个图层生成绘制表，并将其提交给合成线程。

（6）合成线程将图层分成图块，并栅格化将图块转换成位图。

（7）合成线程发送绘制图块命令给浏览器进程。浏览器进程根据指令生成页面，并显示到显示器上。

### 说说对< meta >标签的理解

meta标签位于HTML文档头部的head标签之间。使用meta，可以定义页面编码语言、搜索引擎优化、自动刷新并指向新的页面、控制页面缓冲、响应式视窗等。

HTML5之前，meta标签只有两个属性，分别是name属性和http-equiv属性

（1）**name属性主要用于描述网页，对应属性是content，以便于搜索引擎机器人查找、分类**

| name          | content(举例)                    | 说明                           |
| ------------- | -------------------------------- | ------------------------------ |
| keywords      | 程序员                           | 为搜索引擎提供关键字列表       |
| description   | meta标签很重要                   | 告诉搜索引擎网站的主要内容     |
| robots        | all，none，(no)index，(no)follow | 告诉搜索机器人哪些页面需要索引 |
| author        | TG@qq.com                        | 标注网页的作者                 |
| copyright     | 本网站版权归TG所有               | 标注版权                       |
| generator     | 你所用的编辑器                   | 说明网站采用什么编辑器制作     |
| revisit-after | 7days                            | 网站重访                       |

（2）**http-equiv属性类似于http的头部协议，它回应给浏览器一些有用的信息，以帮助正确和精确地显示网页内容，与之对应的属性值为content**

| name             | content                       | 说明                                       |
| ---------------- | ----------------------------- | ------------------------------------------ |
| Expires          | Wed, 26 Feb 1997 08:21:57 GMT | 指定网页在缓存中的过期时间                 |
| Pragma           | no-cache                      | 禁止浏览器从本地计算机的缓存中访问页面内容 |
| Refresh          | http://www.baidu.com          | 自动刷新并指向新页面                       |
| Set-Cookie       | cookievalue=xxx；expires=xxx  | cookie设定                                 |
| Window-target    | _top                          | 强制页面在当前窗口以独立页面显示           |
| content-Type     | text/html;charset=utf-8       | 设定页面使用的字符集                       |
| content-Language | zh-cn                         | 显示语言的设定                             |
| imagetoolbar     | false/true                    | 指定是否显示图片工具栏                     |

HTML5中，name的属性新增了viewport、format-detection等

语法：

```html
<meta name="viewport" content="width=device-width,initial-scale=1.0,maxmum-scale=1.0,user-scalable=no">
```

- width=device-width-------将页面宽度设置为跟随屏幕宽度变化而变化
- initial-scale=1.0------设置浏览器首次加载页面时的初始缩放比例(0.0-10.0正数)
- maxmum-scale=1.0------允许用户缩放的最大比例(0.0-10.0正数)，必须大于等于minmum-scale
- minmum-scale------允许用户缩放的最小比例(0.0-10.0正数)，必须小于等于maxmum-scale
- user-scalable=no------是否允许用户手动缩放(yes或者no)

-----------------------------------------------------------------



# CSS3

## 盒模型

**什么是盒模型？**

CSS盒模型实质上是一个包围每个HTML元素的框，它定义了一种长方形的盒子，包括：外边距、边框、内边距以及实际的内容。

**盒模型的分类：**

盒模型从标准定义上分为标准盒模型和(替代)IE盒模型，从元素类型上分为块级盒模型和行内盒模型。

**盒模型的切换：**

通过box-sizing属性进行切换：

ie盒模型：box-sizing：border-box；

标准盒模型：box-sizing：border-content；

box-sizing定义元素宽度和高度的计算方式，它们是否应包含内边距和边框。

- box-sizing：border-box；高度和宽度包括内边距和边框
- box-sizing：content-box；高度和宽度不包括内边距和边框

## 三角形

```html
<div class="trangle"></div>
```

```css
.trangle {
    width: 0;
    height: 0;
    border: 10px solid transparent;
    border-left: 10px solid blue;
}
```

## BFC

（1）什么是BFC？

BFC是Block Formatting Context，块级格式化上下文的缩写，简单的说BFC是一个完全独立的空间，这个空间里子元素的渲染不会影响到外面的布局。

（2）如何创建BFC？（可以触发生成BFC的条件有哪些？）

常见的几种如下：

```css
display：inline-block;
display: table-cell;
display: flex;
display: grid;
overflow: hidden;
position: absolute;
position: fixed;
```

（3）BFC解决了什么问题？

- 垂直方向margin重叠的问题。
- 使用Float脱离文档流，父元素高度塌陷问题。
- 两栏布局

## 对齐方式

### 水平居中对齐元素

（1）使用**margin：0 auto；**（没有父盒子）

要使块元素水平居中，使用**margin：0 auto；**元素将占用指定的宽度，剩余空间将在两个外边距之间平均分配。注意：如果未设置width属性（或将其设置为100%），则居中对齐无效。

（2）使用**position+负margin值**

首先进行子绝父相定位，设置子容器的left：50%；然后设置左外边距为负的自身宽度的一半

（3）使用**position和transform**

首先进行子绝父相定位，设置子容器的left：50%；然后再水平向左移动自身盒子宽度的50%，transform：translate(-50%,0);

（4）使用**table-cell**

对父容器设置display：table-cell；**text-align**：center；

对子盒子设置display：inline-block；

（5）使用**flexbox**

将父容器设置display：flex；**justify-content**：center（flex-direction：row）

### 水平居中对齐文本

如果仅需在元素内居中文本，请使用text-align：center；

### 垂直居中对齐元素

（1）给子盒子设置padding：20px 0；

（2）使用**position+负margin值**

（3）使用**position和transform**

（4）使用**table-cell**

对父容器设置display：table-cell；**vertical-align**：middle；

对子盒子设置display：inline-block；

（5）使用**flexbox**

将父容器设置display：flex；**align-items**：center;（flex-direction：row）

### 垂直居中对齐文本

- 如果是单行文字垂直居中，则只需将容器的行高等于高度即可。


- 如果是多行文字垂直居中，则需要对父容器设置行高等于高度，文字盒子设置属性line-height：1.5; display：inline-block；vertical-align：middle; 。


## CSS布局

### flexbox布局

弹性框布局模块，可以更轻松地设计灵活的响应式布局结构，而无需使用浮动或定位。

弹性布局中必须有一个display属性设置为flex的父元素。弹性容器的直接子元素会自动成为弹性项目。

#### flex容器属性

- flex-direction：定义容器要在哪个方向上堆叠flex项目

  垂直堆叠(从上到下)column，垂直堆叠(从下到上)column-reverse，水平堆叠(从左到右)row，水平堆叠(从右到左)row-reverse

- flex-wrap：规定是否应该对flex项目换行

  在必要时进行换行wrap，不换行nowrap，以相反的顺序换行wrap-reverse

- flex-flow：用于同时设置flex-direction和flex-wrap属性的简写属性

- justify-content：用于在主轴方向上对齐flex项目

  在容器的中心对齐center，在开头对齐flex-start，在末端对齐flex-end，显示之前，之间，之后带有空格的flex项目space-around，显示之间有空格的flex项目space-between

- align-items：用于侧轴方向上对齐flex项目

  在容器中间对齐center，顶部对齐flex-start，底部对齐flex-end，

  拉伸flex项目以填充容器stretch，使flex项目基线对齐baseline

- align-content用于对齐弹性线

  弹性线之间有相等的间距space-between，弹性线在其之前、之间和之后带有空格space-around，拉伸弹性线以占据剩余空间stretch，在容器之间显示弹性线center，在容器开头显示弹性线flex-start，在容器末尾显示弹性线

**完美居中**

如果容器的justify-content和align-items属性都设置为center，则项目会在两个轴的方向同时居中。

#### 弹性项目属性

- order：规定flex项目的顺序
- flex-grow：规定某个flex项目相对于其余flex项目将增长多少，项目的放大比例，默认为0，即如果存在剩余空间，也不放大。
- flex-shrink：规定某个flex项目相对于其余flex项目将收缩多少，项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。
- flex-basis：规定flex项目的初始长度，默认值是auto，就是自动。有设置width则占据空间就是width，没有设置就按内容宽度来。
- flex：是flex-grow、flex-shrink和flex-basis属性的简写属性。后两个属性可选。flex默认值为0 1 auto。flex：none等同于flex：0 0 auto；flex：auto等同于flex： 1 1 auto；
- align-self：规定弹性容器内所选项目的对齐方式，将覆盖容器的align-items属性所设置的默认对齐方式

### position属性

position属性规定应用于元素的定位方法的类型

有五个不同的位置值：

- static

  HTML元素默认情况下的定位方式为static，静态定位的元素不受top、bottom、left和right属性的影响，始终根据页面的正常流进行定位。

- relative

  相对于其正常位置进行定位，未脱标

- fixed

  相对于视口进行定位，即使滚动页面，它也始终位于同一位置。脱标。

- absolute

  相对于最近的定位祖先元素进行定位，如果没有祖先，则使用文档主体(body)，并随页面滚动一起移动。脱标。

- sticky

  粘性元素根据滚动位置在相对和固定之间切换。起先它会被相对定位，直到在视口中遇到给定的偏移为止-然后将其“粘贴”在适当的位置。

### CSS网格布局

网格布局由一个display属性设置为grid或inline-grid的父元素以及一个或多个子元素组成。网格容器的直接子元素自动成为网格项目。

- display：grid；生成块级的网格容器
- display：inline-grid；生成行内的网格容器

**网格间隙**

- grid-column-gap：设置列之间的间隙
- grid-row-gap：设置行之间的间隙
- grid-gap：是grid-row-gap和grid-column-gap属性的简写

**列之间的线称为列线，行之间的线称为行线。**当把网格项目放在网格容器中时，可以引用行号或列号。

```css
/* 把网格项目放在列线1，并在列线3结束它 （在水平方向占了两个格子）*/
.item1 {
    grid-column-start: 1;
    grid-column-end: 3;
}
/* 把网格项目放在行线1，并在行线3结束它 （在垂直方向占了两个格子）*/
.item1 {
    grid-row-start: 1;
    grid-row-end: 3;
}
```



## CSS文本效果

### 文字溢出

（1）overflow

overflow属性指定在元素的内容太大而无法放入指定区域时是裁剪内容还是添加滚动条。

overflow可以设置以下值：

- visible：默认。溢出没有被剪裁。内容在元素框外渲染
- hidden：溢出被剪裁，其余内容将不可见
- scroll：溢出被剪裁，同时添加滚动条以查看其余内容
- auto：与scroll类似，但仅在必要时添加滚动条

（2）**text-overflow**

text-overflow属性规定应如何向用户呈现未显示的溢出内容

- 被裁剪：white-space：nowrap；text-overflow：clip；
- 将其呈现为省略号：white-space：nowrap；text-overflow：ellipsis；

### 字换行

word-wrap属性使长文字能够被折断并换行到下一行。

- 允许长单词被打断并换行到下一行：word-wrap：break-word；

### 换行规则

word-break属性指定换行规则。

- 将连字符打断：word-break：keep-all；
- 在任何字符处打断：word-break：break-all；

### 书写模式

writing-mode属性规定文本行是水平放置还是垂直放置。

- 水平放置：writing-mode：horizontal-tb；
- 垂直放置：writing-mode：vertical-rl；

## CSS过渡

过渡属性transition允许在给定时间内平滑地改变属性值。

- transition：property duration timing-function delay；

  ```css
  div {
    width: 100px;
    height: 100px;
    background: red;
    transition: width 2s linear 1s;
  }
  
  div:hover {
    width: 300px;
  }
  ```

  ```css
  div {
    width: 100px;
    height: 100px;
    background: red;
    transition: width 2s, height 2s, transform 2s;
  }
  
  div:hover {
    width: 300px;
    height: 300px;
    transform: rotate(180deg);
  }
  ```

- transition-property：规定设置过渡效果的CSS属性的名称（简写属性，用于将四个过渡属性设置为单一属性）

- transition-duration：规定完成过渡效果需要多少秒或毫秒

- transition-timing-function：规定速度效果的速度曲线

- transition-delay：定义过渡效果何时开始

## CSS动画

动画使元素逐渐从一种样式变为另一种样式。

@keyframes规则

如果在@keyframes规则中指定了CSS样式，动画将在特定时间逐渐从当前样式更改为新样式。

要使动画生效，必须将动画绑定到某个元素。

```css
/* 动画代码 */
@keyframes example {
    /* 方式一：from内一般写入动画的初始状态，to写入动画的结束状态
    from {background-color: red;}
    to {background-color: yellow;} */
    /* 方式二：百分比形式表示动画的状态，0%表示动画的初始状态，100%表示动画的结束状态 */
    0%   {background-color:red; left:0px; top:0px;}
    25%  {background-color:yellow; left:200px; top:0px;}
    50%  {background-color:blue; left:200px; top:200px;}
    75%  {background-color:green; left:0px; top:200px;}
    100% {background-color:red; left:0px; top:0px;}
}
/* 应用动画的元素 */
div {
    width: 100px;
    height: 100px;
    background-color: red;
    position: relative;
	animation-name: example;
	animation-duration:5s;
	animation-timing-function: linear;
	animation-delay: 2s;
	animation-iteration-count: infinite;
	animation-direction: alternate;
    /* 动画属性简写 */
    /* animation: example 5s linear 2s infinite alternate; */
}
```

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1660227514506.png" alt="1660227514506" style="zoom:67%;" />

## CSS媒体查询

语法：

```css
@media not|only mediatype and (expressions) {
    CSS-Code;
}
```

简单实例：

```css
body {
    background-color: pink;
}
/* 此媒体查询应用于：媒体类型为screen，且视口为480px或更宽 */
@media screen and (min-width: 480px) {
    body {
        background-color: lightgreen;
    }
}
```



## CSS其他面试题

### Q1：display：none、visibility：hidden、opacity：0的区别？

- display：none；

  DOM结构：浏览器不会渲染display属性为none的元素，不占据空间；

  事件监听：无法进行DOM事件监听；

  性能：动态改变此属性会引起重排，性能较差；

  继承：不会被子元素继承，毕竟子类也不会被渲染；

  transition：transition不支持display

- visibility：hidden；

  DOM结构：元素被隐藏，但是会被渲染不会消失，占据空间；

  事件监听：无法进行DOM事件监听；

  性能：动态改变此属性会引起重绘，性能较高；

  继承：会被子元素继承，子元素可以通过设置visibility：visible；来取消隐藏；

  transition：visibility会立即显示，隐藏时会延时

- opacity：0；

  DOM结构：透明度为100%，元素隐藏，占据空间；

  事件监听：可以进行DOM事件监听；

  性能：提升为合成层，不会触发重绘，性能较高；

  继承：会被子元素继承，但子元素并不能通过opacity：1来取消隐藏；

  transition：opacity可以延时显示和隐藏

- 其他隐藏元素的方式：position：absolute；设置一个很大的left负值定位，使元素定位在可见区域之外。transform：scale(0)；将一个元素设置为缩放无限小，元素将不可见，元素原来的位置将被保留。

  height：0；将元素高度设置为0，并消除边框。filter：blur(0)；CSS3属性，将一个元素的模糊度设置为0，从而使这个元素“消失”在页面。

### Q2：如何实现左边定宽，右边自适应？

A2：

**严格意义实现方案**（左边盒子宽度变化，右边盒子会自动撑满剩余的空间）

（1）flex布局

```css
<style>
.box-wrapper {
    width: 600px;
    height: 400px;
    border: 1px solid #000;
    display: flex;
}
.left-box {
    width: 200px;
    height: 100%;
    background: red;
}
.right-box {
    background: blue;
    flex: 1;// 无论左边盒子宽度如何修改，右边盒子都会占满剩余的空间
}
</style>
```

（2）table布局

```css
<style>
.box-wrapper {
    width: 600px;
    height: 400px;
    border: 1px solid #000;
    display: table;
}
.left-box {
    width: 200px;
    height: 100%;
    background: red;
    display: table-cell;
}
.right-box {
    height: 100%;
    background: blue;
    display: table-cell; // 无论左边盒子宽度如何修改，右边盒子都会占满剩余的空间
}
</style>
```

（3）grid布局

```css
<style>
.box-wrapper {
    width: 600px;
    height: 400px;
    border: 1px solid #000;
    display: grid;
    /* 声明列的宽度 */
    grid-template-columns: 200px auto; // left-box的宽度是200px，right-box的宽度是auto 
}
.left-box {
    background: red;
}
.right-box {
    background: blue;
}
</style>
```

**非严格意义实现方案**（左边盒子宽度变化，右边盒子宽度需要手动修改）

（1）float+calc(需要手动计算右边盒子计算属性中的宽度)

```html
<body>
    <div class="box-wrapper">
        <div class="left-box">
            left-box
        </div>
        <div class="right-box">
            right-box
        </div>
    </div>
</body>
```

```css
<style>
* {
    margin: 0;
    padding: 0
}
.box-wrapper {
    width: 600px;
    height: 400px;
    border: 1px solid #000;
}
.left-box {
    float: left;
    width: 200px;
    height: 100%;
    background: red;
}
.right-box {
    float: right;
    width: calc(100% - 200px);  // 当左边盒子宽度修改时，右边盒子宽度也需要手动改一下
    height: 100%;
    background: blue;
}
</style>
```

（2）inline-block+calc

```css
<style>
.box-wrapper {
    width: 600px;
    height: 400px;
    border: 1px solid #000;
}
.left-box {
    display: inline-block;
    width: 200px;
    height: 100%;
    background: red;
}
.right-box {
    display: inline-block;
    width: calc(100% - 200px);  // 当左边盒子宽度修改时，右边盒子宽度需要手动修改才能达到真正的自适应
    height: 100%;
    background: blue;
}
</style>
```

（3）position+padding

```css
<style>
.box-wrapper {
    width: 600px;
    height: 400px;
    position: relative;
    border: 1px solid #000;
}
.left-box {
    width: 200px;
    height: 100%;
    background: red;
    position: absolute;
}
.right-box {
    padding-left: 200px;  // 当左边盒子宽度修改时，右边盒子宽度需要手动修改padding-left才能达到真正的自适应
    height: 100%;
    background: blue;
}
</style>
```

### Q3：CSS提高页面性能的方法有哪些？

A3：

1、属性简写     目的：减小生产包体积

2、图标替换     目的：减少http请求节约带宽

3、删除不必要的零和单位     目的：减少生产包体积

4、背景图使用精灵图     目的：减少http请求节约带宽

（1）属性设置使用简写

```css
p {
    margin-top: 10px;
    margin-right: 20px;
    margin-bottom: 30px;
    margin-left: 40px;
}
/* 简写 */
p {
    margin: 10px 20px 30px 40px;
}
```

（2）用CSS替换图片

- 用CSS画三角形
- 用CSS画箭头
- 用CSS画圆形

（3）删除不必要的零和单位

```css
/* 优化前写法 */
.box {
    width: 0.2em;
    height: 20.0em;
    padding: 0px;
}
/* 优化后写法 */
.box {
    width: .2em;
    height: 20em;
    padding: 0;
}
```

（4）用CSS精灵图替代单个文件加载

精灵图中包含很多图标，仅仅用到背景定位就可以拿到想要的图标。方案的优势：用一个HTTP请求替代多个HTTP请求。

### Q4：CSS中哪些属性可以继承

A4：

字体：font、font-family、font-size、font-style、font-variant、font-weight

文字展示：line-height、text-align、text-indent、text-transform(控制文本大小写)

字母间距：letter-spacing

可见性：visibility

字间距：word-spacing

### Q5：如何区分px/em/rem/vw/vh

A5：

px：绝对单位，网页开发基本长度单位

em：相对单位，相对当前盒子字体大小进行计算（没给的话就是浏览器默认字体16px）。常用于字体缩进

rem：相对单位，相对根元素html字体大小进行计算（没给的话就是浏览器默认字体16px）。配合媒体查询处理移动端适配问题

vw+vh：相对单位，相对当前网页视口宽度和高度进行计算

![1662969841322](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1662969841322.png)

### Q6：清除浮动

**为什么要清除浮动**？

 答：清除浮动是为了解决父级元素因为子级元素浮动而引起的内部高度塌陷为0的问题。 

由于父级盒子很多情况下，不方便给高度，但是盒子浮动又不占用位置，最后父级盒子高度为0时，就会影响下面的标准流盒子。由于浮动元素不再占用原文档流的位置，所以它对后面的元素排版产生影响。

清除浮动的本质是清除浮动元素造成的影响

**清除浮动有哪些方法？各有什么优缺点？**

- 父元素固定高度

优点：简单，代码量少，没有兼容问题

缺点：内部元素高度不确定的情况下无法使用

```html
<div class="box-container">
    <img src="./image/js.jpg">
    <div class="right-box">
        <div class="right-box-title">前端开发工程师</div>
        <div class="right-box-content">综合就业率第一</div>
    </div>
</div>
```

```css
.box-container {
    width: 142px;
    height: 45px;  // 给父元素固定高度
    padding: 10px;
    boeder: 1px solid red;
}
img {
    width: 45px;
    height: 45px;
    float: left;
    margin-right: 10px;
}
.right-box {
    float: right;
}
```

- ##### 额外标签法


优点：简单，代码量少，没有兼容性问题

缺点：需要添加无语义的html元素，代码不够优雅，不便于后期的维护

```html
<div class="box-container">
    <img src="./image/js.jpg">
    <div class="right-box">
        <div class="right-box-title">前端开发工程师</div>
        <div class="right-box-content">综合就业率第一</div>
    </div>
    <!-- 添加新元素，利用css提供的clear: both清除浮动 -->
    <div class="clear-element"></div>
</div>
```

```css
.box-container {
    width: 142px;
    padding: 10px;
    boeder: 1px solid red;
}
img {
    width: 45px;
    height: 45px;
    float: left;
    margin-right: 10px;
}
.right-box {
    float: right;
}
/* 清除浮动：添加新元素 */
.clear-element {
    clear: both;
}
```

- ##### 使用伪元素(最常用)


优点：仅用css实现，不容易出现怪问题

缺点：仅支持IE8以上和非IE浏览器

```css
.box-container {
    width: 142px;
    padding: 10px;
    boeder: 1px solid red;
}
/* 对父元素添加伪元素 */
.box-container::after {
    content: "";
    display: block;
    height: 0;
    clear: both;
}
img {
    width: 45px;
    height: 45px;
    float: left;
    margin-right: 10px;
}
.right-box {
    float: right;
}
```

- **使用双伪元素**

优点：代码更简洁

缺点：需要照顾低版本浏览器

```css
.box-container {
    width: 142px;
    padding: 10px;
    boeder: 1px solid red;
}
/* 对父元素添加伪元素 */
.box-container::before,
.box-container::after {
    content: "";
    display: table;
}
.box-container::after {
    clear: both;
}
.box-container {
    *zoom: 1;
}
img {
    width: 45px;
    height: 45px;
    float: left;
    margin-right: 10px;
}
.right-box {
    float: right;
}
```

- **触发父元素BFC**

优点：仅用CSS实现，代码少，浏览器支持好

缺点：用overflow：hidden触发父元素BFC情况下，可能会使内部本应正常显示的元素被裁剪

```css
.box-container {
    width: 142px;
    padding: 10px;
    boeder: 1px solid red;
    /* overflow: hidden、auto或scroll; */
    float: left;
    /* position: absolute; */
    /* display: inline-block */
    /* 以上属性均可触发BFC */
}

img {
    width: 45px;
    height: 45px;
    float: left;
    margin-right: 10px;
}
.right-box {
    float: right;
}
```

### Q7：margin和padding分别适合什么场景使用

A7：

margin是用来隔开元素与元素的间距；padding是用来隔开元素与内容的间隔。
margin用于布局分开元素使元素与元素互不相干。
padding用于元素与内容之间的间隔，让内容（文字）与（包裹）元素之间有一段距离。
何时应当使用margin：
•需要在border外侧添加空白时。
•空白处不需要背景（色）时。
•上下相连的两个盒子之间的空白，需要相互抵消时。如15px+20px的margin，将得到20px的空白。
何时应当时用padding：
•需要在border内测添加空白时。
•空白处需要背景（色）时。
•上下相连的两个盒子之间的空白，希望等于两者之和时。如15px+20px的padding，将得到35px的空白。



----------------------------------------------------------------

# JS

## 原型

**prototype的定义**

只有函数才有prototype属性，当创建函数时，JS会为这个函数自动添加prototype属性，prototype是给其它对象提供共享属性和方法的对象。

**__ proto __的作用**

首先，__ proto __ 是对象所独有的， 当你在访问一个对象属性时，如果该对象内部不存在这个属性，那么就会去它的__ proto __ 属性所指向的对象（父类对象）上查找，如果父类对象依旧不存在这个属性，那么就会去其父类对象的 __ proto __ 属性所指向的对象上去查找，以此类推，直到找到null。这个查找的过程，就构成了原型链。

**原型链**

实例对象的__ proto __ 指向自己构造函数的prototype，原型链由此产生：

在创建构造函数的实例时，实例继承了构造函数上prototype的所有属性和方法（实例通过设置自己的__ proto __ 指向构造函数的prototype来实现这种继承）

原型链的尽头是Object.prototype，所有对象均从Object.prototype继承属性。

即Object.prototype.__ proto __ = null

**JS的成员查找机制(规则)**

1. 当访问一个对象的属性(包括方法)时，首先查找这个**对象自身**有没有该属性。
2. 如果没有就查找它的原型（也就是__ proto __ 指向的**prototype原型对象**）。
3. 如果还没有就查找原型对象的原型（**Object的原型对象**）。
4. 依次类推一直找到Object为止（**null**）。
5. __ proto __对象原型的意义就在于为对象成员查找机制提供一个方向，或者说一条线路。

**总结**

先有Object.prototype（原型链顶端），Function.prototype继承Object.prototype而产生，最后，Function和Object和其他构造函数继承Function.prototype而产生。

Object.__ proto __ = Function.prototype

Function.__ proto __ = Function.prototype

Function.prototype.__ proto __ = Object.prototype

Object.prototype.__ proto __ = null

## 继承

**原型链继承**

关键核心：让父类的实例作为子类的原型

缺点：不能传递参数，且引用值类型的数据会被实例共享

```js
function Person(name, age) {
  this.name = name;
  this.age = age;
  this.friends = ['Yasuo', 'Zed', 'Yi'];
}
Person.prototype.running = function () {
  console.log('在跑步~');
};
function Student() {
  this.score = 99;
}
Student.prototype = new Person();
Student.prototype.goToSchool = function () {
  console.log('去上学~');
};
let s1 = new Student();
let s2 = new Student();
s1.friends.push('LeeSin');
console.log(s1.friends);  // ['Yasuo', 'Zed', 'Yi','LeeSin']
console.log(s2.friends);  // ['Yasuo', 'Zed', 'Yi','LeeSin']
```

**盗用构造函数继承**

关键核心：在子类构造函数中使用call()调用父类构造函数

优点：解决了原型链继承中不能传参且引用值共享的问题

缺点：不能调用父类原型上的方法，因为Student.prototype和Person.prototype没有任何关系

```js
function Person(name, age) {
  this.name = name;
  this.age = age;
  this.friends = ['Yasuo', 'Zed', 'Yi'];
}
Person.prototype.running = function () {
  console.log('在跑步~');
};
function Student(name, age) {
  Person.call(this, name, age);
  this.score = 99;
}
// Student.prototype = new Person();
Student.prototype.goToSchool = function () {
  console.log('去上学~');
};
let s1 = new Student('Cyan', 18);
let s2 = new Student('Csy', 22);
console.log(s1.name);
console.log(s2.name);
s1.friends.push('LeeSin');
console.log(s1.friends);  // ['Yasuo', 'Zed', 'Yi','LeeSin']
console.log(s2.friends);  // ['Yasuo', 'Zed', 'Yi']
console.log(s1.running());  s1.running() is not a function
```

**组合继承（原型链+构造函数）**

关键核心：使用call()调用父类的属性，使用new获取父类原型上的方法

优点：解决了不能调用父类原型上的方法的问题

缺点：多次调用了父类构造函数

```js
function Person(name, age) {
  this.name = name;
  this.age = age;
  this.friends = ['Yasuo', 'Zed', 'Yi'];
}
Person.prototype.running = function () {
  console.log('在跑步~');
};
function Student(name, age) {
  Person.call(this, name, age);
  this.score = 99;
}
Student.prototype = new Person();
Student.prototype.goToSchool = function () {
  console.log('去上学~');
};
let s1 = new Student('Cyan', 18);
let s2 = new Student('Csy', 22);
console.log(s1.name);
console.log(s2.name);
s1.friends.push('LeeSin');
console.log(s1.friends);
console.log(s2.friends);
console.log(s1.running());
```

**寄生组合继承**

关键核心：使用Object.create()来解决多次调用父类构造函数问题

```js
function Father(name) {
    this.name = name;
}
Father.prototype.say = function() {
    console.log('my name is',this.name)
}
function Son(name,age) {
    this.age = age;
    Father.call(this,name)
}
Son.prototype = Object.create(Father.prototype)
Son.prototype.constructor = Son;
const son = new Son('yaya',6);
console.log(son.age);
son.say();
```

**ES6 Class继承**

主要是依靠：extends、super，该继承的效果和寄生组合继承方式一样。class也是通过构造函数模拟实现的，是一种语法糖。

```js
// 如果子类没有定义constructor方法，这个方法会被默认添加
// 子类必须在constructor方法中调用super方法，否则新建实例时会报错。这是因为子类自己的this对象，必须先通过父类的构造函数完成塑造，得到与父类同样的实例属性和方法，然后再对其进行加工，加上子类自己的实例属性和方法。如果不调用super方法，子类就得不到this对象。
class Parent {
    constructor(name,age) {
        this.name = name;
        this.age = age
    }
    say() {
        console.log(this.name)
    }
}
class Child extends Parent {
    constructor(name,age,num) {
        super(name,age); // 调用父类的constructor(x,y)
        this.num = num;
    }
    sing() {
        console.log(this.name)
    }
}
// super这个关键字，既可以当作函数使用，也可以当作对象使用。在这两种情况下，它的用法完全不同。
// super函数
// super作为函数时，代表父类的构造函数。ES6要求，子类的构造函数必须执行一次super函数。
// 若子类中没有定义constructor方法，这个方法会被默认添加，相当于已经执行了一次super函数
// super虽然代表了父类的构造函数，但是返回的是子类B的实例，即super内部的this指的是B的实例，因此super()在这里相当于A.prototype.constructor.call(this)
// 作为函数时，super()只能用在子类的构造函数之中，用在其他地方就会报错
// super对象
// super作为对象时，在普通方法中，super指向父类的原型对象，super可以取到定义在父类原型对象上的属性和方法，取不到父类实例上的属性或方法。通过super调用父类方法时，方法内部的this指向当前的子类实例。
// 在静态方法中，super指向父类,通过super调用父类的方法时，方法内部的this指向当前的子类，而不是子类的实例。
```

## 数据类型

**js中的数据类型有哪些？**

- 基本数据类型

  undefined、null、string、number、boolean、symbol、bigInt

  基本数据类型占用空间固定，保存在栈里面，操作的是值本身。栈一般存放变量的值，内存空间由系统自动分配和释放。

- 引用数据类型

  Object、Array、Function、Date、FormData、Set、Map等等

  引用类型占用空间不固定，保存在堆中，操作的是指向对象的一个指针。堆一般存放复杂对象，内存空间为动态分配，不主动释放的话，可能会由垃圾回收机制自动回收。

**null是对象类型吗？**

不是，typeof null输出object，这只是JS存在的一个悠久的Bug。在JS最初版本中使用的是32位系统，为了性能考虑使用低位存储变量的类型信息，000开头代表是对象，然而null表示全零，所以将它错误的判断为object。虽然现在的内部类型判断代码已经改变了，但是对于这个Bug却是一直流传下来。

**如何理解Symbol类型，使用场景是什么？**

Symbol属于基本数据类型之一，Symbol()可以用来生成唯一值。

使用场景：创建Symbol()实例并将其用作对象的新属性，就可以确保它不会覆盖已有的对象属性，不会发生属性冲突的危险。

**js中判断数据类型的方式有哪些？**

- typeof

  优点：使用简单

  缺点：功能残缺，对于原始数据类型，除了null都可以显示正确的类型typeof null == ’object‘；对于引用类型来说，除了函数都会显示object，所以typeof并不能准确判断变量到底是什么类型的。

  typeof只能准确判断7种数据类型：string、number、boolean、symbol、undefined、bigint、function。

  ```js
  const array = [];
  const object = {};
  const number = 1n;
  const string = 'string';
  
  const type = typeof array;
  console.log(type);// object
  const type1 = typeof number;
  console.log(type1);// bigint
  ```

- Object.prototype.toString.call

  优点：适用于判断所有数据类型

  缺点：使用上相对typeof而言比较繁琐

  ```js
  const array = [];
  const object = {};
  const number = 1;
  const string = 'string';
  
  const type = Object.prototype.toString.call(array);
  console.log(type);// [object Array]
  const type1 = Object.prototype.toString.call(object);
  console.log(type1);// [object Object]
  const type2 = Object.prototype.toString.call(number);
  console.log(type2);// [object Number]
  const type3 = Object.prototype.toString.call(string);
  console.log(type3);// [object String]
  ```

- instanceof（排除）

  instanceof运算符用于检测构造函数的prototype属性是否出现在某个实例对象的原型链上，无法判断原始类型。

**什么是浅拷贝和深拷贝？以及如何实现浅拷贝和深拷贝？**

 对象类型在赋值的过程中其实是复制了地址，从而会导致改变了一方其他也都被改变的情况。通常在开发中我们不希望出现这样的问题，我们可以使用浅拷贝来解决这个情况。 

- 浅拷贝只是拷贝一层，更深层次对象级别的只拷贝引用

  方法一：通过Object.assign实现浅拷贝

  ```js
  let a = {
      age: 1,
  }
  let b = Object.assign({},a);
  a.age = 2;
  console.log(b.age); // 1
  ```

  方法二：通过扩展运算符...实现浅拷贝

  ```js
  let a = {
      age: 1,
  }
  let b = {...a};
  a.age = 2;
  console.log(b.age); // 1
  ```

  方法三：for in循环赋值

  方法四：ES6中Array.from()复制数组，此方法复制为浅拷贝

  浅拷贝只解决了第一层的问题，如果接下去的值中还有对象的话，那么就又回到最开始的话题了，两者享有相同的地址，要解决这个问题，得用深拷贝。

- 深拷贝拷贝多层，每一级别的数据都会拷贝

  方法一：通过JSON.parse(JSON.stringify(object))实现深拷贝

  但是该方法也是有局限性的：（1）在遇到函数、undefined、symbol的时候，该对象不能正常的序列化；（2）不能解决循环引用的对象

  ```js
  let a {
      age: 1,
      jobs: {
          first: 'FE',
      }
  }
  let b = JSON.parse(JSON.stringify(a));
  a.jobs.first = 'native';
  console.log(b.jobs.first); // FE
  ```

  方法二：JQuery中的extend方法

  $extend([deep],target,object)
  
  方法三：自己实现一个简易版的深拷贝
  
  ```js
  function deepClone(obj) {
      function isObject(o) {
          return (typeof o === 'object' || typeof o === 'function') && o !== null;
      }
      if(!isObject(obj)) {
          throw new Error('非对象');
      }
      let isArray = Array.isArray(obj);
      let newObj = isArray ? [...obj] : {...obj};
      Reflect.ownKeys(newObj).forEach(k => {
          newObj[k] = isObject(obj[k]) ? deepClone(obj[k]) : obj[k];
      })
      return newObj;
  }
  ```

## 构造函数

构造函数是一种特殊函数，主要用来初始化对象，即为对象成员赋初值，它总与new一起使用。可以把对象中一些公共的属性和方法抽取出来，然后封装到这个函数里面。

new在执行时会做4件事：

（1）在内存中创建一个新的空对象

（2）让this指向这个新的对象

（3）执行构造函数里面的代码，给这个新对象添加属性和方法

（4）返回这个新对象（所以构造函数里面不需要return）

注意：没有return，默认返回的结果是实例化对象，写了return，如果是return的是简单类型，返回的结果依然是实例化对象，如果是复杂类型，则返回结果是复杂类型

## 事件机制

**事件触发三阶段（捕获阶段，目标阶段，冒泡阶段）**

（1）从window往事件触发处传播，遇到注册的捕获事件会触发

（2）传播到事件触发处时触发注册的事件

（3）从事件触发处往window传播，遇到注册的冒泡事件会触发

**注册事件**

 通常我们使用 `addEventListener` 注册事件，该函数的第三个参数可以是布尔值，也可以是对象。对于布尔值 `useCapture` 参数来说，该参数默认值为 `false` ，`useCapture` 决定了注册的事件是捕获事件还是冒泡事件。对于对象参数来说，可以使用以下几个属性 

- capture：布尔值，和useCapture作用一样
- once：布尔值，职位true表示该回调只会调用一次，调用后会移除监听
- passive：布尔值，preventDefault表示永远不会调用

 一般来说，如果我们只希望事件只触发在目标上，这时候可以使用 `stopPropagation` 来阻止事件的进一步传播。通常我们认为 `stopPropagation` 是用来阻止事件冒泡的，其实该函数也可以阻止捕获事件。`stopImmediatePropagation` 同样也能实现阻止事件，但是还能阻止该事件目标执行别的注册事件。 

注意：有些事件是不支持事件冒泡的，比如onblur、onfocus、onmouseover、onmouseleave

**addEventListener与on绑定事件的区别**

（1）addEventListener可以给一个元素注册多个事件，而on在同一时间只能注册一个事件

（2）addEventListener使用removeEventListener进行解绑，on事件解绑需要将其设置为none

**事件对象**

（1）event就是一个事件对象，写在侦听函数的括号里，当形参来看

（2）事件对象只有有了事件才会存在，是系统自动创建的，不需要传递参数

（3）事件对象是事件的一系列相关数据的组合，比如鼠标点击事件包含了鼠标相关的信息

（4）这个事件可以自己命名，比如event，evt，e等

（5）事件对象也有兼容性，IE6,7,8通过window.event实现

**ev.currentTarget和ev.target的区别**

ev.currentTarget是绑定事件的元素(this)，而ev.target是当前触发事件的元素。

eg：如果给ul元素绑定点击事件，则ev.currentTarget(this)是ul。当点击ul触发事件，ev.target是ul，当点击li触发事件，ev.target是li。

阻止对象默认行为

e.preventDefault()

**事件代理(事件委托)**

不给每个子节点单独设置事件监听器，而是设置在其父节点上，然后利用冒泡原理影响设置每个子节点。

例如：给ul注册事件，然后利用事件对象的target来找到当前点击的li，然后事件冒泡到ul上，ul有注册事件，就会触发事件监听器。

如果一个节点中的子节点是动态生成的，那么子节点需要注册事件的话应该注册在父节点上。

优点：（1）只需要将同类元素的事件委托给父级或者更外级的元素，不需要给所有的元素都绑定事件，减少内存占用空间，提升性能 （2）不需要给子节点注销事件 （3）动态新增的元素无需重新绑定事件

## 闭包

**定义**

**闭包指有权访问另一个函数作用域中变量的函数。---JS高级程序设计**

闭包是一个可以访问到外部作用域的内部函数。

- 内部函数可以访问外部函数中定义的变量
- 内部函数可以访问外部函数中定义的形参
- 内部函数可以访问外部块中定义的变量

闭包需要满足以下特征：（1）有外层函数嵌套内层函数；（2）内层函数使用外层函数的局部变量；（3）内层函数返回外部，并且被全局变量保存。

**作用**

延伸了变量的作用范围。

**执行上下文**

当前代码执行的一个环境与范围。

**词法作用域**

词法作用域是指内部函数在定义的时候就决定了其外部作用域。

```js
(function autorun(){
    let x = 1;
    function log(){  // 闭包的外部作用域是在其定义的时候已决定
      console.log(x);
    };
    
    function run(fn){
      let x = 100;
      fn();   // 而不是执行的时候
    }
    
    run(log); //1
})();
```

上述例子中，log( ) 函数是一个闭包，它在这里访问的是autorun()函数中的x变量，而不是run函数中的变量。autorun()的函数作用域即是log()函数的词法作用域。

**作用域链**

每一个作用域链都有对其父作用域的引用。当使用一个变量的时候，JS引擎会通过变量名在当前作用域查找，若没有找到，会一直沿着作用域链一直向上查找，直到global全局作用域。

**总结**

当一个函数被创建并从另一个函数返回时，它会携带一个背包，背包中是函数声明时作用域内的所有变量。

**被闭包引用的外部作用域中的变量将一直存活直到闭包函数被销毁。如果一个变量被多个闭包所引用，那么直到所有的闭包被垃圾回收后，该变量才会被销毁。**

闭包使得timer定时器，事件处理，Ajax请求等异步任务更加容易。

**闭包的使用场景**

（1）return 回一个函数 （2）函数作为参数 （3）自执行函数 （4）循环赋值 （5）使用回调函数就是在使用闭包 （6）节流/防抖功能函数

**使用闭包需要注意什么**

容易导致内存泄露。闭包会携带包含其他的函数作用域，因此会比其他函数占用更多的内存。过度使用闭包会导致内存占用过多，所以要谨慎使用闭包。

**怎么检查内存泄露**

performance面板和memory面板可以找到泄露的现象和位置

## this指向

this的指向，是在函数被调用的时候确定的，完全取决于函数的调用方式。

**普通函数调用模式**

非严格模式中，普通函数中的this指向为全局对象window。

严格模式中，普通函数中的this表现为undefined。

**对象中的方法调用模式**

指向对象本身。

**new**

当使用new关键字调用函数时，函数中的this一定是JS创建的新对象(实例对象)。

**箭头函数**

箭头函数的this是在创建它时外层this的指向（根据当前的词法作用域来决定this）。

- 创建箭头函数时，就已经确定了它的this指向。
- 箭头函数内的this指向外层的this指向。

**DOM事件处理函数调用**

onclick和addEventListener中的this指向绑定事件的元素。

一些浏览器，比如IE6~8下使用attachEvent，this指向window。

**内联事件处理函数调用**

```js
<button class="btn1" onclick="console.log(this === document.querySelector('.btn1'))">点我呀</button> // true
<button onclick="console.log((function(){return this})());">再点我呀</button> // window
```

**call、apply、bind调用模式**

非严格模式下，指定为null和undefined的this值会自动指向全局对象（浏览器中是window对象）,其余值指向被new Object()包装的对象。

严格模式下，绑定到指定的第一个参数。

**call和apply的共同点**

它们都能改变函数执行时的上下文，将一个对象的方法交给另一个对象来执行，并且是立即执行的。调用call和apply的对象，必须是一个函数Function。

**call和apply的区别**

call和apply用法类似，只是参数不一样，call可以接收任意个参数。apply的参数是数组（或者类数组）。

**bind**

bind方法与apply和call比较类似，也能改变函数体内的this指向。不同的是，bind方法的返回值是函数，并且需要稍后调用才会执行。而apply和call是立即调用。

**call的使用场景**

（1）对象的继承

```js
Father.call(this);
```

（2）借用方法(类数组借用Array原型链上的方法)

```js
// 以下代码可以实现domNodes应用Array下的所有方法
let domNodes = Array.prototype.slice.call(document.getElementByTagName("p"))
```

**apply的使用场景**

（1）获取数组中的最大值/最小值

```js
let max = Math.max.apply(null,array);
let min = Math.min.apply(null,array);
```

（2）实现两个数组的合并

```js
let arr1 = [1,2,3];
let arr2 = [4,5,6];
Array.prototype.push.call(arr1,arr2);
console.log(arr1); // [1,2,3,4,5,6]
```

**总结**

| 调用方式     | this指向                                  |
| ------------ | ----------------------------------------- |
| 普通函数调用 | window                                    |
| 构造函数调用 | 实例对象 原型对象里面的方法也指向实例对象 |
| 对象方法调用 | 该方法所属对象                            |
| 事件绑定方法 | 绑定事件对象                              |
| 定时器函数   | window                                    |
| 立即执行函数 | window                                    |

注：（1）匿名函数也指向window（2）IE中attachEvent中的this总是指向全局对象window

## 事件循环

**JavaScript为什么是单线程的**

如果JS不是单线程的，同时有两个方法操作一个DOM节点，一个做删除任务，一个做修改任务，那么此时浏览器该听谁的？所以，为了避免复杂性，从一诞生，JS就是单线程的。但是单线程就导致很多任务需要排队，只有一个任务执行完才能执行下一个任务。如果某个执行时间太长，就容易造成阻塞；为了解决这一问题，JS引入了事件循环机制。

**事件循环是什么**

主线程不断从任务队列中读取事件， 每次单个宏任务执行完毕后， 检查微任务队列是否为空， 如果不为空，会按照先入先出的规则全部执行完微任务后， 清空微任务队列， 然后再执行下一个宏任务，如此循环。 这个过程是循环不断的，这种运行机制就叫做事件循环。

**同步&异步**

- 同步：是按顺序执行，执行完一个再执行下一个，需要等待、协调运行。
- 异步：就是彼此独立，在等待某事件的过程中继续做自己的事，不需要等待这一事件完成后再工作。宏任务和微任务都属于异步任务

**异步&多线程**

两者并不是一个同等关系，异步是最终目的，多线程只是实现异步的一种手段。异步是当一个调用请求发送给被调用者，而调用者不用等待其结果的返回可以做其他的事情。实现异步可以采用多线程技术或交给另外的进程来处理。

**JavaScript是如何实现异步的**

JavaScript是通过事件循环(Event Loop)实现异步的。

**事件循环的执行顺序**：首先JavaScript代码从上到下执行，每遇到定时器等宏任务会将任务放在宏任务队列中，遇到Promise.then等微任务会将任务放入到微任务队列中。等到主执行栈中的代码执行完毕，会清空微任务队列，先加入的先执行，后加入的后执行，然后再去检查宏任务队列，将可执行的宏任务拿到执行栈中执行，每次只取出一个宏任务，执行完毕再次清空微任务队列，清空完毕再去检查宏任务队列，以此类推。

**浏览器中的宏任务**

宏任务可以理解为每次执行栈执行的代码就是一个宏任务

script(整体代码)，setTimeout，setInterval，setImmediate，MessageChannel，postMessage，I/O，UI render

**浏览器中的微任务**

微任务可以理解为在当前宏任务执行结束后立即执行的任务

- promise.then：promise的then方法就是一个微任务
- async await：async函数的await之后的内容是以微任务的形式来执行
- MutationObserver：MutationObserver的作用是监控dom变化，dom变化了就会执行，时间节点是等待所有代码都执行完，才执行该监控
- process.nextTick

**浏览器是多线程的**

JavaScript是单线程的，但浏览器是多线程的，多个线程相互配合以保持同步。

**浏览器里常驻的线程**

（1）JS线程 （2）GUI渲染线程(管理页面渲染，回流重绘的) （3）基本UI事件线程 （4）定时器线程 （5）异步Ajax线程

**Node和浏览器的事件循环区别**

 浏览器环境下，微任务的任务队列是每个 宏任务 执行完之后执行。而在 Node.js 中，微任务会在事件循环的各个阶段之间执行，也就是一个阶段执行完毕，就会去执行微任务队列的任务。 

**总结**

（1）事件循环是JS引擎等待任务、执行任务、休眠的无线循环，它通过宏任务队列来接收任务，先进的先完成且一次只做一件事。

（2）宏任务队列中的第一个任务是script，它最早被执行

（3）当执行完宏任务后，微任务队列开始执行，然后页面渲染一次，再进行下一个宏任务

（4）宏任务中，事件比定时器先进入宏任务队列（优先级更高）

（5）其他线程无法像JavaScript主线程一样操作DOM

## 垃圾回收

**为什么要垃圾回收**

 如果没有垃圾回收机制，适时清理不被引用的值并释放相应的内存空间，JavaScript 解释器将会消耗完系统中所有可用内存，造成系统崩溃。

**垃圾回收机制**

 JS 的垃圾回收机制是为了以防内存泄漏，**内存泄漏的含义就是当已经不需要某块内存时这块内存还存在着**，垃圾回收机制就是间歇的不定期的寻找到不再使用的变量，并释放掉它们所指向的内存。  

**垃圾回收的两种方式**

- 标记清除

  （1） 给所有变量增加一个标记，如果是进入执行环境（比如声明变量），则标记为“进 入环境”，如果是结束执行环境（比如执行完相关函数），则标记为“离开环境”； 

  （2） 去掉“进入环境”的变量标记以及被该变量所引用的变量标记（比如闭包）； 

  （3） 还存在标记的变量即是需要被清理的变量。 

- 引用计数

  每个对象计算指向它的指针的数量，当有一个指针指向自己，那么计数值记为1，当删除一个指向自己的指针时，计数值减1，那么计数值为0的需要销毁。

**内存泄露**

指程序申请内存后，无法释放已申请的内存空间，造成内存泄露。

**内存溢出**

指程序申请内存时，没有足够的内存供申请者使用。（内存泄露堆积后会导致内存溢出）

**常见内存泄露的原因**

（1）全局变量引起的内存泄露（由于我们使用未声明的全局变量，意外的创建了一个全局变量，这个全局变量一直无法被回收）

（2）闭包引起的内存泄露

（3）dom清空或删除时，事件未清除导致的内存泄露

（4）循环引用带来的内存泄露

**如何减少垃圾回收开销**

（1）在对象结束使用后 ，令 obj = null。这样利于解除循环引用，使得无用变量及时被回收；
（2）js 中开辟空间的操作有 new(), [ ], { }, function (){…}。最大限度的实现对象的重用；
（3）慎用闭包。闭包容易引起内存泄露。本来在函数返回之后，之前的空间都会被回收。但是由于闭包可能保存着函数内部变量的引用，且闭包在外部环境，就会导致函数内部的变量不能够销毁。

**垃圾回收的缺陷**

和其他语言一样，javascript 的 GC 策略也无法避免一个问题：GC 时，停止响应其他操作，这是为了安全考虑。而 Javascript 的 GC 在 100ms 甚至以上，对一般的应用还好，但对于 JS 游戏，动画对连贯性要求比较高的应用，就麻烦了。这就是新引擎需要优化的点：避免 GC 造成的长时间停止响应。

**优化垃圾回收**

（1）分代回收（Generation GC）：与 Java 回收策略思想是一致的。目的是通过区分“临 时”与“持久”对象；多回收“临时对象”区（young generation），少回收“持久对 象”区（tenured generation），减少每次需遍历的对象，从而减少每次 GC 的耗时。
（2）增量GC：这个方案的思想很简单，就是“每次处理一点，下次再处理一点“，如此类推。

## 数组的操作方式

### 数组去重

方法一：双循环去重

```js
function unique(arr) {
    if(! Array.isArray(arr)) {
        console.log('type error!')
        return ;
    }
    let newArr = [arr[0]];
    for(let i = 1; i < arr.length; i++) {
        let flag = true;
        for(let j = 0; j < newArr.length; j++) {
            if(arr[i] == newArr[j])
                {
                    flag = false;
                    break;
                }
        }
        if(flag) {
            newArr.push(arr[i])
        }
    }
    return newArr;
}
```

方法二：indexOf方法去重1

```js
function unique(arr) {
    let res = [];
    for (let i = 0; i <arr.length; i++) {
        if(res.indexOf(arr[i]) === -1) {
            res.push(arr[i])
        }
    }
}
```

方法三：indexOf方法去重2

```js
function unique(arr) {
    if (!Array.isArray(arr)) {
        console.log('type error!')
        return
    }
    return Array.prototype.filter.call(arr, function(item, index){
        return arr.indexOf(item) === index;
    });
}
```

方法四：相邻元素去重（使用Array.sort()+一行遍历冒泡）

```js
function unique(arr) {
    arr = arr.sort();
    let res = [];
    for(var i = 0; i < arr.length; i++) {
        if(arr[i] !== arr[i-1]) {
            res.push(arr[i]);
        }
    }
    return res;
}
```

方法五：利用对象属性去重

```js
function unique(arr) {
    let obj = {};
    let res = [];
    for(let i = 0; i < arr.length; i++) {
        if(!obj[arr[i]]) {
            res.push(arr[i])
            obj[arr[i]] = 1
        } else {
            obj[arr[i]]++
        }
    }
    return res
}
```

方法六：Set与解构赋值去重

```js
function unique(arr) {
    return [...new Set(arr)]
}
```

方法七：Array.from与Set去重

```js
function unique(arr) {
    if (!Array.isArray) {
        console.log('出错了！')
        return ;
    }
    return Array.from(new Set(arr));
}
```

### 数组扁平化

定义：扁平化就是将多维数组变成一维数组，不存在数组的嵌套

方法一：ES6 flat

```js
function flatten(arr) {
    return arr.flat(Infinity);
}
```

方法二：递归

```js
function flatten(arr) {
    let result = [];
    arr.forEach((item) => {
        if(Array.isArray(item)) {
            result = result.concat(flatten(item))
        } else {
            result.push(item)
        }
    })
    return result;
}
```

方法三：解构运算符

```js
function flatten(arr) {
    while(arr.some(function(item) {
        return Array.isArray(item)
    })) {
        arr = [].concat(...arr);
    }
    return arr;
}
```

### 改变原数组的数组操作（9种）

- ES5

  shift()、unshift()、pop()、push()、reverse()、sort()、splice(start,length,item)

- ES6

  copyWith(target,start,end)、fill(value,start,end)

### 不改变原数组的数组操作（8种）

- ES5

  concat()、join()、slice(start,end)、toLocaleString()、toString()、indexOf()、lastIndexOf()

- ES7

  includes()

注：indexOf()不能识别NaN，includes()是为了弥补indexOf的这个缺点

### 数组遍历方法（12种）

js中遍历数组并不会改变原始数组的方法共有12种：

- ES5

  forEach()、every()、some()、filter()、map()、reduce()、reduceRight()

- ES6

  find()、findIndex()、keys()、values()、entries()

**forEach**

定义：按升序为数组中含有效值的每一项执行一次回调函数

语法

```js
array.forEach(function(currentValue,index,arr),thisValue)
```

参数

- function()：必须，数组中每个元素需要调用的函数

  回调函数的参数

  1. currentValue：必须，数组当前元素的值
  2. index：可选，当前元素的索引值
  3. arr：可选，数组对象本身

- thisValue：可选，当执行回调函数时this绑定对象的值，默认为undefined

注意：（1）无法中途退出循环，只能用return退出本次回调，进行下一次回调，类似于for循环中的continue

​            （2）它总是返回undefined值，即使你return了一个值

**every**

定义：检查数组所有元素是否都符合函数定义的条件

语法

```js
array.every(function(currentValue,index,arr),thisValue)
```

方法返回值的规则

（1）如果数组中检测到有一个元素不满足，则整个表达式返回false，且剩余的元素不会再进行检测

（2）如果所有元素都满足条件，则返回true

**some**

定义：数组中是否有满足判断条件的元素

语法

```js
array.every(function(currentValue,index,arr),thisValue)
```

方法返回值的规则

（1）如果有一个元素满足条件，则表达式返回true，剩余的参数不会再执行检测

（2）如果没有满足条件的元素，则返回false

**filter**

定义：返回一个新数组，其包含通过所提供函数实现的测试的所有元素

**map**

定义：创建一个新数组，其结果是该数组中的每个元素都调用所提供函数后返回的结果

**reduce**

定义：对累加器和数组中的每个元素（从左到右）应用一个函数，最终合并为一个值

语法

```js
array.reduce(function(total,currentValue,index,arr),initialValue)
```

参数

- function()：必须，数组中每个元素需要调用的函数

  回调函数的参数

  1. total：必须，初始值，或者上一次调用回调返回的值
  2. currentValue：必须，数组当前元素的值
  3. index：可选，当前元素的索引值
  4. arr：可选，数组对象本身

- thisValue：可选，指定第一次回调的第一个参数

注意：（1） 如果 initialValue 在调用 reduce 时被提供，那么第一个 total 将等于 initialValue，此时 currentValue 等于数组中的第一个值 

​            （2）如果initialValue未被提供，那么total等于数组中的第一个值，currentValue等于数组中的第二个值。此时如果数组为空，那么将抛出TypeError

​            （3）如果数组仅有一个元素，并且没有提供initialValue，或提供了initialValue但数组数组为空，那么回调不会被执行，数组的唯一值将被返回

**reduceRight**

reduceRight()方法的功能和reduce()功能是一样的，不同的是reduceRight()从数组的末尾向前将数组中的项做累加。

**find**

定义：用于找出第一个符合条件的数组成员，并返回该成员，如果没有符合条件的成员，则返回undefined

**findIndex**

定义：返回第一个符合条件的数组成员的位置，如果所有成员都不符合条件，则返回-1

**keys()  values()  entries()**

定义：三个方法都返回一个新的Array Iterator对象，对象根据方法不同包含不同的值

语法

```js
// 无参数
array.keys()
array.values()
array.entries()
```

**其他**

- Array.from()

  入参为一个类数组或者一个可迭代对象，返回一个数组实例

- 什么是类数组，常见的话有哪些

  有元素属性以及可索引的对象，如函数的arguments、Element NodeList等





## JS其他面试题

### Q1：原生JS遍历时获取下标的方法

A1：

方法一：给每个按钮自定义data-index属性

```js
for(var i = 0; i < btns.length; i++){
     btns[i].setAttribute('data-index',i)
     btns[i].onclick = function(){
        console.log(this.dataset['index'])
     }
 }
```

方法二：存下标

```js
for(var i = 0; i < btns.length; i++){
    btns[i].index = i;
    btns[i].onclick = function(){
        console.log(this.index)
     }
}
```

方法三：forEach

```js
btns.forEach(function(item, index) {
    item.onclick = function() {
    console.log(index)
    }
})
```

方法四：let

```js
  for(let i = 0; i< btns.length; i++){ 
    btns[i].onclick = function(){
        console.log(i)
    }
}
```

方法五：闭包

```js
for(var i = 0; i < btns.length; i++) {
    (function(j) {
        btns[j].onclick = function() {
            console.log(j);
        }
    })(i)
}
```

方法六：闭包

```js
for(var i = 0; i < btns.length; i++) {
    btns[i].onclick = (function(j) {
        return function() {
            console.log(j)
        }
    })(i)
}
```



# ES6

ES6是新一代JS语言标准，对JS语言核心内容做了升级优化，规范了JS使用标准，新增了JS原生方法，使得JS使用更加规范，更加优雅，更适合大型应用的开发。

## let const和var的区别

（1）声明变量时不存在变量提升

（2）块级作用域：只在声明所在的块级作用域内有效

（3）暂时性死区(声明变量之前不可以对变量进行赋值，本质：只有等到声明变量的那一行代码出现，才可以获取和使用该变量。 )

（4）不可重复声明同一个变量

（5）声明的变量不会挂在window上

（6）const声明变量后必须立马对其赋值，否则会报错

（7）const声明简单类型的变量值不可更改，复杂类型内部数据可以更改

## 变量的解构赋值

ES6允许按照一定模式，从数组和对象中提取值，对变量进行赋值，这被称为解构。本质上属于模式匹配，只要等号两边的模式相同，左边的变量就会被赋予对应的值。

## 模板字符串

模板字符串是增强版的字符串，用反引号(`)标识。它可以当做普通字符串使用，也可以用来定义多行字符串，或者在字符串中嵌入变量。

```js
// 普通字符串
`In JavaScript '\n' is a line-feed.`

// 多行字符串
`In JavaScript this is
 not legal.`

console.log(`string text line 1
string text line 2`);

// 字符串中嵌入变量
let name = "Bob", time = "today";
`Hello ${name}, how are you ${time}?`
```

## 箭头函数和普通函数的区别

（1）语法更简洁、清新

（2）箭头函数不会创建自己的this，而是指向父级作用域的this（指向在定义时所处的执行环境的this指向）

（3）call()/.apply()/.bind()无法改变箭头函数中this的指向（箭头函数继承而来的this指向永远不变）

（4）箭头函数不可以被当做构造函数

（5）箭头函数没有原型prototype

（6）箭头函数不可以使用arguments对象，可以使用...args

（7）箭头函数不支持new.target

（8）箭头函数不能用作Generator函数，不能使用yield关键字

## rest参数

rest参数(形式为“...变量名”)，用于获取函数的多余参数，这样就不需要使用arguments参数对象了。

rest参数搭配的变量是一个数组，该变量将多余的参数放入数组中。

与解构赋值相结合

```js
const [a,...b] = [1,2,3];
console.log(a); // 1
console.log(b); // [2,3]
```

与Set数据集合一起使用，实现数组去重

```js
const arr = [1,2,3,4,2,5,1];
const [...newArr] = new Set(arr);
console.log(newArr); // [1,2,3,4,5]
```

注意：（1）rest参数之后不能再有其他参数，即只能是最后一个参数，否则会报错。（2）函数的length属性，不包括rest参数。

## 扩展运算符

扩展运算符(spread)是三个点(...)。它好比rest参数的逆运算，将一个数组转为用逗号分隔的参数序列。

**扩展运算符的应用**

（1）复制数组

```js
const a1 = [1,2];
// 写法一
const a2 = [...a1];
// 写法二
const [...a2] = a1;
```

（2）合并数组

```js
const arr1 = ['a','b'];
const arr2 = ['c'];
const arr3 = ['d','e'];
// ES6的合并数组
const arr4 = [...arr1, ...arr2, ...arr3]
```

（3）字符串

扩展运算符还可以将字符串转为真正的数组。

```js
[...'hello']; // ["h", "e", "l", "l", "o"]
```

（4）将伪数组转为真正的数组

```js
const divs = document.querySelectorAll('div');
const divArr = [...divs];
```



## Symbol

ES6引入了一种新的原始类型Symbol，表示独一无二的值。它属于JS语言的原生数据类型之一，其他数据类型是：undefined、null、布尔值（Boolean）、字符串（String）、数值（Number）、大整数（BigInt）、对象（Object）。

## Set

Set数据结构类似数组，数组中所有的数据都是唯一的，没有重复的值，它本身是一个构造函数。

## Map

Map是ES6引入的一种类似于Object的新的数据结构，Map可以理解为是Object的超集，打破了以传统键值对形式定义对象，对象的key不再局限于字符串，也可以是Object。可以更加全面的描述对象的属性。

## for of

**原生具备Iterator接口的数据结构有**

Array，Map，Set，String，TypedArray，函数的arguments对象，NodeList对象

因此for of不能遍历对象，因为对象没有iterable（遍历器）属性。

**遍历数组/字符串**

for of在遍历数组和字符串时，原型上的属性不会被遍历下来

```js
Array.prototype.c = 'c';
const arr = [1,2,3,4];
for(let i of arr) {
    console.log(i);
} // 1 2 3 4
const str = 'abc';
for(let i of str) {
    console.log(i);
} // a b c
```

**遍历Set/Map数据结构**

for of在遍历Set时，与遍历数组方法相同，但在遍历Map时，只能将键和值一起遍历下来，如果只想遍历键或者值的话，i需要写成数组的形式

```js
const s = new Set([1, 2, 3, 4])
for(let i of s ) {
    console.log(i);
}   // 1 2 3 4
   
const myMap=new Map();
myMap.set('1', '2');
myMap.set('3', '4');
for(let i of myMap) {
    console.log(i);
}  //  [ '1', '2' ]  [ '3', '4' ]
    
for (let [key, value] of myMap) {
    console.log(key + value);
}  // 12 34
```

**与for in的区别**

（1）for in遍历的是数据结构的下标(index)或者键(key)，for of遍历的是数据结构的值

（2）for in可以遍历所有的数据结构，但是for of只能遍历具有Iterator属性的数据结构

（3）for in遍历到数据结构自身和原型上的可枚举的属性和方法，但是for of只会遍历数据结构自身的值

## Promise

Promise是异步编程的一种解决方案，用来解决两个问题：

（1）避免了层层嵌套的回调函数（回调地狱），代码难以维护。

（2）Promise可以支持多个并发的请求，获取并发请求中的数据。

注意：Promise可以解决异步的问题，但是不能说Promise本身是异步的。

--------------

Promise是一个构造函数，接收一个函数作为参数，这个函数用于处理异步任务，且需要传递两个参数：

（1）resolve：异步操作执行成功后的回调函数

（2）reject：异步操作执行失败后的回调函数

```js
const promise = new Promise(function(resolve,reject) {
    if(/* 异步操作成功 */) {
       resolve(value)
    } else {
       reject(error)
    }
})
```

**then的用法**

通过Promise.then获取处理结果，then方法可以接收两个参数，第一个对应resolve的回调，第二个对应reject的回调。Promise.then中的函数是异步执行的。

**catch的用法**

和then的第二个参数一样，用来指定reject的回调。

另一个作用：在执行resolve的回调时，如果抛出异常了，那么并不会报错卡死，而是会进到catch方法中执行reject的回调。

**all的用法**

Promise.all接收一个数组参数，里面的值最终都返回Promise对象。利用Promise.all可以并行执行多个异步操作，并且在一个回调中处理所有的返回数据。

**race的用法**

Promise.race()并发处理多个异步任务，只要有一个任务完成就能得到结果。

## Async/Await

## 模块化



## ES6其他面试题

**Q1：日常前端代码开发中，有哪些值得用ES6去改进的编程优化或者规范？**

A1：1、常用箭头函数来取代 var self = this;的做法。 2、常用 let 取代 var 命令。 3、常用数组/对象的结构赋值来命名变量，结构更清晰，语义更明确，可读性更好。 4、在长字符串多变量组合场合，用模板字符串来取代字符串累加，能取得更好地效果 和阅读体验。 5、用 Class 类取代传统的构造函数，来生成实例化对象。 6、在大型应用开发中，要保持 module 模块化开发思维，分清模块之间的关系，常用 import、export 方法。
# 浏览器

## HTTP协议

**什么是HTTP协议**

HTTP协议即超文本传送协议（Hyper Text Transfer Protocol），它规定了客户端与服务器之间进行网页内容传输时，所必须遵守的传输格式。

**HTTP原理**

（1）客户端的浏览器首先要通过网络与服务器建立连接，该连接是通过TCP来完成的，一般TCP连接的端口号是80。建立连接后，客户端发送一个请求给服务器。（2）服务器接收到请求后，给与相应的响应信息。

**HTTP协议交互模型**

HTTP协议采用了**请求/响应**的交互模型。

**HTTP请求消息**

客户端发起的请求叫做HTTP请求，客户端发送到服务器的消息，叫做请求消息。

**HTTP请求消息的组成部分**

- 请求行，请求行由请求方式、URI和HTTP协议版本3个部分组成，中间使用空格隔开

- 请求头部，用来描述客户端的基本信息，从而把客户端相关的信息告知服务器。

  <img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1661924730360.png" alt="1661924730360" style="zoom:50%;" />

- 空行，最后一个请求字段的后面是空行，通知服务器请求头部至此结束。请求消息中的空行，用来分隔请求头部和请求体

- 请求体，请求中存放的，是要通过post方式提交到服务器的数据

  注意：只要post请求才有请求体，get请求没有请求体

**HTTP响应消息**

响应消息就是服务器响应给客户端的消息内容，也叫作响应报文

**HTTP响应消息的组成部分**

- 状态行，由HTTP协议版本、状态码和状态码的描述文本3个部分组成，它们之间使用空格隔开
- 响应头部，用来描述服务器的基本信息
- 空行，在最后一个响应头字段结束之后，会紧跟一个空行，用来通知客户端响应头部至此结束，响应消息中的空行，用来分隔响应头部和响应体
- 响应体，响应体中存放的是服务器响应给客户端的资源内容

**HTTP的请求方法**

![1661926929334](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1661926929334.png)

**HTTP响应状态码**

HTTP响应状态码也属于HTTP协议的一部分，用来标识响应的状态。

**HTTP响应状态码的组成及分类**

HTTP状态码由三个十进制数字组成，第一个十进制数字定义了状态码的类型，后两个数组用来对状态码进行细分。

**HTTP状态码分为5种类型**

| 分类    | 分类描述                                                     |
| ------- | ------------------------------------------------------------ |
| 1**     | 信息，服务器收到请求，需要请求者继续执行操作(实际开发中很少遇到1**类型的状态码) |
| 2**     | **成功，操作被成功接收并处理**                               |
| **3**** | **重定向，需要进一步的操作以完成请求**                       |
| **4**** | **客户端错误，请求包含语法错误或无法完成请求**               |
| **5**** | **服务器错误，服务器在处理请求的过程中发生了错误**           |

1. 2**成功相关的响应状态码

   2** 范围的状态码，表示服务器已成功接收到请求并进行处理。常见的 2**类型的状态码如下：

   | 状态码 | 状态码英文名称 | 中文描述                                                |
   | ------ | -------------- | ------------------------------------------------------- |
   | 200    | OK             | 请求成功。一般用于GET与POST请求                         |
   | 201    | Created        | 已创建。成功请求并创建了新的资源，通常用于POST或PUT请求 |

2. 3**重定向相关的响应状态码

   3** 范围的状态码，表示服务器要求客户端重定向，需要客户端进一步的操作以完成资源的请求。常见的 3**类型的状态码如下：

   | 状态码 | 状态码英文描述    | 中文描述                                                     |
   | ------ | ----------------- | ------------------------------------------------------------ |
   | 301    | Moved Permanently | 永久移动。请求的资源已被永久移动到新的URI，返回信息会包括新的URI，浏览器会自动定向到新URI。今后任何新的请求都应使用新的URI代替 |
   | 302    | Found             | 临时移动。与301类似。但资源只是临时被移动。客户端应继续使用原有URI |
   | 304    | Not Modified      | 未修改。所请求的资源未修改，服务器返回此状态码时，不会返回任何资源(响应消息中不包含响应体)。客户端通常会缓存访问过的资源 |

3. 4**客户端错误相关的响应状态码

   4** 范围的状态码，表示客户端的请求有非法内容，从而导致这次请求的失败。常见的 4** 类型的状态码如下：

   | 状态码  | 状态码英文名称  | 中文描述                                                     |
   | ------- | --------------- | ------------------------------------------------------------ |
   | 400     | Bad Request     | 1、客户端请求的语法有误，当前请求无法被服务器理解。除非进行修改，否则客户端不应该重复提交这个请求。2、请求参数有误。 |
   | 401     | Unauthorized    | 当前请求需要用户验证。                                       |
   | 403     | Forbidden       | 服务器已经理解请求，但是拒绝执行它。                         |
   | **404** | **Not Found**   | **服务器无法根据客户端的请求找到资源(网页)。**               |
   | 408     | Request Timeout | 请求超时。服务器等待客户端发送的请求时间过长，超时。         |

4. 5** 服务端错误相关的响应状态码

   5** 范围的状态码，表示服务器未能正常处理客户端的请求而出现意外错误。常见的5** 类型的状态码如下：

   | 状态码 | 状态码英文名称        | 中文描述                                                     |
   | ------ | --------------------- | ------------------------------------------------------------ |
   | 500    | Internal Server Error | 服务器内部错误，无法完成请求。                               |
   | 501    | Not Implemented       | 服务器不支持该请求方法，无法完成请求。只有GET和HEAD请求方式是要求每个服务器必须支持的，其他请求方法在不支持的服务器上会返回501 |
   | 503    | Service Unavaliable   | 由于超载或系统维护，服务器暂时的无法处理客户端的请求         |

**HTTP缓存**

- 什么是缓存

  缓存是一种保存资源副本并在下次请求时直接使用该副本的技术。

- 为什么需要缓存

  如果没有缓存的话，每一次网络请求都要加载大量的图片和资源，这会使页面的加载变慢许多。那缓存的目的其实就是为了减少网络请求的体积和数量，让页面加载的更快。

- 哪些资源可以被缓存？——静态资源（js，css，img）

  注：（1）网站的html是不能被缓存的。因为网站在使用过程中html随时有可能被更新，随时有可能被替换模板。（2）网页的业务数据也是不能被缓存的。比如留言板和评论区，用户随时都可以在底下评论，那么数据库的内容就会频繁被更新。

**HTTP缓存策略（强制缓存+协商缓存）**

- 强制缓存：文件直接从本地缓存中获取，不需要发送请求

- 强制缓存的过程：

  （1）当初次请求时，浏览器会向服务器发起请求，服务器接收到浏览器的请求后，返回资源并返回一个cache-Control给客户端，该cache-Control一般设置缓存的最大过期时间。

  （2）当浏览器接收到cache-Control的值之后再次发起请求时，它会先检查它的cache-Control是否过期，如果没有过期则直接从本地缓存中拉取资源，返回到客户端，而无需再经过服务器。

  （3）强制缓存有过期时间，如果客户端的cache-Control失效了，那么它就没办法从本地缓存中拉取资源。于是会重新向服务器发起请求，之后服务器会再次返回资源和cache-Control的值。

- cache-Control是什么

  cache-Control存在于响应头Response Headers中，控制强缓存的逻辑，例如cache-Control：max-age=31536000（单位是秒）

- cache-Control的值

  | cache-Control | 含义                                                       |
  | ------------- | ---------------------------------------------------------- |
  | max-age       | 设置缓存的最大过期时间                                     |
  | no-cache      | 不用本地缓存，正常的向服务器请求，服务端怎么处理我们不用管 |
  | no-store      | 简单粗暴，直接从服务端拉取缓存                             |
  | private       | 只能允许最终用户做缓存，最终用户即电脑、手机等等           |
  | public        | 允许中间路由或中间代理做缓存                               |

- Expires

  Expires也在Response Headers中，控制缓存的过期时间（早期使用），如果cache-Control与expires同时存在的话，cache-Control的优先级高于expires。

- 协商缓存：也叫对比缓存，它是一种服务器的缓存策略，即通过服务端来判断某件事情是不是可以被缓存。服务端判断客户端的资源，是否和服务端的资源一样，如果一致则返回304，反之返回200和最新的资源。

- 协商缓存的过程：

  （1）如果浏览器是第一次向服务器发起请求，则服务器返回资源和相对应的资源标识给浏览器。该资源标识就是对当前所返回资源的一种唯一标识，可以是Etag或是Last-Modified。

  （2）之后浏览器再次发送请求时，浏览器就会带上这个资源标识。此时，服务端就会通过这个资源标识，可以判断出浏览器的资源跟服务端此时的资源是否一致，如果一致，就返回304，即表示Not Found资源未修改。如果判断结果为不一致，则返回200，并返回资源以及新的资源标识。

- 资源标识

  在响应头部Request Headers中，有两种资源标识：

  （1）Last-Modified：资源的最后修改时间，对应请求头为If-Modified-Since；（2）Etag资源的唯一标识，所以唯一，可以想象成人类的指纹，具有唯一性；但Etag的本质是一个字符串；对应请求头If-None-Match。（3）当响应头部Response Headers同时存在Last-Modified和Etag的值时，会优先使用Etag；（4）如果资源被重复生成，而内容不变，则Etag更精确。

- HTTP缓存流程图

  <img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1662270927707.png" alt="1662270927707" style="zoom:50%;" />

- 刷新操作方式对缓存的影响

  （1）正常操作：地址栏输入url，跳转链接，前进后退等。

  对缓存的影响：强制缓存有效，协商缓存有效。

  （2）手动刷新：F5，点击刷新按钮，右击菜单刷新

**什么是HTTP协议无状态协议？怎么解决HTTP协议无状态协议**

HTTP协议是一种无状态协议，即每次服务端接收到客户端的请求时，都是一个全新的请求，服务器并不知道客户端的请求记录；Session和Cookie的主要目的就是为了弥补HTTP的无状态特性。除了session和cookie，还有JSON Web Token，都可以为网站提供用户的身份认证。它们既可以对用户进行身份验证，也可以用来在用户单击进入不同页面时以及登录网站或应用程序进行身份验证。

- Session是什么

  客户端请求服务器，服务器会为这次请求开辟一块内存空间，这个对象便是Session对象，服务器可以利用Session存储客户端在同一个会话期间的一些操作记录。

- 创建Session

  服务器第一次接收到请求时，开辟了一块Session空间（创建了Session对象），同时生成一个sessionId，并通过响应头的Set-Cookie：JSESSIONID=XXXXXX的命令，向客户端发送要求设置Cookie的响应；客户端收到响应后，在本机客户端设置了一个JSESSIONID=XXXXXX的Cookie信息，该Cookie的过期时间为浏览器会话结束。接下来客户端每次向同一个网站发送请求时，请求头都会带上该Cookie信息（包含sessionId），然后，服务器通过读取请求头中的Cookie信息，获取名称为JSESSIONID的值，得到此次请求的sessionId。

- Cookie是什么

  Cookie包括Web Cookie和浏览器Cookie，它是服务器发送到Web浏览器的一小块数据。服务器发送到浏览器的Cookie，浏览器会进行存储，并与下一个请求一起发送到服务器。通常，它用于判断两个请求是否来自于同一个浏览器，例如用户保持登录状态。

- 创建Cookie

  当接收到客户端发出的HTTP请求时，服务器可以发送带有响应的Set-Cookie标头，Cookie通常由浏览器存储，然后将Cookie与HTTP标头一同向服务器发出请求。

- Cookies的类型

  有两种类型的Cookies，一种是session Cookie，一种是Persistent Cookies，如果Cookie不包含到期日期，则将其视为会话Cookie。会话Cookie存储在内存中，永远不会写入磁盘，当浏览器关闭时，此后Cookie将永久丢失。如果Cookie包含有效期，则将其视为持久性Cookie。在指定的日期时，Cookie将从磁盘中删除。

- Token是什么

  Token，令牌，代表执行某些操作的权利的对象。简单来说，就是类似Cookie的一种验证信息，客户端通过登录验证后，服务器会返回给客户端一个加密的token，然后当客户端再次向服务器发起连接时，带上token，服务器直接对token进行验证即可完成权限校验。（token需要自己使用localStorage或sessionStorage进行存储，没有内存限制，自己进行发送，不存在跨域限制，因此Token相比于Cookie更加灵活）

**HTTP协议各个版本的比较**

**HTTP缺点**

- 通信使用明文（不加密），内容可能被窃听
- 不验证通信方的身份，因此可能遭遇伪装
- 无法证明报文的完整性，所以可能已经被篡改

## HTTPS协议

**什么是HTTPS协议**

超文本传输安全协议（Hyper Text Transfer Protocol Secure），是一种通过计算机网络进行安全通信的传输协议。（HTTPS是在HTTP上建立SSL加密层，并对传输数据进行加密，是HTTP协议的安全版）

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1663233568973.png" alt="1663233568973" style="zoom:50%;" />

HTTPS比HTTP多了一层TLS/SSL协议，TLS/SSL全称安全传输协议，是介于TCP和HTTP之间的一层安全协议，不影响原有的TCP协议和HTTP协议，所以使用HTTPS基本上不需要对HTTP页面进行太多的改造。

**HTTPS开发的主要目的**

是提供对网站服务器的身份认证，保护交换数据的隐私与完整性。

**HTTPS原理**

- 客户端向服务器索要并验证公钥。这一阶段使用的是非对称加密传输（RSA），服务端将数字证书发给客户端，其中数字证书包括：公钥和数字签名，客户端在拿到后对两者进行校验。
- 在非对称加密传输中，两端协商生成“对话密钥”。
- 双方采用“对话密钥”进行对称加密通信。

**HTTP与HTTPS的区别**

- HTTP是明文传输，HTTPS通过SSL/TLS进行了加密
- HTTP的端口是80，HTTPS的端口是443
- HTTPS需要CA申请证书，一般免费证书很少，需要交费
- HTTP的连接很简单，是无状态的；HTTPS协议是由SSL+HTTP协议构建的可进行加密传输、身份认证的网络协议，比HTTP协议安全

## 从浏览器地址栏输入url到显示页面的步骤

（1）浏览器中输入网址

- http或https
- url
  - URL（全称是UniformResourceLocator）中文叫统一资源定位符，用于标识互联网上每个资源的唯一存放位置。浏览器只有通过URL地址，才能正确定位资源的存放位置，从而成功访问到对应的资源。
  - URL的组成：protocol协议、host主机域名或IP地址、port端口号、path目录路径、query查询参数、fragment #后的hash值，一般用来定位到某个位置

（2）通过DNS解析域名的实际IP地址

- 将域名发送至DNS服务器并获得域名对应的WEB服务器的ip地址
  - DNS解析首先会从 **浏览器 -> 系统 -> 路由器 -> ISP 的DNS缓存**中寻找，如果在某一个缓存中找到，就直接跳到下一步，如果以上缓存中都没有找到就向**ISP或者公共的域名解析服务器发起DNS查找请求**。

（3）检查浏览器是否有缓存

- 检查是否命中强缓存
  - 浏览器通过Cache-Control和Expires来检查是否命中强缓存，命中则直接从本地缓存中拉取资源。
- 如果没有命中强缓存，则向服务器发起请求，检查是否命中协商缓存
  - 服务器通过Etag和Last-Modify来检查资源是否被修改，若未修改，命中协商缓存则浏览器直接从本地缓存中拉取资源。
- 如果强缓存和协商缓存都没有命中则返回请求结果

（4）根据IP，与对应的WEB服务器建立TCP连接，发起TCP三次握手

- TCP协议通过三次握手建立连接
  - 客户端发送SYN包到服务器，并进入SYN_SEND状态，等待服务器确认;
  - 服务器收到SYN包，必须确认客户的SYN（ACK=ACK+1），同时自己也发送一个SYN+ACK包给客户端，此时服务器进入SYN_RECV状态；
  - 客户端收到服务器的SYN+ACK包，向服务器发送ACK，此包发送完毕，客户端和服务器进入ESTABLISHED状态，完成三次握手。

（5）浏览器发送HTTP/HTTPS请求

- 浏览器向WEB服务器的ip地址发送相应的请求获取页面html

（6）服务器响应HTTP/HTTPS请求

（7）浏览器渲染页面(浏览器关键渲染路径)

- 浏览器解析HTML，构建DOM树
- 解析CSS，构建CSS规则树
- 构建渲染树（不可见的DOM元素不会插入到渲染树中）
- 布局，计算DOM树中可见元素的确切位置和大小
- 绘制，将渲染树中的每个节点转换成屏幕上的实际像素

（8）浏览器解析执行js脚本

- DOM操作以及ajax发起http网络请求等

（9）浏览器发起网络请求

- 获取数据

（10）服务器响应ajax请求

（11）浏览器处理事件循环等异步逻辑

（12）HTTP请求结束，断开TCP连接

- 现在的页面为了优化请求的耗时，默认都会开启持久连接(keep-alive)，那么一个TCP连接确切关闭的时机，是这个tab标签页关闭的时候。这个关闭的过程就是四次挥手。
  - 主动关闭方发送一个FIN，用来关闭主动方到被动关闭方的数据传送,但此时主动关闭方还可以接受数据；
  - 被动关闭方收到FIN包后，发送一个ACK给对方，确认序号为收到序号+1（与SYN相同，一个FIN占用一个序号）
  - 被动关闭方发送一个FIN，用来关闭被动关闭方到主动关闭方的数据传送；（也就是告诉主动关闭方，我的数据也发送完了，不会再给你发数据了）
  - 主动关闭方收到FIN后，发送一个ACK给被动关闭方，确认序号为收到序号+1，至此完成四次挥手。

## **跨域**

因为浏览器处于安全考虑，有同源策略。也就是说，如果两个URL的协议、域名或者端口有一个不同就是跨域。Ajax请求会失败。

**解决跨域的方式**

方式一：JSONP

优点：使用简单，兼容性不错

缺点：只限于使用get请求；只可以用于传递数据无法进行DOM查询；需要后端配合

 JSONP 的原理很简单，就是利用script `` 标签没有跨域限制的漏洞。通过 `` script标签指向一个需要访问的地址并提供一个回调函数来接收数据当需要通讯时。 

```html
<script src="http://domain/api?param1=a&param2=b&callback=jsonp"></script>
<script>
    function jsonp(data) {
    	console.log(data)
	}
</script>  
```

封装一个JSONP

```js
function jsonp(url, jsonpCallback, success) {
  let script = document.createElement('script')
  script.src = url
  script.async = true
  script.type = 'text/javascript'
  window[jsonpCallback] = function(data) {
    success && success(data)
  }
  document.body.appendChild(script)
}
jsonp('http://xxx', 'callback', function(value) {
  console.log(value)
})
```

方式二：CORS

优点：支持所有请求方式；可以进行DOM查询

缺点：早期的浏览器不支持；需要后端配合

CORS需要浏览器和后端同时支持，IE 8 和 9需要通过XDomainRequest来实现。浏览器会自动进行CORS通信，实现CORS通信的关键是后端。只要后端实现了CORS，就实现了跨域。

方式三：document.domain

优点：操作简单，支持DOM查询

缺点：只适用于相同主域的子域之间进行跨域

该方式只能用于二级域名相同的情况下，比如a.test.com和b.test.com适用于该方式。只需要给页面添加document.domain = ‘test.com’表示二级域名相同就可以实现跨域。

方式四：postMessage

优点：使用简单

缺点：早期浏览器不支持

 这种方式通常用于获取嵌入页面中的第三方页面数据。一个页面发送消息，另一个页面判断来源并接收消息（通过onmessage的监听来接收数据）

```js
// 发送消息端
window.parent.postMessage('message', 'http://test.com')
// 接收消息端
var mc = new MessageChannel()
mc.addEventListener('message', event => {
  var origin = event.origin || event.originalEvent.origin
  if (origin === 'http://test.com') {
    console.log('验证通过')
  }
})
```

方式五：使用iframe配合window自带的name属性

优点：操作简单，不要求后端配合

缺点：name的大小有限制，一般是2M左右

## 存储

有几种方式可以实现存储功能，区别是什么

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1660813279402.png" alt="1660813279402" style="zoom:80%;" />

 从上表可以看到，`cookie` 已经不建议用于存储。如果没有大量数据存储需求的话，可以使用 `localStorage` 和 `sessionStorage` 。对于不怎么改变的数据尽量使用 `localStorage` 存储，否则可以用 `sessionStorage` 存储。 

**DOM和BOM**

DOM：                                                                           BOM                                            

​			文档对象模型                                                               浏览器对象模型

​			DOM就是把文档当做一个对象来看待                       把浏览器当做一个对象来看待

​			DOM的顶级对象是document                                    BOM的顶级对象是window

​			DOM主要学习的是操作页面元素                               BOM学习的是浏览器窗口交互的一些对象

​			DOM是W3C标准规范                                                  BOM是浏览器厂商在各自浏览器上定义的，兼容性较差

## 多页签通讯

方法一：localstorage在一个标签页里被添加、修改或删除时，都会触发一个storage事件，通过在另一个标签页里监听storage事件，即可得到localstorage存储的值，实现不同签页之间的通信。

方法二：使用cookie+setInterval，将要传递的信息存储在cookie中，每隔一定时间读取cookie信息，即可随时获取要传递的信息。

# Vue

定义：动态构建用户界面的渐进式JavaScript框架

特点：代码简洁，体积小，运行效率高，适合移动/PC端开发

## MVVM

**定义**

MVVM是一种简化用户界面的事件驱动编程方式，是Model-View-ViewModel的简写，即模型-视图-视图模型。模型指的是后端传递的数据。视图指的是所看到的页面。视图模型是MVVM模式的核心，它是连接view和model的桥梁。我们称之为数据的双向绑定，MVVM框架自动更新DOM状态，开发者只需要关心model的变化。

M：模型(Model)：data中的数据

V：视图(View)：模板代码

VM：视图模型(ViewModel)：Vue实例对象

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1661066798947.png" alt="1661066798947" style="zoom:50%;" />

**MVC的定义**

MVC是Model-View-Controller的简写，即模型-视图-控制器。M和V分别指模型和视图，C指的是页面业务逻辑。使用MVC的目的就是将M和V的代码分离。MVC是单向通信。

**与MVC的区别**

MVC和MVVM都是一种设计思想，MVC中Controller演变成MVVM中的viewModel，MVVM主要解决了MVC中大量的DOM操作使页面渲染性能降低，加载速度变慢，影响用户体验。Vue数据驱动，通过数据来显示视图层而不是节点操作。

**场景**

数据操作比较多的场景，需要大量操作DOM元素时，采用MVVM的开发方式，会更加便捷，让开发者更多的精力放在数据的变化上，解放繁琐的操作DOM元素。

**JS在浏览器中操作HTML**

- 第一阶段：直接用JS操作DOM节点，使用浏览器提供的原生API

  ```js
  var dom = document.getElementById('name');
  dom.innerHTML = 'Homer';
  dom.style.color = 'red';
  ```

- 第二阶段：jQuery

  ```js
  $('#name').text('Homer').css('color','red');
  ```

- 第三阶段：MVC模式，需要服务器端配合，JS可以在前端修改服务器渲染后的数据

- 第四阶段：MVVM

  MVVM最早由微软提出来，它借鉴了桌面应用程序的MVC思想，在前端页 面中，把Model用纯JavaScript对象表示，View负责显示，两者做到了最大限度的分离。把 Model和View关联起来的就是ViewModel。ViewModel负责把Model的数据同步到View显示出 来，还负责把View的修改同步回Model。MVVM的核心是 viewModle, 负责转换 Model中的数据对象来让数据变得更容易管理和使用，该层向上与视图层进行双向数据绑定，向下与 Model 层通过接口请求进行数据交互，起呈上启下作用

**Vue中的数据（劫持）代理**

定义：通过vm对象来代理data对象中属性的操作

好处：更加方便的操作data中的数据

原理：

（1）通过Object.defineProperty()把data对象中所有属性添加到vm上

（2）为每一个添加到vm上的属性，都指定一个getter/setter

（3）在getter/setter内部去操作(读/写)data中对应的属性

结论：

（1）data中所有的属性，最后都出现在了vm身上

（2）vm身上所有的属性及Vue原型上所有属性，在Vue模板中都可以直接使用

**Vue的双向绑定原理**

Vue数据双向绑定原理是通过数据劫持+发布者-订阅者模式的方式来实现的，首先是通过es5提供的Object.defineProperty()方法来劫持（监听）各属性的getter和setter，并在当监听的属性发生变动时通知订阅者，是否需要更新，若更新就会执行对应的更新函数。

**数据绑定**

- 单向绑定：v-bind，数据只能从data流向页面

- 双向绑定：v-model：数据不仅能从data流向页面，还可以从页面流向data

  注意：

  （1）双向绑定一般都应用在表单类元素上（如input、select、单选多选，表单域等）

  （2）v-model:value可以简写为v-model

  （3）v-model的三个修饰符：（a）lazy：失去焦点再收集数据（b）number：输入字符串转为有效的数字                                                       （c）trim：输入首尾空格过滤
  
- v-model的底层实现原理分析

  ```html
  <input v-bind:value="msg" v-on:input="msg=$event.target.value">
  ```

  （1）v-bind绑定一个value属性

  （2）v-on给当前元素绑定input事件，从而更新数据

  

**Vue监视数据的原理**

1. vue会监视data中所有层次的数据。

   2. 如何监测对象中的数据？

​       通过setter实现监视，且要在new Vue时就传入要监测的数据。

​           (1).对象中后追加的属性，Vue默认不做响应式处理

​           (2).如需给后添加的属性做响应式，请使用如下API：

​            Vue.set(target，propertyName/index，value) 或 

​            vm.$set(target，propertyName/index，value)

   3. 如何监测数组中的数据？

​           通过包裹数组更新元素的方法实现，本质就是做了两件事：

​           (1).调用原生对应的方法对数组进行更新。

​           (2).重新解析模板，进而更新页面。

   4.在Vue修改数组中的某个元素一定要用如下方法：

​       1.使用这些API:push()、pop()、shift()、unshift()、splice()、sort()、reverse()

​       2.Vue.set() 或 vm.$set()

​    特别注意：Vue.set() 和 vm.$set() 不能给vm 或 vm的根数据对象 添加属性！！！

**Vue中的data为什么是一个函数**

data两种不同的类型有什么区别：

- 当我们组件中的data写成一个函数时，数据是以函数返回值形式定义的，这样每复用一次data，都会返回一份新的data，拥有自己的作用域，不会产生数据污染。
- 当我们组件中的data写成一个对象时，对象是引用数据类型，它就会共用一个内存地址，在多次使用该组件时，改变其中一个组件的值会影响全部使用该组件的值。

**理解data为什么必须是一个函数**

在vue中一个组件可能会被其他的组件引用，为了防止多个组件实例对象之间共用一个data，产生数据污染。将data定义成一个函数，每个组件实例都有自己的作用域，每个实例对象相互独立，不会相互影响。

## 虚拟DOM

**什么是虚拟DOM**

Vue.js通过编译将模板转换成渲染函数，执行渲染函数就可以得到一个以对象作为基础的树形结构，包含tag，props，children等属性，这个树形结构就是虚拟DOM。

**操作DOM的几种方式**

- 通过原生js

  ```js
  // 获取要操作的DOM节点
  const div = document.getElementById('div');
  // 对其进行相应的操作
  div.innerText = 'hello world';
  ```

- 通过一个html模板字符串创建一个节点，替换当前节点(这种方式在jQuery时代非常常用)

  ```js
  const htmlTemplate = `<div>hello world</div>`
  wrap.innerHTML = htmlTemplate
  ```

- 通过虚拟DOM

  ```js
  const virtualDOM = {
      tag: 'div',
      children: [{children: 'hello world'}]
  }
  // render函数将虚拟DOM创建为真实DOM，并将其插入到文档中
  render(virtualDOM)
  ```

**为什么选用虚拟DOM**

（1）一个DOM节点是很庞大的，它有很多属性，每次操作DOM是一个相当耗时的过程

（2）当更新一个DOM节点的时候，很有可能会触发重排操作，导致浏览器会重新渲染部分或全部文档

（3）当对多个DOM进行更新的时候，每一次都要重新计算节点的坐标信息，会造成性能的浪费

（4）虚拟DOM很好的解决了上述问题，当执行更新大量节点操作时，可以通过虚拟DOM找出最小的变化，然后再把这些改动写入实际的DOM中，虚拟DOM减少了实际操作DOM的次数，有利用提升性能

**什么是Diff算法**

将新生成的虚拟节点树与旧的虚拟节点树对比的过程，就是Diff算法

**什么是patch算法**

将vnode渲染成真实的DOM，这个过程是对比新旧虚拟节点之间有哪些不同，然后根据对比结果找出需要更新的节点进行更新

## Vue中的key有什么作用(key的内部原理)

- 虚拟DOM中key的作用

  key是虚拟DOM对象的标识，当数据发生变化时，Vue会根据【新数据】生成【新的虚拟DOM】, 随后Vue进行【新虚拟DOM】与【旧虚拟DOM】的差异比较，比较规则如下：

- 对比规则

  (1).旧虚拟DOM中找到了与新虚拟DOM相同的key：

  ​            ①.若虚拟DOM中内容没变, 直接使用之前的真实DOM！

  ​            ②.若虚拟DOM中内容变了, 则生成新的真实DOM，随后替换掉页面中之前的真实DOM。

   (2).旧虚拟DOM中未找到与新虚拟DOM相同的key

  ​       创建新的真实DOM，随后渲染到到页面。

- 用index作为key可能会引发的问题

  1. 若对数据进行：逆序添加、逆序删除等破坏顺序操作:

  ​       会产生没有必要的真实DOM更新 ==> 界面效果没问题, 但效率低。

  2. 如果结构中还包含输入类的DOM：

  ​       会产生错误DOM更新 ==> 界面有问题。

- 开发中如何选择key(key不写的话默认为index)

  1.最好使用每条数据的唯一标识作为key, 比如id、手机号、身份证号、学号等唯一值。

  2.如果不存在对数据的逆序添加、逆序删除等破坏顺序操作，仅用于渲染列表用于展示，使用index作为key是没有问题的。

## Computed/Watch

计算属性computed

- 支持缓存，只有依赖数据发生变化，才会重新计算
- 不支持异步，当computed内有异步操作时无效，无法监听数据的变化
- 如果一个属性是由其他属性计算而来的，这个属性依赖其他属性，是一个多对一或者一对一，一般用computed

侦听属性watch

- 不支持缓存，数据变，直接会触发相应的操作
- 支持异步
- 当一个属性发生变化时，需要执行对应的操作；一对多
- 监听数据必须是data中声明过或者父组件传递过来的props中的数据

区别：

（1）computed能完成的功能，watch都可以完成

（2）watch能完成的功能，computed不一定能完成，例如：watch可以进行异步操作

## $nextTick

nextTick是在下次DOM更新循环结束之后执行延迟回调，在修改数据之后使用nextTick，则可以在回调中获取更新后的DOM。

## computed和methods

computed访问的时候会直接返回已缓存的结果，而不会像methods一样再次计算

## 条件渲染v-if/v-show

- v-if

  写法：

  ​		（1）v-if = “表达式”

  ​		（2）v-else-if = “表达式”

  ​		（3）v-else = “表达式”

  场景：切换频率较低的场景，与template标签配合使用，控制多个标签的显示与隐藏

  特点：不展示的DOM元素直接被移除

  注意：v-if可以和v-else-if、v-else一起使用，但要求结构不能被“打断”

- v-show

  写法：v-show=“表达式”

  场景：切换频率较高的场景

  特点：不展示的DOM元素未被移除，仅仅是使用样式隐藏

注意：使用v-if时，元素可能无法获取到，而使用v-show一定可以获取到

## v-for和v-if的优先级

当v-if与v-for一起使用时，v-for具有比v-if更高的优先级，每v-for循环一次都要进行v-if判断，影响性能。

解决方案：（1）在外层嵌套template，在这里进行v-if判断，然后内部进行v-for循环 （2）如果条件出现在循环内部，可以通过计算属性提前过滤掉那些不需要显示的项

## vue常见的修饰符

- .stop：阻止单击事件冒泡
- .prevent：阻止事件的默认行为
- .self：当事件发生在该元素本身而不是子元素的时候会触发
- .once：只渲染一次，第二次不会执行

## keep-alive的作用是什么

keep-alive用来缓存组件，避免多次加载响应组件，减少性能消耗。简单来说，就是页面1跳转到页面2，再退回到页面1，这时候不用重新执行页面1的代码，只会从缓存中加载之前已经缓存的页面1，这样可以减少加载时间及性能消耗。比如：当需要频繁切换路由时，可以使用keep-alive来达到避免重复请求数据的目的。

## vue中如何获取DOM

利用vue提供的API，在DOM标签属性上加一个ref=“domName”，然后通过vue实例的this.$refs.domName来直接获取这个元素的节点。

## Vue.set/this.$set

如果在实例创建之后添加新的属性到实例上，它不会触发视图更新。可以使用Vue.set(target,key,value)方法向嵌套对象添加响应式属性。Vue.set()和this.$set()这两个api的实现原理一模一样，都是使用了set函数。区别就在于Vue.set()是将set函数绑定在Vue构造函数上，this.$set()是将set函数绑定在Vue原型上。

## 组件间的通信

**父组件向子组件传递数据**

```js
// 父组件
<child value = '传递数据' />
// 子组件
// 第一种方式：只接收
props: ['value']
// 第二种方式：限制接收数据的类型
props: {value: String}
// 第三种方式：限制类型、限制必要性、指定默认值
props: {
    value: {
        type: String,
        required: true,
        default: 'offer' // 默认值
    }
}
```

**注意**：props是只读的，Vue底层会监测你对props的修改，如果进行了修改，就会发出警告，若业务需求确实需要修改，那么请复制props的内容到data中一份，然后去修改data中的数据。

**插槽(父组件向子组件指定位置插入html结构)**

**子组件向父组件传递数据**

```js
// 在父组件中给子组件绑定一个自定义事件
// 第一种方式
<Demo @atguigu="test" /> 
<Demo v-on:atguigu="test" />
// 第二种方式
<Demo ref="demo">
mounted() {
    this.$refs.demo.$on('atguigu',this.test)
}
// 子组件通过$emit()触发该事件并传值
this.$emit('atguigu','传递的数据')
```

**全局事件总线(适用于任意组件间通信)**

```js
// A组件要接收数据，则在A组件中给$bus绑定自定义事件，事件的回调留在A组件自身
methods() {
    demo(data) {
        ......
    }
}
mounted() {
    this.$bus.$on('xxx',this.demo)
}
// B组件提供数据，则在B组件中通过$emit()触发该事件并传值
this.$bus.$emit('xxx','传递的数据')
```

**消息订阅与发布(适用于任意组件间通信)**

```js
// A组件要接收数据，则在A组件中订阅消息，订阅的回调留在A组件自身
methods() {
    demo(data) {
        ......
    }
}
mounted() {
    this.pId = pubsub.subscribe('xxx',this.demo) // 订阅消息
}
// B组件提供数据
pubsub.publish('xxx','数据')
```

**Vuex(适用于任意组件间通信)**

**Vuex是什么**

Vuex是官方提供的一个插件，状态管理库，可以集中式管理项目中组件的共用数据。vuex就是一个数据仓库，将项目中共用的数据放入仓库中，哪个组件需要共用的数据就从仓库中要。

**书写任何项目都需要vuex吗**

并不是全部项目都需要vuex，如果项目很小，完全不需要vuex；项目大的时候，组件很多，数据很多，数据维护比较费劲，这就需要有一个地方‘统一管理数据’即为仓库store。

**vuex的基本使用**

（1）安装vuex：npm install --save vuex

（2）配置仓库vuex

在src目录下新建一个文件夹store/index.js；

引入插件import Vue from ‘vue’,import Vuex from ‘vuex’

使用插件Vue.use(Vuex)

对外暴露一个Store类的实例

```js
export default new Vuex.store({
state: {}; // 仓库存储数据的地方
mutations: {}; // 修改state中数据的唯一手段
actions: {}; // 处理action，可以书写自己的业务逻辑，也可书写异步任务
getters: {}; // 理解为计算属性，简化仓库数据，让组件更方便的获取数据
modules: {}; // 实现vuex仓库模块式开发存储数据
})
```

（3）在main.js中引入仓库

```js
import store from '@/store'
```

（4）注册仓库

```js
// 当仓库组件注册后，组件实例身上会多一个属性$store
new Vue({
    		reder: h=>h(App), 
    		router, 
    		store
		}).$mount(‘#app’)
```

（5）具体使用

```js
// 在Home模块有一个计数器，点击加1
//（Home组件index.vue）
<template>
<button @click=”add”>点击加1</button>
<span>仓库的数据{{count}}</span>  // 可以使用组件Home身上的count数据
</template>
<script>
import {mapState} from ‘vuex’
export default {
computed: {
...mapState([‘count’]); // 此时组件Home身上就有count数据
},
methods: {
add() {
// 派发action
this.$store.dispatch(‘add’)
}
}
}
</script>

// store仓库index.js
const state = {count: 1};
const mutations = {
ADD(state) {
state.count++;
}
}
const actions = {
// 可以书写业务逻辑，但是不能修改state
add({commit}) {
commit(“ADD”);
}
}
```

**vuex实现模块式开发**

如果项目过大，组件过多，接口也很多，数据也很多，可以让Vuex实现模块式开发

（1）在store文件夹中新建小仓库home，search，detail，user等等，每个小仓库只负责自己模块的数据，小仓库中新建index.js书写核心代码state，mutations，actions，getters，并暴露

```js
export default {state,mutations,actions,getters}
```

（2）将小仓库引入到大仓库

```js
// 在大仓库(store/index.js)中引入小仓库
import home from './home';
import search from './search'
```

（3）注册小仓库

```js
export default new Vuex.Store({
    modules: {
        home,
        search
    }
})
```

## 路由

**什么是vue-router**

Vue Router是Vue.js官方的路由管理器。它和Vue.js的核心深度集成，让构建单页面应用变得易如反掌。

**如何使用vue-router**

（1）安装vue-router：npm install --save vue-router

（2）配置路由

项目当中配置的路由一般放置在router文件夹中（新建router/index.js）

```js
import Vue from ‘vue’
import VueRouter from ‘vue-router’
Vue.use(VueRouter)
import Home from ‘@/pages/Home’
export default new VueRouter({
    routes: [
        {path: “/home”, components: “Home”},
     	{ }
    	]
})
```

（3）在main.js中引入路由

```js
import router from '@/router'
```

（4）在根组件中注册路由

```js
new Vue({
    		reder: h=>h(App), 
    		router
		}).$mount(‘#app’)
```

（5）展示路由组件

```js
// 书写在需要展示路由组件的位置，即路由出口
<Header></Header>
<router-view></router-view>
<Footer></Footer>
```

**route和router的区别**

$route一般用于获取当前路由组件信息【name、path、query、params】等

$router一般用于编程式导航进行路由跳转【push|replace】

## 生命周期

生命周期，又名生命周期回调函数、生命周期函数、生命周期钩子。生命周期是Vue在关键时刻帮我们调用的一些特殊名称的函数。生命周期的名字不可更改，但函数的具体内容是程序员根据需求编写的。生命周期函数中的this指向是vm或组件的实例对象。

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1662096941964.png" alt="1662096941964" style="zoom:50%;" />

## 其他

**注意事项**

（1）methods中配置的函数，不要用箭头函数！否则this就不是vm了

（2）methods中配置的函数，都是被Vue所管理的函数，this的指向是vm或组件实例对象

**绑定样式**

- class样式

  写法:class="xxx" xxx可以是字符串、对象、数组。

  ​         字符串写法适用于：类名不确定，要动态获取。

  ​          数组写法适用于：要绑定多个样式，个数不确定，名字也不确定。

  ​          对象写法适用于：要绑定多个样式，个数确定，名字也确定，但不确定用不用。

- style样式

  :style="{fontSize: xxx}"其中xxx是动态值。

  ​        :style="[a,b]"其中a、b是样式对象。

**v-for**

​		1.用于展示列表数据

​        2.语法：v-for="(item, index) in xxx" :key="yyy"

​        3.可遍历：数组、对象、字符串（用的很少）、指定次数（用的很少，注：次数从1开始）

# Node.js

## 常用模块

Node.js作为一个JavaScript的运行环境，提供了基础的功能和API，是一个渐进式框架：一个功能对应一个模块(js文件)，需要用的时候导入即可。

- 非渐进式框架：套餐，一次性导入所有的功能。无论是项目需要的还是不需要的(浪费资源)。
- 渐进式框架：自助餐，吃什么用什么，不浪费(节省资源)。

**内置模块**

- fs文件系统模块：用来操作文件的模块

  fs.readFile()方法，用来读取指定文件中的内容

  fs.writeFile()方法，用来向指定的文件中写入内容

- path路径模块：用来处理路径的模块

  path.join()方法，用来将路径片段拼接成一个完整的路径字符串

  path.basename()方法，用来从路径字符串中，将文件名解析出来

  path.extname()方法，可以获取路径中的扩展名部分

- http模块：用来创建服务器的模块

  ```js
  // 1 导入http模块
  const http = require('http');
  // 2 创建一个web服务器实例
  const server = http.createServer();
  // 3 为服务器绑定request事件，监听客户端的请求
  server.on('request',(req,res) => {
      console.log('Someone visit our web server')
  })
  // 4 启动服务器
  server.listen(80,() => {
      console.log('http server running at http://127.0.0.1')
  })
  ```

**自定义模块**

用户创建的每个js文件都是自定义模块

**第三方模块**

由第三方开发出来的模块，并非官方提供的内置模块，也不是用户创建的自定义模块，使用前需要下载。

## Node.js中的模块化规范

Node.js遵循了CommonJS模块化规范，CommonJS规定了模块的特性与各模块之间如何相互依赖。

**CommonJS规定：**

（1）每个模块内部，module变量代表当前模块

（2）module变量是一个对象，它的exports属性是对外的接口module.exports

（3）加载某个接口，其实是加载该模块的module.exports属性，require()方法用于加载模块

模块的加载机制

- 优先从缓存中加载

**模块在第一次加载后会被缓存**。这也意味着多次调用require()不会导致模块的代码被执行多次。

注意：不论是内置模块、用户自定义模块、还是第三方模块，它们都会优先从缓存中加载，从而**提高模块的加载效率**。

- 内置模块的加载机制

内置模块是由Node.js官方提供的模块，**内置模块的加载优先级最高**。

例如：require(‘fs’)始终返回内置的fs模块，即使在node_modules目录下有名字相同的包也叫做fs。

- 自定义模块的加载机制

使用 require() 加载自定义模块时，必须指定以 **./** 或 **../** 开头的**路径标识符**。在加载自定义模块时，如果没有指定 ./ 或 ../ 这样的路径标识符，则 node 会把它当作**内置模块**或**第三方模块**进行加载。

同时，在使用require()导入自定义模块时，如果省略了文件的扩展名，则Node.js会**按顺序**分别尝试加载以下的文件：

（1）按照**确切的文件名**进行加载

（2）补全**.js**扩展名进行加载

（3）补全**.json**扩展名进行加载

（4）补全**.node**扩展名进行加载

（5）加载失败，终端报错

- 第三方模块的加载机制

如果传递给 require() 的模块标识符不是一个内置模块，也没有以 ‘./’ 或 ‘../’ 开头，则 Node.js 会从当前模块的父目录开始，尝试从 /node_modules 文件夹中加载第三方模块。

**如果没有找到对应的第三方模块，则移动到再上一层父目录中，进行加载，直到文件系统的根目录。**

例如，假设在 'C:\Users\itheima\project\foo.js' 文件里调用了 require('tools')，则 Node.js 会按以下顺序查找：
 （1） C:\Users\itheima\project\node_modules\tools
 （2）C:\Users\itheima\node_modules\tools
 （3）C:\Users\node_modules\tools
 （4）C:\node_modules\tools

- 目录作为模块

当把目录作为模块标识符，传递给require()进行加载的时候，有三种加载方式：

（1）在被加载的目录下查找一个叫做 package.json 的文件，并寻找 main 属性，作为 require() 加载的入口
（2）如果目录里没有 package.json 文件，或者 main 入口不存在或无法解析，则 Node.js 将会试图加载目录下的 index.js 文件。
（3）如果以上两步都失败了，则 Node.js 会在终端打印错误消息，报告模块的缺失：Error: Cannot find module 'xxx'

## Epress实现服务端功能

Express是基于Node.js平台，快速、开放、极简的Web开发框架。专门用来创建服务器的。本质是npm上的第三方包。

**创建基本的Web服务器**

```js
// 1. 导入express
const express = require('express')
// 2. 创建 web 服务器
const app = express()
// 挂载路由
app.get('/user',(req,res)=>{
    // 向客户端发送JSON对象
    res.send({name: 'zs', age: 20, gender: '男'})
})
app.post('/user',(req,res)=>{
    // 向客户端发送文本内容
    res.send('请求成功')
})
// 3. 调用app.listen(端口号，启动成功后的回调函数)，启动服务器
app.listen(80, () => {
    console.log('express server running at http://127.0.0.1')
})
```

**模块化路由**

将路由抽离为单独模块的步骤如下：

（1）创建路由模块对应的.js文件

（2）调用express.Router()函数创建路由对象

（3）向路由对象上挂载具体的路由

（4）使用module.exports向外共享路由对象

```js
var express = require('express')  // 1. 导入express
var router = express.Router()     // 2. 创建路由对象

router.get('/user/list',function(req,res) {
    // 3. 挂载获取用户列表的路由
    res.send('Get user list.')
})
router.post('/user/add',function(req,res) {
    // 4. 挂载添加用户的路由
    res.send('Add new user.')
})
module.exports=router             // 5. 向外导出路由对象
```

（5）使用app.use()函数注册路由模块

```js
// 1. 导入路由模块
const userRouter = require('./router/user.js')

// 2. 使用app.use()注册路由模块
app.use(userRouter)
```

**使用Express写接口**

- 创建基本的服务器

  ```js
  // 导入express模块
  const express = require('express')
  // 创建express的服务器实例
  const app = express()
  
  // write your code here...
  
  // 调用app.listen方法，指定端口号并启动web服务器
  app.listen(80,function() {
      console.log('Express server running at http://127.0.0.1')
  })
  ```

- 创建API路由模块

  ```js
  // apiRouter.js 【路由模块】
  const express = require('express')
  const apiRouter = express.Router()
  
  // bind your router here
  
  module.exports = apiRouter
  
  // --------------------
  
  // app.js【导入并注册路由模块】
  const apiRouter = require('./apiRouter.js')
  app.use('/api',apiRouter)
  ```

- 编写GET接口

  ```js
  apiRouter.get('/get',(req,res)=>{
      // 1. 获取到客户端通过查询字符串，发送到服务器的数据
      const query = req.query
      // 2. 调用res.send()方法，把数据响应给客户端
      res.send({
          status: 0,           // 状态，0表示成功，1表示失败
          msg: 'GET请求成功！',  // 状态描述
          data: query          // 需要响应给客户端的具体数据
      })
  })
  ```

- 编写POST接口

  ```js
  apiRouter.post('/post',(req,res)=>{
      // 1. 获取到客户端通过查询字符串，发送到服务器的数据
      const body = req.body
      // 2. 调用res.send()方法，把数据响应给客户端
      res.send({
          status: 0,            // 状态，0表示成功，1表示失败
          msg: 'POST请求成功！',  // 状态描述
          data: body            // 需要响应给客户端的具体数据
      })
  })
  ```

  **使用cors中间件解决跨域问题**
  
  cors是Express的一个第三方中间件。通过安装和配置cors中间件，可以很方便地解决跨域问题。
  
  使用步骤分为如下3步：
  
  （1）运行 npm install cors 安装中间件
  
  （2）使用const cors = require(‘cors’) 导入中间件
  
  （3）在路由之前**调用 app.use(cors())** 配置中间件
  
  注意：CORS主要在**服务器端**进行配置。客户端浏览器**无须做任何额外的配置**，即可请求开启了CORS的接口。

# Ajax

**什么是Ajax**

Ajax的全称是Asynchronous Javascript And XML（异步JavaScript和XML）。

通俗的理解：在网页中利用XMLHttpRequest对象和服务器进行数据交互的方式，就是Ajax。可以实现在不重新加载整个网页的情况下，与服务器交换数据，并更新部分网页。

**Ajax的基本步骤**

（1）创建XMLHttpRequest对象，也就是创建一个异步调用对象

（2）创建一个新的HTTP请求，并指定该HTTP请求的方法和URL

（3）设置响应HTTP请求状态变化的函数

（4）发送HTTP请求

（5）获取异步调用返回的数据

（6）使用JavaScript和DOM实现局部刷新

**原生Ajax使用XMLHttpRequest实现**

- 使用xhr发起GET请求

  步骤：

  （1）创建xhr对象

  （2）调用xhr.open()函数   来创建一个请求

  （3）调用xhr.send()函数    来发起这个请求

  （4）监听xhr.onreadystatechange事件    如果请求成功就可拿到服务器响应的数据

  ```js
  // 1. 创建 XHR 对象
  var xhr = new XMLHttpRequest();
  // 2. 调用open函数，指定请求方式与URL地址
  xhr.open('GET','http://liulongbin.top:3006/api/getbooks');
  // 3. 调用send函数，发起Ajax请求
  xhr.send();
  // 4. 监听onreadystatechange事件
  xhr.onreadystatechange = function() {
      // 4.1 监听xhr对象的请求状态readyState；与服务器响应的状态status
      if (xhr.readyState === 4 && xhr.status === 200) {
          // 4.2 打印服务器响应回来的数据
          console.log(xhr.responseText);
      }
  }
  ```

- 使用xhr发起POST请求

  步骤：

  （1）创建xhr对象

  （2）调用xhr.open()函数

  （3）**设置Content-Type属性**(固定写法)

  （4）调用xhr.send()函数，**同时指定要发送的数据**

  （5）监听xhr.onreadystatechange事件

  ```js
  // 1. 创建xhr对象
  var xhr = new XMLHttpRequest()
  // 2. 调用open()
  xhr.open('POST','http://www.liulongbin.top:3006/api/addbook')
  // 3. 设置 Content-type属性(固定写法)
  xhr.setRequestHeader('Content-Type','application/x-www-form-urlencoded')
  // 4. 调用send()，同时将数据以查询字符串的形式，提交给服务器
  xhr.send('bookname=水浒传$author=施耐庵$publisher=天津出版社')
  // 5. 监听 onreadystatechange 事件
  xhr.onreadystatechange = function() {
      if (xhr.readyState === 4 && xhr.status === 200) {
          console.log(xhr.responseText)
      }
  }
  ```

**二次封装Ajax**

```js
// 如何二次封装Ajax
// 在函数中获取配置对象的属性，设置method的默认值，对参数data进行整理，创建xhr实例化对象，并监听onreadystatechange事件，再根据请求方式决定如何携带参数
function sendAjax(options) {
      // 获取到配置对象的属性
      let { url, method, data, success, error } = options
      // 设置method默认值
      method = method ? method : 'get'
      // 实例化xhr
      let xhr = new XMLHttpRequest()
      // 绑定监听
      xhr.onreadystatechange = function () {
        if (xhr.readyState !== 4) return
        if (xhr.readyState >= 200 && xhr.readyState <= 299) {
          if (success) {
            success(xhr.response)
          } else {
            if (error) error('请求出错')
          }
        }
        // 整理参数
        let str = ''
        for (let key in data) {
          str += `${key}=${data[key]}`
        }
        // 根据请求方式决定如何携带参数
        if (method.toUpperCase() === 'GET') {
          xhr.open(method, url + '?' + str)
          xhr.send()
        } else {
          xhr.open(method, url)
          xhr.setRequestHeader('ContentType', 'application/x-www-form-urlencoded')
          // post要将参数的urlencoded传入send中
          xhr.send(str)
        }
        return xhr
      }
    }
```



# Git

**常用命令**

- git init：初始化仓库
- git status：检查文件状态
- git add：跟踪新文件
- git commit -m：提交更新
- git push：将本地代码提交到远程仓库
- git pull：取回远程主机的更新并且与现在开发的代码进行合并
- git bisect是利用二分法的思想，来查找哪一次代码提交引入了错误
- git stash暂存
- git rebase合并
- git fetch/clone远程端下载至本地

# HTTP协议

**什么是HTTP协议**

HTTP协议即超文本传送协议（Hyper Text Transfer Protocol），它规定了客户端与服务器之间进行网页内容传输时，所必须遵守的传输格式。

**HTTP原理**

（1）客户端的浏览器首先要通过网络与服务器建立连接，该连接是通过TCP来完成的，一般TCP连接的端口号是80。建立连接后，客户端发送一个请求给服务器。（2）服务器接收到请求后，给与相应的响应信息。

**HTTP协议交互模型**

HTTP协议采用了**请求/响应**的交互模型。

**HTTP请求消息**

客户端发起的请求叫做HTTP请求，客户端发送到服务器的消息，叫做请求消息。

**HTTP请求消息的组成部分**

- 请求行，请求行由请求方式、URI和HTTP协议版本3个部分组成，中间使用空格隔开

- 请求头部，用来描述客户端的基本信息，从而把客户端相关的信息告知服务器。

  <img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1661924730360.png" alt="1661924730360" style="zoom:50%;" />

- 空行，最后一个请求字段的后面是空行，通知服务器请求头部至此结束。请求消息中的空行，用来分隔请求头部和请求体

- 请求体，请求中存放的，是要通过post方式提交到服务器的数据

  注意：只要post请求才有请求体，get请求没有请求体

**HTTP响应消息**

响应消息就是服务器响应给客户端的消息内容，也叫作响应报文

**HTTP响应消息的组成部分**

- 状态行，由HTTP协议版本、状态码和状态码的描述文本3个部分组成，它们之间使用空格隔开
- 响应头部，用来描述服务器的基本信息
- 空行，在最后一个响应头字段结束之后，会紧跟一个空行，用来通知客户端响应头部至此结束，响应消息中的空行，用来分隔响应头部和响应体
- 响应体，响应体中存放的是服务器响应给客户端的资源内容

**HTTP的请求方法**

![1661926929334](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1661926929334.png)

**HTTP响应状态码**

HTTP响应状态码也属于HTTP协议的一部分，用来标识响应的状态。

**HTTP响应状态码的组成及分类**

HTTP状态码由三个十进制数字组成，第一个十进制数字定义了状态码的类型，后两个数组用来对状态码进行细分。

**HTTP状态码分为5种类型**

| 分类    | 分类描述                                                     |
| ------- | ------------------------------------------------------------ |
| 1**     | 信息，服务器收到请求，需要请求者继续执行操作(实际开发中很少遇到1**类型的状态码) |
| 2**     | **成功，操作被成功接收并处理**                               |
| **3**** | **重定向，需要进一步的操作以完成请求**                       |
| **4**** | **客户端错误，请求包含语法错误或无法完成请求**               |
| **5**** | **服务器错误，服务器在处理请求的过程中发生了错误**           |

1. 2**成功相关的响应状态码

   2** 范围的状态码，表示服务器已成功接收到请求并进行处理。常见的 2**类型的状态码如下：

   | 状态码 | 状态码英文名称 | 中文描述                                                |
   | ------ | -------------- | ------------------------------------------------------- |
   | 200    | OK             | 请求成功。一般用于GET与POST请求                         |
   | 201    | Created        | 已创建。成功请求并创建了新的资源，通常用于POST或PUT请求 |

2. 3**重定向相关的响应状态码

   3** 范围的状态码，表示服务器要求客户端重定向，需要客户端进一步的操作以完成资源的请求。常见的 3**类型的状态码如下：

   | 状态码 | 状态码英文描述    | 中文描述                                                     |
   | ------ | ----------------- | ------------------------------------------------------------ |
   | 301    | Moved Permanently | 永久移动。请求的资源已被永久移动到新的URI，返回信息会包括新的URI，浏览器会自动定向到新URI。今后任何新的请求都应使用新的URI代替 |
   | 302    | Found             | 临时移动。与301类似。但资源只是临时被移动。客户端应继续使用原有URI |
   | 304    | Not Modified      | 未修改。所请求的资源未修改，服务器返回此状态码时，不会返回任何资源(响应消息中不包含响应体)。客户端通常会缓存访问过的资源 |

3. 4**客户端错误相关的响应状态码

   4** 范围的状态码，表示客户端的请求有非法内容，从而导致这次请求的失败。常见的 4** 类型的状态码如下：

   | 状态码  | 状态码英文名称  | 中文描述                                                     |
   | ------- | --------------- | ------------------------------------------------------------ |
   | 400     | Bad Request     | 1、客户端请求的语法有误，当前请求无法被服务器理解。除非进行修改，否则客户端不应该重复提交这个请求。2、请求参数有误。 |
   | 401     | Unauthorized    | 当前请求需要用户验证。                                       |
   | 403     | Forbidden       | 服务器已经理解请求，但是拒绝执行它。                         |
   | **404** | **Not Found**   | **服务器无法根据客户端的请求找到资源(网页)。**               |
   | 408     | Request Timeout | 请求超时。服务器等待客户端发送的请求时间过长，超时。         |

4. 5** 服务端错误相关的响应状态码

   5** 范围的状态码，表示服务器未能正常处理客户端的请求而出现意外错误。常见的5** 类型的状态码如下：

   | 状态码 | 状态码英文名称        | 中文描述                                                     |
   | ------ | --------------------- | ------------------------------------------------------------ |
   | 500    | Internal Server Error | 服务器内部错误，无法完成请求。                               |
   | 501    | Not Implemented       | 服务器不支持该请求方法，无法完成请求。只有GET和HEAD请求方式是要求每个服务器必须支持的，其他请求方法在不支持的服务器上会返回501 |
   | 503    | Service Unavaliable   | 由于超载或系统维护，服务器暂时的无法处理客户端的请求         |

**HTTP缓存**

- 什么是缓存

  缓存是一种保存资源副本并在下次请求时直接使用该副本的技术。

- 为什么需要缓存

  如果没有缓存的话，每一次网络请求都要加载大量的图片和资源，这会使页面的加载变慢许多。那缓存的目的其实就是为了减少网络请求的体积和数量，让页面加载的更快。

- 哪些资源可以被缓存？——静态资源（js，css，img）

  注：（1）网站的html是不能被缓存的。因为网站在使用过程中html随时有可能被更新，随时有可能被替换模板。（2）网页的业务数据也是不能被缓存的。比如留言板和评论区，用户随时都可以在底下评论，那么数据库的内容就会频繁被更新。

**HTTP缓存策略（强制缓存+协商缓存）**

- 强制缓存：文件直接从本地缓存中获取，不需要发送请求

- 强制缓存的过程：

  （1）当初次请求时，浏览器会向服务器发起请求，服务器接收到浏览器的请求后，返回资源并返回一个cache-Control给客户端，该cache-Control一般设置缓存的最大过期时间。

  （2）当浏览器接收到cache-Control的值之后再次发起请求时，它会先检查它的cache-Control是否过期，如果没有过期则直接从本地缓存中拉取资源，返回到客户端，而无需再经过服务器。

  （3）强制缓存有过期时间，如果客户端的cache-Control失效了，那么它就没办法从本地缓存中拉取资源。于是会重新向服务器发起请求，之后服务器会再次返回资源和cache-Control的值。

- cache-Control是什么

  cache-Control存在于响应头Response Headers中，控制强缓存的逻辑，例如cache-Control：max-age=31536000（单位是秒）

- cache-Control的值

  | cache-Control | 含义                                                       |
  | ------------- | ---------------------------------------------------------- |
  | max-age       | 设置缓存的最大过期时间                                     |
  | no-cache      | 不用本地缓存，正常的向服务器请求，服务端怎么处理我们不用管 |
  | no-store      | 简单粗暴，直接从服务端拉取缓存                             |
  | private       | 只能允许最终用户做缓存，最终用户即电脑、手机等等           |
  | public        | 允许中间路由或中间代理做缓存                               |

- Expires

  Expires也在Response Headers中，控制缓存的过期时间（早期使用），如果cache-Control与expires同时存在的话，cache-Control的优先级高于expires。

- 协商缓存：也叫对比缓存，它是一种服务器的缓存策略，即通过服务端来判断某件事情是不是可以被缓存。服务端判断客户端的资源，是否和服务端的资源一样，如果一致则返回304，反之返回200和最新的资源。

- 协商缓存的过程：

  （1）如果浏览器是第一次向服务器发起请求，则服务器返回资源和相对应的资源标识给浏览器。该资源标识就是对当前所返回资源的一种唯一标识，可以是Etag或是Last-Modified。

  （2）之后浏览器再次发送请求时，浏览器就会带上这个资源标识。此时，服务端就会通过这个资源标识，可以判断出浏览器的资源跟服务端此时的资源是否一致，如果一致，就返回304，即表示Not Found资源未修改。如果判断结果为不一致，则返回200，并返回资源以及新的资源标识。

- 资源标识

  在响应头部Request Headers中，有两种资源标识：

  （1）Last-Modified：资源的最后修改时间，对应请求头为If-Modified-Since；（2）Etag资源的唯一标识，所以唯一，可以想象成人类的指纹，具有唯一性；但Etag的本质是一个字符串；对应请求头If-None-Match。（3）当响应头部Response Headers同时存在Last-Modified和Etag的值时，会优先使用Etag；（4）如果资源被重复生成，而内容不变，则Etag更精确。

- HTTP缓存流程图

  <img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1662270927707.png" alt="1662270927707" style="zoom:50%;" />

- 刷新操作方式对缓存的影响

  （1）正常操作：地址栏输入url，跳转链接，前进后退等。

  对缓存的影响：强制缓存有效，协商缓存有效。

  （2）手动刷新：F5，点击刷新按钮，右击菜单刷新

**什么是HTTP协议无状态协议？怎么解决HTTP协议无状态协议**

HTTP协议是一种无状态协议，即每次服务端接收到客户端的请求时，都是一个全新的请求，服务器并不知道客户端的请求记录；Session和Cookie的主要目的就是为了弥补HTTP的无状态特性。除了session和cookie，还有JSON Web Token，都可以为网站提供用户的身份认证。它们既可以对用户进行身份验证，也可以用来在用户单击进入不同页面时以及登录网站或应用程序进行身份验证。

- Session是什么

  客户端请求服务器，服务器会为这次请求开辟一块内存空间，这个对象便是Session对象，服务器可以利用Session存储客户端在同一个会话期间的一些操作记录。

- 创建Session

  服务器第一次接收到请求时，开辟了一块Session空间（创建了Session对象），同时生成一个sessionId，并通过响应头的Set-Cookie：JSESSIONID=XXXXXX的命令，向客户端发送要求设置Cookie的响应；客户端收到响应后，在本机客户端设置了一个JSESSIONID=XXXXXX的Cookie信息，该Cookie的过期时间为浏览器会话结束。接下来客户端每次向同一个网站发送请求时，请求头都会带上该Cookie信息（包含sessionId），然后，服务器通过读取请求头中的Cookie信息，获取名称为JSESSIONID的值，得到此次请求的sessionId。

- Cookie是什么

  Cookie包括Web Cookie和浏览器Cookie，它是服务器发送到Web浏览器的一小块数据。服务器发送到浏览器的Cookie，浏览器会进行存储，并与下一个请求一起发送到服务器。通常，它用于判断两个请求是否来自于同一个浏览器，例如用户保持登录状态。

- 创建Cookie

  当接收到客户端发出的HTTP请求时，服务器可以发送带有响应的Set-Cookie标头，Cookie通常由浏览器存储，然后将Cookie与HTTP标头一同向服务器发出请求。

- Cookies的类型

  有两种类型的Cookies，一种是session Cookie，一种是Persistent Cookies，如果Cookie不包含到期日期，则将其视为会话Cookie。会话Cookie存储在内存中，永远不会写入磁盘，当浏览器关闭时，此后Cookie将永久丢失。如果Cookie包含有效期，则将其视为持久性Cookie。在指定的日期时，Cookie将从磁盘中删除。

- Token是什么

  Token，令牌，代表执行某些操作的权利的对象。简单来说，就是类似Cookie的一种验证信息，客户端通过登录验证后，服务器会返回给客户端一个加密的token，然后当客户端再次向服务器发起连接时，带上token，服务器直接对token进行验证即可完成权限校验。（token需要自己使用localStorage或sessionStorage进行存储，没有内存限制，自己进行发送，不存在跨域限制，因此Token相比于Cookie更加灵活）

**HTTP缺点**

- 通信使用明文（不加密），内容可能被窃听
- 不验证通信方的身份，因此可能遭遇伪装
- 无法证明报文的完整性，所以可能已经被篡改

# 尚品汇

## 项目主要内容

•  项目描述：此项目为在线电商Web App，包括首页、搜索列表、商品详情、用户登录/注册等多个模块
•  技术栈：Vue全家桶 + ES6 + Webpack + Axios
•  项目内容：

1. 使用 编程式导航路由 + 事件委派 + 自定义属性 实现搜索页面的跳转

   **answer**

   **编程式导航路由**

   路由的跳转有两种方式：声明式导航，编程式导航。

   使用声明式导航会出现卡顿现象。因为router-link是一个组件，相当于VueComponent类的实例对象。一瞬间new VueComponent很多实例，很消耗内存，因此导致卡顿。

   因此采用编程式导航进行路由跳转。（好处：可以书写自己的业务逻辑）。

   

   **事件委派**

   TyprNav三级联动菜单，点击a链接实现搜索页面跳转。

   

   **分析**

   点击三级菜单中的a链接都将跳转到搜索页面。利用**事件委派**，给三级菜单的父元素绑定路由跳转点击事件。

   **产生新的问题**

   事件委派满足了需求，但同时引发了新的问题：

   （1）事件委派是把全部子节点的事件委派给父节点(不仅是a标签，还有h3，dt，dl，em)。但是只有点击a标签的时候才会进行路由的跳转，**此时不能确定点击的一定是a标签**。

   （2）即使能确定点击的是a标签，在获取参数（1、2、3级分类的产品名字，ID）时如何区分点击的是一级，二级还是三级的a标签又是一个问题。

   **解决【自定义属性】**

   （1）给子节点当中的a标签，添加**自定义属性data-categoryName**，其余的子节点是没有的。判断标签身上是否有categoryname，如果存在则一定是a标签。

   （2）分别给一级、二级、三级a标签添加category1Id、category2Id、category3Id自定义属性可以区分出不同级的a标签。

   ```js
   // 进行路由跳转【home→search】的方法
         goSearch(event) {
             // 最好的解决方案：编程式导航路由+事件委派+自定义属性
             // 利用事件委派存在的问题：1. 事件委派，是把全部的子节点[h3,dt,dl,em]的事件委派给父节点
             // 点击a标签的时候，才会进行路由跳转【怎么能确定点击的一定是a标签】
             // 2. 即使能确定点击的是a标签，如何区分是一级、二级、三级分类的标签。
             // 解决第一个问题：把子节点当中a标签，加上自定义属性data-categoryName，其余的子节点是没有的
           let element = event.target
           // 获取到当前触发这个事件的节点【h3,a,dt,dl】，需要带有data-categoryName这样的节点【一定是a标签】
           // 节点有一个dataset属性，可以获取节点的自定义属性与属性值
           let {categoryname, category1id, category2id, category3id} = element.dataset
           // 如果标签身上拥有categoryname一定是a标签
           if(categoryname) {
               // 整理路由跳转的参数
               let location = {name: 'search'}
               let query = {categoryName: categoryname}
               // 一级分类、二级分类、三级分类的a标签
               if(category1id) {
                   query.category1Id = category1id
               }else if(category2id) {
                   query.category2Id = category2id
               } else {
                   query.category3Id = category3id
               }
               // 判断：如果路由跳转的时候，带有params参数，捎带传递过去
               if (this.$route.params) {
                   location.params = this.$route.params
                   // 整理完参数
                   location.query = query
                   // 路由跳转
                   this.$router.push(location)
               }
           }
         }
   ```

   

2. 使用lodash插件提供的防抖和节流功能来减少事件处理函数的调用频率，提升用户体验

   **answer**

   按需加载引入lodash

   ```js
   import throttle from 'lodash/throttle'
   ```

   TyprNav三级联动菜单，鼠标进入一级菜单事件。事件处理函数：当鼠标进入一级菜单，将鼠标当前索引等于鼠标移上某一个一级分类元素的索引值。

   **分析**

   正常情况（用户慢慢的操作）：鼠标进入每一个一级分类，都会触发鼠标进入事件；

   非正常情况（用户操作很快）：由于用户的行为过快，导致浏览器反应不过来，如果当前的回调函数中有一些大量的业务，有可能出现卡顿现象。（本身全部的一级分类都应该触发鼠标进入事件，但是经过测试，只有部分被触发了）

   **解决【节流】**

   节流：在规定的间隔时间内不会重复触发回调，只有大于这个时间间隔才会触发回调，把频繁触发变为少量触发

   防抖：前面的所有的触发都被取消，最后一次执行在规定的时间之后才会触发，也就是说如果连续快速的触发 只会执行最后一次

   **总结：【闭包+延时】**

   防抖：用户操作很频繁，但是只是执行一次。场景：输入框搜索事件，等用户输入完毕之后才会响应

   节流：用户操作很频繁，但是把频繁的操作变为少量操作【可以给浏览器充裕的时间去解析代码】，场景：计数器1秒之内只能加1；轮播图在规定时间内只能切换一张

   ```js
   changeIndex: throttle(function(index) {
       this.currentIndex = index
   }, 50)
   ```


​      

3. 使用Vuex模块式开发管理项目的数据，让数据分类更加明确；使用mock模块实现模拟数据

   **answer**

   （1）Vuex经常用的套路是state、mutations、actions、getters、modules

   （2）当后端开发人员没有写好接口时，前端开发人员可以mock一些数据，即模拟一些假的接口，在开发项目时可以把它当成真实的接口看待。在工作中项目上线时，需要把mock数据变为后台开发人员提供的接口数据。

   **第一步**:安装依赖包mockjs

   **第二步**：在src文件夹下创建一个文件夹，文件夹mock文件夹。

      **第三步**:准备模拟的数据(json数据，mock文件夹中创建相应的JSON文件)----格式化一下，别留有空格
      把mock数据需要的图片放置于public文件夹中！【public文件夹在打包的时候，会把相应的资源原封不动打包到dist文件夹中】
      比如:listContainer中的轮播图的数据
      [
         {id:1,imgUrl:'xxxxxxxxx'}, 
         {id:2,imgUrl:'xxxxxxxxx'}, 
         {id:3,imgUrl:'xxxxxxxxx'}, 
   ]

      **第四步**：在mock文件夹中创建一个server.js文件
      注意：在server.js文件当中对于banner.json||floor.json的数据没有暴露，但是可以在server模块中使用。
   对于webpack当中一些模块：图片、json数据格式，不需要对外暴露，因为**默认就是对外暴露**。

   **第五步**:通过mock模块模拟出数据

   通过Mock.mock方法进行模拟数据

      **第六步**:回到入口文件，引入serve.js（至少需要执行一次，才能模拟数据）
      mock需要的数据|相关mock代码页书写完毕，关于mock当中serve.js需要执行一次，
   如果不执行，和你没有书写一样的。

      **第七步**:在API文件夹中创建mockRequest【axios实例：baseURL:'/mock'】
   专门获取模拟数据用的axios实例。

   

4. 使用Swiper + watch + $nextTick实现轮播图效果

   **QA**

   问：swiper可以在移动端使用，还是在PC端使用？

   答：swiper移动端可以使用，pc端也可以使用。

   问：swiper常用于哪些场景？

   答：常用的场景为轮播图----【carousel：轮播图】

    **Swiper使用步骤：**
   第一步：引入依赖包【swiper.js|swiper.css】
   第二步:   静态页面中结构必须完整【container、wrap、slider】，类名不能瞎写
   第三步:   初始化swiper实例【轮播图添加动态效果】

   **问题**

   在**mounted**【组件实例挂载完毕】中初始化swiper实例，轮播图没有实现动态效果。（**初始化swiper实例之前，页面中的结构务必要有**）

   **原因**

   Swiper需要获取到轮播图的节点DOM，才能给swiper轮播添加动态效果，在mounted中，首先向vuex派发了action，ajax向服务器发请求涉及到异步语句，导致v-for遍历轮播图的时候结构还不完整，因此没有动态效果。

   **解决【mounted→watch】**

   watch监听属性可以监测到属性值的变化，当属性值发生变化的时候，可以触发一次。

   组件实例在使用仓库中的bannerList，组件的这个属性一定是bannerList一定是发生过变化，bannerList初始值是空数组，当服务器的数据返回以后，它的bannerList存储的属性值会发生变化【变为服务器返回的数据】，watch可以监听到。

   **还有一个问题**

   watch虽然可以监听到bannerList的变化，但是无法保证v-for已经执行结束了，只有当v-for执行完毕了才有结构。

   **解决【$nextTick】**

   组件实例的一个方法$nextTick

      nextTick官网解释:
      在下次DOM更新, 循环结束之后,执行延迟回调。在 修改数据之后 立即使用这个方法，获取更新后的DOM。
   注意：组件实例的$nextTick方法，在工作当中经常使用，经常结合第三方插件使用，获取更新后的DOM节点

   总结:$nextTick可以保留页面中的结构是一定有的，经常和很多插件一起使用【都需要DOM存在】。

      ```js
      watch: {
              // 监听bannerList数据的变化：因为这条数据发生过变化，由一个空数组变为数组里面有四个元素
              bannerList: {
                  immediate: true,
                  handler(newValue, oldValue) {
                      // 现在咱们通过watch监听bannerList属性的属性值的变化
                      // 如果执行handler方法，代表组件实例的身上这个属性应该有值了【四个元素的数组】
                      // 当前这个函数执行：只能保证bannerList的数据已经有了，但是没有办法保证v-for已经执行结束了【v-for执行也很耗时间】
                      // v-for执行完毕了才有结构【在watch当中没办法保证】
                      // nextTick：在下次DOM更新 循环结束之后 执行延迟回调。在 修改数据 之后，立即使用这个方法，获取更新后的DOM
                      this.$nextTick(() => { 
                          // 当你执行这个回调的时候，保证服务器数据回来了，v-for执行完毕了【轮播图的结构一定有了】初始化swiper实例对象
                          var mySwiper = new Swiper(this.$refs.mySwiper, {
                              loop: true,
                              // 如果需要分页器
                              pagination: {
                                  el: ".swiper-pagination",
                                  // 点击小球的时候也切换图片
                                  clickable: true
                              },
                              // 如果需要前进后退按钮
                              navigation: {
                                  nextEl: ".swiper-button-next",
                                  prevEl: ".swiper-button-prev",
                              }
                          });
                      });
                  }
              }
          }
      ```

   

5. 封装分页器全局组件

   第三方插件:elementUI实现超级简单

   对于分页器而言，自定义前提需要知道四个前提条件：

   （1）pageNo：当前在第几页

   （2）pageSize：代表每一页展示多少条数据

   （3）total：代表整个分页器一共要展示多少条数据

   （4）continue：代表分页连续页码个数

   分页器动态展示，分为上中下三个部分

   ```vue
      <template>
        <div class="pagination">
          <!-- 测试用的数据 -->
          <!-- <h1>{{startNumAndEndNum}}-----当前的页码{{pageNo}}</h1> -->
          <!-- 上 -->
          <button :disabled="pageNo==1" @click="$emit('getPageNo',pageNo-1)">上一页</button>
          <button 
          v-if="startNumAndEndNum.start > 1" 
          @click="$emit('getPageNo',1)" 
          :class="{active: pageNo==1}"
          >
            1
          </button>
          <button v-if="startNumAndEndNum.start > 2">···</button>
      
          <!-- 中间部分 -->
          <button v-for="(page,index) in startNumAndEndNum.end" 
          :key="index" 
          v-if="page>=startNumAndEndNum.start" 
          @click="$emit('getPageNo',page)" 
          :class="{active: pageNo==page}"
          >
            {{page}}
          </button>
          <!-- <button>3</button>
          <button>4</button>
          <button>5</button>
          <button>6</button>
          <button>7</button> -->
          
          <!-- 下 -->
          <button v-if="startNumAndEndNum.end < totalPage - 1">···</button>
          <button 
          v-if="startNumAndEndNum.end < totalPage" 
          @click="$emit('getPageNo',totalPage)" 
          :class="{active: pageNo==totalPage}"
          >
            {{totalPage}}
          </button>
          <button :disabled="pageNo==totalPage" @click="$emit('getPageNo',pageNo+1)">下一页</button>
          
          <button style="margin-left: 30px">共 {{total}} 条</button>
        </div>
      </template>
      
      <script>
        export default {
          name: "Pagination",
          props: ['pageNo', 'pageSize', 'total', 'continues'],
          computed: {
            // 总共多少页
            totalPage() {
              // 向上取整
              return Math.ceil(this.total / this.pageSize)
            },
            // 计算出连续的页码的起始数字与结束数字[连续页码的数字：至少是5]
            startNumAndEndNum() {
              const {continues, pageNo, totalPage} = this
              // 先定义两个变量存储起始数字与结束数字
              let start = 0, end = 0
              // 连续的页码时5,【就是至少五页】如果出现不正常的现象【就是不够五页】
              // 不正常现象【总页码数没有连续页码多】
              if(continues > totalPage) {
                start = 1
                end = totalPage
              } else {
                // 正常现象【连续页码5，但是总页数一定是大于5的】
                // 起始数字
                start = pageNo - parseInt(continues / 2)
                // 结束数字
                end = pageNo + parseInt(continues / 2)
                // 把出现不正常的现象【start数字出现0|负数】纠正
                if(start < 1) {
                  start = 1,
                  end = continues
                }
                // 把出现不正常的现象【end数字大于总页码的】
                if (end > totalPage) {
                  end = totalPage,
                  start = totalPage - continues + 1
                }
              }
              return {start, end}
            }
          }
        }
      </script>
   ```

   

6. 利用路由传参结合会话存储跳转到购物车加入成功页面

   **在路由跳转的时候需要将产品信息以及id带给下一级路由**

   可以用下面这种手段实现路由跳转以及传递参数：

   ```js
   this.$router.push({name: 'addcartsuccess',query: {skuInfo: this.skuInfo,skuNum: this.skuNum}})
   ```

   **其中产品信息skuInfo是一个对象，在地址栏中会转成字符串看着不美观，可以利用会话存储将产品信息存储到浏览器中**

   ```js
   // 本地存储|会话存储一般存储的是字符串，因为需要将其转换成字符串形式
   sessionStorage.setItem("SKUINFO",JSON.stringify(this.skuInfo))
   // 一些简单的数据skuNum，通过query形式给路由组件传递过去，产品信息数据比较复杂，通过会话存储
   this.$router.push({name: 'addcartsuccess',query:{skuNum: this.skuNum}})
   ```

   **会话存储的特点：存储不持久化，会话结束后数据再消失。对于该项目需求，会话存储即可达到目的，使用本地存储是没有必要的。**

   

7. 使用uuidv4封装游客身份模块，通过请求头将临时身份带给服务器，存储用户购物车数据

   **问题**

   向服务器发请求获取购物车数据，请求成功，但是购物车数据为空

   **原因**

   只是向服务器存储了用户数据，但是服务器并不知道存储的这些数据属于谁。

   **解决**

   **解决思路：**在用户将商品添加到购物车时(商品详情页)，需要将用户的临时身份信息携带给服务器，告知服务器产品ID和数量属于哪个用户，把数据存储于相应的用户中。

   **具体办法：**uuidv4生成一个随机字符串，每次都会发生变化，但是游客的身份不能改变，因此需要结合本地存储localStorage封装游客身份模块，作为用户唯一的标识。但是请求获取购物车接口只带有两个参数产品id和产品个数，没有uuid参数，不能通过接口携带。因此需要通过请求头将临时身份携带给服务器(添加userTemp字段)，从而存储用户购物车数据。

   

   **新的问题**

   游客身份在仓库中，ajax请求模块中拿不到游客身份

   **解决**

   要在请求拦截器中捞到仓库

   ```js
   // 在axios二次封装模块中引入仓库
   import store from "@/store"
   
   requests.interceptors.request.use(config => {
     // config: 配置对象，对象里面有一个属性很重要，headers请求头
     if (store.state.detail.uuid_token) {
       // 给请求头添加一个字段(userTempId)：和后台商量好了，不能随便写
       config.headers.userTempId = store.state.detail.uuid_token
     }
     // 需要携带token带给服务器
     if (store.state.user.token) {
       config.headers.token = store.state.user.token
     }
     // 进度条开始滚动
     nprogress.start()
     return config
   })
   ```

   

8. 通过给请求头添加token字段，将token的值携带给服务器，获取用户唯一标识，从而返回用户登录信息。

   **问题**

   向服务器发请求获取用户登录信息，请求成功，但是请求返回未登录

   **原因**

   虽然发起了“获取用户登录信息”请求(平台首页)，但是服务器需要知道是谁需要用户信息才能返回相应的登录信息。因为请求没有携带token参数给服务器，所以服务器认为用户没有登录，因此获取不到用户的信息。（接口没有让带多余的参数）

   **解决**

   需要带着用户的token向服务器要用户信息【获取用户信息】在请求拦截器中给请求头添加token字段，发请求的时候把token携带给服务器。

   

   token**令牌**理解：用户的唯一标识符

   注意：vuex仓库存储数据-----不是持久化（一旦刷新，数据就变没了）

   

   token面试题:项目当中token过期、失效如何处理？
   答：清除本地token（本地存储），让用户回到登录页，获取最新的token

   

9. 不使用vuex仓库，直接在组件中发请求获取数据，数据初始值存储到data中

10. Element-UI按需引入实现支付页面部分业务(遮罩层)



**开发中遇到的困难**：

在搜索页面中，页面没有随着用户选择条件的变化而变化。

在搜索页面中，用户的搜索条件可以发生多次变化，但是如果只在mounted中发请求获取搜索模块的数据，那么请求只会发出一次，所以用户的搜索条件发生变化时并没有再次发起请求。如果要根据用户的搜索条件展示不同的数据，则可以监听路由的信息是否发生变化，如果路由信息变化了则再次发起请求获取数据。

在发请求之前beforeMount中，home→search跳转页面时携带的参数也需要整理好一并传递给服务器。

Object.assign(this.searchParams, this.$route.query, this.$route.params)

```js
watch: {
      // 监听路由的信息是否发生变化，如果发生变化，再次发起请求
      $route(newValue,oldValue) {
        // 再次发请求之前整理需要带给服务器的参数
        Object.assign(this.searchParams,this.$route.query,this.$route.params)
        // 再次发起Ajax请求
        this.getData()
        // 每一次请求完毕，应该把相应的一级、二级、三级分类的id置空，让它接收下一次请求相应的1,2,3id
        // 分类名字与关键字不用清空，因为每一次路由发生变化的时候，都会给他赋予新的值
        this.searchParams.category1Id = undefined
        this.searchParams.category2Id = undefined
        this.searchParams.category3Id = undefined
        
      }
    }
```

根据前台传递参数决定的
根据不同条件，展示不同的数据。----->取决于后台返回的数据

1:发请求，获取搜索模块的数据
2:根据用户搜索的条件携带参数给服务器，展示用户搜索的内容

其中，面包屑在删除时，也会重新发起请求，只不过是自己跳转到自己

1）动态开发面包屑中的分类名，编程式导航路由【自己跳自己】

2）动态开发面包屑中的关键字

2.1 当面包屑中的关键字清除以后，需要让兄弟组件Header组件中的关键字清除

```js
// 删除分类的名字
      removeCategoryName() {
        // 把带给服务器的参数置空了，还需要向服务器发请求
        // 带给服务器的参数说明（都是可有可无的），如果属性值为空的字符串还是会把相应的字段带给服务器
        // 但是把相应的字段变为undefined，当前这个字段不会带给服务器
        this.searchParams.categoryName = undefined
        this.searchParams.category1Id = undefined
        this.searchParams.category2Id = undefined
        this.searchParams.category3Id = undefined
        // 删掉分类面包屑，需清空参数，重新请求默认数据
        this.getData()
        // 地址栏也需要修改：进行路由跳转(现在的路由跳转只是跳转到自己这里)
        // 如果地址栏中带有params参数，则params参数不应该删掉
        // 严谨：本意是删除query，如果路径当中出现params不应该删除，路由跳转的时候应该带着
        if(this.$route.params) {
          this.$router.push({name:"search",params:this.$route.params})
        }
      },
```



--------------------------------------------------------------

## 项目性能优化

（1）TypeNav三级联动性能优化

**问题**

home切换到search或者search切换到home，组件在频繁的向服务器发请求，获取三级联动的数据进行展示。项目中如果频繁的向服务器发请求，很耗性能的，因此需要进行优化。

为什么会频繁的向服务器发请求获取三级联动的数据呢？

因为路由跳转的时候，组件会进行销毁的【home组件的created：在向vuex派发action，因此频繁的获取三级联动的数据】

**解决**

只需要发一次请求，获取到三级联动的数据即可，不需要多次。

答：在App根组件当中发请求【根组件mounted】执行一次

（main.js也是执行一次，但是不可以放在它里面，因为它不是一个组件(以.vue结尾)，而是一个js文件，this是undefined，组件身上才有this.$store）

（2）v-if | v-show选择

（3）按需加载

​			对于loadsh插件，它里面封装的函数功能很多，import _ from lodash 相当于把全部功能引入进来，但是我们只是需要节流。因此只需要按需引入节流函数import throttle from ‘lodash/throttle’

（4）防抖与节流：请求次数优化

（5）search搜索页面请求的性能优化

发一个请求，需要向服务器携带参数：带100个参数 带1个参数【消耗宽带】。

把带给服务器的参数置空了，还需要向服务器发请求。

带给服务器参数说明是可有可无的，如果属性值为空的字符串还是会把相应的字段带给服务器。

此时把相应的字段变为undefined，当前这个字段不会带给服务器。

对于给服务器携带的参数，如果数值为undefined，向服务器发请求时，参数不会携带给服务器的。

（6）图片懒加载：服务器图片数据没回来时，展示默认的图片

（7）路由懒加载：当用户访问的时候，加载对应的组件进行展示



# 科研成果

