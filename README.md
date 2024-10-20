# Wedge
ADA Wedge Project

Task 1: Building a Transaction Database in Google Big Query
Google Big QueryLinks to an external site. is a distributed data warehouse built on a serverless architecture[1]. We’ll discuss this framework in class. In this task, you’ll upload all Wedge transaction records to Google Big Query. You’ll want to make sure that the column data types are correctly specified and that you’ve properly handled the null values.

The requirements for this task change depending on the grade you’re going for.

Note: this assignment can be done manually or programmatically. Naturally, I’d prefer it be done programmatically so that you get more practice, but that’s not required to get full credit.

[1] Amazon has a competitive product called Redshift. A comparison can be found hereLinks to an external site.. Microsoft’s Azure has some offerings in this space (Data Lake), but they seem a bit behind the curve at this point.

Task 2: A Sample of Owners
These files are not easy to use in their current chronological arrangement, though having them in a large system like GBQ will solve a lot of our problems. Nevertheless, it’ll be convenient to have a local sample of owners to do work.

This task asks you to generate a file of owners where the file contains every record for each owner. There will be more than one owner in the file, and I do not want you to include card_no==3, which is the code for non-owners. The size of the sample is up to you, but I’d recommend shooting for a sample that’s around 250 MB. That’s big enough to be rich, but small enough to be fast. Ish.

Deliverable
A Python script that handles the following tasks:

Connects to your GBQ instance.
Builds a list of owners.
Takes a sample of the owners.
Extracts all records associated with those owners and writes them to a local text file.
You’ll submit your code carrying out the steps.

Task 3: Building Summary Tables
It is useful to have summary files that allow you to quickly answer questions such as the following:

How have our sales-by-day changed over the last few months?
What is our most popular item in each department?
Which owners spend the most per month in each department?
The classic way to structure data to answer these questions is in a relational database. In this task, you will build the summary text files that hold this data and populate a relational database with the data.

Input
You will process your owner records in GBQ to build the summary tables.

Output
For this task, you will build a single SQLite database via Python (in a .db file) containing three tables:

Sales by date by hour: By calendar date (YYYY-MM-DD) and hour of the day, determine the total spend in the store, the number of transactions, and a count of the number of items[1].
Sales by owner by year by month: A file that has the following columns: card_no, year, month, sales, transactions, and items.
Sales by product description by year by month: A file that has the following columns: upc, description, department number, department name, year, month, sales, transactions, and items.
You will submit your Python code that builds the database.

You are welcome to generate these tables via queries in Google Big Query, export the text files, and store them locally on your machine. Then you will need to write a Python script that creates the database, creates the tables, and fills those tables. Obviously, it’d be great to do the whole thing in Python.

[1] We can identify the number of items by looking for trans_status of ‘’ or ‘ ‘ (blank string or a single space). To be completely correct you would want to remove Returns (R) and Voids (V) as well. I’ll give you a query that helps with this.

Deliverable
The Python code that creates the summary tables. The Python code that builds the database.

Project Tiers by Grade
This project has multiple potential entry points. We will allow students going for different grades to do different amounts of work on this project.

A Grade
Students going for an A grade will perform all tasks. Exercises during the course will provide code to help those students perform Task 1.

B Grade
Students going for a B will receive cleaned transaction files from the Wedge zipped files. It’s still good to know how to clean those files, but your work on Task 1 will begin with the uploading the data to Google BigQuery.

C Grade
Students going for a C are allowed to skip Task 1. Clean versions of the Wedge data exist up on BigQuery at the following location: https://console.cloud.google.com/bigquery?project=umt-msba&folder=&organizationId=&p=umt-msba&d=transactions&page=datasetLinks to an external site.. You can use these tables to perform tasks 2 and 3.

