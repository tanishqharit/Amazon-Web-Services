# Batch Processing

## What is Batch Processing?

**Batch processing** means collecting data over a period of time and processing it **all at once**.

Think of it like doing laundry:
- You don't wash each shirt the moment it gets dirty
- You collect shirts all week, then wash them all together on Sunday
- That's batch processing!

---

## How It Works

```
Collect data → Wait → Process all data at once → Output
   (hours)     (wait)      (scheduled run)
```

---

## Characteristics

| Feature | Batch Processing |
|---------|-----------------|
| **When** | On a schedule (hourly, daily, weekly) |
| **Data volume** | Large (process lots of data at once) |
| **Latency** | High (minutes to hours delay) |
| **Complexity** | Simpler to build |
| **Cost** | Often cheaper (run when needed) |

---

## Real Examples

1. **Daily sales report** — process all of yesterday's sales at midnight
2. **Monthly billing** — calculate all customer bills at end of month
3. **Data warehouse refresh** — load new data into Redshift every night

---

## AWS Services for Batch Processing

| Service | How it's used |
|---------|--------------|
| **AWS Glue** | Scheduled ETL jobs |
| **Amazon EMR** | Large-scale Spark batch jobs |
| **AWS Batch** | Run batch computing workloads |
| **AWS Lambda** | Small, triggered batch tasks |

---

## Key Takeaway

> Batch processing collects data over time and processes it all at once on a schedule. It's great for large volumes of data where real-time results are not needed.

---

**Previous:** [ETL vs ELT](./07-ETL-vs-ELT.md)
**Next:** [Stream Processing](./09-Stream-Processing.md)
