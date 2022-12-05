```sql
1) SELECT * FROM `students` WHERE YEAR(date_of_birth) = 1990;
2) SELECT * FROM `courses` WHERE cfu >10;
3) SELECT * FROM `students` WHERE TIMESTAMPDIFF(YEAR, `date_of_birth`, CURDATE()) = 30;
4) SELECT * FROM `courses` WHERE period = 'I semestre' && `year` = '1';
5) SELECT * FROM `exams` WHERE `hour` > '14:00:00' && `date` = '2020-06-20';
6) SELECT * FROM `degrees` WHERE `name` LIKE '%Magistrale%';
7) SELECT COUNT(*) FROM `departments`;
8) SELECT COUNT(*) FROM `teachers` WHERE `phone` is Null;
```