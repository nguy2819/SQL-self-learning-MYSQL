- To make people has to enter the specific data you required, type NOT NULL/ UNIQUE after the data you want to receive: 
```
CREATE TABLE student (
    student_id INT,
    name VARCHAR(20) NOT NULL,
    major VARCHAR(20) UNIQUE,
    PRIMARY KEY(student_id)
);
```

- Or DEFAULT:
```
CREATE TABLE student (
    student_id INT,
    name VARCHAR(20) NOT NULL,
    major VARCHAR(20) DEFAULT 'undecided',
    PRIMARY KEY(student_id)
);
```
- So after insert a new data without major's info: INSERT INTO student(student_id, name) VALUES(5, 'Mike');
- What you get back is this:
```
student_id	name	major
5	        Mike	undecided
```



- Or AUTO_INCREMENT, //this will automatically make student_id in order for you
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
```
- The result will be:
```
student_id	name	major
1	        Jack	Biology
2	        Kate	Sociology
```
