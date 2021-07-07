 MySQL-files
 "REAL SQL QUERIES 50 CHALLENGES (Practice for Reporting and Analysis)" is a book by Brian Cohen, Neil Pepi, Neerja Mishra. The Questions in the book is based on Adventure Works Database. It is a big database and has many tables and hence good for practicing.
 The book was mainly for SQL Server users as AdventureWorks is a sample database created for SQL Server. I am a user of MySQL and therefore thought I wouldn't be able to use this book for practicing. Fortuantely someone created a copy of AdventureWorks database which can be used in MySQL. The link to get the database is - https://sourceforge.net/projects/awmysql/
 Download the database and extract it and run it on MySQL workbench. You will have the database in MySQL and then you can start practicing.
 As I solved the queries, I realized there are versions of adventureworks database. And the database we get using the link is a little different. That doesn't hinder in any way practicing the questions in the book. I am mentioning the changes between the database the book is based on and the database we get.
 Changes - 
1) person.person table   is   Contact table 
2) salesperson.BusinessEntityID = Salesperson.salespersonID
3) Person.BusinessEntityAddress  =  CustomerAddress (Probably)
4) person.address = address
5) SalesTerritoryHistory.BusinessEntityID = SalesTerritoryHistory.SalesPersonID
6) Person.Person = Contact Table
7) Contact.contactID = COntact.BusinessEntityID
8) BusinessEntityAddress table = VendorAddress Table
9) We don't have BusinessEntityID column in VendorAddress table and Store table. Therefore, we cannot execute the query if 
we need them. Q20 needs.
10) In employee table, there's no OrganizationalLevel column.
11) We don't have EmailAddress table.
12) Q17 - There's problem. There's no StoreID column in Store. Solution also says there is a table called StoreID in Customer table.
However, there is no StoreID column in entire database. 
Anyway, the problem is not difficult, we just have to use datediff() function. And then in the WHERE clause use the condition as 
shown in solution.


If you are looking at the queries I created for MySQL in the file, you will see that some queries are needlessly large. This is because I directly used subqueries instead of creating a View or Temporary table. So where I could have used just one word, you might see a complete big query. For ex, if you see solution of Question 2, Part 2 is Part 1 except the first two lines. (This was because I avoided creating Views or Temporary Tables)
