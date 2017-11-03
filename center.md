### 今天2017年11月3日 星期五 
### Great来和大家分享一下开发中遇到 如何让 一段文字在在一张图片上 上下左右垂直居中 方法
### 首先图片和这段文字并列关系，外面嵌套一个div，然后给文字设置transform translate属性
### 及绝对定位，然后再给外面的div设置相对定位 然后就ok啦，代码参考如下：
 ```
  <style>
        .a{
            position: relative;
            text-align: center;
        }
        .a img{
            width: 70%;
        }
        .a .titck_num{
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%,-50%);
            font-size: 25px;
            color: white;
        }
    </style>

    <div class="a">
        <img src="./images/ac_ticket2.png" alt="">
        <div class="titck_num">TX2123214</div>
    </div>

    ```
```
如果让一个遮罩层和图片在页面上，图片上下左右垂直居中，同样是遮罩层和图片也是并列
的关系，然后给图片设置transfrom属性，加fixed属性，然后给遮罩层加fixed属性就ok了

```