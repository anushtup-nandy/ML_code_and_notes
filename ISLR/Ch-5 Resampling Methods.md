2022/08/09  (22:40)
Tag: [[MOC_study]]  #study/islr #ml 

# Ch-5 Resampling Methods
Resampling methods is basicallt repeatedly drawing samples from a training set and refitting a model of interest oneach sample in order to obtain additional information.

Such an approach may allow us to obtain information that would not be available from fitting the model only once using the original training sample.

2 methods are used most commonly:
- Cross-validation
- Bootstrap

## 5.1 Cross-Validation:
We hve 2 major forms of error rates:
- Test error rate
- training error rate

Test error rates can be determined iff we have a significant test set available to us. This is usually not the case. So we prefer to use the following methods:
- Mathematical adjustments to the training error to make the test error [[ch-6 Linear Model Selection and Regularization]]
- Holding out on a subset of the trainnig observations from the fitting process.

- [[5.1.1 THE VALIDATION SET APPROACH]]
- [[5.1.2 LEAVE-ONE-OUT CROSS-VALIDATION]]
- [[5.1.3 K-FOLD CROSS-VALIDATION]]
- [[5.1.4 BIAS-VARIANCE TRADE-OFF FOR K-FOLD CROSS VALIDATION]]
- [[5.1.5 CROSS-VALIDATION ON CLASSIFICATION PROBLEMS]]

## 5.2 The Bootstrap:
Its used to qantify the uncertainity associated with a given estimator or statistical learning method.
- An example can be that it can be used to estimate standard errors of the coefficients from a linear regression fit.

***Explaination:***
We have an amount Z of something, and we want to divide it into $\alpha$ (fraction) that goes innto beccoming X and $1-\alpha$ that goes into Y. The X and Y are variable, and hence we want to choose $\alpha$ to *minimize* the total risk/variance. *Basically we want to minimize our variance* $Var(\alpha X + (1-\alpha)Y)$.
$$
{\alpha}=\frac{{\sigma_Y^2}-{\sigma_{XY}}}{{\sigma_X^2}+{\sigma_Y^2}-2{\sigma_{XY}}}----(5.5)
$$
But in reality, $\sigma$ are all unknown, so we need to estimate those too!--> we do this using the dataset (training set maybe). So all the $\sigma\text{ and, }\alpha$ are actually $\hat{\sigma},\hat{\alpha}$. 
We can estimate the accuracy of the $\alpha$ using it's mean, standard deviation (go through [[3.1.2 ASSESSING THE ACCURACY OF COEFFICIENT ESTIMATES]])
 
The approach we showcased above to use the mean and standard deviation to assess the accuracy of $\alpha$ is not really possible because in real world, we cannot really have more independent samples. Rather we need to use the *original dataset*.

==BOOTSTRAP== allows us to do that, we basically repeatedly sample the original dataset.

- [[5.2.1 WHAT WE DO IN BOOTSTRAP]]
---
# References
[An Introduction To Statistical Learning With Applications In R (Second Edition) (Gareth James, Daniela Witten, Trevor Hastie etc.) (z-lib.org).pdf](file:///C:/Users/Anushtup%20Nandy/OneDrive/Documents/BITS/important%20stuff/EXTRA%20BOOKS/Machine%20Learning/An%20Introduction%20To%20Statistical%20Learning%20With%20Applications%20In%20R%20(Second%20Edition)%20(Gareth%20James,%20Daniela%20Witten,%20Trevor%20Hastie%20etc.)%20(z-lib.org).pdf)