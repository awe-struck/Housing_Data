# Difference in Market Value for Occupied vs Not Occupied Housing Units.

## Introduction

The purpose of this project is to test the hypothesis of whether there is a difference in in Market Value of Housing units for occupied vs non-occupied units? Furthermore, I will see if there is a pattern in these differences over the period 2005 through 2013?. Details of the project can be found in the [excel file.](https://github.com/awe-struck/Housing_Data/blob/main/Occupied_versus_Unoccupied_Units/Market%20Value%20of%20Occupied%20vs%20Not-Occupied%20Units.xlsx)

![image](https://user-images.githubusercontent.com/115379520/202359938-85903106-e42a-44d9-8f94-7bacc9d9640d.png)


<br />

## Dataset Information

The data from this project comes the "Housing Affordability Data System” of the U.S. Department of Housing and Urban Development. (HADS). This HADS contains Housing unit level datasets and aims to study housing affordability relative to Median income,
Poverty level income, and Fair market rent. The datsets are based on American Housing Survey (AHS) national files from 1985 onwards. These datasets are made available every two years to the public by the US department of housing and urban development.
For this project, I used the national data from 2005, 2007, 2009, 2011 and 2013. 

- Link to dataset source [URL](https://www.huduser.gov/portal/datasets/hads/hads.html)


<br />

## Cleaning


In this stage, I removed all 'missing' or 'suspect' data which included housing units with either negative or very 'low' Market Values. With that in mind, 
I used conditional formatting to highlight, filter  and remove  units that were less than $1000 in Market Value. Following that, I isolated each year 
for the VALUE column and filtered the units for STATUS (whether unit is 'Occupied' or 'Vacant'). For the years of 2005, 2007, 2009, 2011 and 2013 
there were 30514, 27785, 31317, 85050, and 36675 units deleted respectively. 

Several of the variables were derivatives of other variables or irrelevant to the analysis. Thus, variables were dropped with only the relevenat variables being kept for the analysis. 

- Link to [variables](https://github.com/awe-struck/Housing_Data/blob/main/Occupied_versus_Unoccupied_Units/Variables%20List.docx)

<br />

## Descriptive Statistics for VALUE (Occupied vs Not Occupied)

Here is a brief overview of key descriptive statistics for the VALUE variable for Occupied vs Not Occupied housing units from 2005-2013.

![image](https://user-images.githubusercontent.com/115379520/202360623-4621a4ce-3f06-4283-bc8f-9cdb13048759.png)

<br />

Here are the distributions of VALUES (Occupied vs Not Occupied). The distributions show a right skew.

![image](https://user-images.githubusercontent.com/115379520/202616759-7e37f418-feb8-4b74-94a4-b8c6bf745744.png)

![image](https://user-images.githubusercontent.com/115379520/202616838-bb750ca9-d460-487e-aedb-7a47b2f1e8a0.png)

![image](https://user-images.githubusercontent.com/115379520/202616866-391b29f9-8622-474e-9221-7b62d2b2ebdf.png)

![image](https://user-images.githubusercontent.com/115379520/202616894-4120246c-346a-45b8-be11-ae30d6433135.png)

![image](https://user-images.githubusercontent.com/115379520/202616926-86da8b3e-b13a-46e8-b0b0-a76ce2c10687.png)


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


