# CODE BOOK

This document contains final dataset of Top 10 girls name from year 2016 and 2015, generated from munging, sorting, and summarizing popular children's name data provided on Homework files. This describes code inside YKunwar_Livesesion5assignment.Rmd

## Source of Raw Data:
I pulled the dataset named yob2016.txt and yob2015.txt for analysis provided during homework. The datasets contains popular childrens names during year 2015 and 2016.
The link is as follows:
https://2ds.datascience.smu.edu/local/files/index.php?course_id=104&group=290&userid=1121&groupid=-1

* Contents and Files
I am listing each attributes of the raw files found in local machine with path '~/MSDS6306/Test_git/Homework_git/*.txt' (* = filename). 

yob2016.txt 
This files contains raw data separated by semicolon (;) without headers which contains First name of the child, gender and total children with that name on the year 2016.

yob2015.txt 
This files contains raw data separated by comma (,) without headers which contains First name of the child, gender and total children with that name on the year 2015.

 The code is splitted into sections according to files utilized:

* Data Munging
* Data Merging
* Data Summary
* Uploading to Github repository


### Data Munging
 ** Used to read.table to read and import yob2016.txt and store it into an object (df)
 ** Object (df) contains following columns assigned by using colnames(df): "FirstNames", "Gender", "Total Children" 
 ** At this point checking dataset by using head function, summarizing using summary and structure function.
      - df is data.frame with 32857 observations of 3 variables
      Variables 
      - $FirstNames (factor w/ 30295 levels), 
      - $Gender (factor w/ 2 levels: "M", "F") 
      - $TotalChildren (int)   
 
 **
 
 
 
 
 
 
 
 
 
 
