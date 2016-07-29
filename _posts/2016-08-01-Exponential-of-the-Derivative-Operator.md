---
layout: post
title:  Exponential of the Derivative Operator  
date:   2015-05-02 09:00:00
tags: math
---

The Taylor series definition of $$e^x$$ allows the function to be defined for domains beyond $$\Bb R$$. For example, extending the domain of the exponential function to $$\Bb C$$ results in Euler's formula.

$$
\begin{align*}
\exp{\begin{bmatrix}0&0&0&0&0&0\\1&0&0&0&0&0\\0&2&0&0&0&0\\0&0&3&0&0&0\\0&0&0&4&0&0\\0&0&0&0&5&0\end{bmatrix}} &= \begin{bmatrix}1&0&0&0&0&0\\1&1&0&0&0&0\\1&2&1&0&0&0\\1&3&3&1&0&0\\1&4&6&4&1&0\\1&5&10&10&5&1\end{bmatrix}
\end{align*}
$$

##A Summation Operator

The operator $$e^D-I$$ returns the difference between two consecutive terms in a sequence $$S_n$$. For example, for the sequence $$A_n=n^2$$, it yields $$2n+1$$. The inverse of this operator is a summation operator. (In the previous example, the sum of the first $$n$$ odd numbers is the $$n$$th perfect square.) Therefore, we wish to evaluate $$(e^D-I)^{-1}$$. To do so, we will employ the following Taylor series: 

$$\frac{t}{e^t-1} = \sum_{n=1}^{\infty} B_n \frac{t^n}{n!}$$

Here, $$B_n$$ is the $$n$$th Bernoulli number. We divide by $$t$$ and evaluate the resulting series at $$D$$ to get

$$(e^D-I)^{-1} = D^{-1} - \frac{1}{2}I + \frac{1}{12}D - \frac{1}{720}D^3 + \frac{1}{30240}D^5 + \ldots$$

Let's try this formula out on the sequence $$A_n$$.

$$
\begin{align*}
    (e^D-I)^{-1} A &= D^{-1} A - \frac{1}{2}I A + \frac{1}{12}D A + \ldots\\
    &=\frac{n^3}{3} - \frac{n^2}{2} + \frac{n}{6}
\end{align*}
$$

Luckily, the terms eventually vanish. Note: this formula is the sum of the first $$n-1$$ square numbers. To get the familiar formula, apply $$e^D$$ to get

$$\sum_{i=1}^{n} i^2 = \frac{n^3}{3} + \frac{n^2}{2} + \frac{n}{6}$$
