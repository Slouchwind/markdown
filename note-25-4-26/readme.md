假设有一单摆, 摆长 $l$, 绳质量忽略不计, 摆质量 $m$, 以竖直向下的轴为 $0$ 度角, 记绳与竖线的夹角为 $\theta$, 右侧为正, 将单摆拉至 $\theta_0$ 处释放, 不计阻力.

受力分析得 $m\ddot{\theta}l+mg\sin\theta=0$

即解微分方程

$$\ddot{\theta}+\frac{g}{l}\sin\theta=0$$

由 $\dfrac{\mathrm{d}^2\theta}{\mathrm{d}t^2}=\dfrac{\mathrm{d}\omega}{\mathrm{d}t}=\dfrac{\mathrm{d}\omega}{\mathrm{d}\theta}\dfrac{\mathrm{d}\theta}{\mathrm{d}t}=\omega\dfrac{\mathrm{d}\omega}{\mathrm{d}\theta}$ 得

$$
\begin{aligned}
\omega\dfrac{\mathrm{d}\omega}{\mathrm{d}\theta}+\frac{g}{l}\sin\theta&=0\\
\omega\mathrm{d}\omega&=-\frac{g}{l}\sin\theta\mathrm{d}\theta\\
\int\omega\mathrm{d}\omega&=-\int\frac{g}{l}\sin\theta\mathrm{d}\theta\\
\frac{\omega^2}{2}&=\frac{g}{l}\cos\theta+C
\end{aligned}
$$

由初始条件 $\left.\omega\right|_{t=0}=0$ 可得 $0=\cfrac{g}{l}\cos\theta_0+C$, 即 $C=-\cfrac{g}{l}\cos\theta_0$

于是有

$$
\begin{aligned}
\omega^2&=\frac{2g}{l}(\cos\theta-\cos\theta_0)\\
\dfrac{\mathrm{d}\theta}{\mathrm{d}t}&=\sqrt{\frac{2g}{l}(\cos\theta-\cos\theta_0)}\\
\mathrm{d}t&=\frac{\mathrm{d}\theta}{\sqrt{\frac{2g}{l}(\cos\theta-\cos\theta_0)}}\\
T&=2\int_{-\theta_0}^{\theta_0}\frac{\mathrm{d}\theta}{\sqrt{\frac{2g}{l}(\cos\theta-\cos\theta_0)}}\\
&=\sqrt{\frac{2l}{g}}\int_{-\theta_0}^{\theta_0}\frac{\mathrm{d}\theta}{\sqrt{\cos\theta-\cos\theta_0}}\\
&=2\sqrt{\frac{l}{g}}\int_0^{\theta_0}\frac{\mathrm{d}\theta}{\sqrt{\sin^2\cfrac{\theta_0}{2}-\sin^2\cfrac{\theta}{2}}}\\
&=4\sqrt{\frac{l}{g}}\int_0^{\frac{\theta_0}{2}}\frac{\mathrm{d}\theta}{\sqrt{\sin^2\cfrac{\theta_0}{2}-\sin^2\theta}}\\
&=4\sqrt{\frac{l}{g}}\csc\cfrac{\theta_0}{2}\int_0^{\frac{\theta_0}{2}}\frac{\mathrm{d}\theta}{\sqrt{1-\csc^2\cfrac{\theta_0}{2}\sin^2\theta}}\\
&=4\sqrt{\frac{l}{g}}\csc\cfrac{\theta_0}{2}F\left(\frac{\theta_0}{2},\csc\frac{\theta_0}{2}\right)
\end{aligned}
$$

其中 $F$ 是第一类椭圆积分, 记作

$$
\begin{aligned}
F(\phi,k)=\int_0^\phi \frac{\mathrm{d}t}{\sqrt{1-k^2\sin^2t}}
\end{aligned}
$$

求小角度单摆的周期, 利用 $\sin\theta=\theta+o(\theta)\ (\theta\to0)$

$$
\begin{aligned}
\frac{T}{2\sqrt{\cfrac{l}{g}}}&=\lim_{\theta_0\to0}\int_0^{\theta_0}\frac{\mathrm{d}\theta}{\sqrt{\sin^2\cfrac{\theta_0}{2}-\sin^2\cfrac{\theta}{2}}}\\
&=\lim_{\theta_0\to0}\int_0^{\theta_0}\frac{\mathrm{d}\theta}{\sqrt{\cfrac{1}{4}\left(\theta_0^2-\theta^2\right)}}\\
&=2\lim_{\theta_0\to0}\frac{1}{\theta_0}\int_0^{\theta_0}\frac{\mathrm{d}\theta}{\sqrt{1-\left(\dfrac{\theta}{\theta_0}\right)^2}}\\
&=2\lim_{\theta_0\to0}\int_0^1\frac{\mathrm{d}\theta}{\sqrt{1-\theta^2}}\\
&=2\left.\arcsin\theta\right|_0^1\\
&=\pi\\
T&=2\pi\sqrt\frac{l}{g}
\end{aligned}
$$