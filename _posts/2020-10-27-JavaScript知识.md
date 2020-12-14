---
layout: page
title:  " JavaScript知识"
subtitle: "菜鸟上路"
date:   2020-09-16 21:21:21 +0530
categories: ["WEB基础知识"]
---

## JS基础介绍
### 环境（编译代码的工具）
- 浏览器内置的js解析模块----Javascript（前端唯一语言）
- node--- node.js（后端语言）
- 可以理解为两种语言
- 均基于ECMAscript语法 简称es

## 语法规范
- 如何在html中编写js
 - js代码要以<script type="text/javascript"></script>这对标签包着  代码都写在它们中间
  - text/javascript 可不写
 - 或者在外部建一个js文件  以.js为后缀名 再在html文件的head标签中引入js文件
  - 引入：<script src="你起的js文件名.js"></script>
  - 在外部的js文件不用写<script></script>标签包含

- js可以放在html中的任何位置（head ，body） 但一般浏览器解析时是按先后顺序执行的 所以在前面的js会先被执行
 - 一般进行`页面初始化的j`s必须放在`head`里面

## js变量
  - js的变量用var表示
  - js的变量是要先声明之后再赋值
  - 声明变量直接 `var` 变量名;
   - 1.变量必须使用字母、下划线(_)或者美元符($)开始。
   - 2.然后可以使用任意多个英文字母、数字、下划线(_)或者美元符($)组成。
   - 3.不能使用JavaScript关键词与JavaScript保留字。
  - 赋值 `变量名=你要赋的值`;
   - 可以重复赋值
   - 重复赋值之后会覆盖前面的值

  - 数据类型
  - 默认值--undefined
  - bool
  - Number
  - String
  - Array
   - `声明一个数组：var a = ["元素","不同的元素用逗号相隔"]`;
   - `遍历数组：for(var i=0; i<arr.length; i++) {}`
   - `取数据：a[0] key值`

  - Object (var a = {a:10; b: function() {}}) 值可以是任意类型
   - 声明对象: `var obj = {a: 10; b: function(){}, c: "asdsa"}`
   -  for (var i in obj) {}  用in
   - 获取对象下的某个字段值 对象名.对象下的字段名
   99
   -  obj.a
  - Function 

```html

<script>
var bianlinag;//声明一个变量名为bianliang的变量
bianliang=8;//为bianliang这个变量赋值 赋值8
bianliang=10;//重复赋值 覆盖之前的
docunment.write(bianliang);//第一次输出8 重复赋值刷新之后输出10  
</script>

```

## 代码执行逻辑
- 分支
- 循环(for)

## 复合数据类型的学习
- 声明
- 对元素的增 删 改 查（查看属性值）
- 遍历
- 常用的函数
- 字符串化与反字符串化

- 数组和对象都是复合类
  - 同类事物的集合的时候用数组 数组的key是有顺序的
  - 描述一位事物的时候用对象 


```javascript
//Array
//声明
var arr = ["1","2","3"];

//数组的增删改查
//增 只能在数组最后一位增 本来三位 0 1 2 加一位就要从3开始
arr[3] = "4";

//删

//改 需要改的数组key=需要改的数组value
arr[2] ="5";

//查 用一个变量保存你要查数组那个位置（key）的值
var temp = arr[1];

//遍历
for(var i = 0; i<arr.length; i++> ){
  console.log(i);
}

//object
var vbj = {
  shanggao: 175;
  tizhon: "48kg";
  fuse : white;
}

//对象的增删改查

//增
obj.age = 20;

//删
delete obj.tizhon;

//改 对象名.要改的key键 = 要改的值;
obj.fuse = "yellow";

//查 用一个变量保存 对象名.要查询的key
var temp = obj.fuse;

//遍历
for(var i in obj) {}

```

## 函数的封装
## 类与对象
## 常见的内置函数以及第三方常用的包

# 小程序要学的内容
## 数据绑定
- bingtap="函数名" js文件当中的page当中的函数名
## 数据渲染
## 事件绑定
## 生命周期


## js函数
- js声明一个函数和php一样使用 `function` 函数
- 声明一个函数 
 - `function 函数名(){}`
 - input 里的onclick字段是当按钮被点击是执行代码 参数可以是函数() 要加括号 
```html
<script>
function hanshu(){
  alert('欢迎光临！');//alert（弹窗） 显示带有一条指定消息和一个 OK（确认） 按钮的警告框。
}
hanshu();//调用函数 函数不能自动使用 所以要调用
//网页上会出现一个按钮 点击按钮会有个欢迎光临提示框
//onclick 当按钮被点击时执行Javascript代码 执行hanshu这个js函数内的功能
</script>
<input type="button"  value="点击我" onclick="  hanshu  " />  
```


```html

<body>
    <script>
    document.write("第一次学习js");
    </script>
</body>

```

### js 输出
- 数据显示 js中有不同的显示数据的方式
- `window.alert()` 写入警告框 
 - 警告框就是你打开网页 一个提示框会出来
 - windw是之前版本的写法 现在直接`alert()` 就行

- `document.write()` 写入html输出 直接在网页中输出内容
 - 例如：<p id="demo"></p>
 - document.getElementById("demo(设置好的id字段)").innerHTML=5+6; 输出11
 - 第一种:输出内容用""括起，直接输出""号内的内容。
  - document.write("你要输出的内容");
 - 第二种:通过变量，输出内容
  - var mystr="hello world!"; 
  - document.write(mystr); 会输出hello world 直接写变量名，输出变量存储的内容。
 - 输出多项内容，内容之间用+号连接。
  - var mystr="hello";
  - document.write(mystr + "你好");//输出hello 你好 内容之间用+号连接
  - document.write(mystr + "<br>");//输出hello 和一个换行符
- `innerHTML()` 写入HTML元素
- `console.log()` 写入浏览器控制台


### js弹出警告框（alert 消息对话框）

- 它是什么：我们在访问网站的时候，有时会突然弹出一个小窗口，上面写着一段提示信息文字。如果你不点击“确定”，就不能对网页做任何操作，这个小窗口就是使用alert实现的 就是弹出一个警告框

- alert(字符串或变量); 
 - alert弹出消息对话框(包含一个确定按钮)。
 - 如果有多个alert 则按它们定义的先后顺序弹出
 - 在点击alert的确定按钮时
 - 消息对话框通常可以用于调试程序。
 - alert输出内容，可以是字符串或变量，与document.write 相似。

 - 怎么实现点击按钮就弹出一个对话框
  - 在js中声明一个函数 
  - 然后在html中写一个input按钮 加一个onclick="函数名" 即可
```html
<script>
  function res(){
    var a = "这是弹出消息框";
    alert(a + "欢迎━(*｀∀´*)ノ亻!");
  }
</script>

<input name="a" type="button" value="点击我弹出对号框！" onclick = "res()" >

```


### js弹出确认框 (confirm 消息对号框) 
- confirm(参数：字符串)：参数字符串是在对话框中要显示的内容 
- 返回值：bool值 根据你在if判断定义的true区间和false区间输出代码
 - 当用户点击确定时返回true区间的代码
 - 当用户点击取消时返回false区间的代码
- 消息对话框是排它的，即用户在点击对话框按钮确定或取消前，不能进行任何其它操作。
```html
<script>
  function res() {
    var str =confirm("你觉得js好学吗");
    confirm(str);
    if(str == true) {
      document.write("好学" + "呢！");
    } else {
      document.write("不好学！");
    }
  }
</script>
  <input type = "button" value = "点击我" onclick = "res()">
```


### js弹出提问框(prompt 消息对话框)
- ``prompt``意义：弹出消息对话框,通常用于询问一些需要与用户交互的信息。弹出消息对话框（包含一个确定按钮、取消按钮与一个文本输入框）。
- ``prompt``(参数1，参数2);
 - 参数1：要显示在消息对话框中的文本，不可修改 就是弹出的对话框提示的内容
 - 参数2：显示在要输入的文本框的内容  就是文本框的默认值 就是默认输入的内容
 - 返回值:点击确定按钮，会返回的文本框的内容; 点击取消，将返回null
- 在点击对话框的按钮前（确定或取消），不能进行任何其他操作
```html
  <script>
    function hanshu() {
      var bianliang;
      bianliang=prompt("请输入你的年龄");
      if(bianliang >= 50) {
        alert("您已经步入老年");
      }else if(bianliang >=30 ) {
        document.write("您已经步入中年");
      }else if(bianliang>=18) {
        document.write("您好！青年人");
      }else {
        alert("未满十八岁可不能玩太久游戏哦！");
      }
    }
  </script>
```

### js打开新窗口(window.open)
- open() 方法可以查找一个已经存在或者新建的浏览器窗口。
- 语法：``window.open``(参数1：URL, 参数2：窗口名称, 参数3：参数字符串)
 - 参数：
 - ``URL``:可选参数，在窗口中要显示网页的网址或路径。如果省略这个参数，或者它的值是空字符串，那么窗口就不显示任何文档。
 - ``窗口名称``：可选参数，被打开窗口的名称。
  - 1.该名称由字母、数字和下划线字符组成。
  - 2.``_top``、``_blank``、``_self``具有特殊意义的名称。
   - _top：框架网页中在上部窗口中显示目标网页
   - _blank：在新窗口显示目标网页
   - _self：在当前窗口显示目标网页
  - 3.相同 name(参数2的值) 的窗口只能创建一个，要想创建多个窗口则 name 不能相同。
   - 参数2的值不能包含空格
 - ``参数字符串``：设置窗口参数，各参数用逗号隔开。
  - ``top``
   - 值：数字值
   - 说明：窗口顶部离开屏幕顶部的像素数px（窗口与顶部的边距）
  - ``left``:
   - 值：数字值
   - 说明：窗口左端离开屏幕左端的像素数(窗口与左边的边距) 也就是加上top这两个参数用来调整位置的
  - ``width``:要显示的窗口宽度
  - ``height``:要显示的窗口高度
  - ``menubar``:
   - 值：yes or no 只能选择这个两个
   - 说明：窗口需不需要显示菜单栏
  - ``toolbar``:
   - 值：yes or no 
   - 说明：窗口需不需要显示工具条
  - ``scrollbars``:
   - 值：yes or no
   - 说明：窗口需不需要显示滚动条
  - ``status``:
   - 值：yes or no
   - 说明：窗口需不需要显示状态栏
- 例如:打开打开http://www.baidu.com网站，大小为300px * 200px，无菜单，无工具栏，无状态栏，有滚动条窗口：
```html
<script type="text/javascript"> 
function Wopen() {
window.open('http://www.imooc.com','_blank','width=300,height=200,menubar=no,toolbar=no, status=no,scrollbars=yes')
}
    <input name="button" type="button" onClick="Wopen()" value="点击我，打开新窗口!" / >
</script>
```

### js关闭窗口(window.close)
- ``close()`` 关闭窗口
- 用法：
 - window.close(); 关闭本窗口
 - 打开的窗口(变量或网址).close();  关闭打开的窗口

- 例如:关闭新建的窗口。
```html
<script type="text/javascript">
   var mywin=window.open('http://www.imooc.com'); //将新打的窗口对象，存储在变量mywin中
   mywin.close();
</script>
```

### js通过id获取元素（ document.getElementById('要获取的id值') ）
- 网页由标签将信息组织起来，而标签的id属性值是唯一的，就像是每人有一个身份证号一样，只要通过身份证号就可以找到相对应的人。那么在网页中，我们通过id先找到标签，然后进行操作。
- 注:获取的元素是一个对象，如想对元素进行操作，我们要通过它的属性或方法。

### js innerHTML 属性
- innerHTML 属性用于获取或替换 HTML 元素的内容。
- 语法：Object（对象）.innerHTML = "要改变的内容"
 - 1.Object是获取的元素对象，如通过document.getElementById("ID")获取的元素。
 - 2.注意书写，innerHTML区分大小写。

```html
<h2 id="con">javascript</H2>
<p> JavaScript是一种基于对象、事件驱动的简单脚本语言，嵌入在HTML文档中，由浏览器负责解释和执行，在网页上产生动态的显示效果并实现与用户交互功能。</p>
<script type="text/javascript">
  var mychar=document.getElementById('con');           ;
  document.write("原标题:"+mychar.innerHTML+"<br>"); //输出原h2标签内容
  mychar.innerHTML="Hello Word!";
  document.write("修改后的标题:"+mychar.innerHTML); //输出修改后h2标签内容
</script>
```

## 改变html样式
- 语法：Object.style.property=new style;
 - Object:要改变的html元素对象 获取id的 如通过document.getElementById("id")获取的元素。
 - .style：必填字段
 - property：css属性表（color，backgroundColor，font-size，width，height等）
 - new style：你要改变的属性值（颜色，大小，宽度值等）
 - document.getElementById("id");

```html
<script>
<h2 id="con">I love JavaScript</h2>
  <p> JavaScript使网页显示动态效果并实现与用户交互功能。</p>
  <script type="text/javascript">
    var mychar= document.getElementById("con");
    mychar.style.color = red;
    mychar.style.backgroundColor = #CCC;
    mychar.style.width = 300px;
</script>
```

## 显示隐藏元素（object.style.display = none（或block））
- 网页中经常会看到显示和隐藏的效果，可通过display属性来设置。
- 语法：Object.style.display = value
- Object是获取的元素对象，如通过document.getElementById("id")获取的元素。
- style：必填
- display：必填
- value：none隐藏 block显示

## 控制类名className
- className 属性设置或返回元素的class 属性。
- 语法：object.className = classname
 - object：获取的对象（document.getElementById("id")获取的id）
 - .className:必填
 - classname:名字（你要修改的class选择器名）
- 作用：获取元素的class 属性
- 为网页内的某个元素指定一个css样式来更改该元素的外观