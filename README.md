# mechacar_statistical_analysis

## Deliverable One 

<img width="298" alt="Screenshot 2022-02-22 181940" src="https://user-images.githubusercontent.com/92737670/155236222-67669697-ea97-4c76-9758-898d9d1f974c.png">

**Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?** 

Vehicle Length and Ground Clearance are statistically unlikely to provide random amounts of variance.

**Is the slope of the linear model considered to be zero? Why or why not?**

The p-value is 5.35e-11, which is less than 0.5. Therefore, the slope is not 0.

**Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?**

The R-squared value is 0.7149. Therefore, our model predicts mpg correctly around 71.5% of the time. So, it's moderatley effective. 

## Deliverable Two 

**Summary Statistics on Suspension Coils**

<img width="329" alt="total_summary" src="https://user-images.githubusercontent.com/92737670/155034895-0c224a4a-150a-4433-96cd-cced034d0da7.png">


<img width="494" alt="lot_summary" src="https://user-images.githubusercontent.com/92737670/155045176-f86a0177-5871-4f1d-9069-5f9f079eb4e1.png">

Lot 1 and 2 meet the design specifications (variance NTE 100 pounds per sq. in.), but Lot 3 exceeds the allowable variance.

## Deliverable Three 

**T-Tests on Suspension Coils**

The P value of Lot 1 and Lot 2 are both below .05, therefore there is a statistical difference at those Lots. However, the P value of Lot 3 is above .05, and therefore the means are statistically similar.

**Population**

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
 
 **Lot One**
 
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

**Lot Two**

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

**Lot Three*

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
 
