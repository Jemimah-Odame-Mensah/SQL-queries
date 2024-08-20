# Apply filters to SQL queries

## Project Description

As a security professional at a large organization, part of my role involves investigating security issues to help maintain system integrity. Recently, I identified potential security concerns related to login attempts and employee machines. My task was to examine data from the organization's **_employees_** and **_log_in_attempts_** tables. I used SQL filters to retrieve records from these datasets and investigated the potential security issues.

## Objective

The objective of this project was to enhance the security posture of the organization by investigating and analyzing potential security incidents. By applying SQL queries to the organization's data, I aimed to identify suspicious login attempts, monitor employee activities, and support the IT team in securing critical systems. This project demonstrates my ability to proactively address security challenges through data analysis and incident response.

### Skills Learned

- SQL Query Proficiency
- Data Analysis and Investigation
- Incident Response
- Attention to Detail
- Pattern Recognition and Data Filtering

## Steps
### 1. Retrieve After-Hours Failed Login Attempts:
I identified a potential security incident that occurred after business hours. To investigate, I queried the **_log_in_attempts_** table to review after-hours login activity. Using SQL filters, I created a query to identify all failed login attempts that occurred after 18:00.
The code below demonstrates how I used a SQL query to filter failed login attempts that occurred after business hours:

![SQL retrieve after hours failed login attempts 1](https://github.com/user-attachments/assets/e0b88253-06f8-4a08-9f4d-681c4ab31102)
*Ref 1: SQL query*

In the screenshot, the first three lines represent my query, while the remaining portion shows a sample of the output. I began the query by selecting all data from the **_log_in_attempts_** table using the **_SELECT *_** and **_FROM_** keywords. Then, I used a **_WHERE_** clause with an **_AND_** operator to filter the results, outputting only login attempts that occurred after 18:00 and were unsuccessful. The first condition, **_login_time > '18:00'_**, filters for login attempts after 18:00. The second condition, **_success = FALSE_**, filters for failed login attempts. The **_login_time_** column stores the time of the login attempt, and the **_success_** column contains a value of **_0_** for failed attempts.

### 2. Retrieve Login Attempts on Specific Dates:
To investigate a suspicious event that occurred on 2022-05-09, I reviewed all login attempts on that day and the day before.
The code below demonstrates how I used SQL filters to create a query that identifies all login attempts on 2022-05-09 or 2022-05-08:

![SQL retrieve login attempts on specific dates](https://github.com/user-attachments/assets/e7a4cc68-4eff-4d42-9e26-c4ef696e4ebd)
*Ref 2: SQL query*

In the screenshot, the first three lines represent my query, and the remaining portion shows a sample of the output. I started by selecting all data from the **_log_in_attempts_** table using the **_SELECT *_** and **_FROM_** keywords. Then, I used a **_WHERE_** clause with an **_OR_** operator to filter the results for login attempts that occurred on either 2022-05-09 or 2022-05-08. The first condition, **_login_date = '2022-05-09'_**, filters for logins on 2022-05-09, while the second condition, **_login_date = '2022-05-08'_**, filters for logins on 2022-05-08.

### 3. Retrieve Login Attempts Outside of Mexico:
Another suspicious activity involved login attempts that the team determined did not originate in Mexico. Therefore, I investigated login attempts that occurred outside of Mexico.
As demonstrated below, I used SQL filters to create a query that identifies all login attempts outside of Mexico:

![SQL retrieve login attempts outside of mexico](https://github.com/user-attachments/assets/0bfd8e6d-824c-4ef2-884e-04179f6b135e)
*Ref 3: SQL query*

In the screenshot, the first three lines represent my query, and the remaining portion shows a sample of the output. I started by selecting all data from the **_log_in_attempts_** table using the **_SELECT *_** and **_FROM_** keywords. Then, I used a **_WHERE_** clause with **_NOT_** to filter for countries other than Mexico. I used **_LIKE_** with **_MEX%_** as the pattern to match because the dataset represents Mexico as **_MEX_** and **_MEXICO_**. The percentage sign **_%_** represents any number of unspecified characters when used with **_LIKE_**. 

### 4. Retrieve Employees in Marketing:
My team needed to perform security updates on specific employee machines in the Marketing department located in the East building. I was responsible for gathering information on these employee machines and queried the **_employees_** table.
As demonstrated below, I used SQL filters to create a query that identifies all employees in the Marketing department across offices in the East building:

![SQL retrieve employees in marketing department in the east building](https://github.com/user-attachments/assets/f0fdf982-fce0-46f4-85bd-57def401daff)
*Ref 4: SQL query*

In the screenshot, the first three lines represent my query, and the remaining portion shows a sample of the output. I started by selecting all data from the **_employees_** table using the **_SELECT *_** and **_FROM_** keywords. Then, I used a **_WHERE_** clause with **_AND_** to filter for employees who work in the Marketing department and in the East building. I used **_LIKE 'East%'_** to match the data in the **_office_** column, which represents the East building with a specific office number. The first condition, **_department = 'Marketing'_**, filters for employees in the Marketing department. The second condition, **_office LIKE 'East%'_**, filters for employees in the East building.

### 5. Retrieve Employees in Finance or Sales:
The machines for employees in the Finance and Sales departments also need to be updated. Since a different security update is needed, I had to get information on employees only from these two departments. As shown below, I used SQL filters to create a query that identifies all employees in the Sales or Finance departments:

![SQL retrieve employees in finance or salse department](https://github.com/user-attachments/assets/b58ba27d-bf49-46b0-adf5-704c3887855e)
*Ref 5: SQL query*

In the screenshot, the first three lines represent my query, and the remaining portion shows a sample of the output. I started by selecting all data from the **_employees_** table using the **_SELECT *_** and **_FROM_** keywords. Then, I used a **_WHERE_** clause with **_OR_** to filter for employees in either the Finance or Sales departments. The first condition, **_department = 'Finance'_**, filters for employees in the Finance department. The second condition, **_department = 'Sales'_**, filters for employees in the Sales department.

### 6. Retrieve All Employees Not in IT:
My team needed to make one more update to employee machines. Employees in the Information Technology (IT) department had already received this update, so the update was required for employees in all other departments. I used SQL filters to create a query that identifies all employees not in the IT department:

![SQL retrieve all employees not in IT department](https://github.com/user-attachments/assets/909ccef4-b2f7-499b-8316-79138988c1ec)
*Ref 6: SQL query*

I started by selecting all data from the **_employees_** table using the **_SELECT *_** and **_FROM_** keywords. Then, I used a **_WHERE_** clause with **_NOT_** to filter out employees not in the IT department.


## Summary

In this project, I applied SQL filters to extract specific information on login attempts and employee machines. I worked with two different tables, **_log_in_attempts_** and **_employees_**, using the **_AND_**, **_OR_**, and **_NOT_** operators to filter for the specific information required for each task. Additionally, I used the **_LIKE_** operator and the **_%_** wildcard to match patterns in the data.

