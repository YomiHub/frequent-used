### reset.css清除默认样式

#### web_reset

```css
body,ul,p,h1,h2,h3,h4,dl,dd,form,input,select { padding:0; margin:0;}

li {list-style: none;}

img {border: none; vertical-align:top;} 

body{font-size:14px; color: 1a1a1a; font-family:-apple-system,BlinkMacSystemFont,Helvetica Neue,PingFang SC,Microsoft YaHei,Source Han Sans SC,Noto Sans CJK SC,WenQuanYi Micro Hei,sans-serif;}

a {text-decoration: none;}

a:hover {text-decoration: none;}

input {background: none; border: none; outline: none;}
```



#### 移动端_reset

```css
/* 在上述的web-reset的基础上清除移动端的默认样式 */
a,input,button{ -webkit-tap-highlight-color:rgba(0,0,0,0); }  /*除去点击高亮*/

input,button{ 
    -webkit-appearance:none; -moz-appearance: none; appearance: none; 
    border-radius: 0; 
}

body{ font-family:Helvetica;}  /*所有设备都有的英文字体，中文有什么就用什么字体*/
body *{ margin:0; -webkit-text-size-adjust:100%; } /*禁止用户在横竖屏时缩放、设置字体大小*/
body *{ 
    -webkit-user-select:none;-moz-user-select:none;-o-user-select:none;
	user-select:none;
} /*设置文字不可选中,在部分手机中不起作用，可以在事件中解决*/
```



