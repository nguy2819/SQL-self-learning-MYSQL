- Find all employees order by SALARY
  + From low SALARY to high SALARY
```
SELECT *
FROM employee
ORDER by salary;
```
- We will get back this data, you can see the order for salary is going from low to high
```
emp_id	first_name	last_name	birth_day	sex	salary	super_id	branch_id
104	    Kelly	    Karpoo	    1980-02-05	F	55000	102	        2
108	    Jim	        Halpert	    1978-02-05	M	55000	106     	3
103	    Angela	    Martin	    1971-06-25	F	63000	102	        2
107	    Andy	    Bernard	    1973-07-22	M	65000	106	        3
105	    Standley	Hudson	    1958-02-19	M	69000	102	        2
106	    Josh	    Porter	    1969-06-05	M	78000	100	        3
101	    Jan	        Levinson	1961-05-11	F	110000	100	        1
100	    David	    Wallace	    1969-11-17	M	250000	NULL	    1
102	    Michael	    Scott	    1964-05-01	M	250000	100	        2
```

  + From high SALARY to low SALARY
```
SELECT *
FROM employee
ORDER by salary DESC;
```
- This will be the data we received back, from high SALARY to low SALARY
```
emp_id	first_name	last_name	birth_day	sex	salary	super_id	branch_id
100	    David	    Wallace	    1969-11-17	M	250000	NULL	    1
102	    Michael	    Scott	    1964-05-01	M	250000	100	        2
101	    Jan	        Levinson	1961-05-11	F	110000	100	        1
106	    Josh	    Porter	    1969-06-05	M	78000	100	        3
105	    Standley	Hudson	    1958-02-19	M	69000	102	        2
107	    Andy	    Bernard	    1973-07-22	M	65000	106	        3
103	    Angela	    Martin	    1971-06-25	F	63000	102	        2
104	    Kelly	    Karpoo	    1980-02-05	F	55000	102	        2
108	    Jim	        Halpert	    1978-02-05	M	55000	106     	3
```

- Find all employee ordered by sex then name
```
SELECT *
FROM employee
ORDER by sex,  first_name, last_name;
```
- This is the data we got back, they are in ordered: the first 3 Female with first_name alphabet ordered (Angela - Jan- Kelly); then all the Male, with first_name alphabet ordered (Andy-David-Jim-etc.)
```
emp_id	first_name	last_name	birth_day	sex	salary	super_id	branch_id
103	    Angela	    Martin	    1971-06-25	F	63000	102	        2
101	    Jan	        Levinson	1961-05-11	F	110000	100	        1
104	    Kelly	    Karpoo	    1980-02-05	F	55000	102	        2
107	    Andy	    Bernard	    1973-07-22	M	65000	106	        3
100	    David	    Wallace	    1969-11-17	M	250000	NULL	    1
108	    Jim	        Halpert	    1978-02-05	M	55000	106	        3
106	    Josh	    Porter	    1969-06-05	M	78000	100	        3
102	    Michael	    Scott	    1964-05-01	M	250000	100	        2
105	    Standley	Hudson	    1958-02-19	M	69000	102	        2
```

- Find the first 5 employees in the table
```
SELECT *
FROM employee
LIMIT 5;
```
- We will get the first 5 employees in the table back
```
emp_id	first_name	last_name	birth_day	sex	salary	super_id	branch_id
100	    David	    Wallace	    1969-11-17	M	250000	NULL	    1
101	    Jan	        Levinson	1961-05-11	F	110000	100	        1
102	    Michael	    Scott	    1964-05-01	M	250000	100	        2
103	    Angela	    Martin	    1971-06-25	F	63000	102	        2
104	    Kelly	    Karpoo	    1980-02-05	F	55000	102	        2
```

- Find the first and last name of all employees
``` 
SELECT first_name, last_name
FROM employee;
```
- This is what we got back from DB
```
first_name	last_name
David	    Wallace
Jan	        Levinson
Michael	    Scott
Angela	    Martin
Kelly	    Karpoo
Standley	Hudson
Josh	    Porter
Andy	    Bernard
Jim	        Halpert
```

- Find the forename and surename of all employees
```
SELECT first_name AS forename, last_name AS surename
FROM employee;
```
- We will get data back with first name - changed to - forename; last name - changed to - surename
```
forename	surename
David	    Wallace
Jan	        Levinson
Michael	    Scott
Angela	    Martin
Kelly	    Karpoo
Standley	Hudson
Josh	    Porter
Andy	    Bernard
Jim	        Halpert
```

- Find out all different genders
```
SELECT DISTINCT sex
FROM employee;
```
- The information we got back is:
```
sex
M
F
```
OR 
- Find out all different branch_id
```
SELECT DISTINCT branch_id
FROM employee;
```
- The information we got back is:
```
branch_id
1
2
3
```