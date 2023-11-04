---
{"dg-publish":true,"permalink":"/杂项/2023-11/函数极限L'Hôpital法则法/","dgPassFrontmatter":true}
---

当极限型是$\frac{0}{0}$或$\frac{\infty}{\infty}$时，就可以运用[[杂项/2023-10/L'Hôpital法则\|L'Hôpital法则]]，并且可以连续多次使用
需要注意的是，使用L'Hôpital法则前，先用[[杂项/2023-10/函数极限替换法\|函数极限替换法]]，[[杂项/2023-11/函数极限先算法\|函数极限先算法]]的方法，尽可能将极限化成比较简单的形式，确保运用L'Hôpital法则后，有更简单、明确的极限形式
- **例1**
	求：
	$$
	\lim\limits_{x \to a} \frac{\sin x - \sin a}{x - a}
	$$
	解：当$x \to a$时，极限是$\frac{0}{0}$型，运用L'Hôpital法则，得到
	$$
	\lim\limits_{x \to a} \frac{\sin x - \sin a}{x - a} = \lim\limits_{x \to a} \cos x = \cos a
	$$