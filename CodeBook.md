##The uploaded run_analysis.R performs the following to clean up the data:

Merges the training and test sets to create one data set, namely train/X_train.txt with test/X_test.txt, train/subject_train.txt with test/subject_test.txt,  and train/y_train.txt with test/y_test.txt.

Use features.txt as input and extracts only the measurements on the mean and standard deviation for each measurement. All measurements appear to be floating point numbers in the range (-1, 1).

Reads activity_labels.txt and applies descriptive activity names to name the activities in the data set:
The script also appropriately labels the data set with descriptive names: all feature names (attributes) and activity names are converted to lower case, underscores and brackets () are removed. Then it merges the 10299x66 data frame containing features with 10299x1 data frames containing activity labels and subject IDs. The result is saved as merged_clean_data.txt, a 10299x68 data frame such that the first column contains subject IDs, the second column activity names, and the last 66 columns are measurements. Subject IDs are integers between 1 and 30 inclusive. 

Finally, the script creates a 2nd, independent tidy data set with the average of each measurement for each activity and each subject. The result is saved as New_averaage_data.txt.
