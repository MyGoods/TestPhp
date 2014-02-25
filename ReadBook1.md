认识PHP
=======


从现在起，将一切归零，好好学习php，天天向上不拖延！

###什么是PHP？
* 94年被Rasmus Lerdorf经历4次重新编写产出。
* php是一种服务器端的脚本语言，专为web设计的。
* 可以在html中嵌入php代码 <p><?php echo "Hello World" ?></p>
* php代码无需编译，被web服务器解析执行并生成html输出
* php是开源的，可免费使用和修改并再发布。
* 语法基于C和Perl
* php主页http://www.php.net
* php一般结合数据库Mysql一起使用 比较方便

###php与其他语言相比有哪些优势？
* 性能高 — 一个单独服务器可满足每天几百万次点击
* 可扩展性— 使用中经常会用到 比如Redis扩展，mysql扩展等等
* 有不同数据库系统接口— 不解释 你懂得
* 面对对象高度支持— 继承，抽象类和方法，构造函数，析构函数 不解释
* 成本低— 不解释
* 内置函数库丰富— 不解释 用了就知道
* 开发方法的灵活性— 不解释
* 源码可使用— 不解释 你懂得

###如何使用php？
    请看执行进度......
    
####php有4种标记

* 第一种XML风格

```php
<?php

echo 'Hello World!';

?>
```

* 第二种简短风格

```php
<?

 echo "hello world.";

?>
```

* 第三种script风格

```script
 <script language='php'>

    echo "hello world.";

</script>
```

* 第四种asp风格 要在配置中设置启用asp_tags选项，默认是禁用状态

```asp
<%
 
  echo "hello world.";

%>
```
