Getting and Cleaning Data Course Project

Description of Variables, Data files and the working of the script run_analysis.R

Variables in output file(s)

activity_label 
Name of activity (laying, sitting, standing, walking, walking_downstairs, walking_upstairs)
subject_no. 
Subject number (1 to 30)
activity_no. 
Activity number (1 to 6)
The other columns are as described in the original data set
Input Data

Human Activity Recognition Using Smartphones from UCI Machine Learning Repository.

Data - https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
Website - http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Output files

Step 2 Output
feature2  - Data extract of mean and standard deviation columns

Step 5 Output
X_test -Column Means when grouped by activity and subject

The run_analysis.R

Read data from the following files

Training Features - X_train.txt
Training Response -Y_train.txt
Test Features - X_test.txt
Test Response - Y_test.txt
Training Subjects - subject_train.txt
Test Subjects - subject_test.txt
Features (Column Names) - features_file.txt
Activity Labels - activity_label_file.txt

Apply column names (feature names)

Combine (cbind) features, activity and subject data frames together to form two data sets, test and train

Combine (rbind) test data and train data together

Get names of “mean()” and “std()” features (grep).

Extract required features using the list of names

Add descriptive activity labels.

Write data file of extracted data (mean and standard deviation columns)
tidy_data.txt

Group and split data by "activity" and by "subject"

Calculate means using sapply

Transpose Matrix, add “activity_label” and “subject_no.” columns

Tidy up data and Write data file of means when grouped by activity and subject
tidy_data.txt



Variable list and descriptions

(variable names starting with t means time and units are seconds, variables names starting with f means frecuency and units are Hz)

Variable name	Description
subject	ID the subject who performed the activity for each window sample. Its range is from 1 to 30.
activity	Activity name
tBodyAccelerationMeanX	Feature: Average time body acceleration signal X axis
tBodyAccelerationMeanY	Feature: Average time body acceleration signal Y axis
tBodyAccelerationMeanZ	Feature: Average time body acceleration signal Z axis
tBodyAccelerationStdX	Feature: Standard deviation time body acceleration signal X axis
tBodyAccelerationStdY	Feature: Standard deviation time body acceleration signal Y axis
tBodyAccelerationStdZ	Feature: Standard deviation time body acceleration signal Z axis
tGravityAccelerationMeanX	Feature: Average time body gravity signal X axis
tGravityAccelerationMeanY	Feature: Average time body gravity signal Y axis
tGravityAccelerationMeanZ	Feature: Average time body gravity signal Z axis
tGravityAccelerationStdX	Feature: Standard deviation time body gravity signal X axis
tGravityAccelerationStdY	Feature: Standard deviation time body gravity signal Y axis
tGravityAccelerationStdZ	Feature: Standard deviation time body gravity signal Z axis
tBodyAccelerationJerkMeanX	Feature: Average time body acceleration jerk signal X axis
tBodyAccelerationJerkMeanY	Feature: Average time body acceleration jerk signal Y axis
tBodyAccelerationJerkMeanZ	Feature: Average time body acceleration jerk signal Z axis
tBodyAccelerationJerkStdX	Feature: Standard deviation time body acceleration jerk signal X axis
tBodyAccelerationJerkStdY	Feature: Standard deviation time body acceleration jerk signal Y axis
tBodyAccelerationJerkStdZ	Feature: Standard deviation time body acceleration jerk signal Z axis
tBodyGyroscopeMeanX	Feature: Average time body gyroscope signal X axis
tBodyGyroscopeMeanY	Feature: Average time body gyroscope signal Y axis
tBodyGyroscopeMeanZ	Feature: Average time body gyroscope signal Z axis
tBodyGyroscopeStdX	Feature: Standard deviation time body gyroscope signal X axis
tBodyGyroscopeStdY	Feature: Standard deviation time body gyroscope signal Y axis
tBodyGyroscopeStdZ	Feature: Standard deviation time body gyroscope signal Z axis
tBodyGyroscopeJerkMeanX	Feature: Average time body gyroscope jerk signal X axis
tBodyGyroscopeJerkMeanY	Feature: Average time body gyroscope jerk signal Y axis
tBodyGyroscopeJerkMeanZ	Feature: Average time body gyroscope jerk signal Z axis
tBodyGyroscopeJerkStdX	Feature: Standard deviation time body gyroscope signal X axis
tBodyGyroscopeJerkStdY	Feature: Standard deviation time body gyroscope signal Y axis
tBodyGyroscopeJerkStdZ	Feature: Standard deviation time body gyroscope signal Z axis
tBodyAccelerationMagnitudeMean	Feature: Average time body acceleration signal magnitude
tBodyAccelerationMagnitudeStd	Feature: Standard deviation time body acceleration signal magnitude
tGravityAccelerationMagnitudeMean	Feature: Average time body gravity acceleration signal magnitude
tGravityAccelerationMagnitudeStd	Feature: Standard deviation time body gravity acceleration signal magnitude
tBodyAccelerationJerkMagnitudeMean	Feature: Average time body jerk signal acceleration magnitude
tBodyAccelerationJerkMagnitudeStd	Feature: Standard deviation time body jerk acceleration signal magnitude
tBodyGyroscopeMagnitudeMean	Feature: Average time body gyroscope signal magnitude
tBodyGyroscopeMagnitudeStd	Feature: Standard deviation time body gyroscope signal magnitude
tBodyGyroscopeJerkMagnitudeMean	Feature: Average time body gyroscope jerk signal magnitude
tBodyGyroscopeJerkMagnitudeStd	Feature: Standard deviation time body gyroscope jerk signal magnitude
fBodyAccelerationMeanX	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationMeanX
fBodyAccelerationMeanY	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationMeanY
fBodyAccelerationMeanZ	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationMeanZ
fBodyAccelerationStdX	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationStdX
fBodyAccelerationStdY	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationStdY
fBodyAccelerationStdZ	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationStdZ
fBodyAccelerationJerkMeanX	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationJerkMeanX
fBodyAccelerationJerkMeanY	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationJerkMeanY
fBodyAccelerationJerkMeanZ	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationJerkMeanZ
fBodyAccelerationJerkStdX	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationJerkStdX
fBodyAccelerationJerkStdY	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationJerkStdY
fBodyAccelerationJerkStdZ	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationJerkStdZ
fBodyGyroscopeMeanX	Feature: Fast Fourier Transform (FFT) of tBodyGyroscopeMeanX
fBodyGyroscopeMeanY	Feature: Fast Fourier Transform (FFT) of tBodyGyroscopeMeanY
fBodyGyroscopeMeanZ	Feature: Fast Fourier Transform (FFT) of tBodyGyroscopeMeanZ
fBodyGyroscopeStdX	Feature: Fast Fourier Transform (FFT) of tBodyGyroscopeStdX
fBodyGyroscopeStdY	Feature: Fast Fourier Transform (FFT) of tBodyGyroscopeStdY
fBodyGyroscopeStdZ	Feature: Fast Fourier Transform (FFT) of tBodyGyroscopeStdZ
fBodyAccelerationMagnitudeMean	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationMagnitudeMean
fBodyAccelerationMagnitudeStd	Feature: Fast Fourier Transform (FFT) of tBodyAccelerationMagnitudeStd
fBodyBodyAccelerationJerkMagnitudeMean	Feature: Fast Fourier Transform (FFT) of tBodyBodyAccelerationJerkMagnitudeMean
fBodyBodyAccelerationJerkMagnitudeStd	Feature: Fast Fourier Transform (FFT) of tBodyBodyAccelerationJerkMagnitudeStd
fBodyBodyGyroscopeMagnitudeMean	Feature: Fast Fourier Transform (FFT) of tBodyBodyGyroscopeMagnitudeMean
fBodyBodyGyroscopeMagnitudeStd	Feature: Fast Fourier Transform (FFT) of tBodyBodyGyroscopeMagnitudeStd
fBodyBodyGyroscopeJerkMagnitudeMean	Feature: Fast Fourier Transform (FFT) of tBodyBodyGyroscopeJerkMagnitudeMean
fBodyBodyGyroscopeJerkMagnitudeStd	Feature: Fast Fourier Transform (FFT) of tBodyBodyGyroscopeJerkMagnitudeStd
