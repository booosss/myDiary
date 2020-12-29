### 说一说CSS的盒子模型
    1.标准盒模型
      元素宽度 = 外边距 + 边框 + 内边距 + 内容的宽度
    2.IE盒模型
      元素宽度 = 外边距 + 内容的宽度（border + padding + width）
    box-sizing来设置盒模型的类型，border-box是IE盒模型，content-box是标准盒模型
### 说一说什么是外边距重叠
    假如有两个相邻的块级元素，div1， div2，两个都设置了外边距，div1 { margin: 10px 0; } div2 { margin: 20px 0 }，那么，div1和div2之间的外边距是20，而不是30，这就是外边距重叠。要解决外边距溢出的问题，就需要创建BFC(块级格式化上下文)元素，或者使用浮动
    如何创建BFC元素呢？设置float，position，overflow，display属性
### 说一说link和@import的区别
    1.link是属于标签，没有兼容性的问题，@import在IE5以上才能被识别。
    2.使用link引入的样式会按照页面加载顺序加载，而使用@import引入的样式，会等到页面加载完毕之后，才会加载。
    3.link还可以用来加载RSS文件，而@import只能加载CSS样式
### 说一说常用浏览器的内核
    1.IE浏览器--->trident
    2.Chrome--->webkit
    3.FireFox--->Gecko
    4.Opera--->Presto
    浏览器内核分为：1.渲染引擎， 2.JS引擎
    渲染引擎：负责渲染网页内容，整理信息，引入CSS，以及计算网页的显示方式，将渲染完成的网页显示在显示器上
    JS引擎：用来解析和执行Javascript代码，来实现网页的动态效果
### !DOCTYPE的作用
    1.DOCTYPE位于HTML文档中的第一行，来告知浏览器，以什么样的文档类型来解析这个文档。
    2.还可以用来区分严格模式和混杂模式。严格模式是指浏览器按照W3C的标准来解析代码，混杂模式（又称怪异模式或者兼容模式）是指浏览器用自己的方式来解析代码。浏览器使用哪种标准与文档类型有关系（DTD，document type definition）
    在HTML5中没有文档类型，HTML5没有严格模式和混杂模式的区别。
### 优雅降级和渐进增强的区别
    优雅降级：一开始就构建完整的功能，然后再针对低版本浏览器做兼容处理
    渐进增强：为了兼容低版本的浏览器，先实现在基本的功能，再针对新浏览器优化功能
### HTML5的新特性
    移除的标签：big, center, font, strike, u, s, frame, frameset, noframes, applet,
    新增标签：
      1.语义元素：header, footer, nav, aside, section, article, main, details, summary, figure
      2.表单交互：input, detalist, kegen, meter, progress, command, menu
      3.音视频：audio, video, source
      4.Canvas: canvas