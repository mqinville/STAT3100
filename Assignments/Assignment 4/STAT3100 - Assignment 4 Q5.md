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

**Question 5**
5. If the joint pdf of $X$ and $Y$ is given by: $$
f_{X,Y}(x,y)=\frac{1}{3}(x+y)
	$$
(a) find the $E(X)$, $E(Y)$, and $E(XY)$.
$$\begin{align} \\
&E[X]=\int_{-\infty}^\infty xf_{X}(x)dx=\int_{0}^1x \int_{0}^2f_{X,Y}(x,y)dydx & \\
&E[X]= \int_{0}^1x \int_{0}^2 \frac{1}{3}(x+y)dydx= \; \frac{1}{3} \int_{0}^1x \int_{0}^2 (x+y)dydx& \\
&E[X]=\frac{1}{3} \int_{0}^1x \left[xy+\frac{1}{2}y^2\right]^2_{0}dx& \\
&E[X]=\frac{1}{3} \int_{0}^1x(2x+2)dx= \frac{1}{3} \int_{0}^1(2x^2+2xdx)& \\
&E[X]=\frac{1}{3} \left[\frac{2}{3}x^3+ x^2\right]^1_{0} & \\
&E[X]=\frac{5}{9} & \\ \\
\end{align}$$
$$\begin{align} \\
&E[Y]=\int_{-\infty}^\infty y f_{Y}(y)dy=\int_{0}^2y \int_{0}^1f_{X,Y}(xy)dxdy& \\
&E[Y]=\int_{0}^2y \int^2_{0} \frac{1}{3}(x+y)dxdy = \frac{1}{3} \int^2_{0}y \int^1_{0}x+y\;dxdy & \\
&E[Y]= \frac{1}{3} \int_{0}^2y \left[\frac{1}{2}x^2+xy\right]^1_{0}dy =\frac{1}{3}\int_{0}^2y\left( \frac{1}{2}+y \right)dy& \\
&E[Y]=\frac{1}{3}\int^2_{0} \frac{1}{2}y+y^2dy=\frac{1}{3}\left[\frac{1}{4}y^2+\frac{1}{3}y^2\right]^2_{0} & \\
&E[Y]=\frac{1}{3}\left( 1+\frac{8}{3} \right)=\frac{1}{3}\left( \frac{11}{3} \right)&\\
&E[Y]=\frac{11}{9}& \\ \\
\end{align}$$
$$\begin{align} \\
&E[XY]=\int_{-\infty}^\infty \int_{-\infty}^\infty xyf_{XY}(xy)dxdy=\int_{0}^2
\int_{0}^1xy \frac{1}{3}(x+y)dxdy & \\
&E[XY]=\frac{1}{3} \int_{0}^2y\int_{0}^1x(x+y)dxdy=\frac{1}{3} \int_{0}^2y\int_{0}^1x^2+xy\;dxdy & \\
&E[XY]=\frac{1}{3} \int_{0}^2y \left[\frac{1}{3}x^3+\frac{1}{2}x^2y\right]^1_{0}dy =\frac{1}{3} \int_{0}^2y\left( \frac{1}{3}+\frac{1}{2}y \right)dy& \\
&E[XY]=\frac{1}{3} \int_{0}^2 \frac{1}{3}y+\frac{1}{2}y^2dy& \\
&E[XY]=\frac{1}{3}\left[\frac{1}{6}y^2+\frac{1}{6}y^3\right]^2_{0}=\frac{1}{18}(12)=\frac{12}{18}& \\ 
&E[XY]=\frac{2}{3}
\end{align}$$

(b) find the mean and variance of $W=3X+4Y-5$
$$\begin{align}
&\mu_{W}=E[W]=E[3X+4Y-5]=3E[X]+4E[Y]-5& \\
&\mu_{W}=3\left( \frac{5}{9} \right)+4\left( \frac{11}{9} \right)-5& \\ \\
&\mu_{W}=\frac{15}{9}+\frac{44}{9}-5=\frac{59}{9}-5 & \\
&\mu_{W}=\frac{14}{9}& \\
\end{align}$$
$$\begin{align}
&\sigma^2_{W}=var(W)=var(3X+4Y-5)=var(3X+4Y)& \\
&\sigma^2_{W}=3^2var(X)+4^2var(Y)-2(3)(4)cov(X,Y)& \\
\end{align}$$
$$\begin{align}
&cov(X,Y)=E[XY]-E[X]E[Y]=\frac{2}{3}-\frac{5}{9}\left( \frac{11}{9} \right)& \\
&cov(X,Y)=-\frac{1}{81} \\
\end{align}$$
$$\begin{align}
&E[X^2]=\int^\infty_{-\infty}x^2f_{X}(x)dx=\frac{1}{3}\int^1_{0}x^2(2x+2)dx& \\
&E[X^2]=\frac{1}{3}\int^1_{0}2x^3+2x^2dx=\frac{2}{3} \left[\frac{1}{4}x^4+\frac{1}{3}x^3\right]^1_{0}=\frac{2}{3}\left( \frac{1}{4}+\frac{1}{3} \right)& \\
&E[X^2]=\frac{7}{18}& \\
\end{align}$$
$$\begin{align}
&E[Y^2]=\int^\infty_{-\infty}y^2f_{Y}(y)dy=\frac{1}{3}\int^2_{0}y^2\left( \frac{1}{2}+y \right)dy& \\
&E[Y^2]=\frac{1}{3} \int^2_{0}y^3+\frac{1}{2}y^2dy=\frac{1}{3}\left[\frac{1}{4}y^4+\frac{1}{6}y^3\right]^2_{0}=\frac{1}{3}\left( \frac{16}{3} \right)& \\
&E[Y^2]=\frac{16}{9}& \\
\end{align}$$
$$\begin{align}&\sigma^2_{W}=9(E[X^2]-E^2[X])+16(E[Y^2]-E^2[Y]-24cov(X,Y))& \\
&\sigma^2_{W}=9\left( \frac{7}{18} -\frac{5^2}{9^2} \right)+16\left( \frac{16}{9} -\frac{11^2}{9^2}\right)+24\left( -\frac{1}{81} \right)& \\
&\sigma^2_{W}=\frac{805}{162}&
\end{align}$$



(c) find the conditional mean and conditional variance of $Y$ given $X=\frac{{1}}{2}$
$$
\begin{align} \\
&f_{Y|X}(y|x)=\frac{f_{X,Y}(x,y)}{f_{Y}(y)}=\frac{\frac{1}{3}(x+y)}{\frac{1}{3}(2x+2)}& \\
&f_{Y|X}(y|x)=\frac{1}{2}\frac{(x+y)}{x+1}& \\
&f_{Y|X}\left( y|{\frac{1}{2}} \right)=\frac{1}{2} \left(\frac{{{\frac{1}{2}}+y}}{\frac{3}{2}}\right)=\frac{1}{3} \left( \frac{1}{2}+y \right) & \\
&& \\
&& \\
&E\left[ Y|X=\frac{1}{2} \right] = \int^\infty_{-\infty}yf_{Y|X}{\left( y|{\frac{1}{2}} \right)}dy=\int^2_{0}y \frac{1}{3}\left( \frac{1}{2}+y \right)dy = \frac{1}{3}  \int^2_{0} \frac{1}{2}y+y^2dy& \\
&E\left[ Y|X=\frac{1}{2} \right] = \frac{1}{3} \left[\frac{1}{4}y^2+ \frac{1}{3}y^3\right]^2_{0}& \\
&E\left[ Y|X=\frac{1}{2} \right]=\frac{11}{9} & \\
&& \\
&& \\
&var\left( Y|{X=\frac{1}{2}} \right)=E\left[ Y^2|X=\frac{1}{2} \right]-E^2\left[ Y|X=\frac{1}{2} \right]=\int^2_{0}y^2f_{Y|X}{\left( y|{\frac{1}{2}} \right)}dy-\left( \frac{11}{9} \right)^2&& \\
&var\left( Y|{X=\frac{1}{2}} \right)= \int^2_{0}y^2 \frac{1}{3}\left( \frac{1}{2}+y \right)- \frac{121}{81}=\frac{1}{3}\int^2_{0} \frac{1}{2}y^2+y^3dy- \frac{121}{81} & \\
&var\left( Y|{X=\frac{1}{2}} \right)= \frac{1}{3} \left[\frac{1}{6}y^3+ \frac{1}{4}y^4\right]^2_{0}-\frac{121}{81}& \\
&var\left( Y|{X=\frac{1}{2}} \right)= \frac{16}{9}-\frac{121}{81}& \\
&var\left( Y|{X=\frac{1}{2}} \right)=\frac{23}{81}

\end{align}
$$