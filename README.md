# day01
课堂笔记 例题

## U1课程主要分为三部分：
 **java基础阶段**
 
    配置java开发环境、HelloWorld案例
    数据类型 变量 常量 运算符 Scanner简单应用 数据类型互相转换
    条件语句
    循环语句
    数组
    
 **java面向对象阶段**
    类和对象概念、区别、定义语法
    方法定义、调用、使用细节
    封装、继承、多态、
    接口、异常
    
 **java高级部分**
    String、StringBuilder、StringBuffer
    Date、Calendar、SimpleDateFormat
    Math、Random、装箱和拆箱、包装类
    集合框架
    IO框架
    线程
    
    
  U1阶段考试：笔试+机试+面试

 上课要求：
   边讲边练，遇到不明白问题，在练习时可以提出
   作业，可以在练习阶段提出
 课程上完：
  
 课堂内容：
 JAVA遇到非常多的术语：
 JDK：java  development kits  java开发工具包，JDK包含JRE
 
 JRE:java Runtime environment java运行时环境，无需独立安装

 JDK1.0
 JDK1.5  新特性
 JDK1.6
 JDK1.7 ============== 教师机
 JDK1.8
 JDK1.9==》版本取消发布
 JDK10.0

 更新原则：高版本兼容低版本开发程序、低版本无法运行高版本程序。
 JDK安装：
 安装jdk时，需要按照源代码，便于学习。不需要安装jre
 JDK安装后的目录结构：

 基本DOS命令：
 bin下面所有的exe文件执行，基于dos窗口，运行
1、启动dos窗口 win键+r==>速度启动dos窗口
2、使用DOS切换路径
   2-1 同一盘符下面切换路径  cd 目标位置  jdk安装以后bin
   2-1 不同盘符切换路径
       切换盘符   盘符名称  回车 举例G: 回车
       进入指定目录，使用CD 目标位置
3、javac -version 回车，正常显示jdk安装版本。

注意：dos不区分大小写

## 二、配置path环境变量

  JDK里面提供程序员编写程序和运行程序工具。
  
  使用java语言编写java程序。体现文件格式.java，以java为后缀名的文件，称为源文件。
  计算机不能直接运行java源文件。
  使用javac.exe将java源文件编译成class字节码文件
  每一台计算机想运行class字节码文件，必须安装工具JVM---java virtual machine java虚拟机
  JVM不用独立安装，JRE包含JVM。为什么java程序跨平台，主要原因JVM支持各种操作系统
  
  计算机只认识0101数字序列
  计算机安装jvm可以运行class，通过java.exe运行程序。

     javac.exe
     java.exe

  所有软件只要在环境变量PATH配置，dos命令就可以自动搜索文件执行。
 实际开发一台计算机安装多个版本jdk，多个JDK互相切换。怎么切换不同版本？？？
 建议方案：
 把jdk的根目录配置成一个独立的变量，常用变量名java_home
 path环境变量中只需要书写%java_home%\bin完成java配置

## 三、写HelloWorld案例
  套用java书写的格式。
  开发步骤：
  1. java文件中。创建.java文件
  2. java文件中写代码：
  public class java文件文件名(大小写一模一样){
  	public static void main(String[] args){
		  System.out.print("Hello World");
	  }
  }
  3. 启动dos窗口，使用javac java源文件编译成class字节码文件
  4. java 运行class文件，查看效果

javac语法：
å  javac[.exe]  完整java文件名
  举例：javac Demo1.java
java语法：
  java[.exe] class文件名，不需要后缀
  举例：java Demo1
## 四、介绍书写代码大体意思
   
     1   public class Demo1{
     2	    public static void main(String[] args){
     3		    System.out.print("Hello World");
	  	        System.out.print("Hello World");
	          }
         }
    
1、java高级语言，面向对象语言。java组织代码一种结果
2、jvm识别执行位置一个标志。程序入口
3、向用户输出一段文字""引起文字

3行代码作用：输出信息，只要想输出内容，就可以重复编写第3行
System.out.print()只输出内容，不换行
换行：
 System.out.println()输出内容，并换行
转义符：
\n--- 换行
举例：
System.out.print("aaa\nbbb\nccc\ndddd\n")
\t--- 制表位符，相当于tab 一个\t等同8个空格
举例：
商品    单价   数量    总价
铅笔    1.2     10     12

## 五、取消代码不被jvm执行
注释：jvm不执行注释内容
java分类：
//：单行注释
作用：一行代码不想执行或对一行代码解释作用

/*  */:多行注释
作用：大篇幅代码注释不执行  或   编程思路或分析过程

/**  */:文档注释
作用：帮助手册

学生案例：
  输出以下结果：
  姓名    性别   年龄    学历     婚否
  张三    男     19      高中     未婚
  李四    男     54      初中     已婚


## 六、反编译工具的应用
反编译概念：将class文件转换为java文件。
意义：排错。JVM执行class文件可能与java源文件代码不一样。

使用步骤：
1、FontEnd plus,file→Decompile Class file→指向自己的class文件即可

总结：
1、掌握JDK环境安装及配置
2、JDK  JRE  JVM及三者之间的包含关系
3、print和println区别。\n \t作用用法
4、理解java程序注释的意义，注释分类

预习：
 数据类型、变量、常量定义语法 作用
 运算符分类、优先级
 Scanner的应用
 数据类型转换

 条件结构：
   if
   if-else
   多重if
   嵌套if
   switch-case

作业：

任务：
安装Eclipse工具











 



