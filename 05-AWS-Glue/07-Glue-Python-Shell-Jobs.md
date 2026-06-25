# Glue Python Shell Jobs

## What is a Python Shell Job?

A **Python Shell job** runs plain Python scripts (no Spark). It's designed for **small, lightweight tasks** that don't need distributed processing.

---

## Comparison with Spark Jobs

| Feature | Python Shell | Spark |
|---------|-------------|-------|
| **Engine** | Plain Python | Apache Spark |
| **Scale** | Single machine | Distributed cluster |
| **DPU** | 1 DPU max (or 0.0625 DPU) | 2+ DPUs |
| **Cost** | Very cheap | More expensive |
| **Best for** | Small tasks | Large data processing |

---

## When to Use Python Shell

- Making **API calls** to external services
- Processing **small files** (< few hundred MB)
- Running **database queries**
- Sending **notifications**
- Simple **data validation** checks
- Tasks that don't need Spark's distributed power

---

## When NOT to Use

- ❌ Processing large datasets (GBs/TBs)
- ❌ Complex transformations at scale
- ❌ Anything that needs parallel processing

---

## Key Takeaway

> Python Shell jobs are cheap, lightweight Glue jobs for small tasks. Use 1 DPU max. Great for API calls, small scripts, and notifications. Use Spark jobs for big data processing.

---

**Previous:** [Glue Spark Jobs](./06-Glue-Spark-Jobs.md)
**Next:** [Glue Ray Jobs](./08-Glue-Ray-Jobs.md)
