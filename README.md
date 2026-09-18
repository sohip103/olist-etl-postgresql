# Olist E-Commerce ETL Pipeline — PostgreSQL

End-to-end ETL project: designing and building a normalized relational database
from a real-world e-commerce dataset, using PostgreSQL and pgAdmin.

## Dataset
[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
— ~100,000 real orders (2016–2018) across 9 CSV files.

## What this project covers
- Designing a 9-table relational schema from raw CSV files
- Primary keys (simple and composite) and foreign key relationships
- Choosing appropriate data types based on real data (VARCHAR, DECIMAL, TIMESTAMP, SERIAL)
- Importing and validating over 1,000,000+ rows of raw data
- Diagnosing and fixing real import errors (numeric precision overflow, column misalignment)

## Schema Overview

customers ──< orders >──┬── order_items ──── products ──── product_category_translation
                        ├── order_payments
                        └── order_reviews

sellers ──< order_items
geolocation (standalone — zip code to lat/lng lookup, own surrogate key)

## Tools
PostgreSQL 17 · pgAdmin 4

## Files
- `schema.sql` — full DDL for all 9 tables
