```sql
1) SELECT YEAR(enrolment_date) AS 'anno', COUNT(id) AS 'iscritti' FROM `students` GROUP BY YEAR(enrolment_date);

2) SELECT COUNT(id) AS 'insegnante', `office_address` AS 'edificio' FROM `teachers` GROUP BY `office_address`;

3) SELECT `exam_id` AS 'appello', AVG(`vote`) AS 'media voto' FROM `exam_student` GROUP BY `exam_id`;

4) SELECT `department_id` as 'Dipartimento', COUNT(id) AS 'numero corsi' FROM `degrees` GROUP BY `department_id`;
```