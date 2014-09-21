README 
---
The assignment instructions state that this file should explain how "all of the scripts work and how they are connected."

To create the output tidy data set, one needs to run the run_analysis.R script (only this one script is required).  Input data should be in the directory "UCI HAR Dataset", which should be located immeadiately below the working directory.  The data in "UCI HAR Dataset" should be organized as it is in the zip file (file is available at: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip).  

The output tidy data set (tidydataset.txt) is created in the working directory.

The data provided as output for the assignment set includes the following files:
 - run_analysis.R 
 - script
 - ReadMe.md - markdown document
 - Codebook.md - markdown document
- tidydataset.txt - tidy data text file (loaded on Coursera)

---
Here are the steps that were used to transform the original input data set.

Here is a diagram, based on that provided by David Hood, showing how the input data is pieced together.


|Variable names  | features.txt  | Subject               | Activity      |                              |
| -------------- |---------------| ----------------------|---------------|------------------------------|
|Data            | x_train.txt   | subject_train.txt     | y_train.txt   |  activity_labels.txt         | 
|Data            | x_test.txt    | subject_test.txt      | y_test.txt    |  activity_labels.txt         |

Read in the column names that apply to the x_train.txt and x_test.x data sets (using read.table) from "UCI HAR Dataset\\features.txt" apply column names "id" and "names".

- Merge together the following information for train
 - subject (subject_train.txt)
 - activity identifier (y_train.txt)
 - features (x_train,txt)
- Remove data that is not subject, activity id, or measurements for mean and standard deviation data - Removal is based on column names.  Output is dataframe containing subject, activity id, measurements for mean and standard deviation data.

- Merge together the following information for test
 - subject (subject_test.txt)
 - activity identifier (y_test.txt)
 - features (x_test,txt)

- Remove data that is not subject, activity id, or measurements for mean and standard deviation data - Removal is based on column names.  Output is dataframe containing subject, activity id, measurements for mean and standard deviation data.

Then combine "test" and "training" data sets to create single data set.

- Replace activity id with activity labels.  Reading in activity labels from activity_labels.txt file and merging this using the activityid field in the data frame.  Then remove the unneeded activityid column.

- Rename the column names to be more descriptive.
 - Remove "-" and "()"
 - Remove leading "t" , ""
 - Change leading "f" with "FFT" to show that these are frequency domain values
 - Change:
 - "std" to "StandardDeviation"
 - "Freq", "Frequency"
 - "Gyro", "Gyroscope"
 - "Mag", "Magnitude"
 - "mean", "Mean"
 -"Acc", "Acceleration"

Then transform the data by calculating the mean of the data by activity and subjectID.

The resulting data set is the tidy data set ("tidydataset.txt")

