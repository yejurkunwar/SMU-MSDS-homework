# CODE BOOK

# Introduction
This document contains final dataset of Top 10 girls name from year 2016 and 2015, generated from munging, sorting, and summarizing popular children's name data provided on Homework files. This describes code inside **YKunwar_Livesesion5assignment.Rmd**

## Source of Raw Data:
I pulled the dataset named yob2016.txt and yob2015.txt for analysis provided during homework. The datasets contains popular childrens names during year 2015 and 2016.
The link is as follows:
https://2ds.datascience.smu.edu/local/files/index.php?course_id=104&group=290&userid=1121&groupid=-1

However, dataset belongs to social security administration data. Details can be found by following this link: https://www.ssa.gov/oact/babynames/background.html


* Contents and Files
I am listing each attributes of the raw files found in local machine with path '~/MSDS6306/Test_git/Homework_git/*.txt' (* = filename). 

*yob2016.txt
This files contains raw data separated by semicolon (;) without headers which contains First name of the child, gender and total children with that name on the year 2016.

*yob2015.txt
This files contains raw data separated by comma (,) without headers which contains First name of the child, gender and total children with that name on the year 2015.

 The code is splitted into sections according to files utilized:

* Data Munging
* Data Merging
* Data Summary
* Uploading to Github repository


### Data Munging
 1. Used to read.table to read and import yob2016.txt and store it into an object (df)
 2. Object (df) contains following columns assigned by using colnames(df): "FirstNames", "Gender", "Total Children"
 3. At this point checking dataset by using head function, summarizing using summary and structure function.
      - df is data.frame with 32857 observations of 3 variables
      Variables 
        - $FirstNames (factor w/ 30295 levels), 
        - $Gender (factor w/ 2 levels: "M", "F")
        - $TotalChildren (int)   
 4. Data is cleaned by capturing and removing redundant names into and object called (match_name).
 5. This dataset is stored in an object named (y2016).

### Data Merging
 1. Used to read.table to read and import yob2015.txt and store it into an object (y2015)
 2. Object (y2015) contains following columns assigned by using colnames(y2015): "FirstNames", "Gender", "Total Children"
 3. At this point checked head and last 10 data by using head and tail functions, verified variables. 
 4. Merged dataframe in objects (y2015) and (y2016) to dataframe object named (final) while removing NA's.
 
 ## Data Summary
 1. Calculated total number of First names by adding from y2015 and y2016, assigned it to object called (total) and finally to object named (all).
 2. At this point dataframe object (all)contains variables with: 
    - "FirstNames" 
    - "Gender"
    - "Total Children.x"
    - "Total Children.y"
    - "Total"
 3. Sorted data by ordering (total) in descending order to find top names, assigned to object named (top_10) and (sorted_top10).
 4. Again filtered, female only top list in descending order, assigned into object (femaletop_10), finally storing a;; top 10 female names to (girl_top10)
 4. Lastly, assigned object names (new) to store only two columns into new data frame.
 5. At this point data frame consists of two columns with 10 observations and 2 columns with variables:
    - "GirlsFirstName" (Names of top 10 girls filtered from data set y2016 and 2015)
    - "Total" (Total number of girls with that particular names in year 2015 and 2016)
    
 6. Utilized write.csv function to write girl_top10.csv file from dataframe object (new) without row names. 
 7. Pushed the files and codes to github and shared the link.
 
 * SessionInfo is displayed for more documentation
 
 
 
 
 
 
 
 
 
 
