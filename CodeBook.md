

## Overview

30 volunteers performed 6 different activities while wearing a smartphone. The smartphone captured various data about their 
movements.

Explanation of each file

features.txt: Names of the 561 features.

activity_labels.txt: Names and IDs for each of the 6 activities.

X_train.txt: 7352 observations of the 561 features, for 21 of the 30 volunteers.

subject_train.txt: A vector of 7352 integers, denoting the ID of the volunteer related to each of the observations in X_train.txt.

y_train.txt: A vector of 7352 integers, denoting the ID of the activity related to each of the observations in X_train.txt.

X_test.txt: 2947 observations of the 561 features, for 9 of the 30 volunteers.

subject_test.txt: A vector of 2947 integers, denoting the ID of the volunteer related to each of the observations in X_test.txt.

y_test.txt: A vector of 2947 integers, denoting the ID of the activity related to each of the observations in X_test.txt.

More information about the files is available in README.txt. More information about the features is available in features_info.txt.


## Steps taken to get clean data
* read all the data, put it together in the format of: subjects, labels, everything else
* read the features, select only the means and standard deviations from data
* read the labels (activities),replace labels in data with label names
* make a list of the current column names and feature name, clean that list by removing every non-alphabetic character and 
converting to lowercase, then use the list as column names for data
* find the mean for each combination of subject and label and write the data for uplad tidy_data.txt
