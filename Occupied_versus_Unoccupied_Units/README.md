# Difference in Market Value for Occupied vs Not Occupied housing units.

## Introduction

The purpose of this project is to test the hypothesis of whether there is a difference in in Market Value of Housing units for occupied vs non-occupied units? Furthermore, I will see if there is a pattern in these differences over the period 2005 through 2013?

![image](https://user-images.githubusercontent.com/115379520/202359938-85903106-e42a-44d9-8f94-7bacc9d9640d.png)


<br />

## Dataset Information

The data from this project comes the "Housing Affordability Data System” of the U.S. Department of Housing and Urban Development. (HADS). This HADS contains Housing unit level datasets and aims to study housing affordability relative to Median income,
Poverty level income, and Fair market rent. The datsets are based on American Housing Survey (AHS) national files from 1985 onwards. These datasets are made available every two years to the public by the US department of housing and urban development.
For this project, I used the national data from 2005, 2007, 2009, 2011 and 2013. 

- Link to dataset source [URL](https://www.huduser.gov/portal/datasets/hads/hads.html)

Several of the variables were dropped with only the relevenat variables being kept for the analysis. Below is a link to the word document containing the used variables


<br />

## Cleaning


In this stage, I removed all 'missing' or 'suspect' data which included housing units with either negative or very 'low' Market Values. With that in mind, 
I used conditional formatting to highlight, filter  and remove  units that were less than $1000 in Market Value. Following that, I isolated each year 
for the VALUE column and filtered the units for STATUS (whether unit is 'Occupied' or 'Vacant'). For the years of 2005, 2007, 2009, 2011 and 2013 
there were 30514, 27785, 31317, 85050, and 36675 units deleted respectivley. 


<br />

## Descriptive Statistics for VALUE (Occupied vs Not Occupied)

Here is a brief overview of key statistics for the VALUE variable for Occupied vs Not Occupied housing units from 2005-2013.

![image](https://user-images.githubusercontent.com/115379520/202360623-4621a4ce-3f06-4283-bc8f-9cdb13048759.png)






3.) hypothesis tests throughout the years

To test the hypothesis, I used a difference in means hypothesis test across the two sets of values(Occupied vs Not Occupied)
Here is the result of the tests done on each year:

Screenshot tests below:



According to the test, 2005 and 2011 were the only years that had the market value of housing units statistically different across the occupied and unoccupied units. Theese two years had a t-stat of 2.04 and 6.40 and in a compated to the 2 tailed t*, they both fall in the rejection regions. 2005  -1.960049374 and +1.960049374, 2011 -1.959991878 and +1.959991878
So we reject null where there is no difference in market values for occupied vs not occupied.


year	t-stat 	t* (1 tail)
2005	2.03791929	-1.644903568
2007	-1.12428212	-1.644908474
2009	-0.193604738	-1.644902288
2011	6.396999818	-1.644871544
2013	-0.259914481	-1.644895178


Now I test if the units Occupied is greater than or equal to units not occupied. The t-stats are not in the rejection region
Since none are statistically significant. We do not reject the null. Thus, none of the years of occupied are less than not occupied




NOw i test if ocupied less rthan or equal to units not occupied
2005	2.03791929	1.644903568
2007	-1.12428212	1.644908474
2009	-0.193604738	1.644902288
2011	6.396999818	1.644871544
2013	-0.259914481	1.644895178

2005 and 2011 fall in the rejection regions so we reject null and say than 2005 and 2011 were greater in market value for occupeid vs non occupied.

Plotting the average value for each year against status, we can see the 2005 and 2011 both are greater for occupeid units



Summary:

Looking at all the hypothesis tests run we can conclude that for 2-tail: 

1.) There is a difference in Occupied vs Not Occupied market Values in: 2005 and 2011
2.) All market values for Occupied units are greater than or equal to Not Occupied units (abides by the Null). In other words, none of the Occupied are less than the Not occupied
3.) Occupied values greater than non occupied in 2005 and 2011

The market value of occupied units is never less than that for unoccupied units across all years.
The market value of occupied units is greater than that for unoccupied units across some years.


Are there differences in Market Value means between Occupied vs Not Occupied Units through 2005-2013?

Through hypothesis testing, it was concluded that difference in market value was significant in  the years 2005 and 2011.

For the remaining years, there was no significant difference in market value in Occupied vs Not Occupied units

Do these diffrences have a pattern over the period of 2005 - 2013?

The pattern from this dataset was that the Occupied Market Value Units was always greater than or equal to the Not Occupied Units. It was greater in 2005 and 2011 while equal in all other years. In short, the Occupied Market Value Units were never less than the Not Occupied units

