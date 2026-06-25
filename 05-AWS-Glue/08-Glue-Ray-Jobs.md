# Glue Ray Jobs

## What is a Glue Ray Job?

A **Glue Ray job** uses the **Ray** framework to run distributed Python. It's designed for workloads that need parallelism but don't fit the Spark model well.

---

## When to Use Ray

- **Machine learning** data preprocessing
- Workloads using **pure Python libraries** (pandas, numpy) at scale
- Tasks that benefit from distributed Python but not Spark

---

## Ray vs Spark vs Python Shell

| Feature | Python Shell | Spark | Ray |
|---------|-------------|-------|-----|
| Scale | Single machine | Distributed | Distributed |
| Language | Python | PySpark/Scala | Python |
| Libraries | Any Python | Spark APIs | Any Python |
| Best for | Small tasks | Big data ETL | ML prep, parallel Python |

---

## For the Exam

Ray jobs are less commonly tested. Focus more on **Spark** and **Python Shell**. If you see "distributed Python without Spark" → think Ray.

---

## Key Takeaway

> Glue Ray jobs run distributed Python using the Ray framework. Best for ML workloads and parallel Python tasks. Less common on the exam than Spark.

---

**Previous:** [Glue Python Shell Jobs](./07-Glue-Python-Shell-Jobs.md)
**Next:** [Glue DynamicFrames](./09-Glue-DynamicFrames.md)
