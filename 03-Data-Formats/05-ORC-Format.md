# ORC Format

## What is ORC?

**ORC (Optimized Row Columnar)** is a columnar storage format, similar to Parquet. It was originally created for **Apache Hive** (Hadoop ecosystem).

---

## ORC vs Parquet

| Feature | ORC | Parquet |
|---------|-----|---------|
| Created by | Apache Hive (Hortonworks) | Twitter + Cloudera |
| Best with | Hive, EMR | Athena, Glue, Spark |
| Compression | ZLIB, Snappy | Snappy, GZIP, Zstd |
| Nested data | Basic support | Better support |
| AWS preference | Works but less common | ⭐ Preferred |

---

## When to Use ORC

- You're using **Apache Hive** on **EMR**
- Legacy systems that already use ORC
- Some Redshift operations work well with ORC

---

## When to Use Parquet Instead

- **Most AWS services** prefer Parquet
- Athena, Glue, and Spark work better with Parquet
- Parquet has wider community support

---

## For the Exam

- If the question mentions **Hive** → ORC might be the answer
- For everything else → **Parquet** is usually the preferred answer
- Both are columnar and much better than CSV/JSON

---

## Key Takeaway

> ORC is a columnar format like Parquet, mainly used with Hive on EMR. For most AWS data engineering tasks, Parquet is preferred. Both are excellent for analytics.

---

**Previous:** [Parquet Format](./04-Parquet-Format.md)
**Next:** [Avro Format](./06-Avro-Format.md)
