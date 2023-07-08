# matplotlib-challenge - Pharmaceutical Drug treatment analysis using pandas and matplotlib

## Table of Contents
* [Background](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#background)
* [Analysis](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#analysis)
* [Merged DataFrame](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#merged-dataframe)
* [Summary Statistics](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#summary-statistics)
* [Bar Charts and Pie Charts](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#bar-charts-and-pie-charts)
* [Calculating Quartiles, Finding Outliers, and Creating a Box Plot]()
* [Creating a Line Plot and a Scatter Plot](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#creating-a-line-plot-and-a-scatter-plot)
* [Calculating Correlation and Regression](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#calculating-correlation-and-regression)

## Background

This repository contains an analysis used to create a technical report of a clinical study run by Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. The company began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. The complete data from their most recent animal study was provided. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

Tables and figures needed for the technical report of the clinical study, as well as a top-level summary of the study results are captured in this analysis. The project uses two datasets:
1. [Mouse_metadata.csv](https://github.com/dspataru/pandas-challenge/blob/main/data/Mouse_metadata.csv) : contains data about the mice that were used in the study, including mouse ID, drug regimen , sex, age in months, and weight (g).
2. [Study_results.csv](https://github.com/dspataru/pandas-challenge/blob/main/data/Study_results.csv) : contains data about mouse ID, different timepoints in the treatment, tumor volume (mm3), and metastatic sites.

The above two csv files can be found in the data folder of the current repository. Python's pandas library is used to import, merge, and sort the data into dataframes for analysis. The data was cleaned and prepared for analysis by removingany mouse ID with duplicate time points. Summary statistics of the merged dataframe were prepared. Matplotlib is used to visualize the data using bar charts, pie charts, line plots, scatter plots, and box plots. The correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen was calculated and a linear regression model is displayed as well.

The IDE used for this challenge is Jupyter Notebook.

#### Key Words
Jupyter Notebook, Pandas, Python, DataFrames, DataSets, Matplotlib, Statistics

## Analysis

## Merged Dataframe

## Summary Statistics

## Bar Charts and Pie Charts

## Calculating Quartiles, Finding Outliers, and Creating a Box Plot 

## Creating a Line Plot and a Scatter Plot

## Calculating Correlation and Regression
