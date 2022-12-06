# UR_2022_Project
---
## Project Overview
The purpose of this project is to get a deep analysis on mental health across America with a focus on anxiety. With the data source we will be using, we will get a better look at the different types of demographics that were included in the analysis. 

## Tools and Databases
### Data Collection
- The data source was collected from the Substance Abuse and Mental Health Data Archive (SAMHDA). The analysis will be using the Client-Level Mental Health Data from the year 2020. It will provide the information of indivduals who have gone to facilities that report to individual state administrative data systems.
- The original data provided uses a code book to show us the information; this will have to be converted for our dataframe.
- This data will be cleaned into a database and the variables will be applied to a Machine Learning model to predict anxiety in indiviuals.

## Preprocessing Data and Machine Learning
### Cleaning the Data
Starting with Jupyter Notebook using pandas, we began by first dropping columns that do not help our analysis:
- Year was dropped for all the data was just 2020
- Education was removed for having over 50% 'missing' or 'not collected'
- Ethnicity had 72% of the data with a majority in 'Not of Hispanic or Latino origin'
- MH1, MH2, and MH3 were each removed for having too much overlap
- Sub (Substance use diagnosis) removed for already being included in SAP (Substance abuse problem)
- Marital status was removed for either being 'never married' or 'missing'
- Employee and Veteran was removed for having over 60% in the 'missing or not collected' category  
- Living Arrangment was either 'private residence' or 'missing'
- State was removed for the machine learning but used in graphing
- All flags that had under 5% were removed

### Machine Learning
Using our cleaned data we applied it to three machine learning models
- Logistic Regression had an accuracy score of 81%
- Random Forest had an accuracy of 75%
- Neural Network had the best results of 83%

Despite the slightly higher accuracy score of the neural network, its resource-intensive nature caused it to run for several minutes per epoch, whereas the logistic regression was completed in less than a single minute. Because of this difference in efficiency, we would recommend the logistic regression model be used for analysis of any further data sets.

## Technology
- Jupyter Notebook using Pandas and Python
- Tableau was used for our visual graphing
- Google slides was used for presenting the project

## Presentation
For the analysis we used Google Slides to clearly show the results of all our data. And we also included all of our visuals to show our results
- Link to [Google Slides](https://docs.google.com/presentation/d/1WQd136a2QlFss3xeQWS823-KZhiiS24vuIKxAbzW2Mk/edit#slide=id.g25f6af9dd6_0_0 "Google's Homepage")
- Link to [Tableau Public](https://public.tableau.com/app/profile/olivia.nayeri/viz/MentalHealthDemographics/MvsFbarchart_1#1)
---
