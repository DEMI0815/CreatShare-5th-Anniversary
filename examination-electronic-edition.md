# 技术类

* 加分：将笔试题答案提交到 github 上对下方仓库链接进行 Pull Request：

> https://github.com/creatshare-demos/CreatShare-5th-Anniversary.git

## 基础部分

1. C 标准定义的关键字都有哪些？分别有什么用？
 1>void:声明函数无返回值或无参
 2>char:1字节ASCII
 3>short:2字节补码
 4>int:4字节补码
 5>long:4字节补码
 6>float:4字节浮点
 7>double:8字节浮点
 8>signed:有符号数
 9>unsigned:无符号数
 10>struct:结构体声明
 11>union:共用体声明
 12>enum:枚举声明 
 13>typedef:声明类型别名 
 14>sizeof:得到特定类型或特定类型变量的大小 
 15>auto:指定为自动变量，由编译器自动分配及释放。通常在栈上分配 
 16>static:指定为静态变量，分配在静态变量区，修饰函数时，指定函数作用域为文件内部
 17>register:指定为寄存器变量，建议编译器将变量存储到寄存器中使用，也可以修饰函数形参，建议编译器通过寄存器而不是堆栈传递参数 
 18>extern:指定对应变量为外部变量，即在另外的目标文件中定义，可以认为是约定由另外文件声明的韵蟮囊桓觥耙 谩? 
 19>const:与volatile合称“cv特性”，指定变量不可被当前线程/进程改变（但有可能被系统或其他线程/进程改变） 
 20>volatile:与const合称“cv特性”，指定变量的值有可能会被系统或其他进程/线程改变，强制编译器每次从内存中取得该变量的值
 21>if:条件语句 
 22>else:条件语句否定分支（与if连用）  
 23>switch：开关语句（多重分支语句）  
 24>case：开关语句中的分支标记 
 25>default:开关语句中的“其他”分治，可选
 26>for:for循环结构，for(1;2;3)4;的执行顺序为1->2->4->3->2...循环，其中2为循环条件  
 27>do:do循环结构，do 1 while(2);的执行顺序是1->2->1...循环，2为循环条件  
 28>while:while循环结构，while(1) 2;的执行顺序是1->2->1...循环，1为循环条件
 29>return:用在函数体中，返回特定值（或者是void值，即不返回值）  
 30>continue:结束当前循环，开始下一轮循环  
 31>break:跳出当前循环或switch结构  
 32>goto:无条件跳转语句
 
2. 以下式子的值为多少？为什么？
```
int Anniversary = (2016, ((0x01 << (int)2.0) + sizeof(char)));
```
3. -0 和+0 在计算机里以什么形式存储？这样存储有必要吗？
4. struct 与 class 有什么区别？
	C中struct是结构体声明，结构体由成员组成；JAVA中class可以面向对象编程，类中可以有成员和方法。
5. 面向对象三大特性和五大原则分别是什么？对我们编程有什么启示？
	三大特性：封装，继承，多态

	封装，就是把客观事物封装成抽象的类，并且类可以把自己的数据和方法只让可信的类或者对象操作，对不可信的进行信息隐藏。一个类就是一个封装了数据以及操作这些数据的代码的逻辑实体。在一个对象内部，某些代码或某些数据可以是私有的，不能被外界访问。通过这种方式，对象对内部数据提供了不同级别的保护，以防止程序中无关的部分意外的改变或错误的使用了对象的私有部分。

	继承，指可以让某个类型的对象获得另一个类型的对象的属性的方法。它支持按级分类的概念。继承是指这样一种能力：它可以使用现有类的所有功能，并在无需重新编写原来的类的情况下对这些功能进行扩展。 通过继承创建的新类称为“子类”或“派生类”，被继承的类称为“基类”、“父类”或“超类”。继承的过程，就是从一般到特殊的过程。要实现继承，可以通过 “继承”（Inheritance）和“组合”（Composition）来实现。继承概念的实现方式有二类：实现继承与接口继承。实现继承是指直接使用 基类的属性和方法而无需额外编码的能力；接口继承是指仅使用属性和方法的名称、但是子类必须提供实现的能力。

	多态，是指一个类实例的相同方法在不同情形有不同表现形式。多态机制使具有不同内部结构的对象可以共享相同的外部接口。这意味着，虽然针对不同对象的具体操作不同，但通过一个公共的类，它们（那些操作）可以通过相同的方式予以调用。

	五大原则：SPR, OCP, LSP, DIP, ISP

	单一职责原则SRP(Single Responsibility Principle)
	是指一个类的功能要单一，不能包罗万象。如同一个人一样，分配的工作不能太多，否则一天到晚虽然忙忙碌碌的，但效率却高不起来。

	开放封闭原则OCP(Open－Close Principle)
	一个模块在扩展性方面应该是开放的而在更改性方面应该是封闭的。比如：一个网络模块，原来只服务端功能，而现在要加入客户端功能，那么应当在不用修改服务端功能代码的前提下，就能够增加客户端功能的实现代码，这要求在设计之初，就应当将服务端和客户端分开，公共部分抽象出来。

	替换原则LSP(the Liskov Substitution Principle LSP)
	子类应当可以替换父类并出现在父类能够出现的任何地方。比如：公司搞年度晚会，所有员工可以参加抽奖，那么不管是老员工还是新员工，也不管是总部员工还是外派员工，都应当可以参加抽奖，否则这公司就不和谐了。

	依赖原则DIP(the Dependency Inversion Principle DIP)
	具体依赖抽象，上层依赖下层。假设B是较A低的模块，但B需要使用到A的功能，这个时候，B不应当直接使用A中的具体类： 而应当由B定义一抽象接口，并由A来实现这个抽象接口，B只使用这个抽象接口：这样就达到了依赖倒置的目的，B也解除了对A的依赖，反过来是A依赖于B定义的抽象接口。通过上层模块难以避免依赖下层模块，假如B也直接依赖A的实现，那么就可能 造成循环依赖。一个常见的问题就是编译A模块时需要直接包含到B模块的cpp文件，而编译B时同样要直接包含到A的cpp文件。

	接口分离原则ISP(the Interface Segregation Principle ISP)
	模块间要通过抽象接口隔离开，而不是通过具体的类强耦合起来
	
6. 简述 OSI 七层模型和 TCP/IP 四层模型区别。并理解 HTTP 在其中的定位。

7. 在 x86 系统下，有以下程序的运行结果是什么？在这个过程中系统都发生了什么？

```
#include <stdio.h>
#define HELLO “CREATSHARE %d!”
#define CREATSHARE(x) (x)
int main() {
    printf(HELLO,CREATSHARE(2016));
    return 0;
}
```

8. 在 x86 系统下，以下程序的运行结果是什么？为什么？

```
#include <stdio.h>
int main() {
    int a[4]={1,2,3,4};
    int *ptr1=(int *)(&a+1);
    int *ptr2=(int *)((int)a+1);
    printf("%x,%x",ptr1[-1],*ptr2);
    return 0;
}
```
	4,2
	&a+1=&a+sizeof(4*int)，因此&a+1指向的地址为&a[4]；所以ptr1指向&a[4]； ptr1-1=ptr-sizeof(int)，
	故ptr-1指向&a[3]。因此，ptr1[-1] <=> *(ptr1-1) <=> a[3] <=> 4。

	*ptr2 <=> *(a+1) <=> a[1] <=> 2

9. 编写一个函数，如果操作系统是大端模式返回0，小端模式返回1。
#include<stdio.h>
union node{
	int a;
	char b[4];
}t;

int main(){
	t.a=1;
	printf("%d\n",t.b[0]);
}

10. 编写一个函数，参数中给定正整数 n 和 m，将1到n的这n个整数按字典排序之后，返回其中的第 m 个数字。对于n=11，m=4，按字典序排列依次为1，10，11，2，3，4，5，6，7，8，9。因此第4个数字为2。

## 前端部分

1. 谈谈你对广义的 HTML5 的理解。
2. 谈谈你对盒子模型和弹性盒模型的理解。
3. 列出常见的 CSS 预处理器并说明其优点。
4. 谈谈你对前端组件化开发的理解。
5. 谈谈你对前端 MV* 设计模式的理解。
6. 列出 JavaScript 中有哪些异步方法并区别这些方法。
7. 详细说明 JavaScript 的事件系统并简述事件捕获与事件冒泡的区别和事件委托的概念。
8. 有下列 HTML 及 CSS 片段，

```
<ul id="list">
    <li class="item">C</li>
    <li class="item">R</li>
    <li class="item">E</li>
    <li class="item">A</li>
    <li class="item">T</li>
    <li class="item">S</li>
    <li class="item">H</li>
    <li class="item">A</li>
    <li class="item">R</li>
    <li class="item">E</li>
</ul>

#list{
    margin: 0;
    padding: 0;
    list-style-type: none;
}
```

在不使用 Javascript，不改变现有 HTML 及 CSS 的情况下，添加代码，实现下列效果：

- 奇数位 li 背景为黄色，字的颜色为蓝色，字号为18px
- 偶数位 li 使文字剧中，字母下显示下划线
- 第一个 li 整体透明度为0.5
- 第四个 li 在鼠标移到其上方时使其2D放大3倍，且其他 li 不受影响，放大及缩小过程中应用平滑过渡效果，过渡持续0.3s
- 第八个 li 显示右边框，边框宽度4px，样式为实线，绿色

9. 有下列 JavaScript 代码，判断其运行后 console.log() 所显示的值，并解释原因(均为非严格模式)

```
  <button id="s" onclick="console.log(this)"></button>
  <script>console.log(this)</script>
  <script>
  	function a(){
	    console.log(this);
 	}
	new a();
   </script>
  <script>
  	var a = {};
	  a.print = function(){
              console.log(this);
	  }
       a.print();
  </script>
  <script>
  	function a(name){
            this.name = name;
	}

  	a.prototype.print = function(){
    	    console.log(this.name);
  	}

  	var q = new a('foo');
  	var x = new a('bar’);

  	q.print();
  	x.print();
   </script>
   <script>
	function a(name){}

	a.prototype.print = function(){
	    ;(function(){
            	console.log(this);
	    })();
   	}

	var q = new a();
	q.print();
   </script>
```

如果最后一段代码的 this 不指向 a 的实例，如何让其指向 a 的实例？

10. 以下两道编程题二选一，全做加分。

10.1. 代码实现下图所示布局。

![CreatShare-FE-demo](./CreatShare-FE-demo.jpeg)

10.2. 搭建开发环境，本地环境用 Post 方法向后台发送如下数据。如果是以下内容则返回“Happy 5 Anniversary!”，否则返回“error”。
```
{
    name: “CreatShare”
    anniversary: 5,
    year: 2016
}
```

## 服务端部分

1. 列出常见的关系型数据库和非关系型数据库。
	关系型数据库：SQLite、Oracle、mysql
	非关系型数据库：MongoDb、redis、HBase
2. 谈谈你对数据库和数据仓库的理解。

3. 谈谈你对对象关系型映射(orm)的理解。
4. 区分进程和线程。
5. 请用一个例子表明全局对象的缺点。
6. 区分 Stringbuffer 与 Stringbuilder。
7. 谈谈你对 TCP 三次握手中 TIME_WAIT 和 CLOSE_WAIT 状态的理解。
8. 简述在 epoll 的水平触发下，当 socket  可写的时候，会不停的触发写事件的原因。
9. 简述打开TCP套接字有很大开销的原因。
10. 以下两道编程题二选一，全做加分。

10.1. 使用信号量实现有限缓冲区的生产者和消费者问题。

10.2. 搭建开发环境，本地环境用 Post 方法向后台发送 Json 数据。如果是以下内容则返回“Happy 5 Anniversary!”，否则返回“error”。

```
{
    name: “CreatShare”
    anniversary: 5,
    year: 2016
}
```
