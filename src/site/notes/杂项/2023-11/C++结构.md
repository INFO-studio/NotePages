---
{"dg-publish":true,"permalink":"/杂项/2023-11/C++结构/","dgPassFrontmatter":true}
---

- 结构的定义
	```cpp
	struct structName
	{
		int structInt;
		float structFloat;
		char structString[10];
	};
	```
	- 结构是一种比数组更灵活的数据格式，也是C++ OOP类的基石，一个结构可以存储多个不同种类的数据，从而将数据的表示合并到一起
	- 关键字`struct`表明，这些代码定义的是一个结构的布局，标识符`structName`是这种数据格式的名称
- 结构的声明、初始化和使用
	```cpp
	#include <iostream>
	
	struct structName
	{
		int structInt;
		float structFloat;
		char structString[10];
	};
	
	int main()
	{
		structName varStruct = 
		{
			1,
			3.14,
			"Hello"
		};
		
		std::cout << varStruct.structInt << varStruct.structFloat 
		          << varStruct.structString << std::endl; // output 13.14Hello
	}
	```
	- 结构的声明有两种：**内部声明**和**外部声明**。此处采用的是内部声明，这样的优点是后面的任何函数都可以使用这种类型的结构
	- C++11也支持列表初始化结构，如`structName varStruct = {1,	3.14, "Hello"};`
		- 若大括号内未包含任何东西，则各个成员都将被初始化为0，如`structName a {};`
		- *不允许缩窄转换*
	- 可以声明独特的结构变量，即同时定义一个无名结构类型和这一结构变量，如
		```cpp
		struct
		{
			int x;
			int y;
		} specialStruct;
		```
		- 可以使用成员运算符来访问它的成员（如`specialStruct.x`）
		- 但是这种结构类型没有名称，因此以后无法创建同样类型的变量
- 结构数组
	- 可以创建元素为结构变量的数组，这样数组的每一个元素都是结构变量，如
		```cpp
		structName varStruct[2] = 
		{
			{1, 3.14, "Hello"},
			{2, 6.28, "World"}
		};
		
		std::cout << varStruct[1].structFloat << std::endl; // output 6.28
		```
- 结构位字段
	- C++允许指定占用特定位数的结构成员，这使得创建与某个硬件设备上的寄存器对应的数据结构非常方便
	- 字段的类型应为整形或枚举，接下来是冒号，冒号后面是一个数字，它指定了使用的位数
	- 可以使用没有名称的字段来提供内存间距
	- 每个成员都被称为**位字段**（bit field）
	- 举例如下：
		```cpp
		struct bitsStructExp
		{
			unsigned int A : 4;
			unsigned int : 4;
			bool B : 1;
			bool C : 2;
		};
		
		bitsStructExp example = {12, true, false};
		std::cout << example.A << example.C << std::endl; // output 120
		```