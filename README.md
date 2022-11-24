# UR_2022_Project
---
## Project Overview
The purpose of this project is to get a deep analysis on mental health across America with a focus on anxiety. With the data source we will be using, we will get a better look at the different types of demographics that were included in the analysis. 

## Tools and Databases
### Data Collection
- The data source was collected from the Substance Abuse and Mental Health Data Archive (SAMHDA). The analysis will be using the Client-Level Mental Health Data from the year 2020. It will provide the information of indivduals who have gone to facilities that report to individual state administrative data systems.
- The original data provided uses a code book to show us the information; this will have to be converted for our dataframe.
- This data will be cleaned and consolidated into a database and the variables will be applied to a Machine Learning model to predict anxiety in indiviuals.

## Prprocessing Data and Machine Learning
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
- 
---
