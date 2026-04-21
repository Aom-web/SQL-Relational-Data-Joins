## SQL Relational Data Joins

## Overview
Application of different types on join to answer questions from two tables in SQL

## Image of table used 

<img width="499" height="194" alt="1" src="https://github.com/user-attachments/assets/bae9983f-3478-4df8-9b01-c8a11d1ed4cc" />

## Inner Join

### Question 1 

what are the names of customers with orders less than 800?

```SQL
SELECT Customers.id, Customers.name, Orders.Amount
FROM Customers
JOIN Orders
ON Customers.id = Orders.id;
```
<img width="169" height="116" alt="1" src="https://github.com/user-attachments/assets/89027a40-42d6-4eee-bd00-9e832265082f" />

## Left Join

### Question 2

which customer has no order in the table?

```SQL
SELECT Customers.id, Customers.name, Orders.Amount
FROM Customers
LEFT JOIN Orders
ON Customers.id = Orders.id;
```
<img width="170" height="135" alt="1" src="https://github.com/user-attachments/assets/158c98e6-9d76-4db3-9f6f-73e250ca7f8c" />

### 2a 

To only see customers with no order displayed.

```SQL
SELECT Customers.id, Customers.name, Orders.Amount
FROM Customers
LEFT JOIN Orders
ON Customers.id = Orders.id
WHERE Orders.Amount is NULL;
```
<img width="181" height="67" alt="2" src="https://github.com/user-attachments/assets/2b4eb3a3-de11-42aa-9a46-b83fdafe2306" />

### 2b 

To make the NULL cell in Question 2 above to show 'NO ORDER'

### Step 1

re-write the SQL code for LEFT JOIN introducing COALESCE

```SQL
SELECT Customers.id, Customers.name,COALESCE (Orders.Amount, 'NO ORDER')
FROM Customers
LEFT JOIN Orders
ON Customers.id = Orders.id;
```
<img width="355" height="134" alt="3" src="https://github.com/user-attachments/assets/c189e7d9-b76f-40b2-87ab-15e322d22a71" />

### Step 2

rename the 3rd column of the table by introducing the 'AS' clause.

```SQL
SELECT Customers.id, Customers.name,COALESCE (Orders.Amount, 'NO ORDER') AS Amount
FROM Customers
LEFT JOIN Orders
ON Customers.id = Orders.id;
```
<img width="198" height="141" alt="4" src="https://github.com/user-attachments/assets/af2829a6-2868-48ac-84f0-5b2714b9b17f" />

## Right Join

### Question 3

Identify all orders placed, including those that are not linked to a registered customers name

```SQL
SELECT Customers.id, Customers.name, Orders.Amount
FROM Customers
RIGHT JOIN Orders
ON Customers.id = Orders.id;
```
<img width="167" height="134" alt="5" src="https://github.com/user-attachments/assets/9048b655-95f4-42e9-b095-7e39bcfa5e44" />

## Full Join

 List every unique customer and every unique order record to identify both customers who haven't ordered anything and orders that aren't assigned to a customer

```SQL
SELECT Customers.id, Customers.name, Orders.Amount
FROM Customers
FULL JOIN Orders
ON Customers.id = Orders.id;
```
<img width="178" height="163" alt="6" src="https://github.com/user-attachments/assets/804be874-a396-422a-89b1-2decce4cae8d" />
