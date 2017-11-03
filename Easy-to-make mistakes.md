We have a lot of n, n-1, n-2 in regression process
This md file aims to clear it up.

Syy = sum (y_i - y_bar)^2

Sy^2 = Syy/**n-1**

Similarly, Sx^2 = Sxx/**n-1**

These two hold because they are the estimation of variance of X_i's and Y_i's. AND ***they have no relationship with the regression model***(They just hold in mathematical statistics).

SSE = sum (y_i - y_i_hat)^2

residual standard error^2 = sigma_s^2 = s^2 (just different notations) = SSE/**n-2**. This is ***in the model***, **n-2** is caused by the regression process. Because we currently have two parameters estimated, therefore we lose two degrees of freedom.

This number(*sigma_s^2*) is also our estimation of the **variance of errors**, sigma^2, which is also ***in the model***. And it's also the variance of y_i (when x_i is given and fixed), under the assumption of constant variance.
