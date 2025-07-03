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

<img width="683" alt="Region conditional column" src="https://github.com/user-attachments/assets/df567902-3505-4422-b0b1-9f7fa9aa7ebb" />

**Build the visual** 
1. Drag Gender to the X axis area. Ensure it is set to "Count" (default).
2. Drag Region to the legend area.
3. Drag Department to Y axis area.

**Visualization:** To make the data more presentable, I visualized the data using a stacked bar chart.

<img width="364" alt="ASS1" src="https://github.com/user-attachments/assets/c72de8ef-dd4b-44ae-b3e1-79e1e435fb76" />

# Question 2
*Show insights on ratings based on gender*

To analyze rating based on gender;

**Build the visual** 
1. Drag Name to the X axis area. Ensure it is set to "Count" (default).
2. Drag Gender to the legend area.
3. Drag Rating to Y axis area.

**Visualization:** To make the data more presentable, I visualized the data using a clustered bar chart as show below.

<img width="353" alt="ASS2" src="https://github.com/user-attachments/assets/2732145a-78eb-47da-ab74-2298238148f9" />

# Question 3A
*Analyse the company’s salary structure. Identify if there is a gender pay gap. If there is, identify the department and regions that should be the focus of management*

In order to examine the salary structure of the company and any gender pay gaps by region and department within it, I followed the below steps:

**Build the visual** 
1. Drag Gender to the X axis area. 
2. Drag Salary to Y axis area. For the aggregation, I set it to average (default: Sum).

This displayed the average salary by gender.

**Visualization:** To make the data more presentable, I visualized the data using a clustered Column chart and there is no significant salary gap in respect to genders.

<img width="355" alt="ASS3A" src="https://github.com/user-attachments/assets/eabdfce1-bf54-42ef-a621-21a516de4e38" />

# Question 3B
*Analyse the company’s salary structure. Identify if there is a gender pay gap. If there is, identify the department and regions that should be the focus of management*

In order to examine the salary structure of the company and any gender pay gaps by region and department within it, I followed the below steps:

**Build the visual** 
1. Drag Salary to the X axis area. Ensure it is set to "average" (default).
2. Drag Region to the legend area.
3. Drag Department to Y axis area.

This displayed the average salary by region and department.

**Visualization:** To make the data more presentable, I visualized the data using a stacked bar chart and there is no significant salary gap in respect to Department and Regions.

<img width="367" alt="ASS3B" src="https://github.com/user-attachments/assets/61eb422c-72b5-4dd2-a92d-249e2c02db02" />

# Question 4
*A recent regulation was adopted which requires manufacturing companies to pay employees a minimum of $90,000*

**4A** Does Palmoria meet this requirement?

To determine whether Palmoria meets the recent regulation requiring a minimum salary of $90,000, follow these steps in power BI:

**Add New Column:** Since there is no column in the dataset with Compliance, there is need to create a new column (compliance). To show if the salary of each employee is up to the recent minimum $90,000 regulation requirement for manufactoring companies, using add conditional column.

<img width="669" alt="Compliance conditional column" src="https://github.com/user-attachments/assets/c3c9383b-f517-4104-a24a-895c16df66d0" />

**Build the visual** 
1. Drag Name to the value axis area. Ensure it is set to "count" (default).
2. Drag Compliance to the legend area.

This displayed the percentage of employees that meet the requirement (Complaint and Non Compliant).

**Visualization:** To make the data more presentable, I visualized the data using a pie chart.

<img width="318" alt="ASS4A" src="https://github.com/user-attachments/assets/a2d3c76a-3684-4824-8474-815d471894e3" />

# Question 4
*A recent regulation was adopted which requires manufacturing companies to pay employees a minimum of $90,000*

**4B** Show the pay distribution of employees grouped by a band of $10,000. For example:
How many employees fall into a band of $10,000 – $20,000, $20,000 – $30,000,etc.? Also visualize this by regions.

To analyze and visualize pay distribution by $10,000 bands in Power BI, including breakdown by regions.

**Create a Salary Band Column**
To group employees by salary bands (e.g., $10,000–$20,000), I create a new gropu in Power BI by right click on Salary and then new group renamed to (Salary Band) as show in the picture below.


















