前端技术库整合
======

##移动端

####1.Hammer.js 移动设备触摸手势js库
就几K，有机会试试  [点我](http://www.jingwentian.com/t-497 "不是官网")
####2.fullpage
其实桌面端也可以用  [点我](https://github.com/powy1993/fullpage)
####3.snap scroll
在移动端开发用过，但是感觉没有fullpage的可扩展性高  [点我](https://github.com/baofen14787/zepto-SnapScroll)
####4.iSlider
移动端幻灯片多种模式  [点我](https://github.com/BE-FE/iSlider)

##PC端

####1.One Page Scroll
PC端开发使用过，兼容移动端  [点我](https://github.com/peachananr/onepage-scroll)
####2.Beetle
一个响应式HTML5模版  [点我](http://mokaine.com/beetle-free-html/)
####3.fullpage
跟上面的移动端那个不一样  [点我](http://www.dowebok.com/77.html)
####4.360度产品展示
PC端的优化估计要用到  [点我](https://github.com/creativeaura/threesixty-slider)
####5.bxslider
一个强大的幻灯片  [点我](http://bxslider.com/)

##通用

####1.normalize.css
reset样式  [点我](http://nicolasgallagher.com/about-normalize-css/ "normalize.css的官网")
####2.CSS媒体查询
自适应必备良药  [点我](https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Media_queries)

##字体
####Font 屌

##工具
####1.weinre调试
移动开发必备  [点我](http://qing.blog.sina.com.cn/tj/63fc66e0330010y2.html)
####2.移动设备参数
做个参考  [点我](http://screensiz.es/phone)
####3.bower
包管理工具  [点我](http://blog.fens.me/nodejs-bower-intro/)
[官网](http://bower.io/)
####yeoman
管理流程  [点我](http://yeomanjs.org/)


##一些资源链接

[浅谈css框架开发](http://www.jingwentian.com/t-461)

##一些代码块

####JS快速获取图片宽高的方法
只要判断高度大于零
```
    // 图片地址
    var img_url = 'http://www.qttc.net/static/upload/2013/13643608813441.jpg?'+Date.parse(new Date());
    // 创建对象
    var img = new Image();
    // 改变图片的src
    img.src = img_url;
    // 定时执行获取宽高
    var check = function(){
        document.body.innerHTML += 'from:check : width:'+img.width+',height:'+img.height;
    };
    var set = setInterval(check,40);
    // 加载完成获取宽高
    img.onload = function(){
        document.body.innerHTML += 'from:onload : width:'+img.width+',height:'+img.height;
        // 取消定时获取宽高
        clearInterval(set);
    };
```