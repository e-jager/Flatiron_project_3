# Predicting the condition of water wells in Tanzania
**Author: Em Jager, Columbia University**

## Overview
Tanzania, considered a developing country, struggles with providing access to clean water to its population of 57 million people. The country already has a large amount of water access sites in place, however some require maintenance and others are not functioning and need complete repair or replacement. Here, based on my analysis, I will demonstrate a classifing model that is able to predict the condition of a water well, using information about the type of pump, when it was installed, and location details in order to assist the Tanzanian government in prioritizing locations for providing resources and teams to repair water wells. This information will also be able to recommend for the future which types of pumps and what conditions should be considered when installing brand new wells across the country. 

## Business Understanding

## The Data

The data for this project was provided by the Taarifa waterpoints dashboard, which aggregates data from the Tanzania Ministry of Water.

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


## Methods

## Key Statistics & Analysis

## Recommendations

## Next Steps

## Repository Structure
