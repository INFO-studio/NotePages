---
{"dg-publish":true,"permalink":"/杂项/2023-11/一般函数不定积分凑微分法@todo/","dgPassFrontmatter":true}
---

**原理**：若$\displaystyle\int f(u)\mathrm{d}u=F(u)+C$则$\displaystyle\int f(\varphi(x))\mathrm{d}\varphi(x)=F(\varphi(x))+C$
凑微分是积分最基本的方法，也是求不定积分最简单的方法，因此在求不定积分时，我们首先考虑能否用凑微分法，将积分变成公式的形式

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- 凑成一次函数微分
	$\mathrm{d}x=\cfrac{1}{a}\mathrm{d}(ax+b)$
- 凑成$x^n$的微分
	$x^{n-1}\mathrm{d}x=\cfrac{1}{an}\mathrm{d}(ax^n+b)$
- 凑成倒微分
	$\cfrac{1}{x^2}\mathrm{d}x=-\mathrm{d}\left(\cfrac{1}{x}\right)$
- 凑成跟微分
	$\cfrac{1}{\sqrt{x}}\mathrm{d}x=2\mathrm{d}\left(\sqrt{x}\right)$
- 凑成指数函数微分
	$a^x\mathrm{d}x=\cfrac{1}{\ln a}\mathrm{d}(a^x)$
	$e^x\mathrm{d}x=\mathrm{d}(e^x)$
- 凑成对数函数微分
	$\cfrac{1}{x}\mathrm{d}x=\mathrm{d}(\ln x)$
- 凑成三角函数微分
	$\cos x\mathrm{d}x=\mathrm{d}\sin x$
	$\sin x\mathrm{d}x=-\mathrm{d}\cos x$
	$\sec^2x\mathrm{d}x=\cfrac{1}{cos^2x}\mathrm{d}x=\mathrm{d}\tan x$
	$\csc^2x\mathrm{d}x=\cfrac{1}{\sin^2x}\mathrm{d}x=-\mathrm{d}\cot x$
- 凑成反三角函数微分
	$\cfrac{1}{\sqrt{1-x^2}}\mathrm{d}x=\mathrm{d}\arcsin x$
	$\cfrac{1}{1+x^2}\mathrm{d}x=\mathrm{d}\arctan x$
- 凑成整体或局部的微分
	$f’(x)\mathrm{d}x=\mathrm{d}f(x)$

</div></div>

- **例1**
	求：
	$$\int\cfrac{1}{1-2x}\mathrm{d}x$$
	解：$\mathrm{d}x$可以凑成一次函数的微分，当然可以凑成分母$1-2x$的微分，从而有
	$$\int\cfrac{1}{1-2x}\mathrm{d}x=\int\cfrac{1}{1-2x}\mathrm{d}(1-2x)\cdot\left(-\cfrac{1}{2}\right)=-\cfrac{1}{2}\ln|1-2x|+C$$
- **例2**
	求：
	$$\int\cfrac{x^4}{(x^5+1)^4}\mathrm{d}x$$
	解：$x^4$和$\mathrm{d}x$可以凑成$x^5$的微分，当然可以凑成$\mathrm{d}(x^5+1)$，于是
	$$\int\cfrac{x^4}{(x^5+1)^4}\mathrm{d}x=\cfrac{1}{5}\int\cfrac{1}{(x^5+1)^4}\mathrm{d}(x^5+1)=-\cfrac{1}{15}\cfrac{1}{(x^5+1)^3}+C$$