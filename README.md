前端技术库整合
======

##移动端

###Hammer.js 移动设备触摸手势js库
就几K，有机会试试  [点我](http://www.jingwentian.com/t-497 "不是官网")


##PC端

##通用

###normalize.css
reset样式  [点我](http://nicolasgallagher.com/about-normalize-css/ "normalize.css的官网")

##一些资源链接

[浅谈css框架开发](http://www.jingwentian.com/t-461)

##一些代码块

###JS快速获取图片宽高的方法
只要判断高度大于零
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