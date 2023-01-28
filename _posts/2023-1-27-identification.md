---
layout: post
title: Identification
date: 2023-1-27 11:12:00-0400
description: Understanding identification
---

I review one of the most important notions in econometrics, namely the notion of identification, following the seminal paper [Hurwicz (1962)](https://www.sciencedirect.com/science/article/abs/pii/S0049237X09705907){:target="\_blank"}. In what follows, I begin with a general definition of identification.

<div class="publications">
  <h2 class="topic">General Definition</h2>
</div>

In the context of econometrics, identifiability of the unknown quantity (e.g. parameters or functions of parameters) of our interest serves as the *necessary* condition for the existence of a consistent estimator for that quantity. The condition is only necessary because the estimator may not converge in a probabilistic sense to the true value of the quantity due, for example, to the existence of excessive dependency in the data. That is, the law of large numbers could fail even when the unknown quantity can be identified. That is, if one could not logically deduce the value of the unknown quantity from a presample analysis, then the usual argument for proving the consistency of an estimator would fail, let alone the derivation of its asymptotic distribution.

To fix idea, we denote by $$P_X$$ the true distribution of the observed data, which is the probability measure on the state space of random element $$X$$. Also, let
\begin{gather}
  \mathcal{P}=\{P_{\theta}:\theta\in\Theta\}\label{model}
\end{gather}
be our model for the distribution of the same data, which is indexed by the parameter $$\theta$$. The model $$\mathcal{P}$$ is of particular interest because we are intended to interpret it as a *structural* model for the distribution of the observed data that helps us not only summarize various kinds of statistics, but also understand the underlying mechanism that generates the data. We will introduce the notion of structural model in the next section. Also, there will be no need to introduce such a model if our interest lies only in the statistical characterization of the observed data. $$P_X$$ alone would suffice for that purpose.


