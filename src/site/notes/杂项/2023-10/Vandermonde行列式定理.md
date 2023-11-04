---
{"dg-publish":true,"permalink":"/杂项/2023-10/Vandermonde行列式定理/","dgPassFrontmatter":true}
---

$$
\left | \begin{matrix} 1& 1& 1& \cdots& 1 \\ a_1& a_2& a_3& \cdots& a_n \\ a_1^2& a_2^2& a_3^2& \cdots& a_n^2 \\ \vdots& \vdots& \vdots& \ddots& \vdots \\ a_1^{n-1}& a_2^{n-1}& a_3^{n-1}& \cdots& a_n^{n-1} \\ \end{matrix} \right | = \prod_{1\le j< i\le n}(a_i-a_j)
$$
- **例1**
	求：
	$$\left | \begin{matrix}	1& 1& 1& 1\\	1& 2& 3& 4\\	1& 4& 9& 16\\
	1& 8& 27& 64\\	\end{matrix} \right |$$
	解：
	$$\left | \begin{matrix}	1& 1& 1& 1\\	1& 2& 3& 4\\	1& 4& 9& 16\\	1& 8& 27& 64\\	\end{matrix} \right |	=(2-1)(3-1)(3-2)(4-1)(4-2)(4-3)$$
	该行列式为4阶范德蒙行列式，$a_n$分别为$1, 2, 3, 4$，所有的后减前相乘即得到行列式解
- **例2**
	求：
	$$D=\left | \begin{matrix}	1& 1& 1& 1\\	a& b& c& d\\	a^2& b^2& c^2& d^2\\	a^4& b^4& c^4& d^4\\	\end{matrix} \right |$$
	解：$D$的形式类似范德蒙行列式，若要求解$D$，则要补足范德蒙行列式$P$
	$$P=\left | \begin{matrix}	1& 1& 1& 1& 1\\	a& b& c& d& x\\	a^2& b^2& c^2& d^2& x^2\\	a^3& b^3& c^3& d^3& x^3\\	a^4& b^4& c^4& d^4& x^4\\	\end{matrix} \right |	=(b-a)(c-a)(c-b)(d-a)(d-b)(d-c)\textcolor{cyan}{(x-a)(x-b)(x-c)(x-d)}$$
	把$P$按第五列展开，则有
	$$P=A_{51}-x\cdot A_{52}+x^2\cdot A_{53}-x^3\cdot A_{54}+x^4\cdot A_{55}$$
	要求$D$，即求$P$中$A_{54}$，即$x^3$的系数相反数，即
	$$D=(b-a)(c-a)(c-b)(d-a)(d-b)(d-c)\textcolor{cyan}{(a+b+c+d)}$$