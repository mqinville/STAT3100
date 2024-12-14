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

**Question 3**
3. Gamma($\alpha$, $\beta$) distribution has the pdf $f(x;\alpha,\beta)=\frac{1}{\beta^\alpha \Gamma(\alpha)}x^{\alpha-1}e^{-\frac{x}{\beta}},x>0$
   (a) Find the $r^{th}$ moment, $E[X^r]$ of the distribution. $$\begin{align}
 & E[X^r]=\int_{0}^\infty x^rf(x;\alpha,\beta)dx & \\
 & E[X^r]=\int_{0}^\infty x^r \frac{1}{\beta^\alpha \Gamma(\alpha)}x^{\alpha-1}e^{-\frac{x}{\beta}}dx & \\
 & E[X^r]= \frac{1}{\beta^\alpha \Gamma(\alpha)} \int_{0}^\infty x^r x^{\alpha-1}e^{-\frac{x}{\beta}}dx & \\
 & E[X^r]= \frac{1}{\beta^\alpha \Gamma(\alpha)} \int_{0}^\infty x^{\alpha+r-1}e^{-\frac{x}{\beta}}dx & \\
 & E[X^r]= \frac{1}{\beta^\alpha \Gamma(\alpha)} \beta^{\alpha+r} \Gamma(\alpha+r) \int_{0}^\infty \frac{1}{\beta^{\alpha+r} \Gamma(\alpha+r)} x^{\alpha+r-1}e^{-\frac{x}{\beta}}dx \\
 & E[X^r]=\frac{1}{\beta^\alpha \Gamma(\alpha)} \beta^{\alpha+r} \Gamma(\alpha+r)(1) &  \\
 & E[X^r]= \frac{1}{\beta^\alpha \Gamma(\alpha)} \beta^{\alpha} \beta^r \; \Gamma(\alpha+r) &  \\
 & E[X^r]= \frac{{\beta^r \; \Gamma(\alpha+r)}}{\Gamma(\alpha)}
\end{align}$$ (b) Find the moment generating function of the Gamma distribution and use it to  
find mean and variance of the distribution. $$\begin{align}
 & E[e^{tX}]=\int_{0}^\infty e^{tx}\frac{1}{\beta^\alpha \Gamma(\alpha)}x^{\alpha-1}e^{-\frac{x}{\beta}}dx &  \\
 & E[e^{tX}]=\frac{1}{\beta^\alpha \Gamma(\alpha)}\int_{0}^\infty e^{tx}x^{\alpha-1}e^{-\frac{x}{\beta}}dx &  \\
 & E[e^{tX}]=\frac{1}{\beta^\alpha \Gamma(\alpha)}\int_{0}^\infty x^{\alpha-1}e^{tx-\frac{x}{\beta}}dx &  \\
 & E[e^{tX}]=\frac{1}{\beta^\alpha \Gamma(\alpha)}\int_{0}^\infty x^{\alpha-1}e^{-x(-t+\frac{1}{\beta})}dx
\end{align}$$ Let $y=x\left( -t+\frac{1}{\beta} \right) \implies dx=\frac{1}{-1+\frac{1}{\beta}}dy$, $x=\frac{y}{-t+\frac{1}{\beta}}$, we than have: $$
\begin{align}
 & E[e^{tX}]=\frac{1}{\beta^\alpha \Gamma(\alpha)}\int_{0}^\infty \left(\frac{y}{-t+\frac{1}{\beta}}\right)^{\alpha-1}e^{-y} \frac{1}{\left( -t+\frac{1}{\beta} \right)} dy  &  \\
 & Eß[e^{tX}]=\frac{1}{\beta^\alpha \Gamma(\alpha)}\int_{0}^\infty y^{\alpha-1} \left( -t_+\frac{1}{\beta} \right)^{-(\alpha-1)} e^{-y} \frac{1}{\left( -t+\frac{1}{\beta} \right)} dy &  \\
 & E[e^{tX}]=\frac{1}{\beta^\alpha \Gamma(\alpha)} \left( -t+\frac{1}{\beta} \right)^{-\alpha} \int_{0}^\infty y^{\alpha-1}e^{-y}dy &  \\
 & E[e^{tX}]=\frac{1}{\beta^\alpha \Gamma(\alpha)} \left( -t+\frac{1}{\beta} \right)^{-\alpha} \Gamma(\alpha) &  \\
 & E[e^{tX}]=\frac{1}{\beta^\alpha \left( -t+\frac{1}{\beta} \right)^\alpha} & \\
 & E[e^{tX}]=\frac{1}{(1-\beta t)^\alpha}
	\end{align}$$ Now to find the mean: $$\begin{align}
 & E[X]=\frac{d}{dt}M_{x}(t)\left.\right|_{t=0} \\
 & E[X]= \left.\frac{d}{dt} \frac{1}{(1-\beta t)^\alpha} \right|_{t=0} &  \\
 & E[X]= \left.(1-\beta t)^{-\alpha} \right|_{t=0}  &  \\
 & E[X]= \left. -\alpha (1-\beta t)^{-\alpha-1}(-\beta) \right|_{t=0} &  \\
 & E[X]= -\alpha(-\beta) &  \\
 & E[X]=\alpha \beta
\end{align}$$ So $\mu=\alpha \beta$. Now to find the second moment $$
\begin{align}
 & E[X^2]= \left. \frac{d}{dt} \left( \alpha \beta (1-\beta t)^{-\alpha-1}\right) \right|_{t=0} & \\
 & E[X^2]= \left. \alpha \beta (-\alpha-1)(1-\beta t)^{-\alpha-2}(-\beta) \right|_{t=0} &  \\
 & E[X^2]= -\beta^2(-\alpha^2-\alpha) \\
 & E[X^2]= \alpha^2\beta^2+\alpha \beta^2 & 
\end{align}
$$ Now to find the variance: $$
\begin{align} \\
 & var(X)=E[X^2]-(E[X])^2 &  \\
 & var(X)=\alpha^2\beta^2+\alpha \beta^2-(\alpha \beta)^2 &  \\
 & var(X)=a\beta^2
\end{align}$$
 
   