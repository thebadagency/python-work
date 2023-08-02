# python-work
Work to show my evolving skills with python.

#### WORK ADDED AS OF 07.25.2023 #####
I was presented with an interesting challenge by Achievement First, who found themselves with CSV files of student data from their Student Information System, Infinite Campus due to unforeseen circumstances. The CSV files were 'calendar.csv', 'person.csv', 'enrollment.csv', 'school.csv', and 'schoolyear.csv'. The goal was to analyze this data and extract meaningful insights.

The first step in my process was setting up a Python development environment on an Ubuntu virtual machine. I installed Python and several necessary libraries including pandas, sqlite3, and requests. I also created a new directory, 'PythonProjects', on my desktop to house all the project files.

To begin the data analysis, I loaded the CSV files into pandas dataframes. Then, I used these dataframes to populate a SQLite database named 'ic.db'. I set up logging to record the process, and printed and logged the result of each operation.

I wrote a function to execute SQL queries on the database. I first used this function to set the active school year to 2020 in the 'schoolyear' table. Then, I executed SQL queries to answer the following questions:

How many unique students are enrolled in the active school year?
How many students were enrolled in school 'bp' as of 10/1/2019?
Who are the three students with the most recent startdate of the students that have multiple enrollments in the active school year?
I printed and logged the results of these queries.

Next, I further manipulated the data using pandas in Python. I augmented the 'school' dataframe with a 'city' column, populated using data pulled from the Zippopotam.us API. I also augmented the 'enrollment' dataframe with a 'final_enddate' column, which was either the 'enddate' as reported in the enrollment dataframe, or the 'calendar_enddate' for that enrollment record if 'enddate' was missing.

Finally, I created an 'active_enrollment' dataframe by merging the 'enrollment' dataframe with the 'school' dataframe, adding additional columns such as 'schoolid', 'schoolname', 'endyear', 'city', and 'final_enddate'. This dataframe was then exported as a CSV file.

I committed the entire project, including the Jupyter notebook, the updated SQLite database, and the CSV file, to a local git repository and pushed it to my remote GitHub repository. All of my work can be found at my GitHub account at this link: https://github.com/thebadagency/python-work/.

In the GitHub repo, you can take a look at the code by checking out the Jupyter notebook: AchievementFirst.ipynb, examine the SQLite DB: ic.db, and review the exported csv as a result of my queries and code: active_enrollment.csv.
