一. js语言通识

1、语言分类
   非形式语言：日常用语
   形式语言（乔姆斯基谱系）：上下包含3属于2，1，0
	   > 0 无限制文法
	   > 1 上下文相关文法
	   > 2 上下文无关文法
	   > 3 正则文法
   
2. 产生式（BNF）
   > 尖括号：语法结构
             基础结构：终结符（Terminal Symbol）类似于叶子节点
			 复合结构：非终结符(Nonetermial Symbol)
   > 引号和中间的字符标识终结符
   > *表示重复多次
     | 或
	 + 表示一次
   > 产生式描述四则运算
     number：终结符
	 + - * / 非终结符
     <MultipicativeExpression>::=<Number>|
	                             <MultipicativeExpression>"*"<Number>|
								 <MultipicativeExpression>"/"<Number>|
	 <AddtiveExpression>::=<MultipicativeExpression>|
                           <AddtiveExpression>"+"<MultipicativeExpression>|
						   <AddtiveExpression>"-"|
   > 四则运算带括号
    
     <MultipicativeExpression>::=["("]<Number>[")"]|
	                             ["("]<MultipicativeExpression>"*"<Number>[")"]|
								 ["("]<MultipicativeExpression>"/"<Number>[")"]|
	 <AddtiveExpression>::=<MultipicativeExpression>|
                           ["("]<AddtiveExpression>"+"<MultipicativeExpression>[")"]|
						   ["("]<AddtiveExpression>"-"<MultipicativeExpression>[")"]|
						   
    

3. 深入理解产生式
   这里相对来说理论太多，需要花时间再研究

4. 现代语言分类
   > 根据文法复杂程度
   > 用途分类
     > 数据描述语言：JSON、HTML、XAML、SQL、CSS、XHTML、SGML
	 > 编程语言：C、C++、C#、Java、JavaScript、TypeScript、Delphi、易语言、Php、RUBY、Phyon、LISP、Haskell、Clojure、Kotlin、Go
	  SQL可以用于触发器、存储过程、函数编辑是否属于编程语言？
	  LINUX、UNIX、WINDOW脚本语言属于何种语言
   > 表达方式分类
     声明式语言：JSON、HTML、XAML、SQL、CSS、Lisp、Clojure、Haskell
	 命令性语言: C、C++、C#、Java、JavaScript、TypeScript、Delphi、易语言、Php、RUBY、Phyon、Kotlin 
	 
5. 编程语言的性质
   > 图灵完备性：所有可计算的问题都可用来描述
      > 命令式
	  > 声明式：声明式lambda
   > 动态与静态
   > 强类型和弱类型
   
6. 一般命令式编程语言的设计方式
   > atom: 关键字、变量名
   > expression（表达式）：atom、operator、punctuator 
   > statement（语句）:
   > Structure
   > Program

7. JS基本数据类型
   Number
   Boolean
   String
   Object
   Null: typeof null === 'object'
   Undefined   
   Symbol
   
   Number类型：
   > double float：IEEE754
   > 最大整数范围
   > 1（符号位）+11（指数位）+52（精度位）
   > 语法：
	   > 10进制: 
		 > 0.2 
		 > 0.
		 > .2 
		 > 1e3
	   > 2进制
		 > 0b111 
	   > 8进制
		 > 0o10
	   > 16进制
		 > 0xFF
   > 特殊写法
     0.toString();
	 0. toString();
	 
8.  String类型
    > Character（字符）
	> CodePoint
	> Encoding
	  > ASCII
	  > Unicode
	  > UCS
	  > GB
	    > GB2312
		> GBK(GB13000)
		> GB18030
	> ISO-8859
	> BIG5
	
9.  Boolean类型
    Null
	Undefined

10. 对象基础知识
	原型和继承
    对象行为是改变自身状态的行为

11. js中的对象
    原型及原型链
	属性：key[Symbol] => value
	      Symbol实现对象中权限的控制
	Data Property:
	   > writable
	   > enumerable
	   > configurable
	原型api：
	   Object.defineProperty()
	   Object.create()
	   Object.setPrototypeOf()
	   Object.getPrototypeOf()
	   new/class/extends 
	   new/function/protype
	   
	  
    
		 


   

   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
	