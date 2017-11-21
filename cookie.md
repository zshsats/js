# cookie

> 定义：
>
> >cookie是浏览器提供的一种机制，它将document对象的cookie属性提供给JavaScript。可由JavaScript对其进行控制，而并不是JavaScript本身的性质。cookie是存于用户硬盘的一个文件，这个文件通常对应于一个域名，当浏览器再次访问这个域名时，便使这个cookie可用。因此，cookie可以跨越一个域名下的多个网页，但不能跨越多个域名使用。 
>
> 存储位置：
>
> >将信息存储在用户硬盘，可以作为全局变量
>
> 设置：
>
> > 每一个cookie都是一个名/值对,可以将这样的字符串复制给docume.cookie,如果要复制多对，这中间加上分号;.
> >
> > 例如：document.cookie="name=zsh;id=1";
>
> cookie和web storage的区别：
>
> 1. web storage 容量大，存储在本地，cookie大小受限
>
> 2. web storage有自己的方法，cookie需要自己封装
>
> 3.  请求一个新页面时，cookie都会被发送，浪费了带宽
>
> 4.  cookie需要指定作用域，不可跨域调用
>
>    ​
>
> cookie的特色：
>
> >cookie虽然有很多缺点，但重要的是：cookie的作用是与服务器进行交互，作为http规范的一部分而存在，web storage只是为了本地存储。
>
> 





