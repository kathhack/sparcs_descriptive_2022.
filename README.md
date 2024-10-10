# sparcs_descriptive_2022.

Python Assignment: Descriptive Analytics on SPARCS 2022 Data
Project Title: SPARCS Descriptive 2022
Objective:
In this assignment, you will load a portion of the 2022 SPARCS (Statewide Planning and Research Cooperative System) de-identified data. You will perform basic descriptive statistics and create visualizations based on the data. This will allow you to explore healthcare trends, patient demographics, and hospital performance metrics.

By the end of this assignment, you will have uploaded your Python notebook and analysis to a GitHub repository named "sparcs_descriptive_2022".

Data Source:
The dataset can be found at: Hospital Inpatient Discharges - SPARCS De-Identified 2022.

We will use a subset of this dataset focusing on key fields, including:
Age Group
Gender
Length of Stay
Type of Admission
Total Charges
Total Costs
Discharge Year
Ethnicity
Race


Instructions:
Setup your GitHub Repository:

Create a GitHub repository named sparcs_descriptive_2022.
Your repository should include a README.md file explaining the analysis.
Loading the Data:

Use the dataset available from the link above, or download the file and load a subset of it into your Python environment using Pandas.
Ensure that the data includes the fields Age Group, Gender, Length of Stay, Total Charges, Total Costs, and Type of Admission.
Basic Descriptive Statistics:

I imported pandas as PD, and I added the CSV link.
I was having trouble with colab reading the column I needed to start with "Hospital County" so I edited the excel to change County to one word, and added underscores to the titles of other column headers so there was no white space. I then readded the CSV document to Google Colab.

I added some of the code that was in our example from class, and then worked to get the data to be only Nassau + Suffolk counties, and then only the fields listed above as columns to include in the data set. 

## Not sure why the actual name of the column for counties is not working in the code
## I edited the column titles in Excel to add underscores to the multiword column headers to eliminate white space in case that was the issue. I had already played around with multiple spelling/capitalizations and it still wouldn't read the column header
## I also made Hospital County into just County in the excel because of the trouble I was having getting the code to work with the title name. I am hoping the underscores I added to remove white space in column headers will help me later on, we shall see.

##still has other counties other than suffolk. 
#checking my work
My sample list only had Nassau, so I ran another one of more than just the first 5 lines
# want a random sample of the filtered data, not just the first 5 lines, to make sure more than Nassau is included.
#ensuring the data set includes the fields Age Group, Gender, Length of Stay, Total Charges, Total Costs, and Type of Admission.

Calculate the following basic statistics for Length of Stay, Total Charges, and Total Costs:
Mean
Median
Standard Deviation
Min/Max
Percentiles (25th, 50th, 75th)
Quartiles
Exploring Categorical Variables:

# Convert the relevant columns to numeric, coercing errors into NaN

##wondering if I'm having issues with the data because I downloaded the data to edit the column headers, so maybe some number data was converted weirdly?

then I did the rest of the mathematical coding

Count the distribution of Age Group, Gender, and Type of Admission.

#Exploring Categorical Variables:
#Count the distribution of Age Group, Gender, and Type of Admission.
#Create a bar plot to visualize the counts of each category.

Create a bar plot to visualize the counts of each category.
Visualizations:

Create at least 3 visualizations to summarize the dataset:
Histogram of Length of Stay to show its distribution.
Boxplot for Total Charges to identify outliers.
Bar plot for Type of Admission to analyze admission trends (e.g., Emergency, Elective, Trauma).
Handling Missing Data:

Check for missing data in the selected fields and handle it appropriately (e.g., drop rows with missing data or fill with the mean/median).



Summary Report:

Write a brief summary of your findings in the notebook:
What is the average length of stay? 4.37 days
#Summary Report:
#Average length of stay: 
# Calculate the average length of stay
average_length_of_stay = filtered_df_cleaned['Length_of_Stay'].mean()

# Print the result
print(f"The average length of stay is: {average_length_of_stay:.2f} days")

How does the total cost vary by age group or type of admission?
#The cheapest cost is for the age group 30-49, with the second cheapest group (by average total cost) to be the 0-17 age range. 18-29 years old is the highest average total cost by age group,
# with 70 or older being the second highest group. 
#As for type of admission, Urgent admissions are the highest average total cost. 

Any noticeable trends in admissions or charges?
# noticable trends - look into age group and their average total charges and admission counts
#I'm curious about the difference between urgent and emergency. It turns out Emergency is a life-threatening condition, while urgent needs prompt attention but not life-threatening. 
#This makes sense why there are so many more urgent than emergency admissions.
#As a patient myself, I wonder if that is because urgent care centers are so popular these days so a lot of people go to urgent care when they are sick, vs waiting for a primary visit
#or not having a primary care doctor, but urgent cares are everywhere. 
#One would only go to the emergency room for something really bad and/or after hours

Deliverables:
A Python notebook (.ipynb or .py file) uploaded to a GitHub repository called sparcs_descriptive_2022.
Your notebook should contain:
Data loading steps
Basic descriptive statistics
Visualizations
Summary of findings
Include a README.md file explaining the project and how to run the notebook.

Optional Extensions (Extra Credit):
Analyze the Ethnicity and Race fields to explore healthcare disparities in total charges or length of stay.
Use seaborn to create more advanced visualizations (e.g., heatmaps or pairplots).
*I tried a few times, but I hadn't added Ethnicity into my column sorting earlier, and when I tried to for this, I got the same error I had from the start where the column header wasn't recognized. I tried to work around it a few times, but didn't have any luck. I need to ask about what to do when that happens, because I don't want to manipulate the data source, there has to be a fix when the column is spelled correctly and typed correctly, for it to show up correctly when I pull for it. 

Submission:
Submit the link to your GitHub repository.
Ensure that all code, visualizations, and your final report are included.
