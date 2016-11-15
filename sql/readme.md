### Getting Started with SQL

SQL has sever dialects, the two that will be in use here are Postgres and SQL Server.
Most examples will feature Postgres syntax. Converting to SQL Server is often fairly simple though some functions can be quite different.


### Basic query structure

The basic parts of a SQL query are:
    - SELECT
    - FROM
    - WHERE

*Note: SQL style typically capitalizes keywords *

SELECT:
    SELECT will determine which which fields are returned in your results.
    Use a comma to separate fields chosen for selection. No trailing comma should be present after the last field.
    The * operator will select all fields for a table.
    When using joins the * operator will return all results for both tables unless other parameters are used.

FROM:
    FROM determines the source table for data selection.

WHERE:
    WHERE clauses serve as filters for data selection. For exmple, one can limit results based on date ranges.
    WHERE conditions support boolean operators.
    *Note: do not use commas in the WHERE clause.*

Example:
    ```SELECT name, type
        FROM database.table
        WHERE most_recent_data = 'Y'```