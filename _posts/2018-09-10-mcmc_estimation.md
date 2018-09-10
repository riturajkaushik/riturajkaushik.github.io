---
layout: post
title: Approximation of Bayesian posterior with Markov Chain Monte Carlo 
tags: [statistics, tutorial, Bayesian]
---
Bayes' rule is amazing. Ever since I came across Bayes' rule in statistics I have been in love with this simple yet elegant formula in statistics which has application in wide area of research such as AI, health care, economics and what else. Although it looks very simple, in many cases it becomes very complicated to compute it in closed form. This complication arises due to the denominator of the formula which is the marginal probability distribution of the observations. This term is sometimes very hard (or virtually impossible) to compute analytically. To bypass this complexity, several approaches has been proposed to approximate the Bayesian posterior such as Variational inference, Markov Chain Monte Carlo (MCMC) etc . In this informal tutorial we are going to see how we can approximate the Bayes rule using MCMC.

Before diving into the algorithm, just for revision let's first see the Bayes' rule and what it actually means.

$$ 
P(w|D) = \frac{P(D|w)P(w)}{\int {P(D|w_i)dw_i}}
$$

Post in progress.............

