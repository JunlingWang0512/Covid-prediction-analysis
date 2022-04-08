# COVID's Impact on Society
## qualitative analysis
read some popular papers and summarize their ideas. 

summarize different aspects of social impact, such as economy, education, etc.


##  basic quantitative analysis
utilize data from OECD & Google Trends for basic quantitative discussion.
I think the data on Google Trends is an indicator for people's subjective will, since people tend to search things they realize importance. And data on OECD reflects objective social change. Our work concerns both the changes in ideas and changes in circumstances.

### Specific Subjects

| source| goal | reflection| expected |
| --- | --- | --- | --- |
|GT:zoom, coursera | education medium | subjective | positive |
|GT: invest | property management in unstable circumstance | subjective | positive |
|GT: health| people's concern level for health | subjective | negative |
|OECD: unemployment | macro economy| objective | positive |


### Techniques
basic statistics: t-test, Wilconxin rank test, ...

single time series analysis: stability test, ...

double time series analysis: Granger causality, ...

### Problems
While measuring a social metric, we could regard COVID as a pulse with long-term impact or use COVID's data as an independent variable strength indicators. We need to distinguish between the two opinions.


The preliminary idea is that using single time-series techniques for pulse situation and using double time-series techiniques for strength indicator situation.

For example，we regard COVID as a pulse for GT-invest. We test the stability of this time series or use t-test for data before the step and data after the step.

Even though **Granger causality test** is more convincing, we think few data can give positive results in this situation. That is to say, we have to use basic statistical methods (eg: Wilconxin rank test) for correlation in most instances, instead of stronger conclusion from advanced & specialized methods.

What specific techniques should we use for those two situations? 

How do we reveal causality instead of simple correlation with **reasonable complexity** and available data. In my experience, conclusions considering causality need too much expertise and may be a thesis instead of student project.

How do we clarify the time interval we select is meaningful? For example, we plan to start our discussion from 2016/01 to 2022/03. But how do we prove the change in this interval is due to COVID rather than other social factors?

### Interrupted Time Series Analysis
These concepts & techniques seem to be suitable for our problem and consideration. Even though the technique is not beyond the ordinary time series method very much, the important thing is the area of interrupted time series systematizing the related conceptions.

<br/>

I list some reference material here:

[Interrupted Time Series-DS4PS](https://ds4ps.org/pe4ps-textbook/docs/p-020-time-series.html): A basic introduction to Interrupted Time Series, based on segmented linear model. Introduce some basic concepts:immediate & sustain effect, delay(lag),regression to mean, control groups for valid threat.

[Interrupted time series regression for the evaluation of public health interventions: a tutorial
](https://pubmed.ncbi.nlm.nih.gov/27283160/): A systematic introduction based on segment linear model with everything important to consider. The orchestration order is the pipeline of time series analysis. This paper clarify the central consideration in each step.

[Interrupted time series analysis using autoregressive integrated moving average (ARIMA) models: a guide for evaluating large-scale health interventions](https://bmcmedresmethodol.biomedcentral.com/articles/10.1186/s12874-021-01235-8) A systematic introduction to ARIMA Interrupted Time Series with working example. I think it is the most complex degree we can reach.

[Using intervention time series analysis to assess the effects of imperfectly identifiable natural events: a general method and example](https://bmcmedresmethodol.biomedcentral.com/articles/10.1186/1471-2288-6-16) Most ITSA are used for estimating policy, since clear start date. However, clear start date is not available and essential in most situation. This paper discuss the related issues.



[its.package](https://cran.r-project.org/web/packages/its.analysis/index.html) R package for interrupted time series, based on Type-2 Sum Squares ANCOVA Lagged Dependent Variable model. I think it is too complex to implement in our situation. But it is still a good preparation.

Even though the interrupted time series is not best, we can use the arguments in these papers for solider work. I think they are enough for such a student project.

<br/>

The resource for interrupted time series analysis is adequete:

[The effect of the late 2000s financial crisis on suicides in Spain: an interrupted time-series analysis](https://pubmed.ncbi.nlm.nih.gov/23804080/): The most population for interrupted time series I found.

The reference for COVID's impact on society based on interrupted time series analysis is also adequete, the situation is very similar to us. They are also considering wellbeing. We could even replicate some of them for our results.

[Examining the immediate effects of COVID-19 on residential and commercial burglaries in Michigan: An interrupted time-series analysis](https://www.sciencedirect.com/science/article/pii/S0047235221000544)

[Effects of the COVID-19 pandemic on heart failure hospitalizations in Japan: interrupted time series analysis](https://pubmed.ncbi.nlm.nih.gov/34913269/)

[Suicide trends in the early months of the COVID-19 pandemic: an interrupted time-series analysis of preliminary data from 21 countries](https://www.thelancet.com/journals/lanpsy/article/PIIS2215-0366(21)00091-2/fulltext)

[Disentangling the Impact of Covid-19: An Interrupted Time Series Analysis of Crime in New York City](https://pubmed.ncbi.nlm.nih.gov/35079215/)

[Effectiveness of employer financial incentives in reducing time to report worker injury: an interrupted time series study of two Australian workers’ compensation jurisdictions](https://bmcpublichealth.biomedcentral.com/articles/10.1186/s12889-017-4998-9) (segmented linear model + ARMA)

[Evolutionary cost analysis of valsartan initiation among patients with hypertension: a time series approach](https://pubmed.ncbi.nlm.nih.gov/22011107/)（segmented linear model + ARMA）



## advanced quantitative analysis 
The main requirement for this sub-task is to explore more things that we don't do it in the basic quantitatibe analysis. Their difference is: in the basic quantitative analysis, we emphasize on solid analysis. in the exploration, we emphasize on creativity.

Due to its property, this task is very free. people in charge of this can do whatever he want, even to the extent that do nothing because he thinks there is nothing interesting and available left. But in contrast to this, the results here should be agreed by all members to present for better time allocation and more reliable results.

As for me I think a good topic here should be: Wouldn't think of it the first time, but the data does reveal relationships.
I recommend to refer to some data: google trend-university; google trend-recuitment
I recommend this work begin after the basic quantitative analysis for reference and good startpoint.

## Dataset
[OECD](https://data.oecd.org/)

[Google Trends](https://trends.google.com/trends/?geo=CH)


