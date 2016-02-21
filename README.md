# GettingAndCleaningData_Project

# The data is processed by a R script called run_analysis.r. Script run_analysis.r
# contains 2 primary functions called download.data and run.analysis.

Steps to analyzing the data with run_analysis.r
1) Open a R Console or RStudio

2) Source the script
   > source('~/run_analysis.R')

3) Download the data from the web
   > download.data()

   # This will create a directory called "UCI HAR Dataset"
   # This directory contains all the training and test data
   # including the files that contains feature and label
   # information

4) Analyze the data
   > run.analysis()

   # This processes the files in the UCI HAR Dataset directory
   # The output of the script is two files called "rawdata.csv"
   # and "tidydata.csv". File "rawdata.csv" contains all the 
   # mean and standard deviation measurements for the different 
   # activities and different subjects (people). File "tidydata.csv" 
   # contains mean and standard deviation averages for a given
   # person and a given activity.
