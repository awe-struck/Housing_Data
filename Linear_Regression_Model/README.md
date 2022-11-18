# Linear Regression Model for Market Value of Single Family Housing Units in 2013 

## Introduction

The purpose of this project is to create a model to check which variables contribute to the Market Value of single family units.
Details of the project can be found in the [excel file.](https://github.com/awe-struck/Housing_Data/blob/main/Linear_Regression_Model/Linear%20Regression%20Model.xlsx)

Ln(VALUE) = β0 + β1AGE1 + β2METRO + β3Northeast  + β4Midwest + β5South + β6Ln(LMED) + β7Ln(FMR) + β8BEDRMS + β9BUILT + β10ROOMS + β11PER + β12Ln(ZINC2) + β13Adequate + β14Ln(UTILITY) + β15Ln(OTHERCOST)


<br />

## Dataset Information

The data from this project comes the "Housing Affordability Data System” of the U.S. Department of Housing and Urban Development. (HADS). This HADS contains Housing unit level datasets and aims to study housing affordability relative to Median income, Poverty level income, and Fair market rent. The datsets are based on American Housing Survey (AHS) national files from 1985 onwards. These datasets are made available every two years to the public by the US department of housing and urban development. For this project, I used the national data from 2013. 

- Link to dataset source [URL](https://www.huduser.gov/portal/datasets/hads/hads.html)


<br />

## Cleaning


In this stage, I removed all 'missing' or 'suspect' data which included housing units with either negative or very 'low' Market Values. With that in mind, 
I used conditional formatting to highlight, filter  and remove  units that were less than $1000 in Market Value. Following that, I isolated each year 
for the VALUE column and filtered the units for STATUS (whether unit is 'Occupied' or 'Vacant'). For the year 2013, there was 36675 units deleted respectively. 


![image](https://user-images.githubusercontent.com/115379520/202646011-a74fc8d3-58fb-4b57-a417-50c521d6438a.png)

<br />

Several of the variables were derivatives of other variables or irrelevant to the analysis. Thus, variables were dropped with only the relevenat variables being kept for the analysis. Below is a variable changelog which provides a brief explanation as to why certain variables were removed.

![image](https://user-images.githubusercontent.com/115379520/202646305-afee42b5-c7e3-42b4-9769-397bd755a938.png)

<br />

- Link to initial [variables](https://github.com/awe-struck/Housing_Data/blob/main/Occupied_versus_Unoccupied_Units/Variables%20List.docx)



<br />

## Descriptive Statistics for VALUE (Occupied vs Not Occupied)

Here is a brief overview of key descriptive statistics for the VALUE variable for Single Family Housing Units from 2013

![image](https://user-images.githubusercontent.com/115379520/202650136-cccf6bd7-e97d-403a-89f5-3a9823965fb2.png)

<br />

Here are the distributions of VALUE vs Log Transformed Value. The former distributions show a right skew while the latter has a standard bell curve shape.

![image](https://user-images.githubusercontent.com/115379520/202650288-ebddb73d-6312-4f8b-8a14-f91db3ac8ef7.png)

![image](https://user-images.githubusercontent.com/115379520/202650350-7d723d79-31f3-42ad-b986-24e4677e41b4.png)



<br />

## Regression Models


There were three linear regression models created: no transformatins, Log Transformed VALUE variable and Log Transformed Value and 'X' variables.
Out of the three model variations created, the one with log transformed 'X' and VALUE variables provided the best results. Looking at the adjusted R squared there are 0.409944542, 0.496683194 and 0.527696099 respectively. This adjusted R squared shows how much of the variation can be explained by the model. With the last model having 52.77% of the variation being explained by the variables present.




![image](https://user-images.githubusercontent.com/115379520/202651915-d493d8b0-1f7b-4b0c-8cfd-12c603915739.png)

![image](https://user-images.githubusercontent.com/115379520/202651990-71bbf16a-a3f3-4ffa-838e-fb4ba07277a9.png)

![image](https://user-images.githubusercontent.com/115379520/202652036-3cd0e1fb-c090-45f4-9c12-137ac0c8d88f.png)

<br />

Here is a brief intrepretion the variables used in the model

![image](https://user-images.githubusercontent.com/115379520/202651101-928e1b88-2919-45c3-8ab9-83091e9b6550.png)



<br />


## Summary

Out of the three models crated, the one with Log transformations on both Y and X variables yielded the best results with 52.77% of the variation in the model being explained by the variables.
