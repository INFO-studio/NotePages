---
{"dg-publish":true,"permalink":"/杂项/2023-11/常用git镜像/","dgPassFrontmatter":true}
---

### 加速`clone`
- 方法一：手动替换地址
	```bash
	# 原地址
	$ git clone https://github.com/abc/abc.git
	# 改为
	$ git clone https://github.com.cnpmjs.org/abc/abc.git
	# 或者
	$ git clone https://hub.fastgit.org/abc/abc.git
	# 或者
	$ git clone https://gitclone.com/github.com/abc/abc.git
	```
- 方法二：配置git自动替换
	```bash
	$ git config --global url."https://hub.fastgit.org".insteadOf https://github.com
	# 查看git配置信息
	$ git config --global --list
	# 取消设置
	$ git config --global --unset url.https://github.com/.insteadof
	```
### 加速`release`
```bash
# 原地址 
wget https://github.com/abc
# 改为
wget https://download.fastgit.org/abc
# 或者
wget https://hub.fastgit.org/abc
```
### 加速 `raw`
```bash
# 原地址 
$ wget https://raw.githubusercontent.com/abc
# 改为 
$ wget https://raw.staticdn.net/kubernetes/abc
# 或者 
$ wget https://raw.fastgit.org/kubernetes/abc # 暂时不可用
```