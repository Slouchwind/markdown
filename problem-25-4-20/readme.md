记 $(n\in\mathbb{N})\ p_n(t)=
\begin{cases}
0&t\in(-\infin,-1)\cup(1,+\infin)\\
(1+t)^n&t\in[-1,0]\\
(1-t)^n&t\in(0,1]
\end{cases}$, 求

$$
\mathcal{F}\{p_n(t)\}(\omega)=
\int_{-\infin}^{+\infin}e^{-2\pi\mathrm{i}\omega t}p_n(t)\mathrm{d}t
$$

$$
\mathcal{F}\{p_n(t)\}(\omega)=
\int_{-1}^0e^{-2\pi\mathrm{i}\omega t}(1+t)^n\mathrm{d}t+
\int_0^1e^{-2\pi\mathrm{i}\omega t}(1-t)^n\mathrm{d}t\\
=I_n+J_n
$$

显然

$$
\dfrac{\mathrm{d}e^{-2\pi\mathrm{i}\omega t}}{\mathrm{d}t}=
-2\pi\mathrm{i}\omega e^{-2\pi\mathrm{i}\omega t}
$$

故

$$
\begin{aligned}
I_n&=-\frac{1}{2\pi\mathrm{i}\omega}\int_{-1}^0(1+t)^n\mathrm{d}e^{-2\pi\mathrm{i}\omega t}\\
&=-\frac{1}{2\pi\mathrm{i}\omega}\left[(1-0)-\int_{-1}^0e^{-2\pi\mathrm{i}\omega t}\mathrm{d}(1+t)^n\right]\\
&=\frac{nI_{n-1}-1}{2\pi\mathrm{i}\omega}
\end{aligned}
$$

$$
\begin{aligned}
J_n&=-\frac{1}{2\pi\mathrm{i}\omega}\int_0^1(1-t)^n\mathrm{d}e^{-2\pi\mathrm{i}\omega t}\\
&=-\frac{1}{2\pi\mathrm{i}\omega}\left[(0-1)-\int_0^1e^{-2\pi\mathrm{i}\omega t}\mathrm{d}(1-t)^n\right]\\
&=\frac{1-nJ_{n-1}}{2\pi\mathrm{i}\omega}
\end{aligned}
$$

$$I_n+J_n=\frac{n(I_{n-1}-J_{n-1})}{2\pi\mathrm{i}\omega}$$

$$I_n-J_n=\frac{n(I_{n-1}+J_{n-1})-2}{2\pi\mathrm{i}\omega}$$

下式代入上式

$$
\begin{aligned}
I_n+J_n
=\frac{n}{2\pi\mathrm{i}\omega}\frac{(n-1)(I_{n-2}+J_{n-2})-2}{2\pi\mathrm{i}\omega}\\
=\frac{n}{2\pi^2\omega^2}-\frac{n(n-1)}{4\pi^2\omega^2}(I_{n-2}+J_{n-2})
\end{aligned}
$$

$$f(n)=\frac{n}{2\pi^2\omega^2},\ g(n)=-\frac{n(n-1)}{4\pi^2\omega^2},\ a_n=I_n+J_n$$

$$
\begin{aligned}
a_n&=f(n)+g(n)a_{n-2}\\
&=f(n)+g(n)f(n-2)+g(n)g(n-2)a_{n-4}\\
&=f(n)+g(n)f(n-2)+g(n)g(n-2)f(n-4)+g(n)g(n-2)g(n-4)a_{n-6}\\
&=\dots\\
&=\begin{cases}
n\in\mathrm{odd}, f(n)+g(n)f(n-2)+\dots+g(n)g(n-2)g(n-4)\dots g(3)a_1\\
n\in\mathrm{even}, f(n)+g(n)f(n-2)+\dots+g(n)g(n-2)g(n-4)\dots g(2)a_0
\end{cases}
\end{aligned}
$$

记上述展开式第 $r+1$ 项为 $T_{r+1}\ (r\in\mathbb{N})$

$$
n\in\mathrm{odd},\ T_{r+1}=
\begin{cases}
f(n) &r=0\\
\displaystyle f(n-2r)\prod_{k=0}^{r-1}g(n-2k) &1\le r\le\cfrac{n-3}2\\
\displaystyle a_1\prod_{k=0}^{r-1}g(n-2k) &r=\cfrac{n-1}2
\end{cases}
$$

$$
n\in\mathrm{even},\ T_{r+1}=
\begin{cases}
f(n) &r=0\\
\displaystyle f(n-2r)\prod_{k=0}^{r-1}g(n-2k) &1\le r\le\cfrac{n}2-1\\
\displaystyle a_0\prod_{k=0}^{r-1}g(n-2k) &r=\cfrac{n}2
\end{cases}
$$

$$
\begin{aligned}
\prod_{k=0}^{r-1}g(n-2k)&=\frac{(-1)^rn(n-1)(n-2)\dots (n-2r+1)}{(4\pi^2\omega^2)^r}\\
&=\frac{(-1)^rn!}{(4\pi^2\omega^2)^r(n-2r)!}
\end{aligned}
$$

代回 $a_n$

$$
\begin{aligned}
n\in\mathrm{odd},\ a_n&=\sum_{r=0}^{\frac{n-1}{2}}T_{r+1}\\
&=\frac{n}{2\pi^2\omega^2}+\sum_{r=1}^{\frac{n-3}{2}}\frac{n-2r}{2\pi^2\omega^2}\frac{(-1)^rn!}{(4\pi^2\omega^2)^r(n-2r)!}+\left(-\frac{1}{4\pi^2\omega^2}\right)^\frac{n-1}{2}n!a_1\\
&=\sum_{r=0}^{\frac{n-3}{2}}\frac{(-1)^rn!}{2^{2r+1}(\pi\omega)^{2r+2}(n-2r-1)!}+\left(-\frac{1}{4\pi^2\omega^2}\right)^\frac{n-1}{2}n!a_1
\end{aligned}
$$

$$
\begin{aligned}
n\in\mathrm{even},\ a_n&=\sum_{r=0}^{\frac{n}{2}}T_{r+1}\\
&=\frac{n}{2\pi^2\omega^2}+\sum_{r=1}^{\frac{n-2}{2}}\frac{n-2r}{2\pi^2\omega^2}\frac{(-1)^rn!}{(4\pi^2\omega^2)^r(n-2r)!}+\left(-\frac{1}{4\pi^2\omega^2}\right)^\frac{n}{2}n!a_0\\
&=\sum_{r=0}^{\frac{n}{2}-1}\frac{(-1)^rn!}{2^{2r+1}(\pi\omega)^{2r+2}(n-2r-1)!}+\left(-\frac{1}{4\pi^2\omega^2}\right)^\frac{n}{2}n!a_0
\end{aligned}
$$

$$
\begin{aligned}
a_0&=\int_{-1}^1e^{-2\pi\mathrm{i}\omega t}\mathrm{d}t\\
&=\left[\frac{e^{-2\pi\mathrm{i}\omega t}}{-2\pi\mathrm{i}\omega}\right]_{-1}^1\\
&=\frac{e^{2\pi\mathrm{i}\omega}-e^{-2\pi\mathrm{i}\omega}}{2\pi\mathrm{i}\omega}\\
&=\frac{\sin2\pi\omega}{\pi\omega}
\end{aligned}
$$

$$
\begin{aligned}
a_1&=I_1+J_1\\
&=\frac{I_0-J_0}{2\pi\mathrm{i}\omega}\\
&=\frac{\left[\frac{e^{-2\pi\mathrm{i}\omega t}}{-2\pi\mathrm{i}\omega}\right]_{-1}^0-\left[\frac{e^{-2\pi\mathrm{i}\omega t}}{-2\pi\mathrm{i}\omega}\right]_0^1}{2\pi\mathrm{i}\omega}\\
&=\frac{\frac{1}{-2\pi\mathrm{i}\omega}+\frac{e^{2\pi\mathrm{i}\omega}}{2\pi\mathrm{i}\omega}+\frac{e^{-2\pi\mathrm{i}\omega}}{2\pi\mathrm{i}\omega}+\frac{1}{-2\pi\mathrm{i}\omega}}{2\pi\mathrm{i}\omega}\\
&=\frac{1-\cos2\pi\omega}{2\pi^2\omega^2}\\
&=\frac{\sin^2\pi\omega}{2\pi^2\omega^2}
\end{aligned}
$$

综上

$$
n\in\mathrm{odd},\mathcal{F}\{p_n(t)\}(\omega)=\sum_{r=0}^{\frac{n-3}{2}}\frac{(-1)^rn!}{2^{2r+1}(\pi\omega)^{2r+2}(n-2r-1)!}+\left(-\frac{1}{4\pi^2\omega^2}\right)^\frac{n-1}{2}n!\frac{\sin^2\pi\omega}{2\pi^2\omega^2}\\
n\in\mathrm{even},\mathcal{F}\{p_n(t)\}(\omega)=\sum_{r=0}^{\frac{n}{2}-1}\frac{(-1)^rn!}{2^{2r+1}(\pi\omega)^{2r+2}(n-2r-1)!}+\left(-\frac{1}{4\pi^2\omega^2}\right)^\frac{n}{2}n!\frac{\sin2\pi\omega}{\pi\omega}
$$
