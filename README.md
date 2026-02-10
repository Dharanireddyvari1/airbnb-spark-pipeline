# Airbnb Spark Pipeline

An end-to-end batch data pipeline built using PySpark to process Airbnb listings and reviews data.

## Overview
This project ingests Airbnb listings and reviews datasets, performs data cleaning, joins, aggregations, and derives multiple analytical outputs such as:
- Reviews per listing
- Average price by neighborhood and room type
- Host-level listing counts
- Availability distribution
- Weekend vs weekday review activity
- Sentiment analysis on review text
- Basic data quality metrics

The pipeline is implemented as a single modular PySpark script, designed for batch execution and easy extension to orchestration tools like Airflow.

## Tech Stack
- Python
- Apache Spark (PySpark)
- Spark SQL
- UDFs & Broadcast Variables

## Input Data
- listings.csv.gz
- reviews.csv.gz  
(Data sourced from Inside Airbnb)

## How to Run
```bash
spark-submit airbnb_spark_pipeline.py \
  --listings /data/listings.csv.gz \
  --reviews  /data/reviews.csv.gz \
  --output   /data/output
