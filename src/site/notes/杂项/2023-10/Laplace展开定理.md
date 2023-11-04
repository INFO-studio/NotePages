---
{"dg-publish":true,"permalink":"/杂项/2023-10/Laplace展开定理/","dgPassFrontmatter":true}
---

行列式内取定$k$行，由$k$行元素组成的所有$k$阶子式与其代数余子式的乘积之和为行列式的值
$$
\left | \begin{matrix}
a_{11}& \cdots& a_{1p}& 0& \cdots& 0\\
\vdots& \ddots& \vdots& \vdots& \ddots& \vdots\\
a_{p1}& \cdots& a_{pp}& 0& \cdots& 0\\
c_{11}& \cdots& c_{1p}& b_{11}& \cdots& b_{1q}\\
\vdots& \ddots& \vdots& \vdots& \ddots& \vdots\\
c_{q1}& \cdots& c_{qp}& b_{q1}& \cdots& b_{qq}\\
\end{matrix} \right |=
\left | \begin{matrix}
a_{11}& \cdots& a_{1p}\\
\vdots& \ddots& \vdots\\
a_{p1}& \cdots& a_{pp}\\
\end{matrix} \right | \cdot
\left | \begin{matrix}
b_{11}& \cdots&  b_{1q}\\
\vdots& \ddots& \vdots\\
b_{q1}& \cdots& b_{qq}
\end{matrix} \right |
$$
- 更一般地，
	$$
	\left | \begin{matrix}
	A_1\\
	& A_2\\
	& & \ddots\\
	& & & A_t\\
	\end{matrix} \right | =
	\prod_{i=1}^{t}A_i\quad (A_i=
	\left | \begin{matrix}
	a_{11}& \cdots& a_{p1}\\
	\vdots& \ddots& \vdots\\
	a_{p1}& \cdots& a_{pp}\\
	\end{matrix} \right |)
	$$
- **例1**
	求：
	$$
	D=\left | \begin{matrix}
	2& -1& 1& 1& 2\\
	1& -2& -1& 3& 1\\
	0& 1& -1& 0& 1\\
	0& 2& -2& 0& 2\\
	0& 1& -1& 0& 1\\
	\end{matrix} \right |
	$$
	解：$D$的形式类似拉普拉斯行列式，要求解$D$，则要将其变换为符合拉普拉斯行列式的形式
	$$
	D=(-1)\cdot \left | \begin{matrix}
	2& 1& 1& -1& 2\\
	1& 3& -1& -2& 1\\
	0& 0& -1& 1& 1\\
	0& 0& -2& 2& 2\\
	0& 0& -1& 1& 1\\
	\end{matrix} \right |=
	\left | \begin{matrix}
	2& 1\\
	1& 3\\
	\end{matrix} \right | \cdot
	\left | \begin{matrix}
	-1& 1& 1\\
	-2& 2& 2\\
	-1& 1& 1\\
	\end{matrix} \right |
	=5 \cdot 0 = 0
	$$