# Predicting the condition of water wells in Tanzania
**Author: Em Jager**

## Overview
Tanzania, considered a developing country, struggles with providing access to clean water to its population of 63.6 million people. According to the World Bank, 61% of households in Tanzania have access to a basic water supply. The country has a large amount of water access sites in place, however some require maintenance and others are not functioning and need complete repair or replacement. In this project, I built a classifing model that is able to predict the condition of a water well, using categorical information about the waterpoint including type of pump, when it was installed, and location details in order to assist the Tanzanian government in prioritizing locations for providing resources and teams to repair water wells. This information will also be able to recommend for the future which types of pumps and what conditions should be considered when installing brand new wells across the country. 

## Business Understanding
Water is an essential human right, so the goal of this project is to provide the Tanzanian government and local NGOs with a method to prioritize water pump sites that need repair. Lack of access to water impacts so many parts of society from public health, gender equality, income equality, economic growth and development and overall quality of life so this is a really important research focus. 

## The Data

The data for this project was provided by the TAARIFA waterpoints dashboard, which aggregates data from the Tanzania Ministry of Water. The dataset has about 60,000 water wells with  categorical data on their type, location, and functioning status, ranging from 1960 to 2013.

From the Taarifa website:
> "Taarifa is an open source platform for the crowd sourced reporting and triaging of infrastructure related issues. Think of it as a bug tracker for the real world which helps to engage citizens with their local government. We are currently working on an Innovation Project in Tanzania, with various partners."

### **Column labels for data:**

amount_tsh - Total static head (amount water available to waterpoint)\
date_recorded - The date the row was entered\
funder - Who funded the well\
gps_height - Altitude of the well\
installer - Organization that installed the well\
longitude - GPS coordinate\
latitude - GPS coordinate\
wpt_name - Name of the waterpoint if there is one\
num_private -\
basin - Geographic water basin\
subvillage - Geographic location\
region - Geographic location\
region_code - Geographic location (coded)\
district_code - Geographic location (coded)\
lga - Geographic location\
ward - Geographic location\
population - Population around the well\
public_meeting - True/False\
recorded_by - Group entering this row of data\
scheme_management - Who operates the waterpoint\
scheme_name - Who operates the waterpoint\
permit - If the waterpoint is permitted\
construction_year - Year the waterpoint was constructed\
extraction_type - The kind of extraction the waterpoint uses\
extraction_type_group - The kind of extraction the waterpoint uses\
extraction_type_class - The kind of extraction the waterpoint uses\
management - How the waterpoint is managed\
management_group - How the waterpoint is managed\
payment - What the water costs\
payment_type - What the water costs\
water_quality - The quality of the water\
quality_group - The quality of the water\
quantity - The quantity of water\
quantity_group - The quantity of water\
source - The source of the water\
source_type - The source of the water\
source_class - The source of the water\
waterpoint_type - The kind of waterpoint\
waterpoint_type_group - The kind of waterpoint

### What features are relevant to the analysis of well function?
**Installer** - it's possible that there are some installers that do a less quality job of installing the water pumps, therefore there is a higher chance of them being non functional

**Scheme management** - who operates the waterpoint could influence whether it is functional, some groups may do a better job than others at managing and maintaining the waterpoint

**Construction year** - older waterpoints may be more likely to need repair. Additionally, year could be incorporated into the analysis of other variables because other variables could affect the lifespan of a water pump

**Extraction type** - the type of water pump should be investigated in case some types last longer than others or are more likely to be functional

**Management or management group** - how the waterpoint is managed

**Quantity** - if the waterpoint is dry that seems like an obvious indicator that it may not be functional

**Source** - 

**Waterpoint type** - the kind of waterpoint could have an affect on the lifespan of the waterpoint
From these categories I chose to focus my analysis on: quantity, waterpoint type, payment type, construction year, source, water quality, management group, and installer. These categories were chosen based on preliminary analysis - some categories were eliminated from inclusion in the final model because there was very little range in the categories within a feature. For example, extraction type was considered, but a huge majority of the waterpoints use the same extraction type, so there is not enough variability in the data for it to be a useful predictor of functioning status. Other variables were not included in the model such as latitude and longitude because in the model I worked on, I was not able to logically explain how latitude and longitude would impact the functioning status of the waterpoints. In the future, perhaps lat and long could be used along with other locational variables such as basin, subvillage, and region to analyze the impact of location within the country on whether the waterpoints are functioning. It is possible that some regions receive more attention and therefore have better functioning waterpoints. 

## Methods
I explored several options for models, and ultimately the final model I used is a Decision Tree Model. A decision tree model is a predictive algorithm that uses a tree-like structure to make decisions based on input features. It recursively partitions the data into subsets, aiming to find the most discriminative feature at each step and ultimately leading to leaf nodes that represent predicted outcomes. Prior to running the model I used OneHotEncoder to convert the categorical variables into binary columns for each category within the variable. I also concatenated to the categorical data the numerical data for construction year to include in the model. 

The following are the results of the Decision Tree Model:
Accuracy: 0.8325936883629191
Precision: 0.9119150609516319
Recall: 0.8359769286229272

Based on the accuracy score, the model is able to predict 83.26% of outcomes correctly. The precision tells us that the model predicts 91.19% positive outcomes correctly, or the ability to avoid false positives. The recall tells us the ability of the model to avoid false negatives is 83.60%. The confusion matrix below also shows these results.  

## Key Statistics & Analysis

## Recommendations

## Next Steps

## Repository Structure
