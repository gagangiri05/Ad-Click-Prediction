# Advertisement-with-ML

## Project description:
In this project we will be working with a fake advertising data set, indicating whether or not a particular internet user clicked on an Advertisement on a company website. We will try to create a model that will predict whether or not they will click on an ad based off the features of that user (classification problem).

This data set contains the following features:

* 'Daily Time Spent on Site': consumer time on site in minutes
* 'Age': cutomer age in years
* 'Area Income': Avg. Income of geographical area of consumer
* 'Daily Internet Usage': Avg. minutes a day consumer is on the internet
* 'Ad Topic Line': Headline of the advertisement
* 'City': City of consumer
* 'Male': Whether or not consumer was male
* 'Country': Country of consumer
* 'Timestamp': Time at which consumer clicked on Ad or closed window
* 'Clicked on Ad': 0 or 1 indicated clicking on Ad

## Methodologies: 

We approach the classification problem of predicting the variables 'click on the ad' by the visitors of the website using different classification
algorithms: logistic regression and random forest classifiers. After initial EDA we construct a ML pipeline where the split of the dataset is done with 34% test size. The logistic model does not see any under or over fitting of data. The random forest classifier pergorms better (96% score) in the validation test set
than the logistic model(90%). Using the random forest model we create a hiearchy of features importance. We conclude that the variable more influencial to predict
clicks on the ad is the daily internet usage of the user that visits the website. Since this is a variable that we can not control we decided to run the random forest model where this variable is erased from the ensemble of explanatory features. The score of the model goes a bit down when we run this version of the algorithm. Although interestingly we register in the hierachy of the new features importance that the variable are income surpasses the varaible age (which does not happen in the features importance of the first model). The third part of this project concerns hypothesis A/B testing where we analyse different confidence intervals (5% and 40% associated risk levels respectively) for the proportion rate of clicks done by male and female visitors. For the smallest level of risk 5% nothing can be concluded. Although for the higher level of 40% risk we observe empirically by random sampling thar the proportion of clicks on the add done by females surpasses the one done by males. This can be seen as a first indication of a marketing future strategy to be implemented. Although the Qui2 test built with 5% risk tell us that the variables "click on the add" and "gender" are independent concluding this discussion.  



## Code and resources used:
**Python version:** 3.7
**Libraries/packages used:** pandas, numpy, matplotlib, seaborn, scikitlearn
**Dataset:** available at the repo
