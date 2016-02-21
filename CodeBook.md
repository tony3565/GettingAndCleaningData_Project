# CodeBook For GettingAndCleaningData Project

The run.analysis script produces two CSV files called rawdata.csv and tidydata.csv

## rawdata.csv
The rawdata.csv contains approximately 10000 measurements of 66 different parameters.

The 10000 measurements are spread across 6 different activities from 30 different 
test subjects. The different activities are STANDING, SITTING, LAYING, WALKING, 
WALKING_DOWNSTAIRS, and WALKING_UPSTAIRS. The 66 different parameters are split 
between mean and standard deviation and primarily spread across 3 axes (X, Y, and Z). 

So, the 66 parameters are split between 40 time interval measures and 26 force 
measurements. 

The 40 time interval measurements are divided into 20 mean and 20 standard deviation
measurements. Each group of 20 represent 5 parameters across 4 categories (X-axis, 
Y-axis, Z-axis, and Magnitude). The 5 parameters are Body Acceleration, Gravity 
Acceleration, Body Jerk (change in acceleration?), Body Gyro (presumably for rotation 
acceleration), and Body Gyro Jerk Time.

The 26 force measurements are also divided between mean and standard deviation 
measures. Of these, the 3 parameters of Body Acceleration, Body Jerk, and Body Gyro 
are given for 4 categories (X-axis, Y-axis, Z-axis, and Magnitude). The Gravity
Acceleration parameter is not necessary since the force of gravity can be assumed
to be constant. 

The one odd duck is Body Gyro Jerk. For this parameter, only the magnitude measurement
is included (as far as I can tell). I searched through all of the features in features.txt
and confirmed that the axial force measurements do not exist for Body Gyro Jerk.

So, along with the 24 force measurements for Body Acceleration, Body Jerk, and Body
Gyro, the Body Gyro Jerk measurements only include the mean and standard deviation
of the Magnitude; this results in just 26 force measurements

## tidydata.csv

The tidydata.csv contains 180 measurements of the same 66 parameters provided in 
rawdata.csv. The difference is that each row represents the mean for each activity
for each subject. Since there were 30 subjects and 6 activities, we should expect
180 rows.

The other change is with the column names. The column names were slightly abbreviated
to be slightly more readable. 

