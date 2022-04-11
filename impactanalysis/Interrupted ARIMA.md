# Interrupted ARIMA

Methods: 

* segment regression(trends, types of impact)
* ARIMA(seasonality, autocorrelation)

ITS is considered one of the best designs for establishing causality when RCT are feasible.

## Methods

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


### Components of ARIMA models
assumptions: errors are normally distributed.

Available Situation:

* any continuous outcome
* large count that are not bounded by zero

Unavailable Situation: small counrts following Poisson distribution

ARIMA notation: $(p,d,q)\times (P,D,Q)_S$

* $p$ the order of the AR part of the model
* $d$ the degree of non-seasonal differencing
* $q$ the order of the MA part of the model
* $D$ the degree of seasonal differencing
* $P$, $Q$ AR, MA terms for seasonal component

Lag: 

* prespecify a reasonable period of time in which it would be expected for the impact to be observed based on content knowledge or previous research to avoid spurious associations.
* The most appropriate delay within this range of options can be determined at the modelling stage.



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







