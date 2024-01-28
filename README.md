# Project Title: Zomato Dataset Analysis with SQL
## Overview
This project utilizes a sample dataset from Zomato, a popular restaurant discovery and food delivery platform. To perform data analysis using SQL queries. We have 4 different data  tables for analysis By joining them as per requirments we will find out solutions.

## Requirements
1.SQL Database (e.g. Mysql Workbench)  
2.Zomato Dataset Tables (create table queries are available in above repo)  

## Database Setup:
1.Create a new database in your SQL database management system.  
2.Execute the SQL script provided in the zomato data files script.sql file to create the necessary tables and insert data from the Zomato dataset.

## Sample Queries:

-- how many days has each customer visited zomato?  
select userid,count(distinct created_date) from sale group by userid;  


-- what is the total amount each customer spent on zomato?  
SELECT s.userid,sum(p.price) as total_expenditure FROM sale
as s left join product as p on s.product_id=p.product_id
group by s.userid  order by s.userid;


## Acknowledgments
This project was inspired by the need for analyzing restaurant data for better insights.
Feel free to contribute, provide feedback, or customize the project according to your needs. Happy coding!





