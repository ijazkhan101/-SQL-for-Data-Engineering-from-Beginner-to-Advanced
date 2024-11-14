 SQL for Data Engineering: from Beginner to Advanced

 create table categories(
category_id serial primary key,
name varchar(100)
)

create table Products(
product_id SERIAL Primary key,
name Varchar(100),
price DECIMAL(10,2),
description varchar(255),
tags Varchar(255),
category_id INT,
FOREIGN KEY (category_id) REFERENCES categories(category_id),
supplier VARCHAR(100)
)

create table Customer(
customer_id SERIAL Primary key,
customer_name VARCHAR(100) NOT Null ,
email VARCHAR(100) Not Null,
phone_number VARCHAR(29),
address VARCHAR(255),
City VARCHAR(255)
);

Create Table Orders (
order_id SERIAL Primary Key,
customer_id INT,
product_id INT,
Total_quantity INT,
Total_amount DECIMAL(10,2),
order_rating DECIMAL(3,1),
length DECIMAL(5,2),
width DECIMAL(5,2),
order_timestamp TIMESTAMP,
delivery_timestamp TIMESTAMP,
FOREIGN KEY (customer_id) REFERENCES Customer(category_id),
FOREIGN KEY (product_id) REFERENCES Products(product_id)
);

INSERT into Categories (name) Values ('Electronices'),('Clothing'),('Home and Kitchen')