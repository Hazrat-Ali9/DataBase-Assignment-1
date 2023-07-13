# Question : 1  
# Why is composite key called composite primary key? Describe with proper explanation.
# Answer No : 1
In database design, a composite key refers to a combination of two or more columns that are used together to uniquely identify a record in a table. When this composite key is designated as the primary key of the table, it is referred to as a composite primary key.

The concept of a primary key is essential in relational databases as it ensures the uniqueness and integrity of records within a table. Traditionally, a primary key consists of a single column that uniquely identifies each record. However, there are scenarios where a single column cannot guarantee uniqueness, or it may not provide enough information to identify a record uniquely. In such cases, a composite primary key is used.

A composite primary key combines multiple columns to form a unique identifier for a record. The combination of these columns ensures that no two records have the same values across all the key columns. Each column in the composite key contributes to the uniqueness of the primary key.


# Question No : 2
# What is the benefit of using relational database over non-relational database.
# Answer No. 02

 Using a relational database offers several benefits over non-relational (or NoSQL) databases. Here are some advantages of relational databases:

1. Structure and Data Integrity: Relational databases provide a structured way to organize and store data. They enforce data integrity by using predefined schemas, constraints, and relationships between tables. This ensures that data is consistent, accurate, and follows predefined rules, reducing the chances of data corruption or inconsistency.

2. Powerful Querying Capabilities: Relational databases offer a standardized query language, such as SQL (Structured Query Language), which provides a rich set of operations for retrieving, manipulating, and analyzing data. SQL allows for complex joins, aggregations, filtering, and sorting, enabling efficient and flexible querying of data.


3. Data Relationships and Integrity Constraints: Relational databases allow you to define relationships between tables using foreign keys. These relationships maintain data integrity and enforce referential integrity rules, preventing orphaned or inconsistent data. Constraints, such as unique constraints or check constraints, further ensure data validity.

4. Scalability and Performance Optimization: Relational databases have well-established optimization techniques and indexing mechanisms to enhance query performance. They can handle large datasets and efficiently execute complex queries. Additionally, relational databases support vertical and horizontal scaling by distributing data across multiple servers, enabling high scalability when needed.

5. Flexible Data Manipulation: Relational databases provide flexibility in manipulating data. You can easily update, insert, or delete records without affecting the entire database structure. This flexibility allows for efficient data modification and maintenance.


# Question No.3 
# Explain foreign key with proper examples. If foreign key didn’t exist, what would be the problem? - 10
# Answer No.3
A foreign key is a relational database concept that establishes a link or relationship between two tables. It is a field (or combination of fields) in one table that refers to the primary key of another table. The purpose of a foreign key is to enforce referential integrity and maintain the relationship between related tables.

Suppose we have two tables: "Orders" and "Customers." The "Orders" table contains information about customer orders, and the "Customers" table contains information about the customers themselves. Each order is associated with a specific customer. The tables might look like this:

Orders Table:

OrderID	OrderDate	CustomerID
1	      2023-06-01	101
2	      2023-06-02	102
3	      2023-06-03	101

Customers Table:

CustomerID	CustomerName
101	              John Cena
102	              The Rock

In this example, the "CustomerID" column in the "Orders" table serves as a foreign key that references the primary key "CustomerID" in the "Customers" table. This establishes a relationship between the two tables.

The foreign key constraint ensures that every value in the "CustomerID" column of the "Orders" table must exist as a primary key value in the "Customers" table. It enforces referential integrity by preventing the creation of orphaned records or references to nonexistent customers.

Now, let's consider the problems that would arise if foreign keys did not exist:
1. Data Inconsistency: Without foreign keys, it becomes possible to have inconsistent data in the database. For example, a record in the "Orders" table could reference a nonexistent customer in the "Customers" table, leading to data integrity issues.
2. Inefficient Data Retrieval: Without foreign keys, retrieving related data from multiple tables becomes more cumbersome and less efficient. The relationship between tables would need to be managed explicitly in the application logic, resulting in more complex and slower queries.
3. Orphaned Records: Without foreign keys, it would be possible to delete a customer from the "Customers" table without considering the associated orders in the "Orders" table. This would result in orphaned records in the "Orders" table with references to nonexistent customers.      
 

# Question No: 4
# What is the difference between database and MySQL
# Answer No: 4

 The difference between a database and MySQL lies in their respective roles and functionalities:

Database: A database is a structured collection of data that is organized, stored, and managed in a systematic manner. It provides a way to store and retrieve data efficiently and ensures data integrity and consistency. Databases can be classified into various types, such as relational databases (e.g., MySQL, PostgreSQL, Oracle), NoSQL databases (e.g., MongoDB, Cassandra), graph databases (e.g., Neo4j), and more. A database is a broader concept that encompasses different types and technologies used to manage data.

MySQL: MySQL is a specific Relational Database Management System (RDBMS) that falls under the category of relational databases. It is a popular open-source database system that uses Structured Query Language (SQL) for managing and manipulating data. MySQL is known for its scalability, reliability, and ease of use. It provides features such as data storage, retrieval, modification, and support for complex querying using SQL. MySQL can be used as a backend database for various applications and is widely used in web development.

In summary, a database is a general term referring to a structured collection of data, while MySQL is a specific implementation of a relational database management system that uses SQL as its query language. MySQL is just one option among several relational database systems available in the market, and it is chosen based on its specific features, performance, and suitability for a given application or use case.

# Question No : 5                                                
Suppose you have to make a table named student. The table will have the fields - 15
Name
Roll
Class
Blood group
Contact No
Result
Date of Birth
Age
	Write the Datatypes used here


# Answer No : 5
Based on the fields provided for the "student" table, here are the suggested data types for each field:

Name: VARCHAR or TEXT (depending on the maximum length of the name)
Roll: INTEGER
Class: VARCHAR or TEXT
Blood group: VARCHAR or TEXT
Contact No: VARCHAR or TEXT
Result: VARCHAR or TEXT
Date of Birth: DATE or DATETIME
Age: INTEGER


# Question No : 6                                                         
# Create a table in MySQL for the student table described in question 5.	
# Answer No : 6
Below the syntax to create a table named "student" in MySQL using the provided fields:

CREATE database school;

USE school;

CREATE TABLE student (
    Name VARCHAR(50),
    Roll INT,
    Class VARCHAR(20),
    `Blood group` VARCHAR(10),
    `Contact No` VARCHAR(15),
    Result VARCHAR(20),
    `Date of Birth` DATE,
    Age INT
);


# Question No. 08                                                            
# Rename the table named student to a name whatever you want. And then delete the table. Write the SQL syntaxes also. - 10
# Answer No : 8

-- Rename the table student to school_student
ALTER TABLE student RENAME TO school_student;

-- Delete the table school_student
DROP TABLE school_student;






 
 

 
 

















                                               
 







            




                                                                                            

 

    


 

 

 

 


 




 

 


 







