# SQL FUNCTIONS

- Find the number of employees
```
SELECT COUNT(emp_id)
FROM employee;
```
- The result we got back is 9 because we have David-100, Jan-101, Michael-102, Angela-103, Kelly-104, Standley-105, Josh-106, Andy-107, Jim-108

```
COUNT(emp_id)
9
```

- Find the number of employees have supervisor
```
SELECT COUNT(super_id)
FROM employee;
```
- The result is 8 because David does not have supervisor
```
COUNT(super_id)
8
```

- Find the number of female employees born after 1970
```
SELECT COUNT(emp_id)
FROM employee
WHERE sex = 'F' AND birth_day > '1970-01-01';
```
- The result is 2 because we have total 3 Females but only 2 Females are born after 1970
```
COUNT(emp_id)
2
```

- Find the average of all the employee's salaries
```
SELECT AVG(salary)
FROM employee;
```
- The result will be:
```
AVG(salary)
110555.5556
```
OR - Find the average of all the Male employee's salaries 
```
SELECT AVG(salary)
FROM employee
WHERE sex = 'M';
```
- The result is:
```
AVG(salary)
127833.3333
```

- Find the SUM of all the employee's salaries
```
SELECT SUM(salary)
FROM employee;
```
- We will know how much the company spends to pay all the employees
```
SUM(salary)
995000
```

- Find out how many males and females there are
```
SELECT COUNT(sex), sex
FROM employee
GROUP BY sex;
```
- MySQL will give bac data in groups for us:
```
COUNT(sex)	sex
6	        M
3	        F
```