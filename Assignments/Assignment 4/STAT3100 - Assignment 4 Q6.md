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

**Question 6**
6. (Ex. 3.100, P123, Recommended textbook of Miller & Miller (2014)) A sharpshooter is aiming at a circular target with radius 1. While setting the origin of an $xy$-plane at the center of the target, let the $X$ and $Y$ represent the coordinates of the points of impact at the $xy$-plane. We have the joint pdf of $X$ and $Y$ as: $f_{X,Y}(x,y)=\frac{1}{\pi}$ for $0<x^2+y^2<1$. Find:
   
   (a) $P[(X,Y)\in A]$, where $A$ is the sector of the circle in the first quadrant bounded  
   by the lines $Y=0$ and $Y=X$.
   
   To find this area we will use 2 integrals: $$\int_{0}^{\frac{1}{\sqrt{{2}}}}\int_0^x \frac{1}{\pi}dydx+\int_{\frac{1}{\sqrt{ 2 }}}^1\int_{0}^{\sqrt{ 1-x^2 }} \frac{1}{\pi}dydx$$
   The first integral calculate the triangular area bounded by y=o to y=x, yet this doesnt capture the entire sector $A$ as it doesn't account for the curvature of the target. The second integral accounts for this extra area added by the curvature of the circle, we get our bound for x by observing what is not covered by the first integral, which is $\frac{1}{\sqrt{ 2 }}<x<1$, and we get our bound for y by isolating for in $x^2+y^2=1\implies y=\sqrt{ 1-x^2 }$
   Lets not compute the integral: 
$$\begin{align}
&P[(X,Y)\in A]=\int_{0}^{\frac{1}{\sqrt{{2}}}}\int_0^x \frac{1}{\pi}dydx\;+\int_{\frac{1}{\sqrt{ 2 }}}^1\int_{0}^{\sqrt{ 1-x^2 }} \frac{1}{\pi} dydx& \\
&P[(X,Y)\in A]= \frac{1}{\pi} \int_{0}^{\frac{1}{\sqrt{{2}}}}\int_0^x 1dydx+ \; \frac{1}{\pi}\int_{\frac{1}{\sqrt{ 2 }}}^1\int_{0}^{\sqrt{ 1-x^2 }}1dydx& \\
& P[(X,Y)\in A]=\frac{1}{\pi}\int_{0}^{\frac{1}{\sqrt{{2}}}}\left[y\right]^x_{0}\;dx \;+\frac{1}{\pi}\int_{\frac{1}{\sqrt{ 2 }}}^1[y]^\sqrt{ 1-x^2 }_{0}dx & \\
&P[(X,Y)\in A]=\frac{1}{\pi} \int_{0}^{\frac{1}{\sqrt{{2}}}} xdx\;+\frac{1}{\pi} \int_{\frac{1}{\sqrt{ 2 }}}^1 \sqrt{ 1-x^2 }dx &\\ \\
&P[(X,Y)\in A]= \frac{1}{\pi}\left[ \frac{1}{2}x^2 \right]^{\frac{ 1 }{\sqrt{ 2 }}}_{0}+\frac{1}{\pi}\left[\frac{1}{2}\left(x\sqrt{ 1-x^2 }+\arcsin(x)\right)\right]^1_{\frac{1}{\sqrt{ 2 }}}& \\
&P[(X,Y)\in A]=\frac{1}{8}&
\end{align} \\$$

   
   (b) $P\left( 0<X^2+Y^2<{\frac{1}{2}} \right)$
   
   We know that $X^2+Y^2=r^2$. 
   The bigger circle (the unit circle) is bounded by $0<x^2+y^2<1 \implies 0<r^2<1 \implies 0<r<1,$ thus the maximum radius for the outer circle is 1. It follows the maximum area for the out circle is: $A_{r=1}=\pi r^2=\pi(1)^1=\pi$. 
   Therefore the outer circle has an area of $\pi$.
   
   The inner circle is bounded by $0<X^2+Y^2<{\frac{1}{2}} \implies 0<r^2<{\frac{1}{2}}\implies 0<r<{\frac{1}{\sqrt{ 2 }}}$. Thus the inner circle has a maximum radius of $r=\frac{1}{\sqrt{ 2 }}$. It follows the maximum area for the inner circle is : $A_{r=\frac{1}{\sqrt{ 2 }}}=\pi r^2=\pi\left( \frac{1}{\sqrt{ 2 }} \right)^2=\pi{\frac{1}{2}}$.  
   By laws of probability $P\left( 0<X^2+Y^2<{\frac{1}{2}} \right)=\frac{A_{r={\frac{1}{\sqrt{ 2 }}}}}{A_{r=1}}=\frac{{\pi{\frac{1}{2}}}}{\pi}=\frac{1}{2}$. Logically this follows as the inner circle is half as big as the unit circle, which in this context is our sample space.
   $\therefore P\left( 0<X^2+Y^2<{\frac{1}{2}} \right)=\frac{1}{2}$
