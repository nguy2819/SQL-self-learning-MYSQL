# WildCards 

## % = any # characters ; _ = one character

- Find any client's who are an LLC
```
SELECT *
FROM client
WHERE client_name LIKE '%LLC';
```
- The result is John Daily Law, LLC - because %LLC means any characters stand in front of LLC 

- Find any branch suppliers who are in the label business
```
SELECT *
FROM branch_supplier
WHERE supplier_name LIKE '% Label%';
```
- The result is J.T. Forms & Labels - because % Label% means they will drap any characters stand in front of Label and after Label

- Find any employee born in October
```
SELECT *
FROM employee
WHERE birth_day LIKE '____-10%';
```
- This one they will get the 4 characters on the birth-year and 10 means October with % any characters after that

- Find any clients who are schools
```
SELECT *
FROM client
WHERE client_name LIKE '%school%';
```