Relational Database (SQL)

- Relational Database Management System (RDMS)
  + Help users create and maintain a relational database
    * mySQL, Oracle, postgreSQL, mariaDB, etc. 
    (To download mySQL to macOS, check out this link https://dev.mysql.com/downloads/mysql/ and choose macOS 10.13 (x86, 64-bit), DMG Archive to download)

- Structured Query Language (SQL)
  + Standardized language for interacting with RDMS
  + Used to perform C.R.U.D. operations, as well as other administrative tasks (user management, security, backup,etc.)
  + Used to define tables and structures
  + SQL code used on one RDMS is not always portable to another without modification. 


    * We can use SQL to get RDMS to do things for us:
      1. Create, read, update, and delete data
      2. Create and manage database
      3. Design and create database tables
      4. Perform administration tasks (security, user management, import/export, etc.)

- SQL implementations vary between systems
  + Not all RDMS follow the the SQL standard 
  + The concepts are the same but the implementation may vary

- SQL is actually a hybrid language, it's basically 4 types of languages in 1:
  + Data Query Language (DQL)
    * Used to query the database for information
    * Get information that it is already stored there
  + Data Definition Language (DDL)
    * Used for definiting database schemas
  + Data Control Language (DCL)
    * Used for controlling access to the data in the database 
    * User and permission management
  + Data Manipulation Language (DML)
    * Used for inserting, updating, and deleting data in the database