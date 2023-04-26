# Simple PowerBI Exercise


See raw dataset at: https://www.kaggle.com/datasets/csafrit2/higher-education-students-performance-evaluation

The purpose of this project is to practice transforming a dataset with PowerBI. It is not intended to analyze the data with an intentional assessment. Rather, this project focuses on performing simple exercises and understanding the concepts around it in order to transform the dataset.

Snippet of the raw data
![1](https://user-images.githubusercontent.com/55467236/234654653-da5b09e6-310a-41f6-9433-896aeea03773.jpg)



**Goal 1:**  Display data as text instead of integers using the Replace Values function

*Attribute Information:*
Column 2 - Sex (1: female, 2: male)

First assess the data type. The current data is integer and the targeted data is text. Update the data type from ‘Whole Number’ to ‘Text.’ 

Before:
![2](https://user-images.githubusercontent.com/55467236/234654848-d175dcf0-3ade-4894-b52c-225ad86dfa43.jpg)


After:
![3](https://user-images.githubusercontent.com/55467236/234655028-2d32a376-f046-44af-8eb5-98a04c7b411d.jpg)


After changing to the correct data type, use the Replace Values function to replace ‘1’ -> ‘Female’ and then ‘2’ to ‘Male.’

**Goal 2**: Create Fact Dimensional Model and Relationships
A table may reference another table, and the tables are associated by a foreign key. I created new tables to practice this concept using the attribute information.
*Attribute Information:*
Scholarship type: (1: None, 2: 25%, 3: 50%, 4: 75%, 5: Full)
![4](https://user-images.githubusercontent.com/55467236/234655672-70820b2e-7375-474d-bd30-b1fd3b0bb699.jpg)

Associate the relationships in the Model View.
![5](https://user-images.githubusercontent.com/55467236/234655874-44b5a4a8-e1e1-4859-b407-4b104fa8d13f.jpg)


**Goal 3**: Performing Merge
Perform a merge for the Expected GPA column without changing the data. While we could use Replace Values, it would create confusion by replacing unwanted data. For example, we could replace ‘1’ to ‘<2.00’. However, when we try to replace ‘2’ to ‘2.00-2.49,’ it would impact any data that has the value ‘2.’ Using merge would allow us to bring in the data directly to the main table.

Create a new table for the Expected GPA. 

*Attribute Information:*
Expected Cumulative grade point average in the graduation (4.00): (1: <2.00, 2: 2.00-2.49, 3: 2.50-2.99, 4: 3.00-3.49, 5: above 3.49)

Then perform a merge and select the correct columns:

![6](https://user-images.githubusercontent.com/55467236/234656364-99894f46-6b6b-4ee2-8110-d1423e3e60c8.jpg)


Filter the newly inserted column to display the GPA Range:

![7](https://user-images.githubusercontent.com/55467236/234656434-21cedc3d-27b2-4010-9e97-deeb31c3ee86.jpg)


The GPA Range data is brought into the main table without changing the initial column values.

Use the transformed data to do visualization on what you'd like to analyze.
![image](https://user-images.githubusercontent.com/55467236/234656847-1b22fd76-d8a3-4a2b-a8cc-48e4ecd2779c.png)

