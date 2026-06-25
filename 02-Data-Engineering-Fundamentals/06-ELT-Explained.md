# ELT Explained

## What is ELT?

**ELT** stands for **Extract, Load, Transform**.

It is the modern approach — load the raw data first, then transform it inside the destination.

---

## The Three Steps

### 1. Extract
- Pull raw data from sources (same as ETL)

### 2. Load
- Put the **raw, untransformed data** directly into the destination
- Usually a data lake (S3) or a powerful data warehouse (Redshift)

### 3. Transform
- Transform the data **inside** the destination
- Use SQL or tools like Athena, Redshift, or Spark

---

## ELT Flow

```
[Source] → EXTRACT → LOAD (raw data) → [Data Lake/Warehouse] → TRANSFORM (inside)
```

Important: In ELT, the data is loaded **first**, then transformed where it's stored.

---

## Why ELT is Popular Now

1. **Cloud storage is cheap** — you can store all raw data in S3 cheaply
2. **Processing power is cheap** — tools like Athena and Redshift can transform at scale
3. **Flexibility** — keep raw data, transform it differently for different use cases
4. **Speed** — no waiting for transformation before loading

---

## AWS Services for ELT

| Step | AWS Service |
|------|------------|
| Extract | DMS, Kinesis, AppFlow |
| Load | S3 (raw zone) |
| Transform | Athena, Redshift, Glue |

---

## Key Takeaway

> ELT = Extract data, Load it raw into the destination, then Transform it there. ELT is popular in the cloud because storage is cheap and modern tools can transform data at massive scale.

---

**Previous:** [ETL Explained](./05-ETL-Explained.md)
**Next:** [ETL vs ELT](./07-ETL-vs-ELT.md)
