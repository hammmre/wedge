
# Applied Data Analytics

## Wedge Project

<!-- Any general commentary you'd like to say about the project --> 
In task 1, I think I managed to find the least efficient route possible, but made it work! It is interesting to utilize data from messy start to more cleaned up finish. In the data that I collect and utilize on a daily basis, I am so intimately familiar with it that cleaning it feels very different - of course, it is also a different scale than this project - so it is interesting to have to figure out what is going on with data that I am not familiar with.

### Task 1

* Files for this task: 

[Task 1 notebook](Task1.ipynb):
Loads all data into GBQ data set. Reads in full data, cleans data, creates a new csv of the cleaned data, exports cleaned data to GBQ.



### Task 2

* Files for this task: 

[Task 2 notebook](Task2.ipynb): Also includes extraction of data from zipped files. Connects to GBQ instance, builds a list of owners, takes a sample of the owners, extracts all records associated with those owners and writes them to a local text file.
[Owners Sample](Task_2_Owners_Sample.txt): The text file output of all records associated with a sample of owners


### Task 3

* Files for this task: 

[Task 3 notebook](Task3.ipynb): Builds a SQLite database containing 3 tables. Creates summary tables and builds the database.
[3 tables](Task_3_bigquery_results.db): The SQLite database containing the 3 tables.


## Query Comparison Results

Fill in the following table with the results from the 
queries contained in `gbq_assessment_query.sql`. You only
need to fill in relative difference on the rows where it applies. 
When calculating relative difference, use the formula 
` (your_results - john_results)/john_results)`. 



| Query                                 | Your Results | John's Results | Difference | Rel. Diff     |
|---------------------------------------|--------------|----------------|------------|---------------|
| Total Rows                            | 100551819    | 85760139       | 14791680   | 0.172477332   |
| January 2012 Rows                     | 1153841      | 1070907        | 82934      | 0.077442766   |
| October 2012 Rows                     | 1042287      | 1042287        | 0          | 0             |
| Month with Fewest                     | 2            | 2              | No         | NA            |
| Num Rows in Month with Fewest         | 6681041      | 6556770        | 124271     | 0.018953082   |
| Month with Most                       | 5            | 5              | No         | NA            |
| Num Rows in Month with Most           | 9844196      | 7578372        | 2265824    | 0.298985587   |
| Null_TS                               | 2140775      | 7123792        | -4983017   | -0.699489401  |
| Null_DT                               | 0            | 0              | 0          | 0             |
| Null_Local                            | 270502       | 234843         | 35659      | 0.151841869   |
| Null_CN                               | 0            | 0              | 0          | 0             |
| Num 5 on High Volume Cards            | 14987        | 14987          | No         | NA            |
| Num Rows for Number 5                 | 535885       | 460630         | 75255      | 0.163374075   |
| Num Rows for 18736                    | 13995        | 12153          | 1842       | 0.151567514   |
| Product with Most Rows                | banana organic | banana organic | No         | NA            |
| Num Rows for that Product             | 1078387      | 908639         | 169748     | 0.186815666   |
| Product with Fourth-Most Rows         | avocado hass organic | avocado hass organic | No         | NA            |
| Num Rows for that Product             | 523929       | 456771         | 67158      | 0.147027723   |
| Num Single Record Products            | 2506         | 2769           | -263       | -0.094980137  |
| Year with Highest Portion of Owner Rows | 1970       | 2014           | Yes        | NA            |
| Fraction of Rows from Owners in that Year | 1         | 0.7591         | 0.2409     | 0.317349493   |
| Year with Lowest Portion of Owner Rows  | 2011       | 2011           | No         | NA            |
| Fraction of Rows from Owners in that Year | 0.7374    | 0.7372         | 0.0002     | 0.000271297   |


## Reflections

<!-- I'd love to get 100-200 words on your experience doing the Wedge Project --> 
At some point, I realized my method for task 1 was pretty inefficient and was getting messy, but then I didn't want to start over entirely, so I pushed through with it. I also somehow forgot that I had done so much work during labs, but I had already dug myself in when I realized I should go back and watch labs from much earlier. But I do feel that I learned a lot and if I were to redo it or do another similar project, it would go much smoother.