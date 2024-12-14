<div style="display: flex; justify-content: space-between; font-size: 0.85em; margin-bottom: 0;">
    <div style="text-align: left;">
        <strong>STAT3100</strong><br>
        <strong>Assignment 5</strong><br>
        <strong>November 29th, 2024</strong>
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

**Question 1**
1. A geometric distribution has the probability distribution function 
   $f(x;p)=p(1-p)^{x-1},$ for $x=1,2,3,\dots$
   
 (a) Find the moment generating function for the geometric distribution and use it to find mean and variance of the distribution. 
$$ \begin{align}  \\ 
 & M_{X}(t)=E{[e^{Xt}]=\sum_{x=1}^n e^{xt}f(x;p)} & \\
 & M_{X}(t)=\sum_{x=1}^n e^{xt}p(1-p)^{x-1}=p\left(\frac{{1-p}}{1-p}\right) \sum_{x=1}^n e^{xt}(1-p)^{x-1} & \\
 & M_{X}(t)= {\frac{p}{1-p}} \sum_{x=1}^n e^{xt} (1-p)^x=\frac{{p}}{1-p} \sum_{x=1}^n \left(e^t(1-p)\right)^x&
 \end{align}$$
 Let $z=e^t(1-p)$, we then have: $$\begin{align}& M_{X}(t)={\frac{p}{1-p}}\sum_{x=1}^n z^x & \\\end{align}$$Note that the arithmetic sequence for some some number $k<1$, $\sum_{i=1}^nk^i=\frac{k}{1-k}$. We then have: $$\begin{align}
 & M_{X}(t)={\frac{p}{1-p}}\left( \frac{z}{1-z} \right)=\frac{p}{1-p}\left( \frac{{e^t(1-p)}}{1-e^t(1-p)} \right) & \\
 & M_{X}(t)={\frac{p\;e^t}{1-e^t(1-p)}} & \end{align}$$ Now we find the mean and variance: $$
\begin{align}
& \mu = \left. \frac{d}{dt}M_{X}(t) \right|_{t=0} = \left. \frac{d}{dt} {\frac{p\;e^t}{1-e^t(1-p)}} \right |_{t=0} & \\ \\
& \mu= \frac{{(1-e^t(1-p))(pe^t)+(pe^t(e^t(1-p)))}}{(1-e^t(1-p))^2} \left.\right|_{t=0} & \\
&\mu=\left. \frac{pe^t}{(1-e^t(1-p))^2} \right|_{t=0} =\frac{p}{p^2}& \\
&\mu = \frac{1}{p}
\end{align}$$ To find the variance we must first find $E[X^2]$, which can be found by finding 
$\left.\frac{d^2}{d^2t}(M_{X}(t)) \right|_{t=0}$ $$\begin{align}
&\left.\frac{d^2}{d^2t}(M_{X}(t)) \right|_{t=0}=\frac{d}{dt}\left( \frac{pe^t}{(1-e^t(1-p))} \right)|_{t=0}& \\
&\left.\frac{d^2}{d^2t}(M_{X}(t)) \right|_{t=0}= \left. \frac{{(1-e^t(1-p))^2(pe^t)-p(e^t)2(1-e^t(1-p)(-e^t(1-p)))}}{(1-e^t(1-p))^4} \right|_{t=0}& \\
&\left.\frac{d^2}{d^2t}(M_{X}(t)) \right|_{t=0}= pe^t\left. \frac{{(1-e^t(1-p))^2-2(1-e^t(1-p)(-e^t(1-p)))}}{(1-e^t(1-p))^4} \right|_{t=0}& \\
&\left.\frac{d^2}{d^2t}(M_{X}(t)) \right|_{t=0} =\frac{{p((1-(1-p))^2+2(1-(1-p))(1-p))}}{p^4}& \\
&\left.\frac{d^2}{d^2t}(M_{X}(t)) \right|_{t=0}=\frac{{p^2+2p-2p^2}}{p^3}& \\
&\left.\frac{d^2}{d^2t}(M_{X}(t)) \right|_{t=0} = \frac{{2-p}}{p^2}
\end{align}$$ Now to find the variance $$\begin{align}
&var(X)=E[X^2]-(E[X])^2 = \frac{{2-p}}{p^2}-\left( \frac{1}{p} \right)^2& \\
&var(X)=\frac{{1-p}}{p^2}
\end{align}$$
(b) Differentiating with respect to $p$ on the both sides of the equation $\sum_{x=1}^\infty f(x;p)=1$$$\begin{align}
 & \frac{d}{dp} \sum_{x=1}^\infty f(x;p)= \frac{d}{dp} 1 & \\
 & \sum_{x=1}^\infty \frac{d}{dp} p(1-p)^{x-1}=0 & \\
 & \sum_{x=1}^\infty (1-p)^{x-1}+\left(p(x-1)(1-p)^{x-2}(-1)\right)=0 & \\
 & \sum_{x=1}^\infty (1-p)^{x-1}-\sum_{x=1}^\infty p(x-1)(1-p)^{x-2}=0 & \\
 &  \sum_{x=1}^\infty (1-p)^{x-1}=\sum_{x=1}^\infty p(x-1)(1-p)^{x-2}
\end{align}$$ As seen in class, the LHS is a geometric sum which evaluates to $\frac{1}{1-(1-p)}=\frac{1}{p}$. $$\begin{align}
 & \frac{1}{p}=\sum_{x=1}^\infty p(x-1)(1-p)^{x-2} & \\
 & \frac{1}{p}=\sum_{x=0}^\infty p(x)(1-p)^{x-1} & \\
 & \frac{1}{p}=0+\sum_{x=1}^\infty xp(1-p)^{x-1}& \\
 & \frac{1}{p}=\sum_{x=1}^\infty xp(1-p)^{x-1} &
\end{align}$$ Recall that for a geometric distribution $E[X]=\sum_{x=1}^\infty xf(x;p)=\frac{1}{p}$ Therefore we have : $$\begin{align}
 & \frac{1}{p}=\frac{1}{p} & \\ \\
\end{align}$$
(c) Show that $P(X=x+n|X>n)=P(X=x)$. $$\begin{align}
 & P(X=x+n|X>n)=\frac{{P(X=x+n\;\; \cap X>n)}}{P(X>n)} = \frac{P(X=x+n)}{P(X>n)}& \\
 & P(X=x+n|X>n)=\frac{{p(1-p)^{x+n-1}}}{P(X>n)}
\end{align}$$ We know that $P(X>n)=(1-p)^n$ because the probability that the first success occurs after $n$ trials is the probability that the first $n$ trials are all failures. $$\begin{align}
 & P(X=x+n|X>n)=\frac{p(1-p)^{x+n-1}}{(1-p)^n} & \\
 & P(X=x+n|X>n)=\frac{p(1-p)^{x-1}(1-p)^{n}}{(1-p)^n} & \\
 & P(X=x+n|X>n)=p(1-p)^{x-1} & \\
 & P(X=x+n|X>n) = P(X=x) &
\end{align}$$


  