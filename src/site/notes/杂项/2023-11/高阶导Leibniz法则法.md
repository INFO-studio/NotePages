---
{"dg-publish":true,"permalink":"/杂项/2023-11/高阶导Leibniz法则法/","dgPassFrontmatter":true}
---

函数表示为两个函数的积，而每个函数都可以求出$n$阶导数，此种情况可以利用[[杂项/2023-11/Leibniz法则\|Leibniz法则]]求导，特别是形如$x^ke^x\ ,\ x^k\sin x\ ,\ x^k\ln(x+1)\ ,\ e^x\sin x\ ,\ e^x\cos x$函数的高阶导数，一般都应用Leibniz法则
- **例1**：
	设$f(x)=x^2e^x$，求：$f^{(20)}(x)$
	解：利用Leibniz法则
	$$f^{(20)}(x)=(e^x)^{(20)}x^2+C_{20}^1(e^x)^{(19)}(x^2)’+C_{20}^2(e^x)^{(18)}(x^2)’’=e^x(x^2+40x+380)$$
- **例2**：
	设$f(x)=x\ln(x+2)$，求：$f^{(20)}(0)$
	解：利用Leibniz法则
	$$\begin{aligned}f^{20}(x)&=[\ln(x+2)]^{(20)}\cdot x+C_{20}^1[\ln(x+2)]^{(19)}\cdot(x)’\\&=x[\ln(x+2)]^{(20)}+20[\ln(x+2)]^{(19)}\\&=-19!\cfrac{x}{(x+2)^{20}}+20\cdot18!\cfrac{1}{(x+2)^{19}}\\\therefore f^{(20)}(0)&=\cfrac{20\cdot18!}{2^{19}}=\cfrac{5\cdot18!}{2^{17}}\end{aligned}$$