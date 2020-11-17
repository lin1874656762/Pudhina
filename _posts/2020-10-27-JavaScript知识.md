---
layout: page
title:  "学习 js"
subtitle: "菜鸟上路"
date:   2020-09-16 21:21:21 +0530
categories: ["WEB基础知识"]
---


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

```html

<script>
var bianlinag;//声明一个变量名为bianliang的变量
bianliang=8;//为bianliang这个变量赋值 赋值8
bianliang=10;//重复赋值 覆盖之前的
docunment.write(bianliang);//第一次输出8 重复赋值刷新之后输出10  
</script>

```

## js函数
- js声明一个函数和php一样使用 `function` 函数
- 声明一个函数 
 - `function 函数名(){}`

```js
function hanshu(){
  alert('欢迎光临！');//alert（弹窗） 显示带有一条指定消息和一个 OK（确认） 按钮的警告框。
}
hanshu();//调用函数 函数不能自动使用 所以要调用
//网页上会出现一个按钮 点击按钮会有个欢迎光临提示框
//onclick 当按钮被点击时执行Javascript代码 执行hanshu这个js函数内的功能
<body>
 <form>
      <input type="button"  value="点击我" onclick="  hanshu  " />  
   </form>
</body>

```


```html

<body>
    <script>
    document.write("第一次学习js");
    </script>
</body>

```

## js 输出
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