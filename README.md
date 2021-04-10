# MechaCar_Statistical_Analysis

## Project Overview

This project involves the use of statistics and hypothesis testing to analyze a series of datasets from the automotive industry.
All of the statistical analysis and visualizations is written in the R programming language.

The purpose of this analysis is to offer insights on the MechaCar's production to help the manufacturing team. In order to conduct this analysis, we will be using two datasets containing information related to the miles per gallon and the suspension coils of the MechaCar. We will be using the programming language R and its dplyr library to complete this analysis.


## Resources
- Data source: [MechaCar_mpg](/Resources/MechaCar_mpg.csv) , [Suspension_Coil](/Resources/Suspension_Coil.csv)
- Software : Rstudio

## Summary 

## **1- Deliverable 1**

  ### Linear Regression to Predict MPG
  
In this section, We loaded in the miles per gallon dataset. From there, We preformed a multiple linear regression to see if it could predict the miles per gallon (mpg) dependent variable by using the vehicle length, vehicle weight, spoiler angle, ground clearance, and all wheel drive (AWD) independent variables.

 Also, we will be answering the following questions:

  1- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

  2- Is the slope of the linear model considered to be zero? Why or why not?

  3- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
 
 
 The answers to these questions are:

   1- There were two variables that provided a non-random amount of variance: The vehicle length and the ground_clearance. Both of these have extremely small p-value meaning that they had a high level of significance. It also should be noted that the intercept as had a high level of significance meaning that there are still other factors contributing to the variance of the miles per gallon of the MechaCar.

   2- The slope of the linear model is not considered to be zero. This is because the linear regression shows that some of the independent variables had a significant effect on the dependent variable. If none of the independent variables had an effect on the dependent variable then the linear regression would result in a near zero slope.

   3- The main indicator of whether the linear model predicts the mpg of the MechaCar is the r-squared value. In this case, it is at 0.7149 mean that out of 100 instances, this model would approximately predict the mpg of the MechaCar correctly 71 times. This means We can consider this linear model as fairly efficient to predict mpg of MechaCar prototypes.
   
   Here are the summary results from the linear regression.
   
       mpg = (6.267)vehicle_length + (1.25e-3)vehicle_weight + (6.88e-2)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD + (-1.04e+2)
      
   ![linear_regression](/images/linear_regression.png)

## **2- Deliverable 2**

  ### Summary Statistics on Suspension Coils

In this section, We loaded in the suspension coils dataset. It was comprised of 150 different vehicles ID, 3 different lot numbers, and corresponding PSI levels for each vehicle. From there We created two summary tables to look at the mean, median, variance, and standard deviation of data. The first table looked at of the data as a whole, while the second table looked specific at each of the three different lots that the MechaCars were divided into. Here are the two tables.

                                   **All manufacturing lots**
![lot_summary](/images/lot_summary.PNG)

                                   **By each manufacturing lot**
                                   
![total_summary](/images/total_summary.PNG)


In this section again, We want to answer the following questions:

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

The answer to this question is:

Looking at the total summary, the current variance is approximately 76.23 PSI meaning that is does meet the design specification. When looking at the lots individuals, the first two lotas meet the design specification at a varaince of approximately 1.14 PSI and 10.13 PSI respectfully, but the third lot does not. This is becasue the third lot's variance is approximately 220.01 PSI, exceeding the design specification by more than double the alotted amount. Therefore, the manufacturing team should work with the cars in lots 1 and 2 compared to those in lot 3.

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.
The design specs are respected for all manufacturing lots in total with a global variance of 62.3 psi.
On the lot level, Lot 1 and Lot 2 are into specs with respectively variances of 0.98 and 7.5 psi. The Lot 3 is out of specs with a variance of 170.3 psi.

## **3- Deliverable 3**

## Study Design: MechaCar vs Competition.



