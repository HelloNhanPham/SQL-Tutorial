# Stored Procedures
A stored procedure in SQL is a group of SQL queries that can be saved and reused multiple times. It is very useful as it reduces the need for rewriting SQL queries. It enhances efficiency, reusability, and security in database management.

Users can also pass parameters to stored procedures so that the stored procedure can act on the passed parameter values.

Stored Procedures are created to perform one or more DML operations on the Database. It is nothing but a group of **SQL statements** that accepts some input in the form of parameters, performs some task, and may or may not return a value. 

## Syntax
Two important syntaxes for using stored procedures in SQL are:

**Syntax to Create a Stored Procedure**

> [!IMPORTANT]
> 
>     CREATE PROCEDURE procedure_name
>
>     (parameter1 data_type, parameter2 data_type, …)
>
>     AS
>
>     BEGIN
>
>         — SQL statements to be executed
>
>     END

**Syntax to Execute the Stored Procedure**

> [!IMPORTANT]
> 
>     EXEC procedure_name parameter1_value, parameter2_value, ..

**Parameter**
The most important part is the parameters. Parameters are used to pass values to the Procedure. There are different types of parameters, which are as follows: 

1. **BEGIN**: This is what directly executes or we can say that it is an executable part.
2. **END**: Up to this, the code will get executed.

## SQL Stored Procedure Example
Let’s look at an example of Stored Procedure in SQL to understand it better.

Imagine a database named “SampleDB”, a table named “Customers” with some sample data, and a stored procedure named” GetCustomersByCountry”.

The stored procedure takes the parameter “Country” and returns a list of customers from the “Customers” table that matches the specified country. Finally, the stored procedure is executed with the parameter “Sri Lanka” to retrieve the list of customers from Sri Lanka.

**Query**

> [!IMPORTANT]
> Create a new database named "SampleDB"
>
>      CREATE DATABASE SampleDB;
>
> Switch to the new database
>
>     USE SampleDB;
>
> Create a new table named "Customers"
>
>     CREATE TABLE Customers (
>
>         CustomerID INT PRIMARY KEY,
>
>         CustomerName VARCHAR(50),
>
>         ContactName VARCHAR(50),
>
>         Country VARCHAR(50)
>
>     );
>
> Insert some sample data into the Customers table
>
>     INSERT INTO Customers (CustomerID, CustomerName, ContactName, Country)
>
>     VALUES
>
>             (1, 'Shubham', 'Thakur', 'India'),
>
>             (2, 'Aman ', 'Chopra', 'Australia'),
>
>             (3, 'Naveen', 'Tulasi', 'Sri lanka'),
>
>             (4, 'Aditya', 'Arpan', 'Austria'),
>
>             (5, 'Nishant. Salchichas S.A.', 'Jain', 'Spain');
>
> Create a stored procedure named "GetCustomersByCountry"
>
>     CREATE PROCEDURE GetCustomersByCountry
>
>     @Country VARCHAR(50)
>
>     AS
>
>     BEGIN
>
>         SELECT CustomerName, ContactName
>
>         FROM Customers
>
>         WHERE Country = @Country;
>
>     END;
>
> Execute the stored procedure with parameter "Sri lanka"
>
>     EXEC GetCustomersByCountry @Country = 'Sri lanka';

