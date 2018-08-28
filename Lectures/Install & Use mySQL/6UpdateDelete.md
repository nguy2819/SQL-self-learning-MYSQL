- To UPDATE new data: (for ex: change 'Biology' to 'Bio')
```
UPDATE student
SET major = 'Bio'
WHERE major = 'Biology';
```

- The whole code will look like: 
```
CREATE TABLE student (
    student_id INT AUTO_INCREMENT,
    name VARCHAR(20) NOT NULL,
    major VARCHAR(20) DEFAULT 'undecided',
    PRIMARY KEY(student_id)
);

SELECT * FROM student;

INSERT INTO student(name, major) VALUES('Jack', 'Biology');
INSERT INTO student(name, major) VALUES('Kate', 'Sociology');
INSERT INTO student(name, major) VALUES('Kyle', 'Biology');
INSERT INTO student(name, major) VALUES('Rick', 'Chemistry');

UPDATE student
SET major = 'Bio'
WHERE major = 'Biology';
```
- The result will be:
```
Rows affected: 2
student_id	name	major
1	        Jack	Bio
2	        Kate	Sociology
3	        Kyle	Bio
4           Rick    Chemistry
```



- OR: //change student_id = 2, which is Kate with Sociology major to a new major "Computer Science"
```
UPDATE student
SET major = 'Computer Science'
WHERE student_id = 2;
```
- The result will be:
```
Rows affected: 2
student_id	name	major
1	        Jack	Bio
2	        Kate	Computer Science
3	        Kyle	Bio
4           Rick    Chemistry
```



- OR: //change students with 2 different majors to 1 same major
```
UPDATE student
SET major = 'Biochemistry'
WHERE major = 'Bio' OR major = 'Chemistry';
```
- The result will be:
```
student_id	name	major
1	        Jack	Biochemistry
2	        Kate	Computer Science
3	        Kyle	Biochemistry
4           Rick    Biochemistry
```



- OR: //change student_id with specific details
```
UPDATE student
SET name = 'Tom', major = 'undecided'
WHERE student_id = 1;
```
- The result will be:
```
student_id	name	major
1	        Tom 	undecided
2	        Kate	Computer Science
3	        Kyle	Biochemistry
4           Rick    Biochemistry
```



- OR: //change major undecided to all of the students by deleting WHERE
```
UPDATE student
SET major = 'undecided';
```
- The result will be:
```
student_id	name	major
1	        Tom 	undecided
2	        Kate	undecided
3	        Kyle	undecided
4           Rick    undecided
```



- DELETE a specific row (through student_id)
```
DELETE FROM student
WHERE student_id = 4;
```
- The result will be:
```
student_id	name	major
1	        Tom 	undecided
2	        Kate	undecided
3	        Kyle	undecided
//no longer has the row with student_id number 4
```



- OR: delete a specific row (through name AND major)
```
DELETE FROM student
WHERE name = 'Tom' AND major = 'undecided';
```
- The result will be:
```
student_id	name	major
//no longer has the row with student name = 'Tom' AND major = 'undecided';
2	        Kate	undecided
3	        Kyle	undecided
//no longer has the row with student_id number 4
```



- OR: delete all the row in the table
```
DELETE FROM student;
```
- The result will be:
```
student_id	name	major
//there is no longer any rows in this table
```