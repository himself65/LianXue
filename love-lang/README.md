# The Love Programming Language

恋学程序设计语言(Love-Lang)是一个以帮助程序员恋爱，或者帮助程序员找到恋爱感觉为目的的现代程序设计语言。它具备以下特性

 - 多语言转译，包括C/Python/JavaScript
 - 极小运行时
 - 简单而快速的编译器/解释器前端
 - 接近零开销抽象
 - 垃圾回收功能
 - 面向对象特性和运行时多态
 - 动态弱类型，对非程序员用户友好

## 完全的shiftless
我们精心设计了Love-Lang的语法，使您在编程时完全无需按下shift键：您完全不需要任何特殊符号，就能做任何你想做的事

	/; this is a piece of comment ;/
	function fibonacci takes n returns fib begin
		if n == 0
			fib = 0;
		else if n == 1
			fib = 1;
		else
			fib = fibonacci [n minus 1] plus fibonacci [n minus 2];
	end function

## 一切都是对象
还在为找不到对象而烦恼？在Love-Lang的世界里，一切都是对象(companion)

	/; a prototype companion ;/
	companion girl begin
		name = '',
		age = 18,
		height = 175
	end

	function main takes argc argv begin
		let mygirl = clone[girl];   /; use prototype ;/
		setq[mygirl, 'name', 'xxx']; /; changing companion ;/
	end function

我们没有选择古老的名词object，而选择将对象意译为“伴侣”companion！

## C-FFI支持
Love-Lang可以透过其特有的外部函数接口调用C函数：首先需要从动态链接库中取得它所需要的C函数，之后只需像普通函数那样调用！

	function main takes argc argv begin
		dynmod ['./libextmath.so']; /; load mathematics library ;/
		print [ sin [5.0] ]; /; just use foreign functions as native functions! ;/
	end function

## 何时发布
我们将会在大约十一月底发布测试版本，届时所有项目组成员和社会各界人士均有机会参与测试。