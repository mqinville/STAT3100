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

**Question 5**
5. During one stage in the manufacture of integrated circuit chips, a coating must be applied. If 70% of chip receive a thick enough coating, find the probability that, among 15 chips,


(a) at least 12 will have thick enough coatings;
   
   As we have a fixed number of Bernoulli trials with 2 outcomes, where the probability of each outcome is constant, we can assume that this probability follows a binomial distribution, where $p=0.7,n=15$. We want the probability that **at least** 12 chips will have thick enough coating, in other words we want $P(X\geq12)=1-P(X\lt 12)=1-\sum_{x=0}^{11}P(X=x)$. $$\begin{align}  \\
 &P(X\geq 12) =1-\left( \sum_{x=0}^{11} \binom{15}{x}0.7^x(0.3)^{15-x} \right) & \\
 & P(X \geq 12) = 1-0.7031320577 & \\
 & P(X \geq 12) = 0.2968679423 &\end{align}$$
(b) at most 6 will have thick enough coatings;

This again follows a binomial distribution with $n=15,p=0.7$. We want to find that at most 6 will have thick enough coatings, in other words we want $P(X\leq 6)$. $$\begin{align}
 & P(X\leq 6)=\sum_{x=0}^6 \binom{15}{x}(0.7)^x (0.3)^{15-x}& \\
 & P(X\leq 6)=0.01524252577
\end{align}$$(c) exactly 10 will have thick enough coating;

This again follows the same binomial distribution as the last 2 parts. The probability of getting exactly 10 chips with thick enough coating is $P(X=10)=\binom{15}{10}(0.7)^{10}(0.3)^5=0.206130381$.







   

