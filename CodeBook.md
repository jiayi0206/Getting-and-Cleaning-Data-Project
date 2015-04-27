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
