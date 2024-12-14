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

<hr style=font-size: 0.85em;>

**Question 1**
1. A fair coin is tossed five times. Let $X$ be the number of heads that occur, and let $Y$ be the number of heads occurring on the last two tosses. Find the conditional probability distribution of $X$ for all possible values of $Y$.
   
   The question tells us:
    - $X$ is the number of heads that occur throughout the 5 tosses $\implies X ={0,1,2,3,4,5}$
	-  $Y$ is the number of heads that occur in the **last 2** tosses (out of the 5) $\implies Y = {0,1,2}$
	
	This question is asking us to find $f_{X|Y}(x|y)=P(X=x|Y=y)$, which is the probability that $x$ amount of head were flipped in 5 tosses given that there are $y$ heads flipped in the **last two tossed**. 
	
	Let us define a new event: $X_{3 }$, which represents the number of heads flipped in the first 3 of 5 tosses. Then this question is asking for $P(X_{3}=x_{3})$, the probability of getting $x_{3}$ amount of head within the first three tosses. This implies that $X_{3}=0,1,2,3$. 
	
	Since $x_3$ is the amount of heads flipped in the first 3 tosses, then it follows that $x_3=x-y$, which is the difference between the total number of heads in 5 tosses and the number of heads in the last two tosses.
	Therefore $P(X_{3}=x_{3})=P(X_{3}=x-y)$. We now need to find $f(x_{3})=f_{X|Y}(x|y)$:
	The coin that is being tossed is a fair coin, which means the probility of landing on either heads or tails is $0.5$. We flip the coin three times, each flip being independent from one another. $\implies(0.5)^3$
	In the first flips we have ${3\choose{x_{3}}}={3\choose{x-y}}$ amount of ways to get $x_{3}$ amount heads. $\implies{3\choose{x-y}}$.
	
	Thus, $f(x_{3})=f_{X|Y}(x|y)=P(X_{3}=x-y)={3\choose{x-y}}(0.5)^3$. Now to find the probabilities we sum through all possible values of $x$ and $y$.
		
$${\sum_{\forall x\in X}}\sum_{{\forall y\in Y}}{3\choose{x-y}}(0.5)^3=
 \begin{array}{c c|c|c|c|c}
   & X & 0 & 1 & 2 & 3 & 4 & 5\\
\hline
  & 0 & \frac{1}{8} & \frac{3}{8} & \frac{3}{8} & \frac{1}{8} & 0 & 0 \\\
Y & 1 & 0 & \frac{1}{8} & \frac{3}{8} & \frac{3}{8} & \frac{1}{8} & 0 \\
  & 2 & 0 & 0 & \frac{1}{8} & \frac{3}{8} & \frac{3}{8} & \frac{1}{8} \\
\end{array}$$


 

