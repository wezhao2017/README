Code book for Getting and Cleaning Data course project

Introduction 

This code book summarizes the resulting data fields in tidyData.txt.

The zip file containing the source data is located at
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip.

The following transformations were applied to the source data:
1. Merge the train and the test sets to create one data set.
2. Extract only the measurements on the mean and standard deviation for each measurement, and the others were discarded.
3. Use descriptive activity names to name the activities in the data set.
4. Set appropriately labels the data with descriptive variable names. 
5. Create a second, independent tidy data set with the average of each variable for each activity and each subject.

The collection of the source data and the transformations listed above were implemented by the run_analysis.R. 
	

Variables 

fread() fwrite() from data.table package are used to get the data.
melt(), dcast() from the reshape2 package are used to clean data.
Files in folder ¡®UCI HAR Dataset¡¯ that will be used are:  
  activity_labels.txt
  features.txt
  train/X_train.txt
  train/y_train.txt
  train/subject_train.txt
  test/X_test.txt
  test/y_test.txt
  test/subject_test.txt
sapply() loop over and evaluate a function on each element, output into a vector or list.
getwd() get working directory.
download.file() downloading the dataset.
unzip() unzip datafiles to data directory. 
fread() get the raw data and create a new data table. 
grep() search for matches to ¡®mean¡¯ and ¡®std¡¯ arguments within each element of a character vector. 
gsub() perform replacement of the first and all matches respectively.
setnames() set the name on object ¡®train¡¯ and return the object ¡®train¡¯, and set the name on object ¡®test¡¯ and return the object ¡®test¡¯.  
cbind() clip data to together columns.
rbind() Merge train datasets and test datasets.
factor() turn activities and subjects into factors.
melt() convert data into a molten data frame ¡®combined¡¯.
dcast () take long-format data and casts it into wide-format data.
fwrite() output the tidy data as ¡®tidyData.txt¡¯. 

