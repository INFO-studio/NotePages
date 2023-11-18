---
{"dg-publish":true,"permalink":"/杂项/2023-11/C++枚举/","dgPassFrontmatter":true}
---

- 枚举的定义
	- C++的`enum`工具提供了另一种创建符号常量的方式，这种方式可以代替`const`。它还允许定义新类型，但必须严格的限制进行。使用`enum`句法与使用结构相似，如：
		```cpp
		enum spectrum {red, orange, yellow, green, blue, violet}
		```
	- 这条语句完成两项工作
		- 让`spectrum`成为新类型的名称；`spectrum`被称为**枚举**
		- 将`red`、`orange`等作为符号常量，它们对应整数值0~7。这些常量叫做**枚举量**
	- 默认将整数值赋给枚举量，第一个枚举量的值为0，第二个枚举量的值为1，依此类推
- 枚举的声明、初始化和使用
	- 