describe run_analysis.R variables

library(downloader)
as what question mentioned do not need to download file, it is currently available i working directory
## below two lines is not needed as long as samsung data is available on working directory
##fileUrl <- "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
##download.file(fileUrl,destfile="Dataset.zip",mode="wb")
set path in order to use in future code lines
path_rf: ("UCI HAR Dataset")

##read files
names(dataActivity) = activity create from combining   
  dataActivityTest  : "Y_test.txt" 
  dataActivityTrain : "Y_train.txt"
names(dataSubject) = Subject create from combining
  "subject_train.txt"
  "subject_test.txt"
names(dataFeatures) = feature create combining, names come from feature.txt which is a vector
  "X_test.txt"
  "X_train.txt"

##combine all Data o create Data frame
Data = Combination of (dataSubject, dataActivity)& dataFeatures

##Extract measurements on mean and std = subdataFeaturesNames

## write complete activity names = activityLabels from "activity_labels.txt"

##meaningful & complete data names
"time" => "t"
"frequency" => "f"
"Acc" <= "Accelerometer"
"Gyro" <= "Gyroscope"
"Mag" <= "Magnitude"
"BodyBody" <= "Body"

##In this part,a second, independent tidy data set will be created with the average of each variable for each activity and each subject based on the data set in step 4.

Output file : write Data2 to "tidydata.txt" which is a aggregated file
