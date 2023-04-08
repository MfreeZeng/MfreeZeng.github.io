# 常见不定积分

$$\begin{align*}
    &\int a^x \,\mathrm{d}x=\frac{a^x}{\ln a}+C\\
    &\int \frac{1}{x^k}\,\mathrm{d}x=-\frac1{k-1}\frac1{x^{k-1}} +C\\
    &\int \frac{\mathrm{d}x}{1+x^2}=\arctan x +C\\
    &\int \frac{\mathrm{d}x}{\sqrt{1-x^2}}=\arcsin x +C\\
    &\int \frac{\mathrm{d}x}{\cos ^2 x}=-\cot x +C\\
    &\int \frac{\mathrm{d}x}{\sin ^2 x}=\tan x +C\\
\end{align*}$$
# 常见三角变换

三角函数有理化变换

$$\sin x=\frac{2t}{1+t^2};\cos x=\frac{1-t^2}{1+t^2};x=2\arctan x;\mathrm{d}x=\frac{2\mathrm{d}t}{1+t^2}$$

三角函数升降幂变换

$$sin^2 x=\frac{1-\cos 2x}{2};\cos^2 x=\frac{1+\cos 2x}{2}$$

# 有理式的积分

$$\int \frac{a_nx^n+a_{n-1}x^{n-1}\dots+a_1x+a_0}{b_mx^m+b_{m-1}x^{m-1}\dots+b_1x+b_0}\,\mathrm{d}x=\int \frac{P_n(x)}{Q_m(x)}\,\mathrm{d}x$$

对于 $n\geq m$ 的情况，我们总能分离出分母次数大于分子次数的的有理分式

我们首先关注以下特殊的分式：

$$\frac{Ax+B}{x^2+px+q};\frac{Ax+B}{(x^2+px+q)^m}$$

我们可以将分母整理成

$$x^2+px+q=(x+\alpha)^2+\beta^2$$

做替换：
$$x+\alpha =t,\quad Ax+B=At+\lambda$$

变换后

$$\begin{align*}
    \int \frac{Ax+B}{x^2+px+q}\,\mathrm{d}x
    &=\int \frac{At+\lambda}{t^2+\beta^2}\,\mathrm{d}t\\
    &=\frac{A}2 \int \frac{\mathrm{d}(t^2+\beta^2)}{t^2+\beta^2}+\frac{\lambda}{\beta}\int \frac{\mathrm{d}(\frac{t}{\beta})}{(\frac{t}{\beta})^2+1}\\
    &=\frac{A}2 \ln(x^2+px+q) + \frac{\lambda}{\beta} \arctan \frac{x+\alpha}{\beta}+C
\end{align*}$$

对于 $m\geq 2$ 的情况:

$$\begin{align*}
    \int \frac{Ax+B}{(x^2+px+q)^m}\,\mathrm{d}x
    &=\int \frac{At+\lambda}{(t^2+\beta^2)^m}\,\mathrm{d}t\\
    &=\frac{A}2 \int \frac{\mathrm{d}(t^2+\beta^2)}{(t^2+\beta^2)^m} + \lambda\int \frac{\mathrm{d}t}{(t^2+\beta^2)^m}\\
    &=\frac{A}{2(1-m)} \frac1{(x^2+px+q)^{m-1}} + \lambda J_m
\end{align*}$$

其中 $J_m$ 参考 P22 (7)
当 $m= 2$ 时:
$$\int \frac{Ax+B}{(x^2+px+q)^2}\,\mathrm{d}x =\left( \frac{\lambda x}{2\beta^2}-\frac{A}{2} \right)\frac{1}{(x^2+px+q)}+\frac1{2\beta^3}\arctan \frac{x+\alpha}{\beta} +C$$

其中

$$\alpha=\frac{p}2,\, \beta=q-\frac{p^2}4,\, \lambda=B-\frac{Ap}2$$

