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

## advanced quantitative analysis 
The main requirement for this sub-task is to explore more things that we don't do it in the basic quantitatibe analysis. Their difference is: in the basic quantitative analysis, we emphasize on solid analysis. in the exploration, we emphasize on creativity.

Due to its property, this task is very free. people in charge of this can do whatever he want, even to the extent that do nothing because he thinks there is nothing interesting and available left. But in contrast to this, the results here should be agreed by all members to present for better time allocation and more reliable results.

As for me I think a good topic here should be: Wouldn't think of it the first time, but the data does reveal relationships.
I recommend to refer to some data: google trend-university; google trend-recuitment
I recommend this work begin after the basic quantitative analysis for reference and good startpoint.

## Dataset
[OECD](https://data.oecd.org/)

[Google Trends](https://trends.google.com/trends/?geo=CH)

