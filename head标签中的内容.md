### head标签中的内容

> web-head

```html
<head>
  <meta charset="UTF-8">
  <title>关于head标签</title>
  <meta name="referrer" content="always">
  <meta name="renderer" content="webkit">
  <meta name="force-rendering" content="webkit">
  <meta http-equiv="X-UA-Compatible" content="ie=edge,chrome=1">
  <meta name="google-site-verification" content="Google随机生成的验证码">
  <meta name="description" property="og:description" content="关于网站的介绍">
  <meta name="keywords" content="网站关键字">
  <link rel="shortcut icon" type="image/x-icon" href="http路径或根目录 favicon.ico">  
  <link rel="dns-prefetch" href="预解析的域名">
  <!--[if lt IE 10]>
    <script>
        window.location.href = "提示不支持IE9及以下的浏览器或提示升级url";
    </script>
  <![endif]-->
</head>
```



> 移动端——head

``` html
<head>
  <meta charset="UTF-8">
  <title>关于head标签</title>
  <meta name="referrer" content="always">
  <meta name="renderer" content="webkit">
  <meta name="force-rendering" content="webkit">
  <meta http-equiv="X-UA-Compatible" content="ie=edge,chrome=1">
    
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0,user-scalable = 0">
  <meta name="format-detection" content="telephone=no,email=no" />
    
  <!--网站开启对 web app 程序的支持--> 
  <meta name="apple-mobile-web-app-title" content="标题"><!-- 添加到主屏后标题 iOS 6 新增 -->
  <meta name="apple-mobile-web-app-capable" content="yes">
    
  <!--设置x5内核屏幕全屏-->
  <meta name="x5-fullscreen" content="true"/>   
  <!--UC屏幕全屏-->
  <meta name="full-screen" content="yes">  
  
  <!--使用了application这种应用模式后，页面讲默认全屏，禁止长按菜单，禁止收拾，标准排版，以及强制图片显示。-->
  <meta name="browsermode" content="application">
    
  <!--X5内核(微信、qq)设置竖|横屏-->
  <meta name="x5-orientation" content="portrait|landscape"/>
  <!--UC-->
  <meta name="screen-orientation" content="portrait|landscape">
   
  <!-- windows phone 点击无高光 -->
  <meta name="msapplication-tap-highlight" content="no">
    
  <!-- iOS 图标  iPhone 和 iTouch，默认 57x57 像素，必须有-->
  <link rel="apple-touch-icon-precomposed" href="/apple-touch-icon-57x57-precomposed.png"/>
  <!-- Retina iPhone 和 Retina iTouch，114x114 像素，可以没有，但推荐有 -->
  <link rel="apple-touch-icon-precomposed" sizes="114x114" href="/apple-touch-icon-114x114-precomposed.png"/>
   
  <!--还有baidu-site-verification、360-site-verification、sogou_site_verification-->
  <meta name="google-site-verification" content="Google随机生成的验证码">
  <meta name="description" property="og:description" content="关于网站的介绍">
  <meta name="keywords" content="网站关键字">
  <link rel="shortcut icon" type="image/x-icon" href="http路径或根目录 favicon.ico">  
  <link rel="dns-prefetch" href="路径">
  <!--[if lt IE 10]>
    <script>
        window.location.href = "提示不支持IE9及以下的浏览器或提示升级url";
    </script>
  <![endif]-->
  <script>
     (function(){
        var Ohtml=document.getElementsByTagName('html')[0];
        var htmlW=Ohtml.getBoundingClientRect().width;   //获取设备的宽度
 
        Ohtml.style.fontSize=htmlW/15+'px';   //设置根节点的字体大小，即1rem
        //如上，若设计图中的宽为750px；取1rem=htmlW/15;则1rem=50px;
        //@rem:750/15rem;
    })();
</script>
</head>
```



#### meta标签 name

``` html
<meta name="generator" content="">用以说明生成工具（如Microsoft FrontPage 4.0）等；

<meta name="format-detection" content="telephone=no,email=no" />关闭电话号码、邮箱识别，一般用于移动端

<meta name="keywords" content="">向搜索引擎说明你的网页的关键词，搜索引擎优化；

<meta name="description" content=""> 告诉搜索引擎你的站点的主要内容；

<meta name="author" content="作者"> 告诉搜索引擎你的站点的制作的作者；

<meta name="referrer" content="always">  允许跳转后的页面获取该页面来源信息

<meta name="robots" content= "all|none|index|noindex|follow|nofollow">
```

-  定为all：文件将被检索，且页面上的链接可以被查询；

- 设定为none：文件将不被检索，且页面上的链接不可以被查询；

- 设定为index：文件将被检索；

- 设定为follow：页面上的链接可以被查询；

- 设定为noindex：文件将不被检索，但页面上的链接可以被查询；

- 设定为nofollow：文件将不被检索，页面上的链接可以被查询



```html
<!-- 强制Chromium内核，作用于360浏览器、QQ浏览器等国产双核浏览器 -->
<meta name="renderer" content="webkit"/>

<!-- 强制Chromium内核，作用于其他双核浏览器 -->
<meta name="force-rendering" content="webkit"/>

<!-- 如果有安装 Google Chrome Frame 插件则强制为Chromium内核，否则强制本机支持的最高版本IE内核，作用于IE浏览器 -->
<meta http-equiv="X-UA-Compatible" content="IE=Edge,chrome=1"/>

<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
```

> 关于viewport详解可以参考 ppk的三篇文章：[第一篇]("https://www.quirksmode.org/mobile/viewports.html" )、[第二篇]("https://www.quirksmode.org/mobile/viewports2.html")、[第三篇]("https://www.quirksmode.org/mobile/metaviewport/")；也可以参考 [博客]("https://blog.csdn.net/u012402190/article/details/70172371")



#### meta标签 http-equiv

```html
<meta http-equiv="Content-Type" content="text/html";charset="utf-8">
与<meta http-equiv="Content-Language" content="zh-CN"> 以说明主页制作所使用的文字以及语言；

<meta http-equiv="Refresh" content="n;url=http://yourlink">定时让网页在指定的时间n内，跳转到页面http://yourlink；
<meta http-equiv="Expires" contect="Mon,12 May 2020 00:20:00 GMT">可以用于设定网页的到期时间，一旦过期则必须到服务器上重新调用。需要注意的是必须使用GMT时间格式；

<meta http-equiv="Pragma" contect="no-cache">是用于设定禁止浏览器从本地机的缓存中调阅页面内容，设定后一旦离开网页就无法从Cache中再调出；
<meta http-equiv="set-cookie" contect="Mon,12 May 2020 00:20:00 GMT">cookie设定，如果网页过期，存盘的cookie将被删除。需要注意的也是必须使用GMT时间格式；

<meta http-equiv="Pics-label" contect="">网页等级评定，在IE的internet选项中有一项内容设置，可以防止浏览一些受限制的网站，而网站的限制级别就是通过meta属性来设置的；
<meta http-equiv="windows-Target" contect="_top">强制页面在当前窗口中以独立页面显示，可以防止自己的网页被别人当作一个frame页调用；

<meta http-equiv="Page-Enter" contect="revealTrans(duration=10,transtion= 50)">
与<meta http-equiv="Page-Exit" contect="revealTrans(duration=20，transtion=6)">设定进入和离开页面时的特殊效果，这个功能即FrontPage中的“格式/网页过渡”，不过所加的页面不能够是一个frame页面。
```



#### Open Graph Protocol

> 这种协议可以让网页成为一个“富媒体对象”，用了Meta Property=og标签，就是你同意了网页内容可以被其他社会化网站引用等，目前这种协议被SNS网站如Fackbook、renren采用。开放内容协议(Open Graph Protocol)，任何网页只要遵守该协议，SNS就能从页面上提取最有效的信息并呈现给用户。

``` html
<!--类型-->
<meta property=”og:type” content=”blog”/>

<!--标题-->
<meta property=”og:title” content=“Open Graph Protocol(开放内容协议)”/>

<!--图片-->
<meta property=”og:image” content=“图片url”/>

<!--链接-->
<meta property=”og:url” content=”页面url”/>

<!--视频链接-->
<meta property=”og:videosrc” content=””/>

<!--宽-->
<meta property=”og:width” content=”375″ />

<!--高-->
<meta property=”og:height” content=”667″ />
```



#### link标签

> dns-prefetch—DNS预解析技术
>
> ​	  DNS Prefetch 是一种DNS 预解析技术，当你浏览网页时，浏览器会在加载网页时对网页中的域名进行解析缓存，这样在你单击当前网页中的连接时就无需进行DNS的解析，减少用户等待时间，提高用户体验。目前支持 DNS Prefetch 的浏览器有 google chrome 和 firefox 3.5   

```html
<link rel="shortcut icon" type="image/x-icon" href="http路径或根目录 favicon.ico">  
<link rel="dns-prefetch" href="预解析的域名">
<link rel="stylesheet" type="text/css" href="引入外部样式文件.css"/> 
```



> ico
>
> 对于IOS的图标，icon属性无效，需使用 apple-touch-icon 和 apple-touch-startup-image 。另外rel="icon" 同时可以附加sizes="32x32"等属性，确保浏览器只会把目标图片解析成32x32的大小。当然，我们可以提供多种大小的图片，浏览器会自行选择最合适的图片。

```html
<link rel="apple-touch-icon-precomposed" sizes="57x57" href="apple-icon-114.png" type="image/png">
<link rel="icon" sizes="32x32" href="/favicon.ico" >
<link rel="icon" sizes="128x128" href="/favicon.ico" >      
```



> preload（预加载会让页面打开的视乎空白一段时间）
>
> preload可以预先加载如下这些资源， 并通过as属性指定如下这些资源类型，并通过type类型指定这些资源中的子资源，例如as="vedio" type="vedio/mp4"

```html
<link rel="preload" href="预加载.mp4" as="video" type="video/mp4">
<link rel="preload" href="预加载.mp4" as="image" type="image/png">

结合media根据不同的设备分辨率加载不同的资源
<link rel="preload" href="bg-image-narrow.png" as="image" media="(max-width: 600px)">
<link rel="preload" href="bg-image-wide.png" as="image" media="(min-width: 601px)">

```













