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

**Question 6**
6. Using the gamma function we can write $\Gamma\left( \frac{1}{2} \right)=\sqrt{ 2 }\int_{0}^\infty e^{-1/2z^2}dz$ and $\Gamma\left( \frac{1}{2} \right)=\sqrt{ \pi }$. If $X-N(u,\sigma^2)$, then show that the function $f(x;\mu,\sigma^2)=\frac{1}{\sqrt{ 2\pi }\sigma}e^{-\frac{{(x-\mu)}^2}{2{\sigma^2}}}$ is a probability density.
   
   To show it is a probability density we must show that $f(x;\mu,\sigma^2)\geq 0,\forall x$ and that $\int_{-\infty}^\infty \frac{1}{\sqrt{ 2\pi }\sigma}e^{-\frac{{(x-\mu)}^2}{2{\sigma^2}}}dx=1$. 
   We know that $z=\frac{x-\mu}{\sigma} \implies \frac{dz}{dx}=\frac{1}{\sigma}\implies dx=\sigma dz$. Lets substitute $x$ for $z$ in the integral. 
   $$\begin{align}
  & \int_{-\infty}^\infty \frac{1}{\sqrt{ 2\pi }\sigma}e^{-\frac{{(x-\mu)}^2}{2{\sigma^2}}}dx = \int_{-\infty}^\infty \frac{1}{\sqrt{ 2\pi }\sigma}e^{-\frac{1}{2}z^2}\sigma dz & \\
 & \int_{-\infty}^\infty \frac{1}{\sqrt{ 2\pi }\sigma}e^{-\frac{{(x-\mu)}^2}{2{\sigma^2}}}dx= \int_{-\infty}^\infty \frac{1}{\sqrt{ 2\pi }}e^{-\frac{1}{2}z^2} dz= \frac{1}{\sqrt{ 2\pi }} \int_{-\infty}^\infty e^{-\frac{1}{2}z^2} dz & \\
 & \int_{-\infty}^\infty \frac{1}{\sqrt{ 2\pi }\sigma} e^{-\frac{{(x-\mu)}^2}{2{\sigma^2}}}dx = \frac{1}{\sqrt{ 2\pi }} \left[\int_{0}^\infty e^{-\frac{1}{2}z^2} dz + \int_{-\infty}^0 e^{-\frac{1}{2}z^2} dz\right] & \\
 & \int_{-\infty}^\infty \frac{1}{\sqrt{ 2\pi }\sigma} e^{-\frac{{(x-\mu)}^2}{2{\sigma^2}}}dx = \frac{1}{\sqrt{ 2\pi }} \left[\frac{1}{\sqrt{ 2 }} \int_{0}^\infty \sqrt{ 2 } e^{-\frac{1}{2}z^2} dz + \frac{1}{\sqrt{ 2 }} \int_{-\infty}^0 \sqrt{ 2 } e^{-\frac{1}{2}z^2} dz\right] & \\
 & \int_{-\infty}^\infty \frac{1}{\sqrt{ 2\pi }\sigma}e^{-\frac{{(x-\mu)}^2}{2{\sigma^2}}}dx = \frac{1}{\sqrt{ 2\pi }} \left[\frac{1}{\sqrt{ 2 }} \Gamma\left( \frac{1}{2} \right) + \frac{1}{\sqrt{ 2 }} \int_{-\infty}^0 \sqrt{ 2 } e^{-\frac{1}{2}z^2} dz\right] & \\
\end{align}$$
Since $z$ is squared, for the range $-\infty<x<0,z^2\geq 0$, therefore $\int_{-\infty}^0 \sqrt{ 2 } e^{-\frac{1}{2}z^2} dz=\int_{0}^\infty \sqrt{ 2 } e^{-\frac{1}{2}z^2} dz$. $$\begin{align}
 & \int_{-\infty}^\infty \frac{1}{\sqrt{ 2\pi }\sigma}e^{-\frac{{(x-\mu)}^2}{2{\sigma^2}}}dx = \frac{1}{\sqrt{ 2\pi }} \left[\frac{1}{\sqrt{ 2 }} \Gamma\left( \frac{1}{2} \right) + \frac{1}{\sqrt{ 2 }} \Gamma\left( \frac{1}{2} \right)\right] & \\
 & \int_{-\infty}^\infty \frac{1}{\sqrt{ 2\pi }\sigma}e^{-\frac{{(x-\mu)}^2}{2{\sigma^2}}}dx = \frac{1}{\sqrt{ 2\pi }} \left[\frac{1}{\sqrt{ 2 }} \sqrt{ \pi } + \frac{1}{\sqrt{ 2 }} \sqrt{ \pi }\right] & \\
 & \int_{-\infty}^\infty \frac{1}{\sqrt{ 2\pi }\sigma}e^{-\frac{{(x-\mu)}^2}{2{\sigma^2}}}dx = \frac{1}{2}+\frac{1}{2}=1
\end{align}$$ Now we must show that $f(x;\mu,\sigma^2)\geq 0,\forall x$: $$
\begin{align}
 & f(x;\mu,\sigma^2)= \frac{1}{\sqrt{ 2\pi }\sigma}e^{-\frac{{(x-\mu)}^2}{2{\sigma^2}}} 
\end{align}$$ We know that $\sigma=\sqrt{ \sigma^2 }$, therefore $\frac{1}{\sqrt{ 2\pi }\sigma}$ is always greater or equal to zero. We also know that when $e$ is put to any power it is always non negative, therefore $f(x;\mu,\sigma^2)= \frac{1}{\sqrt{ 2\pi }\sigma}e^{-\frac{{(x-\mu)}^2}{2{\sigma^2}}}$ always non negative.

Since $f(x;\mu,\sigma^2)$ is always non negative and $\int_{-\infty}^\infty f(x;\mu,\sigma^2)=1$, we know that $f(x;\mu,\sigma^2)$ is a probability density.




