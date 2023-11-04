---
{"dg-publish":true,"permalink":"/杂项/2023-10/Stolz-Cesàro定理/","dgPassFrontmatter":true}
---

$\{a_n\}$以及$\{b_n\}$为两个实数数列
若$\{b_n\}$是个严格单调且发散的数列（即严格递增并接近无穷大，或者严格递减并接近负无穷大），且下述极限存在：
$$
\lim\limits_{n \to \infty} \frac{x_{n+1}-x_n}{y_{n+1}-y_n}
$$
则有
$$
\lim\limits_{n \to \infty} \frac{x_n}{y_n} = 
\lim\limits_{n \to \infty} \frac{x_{n+1}-x_n}{y_{n+1}-y_n}
$$
同样，若$\lim\limits_{n \to \infty} a_n \to 0$以及$\lim\limits_{n \to \infty} b_n \to 0$，并且$\{b_n\}$严格单调，则有
$$
\lim\limits_{n \to \infty} \frac{x_n}{y_n} = 
\lim\limits_{n \to \infty} \frac{x_{n+1}-x_n}{y_{n+1}-y_n}
$$