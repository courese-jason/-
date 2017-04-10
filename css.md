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
    p.info { ... }
    p.info.error { ... }
    #info { ... }
    p#info { ... }

二、 多元素的组合选择器

序号| 选择器 | 含义
-|-|-
5. | E,F | 这是测试