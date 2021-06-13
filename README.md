# sql-database-index
I have been reading about databases and I learned that you can create an index on your database table and you can use that to search through a database faster.
So I plan on trying that out.

If you would like to see the logs yourself I put the database code in the database.sql file.

This log is from a regular run of selecting from customers where the first name starts with the letter T.
It goes through everyline and gives back each of the rows with a first name that starts with the letter T.

Seq Scan on customers  (cost=0.00..34.33 rows=76 width=94)

This is after an index is created on the first_name column in the customers table.
With the index on the table the cost for searching for the exact same thing is less.
The larger the table the greater the cost difference between each run will be.

Bitmap Heap Scan on customers  (cost=5.04..24.96 rows=76 width=94)

