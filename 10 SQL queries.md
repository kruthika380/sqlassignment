--QUESTION 1 -- INIT database -- Create the Students table CREATE TABLE Students ( student_id INT PRIMARY KEY, name VARCHAR(50), age INT, grade_level INT );

-- Create the Courses table CREATE TABLE Courses ( course_id INT PRIMARY KEY, course_name VARCHAR(50), credits INT );

-- Create the Enrollments table CREATE TABLE Enrollments ( enrollment_id INT PRIMARY KEY, student_id INT, course_id INT, grade DECIMAL(3, 2), FOREIGN KEY (student_id) REFERENCES Students(student_id), FOREIGN KEY (course_id) REFERENCES Courses(course_id) );

-- Insert sample data into Students INSERT INTO Students (student_id, name, age, grade_level) VALUES (1, 'Alice', 20, 3), (2, 'Bob', 21, 4), (3, 'Charlie', 19, 3), (4, 'Diana', 22, 4), (5, 'Ethan', 20, 3);

-- Insert sample data into Courses INSERT INTO Courses (course_id, course_name, credits) VALUES (1, 'Math', 3), (2, 'Science', 4), (3, 'History', 3), (4, 'Art', 2);

-- Insert sample data into Enrollments INSERT INTO Enrollments (enrollment_id, student_id, course_id, grade) VALUES (1, 1, 1, 3.5), (2, 1, 2, 4.0), (3, 2, 1, 2.5), (4, 2, 3, 3.0), (5, 3, 2, 3.0), (6, 3, 4, 2.0), (7, 4, 1, 3.5), (8, 4, 3, 4.0), (9, 5, 2, 3.0), (10, 5, 4, 3.5); SELECT AVG(grade) AS average_grade FROM Enrollments;

