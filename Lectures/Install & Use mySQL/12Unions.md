# Unions in SQL

- Find a list of employee and branch names (COMBINE)
```
SELECT first_name
FROM employee
UNION
SELECT branch_name
FROM branch;
```
- This will be what we received back
```
first_name
David
Jan
Michael
Angela
Kelly
Standley
Josh
Andy
Jim
Corporate
Scranton
Stamford
```