# Melbourne-Delivery
The aim of this project is to clean the data and prepare it for business analysis.


# About The Dataset

- The dataset contains Food Delivery data from a restaurant in Melbourne, Australia. ​The restaurant has three branches around the CBD area. All three branches share the same menu but they have different management so they operate differently.

## Data Dictionary:

- `order_id` - A unique id for each order.
- `date` - The date the order was made, given in YYYY-MM-DD format.
- `time` - The time the order was made, given in hh:mm:ss format.
- `order_type` - A categorical attribute representing the different types of orders namely: Breakfast, Lunch or Dinner.
- `branch_code` - A categorical attribute representing the branch code inwhich the order was made. Branch information is given in the `​branches.csv` file.
- `order_items` - A list of tuples representing the order items: first element of the tuple is the item ordered, and the second element is the quantity ordered for such item.
- `order_price` - A float value representing the order total price.
- `customer_lat` - Latitude of the customer coming from the `​nodes.csv` ​ file.
- `customer_lon` - Longitude of the customer coming from the `​nodes.csv`file.
- ` customerHasloyalty?` - A logical variable denoting whether the customer has a loyalty card with the restaurant (1 if the customer has loyalty and 0 otherwise).
- `distance_to_customer_KM` - A float representing the shortest distance, in kilometers, between the branch and the customer nodes with respect to the ​nodes.csv​ and the `​edges.csv` ​ files.

​Dijkstra algorithm ​ can be used to find the shortest path between two nodes in a graph.


- `delivery_fee` - A float representing the delivery fee of the order.



## Project Goals 

- Write a python script to transform the data into a usable format for a BI Analyst.

    -  The transformation can generate more than one table if needed.

- Analyze the data.

    -  Highlight critical errors that need to be corrected before the BI analyst can make use of the data.



## Understanding the Data

Based on this information above:

- The dataset has 500 rows and 12 columns.
- The dataset has 0 null values.


Data transformations and cleaning tasks that might be needed include:

- Checking the data type of all columns to make sure they are in the appropriate format for analysis.
- The `order_id`, `date`, `time`, `order_type`, `branch_code`, `order_items` columns datatypes need to be changed.
- The `date` &  `time` need to be merged into a single column, renamed to `order_date` and converted to `datetime` dtype format for Parsing Dates.
- Extracting the food items and their quantities from the `order_items` column into separate columns.
- Checking the category column entries for case sensitivity (Checking if the values in the branch_code and order_type columns are consistent and correctly labeled.)
- feature engineer the `order_date`  column, potentially separating them into year, month, day, and hour columns.
- Removing any unnecessary or irrelevant columns.
- Checking for outliers in numerical columns such as order_price, distance_to_customer_KM, and delivery_fee.
- Checking if the customerHasloyalty? column only contains binary values (0 and 1).
- Checking if the  `distance_to_customer_KM` column is consistent with the values in the `nodes.csv` file.
- Checking if the `delivery_fee` column is consistent with the values in the `edges.csv`  file.
- Checking if the `order_price` column is consistent with the values in the `order_items`  column.
- Checking if the `order_price` column is consistent with the values in the  `delivery_fee` column.


Remember, the goal of this process is to ensure that your dataset is clean, understandable, and ready for further Business Intelligence analysis.

