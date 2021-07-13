---
layout: post
title:  "Homework Solution:Part 1"
date:   2021-07-13 16:13:13 +0800
categories: Study
tags: Solution Homework
---


### Homework
#### Zhen Huang

***1.2.1***

Linear operation:


$$
\begin{align}
D(af(x)+bg(x)) =& DL(x)\\
               =& \lim\limits_{\Delta x \rightarr0} \frac{L(x+\Delta x)-L(x)}{\Delta x}\\
               =& \lim\limits_{\Delta x \rightarr0} \frac{af(x+\Delta x)+bg(x+\Delta x)-af(x)-bg(x)}{\Delta x} \\
               =& a \times \lim\limits_{\Delta x \rightarr0} \frac{f(x+\Delta x)-f(x)}{\Delta x} + b \times \lim\limits_{\Delta x \rightarr0} \frac{g(x+\Delta x)-g(x)}{\Delta x}\\
               =& aDf(x)+bDg(x)
\end{align}
$$


Multiplication of functions


$$
\begin{align}
D[fg]  =& \lim\limits_{\Delta x \rightarr0} \frac{f(x+\Delta x)g(x+\Delta x)-f(x)g(x)}{\Delta x} \\
       =& \lim\limits_{\Delta x \rightarr0} \frac{g(x)[f(x+\Delta x)-f(x)]+f(x+\Delta x)[g(x+\Delta x)-g(x)]}{\Delta x} \\
       =& g(x) \lim\limits_{\Delta x \rightarr0} \frac{[f(x+\Delta x)-f(x)]}{\Delta x}
       + \lim\limits_{\Delta x \rightarr0}\frac{f(x+\Delta x)[g(x+\Delta x)-g(x)]}{\Delta x}\\
       =& g(x)Df(x) + f(x)Dg(x)\\
       =& gDf + fDg
\end{align}
$$


Chain rule


$$
\begin{align}
Df(u(x))     &= \lim\limits_{\Delta x \rightarr0} \frac{f(u(x+\Delta x))-f(u(x))}{\Delta x} \\
             &= \lim\limits_{\Delta x \rightarr0} \frac{f(u+\Delta u)- f(u)}{\Delta u} \cdot \frac{\Delta u}{\Delta x}\\ &= \lim\limits_{\Delta x \rightarr0}\frac{f(u+\Delta u)- f(u)}{\Delta u} \cdot \lim\limits_{\Delta x \rightarr0}\frac{\Delta u}{\Delta x}\\
             &= \frac{df}{du} \cdot \frac{du}{dx}\\
             \\
             &Here\ we\ denote\ \Delta u=u(x+\Delta x)-u(x)
\end{align}
$$


***1.2.2***


$$
\begin{align}
D(\frac{1}{x}) &=  \lim\limits_{\Delta x \rightarr0} \frac{\frac{1}{x+\Delta x}-\frac{1}{x}}{\Delta x} \\
&= \lim\limits_{\Delta x \rightarr0} \frac{\frac{-\Delta x}{x(x+\Delta x)}}{\Delta x} \\
&= \lim\limits_{\Delta x \rightarr0} \frac{-1}{x(x+\Delta x)}\\
&= -\frac{1}{x^2}
\end{align}
$$


***1.3.3***


$$
\begin{align}
sinh(x)   &= \frac{e^x-e^{-x}}{2}\\ 
&= \frac{1}{2}[\sum_{n=0}^{\infty}\frac{x^n}{n!}-\sum_{n=0}^{\infty}\frac{(-x)^n}{n!}]\\
&\text{Here we know that for even terms, they will cancel each other}\\ &\text{ while the odd terms exists as twice the origin value, so:} \\
&= \sum_{n=0}^{\infty} \frac{x^{2n+1}}{(2n+1)!} = x+\frac{x^3}{3!}+...  \\
&\text{This contains the odd terms only}

\end{align}
$$


Similarly,


$$
\begin{align}
cosh(x)   &= \frac{e^x+e^{-x}}{2}\\ 
&= \frac{1}{2}[\sum_{n=0}^{\infty}\frac{x^n}{n!}+\sum_{n=0}^{\infty}\frac{(-x)^n}{n!}]\\
&\text{This will contain the even terms only}\\ 
&= \sum_{n=0}^{\infty} \frac{x^{2n}}{(2n)!} = 1+\frac{x^2}{2!}+...  \\


\end{align}
$$


***1.6.7***

Consider the length of one side of the rectangular is x, the other should be $\frac{L-2x}{2}$

The area could be represented as 


$$
A(x) = x \cdot (\frac{L-2x}{2}) = -x^2+\frac{L}{2}x\\
\frac{dA}{dx}= -2x+\frac{L}{2}
$$


When x is less than $\frac{L}{4}$, the derivative is less than 0, while after x exceeds $\frac{L}{4}$, it becomes positive, so at x= $\frac{L}{4}$, as the derivative is zero, the area function would reach its maximum, with


$$
A_{max}=\frac{L^2}{16}
$$


And the case is that the wire rounds up a square.

***1.6.12***

Method 1


$$
\text{The point is restricts the relationship of y and x}\\
y = \sqrt{\frac{48-3x^2}{4}}\\
\frac{dy}{dx} \bigg{|}_{x=2}= -\frac{1}{2}
$$


Method 2


$$
\text{Direct operating each term with $D_x$}\\
D_x(3x^2+4y^2)= 0\\
6x+8y\frac{dy}{dx}=0\\
\frac{dy}{dx}=-\frac{3x}{4y}=-\frac{1}{2}
$$


***2.1.3***


$$
\begin{align}
F(n) &= \int_0^{\infty} x^ne^{-x}dx \\
     &= -x^ne^{-x} \bigg{|}_0^{\infty}+\int nx^{n-1}e^{-x}\\ 
     &= 0+ nF(n-1)\\
     &= nF(n-1)\\
\end{align}
$$


Since F(0) is the integration of $e^{-x}$ 


$$
\begin{align}
& F(0) = 1\\
& F(1) = 1 * F(0)\\
& F(2) = 2 * F(1)\\
& ...\\
&F(n)  = 1 * 2* 3 *...* n=n! 
\end{align}\\
\text{Here, 0! is defined as F(0) which is 1, or $\Gamma(1)$}
$$


***2.2.1***


$$
x = asin\theta\\
0<x<\pi/2\\
\text{leads to the range of $\theta$}\\
0<\theta<\pi/2a\\
dx = a cos\theta d\theta\\
\text{Plug this in the integral}\\
\int_{x_1}^{x_2} \frac{dx}{\sqrt{a^2-x^2}}=\int_{\theta_1}^{\theta_2} \frac{a cos\theta d\theta}{\sqrt{a^2(1-sin^2\theta)}}=\int_{\theta_1}^{\theta_2} \frac{a cos\theta d\theta}{acos\theta}=\theta_2-\theta_1=\frac{\pi}{2a}
$$


***2.2.8***


$$
use\ u=x^2 \\
du=2xdx\\
\begin{align}
I_1(a) &= \int_0^{\infty}e^{-ax^2}xdx\\
&=\int_0^{\infty}\frac{e^{-au}}{2}du\\
&=\frac{1}{2a}
\end{align}
$$

***2.2.9***


$$
I_3(a)\text{ can be evaluated from $I_1(a)$}\\
\begin{align}
\frac{dI_1}{da} &= \int_0^{\infty}\frac{\partial e^{-ax^2}x}{\partial a}dx\\
                &= \int_0^{\infty}- e^{-ax^2}x^3dx\\
                &= -I_3\\
                &= \frac{d}{da}(\frac{1}{2a})\\
                &= -\frac{1}{2a^2}\\
      I_3(a)    &= \frac{1}{2a^2}
\end{align}
$$


$$
I_4(a)\text{ can be evaluated from $I_2(a)$}\\
 \begin{align}
 \frac{dI_2}{da} &= \int_0^{\infty}\frac{\part e^{-ax^2}x^2}{\part a}dx\\                &= \int_0^{\infty}- e^{-ax^2}x^4dx\\                &= -I_4\\                &= \frac{d}{da}(\frac{1}{4a}\cdot\sqrt{\frac{\pi}{a}})\\                &= -\frac{3\sqrt{\pi}}{8}a^{-5/2}\\      I_4(a)    &= \frac{3\sqrt{\pi}}{8}a^{-5/2}
 \end{align}
$$


***3.1.5***

Define the distance function as the square root of $f(x,y)=x^2+y^2$

Apply Lagrange multiplier and we have


$$
\nabla (f-\lambda g) = 0\\
\nabla(x^2+y^2-\lambda x - 2\lambda y+4)=0\\
\text{Stationary point fits:}\\
2x-\lambda = 0\\
2y - 2\lambda = 0\\
x+2y=4\\
\text{So we have $\lambda=\frac{8}{5}$}\\
\text{Then, at point (4/5,8/5) is the point of shortest distance}
$$




***3.1.6***

Suppose one side is x length while the other is y.

The area is of the function $f(x,y)=x y$

With constrain function $g(x,y)=x+y=a/2$

Then we have 


$$
\nabla (f-\lambda g) = 0\\
\nabla(xy-\lambda x - \lambda y+a/2)=0\\
\text{Stationary point fits:}\\
y-\lambda = 0\\
x - \lambda = 0\\
x+y=a/2\\
\text{So we have $x=y=\lambda=\frac{a}{4}$}\\
\text{This indicates the square has largest area}
$$


***3.1.7***

Part.1

Written as a sum


$$
\begin{align}
 \ln(n!) &=\ln 1+\ln 2+\cdots +\ln n \\
         &\approx\int_1^nlnxdx\\
         &= (xlnx-x)\bigg{|}_1^n\\
         &=nlnn-n+1\\
         &\approx nlnn-n\\
         
 \end{align}
$$


Part.2

Constraints


$$
\sum_i n_i=N\\
\sum_in_i \epsilon_i=E
$$


Part.3 and 4


$$
\text{We have:}\\
\begin{align}
\mathcal F(n_1,n_2,...) &= lnW-\alpha (\sum_in_i-N)-\beta(\sum_in_i \epsilon_i-E)\\
&=lnN!-\sum_ilnn_i! -\alpha (\sum_in_i-N)-\beta(\sum_in_i \epsilon_i-E)\\
&=NlnN-N-\sum_i(n_ilnn_i-n_i)-\alpha (\sum_in_i-N)-\beta(\sum_in_i \epsilon_i-E)\\
\end{align}
$$


$$
\nabla \mathcal F =0\\
\text{For any i, we have}\\

 lnn_i +1-1+\alpha+\beta\epsilon_i=0\\
 n_i=exp(-\alpha-\beta\epsilon_i)\\
 S_{max}=lnW_{max}=ln\frac{N!}{\prod_iexp(-\alpha-\beta\epsilon_i)!}
$$




***3.2.4***


$$
\begin{align}
V(r)&=\int\int\int1*r^2sin\theta d\phi drd\theta\\
&=\int_0^{2\pi} d\phi\int_0^{\pi}sin\theta d\theta\int_0^rr^2dr\\
&=2\pi *2*r^3/3\\
&=4\pi r^3/3
\end{align}
$$


***5.2.5***

Consider the polynomial have a set of roots Z, then:


$$
\sum_i a_i Z^i = 0\\
\text{Taking complex conjugate of two sides}\\
\sum_i a_i \bar{Z}^i = \sum_{2j}a_{2j}\bar{Z}^{2j} +\sum_{2j+1}a_{2j+1}\bar{Z}^{2j+1}\\
\bar{Z}^{2j}=(a-bi)^{2j}=\overline{(a+bi)^{2j}}=\overline {Z^{2j}}\\
\bar{Z}^{2j+1}=(a-bi)^{2j+1}=\overline{(a+bi)^{2j+1}}=\overline {Z^{2j+1}}\\
\sum_i a_i \bar{Z}^i = \sum_i a_i \overline{Z^i}=0
$$


 As a consequent, if one polynomial has a set of complex roots Z, the conjugate of Z are also roots of the equation. So the roots are real, or in complex conjugate pairs

***5.2.6***



#### The first two

The absolute value of a complex number is defined as:


$$
Part1\\
|z|=\sqrt{\bar zz}=\sqrt{(a-bi)(a+bi)}=\sqrt{a^2+b^2}\\
|z|=\sqrt{a^2+b^2}\ge |a|=|Re(z)|\\
|z|=\sqrt{a^2+b^2}\ge |b|=|Im(z)|\\
Part2\\
|z_1+z_2|^2=(\bar{z_1}+\bar{z_2})(z_1+z_2)=(a_1+a_2-b_1i-b_2i)(a_1+a_2+b_1i+b_2i)\\
=a_1^2+b_1^2+a_2^2+b_2^2+a_1a_2+b_1b_2\\
=|z_1|^2+|z_2|^2+2Re(z_1\bar{z_2})\\
Part3\\
|z_1+z_2|=\sqrt{|z_1|^2+|z_2|^2+2Re(z_1\bar{z_2})}\\
\text{As $Re(z_1\bar{z_2})$ is less than $|z_1||z_2|$, so:}\\
|z_1+z_2|^2\le (|z_1|+|z_2|)^2\\
|z_1+z_2|\le |z_1|+|z_2|\\
Part4\\
|z_1z_2|=|a_1a_2-b_1b_2+(a_1b_2+a_2b_1)i|=(a_1a_2-b_1b_2)^2+(a_1b_2+a_2b_1)^2\\
|z_1||z_2|=(a_1^2+b_1^2)(a_2^2+b_2^2)\\
$$


We can tell that the first term and second term are equal as in the first term, the $a_1a_2b_1b_2$ term actually vanished, leaving all the terms being simply the second order term of combination of the four principle values: $a_1,a_2,b_1,b_2$. The second term also only contains the combination of the four principle values. So we can say the first and second are equal.

***5.3.2***


Part 1 


$$
z_1=\frac{1+i}{\sqrt2}=\frac{\sqrt2}{2}+\frac{\sqrt2}{2}i\\
r = 1;tan\theta=1;\theta=\pi/4+2n\pi\\
\overline{z_1} = \frac{\sqrt2}{2}-\frac{\sqrt2}{2}i\\
|z_1|=\sqrt{1/2+1/2} = 1\\

z_2=\sqrt3-i\\
r = 2;\theta=-\pi/6+2n\pi\\
\overline{z_2} = \sqrt3+i\\
|z_2|=\sqrt{3+1} = 2\\
z_1z_2=\frac{\sqrt3+1+(\sqrt3-1)i}{\sqrt2}\\
z_1/z_2=\frac{\sqrt3-1+(\sqrt3+1)i}{4\sqrt2}\\
\overline{z_1/z_2}=\frac{\sqrt3-1-(\sqrt3+1)i}{4\sqrt2}
$$


Part 2


$$
z_1=\frac{3+4i}{3-4i}=\frac{-7+24i}{25}\\
r = 1;tan\theta=-24/7;\theta=arctan(-24/7)+2n\pi\\
\overline{z_1} = \frac{-7-24i}{25}\\
|z_1|=\frac{\sqrt{24^2+7^2}}{25} = 1\\
z_2=[\frac{1+2i}{1-3i}]^2=(\frac{-1+i}{2})^2=-i/2\\
r = 1/2;\theta=-\pi/2+2n\pi\\
\overline{z_2} = i/2\\
|z_2|=1/2\\
z_1z_2=\frac{-7i-24}{50}\\
z_1/z_2=\frac{48+14i}{25}\\
\overline{z_1/z_2}=\frac{48-14i}{25}
$$


***5.3.4***


$$
1.\ \ |e^{i\theta}|^2=e^{i\theta}*e^{-i\theta}=e^{0}=1=sin^2\theta+cos^2\theta\\
2.\ \ e^{2i\theta}=cos2\theta+isin2\theta=e^{i\theta}*e^{i\theta}=(cos\theta+isin\theta)(cos\theta+isin\theta)\\
=cos^2\theta - sin^2 +2i(sin\theta cos\theta)\\
For\ imaginary\ part: isin2\theta=2i(sin\theta cos\theta)\\
For\ real\ part: cos2\theta=cos^2\theta - sin^2 \theta
$$
