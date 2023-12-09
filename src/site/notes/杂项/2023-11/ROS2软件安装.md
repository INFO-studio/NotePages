---
{"dg-publish":true,"permalink":"/杂项/2023-11/ROS2软件安装/","dgPassFrontmatter":true}
---

- 参考[教程1](https://blog.csdn.net/SU_shuer/article/details/113175390)、[教程2](https://zhuanlan.zhihu.com/p/607458999)
- 设置语言环境
	```bash
	locale  # check for UTF-8
	
	sudo apt update && sudo apt install locales
	sudo locale-gen en_US en_US.UTF-8
	sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
	export LANG=en_US.UTF-8
	
	locale  # verify setting
	```
- 设置源
	```bash
	sudo apt update && sudo apt install curl gnupg2 lsb-release
	sudo curl -sSL https://raw.staticdn.net/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
	echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
	```
- 安装ROS2软件包
	```bash
	sudo apt update
	sudo apt upgrade
	sudo apt install ros-humble-desktop
	sudo apt-get install ~nros-humble-rqt*
	```
- 环境设置
	```bash
	echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
	```
- 测试
	```bash
	ros2 run turtlesim turtlesim_node
	```
	然后它就……报错了，提示没有`scipy`库
	安装`sudo pip install scipy`提示系统权限失效，重启系统宕机
	参考[解决方法](https://www.jianshu.com/p/4f65e21dd63c)救回来了
	```bash
	sudo pip install scipy
	ros2 run turtlesim turtlesim_node # 终端1
	ros2 run turtlesim turtle_teleop_key # 新建终端2
	rqt # 新建终端3
	```