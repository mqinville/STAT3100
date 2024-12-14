<div style="display: flex; justify-content: space-between; font-size: 0.85em; margin-bottom: 0;">
    <div style="text-align: left;">
        <strong>STAT3100</strong><br>
        <strong>Assignment 4</strong><br>
        <strong>November 17th, 2024</strong>
    </div>
    <div style="text-align: center;">
        <strong>Intro to Mathematical Statistics</strong><br>
        <strong>University of Guelph</strong><br>
        <strong>Fall 2024</strong>
    </div>
    <div style="text-align: right;">
        <strong>Félix Mainville</strong><br>
        <strong>id: 1279419</strong><br>
        <a href="mailto:fmainvil@uoguelph.ca">fmainvil@uoguelph.ca</a>
    </div>
</div>
<hr>

**Question 4**
4. Show that if a random variable has the pdf $f(x)=\frac{1}{2}e^{-|x|}$ for $-\infty<x<\infty$, its moment generating function is given by $M_{X}(t)=\frac{1}{1-t^2}$. Use this moment generating function to find the mean and variance of $X$
   
   Note that since $X$ is a continuous random variable we must integrate over the defined reagions of $X$ to find its moment generating function.$$ \begin{align}
& M_{X}(t) = E(e^{Xt}) = \int_{-\infty}^\infty e^{xt}\times\frac{1}{2}e^{-|x|} dx & \\
& M_{X}(t)=\int_{{0}}^\infty e^{xt}\times \frac{1}{2}e^{-|x|}dx \; \; + \int_{-\infty}^0 e^{xt} \times\frac{1}{2}e^{-|x|}dx & \\
			\end{align} $$ For $0\leq x < \infty, x\geq 0$, and for $-\infty<x\leq {0}, x\leq 0$ $$\begin{align}
& M_{X}(t)=\frac{1}{2}\int_{0}^\infty e^{xt}\times e^{-x}dx \; + \frac{1}{2}\int_{-\infty}^0e^{xt}\times e^{-(-x)}dx& \\
& M_{X}(t) =\frac{1}{2} \int_{0}^\infty e^{xt-x}dx + \frac{1}{2}\int_{-\infty}^0e^{xt+x}dx & \\
& M_{X}(t)=\frac{1}{2} \int_{0}^\infty e^{x(t-1)} + \frac{1}{2}\int_{-\infty}^0e^{x(t+1)}dx & \\
& M_{X}(t)= \frac{1}{2}{\left[\frac{1}{t-1}e^{x(t-1)}\right]^\infty_{0}} + \frac{1}{2}{\left[\frac{1}{t+1}e^{x(t+1)}\right]^\infty_{0}} &
\end{align}$$ For $t-1$ very small near zero: $t-1<0\implies t<1$. For $t+1$ very small near zero: $t+1>0\implies t>-1\implies-1<t<1$. $$\begin{align}
& M_{X}(t) = \frac{1}{2}\left[ 0-\left(\frac{1}{t-1}(1)\right)\right] +\frac{1}{2} \left[ \left( \frac{1}{t+1}(1) \right) -0 \right]& \\
& M_{X}(t)=\frac{1}{2}\left[ -\frac{1}{t-1}+\frac{1}{t+1} \right] =\frac{1}{2}\left[ \frac{1}{1-t}+\frac{1}{t+1} \right] & \\
&M_{X}(t) = \frac{1}{2}\left[ \frac{{t+1+1-t}}{(1-t)(t+1)}\right] =\frac{1}{2}\left[ \frac{2}{1-t^2} \right] & \\
&M_{X}(t)=\frac{1}{1-t^2}& \\
\end{align}$$ To find $E[X]$ using the moment generating function we simply need to take the first derivative of $M_{X}(t)$ and evaluate at $t=0$: $\frac{d \; M_{X}(t)}{dt} = \frac{d}{dt}\left( \frac{1}{1-t^2} \right) =\frac{2t}{(1-t^2)^2}|_{t=0}$ $$\therefore E[X]=\frac{2(0)}{1-0^2}=0$$ To find $var(X)$ we use the following identity: $\mu^`_{r}=E[X^r]=\frac{d^r}{dt^r}(M_{x}(t))$. Since $E[X]=0$, and $var(X)=E[X^2]-E^2[X]\implies var(X)=E[X^2]-0 \implies var(X)=E[X^2]$, we must simply take the derivative of $\frac{2t}{(1-t^2)^2}$ as this is already the first derivative of the moment generating function, which was used to find $E[X]$. $$\begin{align}
 & var(X)=E[X^2]=\frac{d}{dt}\left( \frac{2t}{(1-t^2)^2}\right)|_{t=0}& \\
 & var(X)=2\left(\frac{1}{(1-t^2)^2} +\frac{4t^2}{(1-t^2)^3}\right) & \\
 & var(X)=\frac{2\left(4t^2(1-t^2)^2 +(1-t^2)^3\right)}{(1-t^2)^3(1-t^2)^2} & \\
 & var(X)=\frac{2\left((1-t^2)^2(4t^2+(1-t^2))\right)}{(1-t^2)^3(1-t^2)^2} & \\ 
 & var(X)=\frac{2(1+3t^2)}{(1-t^2)^3}|_{t=0} & \\
 & var(X)=\frac{2(1+3(0)^2)}{(1-(0)^2)^3} \\
 & var(X)=\frac{2}{1}=2\end{align}$$
