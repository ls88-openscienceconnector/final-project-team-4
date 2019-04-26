
## Jupyter Notebook

The final jupyter notebook consists of 2 parts: The first section is the code from the original study used to produce the original analysis. This was kept as the data tables ultimately produced were a result of feature engineering. The second part which is indicated by “Our analysis” contains our code which includes the t-tests and scatter plots were produced in our reproducibility analysis. 

## Strategy

Our analysis was done using code in Jupyter Python. The original study was done in using the pandas library whereas our coding portions relied upon the datascience library. In the original study, the data frame was manipulated to add new columns and produce new variables, some of which were used in the final analysis. The output of the original study consisted of various bar charts to show which factors were relevant in determining movie success.
In order to see if the results of the original study could be reproduced, we decided to use two statistical methods; the t-test and correlation coefficient. We conducted the t-test on the two most important variables the original study found as relevant predictors of movie success. We then looked at some of the variables the original study left out, and plotted scatter plot visualizations and determined correlation coefficients between those variables and movie success to determine if those variables were correctly left out. Thus, by using a t-test to show the statistical significance of variables deemed important in the original study, and by using correlation coefficients to show moderate correlation for the variables left out in the original study, we were able to reproduce the findings of the original study. 
Analysis and Steps Taken
Our analysis consisted of two main steps. The first was the t-test with variables used in the original study and the second was the correlation coefficient for variables neglected in the original study. It is important to note that the original study did not use the statistical techniques aforementioned, as their final analysis was done using bar chart visualisations. 



## T-test

In the original study, there were weights assigned to different genres to account for the general differences that exist among movies. First, we generated scatter plots to assess the relationship between some of the variables used in the original study. In particular, we generated scatter plots of crew score vs popularity and actor score vs popularity. We found that there was no identifiable threshold in differentiating a successful and unsuccessful movie. 

The t-test was conducted first using crew scores and then actor scores. For our t-test, we took the scores and computed the average value. This average served as the threshold value we used to create two different groups of movies, movies which had high crew scores that is above the threshold value, and movies with low actor scores that is below the threshold value. As a result, we crafted our null hypothesis around this threshold. The null hypothesis was the distance between the average movie rating between high and low crew scores was 0. 

We used the above mentioned method to determine whether the factors were statistically significant in assessing the movie’s success. We used A/B testing and constructed a bootstrapped 95% interval. 
For crew score the bootstrapped 95% confidence interval was:
[-0.057318, 0.056744] and the t-stat = 0.342534. 
For actor score, the bootstrapped 95% confidence interval was:
[-0.060538, 0.058431] and the t-stat = 0.317214

While testing, since the observed statistic was found to be outside of the confidence interval, this implies that it was statistically significant, and hence we can reject our null hypothesis in favor of the alternative. This shows that the variables the original study found to be important, are statistically significant in determining movie success. 


## Outside variables

Since the above t-test showed that the variables used in the original study were significant in determining a movie’s success, we decided to test some of the variables left out in the original study: budget and runtime. These variables were present in the original dataframe, but were not used in the original study when they analysis was conducted.

We converted the dataframe from pandas to datascience and created 2 scatter plots: 
1) runtime vs popularity 
2) budget vs popularity
We then added a line of best fit and computed the correlation coefficient of each factor. We found that there was a small correlation for runtime and a medium correlation for budget.
The correlation for runtime and popularity was 0.23324122282495613.
The correlation for budget and popularity was 0.5000357985863506.

The small correlation value for runtime supports the idea that this variable was appropriately left out in the original study. The correlation value obtained for budget and popularity indicates a moderate correlation and so perhaps the variable could have been included in the final output of the original study.



```python

```
