The run_analysis.R script merges the test and training data from the
UCI HAR Dataset. It renames the feature columns into legal R data
frame column names and changes the saved activities from integers into
descriptive strings that can be loaded as factors. 

All of the mean and std columns of the UCI dataset are selected, then
grouped by subject and activity and the mean of each of these
groupings is found and stored into a data frame called 'tidy'. This
data frame is then written out with write.table().

The first two columns of tidy are the subject (an integer identifier)
and the activity (a string) being performed.  The rest of the columns
are means of scaled floating point numbers (between -1 and +1). 
