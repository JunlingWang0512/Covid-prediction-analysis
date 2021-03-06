# COVID's Impact on Society
## qualitative analysis
read some popular papers and summarize their ideas. 

summarize different aspects of social impact, such as economy, education, etc.

Recommendation:

* [Individual differences and changes in subjective wellbeing during the early stages of the COVID-19 pandemic](https://psycnet.apa.org/doiLanding?doi=10.1037%2Famp0000702&errorCode=invalidAccess)

##  quantitative analysis
utilize data from OECD & Google Trends for quantitative discussion.

### Specific Data & Subjects
source: [OECD](https://data.oecd.org/), [Google Trends](https://trends.google.com/trends/?geo=CH)

| source | suject | method |
| --- | --- | --- | 
| GT|zoom | ITSA | 
| OECD | unemployment | ITSA |


### Central Issues
For analyzing COVID's impact on society, we have two ways to examine COVID.

* **malleable variable**：What really matters is when the change begin and how long does the change last. In order to describe the change clearly, we use policies caused by COVID instead of COVID itself.
* **exogenous variable**：The strength of COVID indeed matters! For example, how many people get infected, how many pepole die in given period is important to us!


### Interrupted Time Series Analysis
The area of **interrupted time series** systematizes the related conceptions for our working scenarios.

**Problem**: while the time of onset is not clear, the ITSA model-building process is more **exploratory** than **confirmatory**. Poorly defined or incorrect dates necessarily lead to a wider range of possible models.


**Notice**: 

* Many researchers recommend against the use of ITSA in not clearly defined occurence of the event.
* the functional form is often defined by the researchers after inspection of the data

<br/>


Introduction & Methodology

* [ITS regression for the evaluation of public health interventions: a tutorial
](https://pubmed.ncbi.nlm.nih.gov/27283160/) An introduction based on segment linear model. 
* [ITSA using ARIMA: a guide for evaluating large-scale health interventions](https://bmcmedresmethodol.biomedcentral.com/articles/10.1186/s12874-021-01235-8) A systematic introduction to ARIMA Interrupted Time Series with working example. Provided us with pipeline and basic concepts in our example.
* [Using ITSA to assess the effects of imperfectly identifiable natural events: a general method & example](https://bmcmedresmethodol.biomedcentral.com/articles/10.1186/1471-2288-6-16) How to do when clear intervention time is not available. This paper also clarify the main issues and precautions for the whole analysis pipeline.


COVID-Wellbeing examples for ITSA

* [Examining the immediate effects of COVID-19 on residential and commercial burglaries in Michigan: An interrupted time-series analysis](https://www.sciencedirect.com/science/article/pii/S0047235221000544)
* [Effects of the COVID-19 pandemic on heart failure hospitalizations in Japan: interrupted time series analysis](https://pubmed.ncbi.nlm.nih.gov/34913269/)
* [Suicide trends in the early months of the COVID-19 pandemic: an interrupted time-series analysis of preliminary data from 21 countries](https://www.thelancet.com/journals/lanpsy/article/PIIS2215-0366(21)00091-2/fulltext)
* [Disentangling the Impact of Covid-19: An Interrupted Time Series Analysis of Crime in New York City](https://pubmed.ncbi.nlm.nih.gov/35079215/)

classical examples for ITSA

* [Effectiveness of employer financial incentives in reducing time to report worker injury: an interrupted time series study of two Australian workers’ compensation jurisdictions](https://bmcpublichealth.biomedcentral.com/articles/10.1186/s12889-017-4998-9) 
* [Evolutionary cost analysis of valsartan initiation among patients with hypertension: a time series approach](https://pubmed.ncbi.nlm.nih.gov/22011107/)
* [The effect of the late 2000s financial crisis on suicides in Spain: an interrupted time-series analysis](https://pubmed.ncbi.nlm.nih.gov/23804080/) 


### Data Usage Issues
| Data| Date Event| Choose Indicator | Exclude Rival Explanation |
| --- | --- | --- | --- |
| GT-zoom | easy| hard | easy |
|OECD-unemployment| hard | easy | hard |


#### Defining & Dating an unplanned event
**Problem**: Poorly defined or incorrect dates necessarily lead to a wider range of possible models

**Solution**: the point of onset of the event is unknown must be inferred from data sources that are independent of the time series data that will be used for the ITSA.

#### Choosing indicator data
**Problem**: Results may be biased 

* if the available data do not represent a properly random sample of all available data
* represents only specific sub-populations of events. 


**Notice**: 

* the data used in ITSA for assessing the effect of intervention should not be used to identify its timing.
* recorded in same way across the entire period of data collection.


#### Evaluating rival explanation
**Problem**: If the timing of the intervention is not clearly defined, the possibility that its effects have a rival explanation increases, such as


* a change occurred in the process of measuring the time series at approximately the same time as the intervention.
* there was confounding by other interventions that occurred concurrently with intervention that may have affect the time series.

**Solution**:

* **Independent data** that provides an insight into the behaviour of the time series
* **Existing research** in the field and related fields;
* The views of **independent experts** who have an understanding of the dynamics of the process being studied



### Granger Causality
