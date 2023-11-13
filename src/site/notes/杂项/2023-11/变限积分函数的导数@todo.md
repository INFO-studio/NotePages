---
{"dg-publish":true,"permalink":"/杂项/2023-11/变限积分函数的导数@todo/","dgPassFrontmatter":true}
---

若$f(x)$连续，$\varphi(x)$和$\psi(x)$可导，则变限积分函数$\displaystyle F(x)=\int_{\psi(x)}^{\varphi(x)}f(t)\mathrm{d}t$可导，且
$$F’(x)=f[\varphi(x)]\varphi’(x)-f[\psi(x)]\psi’(x)$$
根据上述定理的形式可知，在**对变限积分函数求导时，变限积分函数的被积函数不能含有变量x**。如果有变量$x$，可以通过下面三种方法，使被积函数中不再含有$x$，然后应用求导法则和变限积分函数的导数公式计算导数
- **提取**
	$$F(x)=\int_{\psi(x)}^{\varphi(x)}f(t)g(x)\mathrm{d}t=g(x)\int_{\psi(x)}^{\varphi(x)}f(t)\mathrm{d}t$$
- **拆分**
	$$F(x)=\int_{\psi(x)}^{\varphi(x)}(t+x)f(t)\mathrm{d}t=\int_{\psi(x)}^{\varphi(x)}tf(t)\mathrm{d}t+x\int_{\psi(x)}^{\varphi(x)}f(t)\mathrm{d}t$$
- **换元**
	$$\mathrm{Assume\ that}\quad t+x=u \quad so \quad F(x)=\int_{\psi(x)}^{\varphi(x)}f(t+x)\mathrm{d}t=\int_{\psi(x)+x}^{\varphi(x)+x}f(u)\mathrm{d}u$$
- **注**：
	- 提取法将$F(x)$表示为两个函数的积，第二个函数是可以利用公式求导的变限积分函数
	- 拆分法将$F(x)$表示为两个函数的和，其中前者时可以利用公式求导的变限积分函数；后者是两个函数的积
	- 换元法将$F(x)$表示为可以利用公式求导的变限积分函数