# Residual Plot

## residual v.s. standardized residual


When points of high leverage exist, instead of looking at residual plots, it is generally more informative to
look at plots of standardized residuals since plots of the residuals will have nonconstant variance even if the
errors have constant variance. (When points of high leverage do not exist, there is generally little difference
in the patterns seen in plots of residuals when compared with those in plots of standardized residuals.) The
other advantage of standardized residuals is that they immediately tell us how many estimated standard
deviations any point is away from the fitted regression model.


**From Sheather's textbook:**
A number of authors (e.g., Cook and Weisberg, 1999b , p. 350) recommend that
an effective plot to diagnose nonconstant error variance is a plot of
|Residuals|^0.5 against x
or
| Standardized Residuals|^0.5 against x.

The power 0.5 is used to reduce skewness in the absolute values.



## From the two cited sources, we can have some conclusions:
Residual plot and standardized plot are not so different in their use. However, it may be better to use residaul plot to check **independece assumption**, that is, whether there is a discernible pattern; and use standardized residual plot to check **constatn variance assumption**.

### Any violation of these assumptions make the model invalid.
The so-called *model validity check* is just to check whether the assumptions are met.

And the assumptions all come from the model: ***Yi = beta0 + beta1 * Xi + epsilon_i***
In SLR case, the assumptions are:
1. *epsilon_i's* are independent    **checked by residual plot**
2. *epsilon_i's* have a common variance  **usually checked by standardized residual plot, but residual plot is also fine(as long as the points' leverage are not large**
3. *epsilon|X* are normally distributed

Remark: In conclusion, every epsilon_i is a random variable, it's mean is 0 and variance is assumed to be sigma^2, its distribution is assumed to be normal. And all the epsilon_i's are independent(i.i.d. actually)

Remark2: In the model, X is given. Therefore, Y_i is also a random variable and has the same variance as epsilon_i. All the Y_i's are independent but not identically distributed (because they have different means).



**Query 1.** Why do we plot the residuals ej = Yj - Yj against the Yj and not against
the Yj , for the usual linear model?

**Ans.** Because the e's and the Y's are usually correlated but the e's and the Y's
are not. One way to see this is to think of plots of the ej as ordinate against (i) the Yj
and (ii) the Yj , and find the slope of a least squares lines through the points. For (i)
it will be 1 - R2; for (ii) O. This means that, unless R2 = 1, there will always be a
slope of 1 - R^2 in the ej versus Yj plot, even if there is nothing wrong. However, a
slope in the ei versus Yi plot indicates that something is wrong.
