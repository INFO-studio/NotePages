---
{"dg-publish":true,"permalink":"/杂项/2023-11/函数极限Taylor公式法/","dgPassFrontmatter":true}
---

当极限或变化后极限为$\cfrac{0}{0}$或$\cfrac{\infty}{\infty}$时，若应用洛必达法则变得更加复杂，其他方法又不适合的情况下，可考虑利用[[杂项/2023-11/Taylor公式\|Taylor公式]]，将函数展开成带有Peano余项的关于$x$的多项式，再求极限。
- **例1**
	求：
	$$\lim\limits_{x \to 0}\cfrac{x \ln (1-x^2) + 6(x - \sin x)}{x^5}$$
	解：讲函数展开成带有Peano余项的关于$x$的Taylor公式
	$$\begin{aligned} \ln (1-x^2) = -x^2-\cfrac{1}{2} x^4 + o(x^4) & \quad so \quad x \ln (1-x^2) = -x^3 - \cfrac{1}{2} x^5 + o(x^5) \\ \sin x = x - \cfrac{1}{3!}x^3 + \cfrac{1}{5!}x^5 + o(x^5) & \quad so \quad 6(x-\sin x) = x^3 - \cfrac{1}{20x^5} + o(x^5) \\ \therefore \lim\limits_{x \to 0}\cfrac{x \ln (1-x^2) + 6(x - \sin x)}{x^5} &= \lim\limits_{x \to 0}\cfrac{[-x^3-\cfrac{1}{2}x^5 + o(x^5)] - [x^3 - \cfrac{1}{20} x^5 + o(x^5)]}{x^5} \\ &= \lim\limits_{x \to 0}\cfrac{-\cfrac{1}{2} x^5 - \cfrac{1}{20} x^5 + o(x^5)}{x^5} = - \cfrac{11}{20} \end{aligned}$$
- **注**：
	- 关于函数展成几阶Trylor公式的说明：在计算极限时，利用Taylor公式讲函数展开成带有Peano余项的Teylor公式，应该展成几阶Taylor公式，即展到哪项为止，是由展开项对极限是否有影响决定的。如果此项对极限没有影响，而前一项有影响，那就应该展到前一项为止，而且余项不影响极限值！
	- 在例1中，分子的$\sin x$展到$x^5$为止，而$\ln (1-x^2)$展到$x^4$为止，这是由于
	$$x \ln (1-x^2) + 6(x - \sin x) = - \cfrac{11}{20} x^5 + o(x^5)$$
	当$x \to 0$时，极限是由$- \cfrac{11}{20} x^5$决定的，与$o(x^5)$无关（不影响极限值）；如果$\sin x$展到$x^7$，而$\ln (1-x^2)$展到$x^6$为止，则有
	$$x \ln (1-x^2) + 6(x-\sin x) = - \cfrac{11}{20} x^5- \cfrac{279}{840}x^7 + o(x^7)$$
	此时极限仍然是由$-\cfrac{11}{20} x^5$决定的，与$-\cfrac{279}{840}x^7 + o(x^7)$无关（不影响极限值），所以各自多展一项是没有任何意义的。
	如果将函数$\ln(1+x)$写成二阶泰勒公式，即$\ln (1+x) = x - \cfrac{1}{2} x^2 + o(x^2)$，从而得到
	$$\lim\limits_{x \to 0} \cfrac{\ln (1+x)}{x} = \lim\limits_{x \to 0} \cfrac{x - \cfrac{1}{2}x^2 + o(x^2)}{x} = 1 + \lim\limits_{x \to 0} (-\cfrac{1}{2}x) + \lim\limits_{x \to 0}\cfrac{o(x^2)}{x} = 1$$
	多展的一项与分母x的商的极限是0，不影响极限，所以多展的一项是没有任何意义的，于是$\ln (1+x)$展到一阶为止！
	- 又如求极限
	$$\lim\limits_{x \to 0} \cfrac{1+\cfrac{1}{2}x^2-\sqrt{1+x^2}}{\tan
{ #2}
 x ( \cos x - e^{x^2})}$$
	根据
	$$(1+x)^a = 1 + ax + \cfrac{a(a-1)}{2!}x^2+\cdots+\cfrac{a(a-1)\cdots(a-n+1)}{n!}x^n+o(x^n)$$
	则$\sqrt{1+x^2}$的泰勒展开式是
	$$(1+x^2)^{\cfrac{1}{2}} = 1 + \cfrac{1}{2}x^2 + \cfrac{\cfrac{1}{2}\cdot(\cfrac{1}{2}-1)}{2!}x^4 + \cfrac{\cfrac{1}{2}\cdot(\cfrac{1}{2}-1)\cdot(\cfrac{1}{2}-2)}{3!}x^6+\cdots + o(x^2n)$$
	如果展成一阶泰勒公式，即
	$$(1+x^2)^{\cfrac{1}{2}} = 1 + \cfrac{1}{2}x^2 + o(x^2)$$
	则有$1+\cfrac{1}{2}x^2-\sqrt{1+x^2}=o(x^2)$，显然分子极限于余项$o(x^2)$有关，所以展到一阶是不够的，因此应该至少展到二阶，即
	$$(1+x^2)^{\cfrac{1}{2}}=1+\cfrac{1}{2}x^2-\cfrac{1}{8}x^4+o(x^4)$$
	则有$1+\cfrac{1}{2}x^2=\sqrt{1+x^2}=-\cfrac{1}{8}x^4+o(x^4)$，显然分子的极限是由$-\cfrac{1}{8}x^4$决定的，与余项$o(x^4)$无关。所以将$\sqrt{1+x^2}$展成二阶泰勒公式就可以了，自然不必展成三阶的。