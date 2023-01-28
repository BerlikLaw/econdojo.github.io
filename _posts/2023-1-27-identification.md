---
layout: post
title: Identification
date: 2023-1-27 11:12:00-0400
description: an example of a blog post with some math
---

I review one of the most important notions in econometrics, namely the notion of identification, following the seminal paper Hurwicz (1962). In what follows, I begin with a general definition of identification.

## General Definition

In the context of econometrics, identifiability of the unknown quantity (e.g. parameters or functions of parameters) of our interest serves as the *necessary* condition for the existence of a consistent estimator for that quantity. The condition is only necessary because the estimator may not converge in a probabilistic sense to the true value of the quantity due, for example, to the existence of excessive dependency in the data. That is, the law of large numbers could fail even when the unknown quantity can be identified. That is, if one could not logically deduce the value of the unknown quantity from a presample analysis, then the usual argument for proving the consistency of an estimator would fail, let alone the derivation of its asymptotic distribution.

This theme supports rendering beautiful math in inline and display modes using [MathJax 3](https://www.mathjax.org/){:target="\_blank"} engine. You just need to surround your math expression with `$$`, like `$$ E = mc^2 $$`. If you leave it inside a paragraph, it will produce an inline expression, just like $$ E = mc^2 $$.

To use display mode, again surround your expression with `$$` and place it as a separate paragraph. Here is an example:

$$
\sum_{k=1}^\infty |\langle x, e_k \rangle|^2 \leq \|x\|^2
$$

You can also use `\begin{equation}...\end{equation}` instead of `$$` for display mode math.
MathJax will automatically number equations:

\begin{equation}
\label{eq:caushy-shwarz}
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
\end{equation}

and by adding `\label{...}` inside the equation environment, we can now refer to the equation using `\eqref`.

Note that MathJax 3 is [a major re-write of MathJax](https://docs.mathjax.org/en/latest/upgrading/whats-new-3.0.html){:target="\_blank"} that brought a significant improvement to the loading and rendering speed, which is now [on par with KaTeX](http://www.intmath.com/cg5/katex-mathjax-comparison.php){:target="\_blank"}.
