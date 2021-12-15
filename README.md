# DATA512_County_Project

## Project Goal

This extension of A4 serves to address three primary questions:

1) How did the covid pandemic affect St. Louis economy at the county level? 
2) Which demographics in St. Louis County were more susceptible to contracting severe cases of covid? 
3) Were there surrounding, more rural counties that were affected in a similar manner to St. Louis County? 

## Data Sources

The sources used to build the datasets and create their subsequent visualizations are provided below

•	Covid19_deaths_demographics: spreadsheet containing the Covid-19 deaths by sex, age, and race demographics in St. Louis County, Missouri. 
Source: https://fred.stlouisfed.org
•	Unemployment rates: Spreadsheet containing the unemployment rates for St. Louis county provided by the Bureau Labor of Statistics. 
Source: https://www.bls.gov/eag/eag.mo_stlouis_msa.htm
•	Coronavirus (Covid-19) Data in the United States: The primary data published here are the daily cumulative number of cases and deaths reported in each county and state across the U.S. since the beginning of the pandemic.
Source: https://github.com/nytimes/covid-19-data
•	Raw US Confirmed Cases: contains the confirmed cases for states & counties throughout the U.S. from the Kaggle repository of John Hopkins University COVID-19 data. 
Source: https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_confirmed_cases.csv

Google Cloud Platform API Documentation: https://github.com/GoogleCloudPlatform/covid-19-open-data

## Directory Tree

![image](https://user-images.githubusercontent.com/92059047/146136478-dc4bbe4c-252a-43e8-ae1b-5b7bdb97982b.png)

## Data Structure of Finalized Data

All the final datasets that are used for the analyses are stored in the final_data folder, the raw data used to build these datasets exist in the raw_data folder. Some of them are the raw data were downloaded from the Google Cloud Platform API, whereas others are intermediate files saved in the raw_data folder for convenience and to ensure reproducibility.

### MO_stlouis_v_rural

| Attribute | Definition |
|-----------|------------|
| county | Name of county in the United States |
| date | Date of data collection point |
| cases | number of cases in county on date |
| cases_avg | average number of cases in county |
| cases_avg_per_100k | average number of cases in county per 100k residents |
| deaths | number of deaths in county on date |
| deaths_avg | average number of deaths in county |
| deaths_avg_per_100k | average number of deaths in county per 100k residents |

### Case_by_Demographic

| Attribute | Definition |
|-----------|------------|
| Sex | Biological Sex Categorization of Residents |
| Age Group | Age Group Categorization of Residents |
| Cases | Confirmed Covid Cases in St. Louis County |
| Case_Rate | Confirmed Covid Case Rate in St. Louis County |

### Case_by_Race

| Attribute | Definition |
|-----------|------------|
| Race | Race Categorization of Residents |
| Age Group | Age Group Categorization of Residents |
| Cases | Confirmed Covid Cases in St. Louis County |

### stlouis_covid_econ_data

| Attribute | Definition |
|-----------|------------|
| Observation | Month of Unemployment data collection point |
| MOSLURN | Bureau of Labor Statistics (BLS) Metric for measuring unemployment |
