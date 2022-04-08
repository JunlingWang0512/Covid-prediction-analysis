# Interrupted ARIMA

## Background
ITS: evaluate the impact of large-scale health intervention

Methods: 
* segment regression(trends, types of impact)
* ARIMA(seasonality, autocorrelation)

ARIMA modelling is useful when other approaches are not suitable.

observational studies relyingb on a small number of measurememnts pre- and post-intervention are prone to bias as they do not account for pre-existing underlying short- and long-term trends.

ITS is considered one of the best designs for establishing causality when RCT are feasible.

## Methods
topics:
* select the shape of the impact
* the model selection process
* transfer functions
* checking model fit
* interpretation of findings

### time series properties

#### non-stationarity
ARIMA requirement: ts *stationary*
WHAT? constant mean; constant variance; constant covariance depending only on time interval.
sources of non-stationarity
* changing variance : apply a log transformation
* increasing or decreasing trend: take difference $Y_t - Y_{t+1}$

#### Autocorrelation
ACF: correlation between each observation and previous values at various lags.
PACF: correlation between an observation and past values that is not explained by correlations at lower other lags.

#### Seasonality
seasonality is usually dealt with by taking the **seasonal difference**.

**Note** : when taking the seasonal difference for monthly data, the first 12 observations are lost, since the seasonal difference cannot be calculated for those observations. In general, more time points are needed.

### Components of ARIMA models
assumptions: errors are normally distributed.

Available Situation:
* any continuous outcome
* large count that are not bounded by zero
Unavailable Situation: small counrts following Poisson distribution

ARIMA notation: $(p,d,q)$
* $p$ the order of the AR part of the model
* $d$ the degree of non-seasonal differencing
* $q$ the order of the MA part of the model

seasonal ARIMA: $(p,d,q)\times (P,D,Q)_S$
* $D$ the degree of seasonal differencing
* $P$, $Q$ AR, MA terms for seasonal component

### Evaluating interventions using ARIMA
three main types of intervention effect
* step change
* pulse
* ramp
The potential shape of the intervention impact should be hypothesised a prior.

If there are multiple potential models,  use AIC BIC to select the most appropriate combination of impact variables.

Lag: 
* prespecify a reasonable period of time in which it would be expected for the impact to be observed based on content knowledge or previous research to avoid spurious associations.
* The most appropriate delay within this range of options can be determined at the modelling stage.

**Notice**: Unlike segmented regression, including time or seasonal dummy variables in ARIMA model is not necessary, as ARIMA eliminate trends and seasonality through differencing.</br>
**defect**: However, then pre- and post- intervention trends cannot estimated from the model.</br>
**Solution**: include time as covariate and use ARMA models(for autocorrelation) to estimate the intervention trend.

### Fitting an ARIMA model
aim: select the most **parsimonious** model that has good fit and adequately controls for autocorrelation and seasonality.
![](pics/ARIMAflowchart.webp)
Box-Jenkins method
implement:
* automated algorithm
* manual process

##### Plot data to understand patterns
how to deal with outliers depend on their cause and influence on the model.

##### Transform data to stabilise variance(if necessary)
log-transformation for changing variance

##### Model Selection
estimate $p, q$ on ACF/PACF plots

choosing between candidate functions
* model parsimony
* minimization of information criteria
* ANOVA-type test
###### (a) determine differencing order to induce stationarity
trend: first order difference $d=1$

seasonality: seasonal difference $D=1$

test stationarty:
* ACF plot
* unit-root tests(e.g. Dickey-Fuller test)

###### (b) Plot the ACF/PACF of stationary data to determine potential AR/MA orders
Usually models will require only AR terms or MA terms, rarely both.
* AR:tails off or is sinusoidal in **ACF**, cuts off lag $p$ in **PACF**
* MA: cut off lag $q$ in **ACF**, tails off or is sinusoidal in **PACF**
* ARMA: tail off or is sinusoidal in both **ACF** and **PACF**


###### (c) estimate model and use information criteria to find the best model
use information criteria (AIC, BIC) to help identify the best model.

*automated algorithm does not guarantee a well-fitting model*


##### Check if residuals of chosen model are white noise
test autocorrelation; Ljung-Box test
A transformation may help with non-normally distributed residuals


### Transfer Function
WHY:  move beyond the basic intervention impact shapes.
$$
Y_t = \mu + \frac{\omega_0+\omega_1 B+\omega_2 B^2 + \cdots+\omega_hB^h}{1-\delta_1B-\delta_2 B^2 - \cdots - \delta_r B^r} X_t + \varepsilon_t \\
B^p X_t = X_{t-p}
$$
$\omega_0$ initial value for the impact of the intervention
$T$ the time of the intervention
$\delta$ decay rate
$X_t$ the intervention variable
$h$ when the effect happen
$r$ decay pattern

### Appendix
Defect: ITS cannot exclude the possibility that any observed change was due to *the intervention of interest* or *another co-intervention*.

Box Jenkins: 50 time points.




