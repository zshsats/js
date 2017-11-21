# 浏览器渲染

1. 输入网址，浏览器向服务器发送请求，服务器返回html

2. 浏览器开始载入html代码，从上到下执行

3. 处理html构建DOM树

4. 若有css标记，则构建CSSDOM树

5. 将DOM和CSSDOM合并成一个渲染树

6. 根据渲染树布局，计算每个节点的几何信息

7. 将各个节点绘制到屏幕上

   ​

* 1）重排Reflow

> reflow：浏览器根据各种样式来计算并根据计算结果将元素放到它该出现的位置。

> 什么时候会触发Reflow，怎么避免Feflow

> 1）增加、删除、修改DOM节点时，会导致Reflow或Repaint

> 2）移动DOM的位置，会Reflow

> 3）修改CSS样式的时候，会Reflow

> 4）改变窗口或者滚动的时候可能会Reflow

> 5）修改网页默认字体的时候。

 

* 2）重绘Repaint

> repaint 页面要呈现的内容画在页面上。

> 什么时候会触发Repaint

> 1）DOM改动（代码片段）

> 2）CSS改动

