# Company Absenteeism Analysis

**From a business prespective, this project will address absenteeism at a company during work time.**

## Background

The problem is that the business envionment of today is more competitive than it used to be. This leads to increased pressure in the workplace. 
Therefore, it is reasonable to expect that unachievable business goals and an elevated risk of unemployment can raise people's stress levels.
Often the continuous presence of such factors becomes detrimental to a person's health. Sometimes this may result in minor illness which of course is not desired.
However, it may happen that the employee develops a longterm condition. 

An example is being depression. That being said, since we will be solving the problem form the point of view fo the person in charge of productivity in the company, 
we will not focus on that facet of the problem. Rather we will look at predicting absenteeism from work. More precisely, we would like to know whether or not an employeen can be
expected to be missing for a sepcific number of hours in a given work day.

Having such information in advance can improve our decision making by re-organizing the work process in a way that will allow us 
to avoid a lack of productivity and increase the quality of work generated in our firm.

### Definition of the absenteeism
Absence from work during normal working hours, resulting in temporary iincapacity to execute regular working activity

### Purpose of the project
This business analysis is expected to ba away from work at some point in time or not. In other words, we want to know for 
how many working hours an employee could be away from work based on information such as **how far they live from their workplace, how many children and pets they have,
do they have higher education**, and so on.

## Data Preparation
[DataPreprocessing.ipynb](https://gitlab.com/futongli/company-absenteeism-analysis/-/blob/master/ModelPreparation/DataPreprocessing.ipynb) is used for data cleaning and data reassembling.
1. Spliting the categorical variable into multiple dummy variables and re-group them neatly. 
2. Converting data of columns to desired data type and extracting useful information.
3. Mapping a bunch of categories into binary data.
4. Reorder the columns in a meaningful way.

## Logistic Regression Model
[LogRegModel.ipynb](https://gitlab.com/futongli/company-absenteeism-analysis/-/blob/master/ModelPreparation/LogRegModel.ipynb) contains the steps of creating the logistic regression model.
1. Using the median as the cut-off for the target.
2. Creating a "CustomScaler" to standardize the selected inputs, then train and test the logistic regression model by spliting the whole Features and labels into two sets.
3. Pickle the model and the scaler for assembling the Prediction Module.

## Deploying the Module
[DeployingAbsenteeisnModule.ipynb](https://gitlab.com/futongli/company-absenteeism-analysis/-/blob/master/Module/DeployingAbsenteeisnModule.ipynb) the [module](https://gitlab.com/futongli/company-absenteeism-analysis/-/blob/master/Module/absenteeism_module.py), 
and store the result of prediction in to a .csv file.

