# Final Project

## Data Files of Git collaborations

- Uncleaned and Cleaned Data

## Topic
How can we predict the intensity of the 2018-2019 flu season given data from previous flu seasons?

## Links
https://gis.cdc.gov/grasp/fluview/fluportaldashboard.html

This is the CDC’s Flu Portal Dashboard. It provides data and visualizations of flu incidence in the USA.

https://www.cdc.gov/flu/fluvaxview/reportshtml/trends/index.html

This link, also from the CDC, provides data on the amount of people in America who received the flu vaccine each year.

https://www.cdc.gov/flu/about/burden/index.html?CDC_AA_refVal=https%3A%2F%2Fwww.cdc.gov%2Fflu%2Fabout%2Fdisease%2Fburden.htm

This link provides data on the number of flu deaths each year.

## Description 

The CDC provides data on influenza in the United States from 1997 to 2018 (we are using 2010 to 2018 for our project due to missing data prior to 2010). The flu incidence data is broken down by HHS Region, Census Division, and State, and by either public health or clinical laboratory. It includes variables such as the weekly total number of specimens tested, the number of positive influenza tests, and the percent positive by influenza virus type. The flu vaccination data provides information on the % of people vaccinated for each state and nationwide during each month of flu season, and has subgroup data as well such as the % vaccinated for children and adults. Finally the number of flu deaths is just the number of people nationwide who have died of flu from 2010 to 2018, although the CDC notes that these numbers tend to be underestimates.

## Overview

### Part I: Shiny interactive data visualization:

We want to first look at the total flu cases over the past 10 years using a time series plot and identify unusual patterns. For example, the 2018 flu season was the worst since the 2009 swine flu pandemic, and roughly 7.7% of all U.S. citizens seeking medical care experienced flu-like symptoms. 

Then the question becomes--is there a way to figure out who was most at risk for contracting a specific type of virus? We plan to break down the outbreak across different states and try to explore the distributions of various flu cases among different age groups. We will try to build interactive plots such as maps, area plots, and bar graphs.

### Part II: Predict the intensity of the 2018-2019 flu season given data from previous flu seasons: 

After we gain some basic knowledge of the data, we think it’s necessary to predict the intensity of the 2018-19 flu season. We plan to build time series forecasting models that use data for the past 10 years (such as number of people with type A flu) in order to predict number of people who will catch a specific type of flu in the 2018-19 season for each age group by state/region. 

One way to come up with a reasonable dataset is that we try to use number of people who have type X flu from 2010-2017 as predictors, and the same variable for 2018 as response. For example, some potential predictors would be : # of people (age 18-64) who have type A, B, or C flu from 2010-2017 or the % of people (age 18-64) who were vaccinated from 2010-2017. Then, the response would be: # of people (age 18-64) who have type A flu in 2018. The reason for doing this is that we believe for the same state, values of one variable in the past may contribute to that same variable in the future.

The goal of our modeling strategy is to build a variety of different time series forecasting models and select the best one. We will develop some stochastic models such as autoregressive (AR), moving average (MA), and autoregressive-moving average (ARIMA) in order to forecast seasonal influenza in the USA. Then we will use AIC to select the best parameter configuration of the models, use that model to forecast the 2018-2019 flu season, and compare our predictions to the actual results.

## Summary of Progress

We have already finished the data collecting, and moving on to data cleaning parts. The data we have downloaded includes three sets:
- Influenza Positive Tests Reported to CDC by Public Health Laboratories and ILI( influenza-like illness) Activity, from year 2010 to 2019;
- Percentage of visits for ILI, from year 2010 to 2019;
- Total number of people vaccinated, from year 2010 to 2019.

We have done some preliminary data cleaning, such as merging yearly datasets of the percentage of influenza visits nationwide into one large dataset. We have also done some exploratory research on prior time series models, in particular for influenza to see if there are some best practices and underexplored avenues of research that we can pursue. 
