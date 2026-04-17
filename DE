# 📊 Data Engineering Assignment – Multi-Source Data Pipeline

## 🧩 Problem Statement

The objective is to build a scalable data pipeline that ingests data from multiple vendor sources with different formats and schemas, cleans and standardizes the data, and produces a unified dataset for analytics.

---

## 🚀 Solution Overview

I implemented a PySpark-based data pipeline that processes data from multiple sources (CSV, JSON, Parquet), standardizes schema differences, performs data cleaning and validation, and generates a final aggregated dataset.

---

## 🏗️ Pipeline Architecture

The pipeline consists of three main stages:

### 1. Ingestion Layer

* Reads data from multiple vendors
* Supports different file formats
* Adds a `data_source` column to track origin

### 2. Processing Layer

* Standardizes column names (e.g., product_id)
* Handles missing values
* Performs data type conversions
* Removes duplicates
* Applies validation rules

### 3. Output Layer

* Aggregates data at a daily level
* Stores output in CSV/Parquet format
* Uses partitioning for better performance

---

## 📊 Final Output Schema

| Column Name   | Description               |
| ------------- | ------------------------- |
| date          | Transaction date          |
| product_id    | Unique product identifier |
| total_units   | Total units sold          |
| total_revenue | Total revenue generated   |
| data_source   | Source of the data        |

---

## ⚙️ Key Features

* Handles multiple data formats (CSV, JSON, Parquet)
* Dynamic schema handling using `unionByName`
* Data cleaning and validation
* Duplicate removal
* Partitioned output for performance
* Scalable and extensible design

---

## ⚠️ Assumptions

* Input data contains product, date, units, and revenue information
* Vendor schemas may differ but represent similar data
* Missing numeric values are replaced with default values

---

## 🔍 Challenges & Solutions

### Schema Differences

Handled using column standardization and `unionByName`

### Missing Data

Used `fillna()' to ensure data completeness

### Data Quality

Applied filters to remove invalid records

---

## 📦 Output

* Sample output is available in:

```output/sample_output.parquet
```

## 🚀 Future Enhancements

* Implement Delta Lake for ACID transactions
* Add incremental loading (watermark-based)
* Integrate Azure Data Factory for orchestration
* Add monitoring and logging

## ✅ Conclusion

This solution demonstrates a scalable and production-ready approach to handling multi-source data ingestion, transformation, and aggregation using PySpark.
