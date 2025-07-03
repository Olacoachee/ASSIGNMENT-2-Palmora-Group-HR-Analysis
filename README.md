# ASSIGNMENT2: Palmora Group HR Analysis
# Company Overview
The Palmoria Group, a manufacturing company based in Nigeria, is embroiled in issues bordering on gender inequality in its 3 regions. Unfortunately, the media recently published the news with the headline “Palmoria, the Manufacturing Patriarchy”. This doesn’t look good for the owners of the business, based on their ambition to scale the business to other regions and even overseas. Cases like this can only spiral downwards, revealing other issues like the gender pay gap, amongst other possible issues.
## CEO of Palmoria Intention to Tackle Company Major Challenges
The CEO of Palmoria, Mr Ayodeji Chukwuma, is keen to address these issues before they get out of hand. The CHRO, Mr Yunus Shofoluwe, has been assigned the task to identify key areas within the business that could give rise to issues and address them immediately. Mr Shofoluwe decided to recruit you as an HR Analytics expert to analyse the company’s HR data and come up with recommendations for management’s attention. “Now, the future of gender equality in Palmoria lies in your hands” the exact words of Mr Shofoluwe before he handed the data to you.
## Palmoria Group HR Analysis Assignment Portfolio
This is to officially welcome you to the Palmoria Group Analysis Portfolio. This repository includes a well detailed analysis of the organization's employees data, different questions raised by the Chairman of the company were addressed and useful information. This portfolio was built to provide valuable insights for the management of the organization to address the challenges associated with gender equality, compliance with increment regulations, salary structure, and bonus distribution.
## Data Source
Data (Palmoria Group HR Analysis.CSV) [DOWNLOAD HERE](https://canvas.instructure.com/courses/11955369/files/folder/DSA%20Capstone%20Project%20Files) used in this analysis was shared and gotten through the SML channel from the DSA cordinators for the DSA data analysis program.
## Tools Used
- Microsoft Power BI [DOWNLOAD HERE](https://www.microsoft.com/en-us/download/details.aspx?id=58494)
  - For data cleaning
  - For transformation
  - For data query
  - for data analysis
  - For data visualization
 # Data Preparation and Cleaning
  ## Gender Column
There were two gender (Male and Female) in organization as indicated in the dataset by some employees, while others refused to disclose their gender. As a result a generic gender status “Other” was assigned. To fill this 43 empty cells in the gender column with “Other” using power BI using a Conditional Column, follow these step-by-step instructions using Power Query Editor.
**Step-by-Step in Power BI**

**Loa of data file:** File was first load into the power BI after which,

**Open Power Query Editor:** In Power BI Desktop, click on Home > Transform data

**Select Table:** In the Power Query window, I selected the table that contains the Gender column.

**Add a Conditional Column:** By go to the top ribbon:I added a new Column > Conditional Column

**Configure the Conditional Column:** The conditional column was configured as show the image below.
<img width="688" alt="gender conditional column" src="https://github.com/user-attachments/assets/9c98af93-3d89-44ed-9ea3-f9a053caeaf3" />

## Salary Column
As part of the requirements, some of the employees were with no salary which may be due to them leaving the organization prior to the analysis. Therefore, it is important those employees are taking out to promote data robustness and efficiency. To remove those employees without salary in excel, the follow steps were taken:
### Using Filter
a.  **Select the Data Range:** The data was selected including the column headers.

b.  **Filter Application:** Filter drop-downs was clicked to the salary column header. 

c.   **Filter of Salary Column:**  Filter drop-downs on the salary column was clicked to bring out filter by values and the blank (null) values (43) was selected and then enter OK.

## Department Column
Some departments are indicated as “NULL” . To remove those employees with Null as department in power BI, the follow steps were taken:
### Using Filter 
I.  **Select the Data Range:** The data was selected including the column headers.

II.  **Filter Application:** Filter drop-downs was selected to the department column header. 

III.   **Filter of Department Column:**  Filter drop-down on the department column was clicked to bring out filter by values and the NULL values (26) was selected and then enter OK. 
# Pointers from Mr Gamma
In this stage, Exploratory data analysis (EDA) was carried out by examined the datasets in order to provide answers to all the pointers.
## Data Analysis
This is where I carried out some basic lines of code/queries during the analysis and visualization of data.
# Question 1
*What is the gender distribution in the organization? Distil to regions and departments*

First thing that I did was to launched my power BI after which the Palmoria Group HR Analysis Dataset was imported. To attempt question 1, analyzing the gender distribution in the organization in respect to region and department.  The following steps were followed:

**Add New Column:** Since there is no column in the dataset with Region, there is need to create a new column (Region). To generate regions for each location, I used a  add conditional column.




**Build the Pivot Table** 
1. Drag Gender to the Values area. Ensure it is set to "Count" (default).
2. Drag Region to the Rows area.
3. Drag Department below Region in the Rows area.

**Visualization:** To make the data more presentable, I visualized the data using a stacked bar chart.

![Picture1](https://github.com/user-attachments/assets/7d1ab374-1dbd-4dda-8ebd-3b2397e88570)

# Question 2
*Show insights on ratings based on gender*

To analyze rating based on gender in excel, there is a need for numeric rating therefore new column was created named “Rating Numeric” 

**Create New Column:**  To create a numeric scale for ratings based on the qualitative descriptions (Very Poor, Poor, Average, Good, Very Good), I assigned values as follows:
1. Very Poor: 1
2. Poor: 2
3. Average: 3
4. Good: 4
5. Very Good: 5

Then I used the IF formula to assign numeric value for the first cell and then used flash fill to generate the rest column cells  based on the qualitative descriptions in the Rating column. ```=IF(G464="VeryPoor",1,IF(G464="Poor",2,IF(G464="Average",3,IF(G464="Good",4,IF(G464="Very Good",5,"")))))```

**Create a Pivot Table:** A pivot table was created in a separate sheet by selecting the entire dataset then go to insert and click on pivot table to place in a new worksheet.

**Build the Pivot Table** 
1. Drag Gender to the row area. 
2. Drag Rating Numeric to the value area. Ensure it is set to "average" (default).

**Visualization:** To make the data more presentable, I visualized the data using a clustered column chart and the chart show valuable insights as avearge employee has a 3/5 rating.

![Picture2B](https://github.com/user-attachments/assets/241d9e81-c160-4e93-bd11-5c768f4d1583)


# Question 3
*Analyse the company’s salary structure. Identify if there is a gender pay gap. If there is, identify the department and regions that should be the focus of management*

In order to examine the salary structure of the company and any gender pay gaps by region and department within it in Excel, I followed the below steps:

**Set up Pivot Table**

- Drag Gender to Rows area.

 - Below the Gender in the Row area I Drag Region and Department.

- Drag Salary to the Values.

  - For the aggregation, I set it to average (default: Sum).

This displayed the average salary by gender, department and region.

**Visualization:** To make the data more presentable, I visualized the data using a clustered bar chart and there is no significant gender salary gap in respect to region.

![Picture3b](https://github.com/user-attachments/assets/c096e7f8-349a-4735-9155-7442317cd313)


# Question 4
*A recent regulation was adopted which requires manufacturing companies to pay employees a minimum of $90,000*
















