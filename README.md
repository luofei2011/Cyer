   <h2>Cyer</h2>是一个轻量、小巧的js框架，精简易懂的API设计，支持链式调用，有点jQuery的味道。核心部分为选择器(selector)、dom操作、event机制。

   参考jQuery的架构，API应该简洁易懂，且兼容主流浏览器Firefox、chrome、IE以及IE6+。全局对象使用美元符号$，在$(Cyer的简写)里调用一个初始化init构造函数并返回一个实例对象，以便实现链式调用。$对象包含原型方法(实例对象共享的方法)和全局函数(挂在$全局对象上的函数，也可称做静态方法)

   核心部分主要为selector(用于获取和遍历页面上的元素)、dom操作、event机制，暂不支持animate功能。具体实现请看源码，里面有详细的注释和说明。
  
  
<h2>v1.0.1</h2>版本增加的API：
一：对匹配元素追加或前置节点或HTML内容的方法；
二：对匹配元素进行移动和替换的方法；
三：插入一段HTML内容到匹配的元素或元素集合之前或之后；

主要API有：

（1）append
向匹配的元素内部追加节点或HTML内容(注意：追加的HTML内容或节点还是在该匹配元素内部，只不过是成为其最后一个子节点(当存在子节点时))。

（2）prepend
向匹配的元素内部前置节点或HTML内容(注意：前置的HTML内容或节点还是在该匹配元素内部，只不过是成为其第一个子节点(当存在子节点时))。

（3）before
把一个元素或HTML内容移动到匹配的元素之前。

（4）after
把一个元素或HTML内容移动到匹配的元素之后。

注：该四个API都返回实例对象，以便实现链式调用。

<h2>v1.0.2</h2>版本增加的API：
新增全局函数：$.IO
新增实例对象：$.io = new $.IO();
新增API：$.io.ajax()

修改的API：$.each()

introduction：
该API主要封装了一个浏览器与服务器端进行通讯的简单ajax实现，该方法接收一个对象参数，支持服务器响应成功后返回的数据格式有：text、html、xml。

usage：
因为该模块独立出来，使用前请先引入Cyer-1.0.2.js文件，再引入该ajax.js文件即可。

注意，测试时请在服务器端进行测试。



