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
    
####1、php有4种标记
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

####2、php变量&&运算符
#####php变量
* php变量无需在赋值之前声明,使用时会自动声明
* 也不需要声明变量类型,是弱类型语言
* 变量名是$开始,eg:$var_test
* 注意命名规则
  变量名必须以字母或下划线 "_" 开头。<br/>
  变量名只能包含字母数字字符以及下划线。<br/>
  变量名不能包含空格。<br/>
 
ps:如果变量名由多个单词组成，那么应该使用下划线进行分隔（比如 $my_string），或者以大写字母开头。


#####运算符
* 算术运算符 注意++ -- eg:x=2;x++ 表示x=x+1 x=3。x--表示x=x-1;x=1
* 赋值运算符 注意x.y 表示x=x.y eg:x=a;y=b ;x=ab;
* 比较运算符 注意=== 双等和三等的区别在于 ===要比较变量的类型和数值但是双等只比较数值
* 逻辑运算符 与 或 非 你懂得

####3、Switch语句&&数组
#####Switch语句

```php
<?php

    //switch语句 用于执行基于多个不同条件的不同动作。
    //等同多个if...elseif...else,但比if else精简，清晰
    
switch($lan)
{
	case 3:
	echo "Java";
	break;
	
	case 1:
	echo "C语言";
	break;
	
	case 2:
	echo "Python";
	break;
	
	default:
	echo "PHP";
	
}
 
?>
```
#####Array
* 数值数组,会自动分配数值ID键或人工分配关联ID

```php
<?php
	
	//自动分配ID键
	$ApplePros = array("Mac Air","Mac Pro","iPhone","Ipad","Ipod");
	
	//人工分配ID键
	$ApplePro[0] = "Mac Air";
	$ApplePro[1] = "Mac Pro";
	$ApplePro[2] = "iPhone";
	$ApplePro[3] = "Ipad";
	$ApplePro[4] = "Ipod";
	
	//访问页面输出
	echo "自动分配ID键: ".$ApplePros[0]."<br/>";
	echo "人工分配ID键: ".$ApplePro[2];
	
?>
```
* 关联数组,每个ID键关联一个值

```php
<?php
	
$ApplePros =array(
	
	"MacAir" =>"7k",
	"MacPro" =>"1.2W",
	"iPhone" =>"4K~5.5K",
	"Ipad" =>"2.8K~4.5K",
	"Ipod" =>"1K~3K"
);
echo $ApplePros["Ipad"];

//另一种关联键的表现,区别于数值数组的自动分配ID键，自动分配数值ID是分配数组的下标数值；关联数组的键值可以是关联字符键值
$ApplePro["MacAir"] = "7k";
$ApplePro["MacPro"] = "1.2W";
$ApplePro["iPhone"] ="4K~5.5K";
$ApplePro["Ipad"] ="2.8K~4.5K";
$ApplePro["Ipod"] ="1K~3K";
echo $ApplePro['MacAir'];

?>
	
	
```
* 多维数组,主数组中的每个元素也是一个数组。在子数组中的每个元素也可以是数组.也就是 数组中嵌数组

```php
<?php

$ApplePros = array
(
	
	"MacPC" =>array
		(
			"MacBookPro",
			"MacBookAir",
			"Mac mini",
			"iMac"
		),
	"iPhone" =>array
		(
			"iPhone",
			"iPhone 3G",
			"iPhone 3G S",
			"iPhone 4",
			"iPhone 4S",
			"iPhone 5",
			"iPhone 5C",
			"iPhone 5S"
		),
	"iPad" =>array
		(
			"iPad2",
			"iPad3",
			"iPad4",
			"iPad Mini",
			"iPad Mini2",
			"iPad Air"
		)
	
);

//将数组结构打印出来,可知是个3元2维数组
print_r($ApplePros)."<br/>";

//获取数组的值
echo "My PC IS: ".$ApplePros['MacPC']['1'];

?>
```
    
