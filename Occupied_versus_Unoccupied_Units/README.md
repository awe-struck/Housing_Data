# Difference in Market Value for Occupied vs Not Occupied housing units.

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

When testing for Null Hypothesis that Occupied units are greater than or equal

Now I test if the units Occupied is greater than or equal to units not occupied. The t-stats are not in the rejection region
Since none are statistically significant. We do not reject the null. Thus, none of the years of occupied are less than not occupied

![image](https://user-images.githubusercontent.com/115379520/202633246-88dac704-7e2e-4e65-9c2d-4bc50a8a761b.png)


<br />

NOw i test if ocupied less rthan or equal to units not occupied
2005	2.03791929	1.644903568
2007	-1.12428212	1.644908474
2009	-0.193604738	1.644902288
2011	6.396999818	1.644871544
2013	-0.259914481	1.644895178

![image](https://user-images.githubusercontent.com/115379520/202633470-a1a66fe1-edc5-4173-a9d0-8c54f7275610.png)


2005 and 2011 fall in the rejection regions so we reject null and say than 2005 and 2011 were greater in market value for occupeid vs non occupied.

Plotting the average value for each year against status, we can see the 2005 and 2011 both are greater for occupeid units



![image](https://user-images.githubusercontent.com/115379520/202633495-756bd8a0-d74a-4f4e-8a31-3b2254006e5c.png)




## Summary


1.) There is a difference in Occupied vs Not Occupied Market Values in 2005 and 2011
2.) All market values for Occupied units are greater than or equal to Not Occupied units (abides by the Null). In other words, none of the Occupied are less than the Not occupied
3.) Occupied values greater than non occupied in 2005 and 2011

The market value of occupied units is never less than that for unoccupied units across all years.
The market value of occupied units is greater than that for unoccupied units across some years.


Are there differences in Market Value means between Occupied vs Not Occupied Units through 2005-2013?

Through hypothesis testing, it was concluded that difference in market value was significant in  the years 2005 and 2011.

For the remaining years, there was no significant difference in market value in Occupied vs Not Occupied units

Do these diffrences have a pattern over the period of 2005 - 2013?

The pattern from this dataset was that the Occupied Market Value Units was always greater than or equal to the Not Occupied Units. It was greater in 2005 and 2011 while equal in all other years. In short, the Occupied Market Value Units were never less than the Not Occupied units

