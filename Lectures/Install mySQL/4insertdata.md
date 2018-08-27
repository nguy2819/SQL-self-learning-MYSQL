- To insert data into the table that we made, type:
```
INSERT INTO student VALUES(1, 'Jack', 'Biology');
```

- To see how the table looks like, type:
```
SELECT * FROM student;
```


- All the code should looks like this:
```
CREATE TABLE student (
    student_id INT PRIMARY KEY,
    name VARCHAR(20),
    major VARCHAR(20)
);

SELECT * FROM student;

INSERT INTO student VALUES(1, 'Jack', 'Biology');
```

- After typed "SELECT * FROM student;" - then "RUN", the table will look like this:
```
student_id	name	major
1	        Jack	Biology
```



- To keep adding the next data, type:
```
CREATE TABLE student (
    student_id INT PRIMARY KEY,
    name VARCHAR(20),
    major VARCHAR(20)
);

SELECT * FROM student;

INSERT INTO student VALUES(2, 'Kate', 'Sociology');
```
- Checking to see how the table looks like after inserting 2 datas:
```
student_id	name	major
1	        Jack	Biology
2	        Kate	Sociology
```



- To add another data without knowing major's info, type"
```
INSERT INTO student(student_id, name) VALUES(3, 'Claire');
```
- The table will look like:
```
student_id	name	major
1	        Jack	Biology
2	        Kate	Sociology
3	        Claire	NULL
```



- We can use the same INSERT INTO or seperate INSERT INTO
```
CREATE TABLE student (
    student_id INT PRIMARY KEY,
    name VARCHAR(20),
    major VARCHAR(20)
);

SELECT * FROM student;

INSERT INTO student VALUES(1, 'Jack', 'Biology');
INSERT INTO student VALUES(2, 'Kate', 'Sociology');
INSERT INTO student(student_id, name) VALUES(3, 'Claire');
INSERT INTO student VALUES(4, 'Jack', 'Biology');
INSERT INTO student VALUES(5, 'Mike', 'Computer Science');
```
- The final product will look like this:
```
student_id	name	major
1	Jack	Biology
2	Kate	Sociology
3	Claire	NULL
4	Jack	Biology
5	Mike	Computer Science
```



- One unique thing is that you cannot duplicate the data that you did insert and want to insert again, it will say: "Failed, ER_DUP_ENTRY: Duplicate entry '1' for key 'PRIMARY'"