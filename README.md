# TeacherSalary
## Intro
This is a Code Louisville project for the Python class.

Teacher salaries across the US are in jepeordy due to decreased funding thoughout the education system and the attempt to privatize education using charter schools. Different states have different systems and pressures effecting teacher compensation.  The goal of this project is to enable the user to compare teacher salary trends between states of their choice over the last 20 years.  

Future development will enable the user to compare teacher salaries vs other salaries to see if salaries are keeping pace with which occupations.  The data for this is already in the .xls files.
 
## Project Process
The data set consists of 20 .xls files from the US Census Dept.  Each file holds the annual wage and salary data for all occupation  titles.  20 files = 20 years. 

File containing project code: **CLProject_Python_TeacherPay.ipynb**

### Process order
1. Jupyter Notebook Cell 1 :
    - Database created
    - Loop through each .xls file 
        - Load data into DataFrame
        - Clean routine on data
        - Insert into TeacherPay table
    - Consolidate just teacher pay into new table
        - Query TeacherPay table
        - Insert query results into ConTPay table

2. Jupyter Notebook Cell 2 :
    - Get user imput of 5 states to analyse
    - Query ConTPay for 5 state data
    - Display line graph comparing 5 states
    


## Set Up
This project was built using Jupyter Notebooks and includes the use of the Seaborn package and several others.  

There are two cells to run in Jupyter Notebooks.  The first creates the database and tables while the second is the user interactive section that results in a graph of user selected parameters (comparison of states teacher salary trends).

### Mandatory Dependencies:
* Jupyter Notebooks with below environment
* Python
* Libraries for environment:
    *  seaborn (>=0.9.0)  
        * Anaconda will only load up to v.0.8.1 so use:
        ```pip install seaborn==0.9.0``` in conda terminal
    * numpy (>= 1.14.3)
    * matplotlib (>= 2.2.2)
    * scipy (>= 1.1.0) 
        * not used in project but requirement of Seaborn 0.9.0)
    * pandas (>= 0.23.0)

### Script to check your package versions:
```
import seaborn as sns
import numpy as np
import matplotlib as mpl
import scipy as sp
import pandas as pd

print("Seaborn", sns.__version__,"\nNumpy",np.__version__,"\nMatPlotLib",mpl.__version__,"\nScipy",sp.__version__,"\nPandas",pd.__version__ )
```

















## Project requirements checklist

- [x]  Must include a README file that states the following:

- [x]  What question are you answering or problem are you analyzing

- [x]  A brief overview of how you accomplished this, including any necessary background for someone to understand the problem, where your data came from, what you used from that data, any analysis you applied to the data, and what you chose to visualize/display/report in the final product

- [x]   Any special requirements, dependencies, or steps to run the project

- [x]   You must include a SQL database (MySQL or SQLite) where your data will be stored

- [x]   You need to include the script that sets up/creates your database

- [x]   You must include a Python script used to fetch data from a data source and load it into your SQL database

- [x]   Your data source may be an external API, database, a CSV file, or any other data source that you can read/parse via Python code

- [x]   You must include a Python script to retrieve the data from your SQL database into a Python object

- [x]   Visualize the results of your analysis using Matplotlib, Seaborn, Bokeh or another Python Data Visualization library. 

- [x]   Your results cannot be a plain text representation and you 
are encouraged to explore a visualization approach that clearly supports a conclusion/result of the analysis of your data.

- [x]   Your data retrieval for visualization uses at least one SQL query, meaning you can't parse records from your data set using only Python or an ORM. Pushing and retrieving an entire dataframe to and from SQL also does not meet the requirement, e.g. the SQL query should not simply be SELECT * FROM database

- [x]   Your project is uploaded to GitHub