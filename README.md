# End-to-End Data Engineering Project using Databricks (FMCG Domain)

## Overview

This project demonstrates an end-to-end Data Engineering pipeline built using Databricks Free Edition following the Medallion Architecture (Bronze, Silver, Gold). The project simulates a real-world FMCG business scenario where data from multiple sources is ingested, transformed, and prepared for analytics.

The pipeline covers data ingestion, data cleaning, transformation, Delta Lake implementation, and dashboard creation using Databricks.

---

## Business Problem

A large FMCG company has acquired another business whose data exists in multiple formats such as CSV files and spreadsheets. The goal is to integrate these datasets into a centralized analytics platform that enables reliable business reporting and decision-making.

---

## Architecture

```
                Source Files
                      │
                      ▼
                 AWS S3 Storage
                      │
                      ▼
             Databricks Unity Catalog
                      │
        ┌─────────────┼─────────────┐
        ▼             ▼             ▼
     Bronze Layer  Silver Layer  Gold Layer
   (Raw Data)    (Cleaned Data) (Business Tables)
                      │
                      ▼
          Databricks SQL Dashboard
```

---

## Tech Stack

- Databricks Free Edition
- Apache Spark
- PySpark
- SQL
- Delta Lake
- Unity Catalog
- AWS S3
- Databricks Workflows
- Databricks SQL
- Databricks Dashboard

---

## Project Structure

```
data_engineering_project/
│
├── notebooks/
│   ├── setup
│   ├── bronze
│   ├── silver
│   ├── gold
│   └── dashboard
│
├── datasets/
│
├── sql/
│
├── screenshots/
│
├── architecture/
│
└── README.md
```

---

## Medallion Architecture

### Bronze Layer

- Load raw CSV files from AWS S3
- Preserve original data
- Add metadata columns
- Store as Delta Tables

---

### Silver Layer

- Remove duplicates
- Handle null values
- Standardize formats
- Clean customer and product data
- Apply business rules

---

### Gold Layer

- Create analytical tables
- Aggregate sales metrics
- Build reporting datasets
- Optimize for dashboards

---

## Data Pipeline

1. Upload source files to AWS S3
2. Read files into Databricks
3. Load raw data into Bronze tables
4. Clean and transform into Silver tables
5. Build business-ready Gold tables
6. Create SQL dashboards for analytics

---

## Features

- End-to-End ETL Pipeline
- Medallion Architecture
- Delta Lake
- Data Cleaning
- Data Transformation
- SQL Analytics
- Dashboard Reporting
- Cloud Storage Integration
- Unity Catalog

---

## Sample Business KPIs

- Total Sales
- Monthly Revenue
- Product Performance
- Customer Growth
- Regional Sales
- Category-wise Revenue

---

## Learning Outcomes

- Building scalable ETL pipelines
- Working with Databricks Free Edition
- Implementing Medallion Architecture
- Using Delta Tables
- Data Engineering best practices
- SQL Analytics
- Dashboard Development

---

## Future Improvements

- Incremental Data Loading
- Auto Loader
- Streaming Pipelines
- Workflow Scheduling
- CI/CD Integration
- Data Quality Checks
- Monitoring and Logging

---

## Author

**Mrunal Raskar**

GitHub: https://github.com/mgraskar1807-jpg

---

## Acknowledgements

This project is inspired by the Codebasics End-to-End Data Engineering Project using Databricks Free Edition tutorial. The implementation is recreated for learning purposes and to demonstrate practical data engineering concepts.
