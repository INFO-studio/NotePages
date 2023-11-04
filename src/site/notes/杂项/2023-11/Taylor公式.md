---
{"dg-publish":true,"permalink":"/杂项/2023-11/Taylor公式/","dgPassFrontmatter":true}
---

在数学中，Taylor公式是一个用函数在某点的信息描述其附近取值的公式
如果一个可微函数足够光滑的话，在已知函数在某一点的各阶导数值的情况下，Taylor公式可以用这些导数值做系数构建一个多项式来近似函数在这一点的邻域中的值。
设$n$是一个正整数。如果定义在一个包含$a$的区间上的函数$f$在$a$点处$n+1$次可导，那么对于这个区间的任意$x$，都有
$$
f(x) = f(a) + \frac{f'(a)}{1!}(x-a)+\frac{f^{(2)}(a)}{2!}(x-a)^2
+\cdots+\frac{f^{(n)}(a)}{n!}(x-a)^n+R_n(x)
$$
其中的多项式称为函数在$a$处的**Taylor展开式**，剩余的$R_n(x)$是Taylor公式的余项，是$(x-a)^n$的高阶无穷小。
当$n\to\infty$时，则有[[杂项/2023-11/Taylor级数\|Taylor级数]]。
$R_n(x)$的表达形式有若干种，分别以不同的数学家命名
- 带有Peano型余项的Taylor公式说明了多项式和函数的接近程度：
$$f(x) = f(a) + \frac{f'(a)}{1!}(x-a)+\frac{f^{(2)}(a)}{2!}(x-a)^2
+\cdots+\frac{f^{(n)}(a)}{n!}(x-a)^n+o[(x-a)^n]$$也就是说，当$x$无限趋近$a$时，余项$R_n(x)$将会是$(x-a)^n$的高阶无穷小，或者说多项式和函数的误差将远小于$(x-a)^n$。这个结论可以由下面更强的结论推出。
- 带有Lagrange型余项的Taylor公式可视为[[杂项/2023-11/Lagrange中值定理\|Lagrange中值定理]]的推广：
$$f(x) = f(a) + \frac{f'(a)}{1!}(x-a)+\frac{f^{(2)}(a)}{2!}(x-a)^2
+\cdots+\frac{f^{(n)}(a)}{n!}(x-a)^n+\frac{f^{(n+1)}(\theta)}{(n+1)!}(x-a)^{n+1}$$即$R_n(x)=\frac{f^{(n+1)}(\theta)}{(n+1)!}(x-a)^{n+1}$，其中$\theta \in (a,x)$。
- 带有积分型余项的Taylor公式可视为[[微积分基本定理\|微积分基本定理]]的推广：
$$f(x) = f(a) + \frac{f'(a)}{1!}(x-a)+\frac{f^{(2)}(a)}{2!}(x-a)^2
+\cdots+\frac{f^{(n)}(a)}{n!}(x-a)^n+\int_a^x\frac{f^{(n+1)}(t)}{(n+1)!}(x-t)^n\mathrm{d}t$$即$R_n(x)=\int_a^x\frac{f^{(n+1)}(t)}{(n+1)!}(x-t)^n\mathrm{d}t$。

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="//2023-11/taylor/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




当$x\to0$时，
$
e^x=1+x+\frac{1}{2!}x^2+\cdots+\frac{1}{n!}x^n+R_n(x)
$
$
\sin x = x - \frac{1}{3!}x^3+\frac{1}{5!}x^5+\cdots+\frac{(-1)^n}{(2n+1)!}x^{2n+1}+R_{2n+1}(x)
$
$
\cos x = 1 - \frac{1}{2!}x^2+\frac{1}{4!}x^4+\cdots+\frac{(-1)^n}{(2n)!}x^{2n}+R_{2n}(x)
$
$
\ln(1+x)=x-\frac{1}{2}x^2+\frac{1}{3}x^3+\cdots+\frac{(-1)^{n-1}}{n}x^n+R_n(x)
$
$
(1+x)^a = 1+ax+\frac{a(a-1)}{2!}x^2+\cdots+\frac{a(a-1)\cdots(a-n+1)}{n!}x^n+R_n(x)
$

</div></div>
