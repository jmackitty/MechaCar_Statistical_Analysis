# MechaCar_Statistical_Analysis


## Linear Regression to Predict MPG
The results of the linear regression show that  vehicle_length, vehicle_weight, and ground_clearance all have r-squared values less than, 0.05%, so the null hypothesis can be rejected for these factors.
Vehicle_weight is close to the r-squared value so we can take a closer look there. The spoiler_angle and AWD are greater than 0.05% so these suppport the null hypothesis, which means these do not predict the mpg for the prototypes. 

"C:\Users\jemnj\RUT-VIRT-DATA-PT-03-2022-U-B\MechaCar_Statistical_Analysis\Deliverable_1_script.png"
"C:\Users\jemnj\RUT-VIRT-DATA-PT-03-2022-U-B\MechaCar_Statistical_Analysis\Deliverable_1_scriptsummary.png"

## Summary Statistics on Suspension Coils

In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. 
When reviewing the entire manufacturinng lot, the manufacturing data meets the design specification because the variance of the coils is 62.29 PSI, which is well within the 100 PSI variance requirement.

Lots 1 and Lot 2 are within the 100 PSI variance requirement of 0.97 and 7.49. Lot 3 is showing a much larger variance  of 170.29, so lot 3 does not meet this design specification.

"C:\Users\jemnj\RUT-VIRT-DATA-PT-03-2022-U-B\MechaCar_Statistical_Analysis\Deliverable_2_script.png"
"C:\Users\jemnj\RUT-VIRT-DATA-PT-03-2022-U-B\MechaCar_Statistical_Analysis\Deliverable_2_lot_summary.png"
"C:\Users\jemnj\RUT-VIRT-DATA-PT-03-2022-U-B\MechaCar_Statistical_Analysis\Deliverable_2_total_summary.png"

## T-Tests on Suspension Coils
In this dataset we performed t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

The t-test analysis for all manufacturing lots shows that the true mean of the sample is 1498.78 and a p-value of 0.06. This is higher than the common signifigance level of 0.05.

Lot 1 had a t-test result 0 of and Lot 2 had a t-test result of 0.51745. Lot 1 and Lot 2 are not statistically different from the population mean so we can can not reject the null hypothesis with this data. The t-test for Lot 3 had a p-value of 0.04168 which is lower than the common significant level, meaning that there is enough evidence to reject the null hypothesis. Therefore, the mean PSI of Lot 3 is statistically different from the population mean of 1,500 pounds per square inch.
	One Sample t-test

data:  subset(susp, Manufacturing_Lot == "Lot3")$PSI
t = -2.0916, df = 49, p-value = 0.04168
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1492.431 1499.849
sample estimates:
mean of x 
  1496.14 

> t.test(subset(susp,Manufacturing_Lot=="Lot2")$PSI,mu=1500)

	One Sample t-test

data:  subset(susp, Manufacturing_Lot == "Lot2")$PSI
t = 0.51745, df = 49, p-value = 0.6072
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1499.423 1500.977
sample estimates:
mean of x 
   1500.2 

> t.test(subset(susp,Manufacturing_Lot=="Lot1")$PSI,mu=1500)

	One Sample t-test

data:  subset(susp, Manufacturing_Lot == "Lot1")$PSI
t = 0, df = 49, p-value = 1
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1499.719 1500.281
sample estimates:
mean of x 
     1500 

## Study Design: MechaCar vs Competition

For my statistical study, I will look at how the MechaCar performs against the competition based on the cost metric, and how that impacts consumers buying decisions if the mpg is the same between different companies..
Null hypothesis: The cost of a MechaCar vehicle has no affect on consumers deciding on a car based on mpg.
Alternative hypothesis: The cost of a MechaCar vehicle has an affect on consumers deciding on a car based on mpg.
*The statistical test would you use to test the hypothesis is because
*The data needed to run the statistical test would be a multiple linear regression. This could be used to determine the factors that have the highest correlation between MechaCar pricing and a competitors pricing with the same mpg measurement. We can see what the data shows and then we would be able to predict future buying trends based on this data.