# What is a Data Pipeline?

## Simple Explanation

A **data pipeline** is an automated process that moves data from one place to another, usually with some transformation along the way.

Think of it like a factory assembly line:
1. Raw materials come in (raw data)
2. Workers process them (transformations)
3. Finished products come out (clean, usable data)

---

## Stages of a Data Pipeline

```
Source → Ingest → Transform → Store → Serve
```

| Stage | What happens | Example |
|-------|-------------|---------|
| **Source** | Where data comes from | App database, API, logs |
| **Ingest** | Collecting the data | Kinesis streams, S3 upload |
| **Transform** | Cleaning and shaping | Glue ETL job |
| **Store** | Saving the result | S3, Redshift |
| **Serve** | Making it available | Athena queries, dashboards |

---

## Example Pipeline on AWS

```
Mobile App → Kinesis Data Streams → Glue ETL → S3 (Parquet) → Athena → QuickSight Dashboard
```

1. Users interact with a mobile app
2. Events stream into Kinesis in real-time
3. Glue cleans and transforms the data
4. Clean data is stored in S3 in Parquet format
5. Analysts query it with Athena
6. Results are shown in a QuickSight dashboard

---

## Why Pipelines Need to Be Automated

- Data arrives **continuously** (every second, minute, hour)
- Manual processing is **too slow and error-prone**
- Automation ensures **consistency and reliability**

---

## Key Takeaway

> A data pipeline automates the flow of data from source to destination. It follows the pattern: Source → Ingest → Transform → Store → Serve. This is the core of data engineering.

---

**Previous:** [Role of a Data Engineer](./03-Role-of-a-Data-Engineer.md)
**Next:** [ETL Explained](./05-ETL-Explained.md)
