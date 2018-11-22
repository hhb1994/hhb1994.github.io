---
title: ES6语法
tags: [ES6]
categories: 知识
---

## 模板字符串

### 语法

	`string text`
	
	`string text line 1
	 string text line 2`
	
	`string text ${expression} string text`
	
	tag `string text ${expression} string text`

---

### 描述

模板字符串使用反引号 (\` \`) 来代替普通字符串中的用双引号和单引号。模板字符串可以包含特定语法（${expression}）的占位符。占位符中的表达式和周围的文本会一起传递给一个默认函数，该函数负责将所有的部分连接起来，如果一个模板字符串由表达式开头，则该字符串被称为带标签的模板字符串，该表达式通常是一个函数，它会在模板字符串处理后被调用，在输出最终结果前，你都可以通过该函数来对模板字符串进行操作处理。在模版字符串内使用反引号（`）时，需要在它前面加转义符（\）。

``\`` === "`" // --> true`

#### 多行字符串

例如:

##### 普通字符串

	console.log('string text line 1\n' +
	'string text line 2');
	// "string text line 1
	// string text line 2"

##### 模板字符串

	console.log(`string text line 1
	string text line 2`);
	// "string text line 1
	// string text line 2"

#### 插入表达式

例如:

##### 普通表达式

	var a = 5;
	var b = 10;
	console.log('Fifteen is ' + (a + b) + ' and\nnot ' + (2 * a + b) + '.');
	// "Fifteen is 15 and
	// not 20."

##### 模板字符串表达式

	var a = 5;
	var b = 10;
	console.log(`Fifteen is ${a + b} and
	not ${2 * a + b}.`);
	// "Fifteen is 15 and
	// not 20."

### 示例


	'use strict';
	var a = 1;
	console.log(a); //1
	console.log(`a=${a}`); //a=1
	console.log('a=${a}'); // a=${a}


## 三元表达式

### 语法

`test ? expression1 : expression2` 

### 参数

* test: 任何 Boolean 表达式;
* expression1 : 如果 test 的值为 true ,则返回表达式,可能是逗号表达式;
* expression2: 如果 test 的值为 false ,则返回表达式,可以使用逗号表达式链接多个表达式.

### 备注

?: 运算符可以用作 if...else.. 语句的快捷方式,例如:
	
	var now = new Date();
	var greeting = "Good" + ((now.getHours() > 17) ? " evening." : " day.");

如果使用 if...else...的话: 

	var now = new Date();
	var greeting = "Good";
	if (now.getHours() > 17)
	   greeting += " evening.";
	else
	   greeting += " day.";

### 示例



## var/let/const

### 概括

* 使用 const 声明的是常量,在后面出现的代码中不能再修改该常量的值;
* 使用 let 声明的变量,其作用域为该语句所在的代码块中,不存在变量提升;
* 使用 var 声明的变量,其作用域为该语句所在的函数内,且存在变量提升现象.

### 示例

	for(var i=0;i<=2;i++){
	    var a = i;
	}
	console.log(a); //2

---

	for(var i=0;i<=2;i++){
	    let a = i;
	}
	console.log(a); //undefined

---

	for(var i=0;i<=2;i++){
	    const a = i;
	}
	console.log(a); //undefined

---

	const a = 1;
	a = 2 ;
	console.log(a); //Assignment to constant variable. 

---

	const a = {b:1};
	a.b = 2;
	console.log(a.b); // 2 

## 箭头函数 =>

### 定义

`(parameters) => { statements }`

如果没有参数:

`() => { statements }`

如果只有一个参数,可以省略括号:

`parameters => { statements }`

如果返回值只有一个表达式,还可以省略花括号:

`parameters => expression`

等价于:

	function (parameters){
	return expression;
	}






	


