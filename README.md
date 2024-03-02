# StandardizedTestResultsAnalysis

This project revolves around 2 data files containing student and school data for a single district. The objective is to analyze this data in six, separate sections and draw conclusions based on the results. The pandas library is used for the data manipulation and grouping.

The paths of both the csv files are loaded located and then read using the "read_csv" function inside the pandas library. Both these datasets are merged together to create a single dataframe called 'school_data_complete' using the "school_name" column that is present in both data tables. 


## ** Part I: District Analysis
The first portion of this analysis deals with analyzing the entire district and making a dataframe called 'district_summary' that contains all the district's metrics. The total number of schools, number of students, total budget, average math scores, average reading scores, percentage of students passing math, percentage of students passing reading, and percentage of students passing both are calculated and each make up a column in this dataframe. 

## ** Part II: Per School Analysis
The second portion of this analysis creates a dataframe called 'per_school_summary' which makes each school an index and gives informatiion regarding: the school type, total amount of students, total school budget, per student budget (total school budget divided by the total amount of students), average math score, average reading score, percentage of students passing math, percentage of students passing reading, and percentage of students passing overall. The values under the columns "Total School Budget" and "Per Student Budget" are formatted to include a dollar sign, a comma after each thousand's value, and 2 decimal places. 

## ** Part III: Highest and Lowest School Performance
The third portion of this analysis sorts the 'per_school_summary' dataframe based on the "% Overall Passing" column. To find the highest-performing schools, the sorting is done in descending order and the first five rows are isolated to give the top five schools with the highest values in the "% Overall Passing" column. To find the lowest-performing schools, the sorting is conducted in ascending order and the first five rows are extracted. This shows the five schools with the lowest values in the column. 

## ** Part IV: Per Grade Analysis
The fourth portion of the analysis deals with separating the 'per_school_summary' dataframe into grades and finds the average math and reading scores for each grade. The average math score per grade is placed into a dataframe called 'math_scores_by_grade' and the average reading score per grade is added into a dataframe called 'reading_scores_by_grade'.

## ** Part V: Capita Spending and School Size Binning Analysis 
The fifth part of the analysis involves the use of binning to separate the data based on school spending and school size in order to find the mean scores and passing rates for each subgroup. The school spending is based on binning the "Per Student Budget" column. The scores and passing rates for each bin is placed into a dataframe titled 'spending_summary' and the subgroups/bins (spending ranges) are: "<$585", "$585-630", "$630-645", "$645-680". The school size bins the "Total Students" column into 3 subgroups: "Small", "Medium", "Large". The scores and passing rates for each subgroup is found and placed into the dataframe called 'size_summary'. 

## ** Part VI: School Type Analysis
The last section of the analysis calculates the scores and the passing rates for the 2 school types: "Charter" and "District".  
