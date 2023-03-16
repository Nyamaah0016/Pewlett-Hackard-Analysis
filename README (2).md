# Pewlett Hackard Analysis

### Overview
Now that Bobby has proven his SQL chops, his manager has given both of you two more assignments: determine the number of retiring employees per title, and identify employees who are eligible to participate in a mentorship program. Then, you’ll write a report that summarizes your analysis and helps prepare Bobby’s manager for the “silver tsunami” as many current employees reach retirement age.

Deliverable 1: The Number of Retiring Employees by Title
Deliverable 2: The Employees Eligible for the Mentorship Program
Deliverable 3: A written report on the employee database analysis

### Purpose
In this deliverable, Bobby was tasked to determine the number of retiring employees per title, and identify employees who are eligible to participate in a mentorship program. Then, you’ll write a report that summarizes your analysis and helps prepare Bobby’s manager for the “silver tsunami” as many current employees reach retirement age.

### Resources
- Data Source: Employee_Database_challenge.sql
- Data Tools: PostgreSQL, pgAdmin

### Database Keys
Database keys identify records from tables and establish relationships between tables. There are numerous types of keys. For our purposes, we will focus on primary keys and foreign keys.

### Primary Keys
The departments.csv file has a dept_no column with unique identifiers for each row (one department number per department). For example, d001 will always reference the Marketing department, across other worksheets. This unique identifier is known as a primary key.

Primary keys are an important part of database design. When a database is being created, each table added must include a primary key in the architecture. Primary keys serve as a link between these tables.
![image.png](attachment:image.png)

In the graphic above, Table 1 has a primary key, or column of unique identifiers in common with Tables 2 and 4. Table 3's primary key is linked only to Table 2. These links trace the relationships between tables. There are times when we'll need to trace two or three links to get the exact data we need. In these cases, we'll pick the data we need from each table. Linking the tables together in this manner is called a join, a feature we'll get into later.

In the second CSV file, dept_emp.csv, the "emp_no" column contains the primary key
![image-2.png](attachment:image-2.png)

We know this is the primary key because each number is unique. For example, the emp_no column holds employee numbers. Each employee will have only one number, and that number won't be used for any other employee.



### Foreign Keys
Foreign keys are just as important as primary keys. While primary keys contain unique identifiers for their dataset, a foreign key references another dataset's primary key.

Think about it like a phone number. You have your own number. It's your number, assigned to your phone, and unique to you. This is your primary key. Your friend also has a primary key: his or her own phone number.

When you save your friend's number in your phone, you're creating a reference to that person, also known as a foreign key. Your phone has lots of foreign keys (such as parents, doctors offices, friends, and other family), but only one primary key.

Likewise, when your friend saves your number in their phone, your number is now a foreign key in their phone. Saving these keys connects the devices. They show the relationship between your phone and your friend's phone.

Compare our first two CSVs again by looking at the following image.
![image.png](attachment:image.png)

In this example, dept_no shows up in both datasets; as an identifier (or primary key) in one and as a reference (or foreign key) in the other. This demonstrates the link between employees and which department they work in.

We could continue to look for connections between the datasets, or we could create a roadmap of the content. Our roadmap would serve as a quick reference diagramming the different datasets and their interconnections. Additionally, it could be used as a reference guide later, when we begin to create queries to access all of the data.

## ERD
An entity relationship diagram (ERD) is a type of flowchart that highlights different tables and their relationships to each other. The ERD does not include any actual data, but it does capture the following pertinent information from each CSV file:

Primary keys
Foreign keys
Data types for each column
The ERD also shows the flow of information from one table to another, as captured in the image below:

![image.png](attachment:image.png)

In addition to creating new databases, ERDs are used to document existing databases. The visual representation of the tables gives a deeper understanding of the data and the database as a whole.

When creating a diagram, we need to fully understand all of the data being inserted. Database components include tables, known as entities, with data, known as attributes.

### Deliveries : 
Using the ERD you created in this module as a reference and your knowledge of SQL queries, create a Retirement Titles table that holds all the titles of current employees who were born between January 1, 1952 and December 31, 1955. Because some employees may have multiple titles in the database—for example, due to promotions—you’ll need to use the DISTINCT ON statement to create a table that contains the most recent title of each employee. Then, use the COUNT() function to create a final table that has the number of retirement-age employees by most recent job title.

A query is written and executed to create a Retirement Titles table for employees who are born between January 1, 1952 and December 31, 1955
The Retirement Titles table is exported as retirement_titles.csv
​A query is written and executed to create a Unique Titles table that contains the employee number, first and last name, and most recent title.
The Unique Titles table is exported as unique_titles.csv
A query is written and executed to create a Retiring Titles table that contains the number of titles filled by employees who are retiring.
The Retiring Titles table is exported as retiring_titles.csv

### Results

Provide a bulleted list with four major points from the two analysis deliverables. Use images as support where needed:

From the finding of the eligible retirees, High Percentage of the workforce could retire at any given time.
From the job titles of the eligible retirees, the breakdown is below.
32,452 Staff
29,415 Senior Engineer
14,221 Engineer
8,047 Senior Staff
4,502 Technique Leader
1,761 Assistant Engineer


1. A query is written and executed to create a Retirement Titles table for employees who are born between January 1, 1952 and December 31, 1955.
![image.png](attachment:image.png)

2. The Retirement Titles table is exported as retirement_titles.csv
![image-2.png](attachment:image-2.png)

3. A query is written and executed to create a Unique Titles table that contains the employee number, first and last name, and most recent title.
![image-3.png](attachment:image-3.png)

4. The Unique Titles table is exported as unique_titles.csv
![image-4.png](attachment:image-4.png)

5. The Retiring Titles table is exported as retiring_titles.csv
![image-5.png](attachment:image-5.png)


### Summary
Provide high-level responses to the following questions, then provide two additional queries or tables that may provide more insight into the upcoming "silver tsunami.":

1) How many roles will need to be filled as the "silver tsunami" begins to make an impact?.

90,398 roles are in urgent need to be filled out as soon as the workforce starts retiring at any given time.

2) Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?

No, we have less employees who are eligible to participate in a mentorship program.
