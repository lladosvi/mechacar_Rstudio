# mechacar_Rstudio

# Linear Regression to Predict MPG
- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

Vehicle weight, spoiler_angle & AWD provided a non-random amount of variance. The two variables that had the most amount of random variance are ground_clearance and vehicle_length.

- Is the slope of the linear model considered to be zero? Why or why not?

Our slope is not zero just be looking at the p-value, which is less than 0.05.

- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

Our R-squared value is 71%, which means roughly ~71% of the time the model will predict mpg values correctly. There are probably other factors that were not captured in the dataset that contribute to the mpg variability of the MechaCar prototypes.

- Supporting analysis for the responses is below:

![image](https://user-images.githubusercontent.com/96096924/161404894-a0e88064-39a7-48b3-a3be-b52aea1ae9f9.png)

# Summary Statistics on Suspension Coils,
- The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

When looking at the entire population of the production lot, the variance of the coils is 62.29 PSI, which is well within the 100 PSI variance requirement.

Similarly, but significantly more consistent, Lot 1 and Lot 2 are well within the 100 PSI variance requirement; with variances of 0.98 and 7.47 respectively. However, it is Lot 3 that is showing much larger variance in performance and consistency, with a variance of 170.29. It is Lot 3 that is disproportionately causing the variance at the full lot level.

## Total Summary

![image](https://user-images.githubusercontent.com/96096924/161405470-fa12a4f0-c2fc-4b09-8ac8-4234e611d09d.png)

## Lot Summary

![image](https://user-images.githubusercontent.com/96096924/161405515-b59edfae-af6b-4d50-97d9-e9890d8630e4.png)


# T-Tests on Suspension Coils
Lot 1 and Lot 3 the PSI values are not different from the population mean. However lot 2 the p-value is .347 which means there is evidence that the suspension coil is different from the population mean. All t-tests can be seen below:

## Across all lots:

![image](https://user-images.githubusercontent.com/96096924/161405631-b5705e40-4082-4512-9433-b6971999eee5.png)

## Lot 1:

![image](https://user-images.githubusercontent.com/96096924/161405648-de74a717-2bf0-48a0-935f-31cb7da34c63.png)

## Lot 2:

![image](https://user-images.githubusercontent.com/96096924/161405654-d07e4da5-dca5-4591-bfd7-26be695716ad.png)

## Lot 3:

![image](https://user-images.githubusercontent.com/96096924/161405670-d29454ef-ad1d-4ae7-8e90-9e0e1c7143e6.png)

# Study Design: MechaCar vs Competition
One feature that people are interested in when buying a car is how much horsepower the car has. I think horsepower, mpg and how large the engine is are 3 factors that go into consumer decision making. We can use our tests to see if our MechaCar is much different from the competiton. We can make a null hypothesis stating that it is not different from the competition and our Alternative would be the opposite. To do this we will need to use our t-test after collecting data from different types of competitor vehicles. Our t-test will be comparing the population of all types of competitor vehicles.
