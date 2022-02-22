# mechacar_statistical_analysis

## Deliverable One 

lm(mpg ~ vehicle_length + vehicle_weight + spoiler_angle + ground_clearance + AWD, data = car_df)

Call:
lm(formula = mpg ~ vehicle_length + vehicle_weight + spoiler_angle + 
    ground_clearance + AWD, data = car_df)

Coefficients:
     (Intercept)  
      -1.040e+02  
  vehicle_length  
       6.267e+00  
  vehicle_weight  
       1.245e-03  
   spoiler_angle  
       6.877e-02  
ground_clearance  
       3.546e+00  
             AWD  
      -3.411e+00  


summary(lm(mpg ~ vehicle_length + vehicle_weight + spoiler_angle + ground_clearance + AWD, data = car_df))

Call:
lm(formula = mpg ~ vehicle_length + vehicle_weight + spoiler_angle + 
    ground_clearance + AWD, data = car_df)

Residuals:
     Min       1Q   Median       3Q 
-19.4701  -4.4994  -0.0692   5.4433 
     Max 
 18.5849 

Coefficients:
                   Estimate Std. Error
(Intercept)      -1.040e+02  1.585e+01
vehicle_length    6.267e+00  6.553e-01
vehicle_weight    1.245e-03  6.890e-04
spoiler_angle     6.877e-02  6.653e-02
ground_clearance  3.546e+00  5.412e-01
AWD              -3.411e+00  2.535e+00
                 t value Pr(>|t|)    
(Intercept)       -6.559 5.08e-08 
vehicle_length     9.563 2.60e-12  
vehicle_weight     1.807   0.0776 .  
spoiler_angle      1.034   0.3069    
ground_clearance   6.551 5.21e-08 
AWD               -1.346   0.1852    

Signif. codes:  
  0 ‘ *** ’ 0.001 ‘ ** ’ 0.01 ‘*’ 0.05 ‘.’
  0.1 ‘ ’ 1

Residual standard error: 8.774 on 44 degrees of freedom
Multiple R-squared:  0.7149,	Adjusted R-squared:  0.6825 
F-statistic: 22.07 on 5 and 44 DF,  p-value: 5.35e-11

**Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?** 


**Is the slope of the linear model considered to be zero? Why or why not?**


**Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?**



## Deliverable Two 

**Summary Statistics on Suspension Coils**


<img width="329" alt="total_summary" src="https://user-images.githubusercontent.com/92737670/155034895-0c224a4a-150a-4433-96cd-cced034d0da7.png">


<img width="494" alt="lot_summary" src="https://user-images.githubusercontent.com/92737670/155045176-f86a0177-5871-4f1d-9069-5f9f079eb4e1.png">


## Deliverable Three 

t.test(log10(susp_coils$PSI),mu=mean(log10(total_summary$Mean)))

	One Sample t-test

data:  log10(susp_coils$PSI)
t = -0.032082, df = 149, p-value = 0.9744
alternative hypothesis: true mean is not equal to 3.175738
95 percent confidence interval:
 3.175361 3.176103
sample estimates:
mean of x 
 3.175732 
 
 
 
lot_one = subset(susp_coils, Manufacturing_Lot=="Lot1")

	One Sample t-test

data:  log10(lot_one$PSI)
t = 8.7174, df = 49, p-value
= 1.561e-11
alternative hypothesis: true mean is not equal to 3.175738
95 percent confidence interval:
 3.176010 3.176173
sample estimates:
mean of x 
 3.176091 


lot_two = subset(susp_coils, Manufacturing_Lot=="Lot2")

One Sample t-test

data:  log10(lot_two$PSI)
t = 3.6693, df = 49, p-value
= 0.0005995
alternative hypothesis: true mean is not equal to 3.175738
95 percent confidence interval:
 3.175924 3.176373
sample estimates:
mean of x 
 3.176148 


lot_three = subset(susp_coils, Manufacturing_Lot=="Lot3")

One Sample t-test

data:  log10(lot_three$PSI)
t = -1.4558, df = 49, p-value
= 0.1518
alternative hypothesis: true mean is not equal to 3.175738
95 percent confidence interval:
 3.173877 3.176035
sample estimates:
mean of x 
 3.174956
