## Module 4 Challenge

### <p style="color:#CC6600">Background</p> 

You are the new Chief Data Scientist for your city's school district. In this capacity, you'll be helping the school board and mayor make strategic decisions regarding future school budgets and priorities.  

As a first task, you've been asked to analyze the district-wide standardized test results. You'll be given access to every student's math and reading scores, as well as various information on the schools they attend. Your task is to aggregate the data to showcase obvious trends in school performance.  

### <p style="color:#CC6600">District Summary</p> 

Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.  

Include the following:
* Total number of unique schools
* Total students
* Total budget
* Average math score
* Average reading score
* % passing math (the percentage of students who passed math)
* % passing reading (the percentage of students who passed reading)
* % overall passing (the percentage of students who passed math AND reading)  
<br>

<ins>Final Script Outputs</ins>:<img src="Images/uta_icon_checkmark.svg" width="30" height="12">  <br>
![Results](Images/Results01.png)
<br>

### <p style="color:#CC6600">School Summary</p> 

Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.

Include the following:
* School name
* School type
* Total students
* Total school budget
* Per student budget
* Average math score
* Average reading score
* % passing math (the percentage of students who passed math)
* % passing reading (the percentage of students who passed reading)
* % overall passing (the percentage of students who passed math AND reading)  
<br>

<ins>Final Script Outputs</ins>:<img src="Images/uta_icon_checkmark.svg" width="30" height="12">  <br>
![Results](Images/Results02.png)
<br>

### <p style="color:#CC6600">Highest-Performing Schools (by % Overall Passing)</p> 

Sort the schools by % Overall Passing in descending order and display the top 5 rows.

Save the results in a DataFrame called "top_schools".
<br>

<ins>Final Script Outputs</ins>:<img src="Images/uta_icon_checkmark.svg" width="30" height="12">  <br>
![Results](Images/Results03.png)
<br>

### <p style="color:#CC6600">Lowest-Performing Schools (by % Overall Passing)</p> 

Sort the schools by % Overall Passing in ascending order and display the top 5 rows.

Save the results in a DataFrame called "bottom_schools".
<br>

<ins>Final Script Outputs</ins>:<img src="Images/uta_icon_checkmark.svg" width="30" height="12">  <br>
![Results](Images/Results04.png)
<br>

### <p style="color:#CC6600">Math Scores by Grade</p> 

Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.
<br>

<ins>Final Script Outputs</ins>:<img src="Images/uta_icon_checkmark.svg" width="30" height="12">  <br>
![Results](Images/Results05.png)
<br>

### <p style="color:#CC6600">Reading Scores by Grade</p> 

Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.
<br>

<ins>Final Script Outputs</ins>:<img src="Images/uta_icon_checkmark.svg" width="30" height="12">  <br>
![Results](Images/Results06.png)
<br>

### <p style="color:#CC6600">Scores by School Spending</p> 

Create a table that breaks down school performance based on average spending ranges (per student).

Use the code provided below to create four bins with reasonable cutoff values to group school spending.

```python
spending_bins = [0, 585, 630, 645, 680]
labels = ["<$585", "$585-630", "$630-645", "$645-680"]
```

Use pd.cut to categorize spending based on the bins.

Use the following code to then calculate mean scores per spending range.

```python
spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()
spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()
spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()
spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()
overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()
```

Use the scores above to create a DataFrame called spending_summary.

Include the following metrics in the table:
* Average math score
* Average reading score
* % passing math (the percentage of students who passed math)
* % passing reading (the percentage of students who passed reading)
* % overall passing (the percentage of students who passed math AND reading)  
<br>

<ins>Final Script Outputs</ins>:<img src="Images/uta_icon_checkmark.svg" width="30" height="12">  <br>
![Results](Images/Results07.png)
<br>

### <p style="color:#CC6600">Scores by School Size</p> 

Use the following code to bin the per_school_summary.

size_bins = [0, 1000, 2000, 5000]
labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]
Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.

Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).
<br>

<ins>Final Script Outputs</ins>:<img src="Images/uta_icon_checkmark.svg" width="30" height="12">  <br>
![Results](Images/Results08.png)
<br>

### <p style="color:#CC6600">Scores by School Type</p> 

Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.

This new DataFrame should show school performance based on the "School Type".
<br>

<ins>Final Script Outputs</ins>:<img src="Images/uta_icon_checkmark.svg" width="30" height="12">  <br>
![Results](Images/Results09.png)
<br>

### <p style="color:#CC6600">References</p>

Data generated by <a href="https://mockaroo.com" target="_blank">Mockaroo, LLC</a> , (2022). Realistic Data Generator. Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.  📚  
<br>
<br>
<br>
![UTlogo](Images/utaustin-mccombs.png)      <img src="Images/edx-logo-elm.svg" width="200" height="80"> 
