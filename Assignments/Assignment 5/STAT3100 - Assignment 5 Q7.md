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

**Question 7**
7. (Bonus question) A grocery store is running a sales promotion where a customer will  receive one of the letters A, E, L, S, U and V for each purchase. The letters are given away randomly by cashier. If a customer collects all six letters (“VALUES”), he/she will get a coupon of $10 that can be used in the store. What is the expected number of purchases need to get a coupon.
   
   Let $X$ be the number of purchases needed to collect **all six letters** and let $X_{i},i \in \{ 0,1,\dots,5 \}$ be the number of purchases required to get the $i^{th}$ letter, it then follows that $X=X_{0}+X_{1}+\dots+X_{5}$.  Since each $X_{i}$ counts the number of purchases until the $i^{th}$ letter is obtained the probability to get the $i^{th}$ letter is $\frac{{6-i}}{6}$. Therefore, $P( X_{0})=\frac{6}{6},P(X_{1})= \frac{5}{6},P( X_{2})=\frac{4}{6},P( X_{3})=\frac{4}{6},P( X_{4})=\frac{2}{6},P( X_{5})=\frac{1}{6}$.
   
   We are looking for the expected number of purchases needed to get a coupon, or rather $E[X]$. 
   Since $X=X_{0}+X_{1}+\dots+X_{5}$, $$\begin{align}
 &E[X]=E[X_{1}+X_{2}+\dots+X_{6}]=E[X_{1}]+E[X_{2}]+\dots+E[X_{6}] &  \\
 & E[X]=\frac{1}{p_{0}}+\frac{1}{p_{1}}+\frac{1}{p_{2}}+\frac{1}{p_{3}}+\frac{1}{p_{4}}+\frac{1}{p_{5}} &  \\
 & E[X]=1+\frac{6}{5}+\frac{6}{4}+\frac{6}{3}+\frac{6}{2}+\frac{6}{1} &  \\
 & E[X]=14.7
\end{align}$$
   
   