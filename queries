Use Northwind;

## Question 1

SELECT * FROM Region;

UPDATE Region SET RegionDescription = 'AFRICA' WHERE RegionID = 3;


## Question 2

CREATE VIEW Result AS 
SELECT Suppliers.CompanyName AS 'Name of the company',
		Suppliers.ContactName AS 'Contact Name (Supplier)',
		Customers.ContactName AS 'Full Name (Contact Person)',
		SUBSTRING(Customers.ContactName, 1, CHARINDEX(' ', Customers.ContactName) - 1 ) AS 'First Name (Contact Person)',
		SUBSTRING(Customers.ContactName, CHARINDEX(' ', Customers.ContactName) + 1, LEN(Customers.ContactName) ) AS 'Surname (Contact Person)',
		Products.ProductName AS 'Product Name',
		Categories.CategoryName AS 'Category Name',
		Suppliers.Address + ', ' + Suppliers.City AS 'AddressCity (Combined)'
FROM Products
JOIN Categories ON Products.CategoryID = Categories.CategoryID
JOIN Suppliers ON Products.SupplierID = Suppliers.SupplierID
JOIN Employees ON Suppliers.SupplierID = Employees.EmployeeID
JOIN Customers ON Customers.CustomerID = Customers.CustomerID
;

SELECT * FROM Result;

DROP VIEW Result;


## Question 3

SELECT * FROM AdventureWorksDW2022.dbo.FactResellerSales;
