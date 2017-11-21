# 跨域

>同源策略：
>
>定义：
>
>>相同域名、端口、和协议，若这三个相同则视为同一个域，本域下的js脚本只能读写本域下的数据资源，无法访问其它域的资源
>
>
>
>>浏览器为了保护用户的个人信息以及企业数据的安全而设置的一种策略
>
>跨域：
>
>>解决同源策略带来的不便，突破同源策略的限制去获取不同源之间的数据信息或者进行不同源之间的信息传递。
>
>方式：
>
>* jsonp
>
>  >原理：
>  >
>  >在页面上引入不同域上的js脚本文件却是可以的，jsonp正是利用这个特性来实现的
>  >
>  >例如：
>  >
>  >前台：
>  >
>  >```
>  ><script>
>  >	function calname(data){
>  >      	//对json数据进行梳理
>  >	}
>  ></script>
>  ><script src="url?name=zsh&callback=calname"></script>
>  >```
>  >
>  >后台：
>  >
>  >```
>  ><?php
>  >	//通过get获得url中参数name和callback
>  >	$name = $_GET['name];
>  >	$callback = $_GET['callback'];
>  >	$data = {
>  >      //后台处理请求后响应数据
>  >	};
>  >	//输出
>  >	echo $callback.'('.json_encode($data).')';
>  >```
>  >
>  >结果
>  >
>  >```
>  >calname中data={
>  >  //$data后台响应的数据
>  >}
>  >```
>  >
>  >缺点：
>  >
>  >1、安全性：一旦jsonp的服务存在页面注入漏洞，返回的js内容可能被人控制，无法把危险控制在一个域名下，所以在使用jsonp的时候必须要保证使用的jsonp服务必须是安全可信的。
>  >
>  >2、jsonp在调用失败的时候不会返回各种HTTP状态码。
>  >
>  >3、只能get请求
>  >
>  >4、不能解决不同域的两个页面之间如何进行Js调用的问题
>
>* CROS
>
>  >定义：全称：跨域资源共享，它允许浏览器向跨源服务器，发出XMLHttpRequest请求，从而克服了AJAX只能同源使用的限制。
>  >
>  >原理：
>  >
>  >在请求页面上使用Access-Control-Allow-Origin标头。
>  >
>  >　　使用如下标头可以接受全部网站请求：
>  >
>  >header('Access-Control-Allow-Origin:*')
>  >
>  >　　使用如下标头可以接受指定网站请求：
>  >
>  >header('Access-Control-Allow-Origin:*url*')
>  >
>  >​
>
>  ​
>
>  ​