# Modeling-Mental-Health-Disease

## Overview

The goal of this project is to model depression rates in the U.S. This is useful not only for government agencies, but also to better understand what else is correlated with depression. Having a better forecast for depression will allow the government to allocate additional funds to fight the mental health crises. The final project is useful to any mental health organization or government agency that can advocate or provide support for those with depression. 

## Business Understanding

Depression rates in the U.S. have grown significantly in the past two years during Covid. This has a tremendous impact on not only those who experience this disease, it affects those around them, and the Economy as a whole. According to a 2018 study by *[PharmaEconomics](https://link.springer.com/article/10.1007/s40273-021-01019-4)*, depression cost the U.S. economy $326 billion in 2018. This number is rising, not only because of rising rates but because those with the disease are not willing or in many cases unable to receive proper care. 

By modeling Depression Rates more accurately, the CDC will be able to more confidently secure increased funding to help improve the lives of those with this disease and therefore ease the economic and psychological burden of U.S. citizens. 


## Data Understanding

The data used for this analysis is a yearly survey of those diagnosed with Depression. It comes from the World Health Organization from a 2020 report on the Global Burden of Disease from 1990-2019. Additionally, other mental illnesses were tracked during this time. This could prove useful for further analysis of exogenous variables moving forward. 



### EDA
Looking at the graph of mental illness in the U.S. there is little fluctuation between rates during this time period. Additionally, rates are lower than suspected and reported by other disease tracking agencies. This is possibly due to limitations with the survey method and reliant on Doctor's abilities to accurately diagnose these diseases. 

Even still there is some fluctuation in Depression rates in the U.S. that can be modeled. 


## Data Preparation

Attempts were made to make the time series data stationary by using various techniques. These included log and root transformations and various differencing. After attempting multiple times to make the time series stationary, the lowest score achieved on the Dickey-Fuller test was an alpha of .086 meaning I was unable to reject the null hypothesis that the data was not stationary. 

Thankfully, ARIMA models do not require the time series to be stationary, so I was able to move forward with my analysis. 

Before Modelling, I separated the time series so the first 80% of my data would be a training set and the other part could be used as a testing set. Additionally, a validating set was used to grid search the parameters for my ARIMA model. 
