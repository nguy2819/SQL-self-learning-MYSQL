# JOINS

- Find all branches and the name of their managers
```
SELECT employee.emp_id, employee.first_name, branch.branch_name
FROM employee
JOIN branch
ON employee.emp_id = branch.mgr_id;
```
- We got this data back
```
emp_id	first_name	branch_name
100	    David	    Corporate
102	    Michael	    Scranton
106	    Josh	    Stamford
```

## LEFT JOIN (this will include all of the data on the left join - which is employee. They will provide all the employee's names included who does not have position as manager)
```
SELECT employee.emp_id, employee.first_name, branch.branch_name
FROM employee
LEFT JOIN branch
ON employee.emp_id = branch.mgr_id;
```

## RIGHT JOIN (this will include all of the data on the right join - which is branch. They will provide all the branches included the branch that nobody is working with)
```
SELECT employee.emp_id, employee.first_name, branch.branch_name
FROM employee
RIGHT JOIN branch
ON employee.emp_id = branch.mgr_id;
```