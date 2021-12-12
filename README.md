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

To illistrate the varience a little more, I will use boxplots:

![Lot Summary](https://github.com/hmohabir/MechaCar_Statistical_Analysis/blob/main/6%20All%20lots%20ggplot.PNG)

The variance might not seem to be out of range at all, when taken together. However, when they are separated, the difference is stark with lot 3:

![Individual Lot Summary](https://github.com/hmohabir/MechaCar_Statistical_Analysis/blob/main/7%20Individual%20lots%20ggplot.PNG)

The variance in performance in performance and consistency is much larger in lot 3. It is also beyond the design specification.



