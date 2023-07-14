# matplotlib-challenge - Pharmaceutical Drug treatment analysis using pandas and matplotlib

## Table of Contents
* [Background](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#background)
* [Analysis](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#study-observations)
* [Merged DataFrame](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#merged-dataframe)
* [Summary Statistics](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#summary-statistics)
* [Bar Charts and Pie Charts](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#bar-charts-and-pie-charts)
* [Calculating Quartiles, Finding Outliers, and Creating a Box Plot]()
* [Creating a Line Plot and a Scatter Plot](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#creating-a-line-plot-and-a-scatter-plot)
* [Calculating Correlation and Regression](https://github.com/dspataru/matplotlib-challenge/blob/main/README.md#calculating-correlation-and-regression)

## Background

This repository contains an analysis used to create a technical report of a clinical study run by Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. The company began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. The complete data from their most recent animal study was provided. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

Tables and figures needed for the technical report of the clinical study, as well as a top-level summary of the study results are captured in this analysis. The project uses two datasets:
1. [Mouse_metadata.csv](https://github.com/dspataru/matplotlib-challenge/blob/main/data/Mouse_metadata.csv) : contains information about the mice that were used in the study, including mouse ID, drug regimen , sex, age in months, and weight (g).
2. [Study_results.csv](https://github.com/dspataru/matplotlib-challenge/blob/main/data/Study_results.csv) : contains the mouse ID, different timepoints in the treatment, tumor volume (mm3), and metastatic sites.

The above two csv files can be found in the data folder of the current repository. Python's pandas library is used to import, merge, and sort the data into dataframes for analysis. The data was cleaned and prepared for analysis by removingany mouse ID with duplicate time points. Summary statistics of the merged dataframe were prepared. Matplotlib is used to visualize the data using bar charts, pie charts, line plots, scatter plots, and box plots. The correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen was calculated and a linear regression model is displayed as well.

The IDE used for this challenge is Jupyter Notebook.

#### Key Words
Jupyter Notebook, Pandas, Python, DataFrames, DataSets, Matplotlib, Statistics

## Study Observations
* Mice that were part of the Capomulin and Ramicane treatment groups showed smaller final tumor volume than the Infubinol and Ceftamin treatment groups.
* There is a strong positive correlation (r = 0.84) between mouse weight and average tumor volume.
Note: the mouse with the duplicate data was dropped because the same timepoints had different tumor volumes and would only introduce noise in the dataset. See the duplicate mouse data below:
![duplicate mouse data](https://github.com/dspataru/matplotlib-challenge/blob/main/images/duplicate_mouse_data.png)

## Merged Dataframe
A left merge was done on the Study_results.csv file with the Mouse_metadata.csv file to produce one complete dataframe with all the information from the study. The first five entries of the merged dataframe are shown below.
![merged dataframe](https://github.com/dspataru/matplotlib-challenge/blob/main/images/merged_df.png)

## Summary Statistics
A summary statistics table was generated to find the mean, median, variance, standard deviation, and SEM of the tumor volume for each regimen. The results were assembled into a single DataFrame.
![summary statistics](https://github.com/dspataru/matplotlib-challenge/blob/main/images/summary_statistics.png)

## Bar Charts and Pie Charts
A comparison between the total number of mice in each drug regimen was plotted in a bar graph to easily visualize which treatments had the most and least number of mice.
![bar chart](https://github.com/dspataru/matplotlib-challenge/blob/main/images/bar_graph.png)

The total number of mice in the study was grouped by Sex (Male or Female), and visualized using a pie graph. The split is 51% males to 49% females.
![pie chart](https://github.com/dspataru/matplotlib-challenge/blob/main/images/pie_plot.png)

## Calculating Quartiles, Finding Outliers, and Creating a Box Plot 
The final tumor volume of each mouse across four of the treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin, were determined by finding the last (greatest) timepoint for each mouse. This dataframe was merged with the original dataframe to get the tumor volumes at the last timepoint. 

The inner quartile range (IQR) and outliers for each of the above treatment regimens were calculated, and box plots were created to visualize the effectiveness of each treatment. 
![box plot](https://github.com/dspataru/matplotlib-challenge/blob/main/images/box_plot.png)

## Creating a Line Plot and a Scatter Plot
A line plot of the tumor volume over the course of the Capomulin treatment for mouse I509 was generated.
![line plot](https://github.com/dspataru/matplotlib-challenge/blob/main/images/line_plot.png)

A scatter plot was chosen to visualize how mouse weight could be related to the average observed tumor volume for the Capomulin regimen.
![scatter plot](https://github.com/dspataru/matplotlib-challenge/blob/main/images/scatter_plot.png)

## Calculating Correlation and Regression
Finally, the correlation coefficient was calculated using the Pearson Correlation Coefficient (R) function from the SciPy library for mouse weight and average observed tumor volume for the entire Capomulin regimen. The R value is: 0.8419363424694721. A linear regression model was plotted along with the scatter plot from the graph above to visually show a linear relationship between the weight of a mouse and the average tumor volume. The linear regression equation is also displayed on the graph shown below.
![linear regression plot](https://github.com/dspataru/matplotlib-challenge/blob/main/images/correlation_regression.png)
