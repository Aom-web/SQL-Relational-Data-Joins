# SQL Relational Data Joins

## Overview
Application of different types on join to answer questions from two tables in SQL

## Image of table used 

<img width="499" height="194" alt="1" src="https://github.com/user-attachments/assets/bae9983f-3478-4df8-9b01-c8a11d1ed4cc" />

## Inner Join
### Question 1 
what are the names of customers with orders less than 800?

<img width="409" height="312" alt="2" src="https://github.com/user-attachments/assets/780f72ef-ec3d-479f-bd01-365bfc527e2d" />

## Left Join
### Question 2
which customer has no order in the table?

<img width="447" height="328" alt="3" src="https://github.com/user-attachments/assets/94ee1c9f-2cf9-4e29-a0c7-300419ea64f1" />

### 2a : I want to only see customers with no order displayed.

<img width="472" height="263" alt="4" src="https://github.com/user-attachments/assets/2b2f4c77-cb8f-40c0-abc3-8da44d11ed26" />

### 2b : I want the NULL cell in Question 2 above to show 'NO ORDER', so what do i do?

### Step 1: re-write the SQL code for LEFT JOIN introducing COALESCE

<img width="599" height="331" alt="5" src="https://github.com/user-attachments/assets/2185a8ac-93e9-4d62-8bae-9e574b49ec4e" />

### Step 2: rename the 3rd column of the table by introducing the 'AS' clause.

<img width="646" height="320" alt="6" src="https://github.com/user-attachments/assets/f0d0acc8-ddb6-4998-af4a-d3d753831689" />

## Right Join
### Question 3
which customer has an order without a name input

<img width="419" height="329" alt="7" src="https://github.com/user-attachments/assets/d68c7786-0441-41e5-8203-e254b92a9dc5" />

## Full Join
### List all customers including the ones without a purchase and name

<img width="470" height="344" alt="8" src="https://github.com/user-attachments/assets/2d369d07-da40-4dcd-bed0-18fcae2c6d6a" />
