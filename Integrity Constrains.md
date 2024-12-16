Integrity constraints  in a database are rules enforced to ensure the accuracy, consistency, and reliability of data within the database. These constraints define certain conditions that the data must satisfy to maintain its validity and prevent anomalies.

---

### **Types of Integrity Constraints**

#### **1. Primary Key Constraint**

- Ensures that a column (or set of columns) uniquely identifies each row in a table.
- A table can have only one primary key, and it cannot contain `NULL` values.

**Example**:

sql


`CREATE TABLE Students (     StudentID INT PRIMARY KEY,  -- Primary key     Name VARCHAR(50),     Age INT );`

#### **2. Foreign Key Constraint**

- Establishes a relationship between two tables by enforcing a link between the columns of one table and the primary key of another.
- Ensures **referential integrity**, meaning that a value in a foreign key column must exist in the referenced table.

**Example**:

sql

Copy code

`CREATE TABLE Courses (     CourseID INT PRIMARY KEY,     CourseName VARCHAR(50) );  CREATE TABLE Enrollments (     EnrollmentID INT PRIMARY KEY,     StudentID INT,     CourseID INT,     FOREIGN KEY (CourseID) REFERENCES Courses(CourseID)  -- Foreign key constraint );`

#### **3. Unique Constraint**

- Ensures that all values in a column (or a group of columns) are distinct.
- Unlike a primary key, a table can have multiple unique constraints, and `NULL` values are allowed (but only one per column).

**Example**:

sql

Copy code

`CREATE TABLE Employees (     EmployeeID INT PRIMARY KEY,     Email VARCHAR(100) UNIQUE  -- Unique constraint );`

#### **4. Not Null Constraint**

- Ensures that a column cannot contain `NULL` values, meaning it must always have a value.

**Example**:

sql

Copy code

`CREATE TABLE Products (     ProductID INT PRIMARY KEY,     ProductName VARCHAR(50) NOT NULL,  -- Not null constraint     Price DECIMAL(10, 2) );`

#### **5. Check Constraint**

- Enforces that the values in a column meet a specific condition or expression.
- Ensures **domain integrity** by restricting values to a valid range or pattern.

**Example**:

sql

Copy code

`CREATE TABLE Employees (     EmployeeID INT PRIMARY KEY,     Age INT CHECK (Age >= 18 AND Age <= 65),  -- Check constraint     Salary DECIMAL(10, 2) );`

#### **6. Default Constraint**

- Specifies a default value for a column if no value is provided during data insertion.

**Example**:

sql

Copy code

`CREATE TABLE Orders (     OrderID INT PRIMARY KEY,     OrderDate DATE DEFAULT GETDATE()  -- Default constraint );`

#### **7. Domain Constraints**

- Implicitly enforced constraints based on the data type of a column (e.g., `INT`, `VARCHAR`, etc.), which ensures that data in the column adheres to the specified type.

**Example**:

sql

Copy code

`CREATE TABLE Accounts (     AccountID INT PRIMARY KEY,     Balance DECIMAL(15, 2)  -- Ensures the data type is respected );`

---

### **Why Use Integrity Constraints?**

1. **Data Consistency**:
    - Prevents inconsistent or invalid data from being stored.
2. **Reliability**:
    - Guarantees the reliability of data relationships, such as ensuring referenced data exists.
3. **Data Accuracy**:
    - Restricts values to a specific range or format, reducing errors.
4. **Reduces Application Logic**:
    - Enforces rules directly at the database level instead of relying on external code.