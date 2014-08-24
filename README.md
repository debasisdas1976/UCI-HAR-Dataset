Project Details
===============

This project is about creating a tidy dataset from the original raw dataset available at

 https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip


The dataset contains data collected from the accelerometers from the Samsung Galaxy S smartphone.

The project contains the following files

The script **run_analysis.R**, which analyzes the above data files and creates a tidy dataset which is appropriate for 

further analysis.

The file **Codebook.md**, which describes the variables in the final tiday datasets created.

To run the script
=================

1. Download and store the [zip](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) file into to a directory.

2. Untar the zip file into a directory. After unzip, go the the directory which contain the following subdirectories and
data files.

```
+ train/X_train.txt - Train datasets with features observations 
+ train/y_train.txt - Activity labels for train datasets
+ test/X_test.txt - Train datasets with features observations
+ test/y_test.txt - Activity lables for test datasets
+ train/subject_train.txt - subject id for the train data set
+ test/subject_test.txt - subject id for the test data set
+ features.txt - features for which observations were noted
+ activity_labels.txt - activity labels
```

3. Set the above directory (under which the above datasets are available) as the current working directory of R  environment. This can be done by using setwd()

```
e.g. setwd( "G:\\GetCleanData\\getdata-projectfiles-UCI HAR Dataset\\UCI HAR Dataset" )
Download and copy the script run_analysis.R in your current working directory
```

4. Install the package plyr in your R environment, if it is not already installed.

5. install.packages( "plyr" )
To run the script, source **run_analysis.R** script into the R environment and call **prepareTidyDataSet()** function

```
> source( "run_analysis.R")
> finaldataset <- prepareTidyDataSet()
```

 The script outputs following messages to the console during successful execution

  Loading the train dataset...
  Loading the test dataset...
  Loading other data files...
  Joining all datasets by subjectids and activity ids...
  Preparing the column names...
  Merging the train and test datasets...
  Calculating mean values of selected measurements...
  Processing complete and following two files are created
   - UCI-HAR-Dataset-Tidy.txt - Final tidy data set

It also returns a data.frame which contains the tidy data set.

7. Once executed successfully, it returns the data.frame which contains the final tidy dataset. The script also stores the 

final dataset in the following file in your current working directory.

**UCI-HAR-Dataset-Tidy.txt**

The output file is in csv format. The variables are explained in the [Codebook.md](https://github.com/debasisdas1976/UCI-

HAR-Dataset/Codebook.md) file.
