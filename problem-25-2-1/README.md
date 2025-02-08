$$I=\int_0^1{\lfloor log_px \rfloor}\mathrm{d}x\  (p\in\R)$$

$(1)$ 常规方法

$$
\begin{aligned}
I &= \sum_{n=1}^{+\infty}\int_{p^{-n}}^{p^{-n+1}}{\lfloor log_px \rfloor}\mathrm{d}x \\
&= -\sum_{n=1}^{+\infty}\int_{p^{-n}}^{p^{-n+1}}{n}\mathrm{d}x \\
&= -\sum_{n=1}^{+\infty}\left[nx\right]_{p^{-n}}^{p^{-n+1}} \\
&= -(\sum_{n=1}^{+\infty}\frac{n}{p^{n-1}}-\sum_{n=1}^{+\infty}\frac{n}{p^n}) \\
&= -(\sum_{n=1}^{+\infty}\frac{n+1}{p^n}+1-\sum_{n=1}^{+\infty}\frac{n}{p^n}) \\
&= -\sum_{n=1}^{+\infty}\frac{1}{p^n}-1 \\
&= -\frac{1}{p-1}-1 \\
&= -\frac{p}{p-1}
\end{aligned}
$$

$(2)$ 特殊方法

用 $p$-进制 表示 $x$, 并结合 $x\in(0,1)$ 得
$$x=\sum_{n=1}^{+\infty}\frac{a_n}{p^n}$$
设 $a_1=a_2=...=a_{k-1}=0$, $a_{k}\not=0$, 则
$$log_px=log_p({\frac{a_k}{p^k}}+\sum_{n=k+1}^{+\infty}\frac{a_n}{p^n})=-k+log_p(a_k+\sum_{n=1}^{+\infty}\frac{a_{n+k}}{p^n})$$
$$\lfloor log_px \rfloor=-k$$
这里 $k$ 是 $a_n$ 里第一个不是 $0$ 的项的位数
显然 $I$ 求的是 $-E(k)$
显然
$$P(k=n)=\frac{1}{p^{n-1}}\frac{p-1}{p}=\frac{p-1}{p^n}$$
故
$$I=-E(k)=\sum_{n=1}^{+\infty}nP(k=n)=-\frac{p}{p-1}$$