# MechaCar_Statistical_Analysis
Using R to perform statistical analysis on MechaCars prototypes


## Overview

AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called the data analytics team to review the production data for insights that may help the manufacturing team. In this analysis we performed the following:

• Multiple linear regression analysis that identified which variables in the dataset predict the mpg of MechaCar prototypes

• Collected summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots

• Run t-tests to determine if the manufacturing lots are statistically different from the mean population

• Designed a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.

### Linear Regression to Predict MPG

To determine which variables/coefficients provided a non-random amount of variance to the mpg values we look at the individual variable p-values Pr(>|t|). We determined that vehicle length and ground clearance variables provide a significant non-random amount to the linear model with variance of 2.60 and 5.21.

Since the p-value of our linear regression analysis is 5.35, which is much smaller than assumed significance level of 0.05%. Therefore, the null hypothesis can be rejected as slope of our linear model is not zero.

Correlation between two variables in this linear regression is high, with R-squared value of 0.71 and significant p-value of 5.35 along with non-random amount of vehicle length and ground clearance variables it predicts mpg of MechaCar prototypes effectively.


![LinearRegMPG](https://github.com/rloufoster/MechaCar_Statistical_Analysis/blob/main/Images/LinearReg_MPG.png?raw=true)


### Summary Statistics of Suspension Coils

The MechaCar dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots.
Using R we created a summary statistics table to show: The suspension coil’s PSI continuous variable across all manufacturing lots, mean, median, variance, and standard deviation of PSI metrics for each lot.

Our summary statistics table shows us that variance of the suspension coils across all manufacturing lots meet design specification with variance of 62.29356 which does not exceed 100 pounds per square inch.

![]()

 Summary statistics table shows us that Lot1 and Lot2 meet design specification with variance of 0.9795918 and 7.4693878. However, Lot3 significantly exceeds design satisfaction with variance of 170.2861224. Across total summary and individual lots summary mean and median stay fairly close.  
 
![LotSummary](https://github.com/rloufoster/MechaCar_Statistical_Analysis/blob/main/Images/Lot_summary.png?raw=true)


### T-Tests on Suspension Coils

We performed four t test for our Suspension Coils data to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch. By performing the t.test()on our data it produced test statistic "t" along with p-value. Assuming that significance level was the common 0.05 percent, our p-value = 0.06028. which is above significance level. Therefore, we do not have sufficient evidence to reject the null hypothesis according to this specific t test.

![SummaryT](https://github.com/rloufoster/MechaCar_Statistical_Analysis/blob/main/Images/Summary_TTest.png?raw=true)

Similarly, Manufacturing Lots 1 and 2 are above significance level with p-value of 1 and 0.6072

![Lot1T](https://github.com/rloufoster/MechaCar_Statistical_Analysis/blob/main/Images/Lot1_TTest.png?raw=true)


![Lot2T](https://github.com/rloufoster/MechaCar_Statistical_Analysis/blob/main/Images/Lot2_TTest.png?raw=true)

Lot 3 Manufacturing T-Test showed low significance level of p-value of 0.04168, which is enough to reject the null hypothesis.

![Lot3T](https://github.com/rloufoster/MechaCar_Statistical_Analysis/blob/main/Images/Lot3_TTest.png?raw=true)


### Study Design:  MechaCar vs. Competition

This study would involve collecting data on MechaCar and its comparable models across several different manufacturers over the last 3 years.

**Metrics to Test:**

There is a wide range of metrics that will be of interest to a consumer, such as:

   *Safety Feature Rating
   *Current Price (Selling)
   *Drive Package
   *Engine (Electric, Hybrid, Gasoline / Conventional)
   *Resale Value
   *Average Annual Cost of ownership (Maintenance)
   *MPG (Gasoline Efficiency)
   

**Statistical Hypothesis**

There are two types of statistical hypotheses to consider: 
• The null hypothesis(Ho): MechaCar is priced correctly based on its performance of key factors for its market category.  
• The alternate hypothesis(Ha): MechaCar is not priced correctly based on performance of key factors for its market category.

**Type of Statistical Test**

A multiple linear regression would be used to determine the factors that have the highest correlation/predictability with the list selling price (dependent variable); which combination has the greatest impact on price (it may be all of them!)
   

   
   









 
 
 
 
 
 