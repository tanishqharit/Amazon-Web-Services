# Row vs Columnar Formats

## The Core Difference

**Row-based:** Stores all values of a row together.
**Columnar:** Stores all values of a column together.

---

## Visual Example

Data:
```
| Name    | Age | City    |
|---------|-----|---------|
| Tanishq | 25  | Delhi   |
| Priya   | 30  | Mumbai  |
```

**Row-based storage (CSV, JSON, Avro):**
```
Tanishq, 25, Delhi, Priya, 30, Mumbai
```

**Columnar storage (Parquet, ORC):**
```
Tanishq, Priya | 25, 30 | Delhi, Mumbai
```

---

## Why This Matters

Query: `SELECT AVG(age) FROM people`

**Row-based:** Must read ALL data (name, age, city) for every row → slow
**Columnar:** Only reads the "age" column → fast!

---

## Comparison

| Feature | Row-based | Columnar |
|---------|-----------|----------|
| **Read entire row** | ✅ Fast | ❌ Slow |
| **Read specific columns** | ❌ Slow | ✅ Fast |
| **Writing data** | ✅ Fast | ❌ Slower |
| **Compression** | Less effective | Very effective (same data type) |
| **Best for** | Transactions (OLTP) | Analytics (OLAP) |
| **Formats** | CSV, JSON, Avro | Parquet, ORC |

---

## Why Columnar Compresses Better

All values in a column have the **same data type**:
- Ages: `25, 30, 28, 25, 30, 25` → very compressible
- Names: `Tanishq, Priya, Rahul` → somewhat compressible

Row data has **mixed types** → harder to compress.

---

## Key Takeaway

> Row-based = good for writing and reading full records. Columnar = good for analytics and reading specific columns. For data engineering on AWS, columnar (Parquet) is almost always preferred.

---

**Previous:** [Avro Format](./06-Avro-Format.md)
**Next:** [Schema on Read](./08-Schema-on-Read.md)
