---
{"dg-publish":true,"permalink":"/杂项/2023-11/认识Mat类/","dgPassFrontmatter":true}
---

- Mat类是OpenCV中一种用于存储矩阵的数据类型
- Mat类包含
	- 矩阵头
		- 尺寸
		- 行数
		- 列数
		- 通道类型
		- 通道数
		- 引用次数
	- 数据
- Mat能存储的数据
	- `cv::Mat`
		- `cv::Mat_<_Tp>`
		- `cv::Mat_<double>`
		- `cv::Mat_<float>`
		- `cv::Mat_<uchar>`
		- `cv::Mat_<unsigned char>`
	- OpenCV中规定的数据类型
		- | 数据类型 | 具体类型 | 取值范围 |
		| -      | -              | -                          |
		| ------ | -------------- | -------------------------- |
		| CV_8U  | 8位无符号整数  | 0~255                      |
		| CV_8S  | 8位符号整数    | -128~127                   |
		| CV_16U | 16位无符号整数 | 0-65535                    |
		| CV_16S | 16位符号整数   | -32768~32467               |
		| CV_32S | 32位符号整数   | -2147483648~2147483647     |
		| CV_32F | 32位浮点数     | -FLT_MAX~FLT_MAX, INF, NAN |
		| CV_64F | 64位浮点数     | -DBL_MAX~DBL_MAX, INF, NAN |
- Mat类的创建
	- 利用矩阵宽、高和类型参数创建Mat类
		- 原型
			```cpp
			cv::Mat::Mat(int rows, int cols, int type);
			```
			- **rows**：矩阵的行数
			- **cols**：矩阵的列数
			- **type**：矩阵中存储的数据类型，后面加入`Cn`表示通道数，默认为1。此处除了`CV_8UC1`、`CV_64FC4`等从1到4通道外，还提供了更多通道的参数，通过`CV_xxC(n)`，来构建n通道矩阵，n最大可取到512
		- 使用例
			```cpp
			cv::Mat mat1(2, 3, CV_8U);
			cv::Mat mat2(4, 5, CV_16SC3);
			cv::Mat mat3(6, 7, CV_32FC(8));
			```
	- 利用Size()结构和类型参数创建Mat类
		- 原型
			```cpp
			cv::Mat::Mat(Size size, int type);
			```
			- **size**：2D数组变量尺寸，通过`Size(cols, rows)`进行赋值
			- **type**：与前面一致
		- 使用例
			```cpp
			cv::Mat mat1(Size(2, 3), CV_8UC2);
			```
	- 利用已有的Mat类创建新的Mat类
		- 原型
			```cpp
			cv::Mat::Mat(const Mat & m, 
			             const Range & rowRange, 
			             const Range & colRange = Range::all());
			```
			- **m**：已经构建完成的Mat类矩阵数据
			- **rowRange**：在已有矩阵中需要截取的行数范围，是一个Range变量
			- **colRange**：在已有矩阵中需要截取的列数范围，是一个Range变量
		- 使用例
			```cpp
			cv::Mat mat1(mat0, Range(1, 5), Range(2, 6));
			```
- Mat类的赋值
	- 创建时赋值
		- 原型
			```cpp
			cv::Mat::Mat(int rows, int cols, int type, const Scalar & s);
			```
			- **rows**：矩阵的行数
			- **cols**：矩阵的列数
			- **type**：存储数据的类型
			- **s**：给矩阵中每个像素赋值的参数变量，例如`Scalar(0, 0, 255)`
		- 使用例
			```cpp
			cv::Mat mat1(3, 3, CV_8UC3, Scalar(1,2,3,4,5));
			// 创建3行3列Scalar(1,2,3)的矩阵
			```
	- 枚举法赋值
		- 使用例
			```cpp
			cv::Mat mat1 = (cv::Mat_<int>(3,3) << 1, 2, 3, 4, 5, 6, 7, 8, 9);
			cv::Mat mat2 = (cv::Mat_<double>(2,2) << 1.0, 2.1, 3.2, 4.0);
			```
	- 类方法赋值
		- **eye**：单位矩阵
		- **diag**：对角矩阵
		- **ones**：元素全为1的矩阵
		- **zeros**：元素全为0的矩阵
			- 使用例：
				```cpp
				cv::Mat a = (cv::Mat_<int>(3,3) << 
				```
	- 