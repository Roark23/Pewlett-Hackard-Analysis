# Pewlett-Hackard-Analysis
## Purpose

Pewlett-Hackard is a large company with thousands of employees. The company is preparing for a “silver tsunami" where the majority of the employees are going to retire over the next few years. The purpose of this analysis is to assist Pewlett_Hackard with being prepared for this transistion.

The goal is to identify the retiring employees by their title and find the number of retiring employees grouped by title.  This will help Pewlett-Hackard determine the number of positions they will need to hire grouped by each title and department. Also, the company needs to identify the employees eligible for participation in the mentorship program and qualified employees that are ready for retirement to mentor the new employees in the near future.

To find this essential information, Pewlett-Hackard has gathered data in many CSV files 

![CSV Files](/Data)

## Resources
I will mainly be using pgAdmin which is a GUI that uses SQL Language to explore, manipulate and extract the relevant data. Also, QuickDBD as it is useful for database design and better visualization. Lastly, I will be using PostreSQL which is a database system to load, build and manipulate the data.

### ERD
The ERD, entity-relationship diagram, is essential to effectively design a database. The ERD I created for the Pewlett-Hackard analysis shows the relationships between each entities:

![Employee_Database](/Data/EmployeeDB.png)

### Schema
The schema created and provided below outlines how the data will be represented. It is a description of the construction of the database raltive to all the tables, columns, relationships, key constraints, functions and procedures. Schemas are useful for relational database management systems (RDBMS) or designing database management systems (DBMS).

## Results
### Retiring Employees
1. This is the data output displaying the list of retiring employees:

![retirement_titles](/Resources/Retirement_titles.png)

* The table created includes employee number, first name, last name, title, from-date and to-date.
* The query returns 133,776 rows.
* It outlines the employees that are going to retire in the next few years. However, some of the employees are displayed multiple times due to their change of title during their time at Pewlett-Hackard.

2. Here is an updated query that removes the duplicate employees due to their change in title:

![unique_titles](/Resources/unique_titles.png)

* This table still includes employee number, first name, last name, title, from-date and to-date.
* The query only returns 90,398 rows instead of 133,776 rows.
* The table displays a list of employees who are going to retire in the next few years. The difference between this table and the one above is that each employee is only listed once by their most recent title.

### Positions to be Replaced
3. It would be valuable for Pewlett-Hackard to compile a list of positions that need to be replaced. this table highlights the retiring employees grouped by their current title. Pewlett-Hackard can review this for knwoing how many positions they need ot re hire by title:

![retiring_titles](/Resources/retiring_titles.png)

* The table outlines the various titles and how many positions need to be filled per title.
* The query returns a table with 7 rows for each position.
* This shows how many employees will retire in the next few years by their position.

## Summary
The purpose of this analysis is to help Pewlett-Hackard prepare for the upcoming "silver tsunami". One critical question that need to be adressed is how many roles will need to be filled as the "silver tsunami" begins to make an impact?

### Open Positions by Department
To help answer this question, I created another table highlighting open positions for the staff and departments:

![unique_titles_dept](/Resources/unique_titles_dept.png)

Here we can see the positions currently filled that will be open as the employees begin to retire over the next few years. Furthermore, I went in depth to learn more about the open positions that need to be filled:

![positions_open](/Resources/positions_open.png)

### Mentorship Eligibility
Lastly, Pewlet-Hackard needs to know if there are enough qualified, retirement-ready employees in the departments to mentor the next generation of employees:

![mentorship_eligibility](/Resources/mentorship_eligibility.png)

This is the list of employees eligible for the mentorship program. There are 1,940 employees in the list that are eligible.

#### Conclusion
After analyzing all the soon-to-be open positions by each department and cross referencing them with employees eligible for mentorship, we can see a big difference in the amount of employees needed to mentor. The "silver tsunami" will have a huge impact as 90,398 positions will need to be filled over the next few years. Currently, there are only 1,940 employees eligible to participate in the mentorship program. Pewlett-Hackard will need to take neccessary steps to ensure they can fill all the required positions for the large number of employees they have retiring soon.
