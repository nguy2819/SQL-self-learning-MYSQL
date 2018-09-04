```
CREATE TABLE employee (
emp_id INT PRIMARY KEY,
first_name VARCHAR(40),
last_name VARCHAR(40),
birth_day DATE,
sex VARCHAR(1),
salary INT,
super_id INT,
branch_id INT
);

CREATE TABLE branch (
branch_id INT PRIMARY KEY,
branch_name VARCHAR(40),
mgr_id INT,
mgr_start_date DATE,
FOREIGN KEY(mgr_id) REFERENCES employee(emp_id) ON DELETE SET NULL
);

ALTER TABLE employee
ADD FOREIGN KEY(branch_id)
REFERENCES branch(branch_id)
ON DELETE SET NULL;

ALTER TABLE employee
ADD FOREIGN KEY(super_id)
REFERENCES employee(emp_id)
ON DELETE SET NULL;

CREATE TABLE client (
client_id INT PRIMARY KEY,
client_name VARCHAR(40),
branch_id INT,
FOREIGN KEY(branch_id) REFERENCES branch(branch_id) ON DELETE SET NULL
);

CREATE TABLE works_with (
emp_id INT,
client_id INT,
total_sales INT,
PRIMARY KEY(emp_id, client_id),
FOREIGN KEY(emp_id) REFERENCES employee(emp_id) ON DELETE CASCADE,
FOREIGN KEY(client_id) REFERENCES client(client_id) ON DELETE CASCADE
);

CREATE TABLE branch_supplier (
branch_id INT,
supplier_name VARCHAR(40),
supplier_type VARCHAR(40),
PRIMARY KEY(branch_id, supplier_name),
FOREIGN KEY(branch_id) REFERENCES branch(branch_id) ON DELETE CASCADE
);
```



- Inserting data into Employee and Branch boxes:
```
INSERT INTO employee VALUES(100, 'David', 'Wallace', '1969-11-17', 'M', 250000, NULL, NULL);

INSERT INTO branch VALUES(1, 'Corporate', 100, '2006-02-09');

UPDATE employee
SET branch_id = 1
WHERE emp_id = 100;

INSERT INTO employee VALUES(101, 'Jan', 'Levinson', '1961-05-11', 'F', 110000, 100, 1);
```
```
INSERT INTO employee VALUES(102, 'Michael', 'Scott', '1964-05-01', 'M', 250000, 100, NULL);

INSERT INTO branch VALUES(2, 'Scranton', 102, '1992-04-06');

UPDATE employee
SET branch_id = 2
WHERE emp_id = 102;

INSERT INTO employee VALUES(103, 'Angela', 'Martin', '1971-06-25', 'F', 63000, 102, 2);
INSERT INTO employee VALUES(104, 'Kelly', 'Karpoo', '1980-02-05', 'F', 55000, 102, 2);
INSERT INTO employee VALUES(105, 'Standley', 'Hudson', '1958-02-19', 'M', 69000, 102, 2);
```
```
INSERT INTO employee VALUES(106, 'Josh', 'Porter', '1969-06-05', 'M', 78000, 100, NULL);

INSERT INTO branch VALUES(3, 'Stamford', 106, '1998-02-06');

UPDATE employee
SET branch_id = 3
WHERE emp_id = 106;

INSERT INTO employee VALUES(107, 'Andy', 'Bernard', '1973-07-22', 'M', 65000, 106, 3);
INSERT INTO employee VALUES(108, 'Jim', 'Halpert', '1978-02-05', 'M', 55000, 106, 3);
```

- The employee table will look like this: (SELECT * FROM employee;)
```
emp_id	first_name	last_name	birth_day   sex	salary	super_id	branch_id
100	    David	    Wallace	    1969-11-17	M	250000	NULL    	1
101	    Jan	        Levinson	1961-05-11	F	110000	100	        1
102	    Michael	    Scott	    1964-05-01	M	250000	100	        2
103	    Angela	    Martin	    1971-06-25	F	63000	102	        2
104	    Kelly	    Karpoo	    1980-02-05	F	55000	102	        2
105	    Standley	Hudson	    1958-02-19	M	69000	102	        2
106	    Josh	    Porter	    1969-06-05	M	78000	100	        3
107	    Andy	    Bernard	    1973-07-22	M	65000	106	        3
108	    Jim	        Halpert	    1978-02-05	M	55000	106	        3
```

- The branch table will look like this: (SELECT * FROM branch;)
```
branch_id	branch_name	mgr_id	mgr_start_date
1	        Corporate	100	    2006-02-09
2	        Scranton	102	    1992-04-06
3	        Stamford	106	    1998-02-06
```