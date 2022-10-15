2022/07/13  (10:26)
Tag:  #ml  #study/islr  [[MOC_study]]

# Ch-4 Classification
Predicting a qualitative response is called **CLASSIFYING**. Since it involves assigning the observation to a category, or class.
Some popular categories:
- Logistic regression
- linear discriminant analysis
- quadratic discriminant analysis 
- naive bayes
- KNN
>[!important]
>remember that here, X= predictors, Y=response (variable)

PROBLEM STATEMENT:
>[!question]
>In this chapter, we will illustrate the concept of classification using the simulated Default data set. We are interested in predicting whether an individual will default on his or her credit card payment, on the basis of annual income and monthly credit card balance.

![[Pasted image 20220713112611.png]]
## 4.1 Logistic Regression:
Logistic regression models the probability that Y belongs to aparticular category, rather than modelling it directly!
$$
Pr(default=yes| balance)
$$
==CONTENTS==
- [[4.1.1 THE LOGISTIC MODEL]]
- [[4.1.2 ESTIMATING THE REGRESSION COEFFICIENTS]]
- [[4.1.3 MAKING PREDICTIONS]]
- [[4.1.4 MULTIPLE LOGISTIC REGRESSION]]
- [[4.1.5 MULTINOMIAL LOGISTIC REGRESSION]]

## 4.2 Generative Models for Classification:
Logistic regression involves directly modeling Pr(Y = k|X = x) using the logistic function, given by (4.7) for the case of two response classes.
>we model the conditional distribution of the response Y , given the predictor(s) X

In this new approach,<u> we model the distribution of the predictors X separately in each of the response classes (i.e. for each value of Y ). We then use Bayes’ theorem to flip these around into estimates for Pr(Y = k|X = x).</u>

$$
p_k(x)=Pr(Y=k|X=x)= \frac{\pi_{k} * f_k}{\sum_{l=1}^{K}\pi_lf_l(x)}----(4.14)
$$
This is the [[Bayes theorem]], for our new model where:

$\pi_k$: is the prior probability of the randomly chosen observation to occur from the kth class.
 and $f_k=Pr(X|Y=k)$

*Eqn (4.14)* tells us that we can compute the estimates of $\pi_k$ and $f_k$ directly into the equation rather than calculating the probability directly as asked by *LOGISTIC regression* earlier sections.
Reasons:
- calculating $\pi_k$ is easy: we simply compute the fraction of the training observations that belong to the kth class
- Bayesian Classifier has certain benefits as specified in [[2.2.4 THE BAYES CLASSIFIER]]

==CONTENTS==
- [[4.2.1 LINEAR DISCRIMINANT ANALYSIS FOR p=1]]
- [[4.2.2 LINEAR DISCRIMINANT ANALYSIS FOR p greater than 1]]
- [[4.2.3 QUADRATIC DICRIMINANT ANALYSIS]]
- [[4.2.4 NAIVE BAYES]]

## 4.3 Comparison of Classification Models:
- [[4.3.1 ANALYTICAL COMPARISON]]
- [[4.3.2 EMPIRICAL COMPARISON]]

## 4.4 Generalized linear Models:
- [[Ch-3 Linear Regression]]
- [[4.4.2 POISSON REGRESSION]]


---
# References
[An Introduction To Statistical Learning With Applications In R (Second Edition) (Gareth James, Daniela Witten, Trevor Hastie etc.) (z-lib.org).pdf](file:///C:/Users/Anushtup%20Nandy/OneDrive/Documents/BITS/important%20stuff/EXTRA%20BOOKS/Machine%20Learning/An%20Introduction%20To%20Statistical%20Learning%20With%20Applications%20In%20R%20(Second%20Edition)%20(Gareth%20James,%20Daniela%20Witten,%20Trevor%20Hastie%20etc.)%20(z-lib.org).pdf)