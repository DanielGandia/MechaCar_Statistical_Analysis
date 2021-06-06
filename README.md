# MechaCar_Statistical_Analysis

## Overview of the Analysis:

In this analysis, I will assist the AutoRUs team with the following:

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.

For each statistical analysis, there will be a written summary interpretation of the findings.

## Software and Dataset:

- Software: RStudio 1.4.1106, Visual Studio Code 1.54
- Data Sources: MechaCar_mpg.csv, Suspension_Coil.csv
- Script: MechaCarChallenge.RScript

## Linear Regression to Predict MPG

Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset? The vehicle_length and ground_clearance were the variables to provide non-random amounts of variance to the mpg value.

Is the slope of the linear model considered to be zero? Why or why not? The slope is not considered to be zero because the p-value is 5.35e-11 (refer to the image below). The null hypotheisis is therefore rejected.

Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not? The r-squared value of 0.7149 (shown below) shows that the MechaCar prototype's mpg linear model predicted were effective.

![pvalue_rsquared.png](https://github.com/DanielGandia/MechaCar_Statistical_Analysis/blob/main/Resources/pvalue_rsquared.png)

![linear_regresion.png](https://github.com/DanielGandia/MechaCar_Statistical_Analysis/blob/main/Resources/linear_regresion.png)

## Summary Statistics on Suspension Coils

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.

The current manufacturing data meet this design specification for manufacturing lots 1 and 2 but not for lot 3. The results on the below image show that lots 1 and 2 had variances of .97 and 7.46, while variance for lot 3 is more than 100 at 170.29.

![lot_summary_df.png](https://github.com/DanielGandia/MechaCar_Statistical_Analysis/blob/main/Resources/lot_summary_df.png)

## T-Tests on Suspension Coils

briefly summarize your interpretation and findings for the t-test results. Include screenshots of the t-test to support your summary.

### Summary of all lots:

The results for all lots show there is not enough evidence to reject the null hypothesis. The mean of all three of these manufacturing lots is similar enough to the population mean of 1500.

![t.test_all_lots.png](https://github.com/DanielGandia/MechaCar_Statistical_Analysis/blob/main/Resources/t.test_all_lots.png)

### Lot 1:

According to the results on the below image, there is not statistical diference between the samples. Therefore, there is not enough evidence to reject the null hypothesis.

![t.test_lot1.png](https://github.com/DanielGandia/MechaCar_Statistical_Analysis/blob/main/Resources/t.test_lot1.png)

### Lot 2:

As we saw with Lot 1, the results for Lot 2 do not enough show statistical diference with a p-value of .6072. Therefore, the null hypothesis cannot be rejected.

![t.test_lot2.png](https://github.com/DanielGandia/MechaCar_Statistical_Analysis/blob/main/Resources/t.test_lot2.png)

### Lot 3:

In these results for Lot 3, show the p-value of .04168 which is lower than the significance level of 0.05. The data is considered a skewed distribution and the null hypothesis is therefore rejected.

![t.test_lot3.png](https://github.com/DanielGandia/MechaCar_Statistical_Analysis/blob/main/Resources/t.test_lot3.png)

## Study Design: MechaCar vs Competition

In order to get consumer is lookging for a new car, one of the main factors that peaks their interest is the fuel efficiency. The metric to be test would be MechaCar's fuel efficiency in both city and highway compared to the competition. The Null Hypothesis (H<sub>0</sub>) would be that Mechacar's city and highway mpg is similar to the competition. An Alternative Hypothesis (H<sub>a</sub>) is that MechaCar's average city and highway mpg is statistically better than the competition. The statistical test used for the hypothesis would be the t-test. The data for the statistical test that would be needed is the fuel efficiency (mpg) of MechaCar and that of the competition in order to compare it.
