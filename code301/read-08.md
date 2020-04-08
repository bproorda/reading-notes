# SQL

Structured Query Language (SQL) is the standard language for interacting with and extracting data from relational databases.
 - relational database table with labeled columns of properties, each row is an instance.
 - Writing SQL queries
   - to get data from table you need query
   - ` SELECT column_name FROM table_name `
   - all caps not required but helps to make SQLs from other programming
   - use ` SELECT * FROM table_name ` to select all the table
- **Queries with Constraints**
  - the results of your queries can be limited using conditionals
  - format: `SELECT column_name FROM table_name WHERE condition AND/OR condition2`
  - operators
    **numerical operators**
    - =, !=, < <=, >, >=
    - BETWEEN ... AND ... number is within range of two numbers
    - NOT BETWEEN ... AND ...
    - IN (...) number exists in a list
    - NOT IN (...)
    **String Operators**
    - *All strings must be quoted so that the query parser can distinguish words in the string from SQL keywords.*
    - =	Case sensitive exact string comparison (notice the single equals)
    - != or <>	Case sensitive exact string inequality comparison
    - LIKE	Case insensitive exact string comparison
    - NOT LIKE
    - %	Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE) 
    - IN (…)	String exists in a list
    - NOT IN (…)	String does not exist in a list
- **Filtering and Sorting**
  - `SELECT DISTINCT column_name` prevents duplicate column values
  - use `ORDER BY` to sort results with ABC, alphabetical, ASC/DESC, ascending/descending
  - use LIMIT to limit the number of rows returned
  - use OFFSET to specify where to begin counting rows from
- **Inserting Rows**
  - the *database schema* describes the structure of each table and datatypes each column contain
  - `INSERT INTO mytable VALUES (value_or_expr, another_value_or_expr, …), (value_or_expr_2, another_value_or_expr_2, …), …;`
  - if you are entering incomplete data, specify the columns `INSERT INTO mytable (column, another_column, …) VALUES...`
- **Updating Rows**
  - `UPDATE mytable SET column = value_or_expr, other_column = another_value_or_expr, … WHERE condition;`
  - datatypes must match the ones specified in the schema
- **Deleting Rows**
  - `DELETE FROM mytable WHERE condition; example` example: `DELETE FROM movies where year < 2005;`
  - if the WHERE condition is left out, the table will be **EMPTIED!**
- **Creating Tables**
  - `CREATE TABLE IF NOT EXISTS mytable (column DataType TableConstraint DEFAULT default_value, another_column DataType TableConstraint DEFAULT default_value, …);`
- **Altering Tables**
  - Adding columns
  - `ALTER TABLE mytable ADD column DataType OptionalTableConstraint DEFAULT default_value;`
  - Removing columns
  - `ALTER TABLE mytable DROP column_to_be_deleted;`
  - Renaming table
  - `ALTER TABLE mytable RENAME TO new_table_name;`
  - Deleting (Dropping) Table
  - `DROP TABLE IF EXISTS mytable;`
    
