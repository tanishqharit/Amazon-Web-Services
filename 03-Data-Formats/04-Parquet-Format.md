# Parquet Format

## What is Parquet?

**Apache Parquet** is a **columnar storage format** designed for efficient analytics. It is the **#1 recommended format** for data lakes on AWS.

---

## How Columnar Storage Works

Row-based (CSV): Stores data row by row
```
Tanishq, 25, Delhi
Priya, 30, Mumbai
Rahul, 28, Kolkata
```

Columnar (Parquet): Stores data column by column
```
Names:  [Tanishq, Priya, Rahul]
Ages:   [25, 30, 28]
Cities: [Delhi, Mumbai, Kolkata]
```

When you query `SELECT AVG(age)`, Parquet only reads the "Ages" column — not the entire file!

---

## Characteristics

| Feature | Parquet |
|---------|---------|
| **Type** | Binary, columnar |
| **Human-readable** | ❌ No (binary) |
| **Compression** | ✅ Built-in (Snappy, GZIP, Zstd) |
| **Schema** | ✅ Embedded in the file |
| **Supports nesting** | ✅ Yes |
| **File size** | Very small (compressed + columnar) |
| **Query speed** | Very fast for analytics |

---

## Why Parquet is the Best for AWS Data Engineering

1. **Faster queries** — only reads needed columns
2. **Smaller files** — built-in compression (up to 75% smaller than CSV)
3. **Lower cost** — Athena charges per TB scanned (less data = less cost)
4. **Schema included** — schema is stored in the file itself
5. **AWS native** — S3, Athena, Glue, Redshift Spectrum all love Parquet

---

## For the Exam

Whenever the exam asks about:
- "Most cost-effective format for Athena" → **Parquet**
- "Reduce data scanned" → **Parquet + partitioning**
- "Optimize S3 storage" → **Parquet with Snappy compression**

---

## Key Takeaway

> Parquet is THE format for data lakes on AWS. It's columnar, compressed, and includes schema. Always convert CSV/JSON to Parquet for analytics.

---

**Previous:** [JSON Format](./03-JSON-Format.md)
**Next:** [ORC Format](./05-ORC-Format.md)
