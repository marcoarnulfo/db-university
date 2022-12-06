```sql
1) SELECT `students`.`id` AS `Student_Id`, `students`.`degree_id`, `students`.`name`, `students`.`surname`
FROM `students`
JOIN `degrees`
ON `degrees`.`id` = `students`.`degree_id`
WHERE degrees.name = "Corso di Laurea in Economia"
2) SELECT `degrees`.`department_id`, `degrees`.`name` FROM `degrees` JOIN `departments` ON `degrees`.`department_id` = `departments`.`id`
3) SELECT `teachers`.`id`, `teachers`.`name`, `teachers`.`surname`, `courses`.`name` FROM `teachers` JOIN `course_teacher` ON `teachers`.`id` = `course_teacher`.`teacher_id` JOIN `courses` ON `courses`.`id` = `course_teacher`.`course_id` WHERE `teacher_id` = 44;
4) SELECT `students`.`surname`, `students`.`name` AS 'name_student', `students`.`registration_number`, `degrees`.`name`, `degrees`.`level`, `departments`.`name` AS 'departments_name'
FROM `students`
JOIN `degrees`
ON `students`.`degree_id` = `degrees.id`
JOIN `departments`
ON `degrees`.`department_id` = `departments`.`id` 
ORDER BY `students`.`surname`, `students`.`name`;
5) SELECT `degrees`.`name` AS 'Degrees_name', `degrees`.`level`, `degrees`.`address`, `degrees`.`email`, `degrees`.`website`, `courses`.`name` AS 'corse_name', `teachers`.`name` AS 'teacher_name', `teachers`.`surname`
FROM `degrees`
JOIN `courses`
ON `degrees`.`id` = `courses`.`degree_id`
JOIN `course_teacher`
ON `courses`.`id` = `course_teacher`.`course_id`
JOIN `teachers`
ON `teachers`.`id` = `course_teacher`.`teacher_id`;
6) SELECT DISTINCT `teachers`.`name`, `teachers`.`surname`, `teachers`.`phone`, `teachers`.`email`, `teachers`.`office_addressb`, `teachers`.`office_number`, `departments`.`name` as 'departments'
FROM `teachers`
JOIN `course_teacher`
ON `teachers`.`id` = `course_teacher`.`teacher_id`
JOIN `courses`
ON `courses`.`id` = `course_teacher`.`course_id`
JOIN `degrees`
ON `degrees`.`id` = `courses`.`degree_id`
JOIN `departments`
ON `departments`.`id` = `degrees`.`department_id`
WHERE `departments`.`name` = 'Dipartimento di Matematica';
```