# ETL vs ELT

## Quick Comparison

| Feature | ETL | ELT |
|---------|-----|-----|
| **Order** | Extract → Transform → Load | Extract → Load → Transform |
| **Where transformation happens** | In a separate tool (before loading) | Inside the destination (after loading) |
| **Raw data stored?** | No (only transformed data is stored) | Yes (raw data is always available) |
| **Speed of loading** | Slower (must transform first) | Faster (load raw data immediately) |
| **Best for** | Traditional data warehouses | Cloud data lakes and modern warehouses |
| **Flexibility** | Less (transform once) | More (transform many ways later) |
| **Cost** | Higher compute during transform | Cheaper storage, transform on-demand |

---

## When to Use ETL

- You have **strict data quality requirements** before loading
- Your destination has **limited storage** (on-premises warehouse)
- You need to **mask sensitive data** before it reaches the warehouse
- Compliance requires data to be cleaned **before** storage

---

## When to Use ELT

- You're using **cloud storage** (S3 is cheap and unlimited)
- You want to keep **raw data** for future use
- Different teams need the **same data transformed differently**
- You have **powerful destination tools** (Redshift, Athena, Spark)

---

## For the Exam

The exam often asks: "What approach should you use?"

**Tip:** In the cloud, **ELT is usually the preferred answer** because:
- Store everything in S3 (cheap)
- Transform later with Glue, Athena, or Redshift
- Keep raw data for compliance and re-processing

---

## Key Takeaway

> ETL transforms data before loading. ELT loads raw data first, then transforms. In the cloud, ELT is usually preferred because storage is cheap and you keep the raw data.

---

**Previous:** [ELT Explained](./06-ELT-Explained.md)
**Next:** [Batch Processing](./08-Batch-Processing.md)
