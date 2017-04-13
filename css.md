# CSS

### CSS 选择器

一、基本选择器

序号| 选择器 | 名称 | 含义
-|-|-|-
1. | * | 通配选择器 | 通用元素选择器，匹配任何元素
2. | E | 元素选择器 | 标签选择器，匹配所有使用E标签的元素
3. | .info | 类选择器 | class选择器，匹配所有class属性中包含info的元素
4. | #info | ID选择器 | id选择器，匹配所有id属性等于footer的元素

实例：

    * { margin: 0; padding: 0; }
    p { font-size: 0.2em; }
    .info { background: #fff; }
    p.info { background: #fff; }
    p.info.error { background: #fff; }
    #info { background: #fff; }
    p#info { background: #fff; }

二、 多元素的组合选择器

序号| 选择器 | 名称 | 含义
-|-|-|-
5. | E,F | 多元素选择器 | 同时匹配所有E元素或F元素，E和F之间用逗号分隔
6. | E F | 后代元素选择器 | 匹配所有属于E元素后代的F元素，E和F之间用空格分隔
7. | E > F | 子元素选择器 | 匹配所有E元素的子元素F
8. | E + F | 相邻兄弟选择器 | 匹配所有 *紧随* E元素之后的同级元素F
9. | E ~ F | 普通兄弟选择器 | 匹配所有 *非紧随* E元素之后的同级元素F

实例：

    .info,.msg { }
    #nav li { display: inline; }
    div > strong { font-size : 18px; }
    p + p { color: #f00; }

三、 CSS 2.1 属性选择器

序号 | 选择器 | 含义
-|-|-
1. | E[att] | 匹配所有具有att属性的E元素，不考虑它的值（注意：E在此处可以省略，比如“[checked]”。以下同）
2. | E[att=val] | 匹配所有att属性等于"val"的E元素
3. | E[att~=val] | 匹配所有att属性具有多个空格分隔的值并且其中一个值等于“val”的E元素
4. | E[att|=val] | 匹配所有att属性具有多个连字号分隔的值并且其中一个值以"val"开头的的E元素，主要用于lang属性，比如"en"、"en-us"、"en-gb"等等

实例：

    p[title] { color: #f00; }
    div[class=error] { color: #f00; }
    td[headers~=coll] { color: #f00; }
    p[lang|=en] { color: #f00; }
    blockquote[class=quote][cite] { color: #f00; }

四、CSS 2.1 中的伪类

序号 | 选择器 | 含义
-|-|-    
1. | E:first-child | 匹配父元素的第一个子元素
2. | E:link | 匹配所有未被点击的链接
3. | E:visited | 匹配所有已被点击的链接
4. | E:active | 匹配鼠标已经其上按下，还没释放的E元素
5. | E:hover | 匹配鼠标悬停其上的E元素
6. | E:focus | 匹配获得当前焦点的E元素
7. | E:lang(c) | 匹配lang属性等于c的E元素
8. | E:nth-child(an+b) | 匹配E元素的多个子元素，与模式an+b匹配

实例：

    p:first-child { font-style: italic; }
    input[type=text]:focus { color:#000; background: #ffe; }

五、CSS 2.1 中的伪元素
>*备注：在css2 中使用单冒号，是过时用法，并仅用来支持IE8;而css3中则应该使用 双冒号，用来将伪类和伪元素区别开来*

例子：
> :after  // css2.1 过时用法
>
> ::after  // css3 新用法

序号 | 选择器 | 含义 
-|-|-    
1. | E::after | 匹配已选中元素的一个虚拟的最后子元素.通常会配合content属性来为该元素添加装饰内容.这个虚拟元素默认是行内元素。
2. | E::before | 匹配已选中元素的一个子元素作为伪元素。常通过 content 属性来为一个元素添加修饰性的内容。 此元素默认为行内元素。
3. | E::first-letter | 匹配E元素的第一个字母，且无如图片或表格的其他内容
4. | E::first-line | 匹配E元素的第一行

