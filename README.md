🍕 Pizza Sales — SQL Data Analyst Portfolio Project

This is a complete, real-world SQL portfolio project based on a pizza sales database.
The project simulates how data analysts work with transactional sales data to extract business insights around orders, revenue, customer behavior, and product performance.

This project focuses on practical SQL analysis, not just basic queries.


🎯 Who This Project Is For

This project is ideal for:

📊 Data Analyst aspirants building portfolio projects for interviews & LinkedIn

📚 SQL learners looking for hands-on practice with real datasets

💼 Candidates preparing for retail, food delivery, or sales analytics roles

📈 Anyone wanting to understand sales & revenue analysis using SQL



📌 Project Overview

The goal of this project is to simulate how data analysts analyze pizza sales data to:

✅ Design and manage a relational sales database

✅ Perform Exploratory Data Analysis (EDA)

✅ Analyze order trends and peak hours

✅ Calculate revenue and cumulative sales

✅ Identify top-selling and top-earning pizzas

✅ Generate business-driven insights using SQL



📁 Dataset Overview

The dataset represents a pizza restaurant sales system.
It includes information about orders, pizzas, pizza types, prices, and quantities.


🧾 Key Tables:

orders

order_id: Unique order identifier

order_date: Date of the order

order_time: Time of the order

order_details

order_details_id: Unique row identifier

order_id: Reference to orders table

pizza_id: Ordered pizza

quantity: Number of pizzas ordered

pizzas

pizza_id: Unique pizza identifier

pizza_type_id: Type of pizza

size: Pizza size (S, M, L, XL)

price: Price of the pizza

pizza_types

pizza_type_id: Unique pizza type

name: Pizza name

category: Category (Classic, Veggie, Chicken, Supreme)


🔧 Project Workflow


1️⃣ Database & Table Creation

We begin by creating structured tables with proper relationships:

		CREATE TABLE orders (
		    order_id INT PRIMARY KEY,
		    order_date DATE,
		    order_time TIME
		);
		
		CREATE TABLE pizza_types (
		    pizza_type_id VARCHAR(50) PRIMARY KEY,
		    name VARCHAR(100),
		    category VARCHAR(50)
		);
		
		CREATE TABLE pizzas (
		    pizza_id VARCHAR(50) PRIMARY KEY,
		    pizza_type_id VARCHAR(50),
		    size VARCHAR(5),
		    price DECIMAL(10,2)
		);
		
		CREATE TABLE order_details (
		    order_details_id INT PRIMARY KEY,
		    order_id INT,
		    pizza_id VARCHAR(50),
		    quantity INT
		);



2️⃣ Data Import

Imported CSV files into MySQL

Verified data consistency and relationships


3️⃣ 🔍 Exploratory Data Analysis (EDA)

Counted total orders placed

Identified unique pizza categories and sizes

Checked daily and hourly order distribution

Analyzed most frequently ordered pizzas

Compared sales volume across categories


4️⃣ 🧹 Data Cleaning

Checked for null or invalid values

Ensured price and quantity fields were valid

Verified foreign key relationships

Standardized date and time formats


5️⃣ 📊 Business-Driven SQL Analysis

Key insights derived using SQL include:

🍕 Top 5 most ordered pizzas

💰 Top 3 pizzas by total revenue

📦 Category-wise pizza sales

⏰ Peak order hours during the day

📅 Average number of pizzas ordered per day

📈 Cumulative revenue over time

🥇 Top 3 pizzas by revenue within each category

📊 Revenue contribution percentage by category


🛠️ How to Use This Project


1️⃣ Clone the repository

		https://github.com/ShakilHossen537/pizza-sales-sql-project.git



2️⃣ Open the SQL file

Contains table creation

EDA queries

Business analysis queries


3️⃣ Run the project

Create a database in MySQL

Execute SQL scripts step by step



4️⃣ Modify queries

Add filters

Change time ranges

Create your own insights





💡 Thanks for checking out the project! Your support means a lot — feel free to star ⭐ this repo or share it with someone learning SQL.🚀
