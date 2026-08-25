The given MySQL code creates a complete college database management system named college_demo and defines four interconnected tables: department, student, course, and enrollment. First, CREATE DATABASE college_demo creates a new database, while USE college_demo selects it for further operations.
The department table stores information about different departments, where dept_id is an integer primary key that uniquely identifies each department, and dept_name is a maximum 50-character field that is both UNIQUE and NOT NULL, ensuring that every department has a name and that no two departments have the same name.
The student table stores student information, with roll_no as the primary key for uniquely identifying each student, name as a mandatory field, email as a unique field to prevent duplicate email addresses, and dept_id as a foreign key referencing the dept_id of the department table, which establishes a relationship between students and their departments.
The course table stores information about courses, where course_id uniquely identifies each course, course_name contains the course name and cannot be empty, and dept_id identifies the department offering the course through a foreign key relationship with the department table.
Finally, the enrollment table records which students are enrolled in which courses and in which semester.
It contains roll_no and course_id as foreign keys referencing the student and course tables respectively, while semester stores the semester number and uses a CHECK constraint to allow only values between 1 and 8.
The grade field stores the student's grade using CHAR(2).
The combination of roll_no, course_id, and semester is defined as a composite primary key, ensuring that the same student cannot be enrolled in the same course more than once during the same semester.
Overall, this database demonstrates the use of primary keys, foreign keys, composite keys, unique constraints, not-null constraints, and check constraints, while establishing relationships between departments, students, courses, and student enrollments in a structured and consistent manner.

Normalization of College Database

The database is normalized up to Third Normal Form (3NF).

1NF: All fields contain atomic values and no repeating groups.
2NF: All non-key attributes depend on the complete primary key.
3NF: There are no transitive dependencies between non-key attributes.

The data is divided into Department, Student, Course, and Enrollment tables to reduce data redundancy and avoid insert, update, and delete anomalies.

Therefore, the database follows a well-structured normalized relational design.
