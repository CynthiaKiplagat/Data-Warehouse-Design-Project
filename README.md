# Data-Warehouse-Design-Project
## Project Overview 
Welcome to my Data Warehouse Design Project, where I’m building a data warehouse from the ground up for a large pizza store franchise! The goal is to create a powerful, scalable data warehouse solution to help the franchise analyze its sales, streamline operations, and uncover delicious insights.
## Dataset 
The dataset comes from Maven Analytics and is based on the Pizza Place Sales data. It contains four CSV files, providing everything needed for an end-to-end data warehousing process:
Orders: Contains order IDs, dates, and customer information.
Order Details: Breaks down each order into individual items and quantities.
Pizza Types: Provides information on the types of pizzas, including size and category.
Pizzas: Links pizzas to their corresponding details and prices.
### Analyse the Input Data
I carefully analyzed the input data, ensuring it’s clean, consistent, and ready for transformation.
Using the data dictionary provided i was able to identify key relationship links between the datasets to be able to design a data warehouse schema.
### Key Relationship 
The order details table connects to the orders tables using order_id and links to the pizzas table using pizza_id.
### Dimension Modelling 
While mapping the relaationships,I observed that the datasets are structured similarly to an OLTP (Online Transaction Processing) database. While this structure works for day-to-day operations, it’s not optimized for analytical queries.

![Alt Text](https://github.com/CynthiaKiplagat/Data-Warehouse-Design-Project/blob/main/Existing%20Model%20in%20CSV%20.PNG)






