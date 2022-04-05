# ITS Regression Tutorial Concern

### Step 1: Is an interrupted time series design appropriate?
**The intervention**: The intervention does not need to be introduced overnight but the period od implementation should be well defined.

**The outcome**: prefer short-term outcomes expected to change either *relatively quickly* after an intervention is implemented or after *a clearly defined lag*. not prefer timing between intervention and outcome is much less clear and can be highly variable(should consider intermediate outcome here).

### Step 2: Proposing the impact model
whether the change will be:
* trend
* level 
* both

the change follow the intervention immediately or there will be a lag period before any effect is expected.

counting model: Poisson model, quasi-Poisson model(allow mean not equal to variance, i.e. over-dispersion)

**Notice**: 
* prior decision based on *existing literature**and knowledge of the intervention and the mechanism by which it is expected to act on the outcome.
* Relying on the outcome data to select the best impact model will increase the likelihood of an effect being detected due to random fluctuation or chance.

### Step 3: Descriptive Analysis, familiarize data
Looking at the pre-intervention trend can give an indication:
* how stable the trend is over time ?
* whether a linear model is likely to be appropriate ?
* whether there appears to be a seasonal trend ?


### Step 4: Regression Analysis
model: $Y_t = \beta_0 + \beta_1 T + \beta_2 X_t + \beta_3 TX_t$

use ANOVA to show whether it is necessary to add a new effect to our model.

**offset variable** is a special technique for Poison regression to match count and ratio.

**Notice**: the population may change(though this is not essential if the population is relatively stable over time)


### Step 5: Addressing methodological issues
**autocorrelation**: examine the plot of residuals &the partial autocorrelation function. conduct Godfrey test for normally distributed data. Then use ARIMA or Prais regression.

**seasonality**: 

seasonality causes problems
* if there is an uneven distribution of monthes before and after the intervention, this could bias the results, especially in the analysis of short series.
* outcomes tend to be more similar to those in neighbouring months with the same time of year, leading to auto-correlation & over-dispersion.




