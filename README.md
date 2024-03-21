# Analysis of Congestive Heart Failure and its Relationship to Socioeconomic Status and Urbanization Level


## Introduction

In this project, I analyzed county-level data from various sources, including the CDC's WONDER database, U.S. Census Bureau, Feeding America, and the U.S. Department of Agriculture. The purpose of this project is to answer the following question: Is there a relationship between the congestive heart failure crude mortality rate and socioeconomic factors (median household income, food insecurity, etc.) and urbanization level of a county?
 

## Data

The data used in this project comes directly from these sources: 
* [CDC WONDER](https://wonder.cdc.gov/)
* [U.S. Census Bureau](https://www.census.gov/data/datasets/2014/demo/saipe/2014-state-and-county.html)
* [Feeding America](https://www.feedingamerica.org/research/map-the-meal-gap/by-county)
* [U.S. Department of Agriculture](https://www.ers.usda.gov/data-products/county-level-data-sets/county-level-data-sets-download-data/)

#### Congestive Heart Failure (CHF) Crude Mortality Rate 

The response variable (CHF crude mortality rate) is measured as follows: Number of CHF-related deaths per 100,000 population per year (in a given county).

#### Variables of Interest

* **Median Household Income** : The median household income in a county.

* **Education Level** : There are two different variables related to education level:
  * Percentage of people with a Bachelor’s degree or higher
  * Percentage of people who have less than a high school diploma

* **Poverty** : Percentage of people in a county who are living in poverty.

* **Food Insecurity** : Percentage of people facing food insecurity in a county.

* **Urbanization Level** : I used the Rural Urban Continuum to represent urbanization level. Counties are ranked on a scale of 1-9, where 1 = most urban and 9 = most rural.


## Research Questions

* **What is the effect of socioeconomic status on congestive heart failure?** : I.e., do counties with (higher income levels, higher education levels, less poverty, and lower rates of food insecurity) have better outcomes than counties with (lower income levels, lower education levels, higher rates of poverty, and higher rates of food insecurity)?
* **What is the effect of urbanization on congestive heart failure?** : Do urban or rural communities have a higher mortality rate for Congestive Heart Failure? 


## Data Visualization

### Median Household Income vs. Crude Mortality Rate 

  <img width="600" height="400" src="Plots\Income_Plot.png">


As the plot above shows, there is a negative relationship between median household income and crude mortality rate. Counties with a higher median household income generally have a lower crude mortality rate than counties with a low median household income. This means that people from low-income areas are more likely to die from congestive heart failure.


### Food Insecurity vs. Crude Mortality Rate

  <img width="600" height="400" src="Plots\Food_Insecurity_Plot.png">


There is a weak positive relationship between food insecurity and crude mortality rate. Counties with a high rate of food insecurity generally have a higher crude mortality rate than counties with a low rate of food insecurity. This means that people facing food insecurity are more likely to die from congestive heart failure.

### Poverty vs. Crude Mortality Rate 

  <img width="600" height="400" src="Plots\poverty_plot.png">


There is a weak positive relationship between poverty and crude mortality rate. Counties with a high rate of poverty generally have a higher crude mortality rate than counties with a low rate of poverty. This means that people living in poverty-stricken areas are more likely to die from congestive heart failure. 

### Education Level vs. Crude Mortality Rate

  <img width="600" height="400" src="Plots\Bachelors_Plot.png"><img width="600" height="400" src="Plots\HS_Plot.png">

There is a negative relationship between education level and crude mortality rate. Counties with a high percentage of people with a Bachelor’s degree or higher generally have a lower crude mortality rate, and counties with a high percentage of people without a high school diploma have a higher crude mortality rate. This means that people living in more educated counties are less likely to die from congestive heart failure.


### Urbanization Level vs. Crude Mortality Rate 

  <img width="600" height="400" src="Plots\Urbanization_Plot.png">

There is clearly a large difference in the crude mortality rate for urban and rural areas. Counties with an urban population < 5,000 (not adjacent to a metro area) had nearly double the crude mortality rate of counties in metro areas with more than 1,000,000 residents. This means that residents of rural counties are nearly twice as likely to die from congestive heart failure.

  
## Linear Regression Model


Based on this model: 

* Median household income has the greatest impact (negative) on a county’s crude mortality rate.
* Poverty has a significant positive effect on a county's crude mortality rate.
* Urbanization and education level have a significant negative effect on a county's crude mortality rate.
* Food insecurity has a smaller, but still significant effect (positive) on a county's crude mortality rate.



## Final Thoughts

Socioeconomic status and urbanization level both have a measurable impact on a county's CHF crude mortality rate. Although they are not the obvious heart disease risk factors (such as smoking, obesity, etc.), socioeconomic factors and urbanization level of a county can also lead to individuals having a higher risk of dying due to congestive heart failure. 
