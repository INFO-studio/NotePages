---
{"dg-publish":true,"permalink":"/杂项/2023-11/ROS2节点/","dgPassFrontmatter":true}
---

- 简介
	- ROS2中的每一个节点负责一个单独的模块化的功能（比如一个节点负责控制车轮转动，一个节点负责处理激光雷达的数据，一个节点负责定位等等）
	- 比如一个通用机器人可能由以下节点组成，由ROS2 Communication来调度
		- Camera
		- Navigation
		- Driver
		- Joystick
		- ...
- 节点之间如何交互
	- ROS2为节点准备了四种通讯方式
		- 话题 topics
		- 服务 services
		- 动作 action
		- 参数 paramenters
	- 