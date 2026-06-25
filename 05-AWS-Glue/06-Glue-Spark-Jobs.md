# Glue Spark Jobs

## What is a Glue Spark Job?

A Glue Spark job uses **Apache Spark** to process large datasets in a distributed way. Spark splits data across multiple workers and processes it in parallel.

---

## DPU (Data Processing Units)

A **DPU** is a unit of computing power in Glue:

| Worker Type | vCPUs | Memory | Use Case |
|-------------|-------|--------|----------|
| **Standard** | 4 | 16 GB | General ETL |
| **G.1X** | 4 | 16 GB | Memory-intensive |
| **G.2X** | 8 | 32 GB | Very memory-intensive, ML |
| **G.025X** | 2 | 4 GB | Small jobs |

- Minimum: **2 DPUs** for Spark jobs
- You pay per DPU per hour (billed per second)

---

## Glue Versions

| Version | Spark Version | Notes |
|---------|--------------|-------|
| Glue 2.0 | Spark 2.4 | Faster startup |
| Glue 3.0 | Spark 3.1 | Performance improvements |
| **Glue 4.0** | **Spark 3.3** | Latest, recommended ⭐ |

Always use the latest version for better performance and features.

---

## Job Parameters

| Parameter | What it controls |
|-----------|-----------------|
| **Number of workers** | How many compute units to use |
| **Worker type** | G.1X, G.2X, Standard |
| **Timeout** | Max runtime before job is killed |
| **Max retries** | How many times to retry on failure |
| **Job bookmark** | Track what's already processed |

---

## Key Takeaway

> Glue Spark jobs process large data using distributed Spark. Choose worker type based on memory needs. Use Glue 4.0 for best performance. Pay per DPU-hour.

---

**Previous:** [Glue ETL Jobs Overview](./05-Glue-ETL-Jobs-Overview.md)
**Next:** [Glue Python Shell Jobs](./07-Glue-Python-Shell-Jobs.md)
