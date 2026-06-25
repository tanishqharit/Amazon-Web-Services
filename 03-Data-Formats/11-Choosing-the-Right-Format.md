# Choosing the Right Format

## Decision Guide

Use this table when the exam asks "which format should you use?"

---

## By Use Case

| Use Case | Best Format | Why |
|----------|-------------|-----|
| **Analytics on S3 (Athena)** | Parquet | Columnar, fast, cheap |
| **Data warehouse (Redshift)** | Parquet or ORC | Columnar, compressed |
| **Streaming data (Kinesis)** | JSON or Avro | Row-based, fast writes |
| **Schema changes often** | Avro | Schema evolution support |
| **Quick data exchange** | CSV | Simple, universal |
| **API responses** | JSON | Semi-structured, flexible |
| **Hive on EMR** | ORC or Parquet | Both work, ORC is native |
| **Data lake storage** | Parquet + Snappy | Best balance of size + speed |

---

## Exam Keyword Triggers

| Exam says... | Choose... |
|-------------|-----------|
| "Reduce cost" | Parquet (less data scanned) |
| "Improve query performance" | Parquet + partitioning |
| "Schema evolution" | Avro |
| "Streaming ingestion" | JSON or Avro |
| "Convert for analytics" | CSV/JSON → Parquet |
| "Columnar format" | Parquet or ORC |

---

## The Golden Rule

```
Raw data comes in as CSV/JSON
    ↓
Convert to Parquet with Snappy compression
    ↓
Store in S3 with partitioning
    ↓
Query with Athena or Redshift Spectrum
    ↓
Fast + Cheap ✅
```

---

## Key Takeaway

> For analytics: Parquet. For streaming: Avro or JSON. For quick sharing: CSV. Always convert raw data to Parquet before storing in your data lake for best performance and cost.

---

**Previous:** [Data Compression](./10-Data-Compression.md)
**Next:** [Section 04 — Amazon S3](../04-Amazon-S3/01-What-is-S3.md)
