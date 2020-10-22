# Comparative Analysis of Spatial and Temporal Models on PM2.5 Concentration in Beijing

### 0 File Documentation

`raw_data` folder : this folder contains two sub-folders `Beijing_District` folder which contains the shape files and `Beijing_17` which contains the raw air condition data;

`cleaned_data` folder : this folder contains the cleaned and transformed datasets;

`output` folder: .Rdata and .rds: Files to shorten runtime;

[`Final_Report.html`](https://github.com/lichunxiao9501/Comparative-Analysis-of-Spatial-and-Temporal-Models-on-PM2.5-Concentration-in-Beijing/blob/master/Final%20Report.html) file : The final report;

[`Final_Report.Rmd`](https://github.com/lichunxiao9501/Comparative-Analysis-of-Spatial-and-Temporal-Models-on-PM2.5-Concentration-in-Beijing/blob/master/Final%20Report.Rmd) file: The rmd file including all codes.


### 1 Introduction

In this project, we built a spatial-temporal model to predict PM2.5 in Beijing based on the air quality data and meteorology data from 2017-01-31 to 2018-01-31 of several monitoring stations in Beijing. In addition, in order to analyze the Beijing air pollutants in the district scale, we also get the geographical boundaries data of all the districts in Beijing.

### 2 Project Overview
This projects consist of five major parts: 
* Data Introduction
* Data Cleaning
* Time Series Analysis 
* Spatial Analysis 
* Spatial-temporal Analysis.

### 3 Models Details

#### 3.1 Temporal Models
In order to analyze PM2.5 in the time series scale, we pick one of the most busy districts in Beijing, Haidian, where most of the univeristies in Beijing locate, as our target district.

The temporal models we fitted includes:

* Hourly ARIMA model;
* Daily ARIMA model;
* Daily Gaussian Process model;
* Daily linear regression model with Gaussian Process residual;
* Daily Random Forest model.

#### 3.2 Areal Models

In order to build the spatial models, we pick 2017-10-03 as our target date, and try to fit spatial models (areal and point reference) for the PM2.5 concentration. The PM2.5 concentration in each station points and the average PM2.5 of all the stations in each districts are calculated respectively.

The areal spatial models we fitted includes:

* CAR (Conditionally autoregressive) model;
* SAR (simultaneous autoregressive) model;
* Bayesian CAR model;
* Bayesian SAR model;
* Linear regression using air quality data with CAR residual;
* Linear regression using air quality and meteorology data with CAR residual.

#### 3.3 Point Inference

The point reference models we fitted includes:

* Thin Plate Splines model;
* Spatial Gaussian Process model using JAGS;
* Spatial Gaussian Process model using spBayes.

#### 3.4 A Spatial-temporal Model

And finally a Spatial-temporal Model is fitted. In order to build a spatial-temporal model, we use monthly average data of all the air pollutants in each air quality stations by averaging all the observations thoughout each month.

### 4 Visualization Examples

A few data visualization examples are shown as follows:

Pic 1: Beijing Districts
![](https://github.com/lichunxiao9501/Final-Project-STA644-Temporal-and-Spatial-Model/blob/master/pics/beijing_districts.png)

Pic 2: Beijing Air Quality and Meteorology Stations Distribution
![](https://github.com/lichunxiao9501/Final-Project-STA644-Temporal-and-Spatial-Model/blob/master/pics/stations.png)

Pic 3: Beijing PM2.5 Spatial Model Prediction
![](https://github.com/lichunxiao9501/Final-Project-STA644-Temporal-and-Spatial-Model/blob/master/pics/spatial_predictions.png)

