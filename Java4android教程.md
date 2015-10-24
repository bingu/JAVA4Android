# Java For Android 教程

## **第一章 开发环境**

### 一 Java SDK 下载与安装

[Oracle 官网](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

### 二 什么是环境变量

1. 环境变量通常是指在操作系统当中，用来指定操作系统运行时需要的一些参数；
2. 环境变量通常为一系列的 **键值对** ；

### 三 Path 环境变量的作用

1. Path 环境变量是操作系统外部命令搜索路径

### 四 classpath 环境变量的作用

1. classpath 环境变量是类文件搜索路径
2. 键值对 classpath - "." 表示当前文件夹下

### 五 JDK里面有什么？

1. bin 文件夹：所有 Java 用到的命令 javac：编译命令 java：运行命令
2. demo 和 sample 文件夹：Java例子
3. include：C语言程序
4. jre 文件夹：java运行时环境
5. lib 文件夹：java所需要的包文件
6. src 压缩包：java JDK一部分源文件

### 六 什么是JRE

JRE是Java Runtime Environment，即 Java 运行环境，包括以下的几个部分：

1. Java 虚拟机；
2. Java 平台核心类文件；
3. 其他支持文件；

## **第二章 Java 编程基础**

### 一 Java 数据类型

#### 1 什么是变量

#### 2 变量的声明办法

变量类型 变量名;

	int age;

#### 3 变量有哪些类型

1. 基本数据类型：数值型（整数类型，浮点类型）、字符型（char）、布尔型（boolean）
2. 引用数据类型：类（class）、接口（interface）、数组

#### 4 变量的赋值

变量类型 变量名 赋值号 变量值 ;

	int age = 20 ;

#### 5 变量的命名规范

1. 变量名语法归法
+ 应该以字符、下划线或者美元符开头；
+ 后边跟字母、下划线、美元符或者数字；
+ Java 变量名没有长度限制；
+ Java 变量名对大小写敏感
2. 驼峰命名发
+ 变量名应该用有意义的英文单词；
+ 变量名如过只有一个单词，则又有字母小写；
+ 变量名如果由多个英文单词组成，则从第二个单词开始首字母大写；

#### 6 布尔型变量

1. boolean 类型适用于逻辑运算，一般用于承诺工序流程控制
2. 在 Java 当中的 boolean 类型只有两种取值： true 和 false；
3. 不能用0和非0，或者空和非空来表示；

#### 7 字符型变量

char 类型数据用来表示通常意义上的字符；

1. 字符是由单引号包括起来的单个字符

	char c = 'a';
	char b = '中';

2. Java 字符使用 Unicode 字符集；
3. Unicode 字符集为每种语言的每个字符设定了统一并且唯一的二进制码；
+ Unicode 满足了跨语言文本转换和处理的需求；
+ Unicode 在互联网当中扮演着非常重要的角色；
+ unicode 使用数字0-0x10FFFF来表示字符；
+ 最多允许有1114112个字符

#### 8 数值型变量

数值型变量分为两大类

1.	整数类型：
	+ byte		1字节 -128  ~ 127
	+ short		2字节 -2^15 ~ 2^15-1
	+ int		4字节 -2^31 ~ 2^31-1
	+ long		8字节 -2^63 ~ 2^63-1
2.	浮点类型：
	+ float		4字节 -3.403E38  ~ 3.403E38
	+ double	8字节 -1.798E308 ~ 1.798E308

#### 9 整数类型

1.	Java 语言整型常量的三种表示形式；
	+ 十进制整数，如12，-313，0
	+ 八进制整数，要求以0开头，如012
	+ 十六进制数，要求以0x或0X开头，如0x12
2.	Java语言的整形常量默认为 int 型，如
	int i = 3 ;
3.	声明 long 常量 可以后加‘l’或‘L’,如
	long l = 3L ;

#### 10 浮点类型

### 二 Java 运算符与表达式

#### 1 运算符

+ 算数运算符：+ - * / % ++ --
+ 关系运算符：> < >= <= == !=
+ 逻辑运算符：! & | ^ && ||
+ 位运算符：  & | ^ ~ >> << >>>
+ 赋值运算符：=
+ 扩展赋值运算符：+= -= *= /=
+ 字符串连接运算符：+

逻辑晕算法：

	!——逻辑非 &——逻辑与 |——逻辑或
	^——逻辑异或 &&——短路与 ||——短路或

#### 2 表达式的类型和值

表达式：是符合一定语法规则的运算符和操作符的序列：

	i
	10.5+i
	(i+j)-2

表达式的值：对表达式中操作数进行运算得到的结果成为表达式的值

表达式的类型：表达式的值的数据类型即为表达式的类型


### 三 分支语句

#### 1 程序流程的分类

1. 顺序结构
2. 分支结构
3. 循环结构

#### 2 if……else结构

语法结构

	if(逻辑表达式){
		语句;
		语句;
	}
	else if(逻辑表达式)｛
		语句;
		语句;
	｝
	else{
		语句;
		语句;
	}


#### 3 Switch结构

语法结构

	switch(表达式){
		case 常量1:
			语句;
			break;
		case 常量2:
			语句;
			break;
		default:
			默认语句;
			break;
	}

### 四 循环语句

#### 1 for 循环语句

#### 2 while 循环语句

### 五 函数的定义方法

## **第三章 面向对象基础**

终极目标：**消除程序中的重复代码**

**基本概念**

面向对象程序设计中的概念主要包括：对象、类、数据抽象、继承、动态绑定、数据封装、多态性、消息传递。通过这些概念面向对象的思想得到了具体的体现。

1. 对象 对象是运行期的基本实体，它是一个封装了数据和操作这些数据的代码的逻辑实体。
2. 类 类是具有相同类型的对象的抽象。一个对象所包含的所有数据和代码可以通过类来构造。
3. 封装 封装是将数据和代码捆绑到一起，避免了外界的干扰和不确定性。对象的某些数据和代码可以是私有的，不能被外界访问，以此实现对数据和代码不同级别的访问权限。
4. 继承 继承是让某个类型的对象获得另一个类型的对象的特征。通过继承可以实现代码的重用：从已存在的类派生出的一个新类将自动具有原来那个类的特性，同时，它还可以拥有自己的新特性。
5. 多态 多态是指不同事物具有不同表现形式的能力。多态机制使具有不同内部结构的对象可以共享相同的外部接口，通过这种方式减少代码的复杂度。
6. 动态绑定 绑定指的是将一个过程调用与相应代码链接起来的行为。动态绑定是指与给定的过程调用相关联的代码只有在运行期才可知的一种绑定，它是多态实现的具体形式。
7. 消息传递 对象之间需要相互沟通，沟通的途径就是对象之间收发信息。消息内容包括接收消息的对象的标识，需要调用的函数的标识，以及必要的信息。消息传递的概念使得对现实世界的描述更容易。
8. 方法 方法（Method）把执行的代码整合在一个方法中，当需要做这些动作的时候直接通过调用这个方法而达到使用的目的。


### 一 面向对象与面向过程语言之间的区别

#### 1. 什么是面向对象？

1. 面向对象是一种变成方法；
2. 面向对象是一种思维方式；
3. 面向对象不是一种编程语言。

#### 2. 如何学习面向对象？

1. 掌握一门面向对象语言的语法；
2. 掌握面向对象的思维方式；
3. 熟悉面向对象设计原则
4. 掌握面向对象设计模式

#### 3. 什么是面向对象思维方式？

1. 首先确定谁来做，其次确定怎么做；
2. 首先考虑整体，其次考虑局部；
3. 首先考虑抽象，其次考虑具体。

### 二 类

#### 1. 创建类的方法

定义类的方法

	class className{
		属性;
		方法;
	}

+ 属性也叫成员变量，主要用于描述类的状态
+ 方法也叫成员方法，主要用于描述类的行为

类的表示方法

类名：
成员变量：
成员方法：

类的实例：

	class Person{
		int age;
		void shout(){
			System.out.println("oh, my god! I am " + age);
		}
	}

#### 2. 生成对象的方法

格式：ClassName objectiveName = new ClassName()

例如：

	Dog dog = new Dog();

类和对象的关系

类是抽象的
对象是具体的

#### 4. 对象的使用方法

使用对象调用变量和方法——“.”

1. 对象.成员变量
2. 对象.成员方法()

例如：

	Dog dog = new Dog();
	dog.name  = "Wang Cai ";
	dog.age   = 2;
	dog.color = "black";
	d.jump();


#### 5. 多对象的创建方法

使用 new + 构造函数来创建新的对象。

	Dog d1 = new Dog();
	Dog d2 = new Dog();

#### 6. 匿名对象的创建和使用方法

可以不定义对象的引用名称，而直接调用这个对象的方法。这样的对象叫做**匿名对象**。

	new Dog().jump();

匿名对象通常都是一次性的。


### 三 函数的重载

#### 1. 函数的重载

在一个类中，允许函数的重名这种情况的出现，这中现象叫**函数的重载**。

例如：

	class A{
		void funA(){
			System.out.println("没有参数的funA函数")；
		}
		void funA(int i){
			System.out.println("拥有一个整形参数的funA函数")；
		}
	}

构成函数重载的定义标准：

1. 两个或多个函数处于同一个类当中；
2. 函数名相同；
3. 各函数的参数列别不同。

调用类的函数时，通过传输的不同参数来区别具体使用了哪个函数。
作用为根据操作参数的不同而执行不同的代码。

#### 2. 构造函数

构造函数是一种特殊的方法，主要用来在创建对象时初始化对象。即为对象成员变量赋初始值，总与new运算符一起使用在创建对象的语句中。特别的一个类可以有多个构造函数，可根据其参数个数的不同或参数类型的不同来区分它们，即**构造函数的重载**。

构造函数的特征：

1. 构造函数没有返回值类型；
2. 构造函数的名字必须和类名相同；
3. 当类中没有构造函数的情况下，编译器在编译代码时，会默认添加无参数且方法体为空的构造函数；
4. 当类中有构造函数的情况下，编译器不会再添加默认构造函数。

主要作用：

1.  使用new+构造函数生成一个对象；
2.  自行编写构造函数，来简化为成员变量赋初始值的代码。

### 四 this 关键字的作用

#### 1. 使用this调用成员变量和成员函数

	class Person｛
		String name;
		void talk(){
			System.out.println("my name is" + this.name);
		}
	｝

上面的this可以省略。

	class Person{
		String name;
		void talk(String name){
			System.out.println("my name is " + name);
		}
	}

上面的方法体中的name是调用传入的参数，如想使用成员变量的name，则需如修改：

	class Person{
		String name;
		vodi talk(String name){
			System.out.println("my name is " + this.name);
		}
	}

this起到区分成员变量和参数的作用。

#### 2. 使用this调用构造函数

**对this的调用必须是构造函数的第一个语句**

this();

	class Person｛
		String name;
		int age;
		String adress;
		Person(){
			System.out.pringln("无参数构造函数");
		}
		Person(String name, int age){
			this();
			this.name = name;
			this.age = age;
			//前者是调用成员变量，后者是传入的参数
			System.out.println("两个参数的构造函数");
		}
		Person(String name, int age, String address){
			this(name,age);
			//根据参数的个数和类型调用本类中相应的其他构造函数，
			this.address = address;
			System.out.println("三个参数的构造函数");
		}
		void talk(){
			System.out.println("my name is" + this.name);
		}
	｝

### 五 static 关键字的作用

static关键字的作用：

1. 定义静态成员变量；
2. 定义静态函数；
3. 定义静态代码块。

#### 1. 静态成员变量的语法特点

用法：在成员变量数据类型名前加**static**关键字
class Person:

	class Person{
		static int i;
	}

class Test:

	class Test｛
		Public static void main(String args []){
			Person.i = 10;
		}
	｝

1. 静态成员变量可以不生成对象而直接使用类名调用；
2. 静态成员变量在所有此类的对象中都使用同一个值，一个对象进行修改，所有的对象都会进行改变。

#### 2. 静态函数的语法特点

用法：在函数返回值类型名前加**static**关键字

class Person:

	class Person{
		static int i;
		static void fun(){
			System.out.println("我是静态函数");
		}
	}

class Test:

	class Test｛
		Public static void main(String args []){
			Person.fun();
		}

1. 静态函数可以不生成对象而直接使用类名调用；
2. 不能在静态函数中引用非静态的变量。

#### 3. 静态代码块的语法特点

用法：在代码块前加static关键字

	class Person{
		static{
			System.out.println("静态代码块");
		}
		static int i;
		static void fun(){
			System.out.println("我是静态函数");
		}
	}

1. 静态代码块在装载类时执行，就是只要执行这个类就会执行静态代码块。
2. 主要作用是为静态成员赋初始值。

## **第四章 面向对象高级**

面向对象的三个特征：继承、封装、多态。

### 一 继承

#### 1. 什么是继承？

在面向对象的世界当中，继承就是一个类得到了另一个类当中的成员变量和成员方法。

**Java中只支持单继承**，即一个子类只允许继承一个父类，但一个父类可以拥有多个子类。

class Person

	class Person{
		String name;
		int age;
		void eat(){
			System.out.println("吃饭");
		}
		void introduce(){
			System.out.println("我的名字是" + name + "，我的年龄是" + age);
		}
	}

class Student

	class Student extends Person{
	}

用法，在定义子类时，在子类名后加 extends 关键字 和父类名。

子类中还可以加入自身特有的成员变量和成员方法。

class Student

	class Student extends Person{
		int grade;
		void study(){
			System.out.println("学习");
		}
	}

#### 2. 为什么要使用继承

1. 将各子类中共同的成员变量和成员方法集中到父类中，减少重复代码；
2. 方便集中修改代码。



#### 3. 继承的基本语法特点

1. 子类继承父类的成员变量和成员方法。
2. 子类中添加自身特有的成员变量和成员方法。

### 抽象类和抽象函数

#### 1. 抽象函数的语法特征
1.什么是抽象函数
抽象函数就是只有函数的定义，没有函数体的函数。例如：

	abstract void fun();

abstract 为抽象函数的关键字。

函数的定义：返回值类型，函数名和参数列表这三部分组成了函数的定义。
函数体：函数体为大括号及大括号里的内容。

class Person:

	class Person{
		String name;
		int age;

		void introduce(){
			System.out.println("我的名字是" + name + "，我的年龄是" + age);
		}

		abstract void eat();
	}

注：上述代码编译将出错。原因见下面讲解。

#### 2. 抽象类的语法特征
当类当中拥有抽象函数，则该类也必须定义为抽象类。

1. 什么是抽象类

	使用 abstract 定义的类被称之为抽象类

2. 抽象类的语法特征

	* 抽象类不能够生成对象；

		也就是不能调用这个类的构造函数来生成对象

	* 如果一个类当中包含有抽象函数，这个类必须被声明为抽象类；

	* 一个类当中没有包含抽象函数，这个类也可以被声明为抽象类。

如上例则可以通过在类定义的前面添加 abstract 关键字使该类定义为抽象类来通过编译

Person.java

	abstract class Person{
		String name;
		int age;

		void introduce(){
			System.out.println("My name is " + this.name + ", I'm " + this.age +
				" years old.");
		}

		abstract void eat();
	}

这时编译顺利通过。现在写个主函数来尝试调用上面的 Person 抽象类

Test.java

	class Test{
		 public static void main(String args []){
			 Person p = new Person();
		 }
	}

当编译 Test.java 时，编译将出现错误。这很好的说明不能调用一个抽象类的构造函数来生成一个
对象。

为什么不能调用抽象类生成对象？

如果抽象类能生成对象，则意味着该对象也将会调用其中的抽象函数，而抽象函数是没有函数体的，这也
将导致该调用的失败。所以不能调用抽象类来生成对象。

#### 3. 抽象类的作用

抽象类也称为基类，它只能作为父类被子类继承。在子类中需复写抽象类中的抽象函数，以便子类在继承
抽象类中的抽象函数后无需声明为抽象类。如

Chinese.java

	class Chinese extends Person{
		void eat(){
			System.out.println("用筷子吃饭");
		}
	}

将主函数修改为

Test.java

	class Test{
		public static void main(String args[]){
			Person person = new Chinese();
			person.eat();
		}
	}

此时编译顺利通过。

#### 4. 抽象类可以有构造函数吗？

如上所述，抽象类不能生成对象，而构造函数是用于生成类的对象的。那么抽象类可以有构造函数吗？

答案是抽象类也是有构造函数的。而且子类的构造函数同样会调用抽象父类的构造函数。

### 为什么要用抽象类？

抽象类的使用场景：

1. 子类具有的方法，且实现的方法内容不尽相同；

2. 父类采用抽象函数，可避免子类未对该函数进行覆写；

Printer.java

	abstract class Printer{
		void open(){
			System.out.println("Open");
		}

		void close(){
			System.out.println("Close");
		}

		abstract void print();
	}

HPPrinter.java

	class HPPrinter extends Printer{
		void print(){
			System.out.println("Use HP Printer");
		}
	}

CanonPrinter.java

	class CanonPrinter extends Printer{
		void print(){
			System.out.println("Use Canon Printer");
		}
	}

Test.java

	class Test{
		public static void main(String args[]){
			Printer p1 = new HPPrinter();
			p1.open();
			p1.print();
			p1.close();

			Printer p2 = new CanonPrinter();
			p2.open();
			p2.print();
			p2.close();
		}
	}

## **包和访问权限**

### 软件包简介

* 软件包为 JAVA 类提供了命名空间，可以看成用不同的文件夹放置程序
* 打包须在程序的首行使用 package 指令；
* 一个类的全名应该是 ”包名.类名”。

**包名的一般命名规范：**
* 要求包名所拥有的字母都是小写；
* 包名一般情况下为域名倒过来写。

Test.java

	// 将类放置到一个包当中，需要使用package "包名"
	// 编译时需要使用 -d 参数，该参数的作用是依据包名生成相应的文件夹
	// 一个类的全名应该是 包名.类名
	// 本例的运行命令为： java net.bingu.Test

	package net.bingu;

	class Test{
		public static
		 void main(String args []){
			 System.out.println("Hello package");
		 }
	}

### JAVA 当中的访问权限

访问权限即可修饰类，也可以修饰成员变量和成员函数。

JAVA 当中的访问权限包括 4 种

1. public	公共权限

	公共权限的类，其类名必须与源文件的文件名保持一致。

	只有声明为公共权限的类，才能在不同的包中进行访问。

	同样，如想在外部包中访问一个类的成员函数和成员变量，这些成员函数和成员
	变量都必须声明为公共权限。

2. private	私有权限

	一般情况下，私有权限仅用于修饰成员函数和成员变量。这些成员函数和成员变量只能在当前的类当中使用。

3. default	包级别访问权限/默认权限

	此权限无需在类名、变量名或函数名前面使用权限修饰符 default。
	在不同的包里面，不能访问 default 权限的类。

4. protected	受保护权限



Person.java

	package net.bingu;

	public class Person{
	    public String name;
		public int age;

		public void introduce(){
			System.out.println("Name");
		}
	}

Test.java

	package com.wanwp;

	class Test{
		public static void main(String args []){
			// 类的全名进行
			net.bingu.Person = new net.bingu.Person();

			p.name = "zhangsan";
		}
	}

#### 包的导入

在定义类前可以使用 import 导入包，导入包后，访问该包下的类，则可直接使用 “类名” 进行访问，而无需使用 “包名.类名” 进行访问。

上例的 Test.java 可改写为

Test.java

	package com.wanwp;

	import net.bingu.Person;

	class Test{
		public static void main(String args []){
			Person = new Person();

			p.name = "zhangsan";
		}
	}

#### 访问权限与继承

Person.java

	package com.wanwp;

	public class Person{
		String name;
		int age;

		void eat(){
			System.out.println("eat");
		}

		void sleep(){
			System.out.println("sleep");
		}
	}

Student.java

	package net.bingu;

	import com.wanwp.Person;

	class Student extends Person{

	}

#### protected 权限

protected 权限拥有和 default 权限一样的功能，但是该权限只能修饰成员变量和成员函数。
同时 protected 权限可以跨包进行使用。
protected 权限和 public 权限修饰的成员变量和成员函数的区别是 protected 权限修饰的
成员变量和成员函数仅能供其子类使用。

## **接口**

### 声明是接口

类比现实中的 USB 接口。

### 接口的基本语法（一）

1. 使用 interface 定义；

2. 接口当中的方法都是抽象方法；

3. 接口当中的方法都是 public 权限。

### 接口的基本语法（二）

1. 实现接口使用 implements 关键字；

2. 一个类可以实现多个接口；

3. 一个接口可以继承多个接口。

	如有 A 和 B 两个接口，C 接口可以继承 A 和 B 这两个接口
	interface C extends A,B{
		void funC();
	}

实例：
USB.java

	interface USB{
		public void read();

		public void write();
	}

WIFI.java

	interface WIFI{
		void open();

		void close();
	}

Phone.java

	class Phone implements USB,WIFI{
		@Override
		public void read(){
			System.out.println("Read");
		}

		@Override
		public void write(){
			System.out.println("Write");
		}

		@Override
		public void open(){
			System.out.println("Open");
		}

		@Override
		public void close(){
			System.out.println("Close");
		}
	}

Test.java

	class Test{
		public static void main(String[] args){
			Phone phone = new Phone();
			USB usb = phone;
			usb.read();
			usb.write();

			WIFI wifi = phone;
			wifi.open();
			wifi.close();
		}
	}

### 接口的应用

1. 为什么要使用接口

2. 工厂方法模式

Printer.java

	interface Printer{
		public void open();

		public void close();

		public void print(String text);
	}

HPPrinter.java

	class HPPrinter implements Printer{
	    public void open(){
	        System.out.println("HPPrinter open");
	    }
	    public void close(){
	        System.out.println("HPPrinter close");
	    }
	    public void print(String text){
	        System.out.println("HPPrinter print" + text);
	    }
	}

CanonPrinter.java

	class CanonPrinter implements Printer{
	    public void open(){
	        System.out.println("CanonPrinter open");
	    }
	    public void close(){
	        System.out.println("CanonPrinter close");
	    }
	    public void print(String text){
	        System.out.println("CanonPrinter print" + text);
	    }
	}

XXXPrinter.java

	class XXXPrinter implements Printer{
	    public void open(){
	        System.out.println("XXXPrinter open");
	    }
	    public void close(){
	        System.out.println("XXXPrinter close");
	    }
	    public void print(String text){
	        System.out.println("XXXPrinter print" + text);
	    }
	}

PrinterFactory.java

	class PrinterFactory{
	    public static Printer getPrinter(int flag){
	        Printer printer = null;
	        if (flag == 0){
	            printer = new HPPrinter();
	        }
	        else if (flag == 1){
	            printer = new CanonPrinter();
	        }
	        else if (flag == 2){
	            printer = new XXXPrinter();
	        }
	        return printer;
	    }
	}

Test.java

	class Test{
	    public static void main(String[] args){
	        // 根据用户的选择，生成相应的打印机对象
	        // 并且向上转型为 Printer 类型
	        // Printer getPrinter(int flag)

	        int flag = 1;
	        Printer printer = PrinterFactory.getPrinter(flag);
	        printer.open();
	        printer.print("test");
	        printer.close();
	    }
	}

## **JAVA 当中的异常**

1. 什么是异常

	异常：中断了正常指令流的事件。
	程序员对 Error 无能为力，只能处理 Exception。
	对异常的处理关系到系统的健壮性。

2. 异常的分类

	分为 Exception 和 Error 两大类。

3. 使用 try ... catch .... finally 来处理可能出现异常的代码。

	    try{
		    // 打开文件
			// 操作文件
		}
		catch(Exception e){
			// 如果出现异常，打印异常信息。
			e.printStackTrace();
		}
		finally{
			// 关闭文件
			// 不管是不是出现异常，均会执行 finally 里的代码段
		}

4. throw 的作用

	主动抛出异常

User.java

	class User{
		private int age;

		public void setAge(int age){
			if (age < 0){
				RuntimeException e = new RuntimeException("年龄不能为负数");
				throw e;
			}
			this.age = age;
		}
	}

Test.java

	class Test{
		public static void main(String args[]){
			User user = new User();
			user.setAge(-20);
		}
	}

5. throws 的作用

User.java

	class User{
		private int age;

		public void setAge(int age) throws Exception{
			if (age < 0){
				Exception e = new Exception("年龄不能为负数");
				throw e;
			}
			this.age = age;
		}
	}

Test.java

	class Test{
		public static void main(String args[]){
			User user = new User();
			try{
				user.setAge(-20);
			}
			catch(Exception){
				System.out.println(e);
			}
		}
	}

## **JAVA当中的IO**

1. I/O 操作的目标

	从数据源当中读取数据以及将数据写入到数据目的地当中；

2. IO 的分类方法

	* 第一种分法：1.输入流；2.输出流。

	* 第二种分法：1.字节流；2.字符流。

	* 第三种分法：1.节点流；2.处理流。

3. 读取文件和写入文件的方法

Test.java

	// 第一个步骤：导入 IO 类；
	import java.io.* ;

	class Test{

		public static void main(String args[]){
			// 声明输入流引用
			FileInputStream fis = null;
			// 声明输出流引用
			FileOutputStream fos = null;

			try{
				// 生成代表输入流的对象  
				fis = new FileInputStream("/home/bingu/project/java/j4a32/from.txt");

				// 生成代表输出流的对象
				fos = new FileOutputStrem("/home/bingu/project/java/j4a32/to.txt");

				// 生成一个字节数值
				byte [] buffer = new byte[100];
				// 调用输入流对象的 read 方法，读取数据
				int temp = fis.read(buffer,0,buffer.length);

				fos.write(buffer,0,temp);

				//String s = new String(buffer).trim();

				//System.out.println(s);
			}
			catch(Exception e){
				System.out.println(e);
			}
		}
	}

### 大文件的读写方法

	循环读取数据，到达数据末端则停止循环。

Test.java

	// 第一个步骤：导入 IO 类；
	import java.io.* ;

	class Test{

		public static void main(String args[]){
			// 声明输入流引用
			FileInputStream fis = null;
			// 声明输出流引用
			FileOutputStream fos = null;

			try{
				// 生成代表输入流的对象  
				fis = new FileInputStream("/home/bingu/project/java/j4a32/from.txt");

				// 生成代表输出流的对象
				fos = new FileOutputStrem("/home/bingu/project/java/j4a32/to.txt");

				// 生成一个字节数值
				byte [] buffer = new byte[1024];
				while(true){
					// 调用输入流对象的 read 方法，读取数据
					int temp = fis.read(buffer,0,buffer.length);
					if (temp == -1){
						break;
					}
					fos.write(buffer,0,temp);
			    }

				//String s = new String(buffer).trim();

				//System.out.println(s);
			}
			catch(Exception e){
				System.out.println(e);
			}
			finally{
				try{
					fis.close();
					fos.close();
				}
				catch(Exception e){
					System.out.println(e);
				}
			}
		}
	}

### 字符流的使用方法

	由下面的例子可以看到字符流的方法基本是跟字节流的方法是一致的。

TestChar.java

	import java.io.* ;

	class TestChar{
		// 字符流：读写文件时，以字符为基础
		// 字节输入流：Reader <-- FileReader int read(char [] c, int off, int len);
		// 字节输出流：Writer <-- FileWriter void write(char [] c, int off, int len);

		public static void main(String [] args){
			FileReader fr = null;
			FileWriter fw = null;

			try{
				fr = new FileReader("/home/bingu/project/java/j4a33/from.txt");
				fw = new FileWriter("/home/bingu/project/java/j4a33/to2.txt");

				char [] buffer = new char[100];
				while(true){
					int temp = fr.read(buffer, 0, buffer.length);
					if (temp == -1){
						break;
				    }
					fw.write(buffer, 0, temp);
			    }
			}
			catch(Exception e){
				System.out.println(e);
			}
			finally{
				try{
					fr.close();
					fw.close();
				}
				catch(Exception e){
					System.out.println(e);
				}
			}
		}
	}

### 处理流使用实例

#### BufferedReader介绍

public String readLine()
	throwsIOException

生成 BUfferedReader 对象的方法：
BufferedReader in = new BufferedReader(newFileReader("foo.in"));

Test.java

    import java.io.* ;
	class Test{
		public static void main(String args []){
			FileReader fileReader = null;
			BufferedReader bufferedReader = null;

			try{
			    fileReader = new FileReader("/home/bingu/project/java/j4a34/users.txt");
				bufferedReader = new BufferedReader(fileReader);
				while(true){
					String line = bufferedReader.readLine();
					if (line == null){
						break;
					}
					System.out.println(line);
				}
			}
			catch(Exception e){
				System.out.println(e);
			}
			finally{
				try{
					bufferedReader.close();
					fileReader.close();
				}
				catch(Exception e){
					System.out.println(e);
				}
			}
		}
	}

### 装饰者模式

Worker.java

	interface Worker{
		public void doSomeWork();
	}

Plumber.java

	class Plumber implements Worker{
		public void doSomeWork(){
			System.out.println("I'm a Plumber.");
		}
	}

Carpenter.java

	class Carpenter implements Worker{
		public void doSomeWork(){
			System.out.println("I'm a Carpenter.");
		}
	}

AWorker.java

	class AWorker implements Worker{
		private Worker worker;

		public AWorker(Worker worker){
			this.worker = worker;
		}

		public void doSomeWork(){
			System.out.println("Hello, I'm come from A.");
			this.worker.doSomeWork();
		}
	}

TestWorker.java

	class TestWorker{
		public static void main(String args[]){
			Plumber worker1 = new Plumber();
			AWorker aWorker1 = new AWorker(worker1);
			aWorker1.doSomeWork();

			Carpenter worker2 = new Carpenter();
			AWorker aWorker2 = new AWorker(worker2);
			aWorker1.doSomeWork();
		}
	}
	
## **多线程与多进程**

**多进程**：

	在操作系统中能（同时）运行多个任务（程序）

**多线程**：

	在同一应用程序总有多个顺序流（同时）执行
