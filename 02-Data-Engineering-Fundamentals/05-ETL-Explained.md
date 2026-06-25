# ETL Explained

## What is ETL?

**ETL** stands for **Extract, Transform, Load**.

It is the traditional method of moving and processing data.

---

## The Three Steps

### 1. Extract
- **Pull data** from source systems
- Sources can be: databases, APIs, files, spreadsheets
- You're just copying the raw data — no changes yet

### 2. Transform
- **Clean and reshape** the data
- Fix errors, remove duplicates, change formats
- Combine data from multiple sources
- Apply business rules

### 3. Load
- **Put the transformed data** into the destination
- Destination is usually a data warehouse (like Redshift)
- Data is now ready for analysis

---

## ETL Flow

```
[Source Database] → EXTRACT → [Staging Area] → TRANSFORM → [Clean Data] → LOAD → [Data Warehouse]
```

Important: In ETL, transformation happens **before** loading.

---

## Real Example

**Task:** Get sales data from a store's database into a data warehouse.

1. **Extract:** Pull all sales records from the store database
2. **Transform:**
   - Remove incomplete records (missing customer name)
   - Convert dates from `MM/DD/YYYY` to `YYYY-MM-DD`
   - Calculate total = quantity × price
3. **Load:** Insert clean records into Redshift

---

## AWS Service for ETL

**AWS Glue** is the main ETL service on AWS.
- It can extract from S3, RDS, DynamoDB, and more
- It transforms using Apache Spark
- It loads into S3, Redshift, databases

---

## Key Takeaway

> ETL = Extract data from sources, Transform it (clean, reshape), then Load it into a destination. Transformation happens BEFORE loading. AWS Glue is the primary ETL tool on AWS.

---

**Previous:** [What is a Data Pipeline](./04-What-is-a-Data-Pipeline.md)
**Next:** [ELT Explained](./06-ELT-Explained.md)
