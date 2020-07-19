#                                                   第三周学习总结

## 一、JS表达式 | 运算符和表达式

**表达式：**是由运算元和运算符(可选)构成，并产生运算结果的语法结构，简单的概括为能参与计算的最小单元。

### 1.  运算符优先级

#### 1.1 Member运算符：

```javascript
1. a.b
2. a[b]
3. foo`string` 
4. super.b
5. super['b']
6. new.target // 函数调用时是否使用了new方式进行初始化
7. new Foo()
```

#### 1.2 new表达式:

```javascript
new Foo
```

#### 1.3  引用类型：

```javascript
.Object
.Key
.delete
.assign
```

#### 1.4 函数调用：

```javascript
1. foo()
2. super()
3. foo()['b']
4. foo().b
5. foo()`abc`
```

#### 1.5 Left Handside & Right Handside

#### 1.6 Update

```javascript
1. a ++
2. a --
3. -- a
4. ++ a
```

#### 1.7 Unary单目运算符

```javascript
1. delete a.b
2. void foo() // 任何内容变成undefind
3. typeof a
4. + a
5. - a
6. ~ a 
7. ! a
8. await a
```

#### 1.8 右结合表达式

```javascript
3 ** 2 ** 3
```

#### 1.9 四则运算

#### 1.10 未运算

```javascript
<<
>>
>>>
```

#### 1.11  比较

```javascript
< > <= >= instanceof in
```

#### 1.12 相等

```javascript
1. == 
2. !=
3. ===
4. !==
```

#### 1.13 逻辑运算

```javascript
1. &&
2. ||
```

#### 1.14  三目运算符

## 二、JS表达式 | 类型转换

#### 2.1 七种类型之间的转换变成

## 三、JS语句 | 运行时相关概念

### 3.1   Completion Record（结果记录，完成状态）

```javascript
1. [[type]]: normal, break, continue, return, throw
2. [[value]]: 基本类型
3. [[target]]: label
```

## 四、 JS语句 | 简单语句和复合语句

### 4.1  简单语句

```javascript
1. ExpressionStatement 表达式语句，只使用表达式构成
2. EmptyStatement 空语句 ；
3. DebuggerStatement 调试语句
4. ThrowStatement 抛出异常
5. ContinueStatement 
6. BreakStatement 
7. ReturnStatement
```

### 4.2 复合语句

```javascript
1. BlockStatement
2. IfStatement
3. SwitchStatement
4. IterationStatement
5. WithStatement
6. LabelledStatment
7. TryStatement
```

### 4.3  Iteration

```javascript
1. while
2. do while
3. for ( ; ;)
4. for ( in )
5. for ( of )
6. for await(of)
```

### 4.4 try  catch

## 五、JS语句 | 声明

```javascript
// 没有先后，函数体内都可以访问到，旧的声明体系
1. function
2. function *
3. async function
4. async function*
5. var

// 使用前必须先声明，新一代的声明体系
1. const 
2. let
3. class
```

### 5.1 作用域

使用花括号进行作用域的分割

## 六、JS结构化 | 宏任务和微任务

### 6.1  JS执行力度（运行时）

```javascript
1. 宏任务
2. 微任务（Promise）
3. 函数调用
```

## 七、JS结构化 |  JS函数调用

### 7.1  Execution Context

```
1. Code evaluation state
2. Function
3. Script Module
4. Generator
5. Realm 
6. LexicalEnvironment
7. VariableEnvironment
```

### 7.2 LexicalEnvironment

```
1. this
2. new.target
3. super
4. 变量
```

### 7.3 VariableEnvironment

VariableEnvironment仅仅处理var

### 7.4  Environment Record

### 7.5  Function  - Closur

每个函数都会生成一个闭包，闭包分成两部分：代码部分和环境部分（Environment Record）。

### 7.6  Realm

所有的内置对象放到Realm里

