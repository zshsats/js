# javascript运行机制

1. 单线程：

   >因为js主要用途是与用户互动，操作dom，如果有两个线程，一个在某dom上添加，一个删除，此时浏览器就为难了。所以js同一时间只能做一件事，这就是单线程

2.  任务队列：

   >任务分两种：
   >
   >>同步任务：主线程上排队执行的任务，前一个任务结束，才会执行后一个任务
   >
   >>异步任务：不进入主线程、而进入"任务队列"的任务，只有"任务队列"通知主线程，某个异步任务可以执行了，该任务才会进入主线程执行。

3. 运行机制：

   >只要主线程空了，就会去读取"任务队列"，这就是JavaScript的运行机制。这个过程会不断重复。

4. js解析：

   >解析机制：js解释器在解析代码时，并不是一行行解析和执行的，而是一段一段地分析和执行程序，在程序段内，解释器会先预编译声明的变量和函数解构，只有当函数解析和执行完毕后，才会顺序执行其它代码行（段就是,<script>包含的脚本）

   * 编译阶段：

     >js解释器将js代码转化成字节码

   * 执行阶端：

     > js解释器借助执行期环境(例如：浏览器)，把字节码转换生成机械码，并按顺序执行

   ​