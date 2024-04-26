# Highest-Monthly-Paying-Customers-PostgresSQL

This project utilises the DVD dataset from PostgreSQL. This is to conduct an analysis on customer behaviors and identify this highly-valued customers. 
With this analysis report, businesses can strategize on incentive programs i.e. loyalty, membership level, priority along with sales or marketing flights.

<img width="704" alt="image" src="https://github.com/austin-vu1017/Highest-Monthly-Paying-Customers-PostgresSQL/assets/21083126/c4a7630a-9dcb-4fde-895a-0235b645b9a4">

# Report Overview
The report is created from various tables existing at different levels. Starting from 1, each layer becomes more transformed and condensed while also preserving the other tables for other usages:

1. Detailed table
  - first_name VARCHAR(50)
	- last_name VARCHAR(50)
	- customer_id SMALLINT
	- rental_id SMALLINT
	- rental_date DATE
	- rental_payment NUMERIC(5,2)
	- store_id SMALLINT
3. Summary table
  - full_name VARCHAR(100)
	- customer_id SMALLINT
	- rental_payment_rank SMALLINT
	- monthly_rental_payment NUMERIC(5,2)
	- rental_month SMALLINT
	- rental_year SMALLINT
	- store_id SMALLINT
4. Report
  - highest_paying_customer VARCHAR(100)
  - highest_rental_payments NUMERIC(5,2)
  - rental_month SMALLINT
  - rental_year SMALLINT
  - store_id SMALLINT

The report at the lowest level is created from various JOINs, custom FUNCTIONs, and Window functions to conduct transformation. 
As we scale, TRIGGERs and STORED PROCEDUREs are set up to refresh the data on a monthly cadence. 
