# Errata for *Using R for Introductory Statistics*, second edition.


* Thanks to: William Kitto, Antelope Valley College for finding errors in the Solutions Manual (9.2 and 9.4).
* Thanks to  Demetrios Papanastassiou for finding several issues in chapter 3.


## Chapter 3

* p121: the explanation of $y_i = e^{error_i} \cdot e^{b_0}x_i^{b_1}$ is a confusing. Better wording would be:

This is roughly saying that the mean response in the brain is a multiple, ($e^2.15$), of the body 
weight raised to $0.752$ and the errors are multiplicative, not additive. (Thanks to  Demetrios Papanastassiou.)

* p122. The line `fm <- weight/2.2 ~ I(height*2.54/100^2)` is missing a parentheses so that the squaring is of the entire expression:

```
fm <- weight/2.2 ~ I( (height*2.54/100)^2 )
```

This will change the regression values to

```
Call:
lm(formula = fm, data = kid.weights, subset = idx)

Coefficients:
             (Intercept)  I((height * 2.54/100)^2)  
                  15.571                     4.239  
```

The slope of 4 is more reasonable. (Thanks to  Demetrios Papanastassiou.)


* p125: The formulas on robust regression should read $\sum(y_i + (b_0+b-1x_i))^2$ and $\sum \rho(y_i + (b_0+b-1x_i))$.  (Thanks to  Demetrios Papanastassiou.)




