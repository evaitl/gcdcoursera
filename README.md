# gcdcoursera
Course Project for Coursera GCD course

From the project description: 

> The purpose of this project is to demonstrate your ability to collect,
> work with, and clean a data set. The goal is to prepare tidy data that
> can be used for later analysis. You will be graded by your peers on a
> series of yes/no questions related to the project. You will be
> required to submit: 1) a tidy data set as described below, 2) a link
> to a Github repository with your script for performing the analysis,
> and 3) a code book that describes the variables, the data, and any
> transformations or work that you performed to clean up the data called
> CodeBook.md. You should also include a README.md in the repo with your
> scripts. This repo explains how all of the scripts work and how they
> are connected.
> 
> ... 
> 
> You should create one R script called run_analysis.R that does the following. 
> 
> 1. Merges the training and the test sets to create one data set.
> 
> 2. Extracts only the measurements on the mean and standard deviation
>   for each measurement.
> 
> 3. Uses descriptive activity names to name the activities in the data set
> 
> 4. Appropriately labels the data set with descriptive variable names. 
> 
> 5. From the data set in step 4, creates a second, independent tidy data
>   set with the average of each variable for each activity and each
>   subject.

The file run_analysis.R will grab the UCI data if necessary. On a
Linux box, you can run it with ./run_analysis.R as the file has a
shbang to use Rscript.

The R script merges the test and train files. The feature names are
modified to make them unique legal column names in R.  The numbers in
the activity files are replaced with their equivalent names from the
activity_labels.txt file.

The data is trimed to only retain the activity columns with names
containing 'mean' or 'std' 

The R script then uses aggregate to group by activity and subject and
does a mean() on each activity by group and this is saved as the tidy
data.frame.  The tidy data.frame is then saved to a text file
"tidy.txt".
