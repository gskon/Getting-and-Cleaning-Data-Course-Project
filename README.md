## Getting and Cleaning Data Course Project


For creating a tidy data set of wearable computing data originally from 
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

# Files in this repo

* README.md -- you are reading it right now
* CodeBook.md -- codebook describing variables, the data and transformations
* run_analysis.R -- actual R code

# run_analysis.R goals

You should create one R script called run_analysis.R that does the following:

Merges the training and the test sets to create one data set.
Extracts only the measurements on the mean and standard deviation for each measurement.
Uses descriptive activity names to name the activities in the data set
Appropriately labels the data set with descriptive activity names.
Creates a second, independent tidy data set with the average of each variable for each activity and each subject.
It should run in a folder of the Samsung data (the zip had this folder: UCI HAR Dataset) The script assumes it has 
in it's working directory the following files and folders:

* activity_labels.txt
* features.txt
* test/
* train/
The output is created in working directory with the name of tidy_data.txt

Note: the R script is built to run without including any libraries for the purpose of this course.


## run_analysis.R walkthrough

It follows the goals step by step.

* read all the data, put it together in the format of: subjects, labels, everything else
* read the features, selects only the means and standard deviations from data
* read the labels (activities),replace labels in data with label names
* make a list of the current column names and feature name, clean that list by removing every non-alphabetic character and converting to lowercase, then use the list as column names for data
* find the mean for each combination of subject and label and write the data for uplad tidy_data.txt
