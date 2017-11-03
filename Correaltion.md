In **R**, there is a cor.test() function, which can calculate a t-statisticf for the correlation coefficient of X and Y:

Pearson's product moment correlation coefficient cor(x, y) follows a t distribution with length(x)-2 degrees of freedom if the samples follow independent normal distributions.

![t-statistics](https://wikimedia.org/api/rest_v1/media/math/render/svg/e0810a6f2000a63525adbbd2f5e79db1f554057e)


## More on the correlation coefficient
By definition, r = Sxy/sqrt(Sxx * Syy); note that beta_1_hat = Sxy/Sxx, we have:

**beta_1_hat = Sy/Sx * r**

This means that beat_1_hat is a **scaled version of r**, scaled by the ratio of the "spread" of Y_i divided by the spread of X_i.

N.B.: Scale changes in the data will affect beta_1_hat but not r.
