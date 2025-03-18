
# HR Analytics Dahsboard
## Drive link for the Dashboard, you can download and view it.
https://1drv.ms/u/c/6073c47068aa175c/EQZEGV4rVVhNv1CTt1wqctEBlV5KbU4pxejYoN2EWuTPhg?e=eTImAB

## Problem Statement

Employee attrition is a critical challenge for organizations, impacting productivity, morale, and overall business performance. Understanding the underlying reasons for employee turnover is essential for improving retention strategies and creating a more engaging work environment. This dashboard aims to provide insights into the factors influencing employee attrition within the company. By analyzing various attributes such as age, education field, years at the company, job role, and salary, the dashboard helps identify trends and patterns related to employee departures.

Key questions addressed include:

1.How does age impact attrition rates?

2.Does educational background influence the likelihood of leaving the company?

3.What role does tenure or years spent at the company play in attrition?

4.Are certain job roles or salary bands more likely to experience higher turnover?

The insights provided by this dashboard are intended to guide HR teams and management in making data-driven decisions to improve retention and create a more supportive work culture.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is HR, which is a csv file.

- Step 2 : Open power query editor & check for missing values and errors.

  We can see a column called YearsCurrCompany which has missing values.Since we don't need this column, we are deleting it.

- Step 3 : After removing the unwanted column, Now we need to remove the duplicate values from our data by selecting all the columns and clicking the remove duplicates.

- Step 4 : Now we will look for spelling errors. There is one in a column called BusinessTravel. In it's values there is 'travel_rarely' and 'travelrarely'. We replace it with 'travel_rarely'.

- Step 5 : Check whether all the columns are assigned the correct datatype or not. 

- Step 6 : Then we hit close and apply button to close the Power Query Editor.

- Step 7 : In this step, we calculate the Attrition Count based on the "Attrition" column, which indicates whether an employee has left the company ("Yes") or stayed ("No"). We use the SWITCH function to assign a numeric value:

If the Attrition value is "Yes", it assigns a count of 1, indicating the employee has left.

If the Attrition value is "No", it assigns a count of 0, indicating the employee is still with the company.

For any other value in the Attrition column, we default to 0.

Snap of the calculated column-

![Image](https://github.com/user-attachments/assets/65539d99-9d11-4e33-8648-ac5057cff5fb)

- Step 7 :In this step, we calculate the Attrition Rate using the following formula:

AttritionRate = SUM(HR_Analytics[Attrition Count]) / SUM(HR_Analytics[EmployeeCount])

SUM(HR_Analytics[Attrition Count]): This part sums up the Attrition Count values, which represent employees who have left the company.

SUM(HR_Analytics[EmployeeCount]): This part sums up the total number of employees in the dataset.

By dividing the total number of employees who have left by the total number of employees, we calculate the Attrition Rate. This measure gives us the percentage of employees who have left the company, providing an overview of employee turnover within a given period or across different employee groups.

Snap of the calculated measure-
 
![Image](https://github.com/user-attachments/assets/317fdebd-4f24-4bdb-844f-e41c704ce359)

- Step 8 : In the report view, under the view tab, the background was imported and edited.

- Step 7 : In the report view, under the insert tab, we selected the text box from the home tab. We used this text box to set our title.

- Step 8 : Visual filter (Slicer) was added for filtering the data based on department.

Snap of the slicer - 

![Image](https://github.com/user-attachments/assets/53fe37ed-0ffe-405e-8ed2-e2cfae2e330b)


- Step 9 : Six card visuals were added to the canvas:

  1. First one representing the count of employees which is 1.47K.

  Snap of the Card Visual:

  ![Image](https://github.com/user-attachments/assets/1600651a-61f4-4c9e-a882-a9c381563cf2)

  2. Second one represents the sum of Attrition Count which is 237.

  Snap of the Card Visual:

  ![Image](https://github.com/user-attachments/assets/e224b82c-fa0a-4df2-9d98-a22949e9ebc2)

  3. Third one represents the Attrition Rate which is 16.1%.

  Snap of the Card Visual:
  
  ![Image](https://github.com/user-attachments/assets/78488920-cd54-4ae5-9121-f6fe65bd46b5)

  4. Fourth one representing the Average Age of the employees, i.e., 37.

  Snap of the Card Visual:
  
  ![Image](https://github.com/user-attachments/assets/4559f36b-e273-42ee-bbf5-cd3512062ca1)

  5. Fifth One represents the Average Salary which is 6.5K.

  Snap of the Card Visual:

  ![Image](https://github.com/user-attachments/assets/b63e4005-01b5-4867-9304-3eae7616627c)

  6. Sixth One represents the Average Years At Company which are 7 years.

  Snap of the Card Visual:

  ![Image](https://github.com/user-attachments/assets/fb5dcce4-ab2f-474f-b5f2-535d38e6df89)

- Step 10 : A donut chart was added to the report design area representing the count of attrition by Education Field like Marketing, Medical, Life Sciences etc . The highest number of employees leaving were from the Life Sciences field with a rate of 41%.

- Step 11 : A stacked column chart Visual was used to represent the sum of Attrition Count by Age Group i.e., 18-25, 26-35, 36-45, 46-55, 55+.And turns out the highest number of employees leaving were from the Age Group 26-35.

- Step 12 : In the report view, from the visualizations pane, we selected a matrix to show the sum of attrition count by job satisfaction rating (1-4) across different job roles.

- Step 13 : In the report view, from the visualizations pane, we selected a stacked bar chart to represents sum of Attrition Count by Salary. The highest count of people who left the company had a salary upto 5K.

- Step 14 : In the report view, from the visualizations pane, we selected a Are chart to represents sum of Attrition Count by Years At Company.The highest count of people who left the company did so after they completed one year at the company.
        
- Step 15 : In the report view, from the visualizations pane, we selected a  stacked bar chart to represents sum of Attrition Count by JobRole. We then filtered it to show the Top four records, out of which laboratory technician had the highest attrition value of 62.

# Snapshot of Dashboard (Power BI Desktop)

![Image](https://github.com/user-attachments/assets/f4e2eb75-2544-4cd8-b5c1-c01bc7b1fd0e)

# Report Snapshot (Power BI DESKTOP)

![Image](https://github.com/user-attachments/assets/eac0dd3c-8106-42d3-bfd6-76214e3dfdd8)

# Insights

A single page report was created on Power BI Desktop.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Employees who left the company = 1.47K

   Sum of Attrition Count (Male) = 140 

   Sum of Attrition Count (Female) = 79


  thus, higher number of Employees by Attrition Count are Male.

### [2] Sum of Attrition Count By Age Group 
  18-25 : 44
  26-35: 116
  36-45: 43
  46-55: 26
  55+: 8

We can conclude that People from Age Group 26-35 left more.

  ### [3] Attrition By Salary
   Upto 5K: 163
   5k-10K: 49
   10K-15K: 20
   15K+: 5
 so the people who left the most had a salary of upto 5K.

 ### [4] Attrition By JobRole
  
 1.) Laboratory Technician had an Attrition Count of 62.

 2.) Sales Executive had an Attrition Count of 57.

 3.) Research Scientist had an Attrition Count of 47.

 4.) Sales Representarive had an Attrition Count of 33.
 
# HR_Analytics.md.txt
Displaying # HR_Analytics.md.txt
