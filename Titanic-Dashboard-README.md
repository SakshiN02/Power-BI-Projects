
# Titanic-Dashboard
## Drive link for the Dashboard, you can download and view it.
https://1drv.ms/u/c/6073c47068aa175c/EdcJSAW-m01LiuWEsX-UIvkBilwUczTGMgKVu6h27970-w?e=482yny

## Problem Statement

The sinking of the Titanic is one of the most infamous shipwrecks in history.

On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew.

While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others.

In this challenge, we build a dashboard that answers the question: “what sorts of people were more likely to survive?” using passenger data (ie name, age, gender, socio-economic class, etc).

### Steps followed 

- Step 1 : Load data into Power BI Desktop, datasets are train and test data, which are csv files.

- Step 2 : Open power query editor & check for missing values and errors.

- Step 3 : Also remove the unwanted columns. Now we need to merge both the datasets(merge queries from home tab) to get our titanic dataset.

- Step 4 : Then we hit close and apply button to close the Power Query Editor.

- Step 5 : For calculating Age Group Column, we used the Age column that we have and divided it into catergories: 0-10,10-20,20-30, 30-40, ....71 +.
Snap of the Values in calculated column-
![Image](https://github.com/user-attachments/assets/1f9f6a9b-8943-47ad-b31a-935fbfd261ee)

 Another calculated column called Family size was created by adding the two columns SibSp(Siblings and spouse) and Parch(parents and children).

Snap of the Values in calculated column-
 ![Image](https://github.com/user-attachments/assets/99ebea41-ca84-41d2-bde5-0818aacf5c58)
 
 
- Step 6 : In the report view, under the view tab, the background was imported and edited.

- Step 7 : In the report view, under the insert tab, we selected the text box from the home tab. We used this text box to set our title.

- Step 8 : Visual filter (Slicer) was added for filtering the survivors based on Age group.

![Image](https://github.com/user-attachments/assets/646264b1-f8ce-4ede-84f9-f49636f0ae6e)

- Step 9 : Two card visuals were added to the canvas, one representing the count of survivors & other representing survival rate.

- Step 10 : A clustered bar chart was also added to the report design area representing the number of people survived by Pclass. 

- Step 11 : A Donut chart Visual was used to represent the survivors percentage and count by genders.

- Step 12 : In the report view, from the visualizations pane, we selected a scatter chart to represent the survival count by age group and concluded that the highest number of survivors were from age group 0-10.

- Step 13 : In the report view, from the visualizations pane, we selected a clustered column chart to represent survival rate based on the family size. The family with 3 Members had the most survival Rate which was 49 percent.
- Step 14 : Calculated a donut chart of count of Survivers by fare. The highest percentage of survivors had paid 31 dollars. 
        
- Step 15 :  Also create a measure called Survival Rate based on the SUrvival column.

Survival Rate = DIVIDE(CALCULATE(COUNTROWS('Titanic data'),'Titanic data'[Survived] = 1),COUNTROWS('Titanic data'),0)* 100

Step 16: Card visual displaying the Count of survivors
![Image](https://github.com/user-attachments/assets/4beb4f5c-54dd-42a1-8906-e5bc5a424b75)
 
 A card visual was used to represent the Survival perecntage.
 
![Image](https://github.com/user-attachments/assets/15868e59-ff78-4d67-8971-8f954d72a5f2)


# Snapshot of Dashboard (Power BI Desktop)
![Image](https://github.com/user-attachments/assets/db06ff63-2569-4376-aa1e-e0c0b73eda95)

 # Report Snapshot (Power BI DESKTOP)

![Image](https://github.com/user-attachments/assets/0be74ffa-485f-463a-bd07-4b469236fa76)

# Insights

A single page report was created on Power BI Desktop.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Survivors = 889

   Number of Survivors (Male) = 312 (35.1 %)

   Number of Survivors (Female) = 577 (64.9 %)

  thus, higher number of Survivors are Male.

### [2] Survival Count By Age Group 
  0-10 : 241
  10-20: 115
  20-30: 230
  30-40: 154
  40-50: 86
  50-60: 42
  60:70: 16
  71+: 5

We can conclude that Younger people survived more.

  ### [3] Survival Rate by Pclass
   3rd- 491
   2nd- 184
   1st- 214
 So the most survivors were from 3rd class. 

 ### [4] Some other insights
 
 1.1) 26.03  % is the survival rate.
 
 1.2) People with family size of 3 survived the most.(Rate- 48.84%)
 
 1.3) Only 5(16.67%) people of age group 71+ survived.
 
# Titanic-Dashboard.md.txt
Displaying # Titanic-Dashboard.md.txt.
