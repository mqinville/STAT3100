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

**Question 4**
4. Let $X$ and $Y$ be random variables for the location of each point in the unit circle $\left\{(x,y):x^2+y^2< \frac{1}{2} \right\}$ given that each point is equally likely to be selected in the unit circle with the joint pdf of $X$ and $Y$ given as $F_{X,Y}(x,y)=\frac{1}{\pi},for \; 0<x^2+y^2<1$. Suppose 2000 points are selected independently and randomly from the unit circle. Let $W$ be the number of points that fall into $A= \left\{(x,y):x^2+y^2< \frac{1}{2} \right\}$. What is the distribution of $W$. Find its mean and variance.
   
   Our sample space (the unit circle) has a maximum radius of $1$, it follows that its area is $\pi r_{max}^2=\pi(1)^2=\pi$, and thus the probability of a point landing in the unit circle is the inverse of its area. Likewise, the inner circle has a maximum radius of $\frac{1}{2}$ implying that the inner circle's area is $\pi r_{max}^2=\pi\left( \frac{1}{\sqrt{ 2 }} \right)^2=\pi{\frac{1}{2}}$. The probability of any point $(x,y)$ being within the inner circle is the the area of the inner circle over the area over the area of the unit circle. In other words $P((x,y)\in A)=\frac{{\pi{\frac{1}{2}}}}{\pi}=\frac{1}{2}$.
   
   Each point $(x,y)$ has two outcomes possible, it is either in $A$ or not in $A$. We have a fixed sample size of $2000$ points which are selected randomly and independently from the unit circle. In other words we have a fixed number of Bernoulli trials that are selected independently and randomly from the sample space in question, it follows that $W$ has a binomial distribution with $n=2000,p=0.5$.
   
   The mean and variance of a random variable with a binomial distribtuion is $np$ and $np(1-p)$ respectively. Thus : $$\begin{align}
 & \mu=np=2000(0.5)=1000 & \\
 & \sigma^2=np(1-p)=2000(0.5)(0.5)=500
\end{align}$$