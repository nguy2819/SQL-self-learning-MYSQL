- Create a table on PopSQL:
```
CREATE TABLE student (
    student_id INT PRIMARY KEY,
    name VARCHAR(20),
    major VARCHAR(20)
);
```
- OR
```
CREATE TABLE student (
    student_id INT,
    name VARCHAR(20),
    major VARCHAR(20),
    PRIMARY KEY(student_id)
);
```



- To see what did you make successful or not? Type:
```
DESCRIBE student;
```
- Then press "RUN", it will show that on your data, you have:
```
Success
3 rows
Field	    Type	        Null	Key	Default	Extra
student_id	int(11)	NO	    PRI	    NULL	
name	    varchar(20)	    YES		NULL	
major	    varchar(20)	    YES		NULL
```



- To "delete", type:
```
DROP TABLE student;
```
- After pressing "RUN", it will show that "Success, Rows affected: 0" and then "Failed, ER_BAD_TABLE_ERROR: Unknown table 'borlandtien.student'" => to let you know that there is no longer table student inside database (borlandtien)



- If you want to make the table student again, just click your mouse on "CREATE TABLE student" and press "RUN"
- Then it will show the sign "Success" and click your mouse on "DESCRIBE student" - press "RUN" -> it will appear the table back
```
Success
3 rows
Field	    Type	        Null	Key	Default	Extra
student_id	int(11)	NO	    PRI	    NULL	
name	    varchar(20)	    YES		NULL	
major	    varchar(20)	    YES		NULL
```



- To add another column, type:
```
ALTER TABLE student ADD gpa DECIMAL(3, 2);
```
- After typed the ALTER TABLE to add another gpa column, press "RUN" -> "Success, No result found"
- Then click your mouse on "DESCRIBE student" - press "RUN" -> it will show the table with 4 rows in database
```
Success
4 rows
Field	    Type	        Null	Key	Default	Extra
student_id	int(11)	NO	    PRI	    NULL	
name	    varchar(20)	    YES		NULL	
major	    varchar(20)	    YES		NULL	
gpa	        decimal(3,2)	YES		NULL
```



- To delete the gpa column that we just created, type:
```
ALTER TABLE student DROP COLUMN gpa;
```
- After "RUN" and click your mouse on "DESCRIBE student" - press "RUN" again, it will be back to normal 3 rows:
```
Field	    Type	        Null	Key	Default	Extra
student_id	int(11)	NO	    PRI	    NULL	
name	    varchar(20)	    YES		NULL	
major	    varchar(20)	    YES		NULL	
```



- SUM, all the basic:
```
CREATE TABLE student (
    student_id INT PRIMARY KEY,
    name VARCHAR(20),
    major VARCHAR(20)
);

DESCRIBE student;

DROP TABLE student;

ALTER TABLE student ADD gpa DECIMAL(3, 2);

ALTER TABLE student DROP COLUMN gpa;
```