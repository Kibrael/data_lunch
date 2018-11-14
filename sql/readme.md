### Getting Started with SQL

SQL has sever dialects, the two that will be in use here are Postgres and SQL Server.
Most examples will feature Postgres syntax. Converting to SQL Server is often fairly simple though some functions can be quite different.


### Basic Query Structure

The basic parts of a SQL query are:  
    - SELECT  
    - FROM  
    - WHERE  

*Note: SQL style typically capitalizes keywords *  

**Select:**  
    SELECT will determine which which fields are returned in your results.  
    Use a comma to separate fields chosen for selection. No trailing comma should be present after the last field.  
    The * operator will select all fields for a table.  
    When using joins the * operator will return all results for both tables unless other parameters are used.  

**From:**  
    FROM determines the source table for data selection.  

**Where:**  
    WHERE clauses serve as filters for data selection. For exmple, one can limit results based on date ranges.  
    WHERE conditions support boolean operators.  
    *Note: do not use commas in the WHERE clause.*  

**Example:**  
    ```SELECT name, type  
        FROM database.table  
        WHERE most_recent_data = 'Y'```  
        
**Intermediate Usage**  

**Order By**  
    ORDER BY statements allow the results to be returned in a hierarchichal ranking. This can be ascending or descending as specified using `ASC` or `DESC`. One column name is required, but multiple can be listed. Multiple ORDER BY fields should be separated by commas.

**Group By**  
    GROUP BY allows results to be aggregated. Every field in the SELECT statement must be listed in the GROUP BY statement or contained in an aggregate function (such as COUNT()). List fields, separated by commas, in the order of aggregation precedence.  

**Union/Union All**  
    Allows query result sets to be combined. UNION will return distinct results, UNION ALL will return the entire population of both queries.  
    
**Joins**
    JOIN allows data tables to be combined so that filtering criteria may be used against additional tables, or to link data from separate tables together in a single result set. Different JOIN syntax is used to establish the domain of the results.    
    
   Joining requires the use of the ON operator. Using ON requires the use of a key for each table being joined.   
    `ON a.key = b.key` is common syntax.
    
   When joining tables it is common practice to alias them. Meaning, to give them a shorter name that is easier to read/type/process.  
    This takes the form: 
    `JOIN database2.tablename AS db2` 
    where db2 is the alias for the second table.
    
   - Join: Results will be from the subset where both tables have data present
   - Left Join: Results will include all of the table specified in the FROM clause and any additional results that match from the joined table will be included.
   - Right Join: Results will include all of the table specified in the RIGH JOIN clause, any additional results that match from the table in the FROM clause will be included.
   - Inner Join: Different syntax for JOIN
   - Outer Join: All results from both tables will be included, also known as FULL JOIN or FULL OUTER JOIN.
    *Note: this is a basic overview, specifying join keys parameters can drastically change the population of result sets. Check the graphic in this repository for further explanation*
    
   **Join Syntax**
    
     SELECT 
            table1.field1, 
            table1.field2, 
            table2.field3  
     FROM 
            database1.tablename AS table1  
     JOIN 
            database1.tablename2 AS table2  
     ON 
            table1.key = table2.key
     WHERE 
            most_recent = 'Y'
        
