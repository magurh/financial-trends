# The Enscombe Quartet

The Enscombe quartet comprises four data sets that have nearly identical simple descriptive statistics, and yet, very different distributions.

<p align="center">
  <img src="https://github.com/magurh/Enscombe-quartet/assets/122356566/07d2850c-fc5a-4cb2-94f1-1007aaae1b61">
</p>

In particular, running a linear regression on the four datasets gives the same $\hat{\alpha}$ and $\hat{\beta}$ estimates, up to 2 and 3 decimal places. 
However, this is only a good fit for the first model; in the second case, the model is not linear, while for the third set the regression is offset by one outlier, which exerts enough influence to lower the correlation coefficient. 
Finally, the last graph shows an example when a high-leverage point is enough to produce a high correlation coefficient, even though the other data points do not indicate any relationship between the variables.

In the attached jupyter notebook we look into more details at the statistics of these models and see how the models can be remedied.
