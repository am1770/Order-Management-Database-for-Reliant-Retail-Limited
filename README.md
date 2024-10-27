# Order-Management-Database-for-Reliant-Retail-Limited
## Project Overview
This project is designed to analyze and optimize data management for "Reliant Retail Limited," an online retail store. Using SQL, the project addresses queries related to customer information, product inventory, shipping, and order details within an order management database. The solutions provided aim to assist in data-driven decision-making for various business scenarios.

## Database Schema
The project operates on an order management schema that includes tables for:

**Customers:** Stores customer details such as name, email, and country.
**Products:** Contains product descriptions, class, pricing, and inventory details.
**Orders:** Manages order placements, statuses, and payment methods.
**Shippers:** Tracks shipment details, including city and shipping partner.
**Cartons:** Maintains carton dimensions for shipping purposes.

## Project Requirements and Solutions
### 1. Customer Categorization by Creation Date
Displays customer name, email, and categorizes customers based on their account creation year:
Category A: Created before 2005
Category B: Created between 2005 and 2011
Category C: Created in 2011 or later

Used the CASE statement to create a conditional categorization based on the year of the customer creation date. Concatenated first and last names with a title and formatted them in uppercase using string functions for display.

### 2. Unsold Products Inventory Value and Discount Calculation

For unsold products, calculate inventory values and discounts based on product prices:
Products > 200,000: 20% discount
Products > 100,000: 15% discount
Products ≤ 100,000: 10% discount

Implemented CASE logic to apply the appropriate discount based on product price. Calculated inventory value as product_quantity_avail * product_price and sorted results by descending inventory value for prioritization.

### 3. Product Class Inventory Analysis
Displays product class code, description, count, and inventory value for classes with inventory values exceeding 100,000.

Used GROUP BY to aggregate products by class and calculated the total inventory value using the sum of product_quantity_avail * product_price. Applied a HAVING clause to filter classes with inventory values over the specified threshold.
 
### 4. Customers with Cancelled Orders
Lists customers who have cancelled all their orders, including customer ID, full name, email, phone number, and country.

Used a SUBQUERY to filter for customers who cancelled all of their orders and displayed customer details, including ID, full name, email, phone, and country.

### 5. Shipper Details for DHL
Displays DHL shipper data, including the city serviced, customer count per city, and consignment count.

Joined multiple tables to identify DHL shipments by city, then grouped and counted unique customers and consignments for each city served by DHL.

### 6. Inventory Status by Category
Provides inventory status for each product category with recommendations on inventory levels based on sold quantity, helping to optimize inventory management.

Built a CASE statement with sub-categorization based on the product category. Each condition adjusted the status based on the percentage of inventory remaining compared to the quantity sold. This method identifies items needing restocking or discounting to reduce inventory.
 
### 7. Biggest Order Volume for Carton Fit
Identifies the largest order (in volume) that can fit within a specific carton ID.

Calculated the volume of each product in the order based on dimensions. Using aggregation and filtering, identified the largest fitting order for the given carton.

### 8. Cash Payment Orders for Specific Customers
Displays customer and order details for cash payments where the customer's last name starts with 'G.'

Filtered orders by payment mode (Cash) and used string functions to match customers with last names starting with 'G.' Calculated total quantity and order value (quantity * price) for these records.

### 9. Co-Purchased Products Excluding Certain Cities
Lists of products sold with product ID 201, excluding shipments to Bangalore and New Delhi.

Used a SUBQUERY to filter out orders shipped to specific cities. Joined tables to find products sold with product ID 201 and displayed them in descending order of total quantity sold.

### 10. Even-Numbered Order Details by Specific Address Pincode
Shows details of even-numbered orders shipped to addresses with pin codes not starting with '5.'

Filtered orders by even order IDs and used a NOT LIKE '5%' condition to exclude specific pincode patterns. Displayed order details, customer ID, and full name for these criteria.

### Technologies Used
MySQL: For database management and SQL query execution.
SQL: To perform data retrieval, manipulation, and analysis.
