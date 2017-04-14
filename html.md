# HTML

### 根元素
    <html>

### 文档元数据

1. `<head>`

2. `<meta>`

    * http-equiv

         > 这个枚举属性定义了能改变服务器和用户引擎行为的编译。这个编译值使用content 来定义

         常用类型
         
         。charset和Content-Type
         
         例子：`<Meta http-equiv="Content-Type" Content="text/html; Charset=UTF-8">`

         。Content-Language: 定义页面使用的默认语言

         例子：`<Meta http-equiv="Content-Language" Content="zh-CN">`

         。Content-Security-Policy：
         
           简称*CSP*,这个属性允许网站管理员对服务资源定制内容安全规范。主要是用来定义页面可以加载哪些资源，减少*跨域脚本攻击XSS*

           完整的浏览器 CSP 支持情况请移步 [CanIUse](http://caniuse.com/#feat=contentsecuritypolicy)。

           



    * name
