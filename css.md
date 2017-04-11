# CSS

### CSS 选择器

一、基本选择器

序号| 选择器 | 含义
-|-|-
1. | * | 通用元素选择器，匹配任何元素
2. | E | 标签选择器，匹配所有使用E标签的元素
3. | .info | class选择器，匹配所有class属性中包含info的元素
4. | #info | id选择器，匹配所有id属性等于footer的元素

实例：

    * { margin: 0; padding: 0; }
    p { font-size: 0.2em; }
    .info { background: #fff; }
    p.info { background: #fff; }
    p.info.error { background: #fff; }
    #info { background: #fff; }
    p#info { background: #fff; }

二、 多元素的组合选择器

序号| 选择器 | 含义
-|-|-
5. | E,F | 多元素选择器，同时匹配所有E元素或F元素，E和F之间用逗号分隔
6. | E F | 后代元素选择器，匹配所有属于E元素后代的F元素，E和F之间用空格分隔
7. | E > F | 子元素选择器，匹配所有E元素的子元素F
8. | E + F | 毗邻元素选择器，匹配所有紧随E元素之后的同级元素F

实例：

    .info,.msg { }
    #nav li { display: inline; }
    div > strong { font-size : 18px; }
    p + p { color: #f00; }

三、 CSS 2.1 属性选择器

序号 | 选择器 | 含义
-|-|-
9. | E[att] | 匹配所有具有att属性的E元素，不考虑它的值（注意：E在此处可以省略，比如“[checked]”。以下同）
10. | E[att=val] | 匹配所有att属性等于"val"的E元素
11. | E[att~=val] | 匹配所有att属性具有多个空格分隔的值并且其中一个值等于“val”的E元素
12. | E[att|=val] | 匹配所有att属性具有多个连字号分隔的值并且其中一个值以"val"开头的的E元素，主要用于lang属性，比如"en"、"en-us"、"en-gb"等等

实例：

    p[title] { color: #f00; }
    div[class=error] { color: #f00; }
    td[headers~=coll] { color: #f00; }
    p[lang|=en] { color: #f00; }
    blockquote[class=quote][cite] { color: #f00; }

四、CSS 2.1 中的伪类

序号 | 选择器 | 含义
-|-|-    
13. | E:first-child | 匹配父元素的第一个子元素
14. | E:link | 匹配所有未被点击的链接
15. | E:visited | 匹配所有已被点击的链接
16. | E:active | 匹配鼠标已经其上按下，还没释放的E元素
17. | E:hover | 匹配鼠标悬停其上的E元素
18. | E:focus | 匹配获得当前焦点的E元素
19. | E:lang(c) | 匹配lang属性等于c的E元素

实例：

    p:first-child { font-style: italic; }
    input[type=text]:focus { color:#000; background: #ffe; }


    

