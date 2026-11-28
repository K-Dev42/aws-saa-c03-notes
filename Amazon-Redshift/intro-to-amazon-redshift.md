## Definition
Amazon Redshift is a fully managed Petabyte-size Data Warehouse.

The main purpose here is to analyze (Run complex SQL queries) on massive amounts of data 

Amazon RedShift is a Columnar Store database 

What is Database Transaction?
A transaction symbolizes a unit of work performed within a database management system eg. reads and writes

### Database
Online Transaction Processing (OLTP)
OLTP systems are optimized for executing large numbers of relatively small, fast transactions 

A database was built to store current transactions and enable fast access to specific transactions for ongoing business processes

Adding items to your shopping list: single source

Short transactions (small and simple queries) with an emphasis on writes

### Data Warehouse
Online Analytical Processing (OLAP)
OLAP systems are designed for complex queries that analyze large volumes of data to identify patterns, trends, and insights

A data warehouse is built to store large quantities of historical data and enable fast, complex queries across all the data

Generating reports: multiple sources

Long transactions (long and complex queries) with an emphasis on reads

### More about RedShift
Pricing starts at just $0.25 per hour with no upfront costs or commitments

Scale up to petabytes for $1000 per terabyte, per year

> RedShift's price is less than 1/10 cost of most similar services

RedShift is used for Business Intelligence
Redshift uses OLAP
Redshift is Columnar Storage Database

Columnar storage for database tables in an important factor in optimizing analytic query performance because ut drastically reduces the overall disk I/O requirements and reduces the amount of data you need to load from disk