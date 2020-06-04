# Part 1 - MPG Regression

library(tidyverse)
# Load in MechCar dataset
mcar <- read.csv('MechaCar_mpg.csv')

# View summary of exploratory regression model
summary(lm(mpg ~ vehicle.length + vehicle.weight + spoiler.angle + ground.clearance + AWD, data = mcar))

# View summary of chosen regression model based statistically significant results
summary(lm(mpg ~ vehicle.length + ground.clearance, data = mcar))

# PART 2 - Suspension Coil Summary Statistics

# Import coil data
coil_data <- read.csv('Suspension_Coil.csv')

# Note pastecs must be installed before the following import will work
library(pastecs)

# Get the summary statistics
stat.desc(coil_data$PSI)

# Part 3 - Suspension Coil T-Test

# Choosing a sample size of 50
coil_sample <- coil_data %>% sample_n(50)

# Conduct the t-test using sample and population
t.test(log10(coil_sample$PSI),mu=mean(log10(coil_data$PSI)))
