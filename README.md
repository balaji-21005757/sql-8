## Experiment 8
## Aim:
To implement the keyword-Case ,Cross,Join ,full outer joinAssignment

## Algorithm:
1.Start MYSQL Workbench.

2.Create a database to store your data.

3.Use the database and create a table.

4.Inside the table ,create variables with appropriate datatype.

5.Insert values and apply logic to visualize the output.

## Program:
```
CREATE TABLE Library (  
  BookNumber int NOT NULL,  
  BookCode varchar(15) NOT NULL,  
  BookIssue int NOT NULL,  
  CostEach decimal(10,2) NOT NULL,  
  PRIMARY KEY (BookNumber,BookCode)  
); 
INSERT INTO Library(BookNumber, BookCode, BookIssue, CostEach) VALUES    
(10100, 'B18_1749', 30, '136.00'),    
(10100, 'B18_2248', 50, '55.09'),    
(10101, 'B18_2325', 25, '108.06'),    
(10101, 'B18_2795', 26, '167.06'),    
(10102, 'B18_1342', 39, '95.55'),    
(10102, 'B18_1367', 41, '43.13'),    
(10103, 'B10_1949', 26, '214.30'),    
(10103, 'B10_4962', 42, '119.67'),    
(10103, 'B18_2432', 22, '58.34'),    
(10103, 'B18_2949', 27, '92.19'),    
(10104, 'B18_3232', 23, '165.95');
CREATE TABLE Books (  
  BookCode varchar(50) NOT NULL,  
  BookName varchar(100) NOT NULL,  
  BookType varchar(100) NOT NULL,  
  BookVendor varchar(100) NOT NULL,  
  BookDescription varchar(250),  
  BookInStock int NOT NULL,  
  Cost decimal(10,2) NOT NULL,  
  PRIMARY KEY (BookCode)  
) ; 
INSERT INTO Books(BookCode, BookName, BookType, BookVendor, BookDescription, BookInStock, Cost) VALUES    
('B10_001', 'Coding Fundamentals - C', 'Core Book', 'Min Lin Diecast', null, 7933, '48.81'),    
('B10_002', 'Coding Fundamentals - C++', 'Core Book', 'Classic Metal Creations', null, 7305, '98.58'),    
('B10_003', 'Coding Fundamentals - C#', 'Advanced Book', 'Mini Classics', null, 6625, '68.99'),    
('B10_004', 'Coding Fundamentals - PHP', 'E-Book', 'Start Diecast', null, 5582, '91.02'),    
('B10_005', 'Coding Fundamentals - Java', 'E-Book', 'City Art Classics', null, 3252, '85.68'),    
('B10_006', 'Coding Fundamentals - JavaScript', 'E-Book', 'Second Diecast', null, 6791, '103.42'),    
('B12_007', 'Coding Fundamentals - Angular', 'Advanced Book', 'Autoart Studio Design', null, 68, '95.34'),    
('B12_008', 'Coding Fundamentals - R', 'E-Book', 'Second Diecast', null, 3619, '95.59');
---cross join
select 
select_list 
from T1 cross join T2
---Right join
SELECT Student.NAME,StudentCourse.COURSE_ID 
FROM Student
RIGHT JOIN StudentCourse 
ON StudentCourse.ROLL_NO = Student.ROLL_NO;
---full outer join
SELECT Student.NAME,StudentCourse.COURSE_ID 
FROM Student
FULL JOIN StudentCourse 
ON StudentCourse.ROLL_NO = Student.ROLL_NO;
```
## Result:
Therefore we have successfully implemented the keyword-Case ,Cross,Join ,full outer join.
