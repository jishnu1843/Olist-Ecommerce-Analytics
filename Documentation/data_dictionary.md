# Data Dictionary — Olist E-Commerce Analytics

## Overview

This project uses the Brazilian E-Commerce Public Dataset by Olist to analyze orders, customers, products, payments, sellers, and customer reviews.

## Dataset Tables

| Table                | Description                                          | Example Analysis                            |
| -------------------- | ---------------------------------------------------- | ------------------------------------------- |
| Customers            | Customer identifiers and location information        | Customer distribution and repeat purchasing |
| Orders               | Order status and purchase and delivery timestamps    | Order volume and delivery performance       |
| Order Items          | Products purchased, prices, freight charges, sellers | Sales and shipping analysis                 |
| Products             | Product identifiers and product attributes           | Category performance                        |
| Payments             | Payment methods, values, and installments            | Payment behavior                            |
| Reviews              | Customer review scores and comments                  | Customer satisfaction                       |
| Sellers              | Seller identifiers and location information          | Seller performance                          |
| Geolocation          | Geographic coordinates associated with postal codes  | Geographic analysis                         |
| Category Translation | Portuguese-to-English product category mappings      | Readable category reporting                 |

## Important Fields

### Customers

* `customer_id`: Identifier associated with an order's customer record.
* `customer_unique_id`: Identifier used to recognize the same customer across multiple customer records.
* `customer_city`: Customer's city.
* `customer_state`: Customer's state.

### Orders

* `order_id`: Unique order identifier.
* `customer_id`: Customer record associated with the order.
* `order_status`: Current recorded order status.
* `order_purchase_timestamp`: Date and time of purchase.
* `order_delivered_customer_date`: Recorded customer delivery date.
* `order_estimated_delivery_date`: Estimated delivery date.

### Order Items

* `order_id`: Associated order.
* `product_id`: Purchased product.
* `seller_id`: Seller associated with the item.
* `price`: Item price.
* `freight_value`: Freight charge associated with the item.

### Products

* `product_id`: Product identifier.
* `product_category_name`: Product category in Portuguese.
* `product_weight_g`: Product weight in grams.

### Payments

* `order_id`: Associated order.
* `payment_type`: Payment method.
* `payment_value`: Recorded payment amount.
* `payment_installments`: Number of installments.

### Reviews

* `review_id`: Review identifier.
* `order_id`: Associated order.
* `review_score`: Customer rating.
* `review_comment_title`: Review title.
* `review_comment_message`: Review text.

### Sellers

* `seller_id`: Seller identifier.
* `seller_city`: Seller's city.
* `seller_state`: Seller's state.

## Data Quality Considerations

* Some orders have missing delivery timestamps.
* Review titles and messages may be missing.
* Geolocation data may contain duplicate records.
* Multiple payment records can exist for one order.
* Customer records and unique customer identifiers represent different concepts.

## Dataset Source

Brazilian E-Commerce Public Dataset by Olist:

https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

## Note

This dictionary describes the principal fields used in the project. Confirm column names and data types against the actual source files and database schema before finalizing the documentation.
