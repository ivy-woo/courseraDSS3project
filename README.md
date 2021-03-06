# Data processing project

This is a repo for the course Getting and Cleaning Data on Coursera, the 3rd course from the [Data Science Specialization](https://www.coursera.org/specializations/jhu-data-science).  
Here you find the 3 files listed below:

### run_analysis.R
This is the R script used to read in and tidy the data files provided from the course.  
To obtain the resulting tidied data, follow these steps:  
1. place the R script and the folder 'UCI HAR Dataset' (obtained from the assignment instruction page) in the same location,  
2. set the working directory to where the R code and the dataset folder are in,  
3. run the full script.  
The tidied data will be produced in the directory.  
(The packages 'reshape2' and 'plyr' are needed. Please install them first if they are not already.)  

Below is a summary of what the script does in order:  
1. read in the relevant raw data files  
2. combine the raw data frames from the training and test sets to one dataset (task1)  
3. assign variable names to the dataset (task4)  
4. locate the columns which contain data on the mean and standard deviation of the measurements, then subset the dataset accordingly (task2)  
5. replace the numbering for the activities to descriptive names  (task3)  
6. melt the dataset to a tall thin data frame  
7. create another data frame that averages the measurements for each subject, activity and measurements (task5)  
8. output the final result  

The R script also contains various explanatory comments, which help readers to follow the flow.
The 5 required tasks are labelled in the comments, showing that all tasks have been completed.  

### TidyData.txt
This is the tidied and submitted data on coursera.  
The first column is the subject number, the second column is the activity, the third column is the code of the measurement (the meanings for which are described in the codebook), and the forth column gives the average for the corresponding subject, activity and measurement.  
This data is tidy in the sense that it fulfills all the listed requirements for a tidy data given in the course:
each variable measured is in one column, each different observation of the variable is in a different row, and the column variables are named in a human readable way.  

To read the data into R, place the file into the working directory and type the command:  
read.table("TidyData.txt")  


### Codebook.md
The codebook provides details for the variables in the tidied data, so that one can easily understand how to read the data.  
Variables are listed in the same order as appeared in the tidied data.
