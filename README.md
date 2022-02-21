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


