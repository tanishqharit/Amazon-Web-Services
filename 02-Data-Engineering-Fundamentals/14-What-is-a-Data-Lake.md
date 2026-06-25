# What is a Data Lake?

## Simple Explanation

A **data lake** is a **centralized storage** that holds a massive amount of raw data in its **original format** — structured, semi-structured, and unstructured.

Think of it like a real lake:
- A lake collects water from rivers, rain, and streams
- The water stays in its natural form
- You can use it for swimming, drinking (after filtering), or fishing

A data lake collects all kinds of data, stores it raw, and lets you process it later.

---

## Key Characteristics

| Feature | Data Lake |
|---------|-----------|
| **Data format** | Any format (CSV, JSON, Parquet, images, logs) |
| **Schema** | Schema-on-read (define structure when reading) |
| **Storage cost** | Very low (uses object storage like S3) |
| **Users** | Data engineers, data scientists, analysts |
| **Processing** | Transform data as needed, when needed |

---

## Data Lake on AWS

On AWS, a data lake is built using **Amazon S3**.

```
Data Lake (S3)
├── raw/          ← Raw data as received
├── processed/    ← Cleaned and transformed data
└── curated/      ← Final, ready-for-analysis data
```

---

## Benefits

- ✅ Store **everything** — don't throw away any data
- ✅ Very **cheap** storage (S3 costs ~$0.023/GB/month)
- ✅ **Flexible** — process data however you need later
- ✅ Supports all data types

---

## Risks

- ❌ Can become a **"data swamp"** if not organized
- ❌ No enforced structure → data quality issues
- ❌ Needs governance tools (like Lake Formation)

---

## Key Takeaway

> A data lake stores all raw data in its original format using cheap storage (S3). It's flexible but needs proper organization and governance to stay useful.

---

**Previous:** [Unstructured Data](./13-Unstructured-Data.md)
**Next:** [What is a Data Warehouse](./15-What-is-a-Data-Warehouse.md)
