#StudentAcademicManagementSystem
This project is based on core Database Management System (DBMS) concepts to efficiently manage student academic data. It uses the Entity-Relationship (ER) model where tables like STUDENT, STUDENT_SEMESTER, STUDENT_MARKS, and SEMESTER_SUMMARY represent entities, and relationships such as one-to-many (one student having multiple semesters and subjects) are established using primary and foreign keys. Normalization is applied to reduce data redundancy by separating student, semester, and marks data into different tables. SQL joins are used to retrieve combined data from multiple tables. The project also implements stored procedures for reusable logic and triggers for automatic calculations like SGPA, percentage, and result updates. Aggregate functions such as SUM are used for computing totals, while constraints like PRIMARY KEY, FOREIGN KEY, and NOT NULL ensure data integrity and consistency. Overall, the system demonstrates structured data organization, relationship management, and automation in a real-world academic database scenario.
This project is a Student Academic Database System built using SQL Server. 
It manages:
1. Student Information
2. Semester-wise Enrollment
3. Subject-wise Marks
4. Automatic Result Calculation
5. SGPA, Percentage, and Division
Entities (Tables)
1. STUDENT - Stores basic student information.
➡ One student can have multiple semesters.

2. STUDENT_SEMESTER - Stores semester-wise data like roll no, result, branch.
➡ Each semester belongs to one student.

3. STUDENT_MARKS - Stores subject-wise marks for each semester.
➡ One semester has many subjects.

4. SEMESTER_SUMMARY - Stores calculated result (SGPA, total marks, division).
➡ One record per student per semester.

5. EDUCATIONAL_LEVEL - Stores qualification details (10th, 12th, B.Tech).
➡ One student can have multiple education records.

 6. Relationships
STUDENT → STUDENT_SEMESTER = One-to-Many
STUDENT_SEMESTER → STUDENT_MARKS = One-to-Many
STUDENT_SEMESTER → SEMESTER_SUMMARY = One-to-One
STUDENT → EDUCATIONAL_LEVEL = One-to-Many

Key Concepts
Primary Key (PK) → Unique ID (e.g., STUDENT_ID)
Foreign Key (FK) → Links tables
One-to-Many → One record linked to many
One-to-One → One record linked to one

Logic Used
SGPA = Total GPU / Total Credits
Percentage = (Obtained / Total) × 100
Result = PASS / FAIL
Division = Based on percentage

🚀 Conclusion
This ER model:
✔ Organizes academic data properly
✔ Supports multiple semesters
✔ Automates result calculation
✔ Represents real-world college system
