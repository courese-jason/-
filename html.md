# HTML
> *网页由主干`<html>`与其他元素组合成树形结构，这个层次性的结构就是 DOM : Document Object Modal(文档对象模型)*

### 文档类型声明

    <!DOCTYPE html>

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

         。X-UA-Compatible:

         例子：`<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />` 

         含义：IE=edge告诉IE使用最新的引擎渲染网页，chrome=1则可以激活Chrome Frame

         。Content-Security-Policy：
         
           简称*CSP*,中文简称*内容安全策略*，这个属性允许网站管理员对服务资源定制内容安全规范。主要是用来定义页面可以加载哪些资源，减少*跨域脚本攻击XSS*

           完整的浏览器 CSP 支持情况请移步 [CanIUse](http://caniuse.com/#feat=contentsecuritypolicy)。

           有什么用？
           我们知道前端有个很著名的”同源策略”,简而言之,就是说一个页面的资源只能从与之同源的服务器获取,而不允许跨域获取.这样可以避免页面被注入恶意代码,影响安全.但是这个策略是个双刃剑,挡住恶意代码的同时也限制了前端的灵活性,那有没有一种方法既可以让我们可以跨域获取资源,又能防止恶意代码呢？CSP就可以解决这个问题。通过定义策略来限制资源的访问。

           使用CSP:

           > Content-Security-Policy: policy
           > policy参数是一个描述你的CSP策略指令的字符串
           > 升级到level 2 以后，推荐在服务器端(nginx,apache,iis的web配置文件中设置这个安全策略)
           常用实例：
           
           示例1：一个网站管理者想要所有内容均来自站点自己 (这排除子域名.)
           Content-Security-Policy: default-src 'self'

           示例2：一个网站管理者允许内容来自信任的域名极其子域名 (it doesn't have to be the same domain that the CSP is set on.)
           Content-Security-Policy: default-src 'self' *.trusted.com
           
           示例3：一个网站管理者允许网页应用的用户在他们自己的内容上从任何源获取图片, 但是限制音频或视频需从信任的资源提供者(获得), 所有脚本必须从特定主机服务器获取可信的代码.
           Content-Security-Policy: default-src 'self'; img-src *; media-src media1.com media2.com; script-src userscripts.example.com

           [基本解说](http://www.bkjia.com/webzh/866374.html)

    * name

        name属性的合理使用，是增强SEO的方式之一。

        示例：
        `<Meta name="Kyewords" Lang="EN" Content="vacation,greece,sunshine">`

3. `<link>`

    指定外部资源，常用来链接css文件
    ```
    <script>
    function sheetLoaded() {
    // Do something interesting; the sheet has been loaded
    }

    function sheetError() {
    alert("An error occurred loading the stylesheet!");
    }
    </script>

    <link rel="stylesheet" href="mystylesheet.css" onload="sheetLoaded()" onerror="sheetError()">
    ```
4. `<style>`

    在html文档内定义 css 样式

5. `<script>`    

    * 引用可执行 js 脚本

    ```<script type="text/javascript" src="demo.js"></script>```

    * 文档嵌入 script 脚本
    ```
    <script>
        // do something interacting, to do actions
    </script>
    ```
### 常用块级元素

    
