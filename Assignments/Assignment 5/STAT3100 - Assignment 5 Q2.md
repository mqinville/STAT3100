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

**Question 2**
2. Flaws on a certain type of drapery material appear on the average of one in 150 square feet. Assume flaws appear according to a Poisson distribution.
   
   (a) Find the probability of at most one flaw appearing in 225 square feet of drapery.
   
   Assuming flaws appear according to a poisson distribution, then we know the $p.m.f$ of flaws appearing on certain type of drapery material is: $$
\begin{align}
f(x;\lambda)=\frac{{\lambda^xe^{-\lambda}}}{x!},x \in \{ 0,1,2,3,\dots \}
\end{align}
$$ In this scenario, a success represents finding flaw on the drapery material in question, and $\lambda$ represents the mean number of successes per area unit, in other words $\lambda=\frac{1}{150}$. We want to find the probability of having one flaw in 225 square feet of drapery, thus we must scale $\lambda$ by the area being considered, hence $\lambda=\frac{1}{150}(250)=1.5$. So we want to find  $P(X\leq 1)=f\left( 0;1.5\right)+f\left( 1;1.5 \right)$. $$\begin{align} \\ &P(X\leq1)=\frac{{\left({1.5}\right)^0 e^{-(1.5)}}}{0!}+\frac{{\left(1.5\right)^1 e^{-(1.5)}}}{1!}& \\ &P(X\leq 1)=0.5578254003&\end{align}$$
(b) Find the probability that no flaws appear in 75 square feet of drapery.

We want the probability of no flaws, since a success represents the number of flaws we found, we want the probability of no successes $\implies x=0$. We scale lambda to the square footage being considered $\implies \lambda=\frac{1}{150}\times 75=0.5$. We want $P(X=0)=f(0;0.5)$ $$\begin{align} \\
&P(X=0)=\frac{{\left({0.5}\right)^0 e^{-(0.5)}}}{0!}& \\
&P(X=0)=0.6065306597
\end{align}$$
















   