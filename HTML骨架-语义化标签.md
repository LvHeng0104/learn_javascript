# 一. HTML

## 1.1 什么是语义化标签 ?

>语义类标签也是大家工作中经常会用到的一类标签，它们的特点是视觉表现上互相都差不多，主要的区别在于它们表示了不同的语义，比如大家会经常见到的section、nav、p，这些都是语义类的标签。

>语义是我们说话表达的意思，多数的语义实际上都是由文字来承载的。语义类标签则是纯文字的补充，比如标题、自然段、章节、列表，这些内容都是纯文字无法表达的，我们需要依靠语义标签代为表达。

> 有的语义化标签时为了方便人阅读的,有的是方便机器爬虫识别的,有的是方便程序员阅读的;

## 1.2 标签介绍

1. `hgroup `
   - 在文本拥有主标题和副标题的时候,使用该标签包裹两个标题作为和文本内容的区分
2. `abbr`
   - 但文中出现缩写英文时,用abbr包裹缩写后的字符,并用title属性记录缩写前的内容
   - `<abbr title="World Wide Web">WWW</abbr>.`
3. `strong `
   1. 加粗,黑体
4. 引述内容(鼠标放置后悬浮出一个框,移除后消失)
   1. `blockquote` 引述段落级类容
   2. `p` 引述行内引述内容
   3. `cite `表示引述的作品名称

5. `time `

   1. 用于描述时间.包裹时间

6. `figure`

   1. 结合图片展示
   2. 配合`figcaption`,给图片以描述

   ```javascript
   <figure>
    <img src="https://.....440px-NeXTcube_first_webserver.JPG"/>
    <figcaption>The NeXT Computer used by Tim Berners-Lee at CERN.</figcaption>
   </figure>
   ```

   

7. `nav`,`ol` ,`ul` 

   1. nav 用来定义导航连接部分,其内部内容是有序的排列
   2. ol 子元素在功能是不分先后的
   3. ul 表示有序分布
   4. `pre`, `samp`,`code`
   5. 该功能组合能够在页面中嵌入代码,可以让浏览器不解析其中信息
   6. 语义化 `pre`元素,对于内容连内容排版原封不动的显示,可用于显示大量的计算机代码片段
   7. `samp`元素,表示由程序或计算机输出的文本字符串
   8. `code` 用于表示简短的计算机代码片段

   - 思考: 输入一段HTML代码

     1. 排版样式不能乱,所以需要pre包裹
     2. 输入的是代码,所以需要code包裹
     3. samp和code的作用差不多

     ```javascript
     <pre><code>
     &lt;html&gt;
       &lt;head&gt;
         &lt;title&gt;Example.org – The World Wide Web&lt;/title&gt;
       &lt;/head&gt;
       &lt;body&gt;
         &lt;p&gt;The World Wide Web, abbreviated as WWW and commonly known ...&lt;/p&gt;
       &lt;/body&gt;
     &lt;/html&gt;
     </code></pre>
     ```

     ```
     <pre><samp>
     GET /home.html HTTP/1.1
     Host: www.example.org
     </samp></pre>
     ```

8. `small`

   1. 表示字体缩小

      <small>小小小</small>

      ```<small>小小小</small>```

9. `s`

   1. 表示错误的内容,就是加上删除线

      <s>adasasdad</s>

      ```<s>adasasdad</s>```

10. `b`
    1. 表示为关键字
11. `var`
    1. 表示变量
12. `dl`,`dd`,`dt`
    1. 一般从出现在较为严肃的文章内,对一些术语进行定义
13. `main`
    1. 一个页面只出现一个,表示为页面的主要内容,可以理解为特殊的div



