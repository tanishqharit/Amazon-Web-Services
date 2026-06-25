# Schema on Write

## What is Schema on Write?

**Schema on Write** means you define the structure of data **before you store it**. Data must match the schema or it gets rejected.

---

## How It Works

1. Define a table with columns and data types
2. When you load data, it **must match** the schema
3. If data doesn't match → error / rejected

---

## Example

You create a Redshift table:
```sql
CREATE TABLE customers (
  id INT,
  name VARCHAR(100),
  age INT,
  city VARCHAR(50)
);
```

Now if you try to load `age = "twenty-five"` (text instead of number) → **it fails**.

---

## Where Schema on Write is Used

| Service | How |
|---------|-----|
| **Amazon Redshift** | Define table schema before loading |
| **Amazon RDS / Aurora** | Traditional SQL databases |
| **Data Warehouses** | Always Schema on Write |

---

## Pros and Cons

| Pros | Cons |
|------|------|
| ✅ Data quality guaranteed | ❌ Less flexible |
| ✅ Fast queries (pre-organized) | ❌ Schema changes are hard |
| ✅ No bad data in the system | ❌ Must know structure beforehand |

---

## Schema on Read vs Schema on Write

| Feature | Schema on Read | Schema on Write |
|---------|---------------|-----------------|
| When schema is defined | At read time | At write time |
| Data quality | Not guaranteed | Guaranteed |
| Flexibility | High | Low |
| Speed | Slower reads | Faster reads |
| Used by | Data Lakes (S3) | Data Warehouses (Redshift) |

---

## Key Takeaway

> Schema on Write = define structure before loading data. Data warehouses use Schema on Write. It ensures data quality but is less flexible than Schema on Read.

---

**Previous:** [Schema on Read](./08-Schema-on-Read.md)
**Next:** [Data Compression](./10-Data-Compression.md)
