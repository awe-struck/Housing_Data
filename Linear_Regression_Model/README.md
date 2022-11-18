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

## Hypothesis Test: Is there a difference in Market Value for Occupied vs Not Occupied Units?


Hypothesis testing was done against the Null Hypothesis that there is no difference in Market Value for Occupied vs Not Occupied Units. The hypothesis tests revealed that 2005 and 2011 years had a statistically significant result. They had a t-stat of 2.04 and 6.40 with t* being +/-1.960049374 and +/-1.959991878 respectively. Since t-stat > t*, they both fell in the rejection region when compared to their 2-tailed t* scores. Thus, we reject null where there is no difference in market values for occupied vs not occupied. From this result, there is a difference in Market Values in the years 2005 and 2011.


![image](https://user-images.githubusercontent.com/115379520/202617125-52505851-85d2-4cc0-821e-8519f86e0097.png)

![image](https://user-images.githubusercontent.com/115379520/202617141-81102600-a034-43c4-af4d-319ec12a2b69.png)

![image](https://user-images.githubusercontent.com/115379520/202617158-22a8627c-39a5-41ba-9bdd-3ea7b05d41b1.png)

![image](https://user-images.githubusercontent.com/115379520/202617175-9ecf7193-bec1-41ff-91b8-b1ddb1f64f68.png)

![image](https://user-images.githubusercontent.com/115379520/202617191-9dee0501-8b20-4267-bee7-9c1c92534534.png)


<br />

When testing for Null Hypothesis that Occupied units are greater than or equal to Not Occupied Units. None of the years were statistically significant, so the there is not enough evidence to reject the Null. Thus, on average the Occupied Units are greater than or equal to Not Occupied units in terms of Market Value.

![image](https://user-images.githubusercontent.com/115379520/202633246-88dac704-7e2e-4e65-9c2d-4bc50a8a761b.png)


<br />


When testing for Null Hypothesis that Occupied units are less than or equal to Not Occupied Units. The years 2005 and 2011 were statistically significant. Thus, on average the Occupied Units for 2005 and 2011 were greater than Not Occupied units in terms of Market Value.


![image](https://user-images.githubusercontent.com/115379520/202633470-a1a66fe1-edc5-4173-a9d0-8c54f7275610.png)

<br />


From these hypothesis tests, there is a a general pattern with the Market Values. On average, the Market Value for Occupied Units was always greater than or equal to Not Occupied units. It was greater in 2005 and 2011 while equal in all other years. As shown below, both STATUS labels are roughly equal in terms of average Market Value except in 2005 and 2011. This of course coincides with the results done by hypthesis testing.


![image](https://user-images.githubusercontent.com/115379520/202633495-756bd8a0-d74a-4f4e-8a31-3b2254006e5c.png)

<br />


## Summary


1.) Through hypothesis testing againsit the Null, the results reject it for the years 2005 and 20011 and show a difference in Occupied vs Not Occupied Market Values

2.) All market values for Occupied units are greater than or equal to Not Occupied units

3.) Occupied values greater than Not occupied in 2005 and 2011 and equal in all other years
