# Various use cases on Covid-19 analysis

### Use Case-1: Covid forecasting using DL & Stats models
#### [dataset](https://www.kaggle.com/anirbansarkar823/covid-forecasting-using-dl-stats-models/data)
* predicting the number of COVID cases, Deaths & number of Cured cases using Indian covid count dataset from kaggle. 
* This is a time series analysis problem
* Worked on various types of visualization to understand how many cases/deaths/cured cases are being reported monthly, weekly and daily basis.
* converted the dataset into time series using below method:
    * First divided the whole dataset into train and test data and converted them to numpy arrays.
    * Then for every 'n' number of samples in train data do
        * take first n-1 data points as X, and nth sample as y
    * For test data, take first n data set x_test, and remaining all as y_test
* Used LSTM architecture to predict the number of cases
* Then used statistical models for decomposition of Cured count into 3 time series components: Trend, Seasonality and Residual.
* Used Augmented Dickey Fuller statistical test to find out whether the given Time Series is stationary (fixed mean and variance over time) or not. Here, if p-value is less than significance level (0.05), the we can reject the null hypothesis (the time series is not stationary)
* Used statistical models like Holt, SimpleExponentialSmoothing to predict the future cases.


### Use Case-2: Covid Presence Detection - Based on symptoms given as features
#### [dataset](https://www.kaggle.com/anirbansarkar823/covid-presense-detection-ensembling/data)

* I have used Dataprep library, which is a python library that is used for data preparation and EDA.
* Used Bi-Variate analysis to understand which features are actually affecting individuals with COVID-19.
* Used ensembling and selected best classifier to predict the final output.