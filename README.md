# EqualSets

Your mission, should you accept:

1) Download setup.sql and execute it an a database of your choosing. It creates the `dbo.SupplierProduct` table and the `dbo.EqualSetsTest` stored procedure. It also inserts some 1000 suppliers with several products each into that table.
2) There are two suppliers in the dataset that have the exact same list of products each. Write a T-SQL query that finds them.
3) Call the `EXEC dbo.EqualSetsTest @P1=?, @P2=?;` procedure passing in the two `SupplierId` Values.
4) The output is a secret code word painted in the spatial results tab. !!Keep that word to yourself!! (If there's no word, you've got the wrong result.)
5) Measure the total number of logical reads your query used to find the two suppliers. Report that number to me as soon as you have it.


The team with the lowest number of logical reads wins. In case of a tie, the first submission wins.

For reference, I came up with 5 different solutions ranging from just over 2,000,000 logical reads to 71. The slowest executed in about 1 minute (CPU-bound but only 433,000 logical reads), the fastest finished after 8 ms. (That's in a VM with access to 3 CPU cores on my laptop.)

Good Luck!
