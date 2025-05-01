大二生之梦: $\displaystyle\int_0^1\frac{\mathrm{d}x}{x^x}=\sum_{n=1}^\infty\frac{1}{n^n}$

$$
\begin{aligned}
\int_0^1\frac{\mathrm{d}x}{x^x}&=\int_0^1e^{-x\ln x}\mathrm{d}x\\
&=\int_0^1\sum_{n=0}^\infty\frac{(-x\ln x)^n}{n!}\mathrm{d}x\\
&=\sum_{n=0}^\infty\frac{(-1)^n}{n!}\int_0^1x^n\ln^nx\mathrm{d}x\\
\end{aligned}
$$

换元 $t=\ln x$, 再换成 $-\dfrac{t}{n+1}$

$$
\begin{aligned}
\int_0^1x^n\ln^nx\mathrm{d}x&=\int_{-\infty}^0t^ne^{(n+1)t}\mathrm{d}t\\
&=\int_{+\infty}^0(-\frac{1}{n+1})^nt^ne^{-t}\mathrm{d}(-\frac{t}{n+1})\\
&=\frac{(-1)^n}{(n+1)^{n+1}}\int_0^{+\infty}t^ne^{-t}\mathrm{d}t\\
&=\frac{(-1)^nn!}{(n+1)^{n+1}}
\end{aligned}
$$

代回

$$
\begin{aligned}
\int_0^1\frac{\mathrm{d}x}{x^x}&=\sum_{n=0}^\infty\frac{(-1)^n}{n!}\frac{(-1)^nn!}{(n+1)^{n+1}}\\
&=\sum_{n=1}^\infty\frac{1}{n^n}
\end{aligned}
$$