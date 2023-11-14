---
{"dg-publish":true,"permalink":"/杂项/2023-11/C++共用体/","dgPassFrontmatter":true}
---

- 共用体的定义
	```cpp
	union unionName
	{
		int unionInt;
		long unionLong;
		double unionDouble;
	};
	```
	- 共用体是一种数据格式，它能够存储不同的数据类型，但是只能同时存储其中的一种类型
	- 共用体常用于节省内存，另外，共用体也用于操作系统数据结构和硬件数据结构
- 共用体的声明、初始化和使用
	```cpp
	#include <iostream>
	
	union unionName
	{
		int unionInt;
		long unionLong;
		double unionDouble;
	};
	
	int main()
	{
		unionName varUnion;
		varUnion.unionInt = 15;
		std::cout << varUnion.unionInt << std::endl; // output 15
		varUnion.unionDouble = 3.1415;
		std::cout << varUnion.unionDouble << std::endl; // output 3.1415
	}
	```
	- 共用体的初始化必须使用其第一个成员
- 匿名共用体
	- 匿名共用体没有名称，其成员将位于相同地址处的变量，如
		```cpp
		#include <iostream>
		
		struct structA
		{
			int unionType;
			union
			{
				long B;
				char C[10];
			};
		};
		
		int main()
		{
			structA A = {0, 10000};
			if (A.unionType == 0)
			{
				std::cout << A.B << std::endl; // output 10000
			}
			else
			{
				std::cout << A.C << std::endl;
			}
			
			A.unionType = 1;
			strncpy(A.C, "Hello", sizeof(A.C));
			if (A.unionType == 0)
			{
				std::cout << A.B << std::endl;
			}
			else
			{
				std::cout << A.C << std::endl; // outout Hello
			}
		}
		```
	- 由于共用体是匿名的，因此`B`和`C`被视为`A`的两个成员，它们的地址相同，程序员负责确定当前共用体中哪个成员是活动的
