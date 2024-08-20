# Database and Database Management System

## Database
A database is an organized collection of structured data stored electronically. It allows for efficient data storage, retrieval, and management, typically in tables. Examples include MySQL, Oracle, and MongoDB.

## Database Management System (DBMS)
A DBMS is software that manages databases, providing tools for defining, querying, updating, and securing data. It acts as an interface between the database and users or applications, ensuring data integrity, security, and efficient access. Examples include SQL Server, PostgreSQL, and MongoDB.

## Constraints
Constraints in a database are rules applied to columns in a table to enforce data integrity, accuracy, and reliability. They ensure that the data entered into the database adheres to certain conditions or rules.

### Types of Constraints

1. **Primary Key Constraint**
   - Ensures each row in the table is unique and not null.
   - Example: `PRIMARY KEY (ID)`

2. **Foreign Key Constraint**
   - Enforces a link between two tables by ensuring the value in a column matches a value in the referenced table.
   - Example: `FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)`

3. **Unique Constraint**
   - Ensures that all values in a column or a set of columns are unique across the table.
   - Example: `UNIQUE (Email)`

4. **Not Null Constraint**
   - Ensures that a column cannot contain NULL values.
   - Example: `Name VARCHAR(100) NOT NULL`

5. **Check Constraint**
   - Ensures that all values in a column satisfy a specific condition.
   - Example: `CHECK (Age >= 18)`

6. **Default Constraint**
   - Assigns a column default value if no value is specified during data insertion.
   - Example: `Salary DECIMAL(10, 2) DEFAULT 50000`

## Primary Key
A primary key is a column or a combination of columns in a database table that uniquely identifies each row in that table. It ensures that no two rows have the same primary key value, maintaining the integrity and uniqueness of the data.

### Key Characteristics
- **Uniqueness**: Each value in the primary key column(s) must be unique.
- **Not Null**: A primary key cannot contain NULL values.
- **Single or Composite**: It can be a single column (e.g., ID) or a combination of columns (composite key, e.g., FirstName + LastName).

**Example**:
```sql
CREATE TABLE Student (
  UserID INT PRIMARY KEY,
  Username VARCHAR(50),
  Email VARCHAR(100)
);
