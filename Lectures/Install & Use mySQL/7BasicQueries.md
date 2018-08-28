- READ datas:
```
SELECT student.name, student.major
FROM student
ORDER BY name; // this will be all the student names in alphabet order
```
- It also can be the backward the alphabet order
```
SELECT * 
FROM student
ORDER BY name DESC; //backward the alphabet order
```
```
SELECT * 
FROM student
ORDER BY student_id ASC; //order from 1 to up in number order
```
```
SELECT * 
FROM student
WHERE major = 'Chemistry';
```
```
SELECT * 
FROM student
WHERE major = 'Chemistry' OR major = 'Biology';
```
```
SELECT * 
FROM student
WHERE major = 'Chemistry' OR name = 'Kate';
```
```
SELECT * 
FROM student
WHERE name IN ('Claire', 'Kate', 'Mike'); //get any student with the name is Claire, or Kate, or Mike.
```