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

### 2. Unsold Products Inventory Value and Discount Calculation

For unsold products, calculates inventory values and discounts based on product prices:
Products > 200,000: 20% discount
Products > 100,000: 15% discount
Products ≤ 100,000: 10% discount

### 3. Product Class Inventory Analysis
Displays product class code, description, count, and inventory value for classes with inventory values exceeding 100,000.

### 4. Customers with Cancelled Orders
Lists customers who have cancelled all their orders, including customer ID, full name, email, phone number, and country.

### 5. Shipper Details for DHL
Displays DHL shipper data, including the city serviced, customer count per city, and consignment count.

### 6. Inventory Status by Category
Provides inventory status for each product category with recommendations on inventory levels based on sold quantity, helping to optimize inventory management.

### 7. Biggest Order Volume for Carton Fit
Identifies the largest order (in volume) that can fit within a specific carton ID.

### 8. Cash Payment Orders for Specific Customers
Displays customer and order details for cash payments where the customer's last name starts with 'G.'

### 9. Co-Purchased Products Excluding Certain Cities
Lists products sold with product ID 201, excluding shipments to Bangalore and New Delhi.

### 10. Even-Numbered Order Details by Specific Address Pincode
Shows details of even-numbered orders shipped to addresses with pincodes not starting with '5.'

### Technologies Used
MySQL: For database management and SQL query execution.
SQL: To perform data retrieval, manipulation, and analysis.
