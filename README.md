# MechaCar_Statistical_Analysis

Module 15 - R and Statistics

## Linear Regression to Predict MPG

The mecha_mpg.csv contained data from 50 cars. the metrics included vehicle length, vehicle weight, spoiler angle, ground clearance and MPG


![Statistical Analysis](https://github.com/hmohabir/MechaCar_Statistical_Analysis/blob/main/1Linear%20regression.PNG)

We can see here in the linear model the metrics used and their general coefficients.

![Statistical Summary](https://github.com/hmohabir/MechaCar_Statistical_Analysis/blob/main/2Summary.PNG)

In addition, the summary provises some interesting information:

Vehicle length, and vehicle ground clearance are statistically likely to provide non-random amounts of variance to the model. As such, these have s significant impact on the MPG for MechaCar. On the other hand, vehicle weight, spoiler angle, and All Wheel Drive (AWD) have p-Values that shows a random amount of variance with the dataset.

The p-Value for this model is 5.35e-11, is much smaller than the assumed significance level of 0.05%. This shows that there is enough evidence to reject our null hypothesis, which additionally indcates that the slope of this linear model is not zero.

The linear model shows an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. As such, this  regression model can effectively predict MPG of MechaCar.

If we go a step further and remove the variables that creat less impact (vehicle weight, spoiler angle, and All Wheel Drive), the prediction does decrease, but not significantly.

![Removing independent variables](https://github.com/hmohabir/MechaCar_Statistical_Analysis/blob/main/3%20Remove%20independent%20variables.PNG)

Here, we can see that the r-squared valie drops from 0.7149 to 0.674. This is not enough to make a significant difference in predictability.


## Summary Statistics on Suspension Coils

The Suspension Coil dataset provided for the MechaCar contains the result of testing the weight capacities of multiple suspension coils from different lots to determine consistency.

![Total Summary](https://github.com/hmohabir/MechaCar_Statistical_Analysis/blob/main/4%20Total%20Summary.PNG)

Here we can see that suspension coil's continuous variable across all manufacturing lots, with a variance PSI of 62.28, well within the 100 pounds per square inch. Now, we dive a little deeper into the various manufacturing lots:

![Lot Summary](https://github.com/hmohabir/MechaCar_Statistical_Analysis/blob/main/5%20Lot%20summary.PNG)

We see the variance of 0.09 and 7.47 for lots 1 and 2 respectively - well within the design specification. However, lot 3 has a variance of 170.3. This lot is responsible for the higher varience in the whole lot level.

To illustrate the varience a little more, I will use boxplots:

![Lot Summary](https://github.com/hmohabir/MechaCar_Statistical_Analysis/blob/main/6%20All%20lots%20ggplot.PNG)

The variance might not seem to be out of range at all, when taken together. However, when they are separated, the difference is stark with lot 3:

![Individual Lot Summary](https://github.com/hmohabir/MechaCar_Statistical_Analysis/blob/main/7%20Individual%20lots%20ggplot.PNG)

The variance in performance in performance and consistency is much larger in lot 3. It is also beyond the design specification.

## T-Tests on Suspension Coils

![Overall t-test](https://github.com/hmohabir/MechaCar_Statistical_Analysis/blob/main/8%20t-test%201500PSI.PNG)

We can see the mean of sampling the lots together is 1498.8 with a p-value of 0.06, which is higher than the common significance of 0.05. As such, there is not enough evidence to support a rejection of the null hypothesis. Therefore, the mean of the three lots is ststistically similar to the given mean of 1500 PSI.

However, if we are to look at them individually:

![Overall t-test](https://github.com/hmohabir/MechaCar_Statistical_Analysis/blob/main/9%20Individual%20t-test%201500PSI.PNG)

Lot 1 has a true mean of 1500 PSY with a p-value of 1. As such, the null hypothesis can be accepted since there is no statistical difference between the observed mean and the given meam.

Lot 2 is similar to Lot 1 both with regards to the actual mean and its p-value. Hence the null hypothesis can also be accepted.

Lot 3, on the other hand has a mean of 1496.14 and a p-value of 0.04. Since this p-value is lower than the accepted significance of 0.05, the null hypothesis is rejected and the presumed mean is not statistically different.

The above data shows that something is definitely wrong with lot 3 production.


## Study Design: MechaCar vs Competition

Such a study would involve collecting data on MechaCar and its competition over a period of about three years.

### Metrics
Collecting data would involve the following metrics:

*  Safety Feature Rating: **Independent Variable**
*  Current Price (Selling): **Dependent Variable**
*  Drive Package : **Independent Variable**
*  Engine (Electric, Hybrid, Gasoline / Conventional): **Independent Variable**
*  Resale Value: **Independent Variable**
*  Average Annual Cost of ownership (Maintenance): **Independent Variable**
*  MPG (Gasoline Efficiency): **Independent Variable**

### Null and Alternative Hypothesis

When it is determined which factors are key to the MechaCar's classification, the followingcan be furhter investigated:

Null Hypothesis - MechaCar is properly priced by virtue of its performance of the main factors in its clasification.
Alternative Hypothesis - MechaCar is not properly priced by virtue of its performance of the main factors in its clasification.

### Statistical tests

A multiple linear regression would be used to determine the dependent variavles havinf the highest correlation/predictability with the list selling price. 
Also, which combination has the greatest impact on price (it may be all of them!)

### Data of Statistical test

The data would show which factors habe a mean that is closest or actual to MechaCar's mean and their p-value, which will show if the null hypothesis can be accepted or rejected.
