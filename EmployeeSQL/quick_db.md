departments as d
---
dept_no VARCHAR pk
dept_name VARCHAR


titles as t
---
title_id VARCHAR pk
title VARCHAR


employees as e
---
emp_no INT pk
emp_title_id VARCHAR FK >- titles.title_id
birth_date DATE
first_name VARCHAR
last_name VARCHAR
sex VARCHAR(1)
hire_date DATE


salaries as s
---
emp_no INT pk FK - employees.emp_no
salary INT


dept_emp as de
---
emp_no INT FK - employees.emp_no
dept_no VARCHAR FK >- departments.dept_no


dept_manager as dm
---
dept_no VARCHAR fk FK - departments.dept_no
emp_no INT FK - employees.emp_no

