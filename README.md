# Data-Warehouse-Design-Project
## Project Overview 
Welcome to my Data Warehouse Design Project, where I’m building a data warehouse from the ground up for a large pizza store franchise! The goal is to create a powerful, scalable data warehouse solution to help the franchise analyze its sales, streamline operations, and uncover delicious insights.
## Dataset 
The dataset comes from Maven Analytics and is based on the Pizza Place Sales data. It contains four CSV files, providing everything needed for an end-to-end data warehousing process:
Orders: Contains order IDs, dates, and customer information.
Order Details: Breaks down each order into individual items and quantities.
Pizza Types: Provides information on the types of pizzas, including size and category.
Pizza: Links pizzas to their corresponding details and prices.
### Analyse the Input Data
I carefully analyzed the input data, ensuring it’s clean, consistent, and ready for transformation.
Using the data dictionary provided i was able to identify key relationship links between the datasets to be able to design a data warehouse schema.
### Key Relationship 
The order details table connects to the orders tables using order_id and links to the pizzas table using pizza_id.
### Dimension Modelling 
While mapping the relationships,I observed that the datasets are structured similarly to an OLTP (Online Transaction Processing) database.While this structure works for day-to-day operations, it’s not optimized for analytical queries.

![Alt Text](https://github.com/CynthiaKiplagat/Data-Warehouse-Design-Project/blob/main/Existing%20Model%20in%20CSV%20.PNG)

For this project, I streamlined the data structure to enhance simplicity and usability:
•	I merged the Order and Order Details tables into a single table called Orders, making it easier to track and analyze order-level information.
•	Similarly, I combined the Pizza and Pizza Types tables into a unified table named Products, providing a consolidated view of all product-related details.
•	To enable time-based analysis and store-level insights, I introduced two additional dimensions: Date, time and Store.
•	Finally, I created a fact table called Sales, which includes key metrics like quantity and price, along with foreign key links to the dimension tables (Orders, Products, Date, and Store).

![Alt Text](https://github.com/CynthiaKiplagat/Data-Warehouse-Design-Project/blob/main/Dimension%20Modelling.drawio.png)

This design ensures an efficient, scalable, and analytics-ready data warehouse structure, optimized for extracting actionable business insights.
### Staging Tables 
After creating the dimensional tables, i moved on to setting up the staging tables that will load our data into the MySQL database. I have already created a database called sch_pizza_stg which contains four tables: order_details, orders, pizza, and pizza_types. I have successfully created and loaded the corresponding data from four CSV files into these MySQL tables.

![Alt Text](https://github.com/CynthiaKiplagat/Data-Warehouse-Design-Project/blob/main/Order%20Details.PNG)

(![image](https://github.com/user-attachments/assets/e7d74f7b-9338-4fbf-8fe0-10bc2c04c673)









