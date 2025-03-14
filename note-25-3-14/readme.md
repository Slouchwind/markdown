斐波那契数列: $a_1=a_2=1, a_{n+1}=a_n+a_{n-1} (n\ge2, n\in\N)$

设有 $k\in\R$, $a_{n+1}+ka_n=a_n+a_{n-1}+ka_n=(k+1)a_n+a_{n-1}$

使 $\{a_{n+1}+ka_n\}$ 是等比数列，即 $\displaystyle\frac{1}{k+1}=k$

得 $k^2+k-1=0$, 解得 $\displaystyle k=\frac{-1\pm\sqrt5}{2}$

也就是 $\displaystyle\left\{a_{n+1}+\frac{-1\pm\sqrt5}{2}a_n\right\}$ 这两个数列同时是等比数列

求公比: (利用了 $\displaystyle\frac{1}{k+1}=k$)

$$
\frac{a_{n+1}+ka_n}{a_n+ka_{n-1}}=\frac{(k+1)a_n+a_{n-1}}{a_n+ka_{n-1}}=\frac{(k+1)(a_n+ka_{n-1})}{a_n+ka_{n-1}}=k+1\ (n\in\N^*)
$$

于是有 $a_{n+1}+ka_n=(k+1)^n$, 我们代入两个 $k$ 解方程组

$$
\left\{
\begin{aligned}
a_{n+1}+\frac{-1+\sqrt{5}}{2}a_n=\left(\frac{1+\sqrt{5}}{2}\right)^n\\
a_{n+1}+\frac{-1-\sqrt{5}}{2}a_n=\left(\frac{1-\sqrt{5}}{2}\right)^n
\end{aligned}
\right.
$$

很明显两式相减能消元，最终就能得到：

$$
a_n=\frac{1}{\sqrt{5}}\left[\left(\frac{1+\sqrt{5}}{2}\right)^n-\left(\frac{1-\sqrt{5}}{2}\right)^n\right]\ (n\in\N^*)
$$