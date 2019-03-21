# HTML页面定时跳转代码总结

在我们做网页的时候，需要对网页进行跳转的操作。


## 1.html代码实现网页跳转

只需要在网页的头部也就是页面的head区域块内加上如下代码

```markup
//5秒钟之后跳转到幽水蓼蓝博客
<meta http-equiv="refresh" content="5;url=http://blog.lanhonghao.com" />
```


## 2.利用Js的setTimeout函数来实现网页的跳转

setTimeout() 方法用于在指定的毫秒数后调用函数或计算表达式

语法

```javascript
setTimeout(code, milliseconds, param1, param2, ...)
setTimeout(function, milliseconds, param1, param2, ...)
```
注：
code/function必需。要调用一个代码串，也可以是一个函数。
milliseconds可选。执行或调用 code/function 需要等待的时间，以毫秒计。默认为 0。
param1, param2, ...可选。 传给执行函数的其他参数（IE9 及其更早版本不支持该参数）。


网页跳转实现代码
```javascript
<script type="text/javascript"> 
//3秒钟之后跳转到幽水蓼蓝博客
    setTimeout(window.location.href = 'http://blog.lanhonghao.com', 3); 
</script>
```


## 3. 利用JS实现网页跳转，并给出提示

代码：

```javascript
<script type="text/javascript"> 
    var t = 10;//设定跳转的时间 
    setInterval("refer()", 1000); //启动1秒定时 
    function refer() {
        if (t == 0){
            location = "http://blog.lanhonghao.com"; //跳转的地址
        }
        document.getElementById('show').innerHTML = "" + t + "秒后跳转转到幽水蓼蓝博客"; // 显示倒计时 
        t--; // 计数器递减 
    } 
</script>
<span id="show"></span>
```
注：这种方式可以实现倒计时跳转

## 4.总结一下

上面说了三种可以跳转网页的方法，如果在一般项目中，只要使用第一种就可以了，而第三种可以输出倒计时时间的方法，多用于404页面。第二种方法，不推荐使用。