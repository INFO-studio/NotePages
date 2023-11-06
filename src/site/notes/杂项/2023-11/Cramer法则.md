---
{"dg-publish":true,"permalink":"/杂项/2023-11/Cramer法则/","dgPassFrontmatter":true}
---

若有线性方程组$\textbf{A}\textbf{x}=\textbf{c}$，其中
$$
\textbf{A}=\left ( \begin{matrix} a_{11}& a_{12}& \cdots& a_{1n}\\ a_{21}& a_{22}& \cdots& a_{2n}\\ \vdots& \vdots& \ddots& \vdots\\ a-{n1}& a_{n2}& \cdots& a_{nn}\\ \end{matrix} \right ), \quad \textbf{x}=\left ( \begin{matrix} x_1\\ x_2\\ \vdots\\ x_{n} \end{matrix} \right ), \quad \textbf{c}=\left ( \begin{matrix} c_1\\ c_2\\ \vdots\\ c_{n} \end{matrix} \right )
$$
定义$\textbf{A}_i$为$\textbf{A}$将第$i$列更换为$\textbf{c}$后得到的矩阵，则Carmer法则说明：
若$\det(\textbf{A}) \neq \textbf{0}$，那么方程组有解$x$，其中
$$
x_i=\cfrac{\det(\textbf{A}_i)}{\det(\textbf{A})}
$$
- 特别地，若$c=\textbf{0}$，则称方程组为齐次方程组，方程组至少有解$\textbf{x}=\textbf{0}$，在齐次方程组中：
	- 若$\det(\textbf{A}) \neq 0$，则方程组只有解$\textbf{x}=\textbf{0}$
	- 若$\det(\textbf{D}) = 0$，则方程组一定有解$\textbf{x}=\textbf{0}$和另至少一解$\textbf{x} \neq \textbf{0}$
	- 若方程组有解$\textbf{x} \neq \textbf{0}$，则$\det(\textbf{D}) = 0$