> 注：一些用到的简称如下。
>
> - MCT: the Monotone Convergence Theorem.
> - MI: Mathematical Induction.

# 第二章

## 第一节

### 1. 下述几种说法与数列极限定义是否等价? 说明理由.

注: 为方便区分, 极限定义中的 $\varepsilon$, $N$ 在下文分别记作 $\varepsilon_l$, $N_l$.

#### (1) 对任意给定的 $\varepsilon>0$, 存在正整数 $N$, 当 $n\geq N$ 时, $\left|x_n−A\right|\leq\varepsilon$.

是. 下证该描述为数列极限定义的充要条件.

充分性:
对于任意给定 $\varepsilon_l>0$, 取 $\displaystyle\varepsilon=\frac{\varepsilon_l}2$, $N_l=N$, 由上述命题, 有 $\displaystyle\forall\,n>N_l:\left|x_n-A\right|\leq\varepsilon<\varepsilon_l$.

必要性:
对于任意给定 $\varepsilon>0$, 取 $\varepsilon_l=\varepsilon$, $N=N_l+1$, 由极限定义, $\displaystyle\forall\,n\geq N:\left|x_n-A\right|\leq\varepsilon$.

#### (2) 存在正整数 $N$, 对任意给定的 $\varepsilon>0$, 当 $n>N$ 时, $\left|x_n−A\right|<\varepsilon$.

否. 该描述并非数列极限定义的必要条件. 下举反例.

对于数列 $\displaystyle\left\{\frac1n\right\}$, 对任意给定 $\varepsilon_l>0$, 取 $\displaystyle N_l=\left[\frac1{\varepsilon_l}\right]+1$. 则当 $n>N_l$ 时, 有 $\displaystyle\left|\frac1n-0\right|=\frac1n<\varepsilon_l$.

然而, 对于任意给定 $N\in\N^*$, 取 $\displaystyle\varepsilon=\frac1{N+1}$, 当 $n=N+1>N$, 有 $\displaystyle\left|\frac1n-0\right|=\frac1{N+1}=\varepsilon$.

#### (3) $\forall\,0<\varepsilon<1$, 存在正整数 $N$, 当 $n>N$ 时, $\left|x_n-A\right|<\varepsilon$.

是. 下证该描述为数列极限定义的充要条件.

充分性:
对于任意给定 $\varepsilon_l>0$, 取 $\varepsilon=\min\left\{\varepsilon_l,0.9\right\}$, $N_l=N$, 由上述命题, $\displaystyle\forall\,n>N_l:\left|x_n-A\right|<\varepsilon\leq\varepsilon_l$.

必要性显然.

#### (4) $\forall\,\varepsilon>0$, 存在正整数 $N$, 当 $n>N$ 时, $\left|x_n-A\right|<k\varepsilon$, 此处 $k$ 是与 $\varepsilon$ 无关的正数.

是. 下证该描述为数列极限定义的充要条件.

充分性:
对于任意给定 $\varepsilon_l>0$, 取 $\varepsilon=\varepsilon_l/k$, $N_l=N$, 由上述命题, $\displaystyle\forall\,n>N_l:\left|x_n-A\right|<k\varepsilon=\varepsilon_l$.

必要性:
对于任意给定 $\varepsilon>0$, 取 $\varepsilon_l=k\varepsilon$, $N=N_l$, 由上述命题, $\displaystyle\forall\,n>N:\left|x_n-A\right|<\varepsilon_l=k\varepsilon$.

#### (5) 对任意给定的正整数 $m$, 存在正整数 $N$, 当 $n>N$ 时, $\displaystyle\left|x_n-A\right|<\frac1m$.

是. 下证该描述为数列极限定义的充要条件.

充分性:
对于任意给定 $\varepsilon_l>0$, 取 $\displaystyle m=\left[\frac1{\varepsilon_l}\right]+1>\frac1{\varepsilon_l}$, $N_l=N$, 由上述命题, $\displaystyle\forall\,n>N_l:\left|x_n-A\right|<\frac1m<\varepsilon_l$.

必要性:
对于任意给定 $m\in\N^*$, 取 $\displaystyle\varepsilon_l=\frac1m$, $N=N_l$, 由极限定义, $\displaystyle\forall\,n>N:\left|x_n-A\right|<\varepsilon_l=\frac1m$.

#### (6) $\forall\,\varepsilon>0$, 存在无限多个 $x_n$, 满足 $\left|x_n-A\right|<\varepsilon$.

否. 该描述并非数列极限定义的充分条件. 下举反例.

对于数列 $\left\{\left(-1\right)^n\right\}$, 对任意给定 $\varepsilon>0$, 当 $n=2k$ ($k\in\N^*$) 时, 有 $\left|\left(-1\right)^n-1\right|=0<\varepsilon$.

然而, 取 $\varepsilon_l=1$, 对于任意 $N\in\N^*$, $\left|x_{N+1}-1\right|+\left|x_{N+2}-1\right|\geq\left|\left(x_{N+1}-1\right)-\left(x_{N+2}-1\right)\right|=\left|\left(-1\right)^{N+1}-\left(-1\right)^{N+2}\right|=2$.

又由 $\left|x_{N+1}-1\right|\geq0$, $\left|x_{N+2}-1\right|\geq0$, 可知 $\left|x_{N+1}-1\right|$ 和 $\left|x_{N+2}-1\right|$ 中至少有一者不小于 $1$, 即 $\varepsilon_l$.

### 2. 按定义证明下列极限:

#### (1) $\displaystyle\lim_{n\to\infty}\frac1{n\left(n+1\right)}=0$.

$$
\frac1{n\left(n+1\right)}<\frac1{n^2}
$$

对任意给定 $\varepsilon>0$, 取 $\displaystyle N=\left[\sqrt{\frac1\varepsilon}\right]+1$. 则当 $n>N$ 时, 有 $\displaystyle\left|\frac1{n\left(n+1\right)}-0\right|<\frac1{n^2}<\varepsilon$.

#### (2) $\displaystyle\lim_{n\to\infty}\frac{3n^2+n+1}{2n^2-1}=\frac32$.

$$
\left|\frac{3n^2+n+1}{2n^2-1}-\frac32\right|=\left|\frac{2n+5}{4n^2-2}\right|
$$

当 $n\in\N^*$, 有 $7n\geq2n+5>0$, $4n^2\geq2n^2>0$. 故:
$$
\left|\frac{3n^2+n+1}{2n^2-1}-\frac32\right|=\frac{2n+5}{4n^2-2}\leq\frac{7n}{2n^2}=\frac7{2n}
$$
对任意给定 $\varepsilon>0$, 取 $\displaystyle N=\left[\frac7{2\varepsilon}\right]+1$. 则当 $n>N$ 时, 有 $\displaystyle\left|\frac{3n^2+n+1}{2n^2-1}-\frac32\right|\leq\frac7{2n}<\varepsilon$.

#### (3) $\displaystyle\lim_{n\to\infty}\frac{\sqrt{n^2+n}}n=1$.

$$
\left|\frac{\sqrt{n^2+n}}n-1\right|=\frac{\sqrt{n^2+n}-n}n=\frac1{\sqrt{n^2+n}+n}<\frac1n
$$

对任意给定 $\varepsilon>0$, 取 $\displaystyle N=\left[\frac1{\varepsilon}\right]+1$. 则当 $n>N$ 时, 有 $\displaystyle\left|\frac{\sqrt{n^2+n}}n-1\right|<\frac1n<\varepsilon$.

#### (4) $\displaystyle\lim_{n\to\infty}\arctan n=\frac\pi2$.

$$
\left|\arctan n-\frac\pi2\right|=\frac\pi2-\arctan n=\arctan\frac1n
$$

对任意给定 $\varepsilon>0$, 当 $\displaystyle\varepsilon\geq\frac\pi2$, 取 $N=1$, 当 $n>N$ 时, 恒有 $\displaystyle\left|\arctan n-\frac\pi2\right|=\arctan\frac1n<\varepsilon$; 
当 $\displaystyle\varepsilon<\frac\pi2$, 取 $N=\left[\cot\varepsilon\right]+1$, 当 $n>N$ 时, 有 $\displaystyle\left|\arctan n-\frac\pi2\right|=\arctan\frac1n<\varepsilon$.

#### (5) $\displaystyle\lim_{n\to\infty}\left(\ln\left(n+1\right)-\ln n\right)=0$.

$$
\left|\ln\left(n+1\right)-\ln n-0\right|=\ln\left(1+\frac1n\right)
$$

对任意给定 $\varepsilon>0$, 取 $\displaystyle N=\left[\frac1{e^\varepsilon-1}\right]+1$, 当 $n>N$ 时, 有 $\displaystyle\left|\ln\left(n+1\right)-\ln n-0\right|=\ln\left(1+\frac1n\right)<\varepsilon$.

### 3. 设 $\displaystyle\lim_{n\to\infty}x_n=A>0$, 求证存在正整数 $N$, 使得当 $n>N$ 时, 有 $\displaystyle\frac A2<x_n<\frac{3A}2$.

取 $\displaystyle\varepsilon=\frac A2$, 由极限定义, $\displaystyle\exist\,N\in\N^*:\forall\,n>N:\left|x_n-A\right|<\frac A2$, 即 $\displaystyle-\frac A2<x_n-A<\frac A2$, 即 $\displaystyle\frac A2<x_n<\frac{3A}2$.

### 4. 证明:

#### (1) $\displaystyle\lim_{n\to\infty}x_n=A\iff\lim_{k\to\infty}x_{2k}=\lim_{k\to\infty}x_{2k-1}=A$.

充分性:
对任意给定 $\varepsilon>0$, 取 $\varepsilon_e=\varepsilon_o=\varepsilon$.
由极限定义, $\exist\,N_e\in\N^*:\forall\,k>N_e:\left|x_{2k}-A\right|<\varepsilon_e$; $\exist\,N_o\in\N^*:\forall\,k>N_o:\left|x_{2k-1}-A\right|<\varepsilon_o$.
取 $N=\max\left\{2N_e,2N_o-1\right\}$, 当 $n>N$ 时, 有 $\left|x_n-A\right|<\varepsilon$.

必要性:
对任意给定 $\varepsilon>0$, 取 $\varepsilon_l=\varepsilon$, 由极限定义, $\exist\,N_l\in\N^*:\forall\,n>N_l:\left|x_n-A\right|<\varepsilon_l$.
取 $N=\left[N_l/2\right]+1$, 当 $k>N$ 时, 有 $2k>2k-1>N_l$, 故 $\left|x_{2k}-A\right|<\varepsilon_l=\varepsilon$, $\left|x_{2k-1}-A\right|<\varepsilon_l=\varepsilon$.

#### (2) $\left\{x_n\right\}$ 收敛 $\iff$ $\left\{x_{2k}\right\}$, $\left\{x_{2k-1}\right\}$ 和 $\left\{x_{3k}\right\}$ 都收敛.

充分性:
设 $\displaystyle\lim_{k\to\infty}x_{2k}=A$, $\displaystyle\lim_{k\to\infty}x_{2k-1}=B$, $\displaystyle\lim_{k\to\infty}x_{3k}=C$.
同 *(1)必要性* 易证:
$\displaystyle\lim_{k\to\infty}x_{6k}=\lim_{k\to\infty}x_{2\left(3k\right)}=A$, $\displaystyle\lim_{k\to\infty}x_{6k}=\lim_{k\to\infty}x_{3\left(2k\right)}=C$. 由极限的唯一性, 有 $A=C$.
$\displaystyle\lim_{k\to\infty}x_{6k-3}=\lim_{k\to\infty}x_{2\left(3k-1\right)-1}=B$, $\displaystyle\lim_{k\to\infty}x_{6k-3}=\lim_{k\to\infty}x_{3\left(2k-1\right)}=C$. 由极限的唯一性, 有 $B=C$.
故 $A=B=C$, 同 *(1)充分性* 易证 $\left\{x_n\right\}$ 收敛于 $A$.

必要性同 *(1)必要性* 易证.

### 5. 设数列 $\left\{x_n\right\}$ 有界, 且 $\displaystyle\lim_{n\to\infty}y_n=0$. 求证 $\displaystyle\lim_{n\to\infty}x_ny_n=0$.

由 $\left\{x_n\right\}$ 有界, 取 $M>0$ 使 $\forall\,n\in\N^*:\left|x_n\right|\leq M$.

对任意给定 $\varepsilon>0$, 取 $\displaystyle\varepsilon_y=\frac\varepsilon{\left|M\right|}$, 由极限定义, $\exist\,N_y\in\N^*:\forall\,n>N_y:\left|y_n-0\right|<\varepsilon_y$.

取 $N=N_y$, 当 $n>N$ 时, 有 $\left|x_ny_n-0\right|=\left|x_n\right|\left|y_n\right|<M\varepsilon_y=\varepsilon$.

### 6. 设 $x_n\geq0$, 且 $\displaystyle\lim_{n\to\infty}x_n=a\geq0$, 证明 $\displaystyle\lim_{n\to\infty}\sqrt{x_n}=\sqrt a$.

1. 若 $a=0$:

   对任意给定 $\varepsilon>0$, 取 $\varepsilon_s=\varepsilon^2$, 由极限定义, $\exist\,N_s\in\N^*:\forall\,n>N_s:\left|x_n-a\right|=x_n<\varepsilon_s$.

   取 $N=N_s$, 当 $n>N$, 由于 $x_n<\varepsilon^2$, 有 $\displaystyle\left|\sqrt{x_n}-\sqrt a\right|=\sqrt{x_n}<\varepsilon$.

2. 若 $a>0$:

   对任意给定 $\varepsilon>0$, 取 $\varepsilon_s=\varepsilon\sqrt a$, 由极限定义, $\exist\,N_s\in\N^*:\forall\,n>N_s:\left|x_n-a\right|<\varepsilon_s$.

   取 $N=N_s$, 当 $n>N$,
由于 $\left|x_n-a\right|=\left|\sqrt{x_n}-\sqrt a\right|\left(\sqrt{x_n}+\sqrt a\right)$, 有 $\displaystyle\left|\sqrt{x_n}-\sqrt a\right|<\frac{\varepsilon_s}{\sqrt{x_n}+\sqrt a}\leq\frac{\varepsilon_s}{\sqrt a}=\varepsilon$.

### 7.

#### (1) 设数列 $\left\{x_n\right\}$ 收敛而 $\left\{y_n\right\}$ 发散, 判断数列 $\left\{x_n+y_n\right\}$ 和 $\left\{x_ny_n\right\}$ 的敛散性.

$\left\{x_n+y_n\right\}$ 发散. 下证:
假设 $\left\{x_n+y_n\right\}$ 收敛, 设 $\displaystyle\lim_{n\to\infty}x_n=A$, $\displaystyle\lim_{n\to\infty}\left(x_n+y_n\right)=B$, 则 $\displaystyle\lim_{n\to\infty}y_n=\lim_{n\to\infty}\left(x_n+y_n-x_n\right)=B-A$.

$\left\{x_ny_n\right\}$ 无法判断. 下举例:
若 $x_n=1$ ($\forall\,n\in\N^*$), $y_n=n$ ($\forall\,n\in\N^*$), 则 $x_ny_n=n$ ($\forall\,n\in\N^*$), $\left\{x_ny_n\right\}$ 发散.
若 $x_n=0$ ($\forall\,n\in\N^*$), $y_n=n$ ($\forall\,n\in\N^*$), 则 $x_ny_n=0$ ($\forall\,n\in\N^*$), $\left\{x_ny_n\right\}$ 收敛.

#### (2) 设数列 $\left\{x_n\right\}$ 和 $\left\{y_n\right\}$ 都发散, 判断数列 $\left\{x_n+y_n\right\}$ 和 $\left\{x_ny_n\right\}$ 的敛散性.

$\left\{x_n+y_n\right\}$ 无法判断. 下举例:
若 $x_n=n$ ($\forall\,n\in\N^*$), $y_n=n$ ($\forall\,n\in\N^*$), 则 $x_n+y_n=2n$ ($\forall\,n\in\N^*$), $\left\{x_n+y_n\right\}$ 发散.
若 $x_n=-n$ ($\forall\,n\in\N^*$), $y_n=n$ ($\forall\,n\in\N^*$), 则 $x_n+y_n=0$ ($\forall\,n\in\N^*$), $\left\{x_n+y_n\right\}$ 收敛.

$\left\{x_ny_n\right\}$ 无法判断. 下举例:
若 $x_n=n$ ($\forall\,n\in\N^*$), $y_n=n$ ($\forall\,n\in\N^*$), 则 $x_ny_n=n^2$ ($\forall\,n\in\N^*$), $\left\{x_ny_n\right\}$ 发散.
若 $x_n=\left(-1\right)^n$ ($\forall\,n\in\N^*$), $y_n=\left(-1\right)^n$ ($\forall\,n\in\N^*$), 则 $x_ny_n=1$ ($\forall\,n\in\N^*$), $\left\{x_ny_n\right\}$ 收敛.

### 8. 求下列极限:

#### (1) $\displaystyle\lim_{n\to\infty}\frac{n^2+2n+5}{3n^2-n+1}$.

$$
\lim_{n\to\infty}\frac{n^2+2n+5}{3n^2-n+1}=\lim_{n\to\infty}\frac{\displaystyle1+\frac2n+\frac5{n^2}}{\displaystyle3-\frac1n+\frac1{n^2}}=\frac{\displaystyle\lim_{n\to\infty}1+\lim_{n\to\infty}\frac2n+\lim_{n\to\infty}\frac5{n^2}}{\displaystyle\lim_{n\to\infty}3-\lim_{n\to\infty}\frac1n+\lim_{n\to\infty}\frac1{n^2}}=\frac13
$$

#### (2) $\displaystyle\lim_{n\to\infty}\frac{1-2^n}{1+2^{n+1}}$.

$$
\lim_{n\to\infty}\frac{1-2^n}{1+2^{n+1}}=\lim_{n\to\infty}\frac{2^{-n}-1}{2^{-n}+2}=\frac{\displaystyle\lim_{n\to\infty}2^{-n}-\lim_{n\to\infty}1}{\displaystyle\lim_{n\to\infty}2^{-n}+\lim_{n\to\infty}2}=-\frac12
$$

#### (3) $\displaystyle\lim_{n\to\infty}\left(1-\frac{\sqrt{n^2+1}}n\right)\sin n$.

其中
$$
\lim_{n\to\infty}\left(1-\frac{\sqrt{n^2+1}}n\right)=\lim_{n\to\infty}-\frac1{\left(\sqrt{n^2+1}+n\right)n}=0
$$
而 $\left\{\sin n\right\}$ 有界.

由 *5* 易知 $\displaystyle\lim_{n\to\infty}\left(1-\frac{\sqrt{n^2+1}}n\right)\sin n=0$.

#### (4) $\displaystyle\lim_{n\to\infty}\frac{\displaystyle\sum_{i=1}^ni}{n^2}$.

$$
\lim_{n\to\infty}\frac{\displaystyle\sum_{i=1}^ni}{n^2}=\lim_{n\to\infty}\frac{\displaystyle\left(\frac{n\left(n+1\right)}2\right)}{n^2}=\lim_{n\to\infty}\frac{n^2+n}{2n^2}=\lim_{n\to\infty}\left(\frac12+\frac1{2n}\right)=\lim_{n\to\infty}\frac12+\lim_{n\to\infty}\frac1{2n}=\frac12
$$

#### (5) $\displaystyle\lim_{n\to\infty}\left(\sqrt{n+2}-2\sqrt{n+1}+\sqrt n\right)\sqrt{n^3}$.

$$
\begin{aligned}&\lim_{n\to\infty}\left(\sqrt{n+2}-2\sqrt{n+1}+\sqrt n\right)\sqrt{n^3}\\={}&\lim_{n\to\infty}\left(\frac1{\sqrt{n+2}+\sqrt{n+1}}-\frac1{\sqrt{n+1}+\sqrt n}\right)\sqrt{n^3}\\={}&\lim_{n\to\infty}\frac{\sqrt n-\sqrt{n+2}}{\left(\sqrt{n+2}+\sqrt{n+1}\right)\left(\sqrt{n+1}+\sqrt n\right)}\cdot\sqrt{n^3}\\={}&\lim_{n\to\infty}\frac{-2\sqrt{n^3}}{\left(\sqrt{n+2}+\sqrt{n+1}\right)\left(\sqrt{n+1}+\sqrt n\right)\left(\sqrt n+\sqrt{n+2}\right)}\\={}&\lim_{n\to\infty}\frac{-2}{\displaystyle\left(\sqrt{1+\frac2n}+\sqrt{1+\frac1n}\right)\left(\sqrt{1+\frac1n}+1\right)\left(1+\sqrt{1+\frac2n}\right)}\\={}&\frac{-2}{\left(1+1\right)\left(1+1\right)\left(1+1\right)}\\={}&-\frac14\end{aligned}
$$

## 第二节

### 1. 试用不等式方法证明下列极限:

#### (2) $\displaystyle\lim_{n\to\infty}\frac{n+5}{n^2+1}=0$.

当 $n\in\N^*$, 有 $\displaystyle0<\frac{n+5}{n^2+1}<\frac{6n}{n^2}=\frac6n$.

而 $\displaystyle\lim_{n\to\infty}\frac6n=\lim_{n\to\infty}0=0$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\frac{n+5}{n^2+1}=0$.

#### (4) $\displaystyle\lim_{n\to\infty}\frac{\sqrt{n^2+n}}n=1$.

当 $n\in\N^*$, 有 $\displaystyle1<\frac{\sqrt{n^2+n}}n=\sqrt{1+\frac1n}<1+\frac1n$.

而 $\displaystyle\lim_{n\to\infty}1=\lim_{n\to\infty}\left(1+\frac1n\right)=1$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\frac{\sqrt{n^2+n}}n=1$.

#### (6) $\displaystyle\lim_{n\to\infty}\left(\sqrt[n]{n+a}-\sqrt[n]n\right)=0$, $a>0$.

设 $x_n=\sqrt[n]{n+a}-1$ ($\forall\,n\in\N^*$), 则 $\displaystyle n+a=\left(1+x_n\right)^n\geq1+\frac{n\left(n-1\right)}2x_n^2$.

故当 $n\in\N^*$ 且 $n\geq2$, 有 $\displaystyle0<\sqrt[n]{n+a}-\sqrt[n]n<x_n\leq\sqrt{\frac{2\left(n+a-1\right)}{n\left(n-1\right)}}=\sqrt{\frac2n+\frac{2a}{n\left(n-1\right)}}$.

而 $\displaystyle\lim_{n\to\infty}0=\lim_{n\to\infty}\sqrt{\frac2n+\frac{2a}{n\left(n-1\right)}}=0$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\left(\sqrt[n]{n+a}-\sqrt[n]n\right)=0$.

#### (8) $\displaystyle\lim_{n\to\infty}\left(\left(\sqrt{n+1}-\sqrt n\right)\sqrt{n+\frac12}\right)=\frac12$.

$\displaystyle\left(\left(\sqrt{n+1}-\sqrt n\right)\sqrt{n+\frac12}\right)=\frac{\displaystyle\sqrt{n+\frac12}}{\sqrt{n+1}+\sqrt n}$.

当 $n\in\N^*$, 有 $\displaystyle\frac12=\frac{\displaystyle\sqrt{n+\frac12}}{\sqrt2\cdot\sqrt{2n+1}}<\frac{\displaystyle\sqrt{n+\frac12}}{\sqrt{n+1}+\sqrt n}<\frac{\displaystyle\sqrt{n+1}}{2\sqrt n}=\sqrt{\frac14+\frac1{4n}}$.

而 $\displaystyle\lim_{n\to\infty}\frac12=\lim_{n\to\infty}\sqrt{\frac14+\frac1{4n}}=\frac12$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\left(\left(\sqrt{n+1}-\sqrt n\right)\sqrt{n+\frac12}\right)=\frac12$.

### 2. 试用不等式方法求下列极限:

#### (1) $\displaystyle\lim_{n\to\infty}\frac{n^2+2n+5}{3n^2-n+1}$.

当 $n\in\N^*$, 有 $\displaystyle\frac{n^2+2n+5}{3n^2-n+1}=\frac13+\frac{7n+14}{9n^2-3n+3}>\frac13$.

另一方面, $\displaystyle\frac{n^2+2n+5}{3n^2-n+1}=\frac13+\frac{7n+14}{9n^2-3n+3}<\frac13+\frac{7n+14}{6n^2}=\frac13+\frac7{6n}+\frac7{3n^2}$.

而 $\displaystyle\lim_{n\to\infty}\frac13=\lim_{n\to\infty}\frac13+\frac7{6n}+\frac7{3n^2}=\frac13$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\frac{n^2+2n+5}{3n^2-n+1}=\frac13$.

#### (2) $\displaystyle\lim_{n\to\infty}\left(\sqrt{n+\sqrt n}-\sqrt n\right)$.

$$
\sqrt{n+\sqrt n}-\sqrt n=\frac{\sqrt n}{\sqrt{n+\sqrt n}+\sqrt n}=\frac1{\displaystyle\sqrt{1+\frac1{\sqrt n}}+1}
$$

当 $n\in\N^*$, 有 $\displaystyle\frac1{\displaystyle2+\frac1{\sqrt[4]n}}<\frac1{\displaystyle\sqrt{1+\frac1{\sqrt n}}+1}<\frac12$.

而 $\displaystyle\lim_{n\to\infty}\frac1{\displaystyle2+\frac1{\sqrt[4]n}}=\lim_{n\to\infty}\frac12=\frac12$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\left(\sqrt{n+\sqrt n}-\sqrt n\right)=\frac12$.

#### (3) $\displaystyle\lim_{n\to\infty}\left(1+\frac1{\sqrt n}\right)^{-n}$.

当 $n\in\N^*$, 有 $\displaystyle\left(1+\frac1{\sqrt n}\right)^{-n}>0$.

另一方面, 由 Bernoulli's Inequality, 有 $\displaystyle\left(1+\frac1{\sqrt n}\right)^n\geq1+\sqrt n$, 故 $\displaystyle\left(1+\frac1{\sqrt n}\right)^{-n}\leq\frac1{1+\sqrt n}$.

而 $\displaystyle\lim_{n\to\infty}0=\lim_{n\to\infty}\frac1{1+\sqrt n}=0$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\left(1+\frac1{\sqrt n}\right)^{-n}=0$.

#### (4) $\displaystyle\lim_{n\to\infty}\left(\sin\sqrt{n+1}-\sin\sqrt n\right)$.

$$
\sin\sqrt{n+1}-\sin\sqrt n=2\cos\frac{\sqrt{n+1}+\sqrt n}2\sin\frac{\sqrt{n+1}-\sqrt n}2
$$

当 $n\in\N^*$, 有 $\displaystyle-2\sin\frac1{2\left(\sqrt{n+1}+\sqrt n\right)}\leq2\cos\frac{\sqrt{n+1}+\sqrt n}2\sin\frac{\sqrt{n+1}-\sqrt n}2\leq2\sin\frac1{2\left(\sqrt{n+1}+\sqrt n\right)}$.

而 $\displaystyle\lim_{n\to\infty}2\sin\frac1{2\left(\sqrt{n+1}+\sqrt n\right)}=0$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\left(\sin\sqrt{n+1}-\sin\sqrt n\right)=0$.

#### (5) $\displaystyle\lim_{n\to\infty}\frac{\displaystyle\sum_{i=1}^n\sqrt[n]i}n$.

-   引理: $\displaystyle\lim_{n\to\infty}\sqrt[n]n=1$.

    设 $x_n=\sqrt[n]n-1$, 则 $\displaystyle n=\left(1+x_n\right)^n\geq1+\frac{n\left(n-1\right)}2x_n^2$.

    故当 $n\in\N^*$ 且 $n\geq2$, 有 $\displaystyle1<\sqrt[n]n=x_n+1\leq\sqrt{\frac2n}+1$.

    而 $\displaystyle\lim_{n\to\infty}1=\lim_{n\to\infty}\sqrt{\frac2n}+1=1$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\sqrt[n]n=1$.

当 $n\in\N^*$, 有 $\displaystyle1=\frac{\displaystyle\sum_{i=1}^n\sqrt[n]1}n\leq\frac{\displaystyle\sum_{i=1}^n\sqrt[n]i}n\leq\frac{\displaystyle\sum_{i=1}^n\sqrt[n]n}n=\sqrt[n]n$.

由 *引理* 可知, $\displaystyle\lim_{n\to\infty}1=\lim_{n\to\infty}\sqrt[n]n=1$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\frac{\displaystyle\sum_{i=1}^n\sqrt[n]i}n=1$.

#### (6) $\displaystyle\lim_{n\to\infty}\sqrt[n]{1+a^n}$, $a>0$.

-   引理: $\displaystyle\lim_{n\to\infty}\sqrt[n]t=1$, 其中 $t\in\R$ 且 $t>0$.

    1. 若 $0<t<1$:

       设 $\displaystyle x_n=\frac1{\sqrt[n]t}-1>0$, 由 Bernoulli's Inequality, $\displaystyle\frac1t=\left(1+x_n\right)^n\geq1+nx_n$.

       故当 $n\in\N^*$, 有 $\displaystyle\frac1{\displaystyle1+\frac{t^{-1}-1}n}\leq\frac1{1+x_n}=\sqrt[n]t<1$.

       而 $\displaystyle\lim_{n\to\infty}\frac1{\displaystyle1+\frac{t^{-1}-1}n}=\lim_{n\to\infty}1=1$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\sqrt[n]t=1$.

    2. 若 $t=1$ 显然.
    
    3. 若 $1<t$:

       设 $x_n=\sqrt[n]t-1>0$, 由 Bernoulli's Inequality, $t=\left(1+x_n\right)^n\geq1+nx_n$.

       故当 $n\in\N^*$, 有 $\displaystyle1<\sqrt[n]t=1+x_n\leq1+\frac{t-1}n$.

       而 $\displaystyle\lim_{n\to\infty}1=\lim_{n\to\infty}1+\frac{t-1}n=1$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\sqrt[n]t=1$.

1. 若 $0<a\leq1$:

   当 $n\in\N^*$, 有 $1<\sqrt[n]{1+a^n}\leq\sqrt[n]2$.

   由 *引理* 可知, $\displaystyle\lim_{n\to\infty}1=\lim_{n\to\infty}\sqrt[n]2=1$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\sqrt[n]{1+a^n}=1$.

2. 若 $1<a$:

   当 $n\in\N^*$, 有 $a<\sqrt[n]{1+a^n}\leq\sqrt[n]{2a^n}=a\sqrt[n]2$.

   由 *引理* 可知, $\displaystyle\lim_{n\to\infty}a=\lim_{n\to\infty}a\sqrt[n]2=a$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\sqrt[n]{1+a^n}=a$.

综上, $\displaystyle\lim_{n\to\infty}\sqrt[n]{1+a^n}=\max\left\{1,a\right\}$.

#### (7) $\displaystyle\lim_{n\to\infty}\sum_{i=1}^n\frac1{\sqrt{n^2+i}}$.

当 $n\in\N^*$, 有 $\displaystyle\frac1{\sqrt{\displaystyle1+\frac1n}}=\sum_{i=1}^n\frac1{\sqrt{n^2+n}}\leq\sum_{i=1}^n\frac1{\sqrt{n^2+i}}<\sum_{i=1}^n\frac1{\sqrt{n^2+0}}=1$.

而 $\displaystyle\lim_{n\to\infty}\frac1{\sqrt{\displaystyle1+\frac1n}}=\lim_{n\to\infty}1=1$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\sum_{i=1}^n\frac1{\sqrt{n^2+i}}=1$.

#### (8) $\displaystyle\lim_{n\to\infty}\sum_{i=0}^n\frac1{\left(n+i\right)^2}$.

当 $n\in\N^*$, 有 $\displaystyle0<\sum_{i=0}^n\frac1{\left(n+i\right)^2}<\sum_{i=0}^n\frac1{n^2}=\frac1n+\frac1{n^2}$.

而 $\displaystyle\lim_{n\to\infty}0=\lim_{n\to\infty}\frac1n+\frac1{n^2}=0$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\sum_{i=0}^n\frac1{\left(n+i\right)^2}=0$.

#### (9) $\displaystyle\lim_{n\to\infty}\sqrt[n]{\displaystyle\sum_{i=1}^ma_i^n}$, 其中 $m$ 为正整数, $a_k>0$ ($\forall\,k\in\N^*,k\leq m$).

不失一般性, 假设 $a_1=\max\left\{a_1,a_2,\cdots,a_m\right\}$.

当 $n\in\N^*$, 有 $\displaystyle a_1=\sqrt[n]{a_1^n}\leq\sqrt[n]{\displaystyle\sum_{i=1}^ma_i^n}\leq\sqrt[n]{\displaystyle\sum_{i=1}^ma_1^n}=a_1\sqrt[n]m$.

由 *(6)引理* 可知, $\displaystyle\lim_{n\to\infty}a_1=\lim_{n\to\infty}a_1\sqrt[n]m=a_1$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\sqrt[n]{\displaystyle\sum_{i=1}^ma_i^n}=a_1$.

根据假设, $\displaystyle\lim_{n\to\infty}\sqrt[n]{\displaystyle\sum_{i=1}^ma_i^n}=\max\left\{a_1,a_2,\cdots,a_m\right\}$.

### 3. 用不等式方法证明:

#### (1) $\displaystyle\lim_{n\to\infty}\left(\sqrt[n]{1+\frac an}-1\right)=0$, $a>0$.

当 $n\in\N^*$, 有 $\displaystyle0=\sqrt[n]1-1<\sqrt[n]{1+\frac an}-1\leq\sqrt[n]{1+a}-1$.

由 *2(6)引理* 可知, $\displaystyle\lim_{n\to\infty}0=\lim_{n\to\infty}\left(\sqrt[n]{1+a}-1\right)=0$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\left(\sqrt[n]{1+\frac an}-1\right)=0$.

#### (2) $\displaystyle\lim_{n\to\infty}\frac{n!}{n^n}=0$.

当 $n\in\N^*$, 有 $\displaystyle0<\frac{n!}{n^n}=\frac{\displaystyle\prod_{i=2}^ni}{n^n}\leq\frac{\displaystyle\prod_{i=2}^nn}{n^n}=\frac{n^{n-1}}{n^n}=\frac1n$.

而 $\displaystyle\lim_{n\to\infty}0=\lim_{n\to\infty}\frac1n=0$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\frac{n!}{n^n}=0$.

#### (3) $\displaystyle\lim_{n\to\infty}\frac{n^k}{n!}=0$, $k>0$.

当 $n\in\N^*$ 且 $n\geq2$, 有 $\displaystyle0<\frac{n^k}{n!}=\frac{n^k}{2^n}\cdot\frac{2^n}{n!}\leq\frac{n^k}{2^n}\cdot\frac4n$.

由 *(4)* 可知, $\displaystyle\lim_{n\to\infty}\frac{n^k}{2^n}=0$.

故 $\displaystyle\lim_{n\to\infty}0=\lim_{n\to\infty}\frac{n^k}{2^n}\cdot\frac4n=0$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\frac{n^k}{n!}=0$.

#### (4) $\displaystyle\lim_{n\to\infty}\frac{n^k}{a^n}=0$, $a>1$.

设 $m=\max\left\{\left[k\right]+1,1\right\}$. 则 $m\in\N^*$ 且 $m>k$.

设 $x=a-1$, 则当 $n\in\N^*$ 且 $n\geq m$ 时, $\displaystyle a^n=\left(1+x\right)^n\geq C_n^m x^m=\frac{\displaystyle\prod_{i=0}^{m-1}\left(n-i\right)}{m!}x^m$.

故当 $n\in\N^*$ 且 $n\geq m$ 时, 有 $\displaystyle0<\frac{n^k}{a^n}\leq\frac{m!\cdot n^k}{\displaystyle x^m\prod_{i=0}^{m-1}\left(n-i\right)}=\frac{m!}{\displaystyle x^m\prod_{i=0}^{m-1}\left(1-\frac in\right)}\cdot n^{k-m}$.

而 $\displaystyle\lim_{n\to\infty}0=\lim_{n\to\infty}\frac{m!}{\displaystyle x^m\prod_{i=0}^{m-1}\left(1-\frac in\right)}\cdot n^{k-m}=\frac{m!}{\displaystyle x^m\cdot\lim_{n\to\infty}\prod_{i=0}^{m-1}\left(1-\frac in\right)}\cdot\lim_{n\to\infty}n^{k-m}=\lim_{n\to\infty}\frac{m!}{x^m}\cdot0=0$,
由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\frac{n^k}{a^n}=0$.

#### (5) $\displaystyle\lim_{n\to\infty}\frac{a^n}{n!}=0$.

设 $t=\left[\left|a\right|\right]+1$. 则 $t\in\N^*$ 且 $t>\left|a\right|$.

当 $n\in\N^*$ 且 $n\geq t+1$, 有 $\displaystyle0\leq\frac{\left|a\right|^n}{n!}\leq\frac{\left|a\right|^{t+1}}{t!\cdot n}$.

而 $\displaystyle\lim_{n\to\infty}0=\lim_{n\to\infty}\frac{\left|a\right|^{t+1}}{t!\cdot n}=0$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\frac{\left|a\right|^n}{n!}=0$.

故 $\displaystyle\lim_{n\to\infty}\left|\frac{a^n}{n!}\right|=0$, 因此 $\displaystyle\lim_{n\to\infty}\frac{a^n}{n!}=0$.

#### (6) $\displaystyle\lim_{n\to\infty}\left(n^2+n\right)^{\tfrac1{2n+1}}=1$.

当 $n\in\N^*$, 有 $\displaystyle1<\left(n^2+n\right)^{\tfrac1{2n+1}}\leq\left(2n+1\right)^{\tfrac2{2n+1}}$.

由 *2(5)引理* 可知, $\displaystyle\lim_{n\to\infty}\left(2n+1\right)^{\tfrac1{2n+1}}=1$.

因此, $\displaystyle\lim_{n\to\infty}1=\lim_{n\to\infty}\left(2n+1\right)^{\tfrac2{2n+1}}=1$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\left(n^2+n\right)^{\tfrac1{2n+1}}=1$.

#### (7) $\displaystyle\lim_{n\to\infty}\left(\sum_{i=0}^ma_i\sqrt{n+i}\right)=0$, 其中 $m$ 为正整数, $\displaystyle\sum_{i=0}^ma_i=0$.

设 $\displaystyle P=\sum_{i=0}^m\left|a_i\right|/2$.

则 $\displaystyle-P\frac{m}{\sqrt n+\sqrt{n+m}}=P\sqrt n-P\sqrt{n+m}\leq\sum_{i=0}^ma_i\sqrt{n+i}\leq P\sqrt{n+m}-P\sqrt n=P\frac{m}{\sqrt n+\sqrt{n+m}}$.

而 $\displaystyle\lim_{n\to\infty}P\frac{m}{\sqrt n+\sqrt{n+m}}=0$, 由 the Squeeze Theorem, $\displaystyle\lim_{n\to\infty}\left(\sum_{i=0}^ma_i\sqrt{n+i}\right)=0$.

## 第三节

### 1. 利用 MCT 证明下列数列收敛, 并求极限:

#### (1) $x_1=\sqrt2$, $x_{n+1}=\sqrt{2x_n}$, $n=1,2,\cdots$.

当 $n=1$, 有 $\sqrt2\leq x_n<2$.

当 $n=k$, 假设 $\sqrt2\leq x_n<2$.
则当 $n=k+1$, $x_n=\sqrt{2x_k}>\sqrt2$, 且 $x_n=\sqrt{2x_k}<\sqrt{2\times2}=2$. 故有 $\sqrt2\leq x_n<2$.

由 MI, 有 $\forall\,n\in\N^*:\sqrt2\leq x_n<2$. 故 $\left\{x_n\right\}$ 有界.

$\displaystyle\forall\,n\in\N^*:\frac{x_n}{x_{n+1}}=\sqrt{\frac{x_n}2}<\sqrt{\frac22}=1$, 故 $\left\{x_n\right\}$ 单调递增.

由 MCT, $\left\{x_n\right\}$ 收敛. 设 $\displaystyle\lim_{n\to\infty}x_n=A$.

由 $x_{n+1}=\sqrt{2x_n}$, 有 $A^2=2A$, 解得 $A=0$ 或 $A=2$.
由 $\forall\,n\in\N^*:\sqrt2\leq x_n<2$, 有 $\sqrt2\leq A\leq2$, 故 $A=2$.

即 $\displaystyle\lim_{n\to\infty}x_n=2$.

#### (2) $0<x_1<1$, $x_{n+1}=x_n\left(1-x_n\right)$, $n=1,2,\cdots$.

当 $n=1$, 有 $0<x_n<1$.

当 $n=k$, 假设 $0<x_n<1$.
则当 $n=k+1$, $\displaystyle x_n=x_k\left(1-x_k\right)=\frac14-\left(x_k-\frac12\right)^2$, 故 $\displaystyle0<x_n\leq\frac14<1$.

由 MI, 有 $\forall\,n\in\N^*:0<x_n<1$. 故 $\left\{x_n\right\}$ 有界.

$\displaystyle\forall\,n\in\N^*:\frac{x_n}{x_{n+1}}=\frac1{1-x_n}>\frac11=1$, 故 $\left\{x_n\right\}$ 单调递减.

由 MCT, $\left\{x_n\right\}$ 收敛. 设 $\displaystyle\lim_{n\to\infty}x_n=A$.

由 $x_{n+1}=x_n\left(1-x_n\right)$, 有 $A=A\left(1-A\right)$, 解得 $A=0$. 即 $\displaystyle\lim_{n\to\infty}x_n=0$.

#### (3) $x_0=1$, $\displaystyle x_{n+1}=1+\frac{x_n}{1+x_n}$, $n=0,1,2,\cdots$.

当 $n=0$, 有 $\displaystyle1\leq x_n<\frac{\sqrt5+1}2$.

当 $n=k$, 假设 $\displaystyle1\leq x_n<\frac{\sqrt5+1}2$.
则当 $n=k+1$, $\displaystyle1+\frac{x_k}{1+x_k}>1$, 且 $\displaystyle1+\frac{x_k}{1+x_k}=2-\frac1{1+x_k}<2-\frac1{\displaystyle1+\frac{\sqrt5+1}2}=\frac{\sqrt5+1}2$.
故有 $\displaystyle1\leq x_n<\frac{\sqrt5+1}2$.

由 MI, 有 $\displaystyle\forall\,n\in\N^*:1\leq x_n<\frac{\sqrt5+1}2$. 故 $\left\{x_n\right\}$ 有界.

由 $\displaystyle\forall\,n\in\N^*:1\leq x_n<\frac{\sqrt5+1}2$ 可知 $-x_n^2+x_n+1>0$,
故 $\displaystyle\forall\,n\in\N^*:x_{n+1}-x_n=1+\frac{x_n}{1+x_n}-x_n=\frac{-x_n^2+x_n+1}{x_n+1}>0$, 故 $\left\{x_n\right\}$ 单调递增.

由 MCT, $\left\{x_n\right\}$ 收敛. 设 $\displaystyle\lim_{n\to\infty}x_n=A$.

由 $\displaystyle x_{n+1}=1+\frac{x_n}{1+x_n}$, 有 $\displaystyle A=1+\frac A{1+A}$, 解得 $\displaystyle A=\frac{1-\sqrt5}2$ 或 $\displaystyle A=\frac{\sqrt5+1}2$.
由 $\displaystyle\forall\,n\in\N^*:1\leq x_n<\frac{\sqrt5+1}2$, 有 $\displaystyle1\leq A\leq\frac{\sqrt5+1}2$, 故 $\displaystyle A=\frac{\sqrt5+1}2$.

即 $\displaystyle\lim_{n\to\infty}x_n=\frac{\sqrt5+1}2$.

#### (4) $x_0>0$, $\displaystyle x_{n+1}=\frac12\left(x_n+\frac a{x_n}\right)$, $a>0$, $n=0,1,2,\cdots$.

对于任意 $n\in\N^*$, $\displaystyle x_n=\frac12\left(x_{n-1}+\frac a{x_{n-1}}\right)>0$, 故 $\displaystyle\frac a{x_n}>0$.
故对于任意 $n\in\N^*$, $\displaystyle x_n=\frac12\left(x_{n-1}+\frac a{x_{n-1}}\right)\geq\sqrt a$.

则 $\displaystyle\forall\,n\in\N^*:x_{n+1}-x_n=\frac12\left(\frac a{x_n}-x_n\right)\leq\frac12\left(\sqrt a-\sqrt a\right)=0$, 故 $\left\{x_n\right\}$ 在 $n\in\N^*$ 单调递减.

故 $\forall\,n\in\N^*:\sqrt a\leq x_n\leq x_1$. 故 $\left\{x_n\right\}$ 有界.

由 MCT, $\left\{x_n\right\}$ 收敛. 设 $\displaystyle\lim_{n\to\infty}x_n=A$.

由 $\displaystyle x_{n+1}=\frac12\left(x_n+\frac a{x_n}\right)$, 有 $\displaystyle A=\frac12\left(A+\frac aA\right)$, 解得 $A=-\sqrt a$ 或 $A=\sqrt a$.
由 $\forall\,n\in\N^*:\sqrt a\leq x_n\leq x_1$, 有 $\sqrt a\leq A\leq x_1$, 故 $A=\sqrt a$.

### 2. 给定 $0<a<b$, 令 $x_1=a$, $y_1=b$.

#### (1) 若 $x_{n+1}=\sqrt{x_ny_n}$, $\displaystyle y_{n+1}=\frac{x_n+y_n}2$, $n=1,2,3,\cdots$, 证明 $\left\{x_n\right\}$, $\left\{y_n\right\}$ 收敛, 且 $\displaystyle\lim_{n\to\infty}x_n=\lim_{n\to\infty}y_n$, 称这个公共极限为 $a$ 与 $b$ 的算术几何平均.

由 AM-GM Inequality 和 MI 可知, $\forall\,n\in\N^*:x_n<y_n$. 因此 $x_{n+1}>x_n$, $y_{n+1}<y_n$.

因此 $\left\{x_n\right\}$ 单调递增, $\left\{y_n\right\}$ 单调递减. 故 $\forall\,n\in\N^*:a\leq x_n<y_n\leq b$.

由 MCT, $\left\{x_n\right\}$, $\left\{y_n\right\}$ 收敛. 设 $\displaystyle\lim_{n\to\infty}x_n=A$, $\displaystyle\lim_{n\to\infty}y_n=B$.

则由 $\displaystyle y_{n+1}=\frac{x_n+y_n}2$, 有 $\displaystyle B=\frac{A+B}2$, 故 $A=B$, 即 $\displaystyle\lim_{n\to\infty}x_n=\lim_{n\to\infty}y_n$.

#### (2) 若 $\displaystyle x_{n+1}=\frac{x_n+y_n}2$, $\displaystyle y_{n+1}=\frac{2x_ny_n}{x_n+y_n}$, $n=1,2,3,\cdots$, 证明 $\left\{x_n\right\}$, $\left\{y_n\right\}$ 收敛, 且 $\displaystyle\lim_{n\to\infty}x_n=\lim_{n\to\infty}y_n$, 称这个公共极限为 $a$ 与 $b$ 的算术调和平均.

由 AM-HM Inequality 和 MI 可知, $\forall\,n\in\N^*,n\geq2:x_n>y_n$. 因此当 $n\geq2$, 有 $x_{n+1}<x_n$, $y_{n+1}>y_n$.

因此 $\left\{x_n\right\}$ 在 $n\geq2$ 时单调递减, $\left\{y_n\right\}$ 在 $n\geq2$ 时单调递增. 故 $\forall\,n\in\N^*,n\geq2:a\leq y_n<x_n\leq b$.

由 MCT, $\left\{x_n\right\}$, $\left\{y_n\right\}$ 收敛. 设 $\displaystyle\lim_{n\to\infty}x_n=A$, $\displaystyle\lim_{n\to\infty}y_n=B$.

则由 $\displaystyle x_{n+1}=\frac{x_n+y_n}2$, 有 $\displaystyle A=\frac{A+B}2$, 故 $A=B$, 即 $\displaystyle\lim_{n\to\infty}x_n=\lim_{n\to\infty}y_n$.

### 3. 利用 $\displaystyle\lim_{n\to\infty}\left(1+\frac1n\right)^n=e$, 求下列极限:

#### (1) $\displaystyle\lim_{n\to\infty}\left(1-\frac1n\right)^n$.

当 $n\geq2$:
$$
\lim_{n\to\infty}\left(1-\frac1n\right)^n=\lim_{n\to\infty}\left(\frac{n-1}n\right)^n=\lim_{n\to\infty}\left(\left(1+\frac1{n-1}\right)^{n-1}\cdot\left(1+\frac1{n-1}\right)\right)^{-1}=e^{-1}
$$

#### (2) $\displaystyle\lim_{n\to\infty}\left(\frac{3n+1}{3n+2}\right)^n$.

$$
\lim_{n\to\infty}\left(\frac{3n+1}{3n+2}\right)^n=\lim_{n\to\infty}\left(\left(1-\frac1{3n+2}\right)^{3n+2}\cdot\left(1-\frac1{3n+2}\right)^{-2}\right)^{\tfrac13}=e^{-\tfrac13}
$$

### 4. 证明 $\displaystyle\frac1{n+1}<\ln\left(1+\frac1n\right)<\frac1n$, $n=1,2,\cdots$.

构造数列 $\left\{x_n\right\}$, $\left\{y_n\right\}$ 满足 $\displaystyle x_n=\left(1+\frac1n\right)^n$, $\displaystyle y_n=\left(1+\frac1n\right)^{n+1}$, $n=1,2,\cdots$. 则 $\forall\,n\in\N^*:x_n<y_n$.

由 Bernoulli's Inequality:
$$
\begin{aligned}\frac{x_{n+1}}{x_n}&=\frac{n^n\left(n+2\right)^{n+1}}{\left(n+1\right)^{2n+1}}=\left(1-\frac1{n^2+2n+1}\right)^n\frac{n+2}{n+1}\\&\geq\frac{\left(n^2+n+1\right)\left(n+2\right)}{\left(n^2+2n+1\right)\left(n+1\right)}=\frac{n^3+3n^2+3n+2}{n^3+3n^2+3n+1}>1\end{aligned}
$$

$$
\begin{aligned}\frac{y_n}{y_{n+1}}&=\frac{\left(n+1\right)^{2n+3}}{n^{n+1}\left(n+2\right)^{n+2}}=\left(1+\frac1{n^2+2n}\right)^{n+1}\frac{n+1}{n+2}\\&\geq\frac{\left(n^2+3n+1\right)\left(n+1\right)}{\left(n^2+2n\right)\left(n+2\right)}=\frac{n^3+4n^2+4n+1}{n^3+4n^2+4n}>1\end{aligned}
$$

故 $\left\{x_n\right\}$ 单调递增, $\left\{y_n\right\}$ 单调递减. 故 $\forall\,n\in\N^*:2=x_1\leq x_n<y_n\leq y_1=4$. 故 $\left\{x_n\right\}$, $\left\{y_n\right\}$ 有界.
由 MCT, $\left\{x_n\right\}$, $\left\{y_n\right\}$ 收敛.

由自然常数 $e$ 的定义, $\displaystyle\lim_{n\to\infty}x_n=e$; $\displaystyle\lim_{n\to\infty}y_n=\lim_{n\to\infty}\left(1+\frac1n\right)x_n=e$. 故 $\displaystyle\lim_{n\to\infty}\left(y_n-x_n\right)=0$.

由 Cantor's Nested Interval Theorem, $\forall\,n\in\N^*:e\in\left[x_n,y_n\right]$.
因此, $\forall\,n\in\N^*:e\in\left[x_{n+1},y_{n+1}\right]\subset\left(x_n,y_n\right)$, 即:
$$
\left(1+\frac1n\right)^n<e<\left(1+\frac1n\right)^{n+1}\\n\ln\left(1+\frac1n\right)<1<\left(n+1\right)\ln\left(1+\frac1n\right)\\n<\frac1{\displaystyle\ln\left(1+\frac1n\right)}<n+1\\ \frac1{n+1}<\ln\left(1+\frac1n\right)<\frac1n
$$

### 7. 设 $X$ 是无限集, $a>0$, 且对任何 $x_1,x_2\in X$, $x_1\neq x_2$, 都有 $\left|x_1-x_2\right|\geq a$, 求证集 $X$ 是无界集.

假设集 $X$ 为有界集, 则存在常数 $M$ 使 $\forall\,x\in X:|x|<M$. 设 $\displaystyle n=\left[\frac{2M}a\right]+1$.

设 $Y_i=\left\{x\in X\mid x\in\left(-M+\left(i-1\right)a,-M+ia\right]\right\}$, $i=1,2,\cdots,n$. 则 $\displaystyle\bigcup_{i=1}^nY_i=X$.

则存在 $t\in\N^*$, $t\leq n$ 使得 $Y_t$ 为无限集. 取 $p,q\in Y_t$, $p\neq q$, 则 $-M+\left(t-1\right)a<p,q\leq-M+ta$.
故 $\left|p-q\right|<-M+ta-\left(-M+\left(t-1\right)a\right)=a$.

然而 $p,q\in X$, 故 $\left|p-q\right|\geq a$. 矛盾. 故集 $X$ 为无界集.

### 8. 证明下列集合有界:

#### (1) $\displaystyle\left\{1+\frac{\cos n}{n^2}\mid n\in\N^*\right\}$.

$$
0=1-\frac11\leq1-\frac1{n^2}\leq1+\frac{\cos n}{n^2}\leq1+\frac1{n^2}\leq1+\frac11=2
$$

故 $\displaystyle\forall\,x\in\left\{1+\frac{\cos n}{n^2}\mid n\in\N^*\right\}:0\leq x\leq2$. 故 $\displaystyle\left\{1+\frac{\cos n}{n^2}\mid n\in\N^*\right\}$ 有界.

### 9. 证明下列集合无界:

#### (1) $\displaystyle\left\{\frac{n+2}{\sqrt n-1}\mid n\in\N^*,n\geq2\right\}$.

对于任意给定 $M>0$, 取 $n=\max\left\{\left[M^2\right]+1,2\right\}$, 则 $\sqrt n>M$, $\sqrt n-1\geq0$.

故有 $\sqrt n\left(\sqrt n-M\right)+M+2>0$, 则 $\displaystyle\frac{n+2}{\sqrt n-1}>M$ 且 $\displaystyle\frac{n+2}{\sqrt n-1}\in\left\{\frac{n+2}{\sqrt n-1}\mid n\in\N^*,n\geq2\right\}$.

故 $M$ 不为 $\displaystyle\left\{\frac{n+2}{\sqrt n-1}\mid n\in\N^*,n\geq2\right\}$ 的上界. 因此, $\displaystyle\left\{\frac{n+2}{\sqrt n-1}\mid n\in\N^*,n\geq2\right\}$ 无上界, 故无界.

### 10. 设 $a\geq0$, 且对任意 $\varepsilon>0$, 都有 $a-\varepsilon\leq0$, 试用 the Supremum and Infimum Principle 证明 $a=0$.

构造集合 $E=\left\{\varepsilon\in\R\mid\varepsilon>0\right\}$, 则 $0$ 为 $E$ 的一个下界.

由 the Infimum Principle, $E$ 有下确界 $\inf E$.

对于任意给定 $M>0$, 取 $\displaystyle\varepsilon=\frac M2$, 则 $\varepsilon\in E$ 且 $\varepsilon<M$. 故 $M$ 不为 $E$ 的下界.

因此, $\inf E=0$.

由于 $\forall\,\varepsilon\in E:a\leq\varepsilon$, 有 $a$ 为 $E$ 的一个下界. 故 $a\leq\inf E=0$.

结合 $a\geq0$, 有 $a=0$.

### 12. 求下列数集的上下确界:

#### (1) $\left\{x\mid x\in\Q,x>0\right\}$.

上确界:
对于任意给定 $M>0$, 取 $\displaystyle x=\left[M\right]+1$, 则 $x\in\left\{x\mid x\in\Q,x>0\right\}$ 且 $x>M$.
故 $M$ 不为 $\left\{x\mid x\in\Q,x>0\right\}$ 的上界. 因此, $\left\{x\mid x\in\Q,x>0\right\}$ 无上界, 故无上确界.

下确界:
$\forall\,x\in\left\{x\mid x\in\Q,x>0\right\}:x>0$, 故 $0$ 为 $\left\{x\mid x\in\Q,x>0\right\}$ 的一个下界.
对任意给定 $\varepsilon>0$, 取 $\displaystyle x=\frac1{\left[1/\varepsilon\right]+1}$, 则 $x\in\left\{x\mid x\in\Q,x>0\right\}$ 且 $x<0+\varepsilon$.
由下确界的充要条件, $\inf\left\{x\mid x\in\Q,x>0\right\}=0$.

#### (3) $\displaystyle\left\{n\sin\frac{n\pi}4\mid n\in\N^*\right\}$.

上确界:
对于任意给定 $M>0$, 取 $x=8\left(\left[M/8\right]+1\right)+2$,
则 $\displaystyle x\sin\frac{x\pi}4\in\left\{n\sin\frac{n\pi}4\mid n\in\N^*\right\}$ 且 $\displaystyle x\sin\frac{x\pi}4=x>M$.
故 $M$ 不为 $\displaystyle\left\{n\sin\frac{n\pi}4\mid n\in\N^*\right\}$ 的上界. 因此, $\displaystyle\left\{n\sin\frac{n\pi}4\mid n\in\N^*\right\}$ 无上界, 故无上确界.

下确界:
对于任意给定 $m<0$, 取 $x=8\left(\left[-m/8\right]+1\right)+6$,
则 $\displaystyle x\sin\frac{x\pi}4\in\left\{n\sin\frac{n\pi}4\mid n\in\N^*\right\}$ 且 $\displaystyle x\sin\frac{x\pi}4=-x<m$.
故 $m$ 不为 $\displaystyle\left\{n\sin\frac{n\pi}4\mid n\in\N^*\right\}$ 的下界. 因此, $\displaystyle\left\{n\sin\frac{n\pi}4\mid n\in\N^*\right\}$ 无下界, 故无下确界.

#### (5) $\displaystyle\left\{x^2\mid x\in\left(-1,\frac12\right)\right\}$.

上确界:
$\displaystyle\forall\,y\in\left\{x^2\mid x\in\left(-1,\frac12\right)\right\}:y\in\left[0,1\right]$, 故 $1$ 为 $\displaystyle\left\{x^2\mid x\in\left(-1,\frac12\right)\right\}$ 的一个上界.
对任意给定 $\varepsilon>0$, 取 $x=-\sqrt{\max\left\{1-\varepsilon/2,0\right\}}$, 则 $\displaystyle x^2\in\left\{x^2\mid x\in\left(-1,\frac12\right)\right\}$ 且 $x^2>1-\varepsilon$.
由上确界的充要条件, $\displaystyle\sup\left\{x^2\mid x\in\left(-1,\frac12\right)\right\}=1$.

下确界:
$\displaystyle\forall\,y\in\left\{x^2\mid x\in\left(-1,\frac12\right)\right\}:y\in\left[0,1\right]$, 故 $0$ 为 $\displaystyle\left\{x^2\mid x\in\left(-1,\frac12\right)\right\}$ 的一个下界.
对任意给定 $\varepsilon>0$, 取 $x=0$, 则 $\displaystyle x^2\in\left\{x^2\mid x\in\left(-1,\frac12\right)\right\}$ 且 $x^2<0+\varepsilon$.
由下确界的充要条件, $\displaystyle\inf\left\{x^2\mid x\in\left(-1,\frac12\right)\right\}=0$.

### 14. 设数集 $A$ 和 $B$ 的上下确界都存在且 $A\subset B$. 求证 $\sup A\leq\sup B$, $\inf A\geq\inf B$.

由上确界定义, $\forall\,x\in B:x\leq\sup B$. 则对于任意给定 $x\in A$, 由 $A\subset B$, 有 $x\in B$, 故 $x\leq\sup B$.

因此, $\sup B$ 为 $A$ 的一个上界. 由于 $\sup A$ 为 $A$ 的最小上界, 有 $\sup A\leq\sup B$.

同理可证 $\inf A\geq\inf B$.

### 15. 设 $X$ 为非空有界数集, 求证 $\inf\left(-X\right)=-\sup X$, $\sup\left(-X\right)=-\inf X$, 其中 $-X$ 表示数集 $\left\{-x\mid x\in X\right\}$.

由上确界定义, $\forall\,x\in X:x\leq\sup X$, 则 $\forall\,x\in X:-x\geq-\sup X$, 故 $-\sup X$ 为 $-X$ 的一个下界.

对任意给定 $\varepsilon>0$, 取 $\varepsilon_X=\varepsilon$, 由上确界定义, $\exist\,x\in X:x>\sup X-\varepsilon_X$, 则 $-x<-\sup X+\varepsilon$.

故 $\inf\left(-X\right)=-\sup X$. 同理可证 $\sup\left(-X\right)=-\inf X$.

### 16. 设 $X$ 和 $Y$ 是两个非空有界非负数集, 求证 $\inf\left(X\cdot Y\right)=\inf X\cdot\inf Y$, $\sup\left(X\cdot Y\right)=\sup X\cdot\sup Y$, 这里 $X\cdot Y:=\left\{xy\mid x\in X,y\in Y\right\}$.

由上确界定义, $\forall\,x\in X:0\leq x\leq\sup X$, $\forall\,y\in Y:0\leq y\leq\sup Y$,
则 $\forall\,x\in X,y\in Y:0\leq xy\leq\sup X\cdot\sup Y$, 故 $\sup X\cdot\sup Y$ 为 $X\cdot Y$ 的一个上界.

对任意给定 $\varepsilon>0$:

1. 当 $\sup X\cdot\sup Y=0$, 不失一般性, 假设 $\sup X=0$, 则 $X=\left\{0\right\}$.

   故 $X\cdot Y=\left\{0\right\}$, $\sup\left(X\cdot Y\right)=\sup X\cdot\sup Y=0$.

1. 当 $\varepsilon>\sup X\cdot\sup Y>0$:

   任取 $x\in X$, $y\in Y$, 有 $xy\in X\cdot Y$, 且 $xy\geq0>\sup X\cdot\sup Y-\varepsilon$.

1. 当 $0<\varepsilon\leq\sup X\cdot\sup Y$:

   取 $\displaystyle\varepsilon_X=\frac\varepsilon{2\sup Y}$, $\displaystyle\varepsilon_Y=\frac\varepsilon{2\sup X}$, 由上确界定义,
   $\exist\,x\in X:x>\sup X-\varepsilon_X$, $\exist\,y\in Y:y>\sup Y-\varepsilon_Y$. 此外, $\varepsilon_X<\sup X$, $\varepsilon_Y<\sup Y$.
   有:
   $$
   \begin{aligned}xy&>\left(\sup X-\varepsilon_X\right)\left(\sup Y-\varepsilon_Y\right)\\&>\sup X\cdot\sup Y-\varepsilon_X\sup Y-\varepsilon_Y\sup X\\&=\sup X\cdot\sup Y-\varepsilon\end{aligned}
   $$
   故 $\sup\left(X\cdot Y\right)=\sup X\cdot\sup Y$.

由 $\forall\,x\in X:x\geq0$, 有 $0$ 为 $X$ 的一个下界. 同理, $0$ 为 $Y$ 的一个下界.
因此, 由下确界定义, $\forall\,x\in X:0\leq\inf X\leq x$, $\forall\,y\in Y:0\leq\inf Y\leq y$.
故 $\forall\,x\in X,y\in Y:0\leq\inf X\cdot\inf Y\leq xy$. 故 $\inf X\cdot\inf Y$ 为 $X\cdot Y$ 的一个下界.

对任意给定 $\varepsilon>0$, 取 $\displaystyle\varepsilon_X=\varepsilon_Y=\min\left\{1,\frac\varepsilon{\inf X+\inf Y+1}\right\}$, 由下确界定义,
$\exist\,x\in X:x<\inf X+\varepsilon_X$, $\exist\,y\in Y:y<\inf Y+\varepsilon_Y$. 有:
$$
\begin{aligned}xy&<\left(\inf X+\varepsilon_X\right)\left(\inf Y+\varepsilon_Y\right)\\&=\inf X\cdot\inf Y+\varepsilon_X\inf Y+\varepsilon_Y\inf X+\varepsilon_X\varepsilon_Y\\&=\inf X\cdot\inf Y+\varepsilon_X\left(\inf X+\inf Y+\varepsilon_X\right)\\&\leq\inf X\cdot\inf Y+\varepsilon_X\left(\inf X+\inf Y+1\right)\\&=\inf X\cdot\inf Y+\varepsilon\end{aligned}
$$
故 $\inf\left(X\cdot Y\right)=\inf X\cdot\inf Y$.

### 17. 设 $X$ 为非空有界数集, 且 $a>0$, 求证 $\sup\left(aX\right)=a\sup X$, $\inf\left(aX\right)=a\inf X$, 这里 $aX:=\left\{ax\mid x\in X\right\}$.

由上确界定义, $\forall\,x\in X:x\leq\sup X$, 则 $\forall\,x\in X:ax\leq a\sup X$, 故 $a\sup X$ 为 $aX$ 的一个上界.

对任意给定 $\varepsilon>0$, 取 $\varepsilon_X=\varepsilon/a$, 由上确界定义, $\exist\,x\in X:x>\sup X-\varepsilon_X$, 则 $ax>a\sup X-\varepsilon$.

故 $\sup\left(aX\right)=a\sup X$. 同理可证 $\inf\left(aX\right)=a\inf X$.

## 第四节

### 1. 求下列数列的上下数列和上下极限:

#### (2) $\displaystyle x_n=1+\frac n{n+1}\cos\frac{n\pi}2$.

$\displaystyle\forall\,k\in\N^*:x_{4k-3}=1,x_{4k-2}=\frac1{4k-1}\in\left(0,1\right),x_{4k-1}=1,x_{4k}=2-\frac1{4k+1}\in\left(1,2\right)$.

上数列与上极限:
对于任意 $n\in\N^*$, 有 $\forall\,p\in\N:x_{n+p}<2$.
且对于任意给定 $\varepsilon>0$, 取 $\displaystyle p=\max\left\{4\left[\frac1{4\varepsilon}\right]+4-n,3n\right\}$, 则 $\displaystyle x_{n+p}=2-\frac1{n+p+1}>2-\varepsilon$.
由上确界的充要条件, 有 $\displaystyle\sup_{p\in\N}x_{n+p}=2$, 故 $\forall\,n\in\N^*:\overline x_n=2$, $\displaystyle\varlimsup_{n\to\infty}x_n=\lim_{n\to\infty}\overline x_n=2$.

下数列与下极限:
对于任意 $n\in\N^*$, 有 $\forall\,p\in\N:x_{n+p}>0$.
且对于任意给定 $\varepsilon>0$, 取 $\displaystyle p=\max\left\{4\left[\frac1{4\varepsilon}\right]+6-n,3n+2\right\}$, 则 $\displaystyle x_{n+p}=\frac1{n+p-1}<\varepsilon$.
由上确界的充要条件, 有 $\displaystyle\inf_{p\in\N}x_{n+p}=0$, 故 $\forall\,n\in\N^*:\underline x_n=0$, $\displaystyle\varliminf_{n\to\infty}x_n=\lim_{n\to\infty}\underline x_n=0$.

#### (4) $x_n=-n\left[2+\left(-1\right)^n\right]$.

$\forall\,k\in\N^*:x_{2k-1}=-2k+1,x_{2k}=-6k<-2k-1=x_{2k+1}$.

上数列与上极限:
对于任意 $n\in\N^*$, 有 $\forall\,p\in\N:x_{n+p}\leq-2\left[n/2\right]-1$.
且对于任意给定 $\varepsilon>0$, 取 $p=2\left[n/2\right]+1-n$, 则 $x_{n+p}-\left(-2\left[n/2\right]-1\right)=0<\varepsilon$.
由上确界的充要条件, 有 $\displaystyle\sup_{p\in\N}x_{n+p}=-2\left[n/2\right]-1$, 故 $\forall\,m\in\N^*:\overline x_n=-2\left[n/2\right]-1$, 上极限不存在.

下数列与下极限:
对于任意 $n\in\N^*$, $m<0$, 取 $p=\max\left\{2\left[-m/2\right]+2-n,n\right\}$, 则 $x_{n+p}\leq-6\left[-m/2\right]-6<m$.
故 $\left\{x_{n+p}\right\}$ 无下界, $\left\{x_n\right\}$ 的下数列与下极限均不存在.

### 3. 设 $\left\{x_n\right\}$ 和 $\left\{y_n\right\}$ 都是有界非负数列, 求证下式.
$$
\begin{aligned}&\varliminf_{n\to\infty}x_n\cdot\varliminf_{n\to\infty}y_n\leq\varliminf_{n\to\infty}x_ny_n\\ \leq{}&\varliminf_{n\to\infty}x_n\cdot\varlimsup_{n\to\infty}y_n\\ \leq{}&\varlimsup_{n\to\infty}x_ny_n\leq\varlimsup_{n\to\infty}x_n\cdot\varlimsup_{n\to\infty}y_n\end{aligned}
$$
注意到:
$$
\begin{aligned}&\underline x_n\underline y_n\\={}&\inf_{p\in\N}\left(x_{n+p}\underline y_n\right)\leq\inf_{p\in\N}\left(x_{n+p}y_{n+p}\right)\\ \leq{}&\inf_{p\in\N}\left(x_{n+p}\overline y_n\right)=\underline x_n\overline y_n\\={}&\sup_{p\in\N}\left(\underline x_ny_{n+p}\right)\leq\sup_{p\in\N}\left(x_{n+p}y_{n+p}\right)\\ \leq{}&\sup_{p\in\N}\left(\overline x_ny_{n+p}\right)=\overline x_n\overline y_n\end{aligned}
$$
由极限的保序性, 有:
$$
\begin{aligned}&\lim_{n\to\infty}\underline x_n\underline y_n\leq\lim_{n\to\infty}\inf_{p\in\N}\left(x_{n+p}y_{n+p}\right)\\ \leq{}&\lim_{n\to\infty}\underline x_n\overline y_n\\ \leq{}&\lim_{n\to\infty}\sup_{p\in\N}\left(x_{n+p}y_{n+p}\right)\leq\lim_{n\to\infty}\overline x_n\overline y_n\end{aligned}
$$
即:
$$
\begin{aligned}&\varliminf_{n\to\infty}x_n\cdot\varliminf_{n\to\infty}y_n\leq\varliminf_{n\to\infty}x_ny_n\\ \leq{}&\varliminf_{n\to\infty}x_n\cdot\varlimsup_{n\to\infty}y_n\\ \leq{}&\varlimsup_{n\to\infty}x_ny_n\leq\varlimsup_{n\to\infty}x_n\cdot\varlimsup_{n\to\infty}y_n\end{aligned}
$$
### 6. 设 $\displaystyle\lim_{n\to\infty}x_n=A$, 求证 $\displaystyle\lim_{n\to\infty}\frac{\displaystyle\sum_{i=1}^n\frac i{i+1}x_i}n=A$.

设数列 $\left\{a_n\right\}$ 满足 $\displaystyle\forall\,n\in\N^*:a_n=\sum_{i=1}^n\frac i{i+1}x_i$, $\left\{b_n\right\}$ 满足 $\displaystyle\forall\,n\in\N^*:b_n=n$.

则 $\left\{b_n\right\}$ 单调递增, 且 $\displaystyle\lim_{n\to\infty}b_n=+\infty$.
$$
\lim_{n\to\infty}\frac{a_{n+1}-a_n}{b_{n+1}-b_n}=\lim_{n\to\infty}\frac{n+1}{n+2}x_{n+1}=1\cdot A=A
$$
由 Stolz–Cesàro Theorem, $\displaystyle\lim_{n\to\infty}\frac{\displaystyle\sum_{i=1}^n\frac i{i+1}x_i}n=\lim_{n\to\infty}\frac{a_n}{b_n}=\lim_{n\to\infty}\frac{a_{n+1}-a_n}{b_{n+1}-b_n}=A$.

### 8. 设 $p\in\N^*$, 求证 $\displaystyle\lim_{n\to\infty}\frac{\displaystyle\sum_{i=1}^ni^p}{n^{p+1}}=\frac1{p+1}$.

设数列 $\left\{a_n\right\}$ 满足 $\displaystyle\forall\,n\in\N^*:a_n=\sum_{i=1}^ni^p$, $\left\{b_n\right\}$ 满足 $\displaystyle\forall\,n\in\N^*:b_n=n^{p+1}$.

则 $\left\{b_n\right\}$ 单调递增, 且 $\displaystyle\lim_{n\to\infty}b_n=+\infty$.
$$
\lim_{n\to\infty}\frac{a_{n+1}-a_n}{b_{n+1}-b_n}=\lim_{n\to\infty}\frac{(n+1)^p}{(n+1)^{p+1}-n^{p+1}}=\lim_{n\to\infty}\frac{(n+1)^p}{\displaystyle\sum_{i=0}^{p}C_{p+1}^in^i}=\frac1{p+1}
$$
由 Stolz–Cesàro Theorem, $\displaystyle\lim_{n\to\infty}\frac{\displaystyle\sum_{i=1}^ni^p}{n^{p+1}}=\lim_{n\to\infty}\frac{a_n}{b_n}=\lim_{n\to\infty}\frac{a_{n+1}-a_n}{b_{n+1}-b_n}=\frac1{p+1}$.

## 第五节

### 1. 利用 Cauchy's Criterion 判定下列数列的敛散性.

#### (2) $\displaystyle x_n=\sum_{i=1}^n\frac1{i^2}$.

对于任意给定 $\varepsilon>0$, 取 $\displaystyle N=\left[\frac1\varepsilon\right]+1$, 当 $m\geq n>N$, 有:
$$
\left|x_m-x_n\right|=\sum_{i=n+1}^m\frac1{i^2}<\sum_{i=n+1}^m\frac1{i(i-1)}=\sum_{i=n+1}^m\left(\frac1{i-1}-\frac1{i}\right)=\frac1n-\frac1m<\frac1n<\varepsilon
$$
故 $\displaystyle\lim_{n\to\infty}\omega(x_n)=0$. 由 Cauchy's Criterion, 有 $\left\{x_n\right\}$ 收敛.

#### (3) $\displaystyle x_n=a_0+\sum_{i=1}^na_iq^i$, $\left|q\right|<1$, $\left|a_k\right|\leq M$.

当 $q=0$, $x_n=a_0$, $\left\{x_n\right\}$ 收敛.

当 $0<\left|q\right|<1$, 对于任意给定 $\varepsilon>0$, 取 $\displaystyle N=\max\left\{\left[\log_{\left|q\right|}\left(\frac{1-\left|q\right|}M\varepsilon\right)\right],1\right\}$, 当 $m\geq n>N$, 有:
$$
\left|x_m-x_n\right|=\left|\sum_{i=n+1}^ma_iq^i\right|\leq\sum_{i=n+1}^m\left|a_i\right|\left|q\right|^i\leq M\sum_{i=n+1}^m\left|q\right|^i=M\frac{\left|q\right|^{n+1}-\left|q\right|^{m+1}}{1-\left|q\right|}<\frac{M\left|q\right|}{1-\left|q\right|}\left|q\right|^n<\varepsilon
$$
故 $\displaystyle\lim_{n\to\infty}\omega(x_n)=0$. 由 Cauchy's Criterion, 有 $\left\{x_n\right\}$ 收敛.

#### (5) $x_n=\begin{cases}\displaystyle1+\frac1n,&2\mid n\\ \displaystyle\frac1{n^2},&2\nmid n\end{cases}$.

取 $\varepsilon=1$, 对于任意给定 $N\in\N^*$, 取 $n=2N$, $m=2N+1$, 有:
$$
\left|x_m-x_n\right|=\left|\frac1{\left(2N+1\right)^2}-1-\frac1{2N}\right|=1+\frac1{2N}-\frac1{\left(2N+1\right)^2}>1=\varepsilon
$$
故 $\left\{x_n\right\}$ 不为 Cauchy sequence, 故 $\left\{x_n\right\}$ 发散.

### 4. 设数列 $\left\{x_n\right\}$ 满足压缩性条件 $\left|x_{n+1}-x_n\right|\leq K\left|x_n-x_{n-1}\right|$, $0<K<1$, $n=2,3,\cdots$, 其中 $K$ 为常数, 则 $\left\{x_n\right\}$ 收敛.

设 $a=\left|x_2-x_1\right|$, 则由 MI 易得 $\forall\,n\in\N^*:\left|x_{n+1}-x_n\right|\leq K^{n-1}a$.

当 $a=0$, $0\leq\left|x_{n+1}-x_n\right|\leq0$, $\left\{x_n\right\}$ 为常数列, 收敛.

当 $a>0$, 对于任意给定 $\varepsilon>0$, 取 $\displaystyle N=\max\left\{\left[\log_K\left(\frac{1-K}a\varepsilon\right)\right]+2,1\right\}$, 当 $m\geq n>N$, 有:
$$
\begin{aligned}\left|x_m-x_n\right|&=\left|\sum_{i=n}^{m-1}x_{i+1}-x_i\right|\leq\sum_{i=n}^{m-1}\left|x_{i+1}-x_i\right|\leq\sum_{i=n}^{m-1}K^{i-1}a\\&=\frac{K^{n-1}-K^{m-1}}{1-K}a<\frac a{K\left(1-K\right)}K^n<\varepsilon\end{aligned}
$$
故 $\displaystyle\lim_{n\to\infty}\omega(x_n)=0$. 由 Cauchy's Criterion, 有 $\left\{x_n\right\}$ 收敛.