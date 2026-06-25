# Glue ETL Jobs Overview

## What is a Glue ETL Job?

A **Glue ETL Job** is a piece of code that reads data from a source, transforms it, and writes it to a destination. AWS Glue runs this code on serverless infrastructure.

---

## Three Types of Glue Jobs

| Job Type | Engine | Best For |
|----------|--------|----------|
| **Spark** | Apache Spark | Large-scale data processing |
| **Python Shell** | Plain Python | Small tasks, simple scripts |
| **Ray** | Ray framework | ML workloads, distributed Python |

---

## Spark Jobs (Most Important)

- Uses **Apache Spark** (distributed computing engine)
- Written in **PySpark** (Python) or **Scala**
- Can process **terabytes** of data
- Supports DynamicFrames and DataFrames
- **This is what the exam focuses on**

## Python Shell Jobs

- Runs plain Python (no Spark)
- Limited to **1 DPU** (small scale)
- Good for: API calls, small file processing, notifications
- Cheaper than Spark jobs

## Ray Jobs

- Uses **Ray** framework for distributed Python
- Good for ML preprocessing and parallelized Python
- Newer, less common on the exam

---

## How a Glue Spark Job Works

```python
# 1. Read data from source
datasource = glueContext.create_dynamic_frame.from_catalog(
    database="sales_db", table_name="raw_orders"
)

# 2. Transform data
transformed = datasource.drop_fields(["temp_column"])

# 3. Write data to destination
glueContext.write_dynamic_frame.from_options(
    frame=transformed,
    connection_type="s3",
    connection_options={"path": "s3://bucket/processed/"},
    format="parquet"
)
```

---

## Key Takeaway

> Glue ETL Jobs transform data at scale. Spark jobs are the most important (exam-focused). Python Shell is for small tasks. Jobs read from sources, transform, and write to destinations.

---

**Previous:** [Glue Databases and Tables](./04-Glue-Databases-and-Tables.md)
**Next:** [Glue Spark Jobs](./06-Glue-Spark-Jobs.md)
