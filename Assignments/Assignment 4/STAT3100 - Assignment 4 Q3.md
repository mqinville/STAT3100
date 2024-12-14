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

**Question 3**
3. Let $\mu$ and $\sigma^2$ be the mean and variance of the random variable $X$. Determine $E\left[ \frac{X-\mu}{\sigma} \right]$ and $E\left[( \frac{X-\mu}{\sigma} )^2\right]$.
	
	We will first start with $E\left[ \frac{X-\mu}{\sigma} \right]$:
		$$\begin{align} \\
 & E\left[ \frac{X-\mu}{\sigma} \right]=\frac{E[X-\mu]}{\sigma}=\frac{{E[X]-\mu}}{\sigma}& \\
 & \frac{{E[X]-\mu}}{\sigma}=\frac{{\mu-\mu}}{\sigma}=\frac{0}{\sigma}=0 & \\
 & \therefore \; \; \;  E\left[ \frac{X-\mu}{\sigma} \right]=0
\end{align}$$We will now determine $E\left[( \frac{X-\mu}{\sigma} )^2\right]$. We will start by expanding $( \frac{X-\mu}{\sigma} )^2$:$$
\left(  \frac{X-\mu}{\sigma}  \right)^2=\frac{(X-\mu)^2}{\sigma^2}=\frac{{X^2+\mu^2-2X\mu}}{\sigma^2}$$ Continuing with $E\left[( \frac{X-\mu}{\sigma} )^2\right]$: $$
E\left[\left(  \frac{X-\mu}{\sigma}  \right)^2\right]=E\left[ \frac{{X^2+\mu^2-2X\mu}}{\sigma^2} \right]=\frac{{E[{X^2+\mu^2-2X\mu}]}}{\sigma^2}=\frac{{E[X^2]+\mu^2-2\mu E[X]}}{\sigma^2}$$$$
E\left[\left(  \frac{X-\mu}{\sigma}  \right)^2\right]=\frac{{E[X^2]+{E[X]}^2-2\mu^2}}{\sigma^2}=\frac{{E[X^2]+{E[X]}^2-2{E[X]}^2}}{\sigma^2} $$ $$
E\left[\left(  \frac{X-\mu}{\sigma}  \right)^2\right]=\frac{{E[X^2]-E^2[X]}}{\sigma^2}=\frac{var(X)}{\sigma^2}=\frac{\sigma^2}{\sigma^2}$$ $$
E\left[\left(  \frac{X-\mu}{\sigma}  \right)^2\right]=1$$
 