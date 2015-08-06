The run_analysis.R script merges the test and training data from the
UCI HAR Dataset. It renames the activities into legal R data frame
column names and changes the activities from integers into descriptive
strings.


All of the mean and std columns are selected, then grouped by subject
and activity and the mean of each of these groupings is found and
stored into a data frame called 'tidy'. This data frame is then
written out with write.table().

