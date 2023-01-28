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

We assume that the model $$\mathcal{P}$$ is *complete* in the following sense: there exists some $$\theta\in\Theta$$ such that $$P_{\theta}=P_X$$. Cautions are needed here because it is possible that there exists another $$\theta^*\in\Theta$$ such that $$\theta^*\neq\theta$$ and $$P_{\theta^*}=P_X$$ if, for example, the observed data is not sufficiently informative. Therefore, the only legitimate claim we can make from the knowledge of $$P_X$$ alone is that
\begin{gather}
  \theta\in\Theta_0(P_X):=\{\theta\in\Theta:P_{\theta}=P_X\}
\end{gather}
where $$\Theta_0(P_X)$$ is referred to as the identified set. We say that $$\theta$$ is *identified* if $$\Theta_0(P_X)$$ is a singleton. Identification in our general discussion so far is really a global concept. [Rothenberg (1971)](https://www.jstor.org/stable/1913267){:target="\_blank"} showed that the necessary and sufficient condition for *local* identification is the nonsingularity of the Fisher information matrix. [Iskrev (2008)](https://www.sciencedirect.com/science/article/abs/pii/S0165176507003898){:target="\_blank"} shows how the information matrix of linearized DSGE models can be evaluated analytically, which can be used to check the local identifiability in DSGE models. Thus, the natural question is that under what restrictions on $$\Theta_0(P_X)$$ can the identification of $$\theta$$ be achieved. We will explore these restrictions in the next section.

As an example, consider the following linear regression model
\begin{gather}
  Y=X'\beta+\epsilon\label{regression}
\end{gather}
where $$X$$ is a $$k\times 1$$ vector and $$\theta=(P_X,\beta,P_{\epsilon|X})$$. A standard set of restrictions on $$\Theta_0(P)$$ under which $$\theta$$ can be identified are the following:

* A1. $$\mathbb{E}_{P_{\theta}}[\epsilon X]=0$$.
* A2. $$\mathbb{E}_{P_{\theta}}[XX']$$ is nonsingular.

Note that restriction (A1) is usually referred to as the orthogonality condition in the traditional framework of classical regression models. [Park (2010)](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=4c5678380faf48f4df3155548fda54a0d5dcbccc){:target="\_blank"} proposes a more general class of regression models, called the *martingale regression* since it is identified by the condition that the error process is a martingale. It allows for the presence of arbitrary time-varying and stochastic volatilities that are often quite persistent and strongly endogenous.

<div class="publications">
  <h2 class="topic">A Priori Information and Prediction</h2>
</div>

Our general definition of identification has hid two essential points of identification: both the degree of and the need for identification are *relative* notions. First, we describe the identification issue one might encounter even in the simplest case. To fix idea, let $$x=[x_1,x_2,\ldots,x_n]'$$ denote the state of a configuration that takes the form of simultaneous equations system given by
\begin{gather}
  f_i(x)=0,\qquad i=1,2,\ldots,m\label{configuration}
\end{gather}
Hurwicz refers to $$f_i$$ as the *behavior pattern* of the $$i$$-th component in the configuration. In the context of probabilistic models, the zero's on the right hand side of \eqref{configuration} should be replaced by stochastic disturbance terms so that $$f_i$$'s take the form of, for example, first-order conditions derived from agents' optimizing behavior in a dynamic stochastic general equilibrium (DSGE) model, or the classical linear regression model given in the previous section.

In what follows, we will focus only on the linear deterministic behavior pattern which, in matrix notation, can be compactly written as
\begin{gather}
  Ax-b=0\label{linear}
\end{gather}
where the behavior pattern is now completely determined by the $$m\times n$$ matrix $$A$$ and the $$m\times 1$$ vector $$b$$. Note that \eqref{linear} imposes a restriction on the possible values that $$x$$ can take under the particular configuration specified by $$(A,b)$$. Let $$\mathcal{H}$$ be the state space of $$x$$ that is spanned by the true values of $$A$$ and $$b$$. Following the language and notation established in the previous section, we can take $$P_X$$ to be $$\mathcal{H}$$ here because the knowledge of $$P_X$$ boils down to that of $$\mathcal{H}$$ in a deterministic setting. Therefore, the identified set of $$(A,b)$$ can be written as
\begin{gather}
  \Theta_0(\mathcal{H})=\{(A,b):Ax-b=0,\ \ \ \forall\ x\in\mathcal{H}\}\label{set}
\end{gather}
and the completeness assumption of our model $$\mathcal{P}$$ amounts to requiring that $$\Theta_0(\mathcal{H})$$ is a nonempty set. Cautions are needed again because it is straightforward to see that for any $$(A,b)\in\Theta_0(\mathcal{H})$$ and any $$m\times m$$ invertible matrix $$P$$, the combination
\begin{gather}
  C=PA\ \ \ \text{and}\ \ \ d=Pb\label{transform}
\end{gather}
is also contained in $$\Theta_0(\mathcal{H})$$. Since these two behavior patterns both span the state space $$\mathcal{H}$$, we say that $$(A,b)$$ and $$(C,d)$$ are *observationally equivalent* with data. Therefore, the knowledge of $$\mathcal{H}$$ alone fails to single out the true behavior pattern specified by a particular combination of $$A$$ and $$b$$.

The above discussion still remains unclear about how much identification one is able to achieve and what purposes is identification intended for. Indeed, both the degree of and the need for identification are only defined as relative notions that are intimately connected.

1. **Identification is no free lunch.** Because the knowledge of $$\mathcal{H}$$ alone does not suffice here, we may look for additional restrictions that are not contained in $$\mathcal{H}$$ for the purpose of identification. These extra restrictions are usually called *a priori* information, which comes from our economic theory or empirical experience, etc., and can be conveniently formulated in the Bayesian framework by imposing appropriate prior probability measures on $$(A,b)$$. Thus, the imposition of *a priori* information helps us rule out all those transformation matrices $$P$$ in \eqref{transform} that are incompatible with the restrictions provided by the *a priori* information. To see this more clearly, consider the following two extreme cases: