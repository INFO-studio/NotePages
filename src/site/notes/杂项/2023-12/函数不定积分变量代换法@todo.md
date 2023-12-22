---
{"dg-publish":true,"permalink":"/杂项/2023-12/函数不定积分变量代换法@todo/","dgPassFrontmatter":true}
---

在变量代换中，通常有五种代换：根式代换、指数代换、对数代换、三角代换和反三角代换，其代换的目的是将被积函数化为有理函数、三角函数，或者两类不同函数积的形式。
在变量代换过程中，不仅被积函数改变，而且微元也在改变，这是不容忽视的问题。
- 
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="//2023-12//" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




如果被积函数含有指数函数，若不能凑微分，又不适用分部积分，一般是做指数代换，将被积函数化为有理函数。
- **例1**
	求：
	$\int\cfrac{e^{2x}\mathrm{d}x}{1+e^x}$
	解：令$e^x=t$，则$x=\ln t$，$\mathrm{d}x=\cfrac{1}{t}\mathrm{d}t$，于是
	$\begin{aligned}\int\cfrac{e^{2x}\mathrm{d}x}{1+e^x}&=\int\cfrac{t^2\mathrm{d}t}{t(1+t)}=\int\cfrac{t}{1+t}\mathrm{d}t=\int\mathrm{d}t-\int\cfrac{1}{1+t}\mathrm{d}t\\&=t+\ln|1+t|+C=e^x-\ln(1+e^x)+C\end{aligned}$
- **例2**
	求：
	$\int\cfrac{\mathrm{d}x}{\sqrt{1+e^x}}$
	解：令$\sqrt{e^x+1}=t$，则$e^x=t^2-1$，$e^x\mathrm{d}x=2t\mathrm{d}t$，$\mathrm{d}x=\cfrac{2t}{t^2-1}\mathrm{d}t$，于是
	$\int\cfrac{\mathrm{d}x}{\sqrt{1+e^x}}=\int\cfrac{2\mathrm{d}t}{t^2-1}=\int\left(\cfrac{1}{t-1}-\cfrac{1}{t+1}\right)\mathrm{d}t=\ln\left|\cfrac{t-1}{t+1}\right|+C=\ln\left|\cfrac{\sqrt{1+e^x}-1}{\sqrt{1+e^x}+1}\right|+C$

</div></div>

- 
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="//2023-12//" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




如果被积函数含有对数函数，若不能凑微分，又不适用分部积分，一般是做对数代换，使被积函数化为有理函数或两类不同函数积的形式，然后应用分部积分。
- **例1**
	求：
	$\int\left(\cfrac{\ln x}{x}\right)^2\mathrm{d}x$
	解：令$t=\ln x$，则$x=e^t$，$\mathrm{d}x=e^t\mathrm{d}t$，于是
	$\begin{aligned}\int\left(\cfrac{\ln x}{x}\right)^2\mathrm{d}x&=\int t^2e^{-t}\mathrm{d}t=-t^2e^{-t}+\int2te^{-t}\mathrm{d}t=-t^2e^{-t}-2te^{-t}-2e^{-t}+C\\&=-\cfrac{1}{x}(\ln^2x+2\ln x+2)+C\end{aligned}$
- **例2**
	求：
	$\int\cos(\ln x)\mathrm{d}x$
	解：令$t=\ln x$，则$x=e^t$，$\mathrm{d}x=e^t\mathrm{d}t$，于是
	$\int\cos(\ln x)\mathrm{d}x=\int\cos te^t\mathrm{d}t=\cos te^t+\int\sin te^t\mathrm{d}t=\cos te^t+\sin te^t-\int\cos te^t\mathrm{d}t$
	$\therefore\int\cos(\ln x)\mathrm{d}x=\cfrac{1}{2}(\cos te^t+\sin te^t)+C=\cfrac{1}{2}x(\cos\ln x+\sin\ln x)+C$

</div></div>

- 
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="//2023-12//" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




一般地，如果被积函数含有二次根式，而且根式下是二次多项式，如$\sqrt{ax^2+bc+c}$。常常利用配方，将其化为$\sqrt{u^2\pm p^2}$或$\sqrt{p^2-u^2}$的形式，然后作三角代换。
- $\sqrt{a^2-x^2}$，作变量代换$x=a\sin t\quad(-\cfrac{\pi}{2}<t<\cfrac{\pi}{2})$，则
	$\sqrt{a^2-x^2}=a\cos t\quad,\quad\mathrm{d}x=a\cos t\mathrm{d}t$
- $\sqrt{a^2+x^2}$，作变量代换$x=a\tan t\quad(-\cfrac{\pi}{2}<t<\cfrac{\pi}{2})$，则
	$\sqrt{a^2+x^2}=a\sec t\quad,\quad\mathrm{d}x=\cfrac{a}{\cos^2t}\mathrm{d}t$
- $\sqrt{x^2-a^2}$，当$x>a$时，作变量代换$x=a\sec t\quad(0<t<\cfrac{\pi}{2})$，则
	$\sqrt{x^2-a^2}=a\tan t\quad,\quad\mathrm{d}x=a\sec t\tan t\mathrm{d}t$
	当$x<a$时，作负变换，令$x=-u$，则$u>a$，再利用$x>a$时的积分结果，得到$x<-a$时的不定积分。具体见例2
- **例1**
	求：
	$\int\cfrac{\mathrm{d}x}{x\sqrt{1-x^2}}$
	解：令$x=\sin t$，则$\mathrm{d}x=\cos t\mathrm{d}t$，于是
	$\int\cfrac{\mathrm{d}x}{x\sqrt{1-x^2}}=\int\cfrac{\cos t}{\sin t\cos t}\mathrm{d}t=\int\cfrac{1}{\sin t}\mathrm{d}t=\ln|\csc t-\cot t|+C=\ln\left|\cfrac{1-\sqrt{1-x^2}}{x}\right|+C$
- **例2**
	求：
	$\int\cfrac{\sqrt{x^2-a^2}}{x^4}\mathrm{d}x$
	解：当$x>a$时，令$x=a\sec t\quad(0<t<\cfrac{\pi}{2})$，则$\sqrt{x^2-a^2}=a\tan t$，$\mathrm{d}x=a\sec t\tan t\mathrm{d}t$
	$\begin{aligned}\int\cfrac{\sqrt{x^2-a^2}}{x^4}\mathrm{d}x&=\int\cfrac{a\tan t\cdot a\sec t\tan t}{a^4\sec^4t}\mathrm{d}t=\int\cfrac{\tan^2t}{a^2\sec^3t}\mathrm{d}t=\cfrac{1}{a^2}\int\sin^2t\cos t\mathrm{d}t\\&=\cfrac{1}{3a^2}\sin^3t+C=\cfrac{1}{3a^2}\left(\cfrac{\sqrt{x^2-a^2}}{x}\right)^3+C\end{aligned}$
	当$x<a$时，令$x=-u$，则$u>a$，$\mathrm{d}x=-\mathrm{d}u$，于是
	$\int\cfrac{\sqrt{x^2-a^2}}{x^4}\mathrm{d}x=-\int\cfrac{\sqrt{u^2-a^2}}{u^4}\mathrm{d}u=-\cfrac{1}{3a^2}\left(\cfrac{\sqrt{u^2-a^2}}{u}\right)^3+C=\cfrac{1}{3a^2}\left(\cfrac{\sqrt{x^2-a^2}}{x}\right)^3+C$
	所以
	$\int\cfrac{\sqrt{x^2-a^2}}{x^4}\mathrm{d}x=\cfrac{1}{3a^2}\left(\cfrac{\sqrt{x^2-a^2}}{x}\right)^3+C$

</div></div>

- 
<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



如果被积函数含有反三角函数，若不能凑微分，又不适用分部积分，一般是做反三角函数代换，使被积函数化为有理函数、无理函数和三角函数等形式。
- **例1**
	求：
	$\int\sin(\arctan x)\mathrm{d}x$
	解：令$\arctan x=t$，则$x=\tan t$，$\mathrm{d}x=\sec^2t\mathrm{d}t$，于是
	$\int\sin(\arctan x)\mathrm{d}x=\int\cfrac{\sin t}{\cos^2t}\mathrm{d}t=-\int\cfrac{1}{\cos^2t}\mathrm{d}\cos t=\cfrac{1}{\cos t}+C=\sqrt{1+x^2}+C$
- **例2**
	求：
	$\int\cfrac{\arccos x}{x^2\sqrt{1-x^2}}\mathrm{d}x$
	解：令$\arccos x=t$，则$x=\cos t\quad(0<t<\pi)$，$\mathrm{d}x=-\sin t\mathrm{d}t$，于是
	$\begin{aligned}\int\cfrac{\arccos x}{x^2\sqrt{1-x^2}}\mathrm{d}x&=-\int\cfrac{t\sin t}{\cos^2t\sin t}\mathrm{d}t=-\int\cfrac{t}{\cos^2t}\mathrm{d}t=-t\tan t+\int\tan t\mathrm{d}t\\&=-t\tan t-\ln|\cos t|+C=-\arccos x\cdot\tan(\arccos x)-\ln|x|+C\end{aligned}$

</div></div>
